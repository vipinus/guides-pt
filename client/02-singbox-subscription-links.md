# 02 · Como importar um link de assinatura (Hiddify, Clash, Shadowrocket)

> Versão no site (mais completa): https://www.leotun.com/pt/guides/singbox-subscription?utm_source=github&utm_content=client-02

O "link de assinatura" que um provedor de linhas de proxy entrega é só um endereço HTTPS de onde o cliente baixa uma configuração completa: servidor, porta e credenciais estão todos lá, e nada precisa ser digitado à mão. A página do Hiddify da LeoTun entrega o mesmo tipo de coisa, e já em três formatos, então o Hiddify, o Clash e o Shadowrocket pegam cada um o seu e nada precisa ser convertido.

## Os três botões da janela

Entre no site → página do Hiddify → clique na bandeira de uma região. Aparece um QR code com três botões embaixo. Os botões são agrupados **por tipo de assinatura**, não por sistema operacional, então o celular e o computador mostram os mesmos:

| Clientes que aparecem no botão | Subtítulo | O que o clique copia |
|---|---|---|
| Hiddify / sing-box / GUI.for.SingBox / Karing | Assinatura sing-box | No celular, o link de importação `sing-box://import-remote-profile?url=…`, que abre o app; no computador, a URL de configuração `https://…` simples, para colar. A configuração já traz as regras de roteamento e uma regra que rejeita IPv6, então não precisa embrulhar num "modelo de assinatura" |
| Clash Meta / Clash Verge / FlClash / Stash / Mihomo Party / Clash Nyanpasu / ClashX Meta / OpenClash | Assinatura Clash | Uma URL de assinatura no formato do Clash (YAML), para colar na lista de assinaturas / perfis do cliente |
| NekoBox / Shadowrocket / v2rayN / v2rayNG / Streisand / V2Box / Loon / Egern / Husi / NekoRay / Pharos Pro / Bedlam / Furious / daed / Lumen KVN / Kitty Pro | Link de compartilhamento | Uma linha `hysteria2://…`, só com o nó, sem regras de roteamento |

- Quando os nomes não cabem numa linha, eles rolam em loop; é normal.
- **Clicar num botão também troca o QR code de cima para aquele tipo**, para o cliente correspondente escanear. Quando a janela abre, o QR code é o do Hiddify / sing-box, e outros clientes que escaneiam direto recebem "QR code inválido": clique primeiro no botão do seu cliente e depois escaneie ou cole.
- A janela "Importar todas as regiões · seleção automática", no topo da página, tem só os dois primeiros botões, sem o link de compartilhamento.

**Conversão de assinatura**: sites de terceiros que convertem um formato em outro. A LeoTun entrega os três formatos direto, então **não é preciso converter**; entregar a um site de conversão um link que contém as suas credenciais é o mesmo que entregar a sua conta a um estranho, então não faça isso.

## Família Hiddify / sing-box: o primeiro botão

1. Instale o Hiddify (Android: a página de downloads do site ou o Google Play; iOS: App Store; o app de computador cobre Windows / macOS / Linux). O núcleo sing-box já vem embutido.
2. Clique na bandeira de uma região, e o QR code aparece.
3. Celular: toque no primeiro botão e mude para o Hiddify, que vai oferecer adicionar a partir da área de transferência; ou use "Escanear QR code" no Hiddify de outro aparelho. Computador: clique no mesmo botão, que copia um endereço https://, depois no Hiddify vá em "+" → "Adicionar da área de transferência" e salve.
4. Toque em conectar e, na primeira vez, autorize a permissão de VPN. Para acrescentar uma região, clique em outra bandeira; cada região é um perfil separado.

## Família Clash: o segundo botão

Para Clash Meta (mihomo), Clash Verge, FlClash, Stash e afins, clique no botão "Assinatura Clash" e cole a URL copiada na lista de assinaturas / perfis do cliente. Não precisa de conversor de assinatura.

**Clientes da família Clash não devem usar o link de compartilhamento**: eles não conseguem importar uma única linha `hysteria2://` como perfil.

## Outros clientes: o terceiro botão

Clique no botão "Link de compartilhamento" e use "Importar da área de transferência" no NekoBox / Shadowrocket / v2rayN / v2rayNG e afins, ou escaneie o QR code de cima depois de clicar no botão. Um link de compartilhamento não traz regras, então você mesmo precisa configurar o roteamento e o IPv6: se está no exterior e quer ver conteúdo da China, mande os domínios chineses pelo nó e desligue o IPv6.

Os clientes listados depois do v2rayN no botão aceitam hysteria2, mas o link de compartilhamento usa um formato hysteria2 estendido que alguns clientes não conseguem ler; se a importação falhar ou não conectar, troque para o Hiddify.

## Clientes que não servem

| Cliente | Por quê |
|---|---|
| Surge | Aceita hysteria2, mas só lê o próprio formato de configuração, então nenhum dos três tipos serve |
| Quantumult X | Não aceita esse tipo de linha |
| O Clash original, Clash for Windows | O núcleo não tem hysteria2; use um cliente com núcleo mihomo |

## A assinatura expira?

- **Não expira com o tempo.** O token na URL da assinatura está ligado à sua conta e continua funcionando enquanto a conta for válida; renovar ou trocar de plano não exige importar de novo.
- **Trocar a senha invalida a URL antiga na hora.** É assim que você corta o acesso se perder o celular ou se um link vazar; depois de trocar, escaneie o código de novo.
- **Depois que a conta vence**, a URL retorna 401; quando você renovar, não precisa substituir o perfil que já existe.
- **Perfis importados antes de setembro de 2026** não têm a regra que rejeita IPv6; apague e importe de novo.

Se você importou e não conecta, veja [Solução de problemas 04](../troubleshooting/04-singbox-import-not-connecting.md).

## Perguntas frequentes

**Qual a diferença entre uma assinatura do Hiddify e uma assinatura do Clash?** O formato é diferente (JSON x YAML), e cada cliente não reconhece a assinatura do outro, mas os nós em si funcionam nos dois. A LeoTun entrega os dois direto: clientes da família Clash clicam no botão "Assinatura Clash" e não devem usar o link de compartilhamento.

**Um perfil pode ter todas as regiões?** Importando pela bandeira você ganha um perfil por região e troca entre eles na lista de perfis do cliente; assim, uma mudança de endereço numa região afeta só aquela região. Para importar de uma vez todas as regiões fora da China e deixar o cliente escolher sozinho, clique em "Importar todas as regiões · seleção automática" no topo da página (ela tem só os botões de assinatura sing-box e assinatura Clash).

**Posso mandar o QR code para a minha família?** O QR code contém as credenciais da sua conta; quem recebe fica com a sua conta. Dividir com a família é permitido (aparelhos simultâneos conforme o plano: Individual 2, Família 4, Empresa 8), mas não publique em lugar público; se vazar, troque a senha e ele para de funcionar.

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=client-02) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=client-02) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 24 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, oferta permanente
