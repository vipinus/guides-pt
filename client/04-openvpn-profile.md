# 04 · OpenVPN: baixe o perfil .ovpn, importe e conecte; funciona em roteadores, NAS e Linux

> Versão no site (mais completa): https://www.leotun.com/pt/guides/openvpn-setup?utm_source=github&utm_content=client-04

O OpenVPN é um protocolo de código aberto consagrado, e quase todo sistema operacional, firmware de roteador e NAS já vem com um cliente para ele. Os arquivos de perfil da LeoTun já trazem sua conta, sua senha e as chaves de criptografia, então é só importar e conectar. Para o dia a dia no celular e no computador, AnyConnect ou Hiddify dão menos trabalho; o valor do OpenVPN está nos **lugares que só aceitam OpenVPN**: roteadores OpenWrt, NAS Synology / QNAP, servidores Linux e aparelhos mais antigos.

## Três passos

1. Na tabela da [página do OpenVPN no site](https://www.leotun.com/pt/openvpn?utm_source=github&utm_content=client-04), instale o cliente do seu sistema (todas as plataformas têm o OpenVPN Connect oficial; no Windows também dá para usar o OpenVPN GUI, e no macOS o Tunnelblick).
2. Depois de entrar na conta, **clique na bandeira de uma região** para baixar o .ovpn dela. Um arquivo por região.
3. Abra o arquivo no cliente e conecte.

| Plataforma | Observações |
|---|---|
| Windows / macOS / Android / iOS | O perfil já vem com conta e senha; importe e conecte |
| Linux | Configurações de VPN do sistema → importar de arquivo, e na primeira conexão digite o e-mail e a senha do site; pela linha de comando `openvpn --config file`; para iniciar com o sistema, coloque em `/etc/openvpn/client/` |
| Roteador OpenWrt | Instale o luci-app-openvpn, envie o .ovpn e ative; não é necessário se o firmware deste site já estiver instalado |
| NAS Synology | Painel de Controle → Rede → Interface de Rede → Criar → VPN → OpenVPN (importe o .ovpn); para mandar o tráfego de saída do NAS pela linha, marque "Usar gateway padrão na rede remota" |
| NAS QNAP | QVPN → VPN Client → Add → OpenVPN, importe |

## Usuários na China: conexão direta com sites chineses

Depois de conectar, o tráfego para sites chineses faz um desvio. O site oferece uma "ferramenta de rota direta para a China": dê dois cliques para executar, e os IPs chineses passam a conectar direto enquanto todo o resto vai pela linha. Funciona com Cisco e com OpenVPN. Quem está fora da China não deve usar.

## Se não conectar, verifique nesta ordem

| Palavra-chave no log / sintoma | Causa | O que fazer |
|---|---|---|
| AUTH_FAILED | Conta ou senha erradas, ou vencida | Entre no site e confira a data de vencimento; se você mudou a senha, baixe o perfil de novo |
| UDP dá timeout primeiro e depois conecta por TCP | A rede atual restringe UDP, e ele caiu para TCP automaticamente | Funciona, mas mais lento; se ficar lento demais, troque de rede ou use o AnyConnect |
| UDP e TCP mostram TLS handshake failed / key negotiation failed | O caminho de rede até o servidor está fora | Troque de região ou de rede |
| Erro ao importar | Cliente antigo demais (anterior ao OpenVPN 2.5) | Atualize o cliente |
| Cai de repente durante a conexão | A conta venceu e o servidor desconectou você | Renove e reconecte; não precisa trocar o perfil |

## UDP ou TCP

Os dois estão disponíveis e você não precisa escolher. O UDP vem primeiro no perfil, então o cliente tenta UDP antes; se o UDP estiver restrito ou não conectar, ele passa sozinho para TCP depois de alguns segundos. O UDP tem latência menor e é mais rápido; o TCP é só um plano B e fica bem mais lento em conexões internacionais. Em redes que restringem UDP permanentemente (algumas redes de universidades e empresas), recomendamos usar direto o AnyConnect.

> Perfis baixados antes de 15 de setembro de 2026 só têm UDP; baixe de novo se quiser a troca automática.

## Segurança

O arquivo de perfil contém sua conta e sua senha, então vale tanto quanto a própria conta: não passe adiante; se vazar, mude a senha no site e o arquivo antigo para de funcionar na hora. O próprio handshake também é criptografado: sem a chave do perfil, não dá nem para começar um handshake, e o servidor fica invisível para scanners.

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=client-04) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=client-04) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 24 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, oferta permanente
