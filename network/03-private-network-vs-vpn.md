# 03 · Rede privada (Tailscale) x VPN: qual a diferença e quando usar

> Versão no site (mais completa): https://www.leotun.com/pt/guides/tailscale-mesh?utm_source=github&utm_content=network-03

A seção Rede privada usa o Tailscale, uma ferramenta de rede baseada no WireGuard. A LeoTun roda o próprio servidor de controle, e você entra com a sua conta deste site. Não é a mesma coisa que as VPNs "de conexão", como AnyConnect e OpenVPN.

## Três diferenças

| | VPN de conexão (AnyConnect / OpenVPN / Hiddify) | Rede privada (Tailscale) |
|---|---|---|
| Conexão | Você toca em conectar toda vez e reconecta quando cai | Entra uma vez e fica on-line; volta sozinha quando você troca de rede |
| Saída | Depois de conectar, todo o tráfego passa pela saída | A saída é opcional: sem saída escolhida, o tráfego da internet sai pela sua própria rede e só o tráfego entre os aparelhos da Rede privada é criptografado; só quando você escolhe a saída de uma região ela passa a funcionar como uma VPN |
| Acesso entre aparelhos | Não tem | Celulares, computadores e NAS da mesma conta se acessam direto, sem redirecionamento de portas nem IP público |

## Quando usar

- Você tem vários aparelhos e quer configurar uma vez e deixar sempre on-line.
- Você tem em casa um NAS, um computador ou uma câmera que quer acessar de fora: entre na Rede privada dos dois lados e conecte direto pelo nome do aparelho, como se estivessem na mesma rede local.
- Aparelhos que precisam ficar conectados por muito tempo: não há tempo limite de sessão.

## Quando outra forma serve melhor

- Você só quer usar uma vez, de forma temporária: importar o Hiddify por QR code ou instalar o AnyConnect é mais rápido.
- O aparelho já está rodando a VPN da empresa ou outro software de rede: os dois brigam por DNS e rotas, e os sintomas são aviso de direitos autorais ao assistir vídeos chineses e a intranet da empresa sem abrir. Use uma forma que afete só o navegador, como o Proxy Web.
- Redes de universidade ou de empresa que restringem UDP: o WireGuard roda sobre UDP e aí só consegue passar por retransmissão, que é lenta; mude para o AnyConnect.

## Vencimento e número de aparelhos

O login de cada aparelho segue a data de vencimento da conta; ele fica off-line poucos minutos depois do vencimento, e depois de renovar basta entrar de novo. O número de aparelhos on-line ao mesmo tempo depende do plano (Individual 2, Família 4, Empresa 8) e a cota é dividida com as outras formas de conexão; se passar do limite do plano, você pode subir de plano temporariamente (o tempo restante é convertido pelo valor equivalente) e voltar quando terminar.

Para os passos de instalação e login, veja o [Guia de aplicativos 05](../client/05-tailscale-private-network.md).

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=network-03) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=network-03) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 15 créditos (cerca de 15 dias do plano Individual), oferta permanente
