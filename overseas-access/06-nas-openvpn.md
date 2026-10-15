# 06 · Como mandar um NAS Synology ou QNAP pela linha

O NAS é o aparelho da casa que mais precisa da linha e que menos recebe atenção: o gerenciador de downloads precisa alcançar recursos de fora, o Docker precisa baixar imagens, o Cloud Sync precisa sincronizar nuvens de fora e o Plex precisa buscar metadados. Um NAS não roda o Hiddify, mas o Synology e o QNAP já vêm com um cliente OpenVPN: baixe um .ovpn na página OpenVPN deste site, importe e ele conecta, e reconecta sozinho quando o NAS liga. Este artigo mostra onde fica a importação no Synology e no QNAP, a opção-chave "Use default gateway" (usar como gateway padrão), o que fazer depois de trocar a senha e por que "acessar o NAS de fora" é outra história, que pede a Rede privada.

## Primeiro, separe duas coisas

Mandar o próprio NAS pela linha (downloads, imagens do Docker, sincronizar nuvens de fora): use o OpenVPN, que é o assunto deste artigo.

Acessar o NAS de fora (abrir pastas compartilhadas numa viagem, ver câmeras): use a Rede privada (Tailscale), que coloca o NAS e o seu celular na mesma rede privada; veja "Ver câmeras e NAS de casa na China estando no exterior". Deixe esse trabalho para a Rede privada: o OpenVPN liga o NAS à nossa linha, e a Rede privada liga você à sua casa.

## Synology

1. Entre neste site e, na página OpenVPN, clique na bandeira de uma região para baixar o arquivo .ovpn dela.
2. Control Panel (Painel de controle) → Network (Rede) → Network Interface (Interface de rede) → Create (Criar) → Create VPN profile (Criar perfil de VPN) → OpenVPN (via importing a .ovpn file, importando um arquivo .ovpn), e digite o e-mail e a senha da sua conta deste site.
3. "Use default gateway" (usar como gateway padrão): marcada, todo o tráfego de saída do NAS passa pela linha (downloads, Docker e Cloud Sync se beneficiam); desmarcada, ele só abre o túnel e o tráfego de saída continua saindo pela sua rede. Na grande maioria dos casos, deixe marcada.
4. Marque "Reconnect when the VPN connection is lost" (reconectar quando a conexão VPN cair) para que ele volte sozinho depois que o NAS reiniciar ou a linha oscilar. Conecte e faça um download de teste num pacote.

## QNAP

1. Baixe o .ovpn do mesmo jeito.
2. QVPN Service → VPN Client (cliente VPN) → Add (Adicionar) → OpenVPN, importe o arquivo e digite a conta e a senha.
3. Nas configurações da conexão, marque "Use VPN as the default gateway of the NAS" (usar a VPN como gateway padrão do NAS) e a reconexão automática, e conecte.

## Que tráfego passa e qual não passa

- Passa: tarefas BT e HTTP no Download Station / Download Station, downloads de imagens do Docker, Cloud Sync sincronizando Google Drive / Dropbox / OneDrive, busca de metadados do Plex e do Emby e atualizações da Central de Pacotes.
- Não passa: o tráfego de quando você acessa o NAS na rede local; ele já está dentro da rede local e não é afetado.
- Você está na China e quer que os sites chineses conectem direto: o NAS não tem script de roteamento dividido, e depois que o OpenVPN conecta, todo o tráfego de saída do NAS passa pela linha. Se as fontes de download chinesas ficarem lentas, use endereços de espelhos chineses nas tarefas de download, ou conecte na linha só quando precisar.

## O que você precisa saber

- O arquivo de configuração leva os dados da sua conta, e o campo de senha no NAS deixa de funcionar depois que você troca a senha: baixe o .ovpn de novo e substitua, ou mude só a senha no perfil de VPN.
- Quando a conta vence, o NAS é desconectado; depois de renovar, ele reconecta sozinho, e a configuração não precisa ser trocada.
- O NAS conta como um aparelho e divide a cota de aparelhos on-line ao mesmo tempo com os seus outros aparelhos (Individual 2, Família 4, Empresa 8).
- A linha roda sobre UDP; um NAS numa internet doméstica quase nunca esbarra em restrição de UDP.

## Perguntas frequentes

**Depois de marcar "Use default gateway", o NAS continua acessível na rede local?** Continua. O tráfego da rede local não passa pelo gateway; pastas compartilhadas, reprodução no Plex e a página de administração não são afetadas.

**O acesso remoto ao Plex ficou mais lento depois que o NAS passou pela linha?** O acesso remoto do Plex usa o tráfego de saída do NAS, então, com o gateway padrão marcado, ele faz um desvio pela linha. Para assistir de fora, acessar o NAS pela Rede privada é mais direto; ou conecte o OpenVPN só quando precisar baixar.

**Dá para mandar só o Download Station pela linha?** O Synology e o QNAP não têm roteamento dividido por app. Para um controle mais fino, rode no Docker um contêiner de download com OpenVPN (como qbittorrent + gluetun) e mande só ele pela linha.

**E um NAS com sistema Linux (TrueNAS, Unraid)?** Faça do jeito do Linux: o pacote openvpn mais um arquivo de configuração em /etc/openvpn/client/; veja "Como mandar um servidor Linux e ferramentas de linha de comando pela linha".

## Leia também

- [Página OpenVPN: downloads do aplicativo e arquivos de configuração](https://www.leotun.com/pt/openvpn?utm_source=github&utm_content=overseas-access-06)
- [Como usar o OpenVPN e quando escolhê-lo](https://www.leotun.com/pt/guides/openvpn-setup?utm_source=github&utm_content=overseas-access-06)
- [Ver câmeras e NAS de casa na China estando no exterior](https://www.leotun.com/pt/guides/home-camera?utm_source=github&utm_content=overseas-access-06)
- [Como mandar um servidor Linux e ferramentas de linha de comando pela linha](https://www.leotun.com/pt/guides/linux-server?utm_source=github&utm_content=overseas-access-06)

Versão deste artigo no site: https://www.leotun.com/pt/guides/nas-openvpn?utm_source=github&utm_content=overseas-access-06

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=overseas-access-06) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=overseas-access-06) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 24 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, oferta permanente
