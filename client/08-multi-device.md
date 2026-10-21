# 08 · Configure vários aparelhos de uma vez e troque de celular sem recomeçar

Para quem tem muitos aparelhos, o mais chato é configurar cada um, refazer tudo ao trocar de celular e tocar em conectar em cada aparelho quando sai de casa. A Rede privada acaba com isso: cada aparelho entra uma vez com a sua conta deste site e depois fica on-line, sem nada a fazer após reiniciar ou trocar de Wi‑Fi; cada aparelho escolhe a própria região de saída, então o notebook pode usar o Japão e o celular a região China sem um atrapalhar o outro; os aparelhos da mesma conta se enxergam, então um notebook fora de casa abre direto as pastas compartilhadas do NAS de casa. Um celular novo só precisa entrar na conta. Este artigo explica como colocar todos os aparelhos da casa, como a cota é contada e o que fazer com vencimento e troca de aparelho.

## O que você faz uma vez só em cada aparelho

1. Instale o cliente Tailscale (Android, Windows, macOS e Linux pela área de download da página da Rede privada deste site; iPhone / iPad pela App Store, o que exige um ID Apple de fora da região China).
2. Se você já entrou numa conta oficial do Tailscale, saia antes e depois aponte o login para o servidor de controle deste site (celular: "⋯" na tela sem login → Use custom server, ou seja, usar servidor personalizado; computador: copie o comando da página; macOS: Account Settings → Accounts → a seta ao lado de "Add Account…" → Add Account Using Alternate Server, ou seja, adicionar conta usando outro servidor).
3. Confirme no navegador com a sua conta deste site. A partir daí o aparelho está na Rede privada e não precisa de mais nada.
4. Escolha uma saída: cada aparelho escolhe no próprio menu, independente dos outros. Para não usar saída nenhuma, escolha None (nenhuma), o que mantém só o acesso entre aparelhos.

## Como os aparelhos simultâneos são contados

Uma conta pode ser instalada em quantos aparelhos você quiser; o único limite é quantos ficam on-line ao mesmo tempo: Individual 2, Família 4, Empresa 8, dividindo a mesma cota com Cisco, Hiddify e as outras formas. Se passar do limite do seu plano, você pode subir de plano temporariamente (o tempo restante é convertido pelo valor equivalente) e voltar quando terminar.

Um roteador conta como um aparelho, e os aparelhos ligados a ele não entram na conta. Um roteador ou NAS em casa mais o celular e o notebook que você leva costumam bastar.

## Os aparelhos se enxergam

- Cada aparelho da mesma conta tem um endereço na Rede privada e também pode ser acessado pelo nome, sem precisar de IP público nem de redirecionamento de portas.
- Abrir uma pasta compartilhada do NAS de casa num notebook fora de casa, ver o gravador de vídeo de casa pelo celular ou usar a área de trabalho remota num computador de casa: tudo conecta direto pelos endereços da Rede privada.
- Um roteador de casa com o firmware deste site pode compartilhar toda a rede local com a Rede privada, então aparelhos que não rodam cliente, como impressoras e TVs, também ficam acessíveis de fora.
- Os aparelhos de outros clientes nem existem na sua Rede privada; não é só que você não consegue vê-los.

## Vencimento, troca de aparelho, desinstalação

- Vencimento da conta: todos os aparelhos ficam off-line em poucos minutos; depois de renovar, entre mais uma vez em cada um, e as configurações de saída continuam salvas.
- Troca de celular: entre no celular novo seguindo os passos acima; se aparecer que o limite foi atingido, saia da conta no celular antigo, ou suba de plano temporariamente e volte quando terminar.
- Se você não quer mais um aparelho na Rede privada: saia da conta no cliente; para derrubar um aparelho à força, fale com o suporte.
- Não rode outra VPN no mesmo aparelho ao mesmo tempo (um Cisco da empresa, outro software de rede mesh); elas brigam por DNS e rotas.

## Perguntas frequentes

**Cada aparelho pode escolher uma região de saída diferente?** Pode, cada aparelho escolhe a própria saída. O notebook pode usar o Japão para vídeo enquanto o celular usa a região China para o banco, sem um atrapalhar o outro.

**Deixar a Rede privada sempre ligada gasta bateria?** Sem saída escolhida quase não há tráfego; ela só é usada para falar com os aparelhos da Rede privada. O gasto de bateria é parecido com o da VPN do sistema.

**Como instalo no NAS de casa?** Synology e QNAP têm um pacote do Tailscale, e sistemas Linux usam o script de instalação oficial; na hora de entrar, aponte para o servidor de controle deste site do mesmo jeito. Um roteador com o firmware deste site não precisa de instalação: entre na sua conta e ele já está na Rede privada.

**Por que não configurar o Cisco em todos os aparelhos?** Dá, mas no Cisco você precisa tocar em conectar toda vez, reconectar quando cai e trocar o endereço para mudar de saída; com muitos aparelhos, a Rede privada dá muito menos trabalho. A exceção é um aparelho numa rede de universidade que restringe UDP; nesse, use o Cisco.

## Leia também

- [Página da Rede privada: download e passos para entrar](https://www.leotun.com/pt/mesh?utm_source=github&utm_content=client-08)
- [O que é a Rede privada (Tailscale)](https://www.leotun.com/pt/guides/tailscale-mesh?utm_source=github&utm_content=client-08)
- [Ver as câmeras e o NAS da sua casa na China a partir do exterior](https://www.leotun.com/pt/guides/home-camera?utm_source=github&utm_content=client-08)
- [O que o firmware do roteador faz](https://www.leotun.com/pt/guides/router-firmware?utm_source=github&utm_content=client-08)

Versão deste artigo no site: https://www.leotun.com/pt/guides/multi-device?utm_source=github&utm_content=client-08

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=client-08) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=client-08) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 15 créditos (cerca de 15 dias do plano Individual), oferta permanente
