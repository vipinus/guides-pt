# 05 · Como mandar um servidor Linux e ferramentas de linha de comando pela linha

No Linux há dois caminhos até a linha; escolha conforme a necessidade. Para mandar a máquina inteira por ela (baixar imagens do Docker, rodar serviços que precisam de rede de fora da China, operação sem supervisão), use o OpenVPN: um arquivo de configuração colocado em /etc/openvpn/client/ e iniciado com o sistema. Para mandar só alguns comandos (git, pip, npm, curl), use o Proxy Web: coloque o endereço do proxy na variável de ambiente http_proxy e o resto do tráfego fica como está. No Linux de desktop também dá para importar no NetworkManager. Este artigo cobre os três, com como escrever o arquivo de senha e os comandos para conferir.

## Caminho 1: a máquina inteira pela linha (OpenVPN)

1. Instale o cliente: Debian / Ubuntu sudo apt install openvpn, Fedora sudo dnf install openvpn, Arch sudo pacman -S openvpn.
2. Entre neste site e, na página do OpenVPN, clique na bandeira de uma região para baixar o .ovpn. A configuração que o Linux recebe não traz conta e senha embutidas (o NetworkManager não aceita arquivos com credenciais embutidas), então crie um arquivo de senha à parte: duas linhas, a primeira com o seu e-mail deste site e a segunda com a sua senha, chmod 600.
3. Copie o .ovpn para /etc/openvpn/client/<região>.conf e, no arquivo, acrescente o caminho do arquivo de senha depois de auth-user-pass.
4. sudo systemctl enable --now openvpn-client@<região>. Veja o status com systemctl status openvpn-client@<região> e confira se curl -s https://ipinfo.io/country mostra a região escolhida.
5. Para mudar de região, baixe outra configuração e ative outra unidade; rode só uma de cada vez.

## Caminho 2: só as ferramentas de linha de comando pela linha (Proxy Web)

O endereço de proxy mostrado na página do Proxy deste site, junto com sua conta e senha, pode ir direto para as variáveis de ambiente: export https_proxy=https://usuario:senha@endereco-do-proxy export http_proxy=$https_proxy. Caracteres especiais na senha precisam ser codificados para URL. Depois disso, curl, wget, git, pip e npm passam pela linha neste terminal, e os outros programas não são afetados.

O daemon do Docker não lê as variáveis de ambiente do shell; escreva em Environment= no /etc/systemd/system/docker.service.d/proxy.conf e reinicie o docker. Para o apt, escreva Acquire::https::Proxy em /etc/apt/apt.conf.d/proxy.conf.

Neste caminho, por design não há conexão para cair; não precisa de root e não muda rotas. Serve para servidores da empresa e para quando você só quer acelerar downloads; vale só para programas que respeitam as variáveis de proxy, e o resto do tráfego fica como está.

## Caminho 3: NetworkManager no Linux de desktop

1. Instale o network-manager-openvpn-gnome (um clique na página do OpenVPN deste site pode abrir a central de programas).
2. Configurações → Rede → VPN → "+" → Importar de arquivo, escolha o .ovpn, digite o e-mail e a senha deste site e salve.
3. Ligue e desligue a VPN pela barra superior ou pela bandeja. Para conectar automaticamente ao iniciar, marque "Conectar automaticamente à VPN" nas configurações da conexão com fio/sem fio.

## Conferir e resolver problemas

- Confira a saída: o país em curl -s https://ipinfo.io é a região escolhida.
- Confira o DNS: em resolvectl status, o DNS da interface da VPN deve ser o enviado pela linha; se vazar, acrescente dhcp-option DNS à configuração ou use o script update-systemd-resolved.
- AUTH_FAILED: o arquivo de senha está errado ou a conta venceu; se você mudou a senha, atualize o arquivo de senha.
- Timeout no handshake TLS: o UDP até o servidor não está passando; troque de região ou de rede. Num servidor em nuvem, o grupo de segurança precisa liberar UDP de saída.
- O servidor está na China e as fontes chinesas devem conectar direto: com o OpenVPN conectado, todo o tráfego de saída passa pela linha. Troque as fontes do apt / pip / npm por espelhos chineses, ou use o caminho 2 para que só comandos específicos passem pela linha.

## Bom saber

- Uma máquina Linux conta como um aparelho e divide a cota de aparelhos on-line ao mesmo tempo com os seus outros aparelhos (Individual 2 aparelhos, Família 4 aparelhos, Empresa 8 aparelhos); o Proxy Web do caminho 2 é contado por conexão e também entra.
- O arquivo de configuração e o arquivo de senha valem tanto quanto a sua conta; não faça commit deles num repositório git nem coloque numa imagem.
- Quando você muda a senha, a configuração antiga para de funcionar na hora; é o mecanismo de revogação, de propósito. Basta atualizar o arquivo de senha.
- Ao rodar a linha num servidor em nuvem, siga os termos de uso do provedor; a linha registra só a duração da conexão e o tráfego total.

## Perguntas frequentes

**Por que a configuração do Linux não traz conta e senha embutidas?** Ao importar uma configuração, o NetworkManager não aceita arquivo com credenciais embutidas e acusa falha na importação, então a cópia entregue para Linux deixa você preencher; no método com systemd, escreva no arquivo de senha.

**Dá para mandar só o Docker pela linha?** Dá: configure as variáveis de proxy só para o daemon do Docker (caminho 2); ou rode um contêiner com OpenVPN dentro (gluetun) para que contêineres específicos passem pela linha.

**E a Rede privada (Tailscale) no Linux?** O script oficial instala com uma linha, e tailscale up --login-server=<servidor de controle deste site> faz o login. Serve para quando você precisa acessar esta máquina de fora, ou quer configurar uma vez e deixar sempre on-line; para só acelerar downloads, OpenVPN ou o proxy são mais simples.

**No OpenWrt de um roteador é igual?** No OpenWrt, instale o luci-app-openvpn e envie o .ovpn, e a rede local inteira passa pela linha; um roteador com o firmware deste site não precisa disso, basta entrar na sua conta.

## Leia também

- [Página do OpenVPN: downloads do cliente e arquivos de configuração](https://www.leotun.com/pt/openvpn?utm_source=github&utm_content=overseas-access-05)
- [Como usar o OpenVPN e quando escolhê-lo](https://www.leotun.com/pt/guides/openvpn-setup?utm_source=github&utm_content=overseas-access-05)
- [Como mandar um NAS Synology ou QNAP pela linha](https://www.leotun.com/pt/guides/nas-openvpn?utm_source=github&utm_content=overseas-access-05)
- [O que é o Proxy Web e quando usar](https://www.leotun.com/pt/guides/web-proxy?utm_source=github&utm_content=overseas-access-05)

Versão deste artigo no site: https://www.leotun.com/pt/guides/linux-server?utm_source=github&utm_content=overseas-access-05

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=overseas-access-05) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=overseas-access-05) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, válido por tempo indeterminado
