# 05 · Rede privada (Tailscale): instalar, entrar no servidor de controle deste site e escolher uma saída

> Versão no site (mais completa): https://www.leotun.com/pt/guides/tailscale-mesh?utm_source=github&utm_content=client-05

A seção Rede privada usa o Tailscale (uma ferramenta de rede feita sobre o WireGuard). A LeoTun mantém um servidor de controle próprio, e você entra com **a sua conta deste site**, que não tem nada a ver com uma conta oficial do Tailscale. Entre uma vez e o aparelho fica on-line; a região de saída pode ser trocada pelo menu a qualquer momento. Para saber como ela difere de uma VPN e para quem serve, veja o [Guia de rede 03](../network/03-private-network-vs-vpn.md).

## Instalação

| Plataforma | Onde baixar |
|---|---|
| Windows / macOS / Linux / Android | A área de download da [página da Rede privada no site](https://www.leotun.com/pt/mesh?utm_source=github&utm_content=client-05) (baixada direto deste site, sem precisar ir ao site oficial) |
| iPhone / iPad | App Store; exige um ID Apple de fora da região China (veja o [Guia de aplicativos 06](06-ios-app-store.md)) |

## Como entrar

1. **Saia antes da conta oficial** (se você já entrou alguma vez): no celular, toque no seu avatar → Log Out (sair); no computador, rode `tailscale logout`. Se você não sair por completo, a opção do passo seguinte não aparece.
2. **Aponte o login para este site**:
   - Celular: na tela sem login, toque em "⋯" no canto superior direito → Use custom server (usar servidor personalizado; em algumas versões aparece como Use an alternate server), digite o endereço que aparece na página da Rede privada do site e toque em Log in (entrar).
   - Windows / Linux: copie o comando `tailscale up --login-server=…` da página do site e rode no PowerShell / no terminal.
   - macOS: **não clique em Log in**. Na janela do Tailscale, clique na seta da linha da conta → Account Settings… → Accounts → a setinha ao lado de "Add Account…" → Add Account Using Alternate Server (adicionar conta usando outro servidor), cole o endereço e clique em Add Account….
3. O navegador abre sozinho a página de login deste site; confirme com a sua conta deste site. Quando você voltar ao cliente, ele já estará on-line.

## Escolher uma saída

- Celular: menu → Exit Node (nó de saída), escolha uma região; vale na hora.
- Computador: ícone na bandeja / na barra de menus → submenu Exit Node; ou `tailscale set --exit-node=<region-name>` (`tailscale exit-node list` mostra as opções disponíveis).
- Para não usar saída nenhuma, escolha None (nenhuma) (na linha de comando, deixe vazio o valor depois do sinal de igual). Só uma saída pode ser usada por vez.

## Vencimento e número de aparelhos

- A validade do login de cada aparelho acompanha o vencimento da conta, e ele fica off-line poucos minutos depois do vencimento; depois de renovar, é só entrar mais uma vez. Não precisa reinstalar.
- O número de aparelhos on-line ao mesmo tempo depende do seu plano (Individual 2, Família 4, Empresa 8), e a cota é dividida com as outras formas de conexão; se passar do limite do seu plano, você pode subir de plano temporariamente (o tempo restante é convertido pelo valor equivalente) e voltar quando terminar.

## Dois casos em que outra forma serve melhor

- Com outra VPN rodando no mesmo aparelho (um AnyConnect da empresa, outro software de rede mesh): elas brigam por DNS e rotas. É por isso que aparecem avisos de direitos autorais ao ver vídeos chineses e que a intranet da empresa não abre.
- Numa rede de universidade / de empresa que restringe UDP: o WireGuard roda sobre UDP, então só consegue passar pelos relays do Tailscale, o que fica muito lento; troque para o AnyConnect.

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=client-05) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=client-05) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 24 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, oferta permanente
