# 10 · O que fazer quando o Dropbox e outros programas pedem um proxy HTTP / SOCKS

> Versão no site (mais completa): https://www.leotun.com/pt/guides/app-proxy?utm_source=github&utm_content=client-10

**Primeiro, como as coisas são: o proxy precisa ser criptografado.** Proxies sem criptografia (HTTP simples, SOCKS4, SOCKS5) são identificados e sofrem interferência nas redes da China; em pouco tempo a conexão fica lenta ou cai, e a conta e a senha ainda trafegam em texto aberto. Só conexões criptografadas continuam funcionando a longo prazo, por isso o Proxy Web deste site usa conexão criptografada em tudo; **para programas que só aceitam HTTP / SOCKS5, deixe o Hiddify assumir o computador inteiro** (veja abaixo).

Programas independentes como Dropbox, Telegram Desktop, Steam, clientes de armazenamento em nuvem e ferramentas de desenvolvimento não leem as configurações do navegador, e as próprias configurações de proxy deles só aceitam HTTP / SOCKS5 sem criptografia. Os dois lados não se encaixam, então digitar um proxy não faz conectar. A solução é **não digitar proxy nenhum**: use o Hiddify para mandar o computador inteiro pela linha e deixe o proxy do programa em "Sem proxy".

## Por que continua sem conectar depois de digitar um proxy

| Causa | Explicação |
|---|---|
| Tipo incompatível | O programa só oferece HTTP, SOCKS4 e SOCKS5, nenhum criptografado; o proxy deste site precisa ser criptografado e não dá para digitá-lo ali |
| Um proxy sem criptografia achado na internet | Conecta por um tempo, depois sofre interferência e só funciona de vez em quando |
| Cobre só parte do tráfego | Em muitos programas só o login e a sincronização usam o proxy, enquanto atualizações, chamadas e sincronização pela rede local continuam conectando direto; um proxy HTTP nem encaminha o tráfego UDP de jogos e chamadas |
| Configurado separadamente em cada programa | Mudar de região ou de senha obriga a mudar um por um, e o que você esquecer para de funcionar |

## Jeito recomendado: deixe o Hiddify assumir o computador inteiro

1. Instale o Hiddify seguindo o [09 · Instalar o Hiddify em todas as plataformas](09-hiddify-install-all-platforms.md) e importe um perfil seguindo o [02](02-singbox-subscription-links.md).
2. Conecte no modo "VPN" (o padrão). No Windows, a primeira conexão pede permissão de administrador.
3. Volte o proxy do programa para "Sem proxy": no Dropbox, escolha "Sem proxy" (No proxy) ou "Detectar automaticamente" (Auto-detect) em "Preferências → Rede → Proxies"; no Telegram Desktop, escolha "Desativar proxy" (Disable proxy) em "Configurações → Avançado → Tipo de conexão". Em qualquer outro programa com opção de proxy, desligue.
4. Confira: o ícone do Dropbox na bandeja mostra "Atualizado" (Up to date) e a sincronização começa; abra no navegador uma página que mostre o seu IP, e a saída está na região escolhida.

Com o "roteamento automático" ligado, serviços estrangeiros como o Dropbox passam pela linha, enquanto WeChat, internet banking e sites chineses conectam direto, como sempre.

## Programas comuns

| Programa | Como configurar |
|---|---|
| Dropbox | Proxy em "Sem proxy" ou "Detectar automaticamente"; se ficar em "Manual" com algum outro endereço, ele fica off-line quando o Hiddify é desligado |
| Telegram Desktop | Tipo de conexão "Desativar proxy"; o MTProto / SOCKS5 embutido por cima do túnel só deixa mais lento |
| OneDrive, Google Drive, iCloud para computador | Seguem a rede do sistema; nada a configurar |
| Steam, Epic, Battle.net | Não precisam de proxy; se o download estiver lento, mude para uma região mais próxima |
| Zoom, Teams, Slack, Discord | Voz e vídeo usam UDP, que só uma forma de computador inteiro transporta |
| VS Code, JetBrains, Cursor | Seguem a rede do sistema; apague qualquer proxy configurado à parte dentro da ferramenta |

## Quando não dá para instalar um cliente (computador da empresa)

- Use a versão web do Dropbox e dos serviços de nuvem: abra dropbox.com num navegador com o [Proxy Web](03-web-proxy-extension.md); dá para enviar e baixar arquivos, mas sem sincronização automática.
- Ferramentas de linha de comando (git, pip, npm, curl) aceitam proxy criptografado: coloque o endereço do Proxy Web em `https_proxy`; veja [Acessar serviços de fora a partir da China 05 · Linux e linha de comando](https://github.com/vipinus/guides-zh-CN/blob/main/overseas-access/05-linux-server.md) (em chinês).
- Outros programas de computador que só aceitam HTTP / SOCKS5 é melhor usar no seu próprio computador ou celular; não instale uma VPN de computador inteiro na máquina da empresa por causa disso, porque vai disparar os alertas de segurança da empresa.

## Perguntas frequentes

**Vocês podem me dar um endereço de proxy SOCKS5 ou HTTP?** O proxy deste site usa conexão criptografada em tudo; um sem criptografia logo passa a funcionar só de vez em quando. Deixar o Hiddify assumir o computador inteiro é mais estável e cobre todos os programas de uma vez.

**Com o Hiddify ligado, ainda preciso digitar um proxy no programa?** Não. Digitar um significa dar duas voltas: na melhor das hipóteses fica mais lento, na pior não conecta.

**E o Dropbox no celular?** Apps de celular não têm configuração de proxy. Instale o Hiddify ou use o Cisco (AnyConnect); depois de conectar, todos os apps passam pela linha.

**Dá para ficar sem o Hiddify?** Dá. Cisco, Rede privada e OpenVPN também assumem o computador inteiro, e o programa fica igualmente em "Sem proxy". A vantagem do Hiddify é o roteamento embutido e a velocidade melhor em redes com muita perda de pacotes.

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=client-10) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=client-10) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 15 créditos (cerca de 15 dias do plano Individual), oferta permanente
