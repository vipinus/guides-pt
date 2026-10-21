# 08 · Depois de instalar o firmware: o que ele faz sozinho e as poucas chaves que você deve conhecer

> Versão no site (mais completa): https://www.leotun.com/pt/guides/router-firmware?utm_source=github&utm_content=router-08

Depois de instalar o firmware deste site ou comprar um roteador já configurado, tudo o que você precisa fazer é entrar na sua conta na página de administração. Este artigo mostra o que o firmware **faz sozinho** e as poucas chaves em que você talvez precise mexer; para começar, veja o [01](01-plug-and-play-router.md); para o roteamento dividido, o [03](03-router-split-routing.md); e para vínculo e troca de roteador, o [05](05-mac-binding-and-replacing.md).

## O que ele faz sozinho

| O quê | Como funciona | O que você precisa fazer |
|---|---|---|
| Atualização de componentes e da lista de roteamento dividido | Verifica ao ligar e baixa o que houver de novo, que **passa a valer na próxima inicialização**; a lista de sites bloqueados usada para acessar serviços de fora a partir da China também se atualiza sozinha todo dia | Nada; endereços de linha alterados e sites acrescentados à lista são aplicados automaticamente |
| Código de país do Wi‑Fi | Detecta o país em que está depois de entrar na internet e ajusta a potência e os canais do sinal automaticamente | Logo depois da instalação, **ligue primeiro um cabo de rede** para ele entrar na internet uma vez; sinal mais fraco antes disso é normal |
| Vencimento | Quando a conta vence, ele para de passar pela VPN; a rede local continua normal | Volta sozinho depois de renovar, sem precisar entrar de novo |
| Vínculo do roteador | O primeiro login registra este roteador na conta | Desvincule no site antes de trocar de roteador |

Só uma atualização de versão maior do firmware inteiro exige instalar o arquivo sysupgrade. Isso acontece poucas vezes por ano, e o site avisa.

## Onde você talvez precise mexer

- **Modo de roteamento dividido**: Split routing (dividido, padrão) / Global / Direct (direto). Se um site não abrir, mude primeiro para Global para testar: se abrir no Global, ele não está na lista, então passe o endereço ao atendimento para ser incluído; se não abrir nem no Global, o problema é do próprio site.
- **Região**: escolhida na página de administração. Escolha a região China para assistir conteúdo chinês no exterior, e uma região de fora para acessar serviços de fora a partir da China.
- **Blocked sites only** (só sites bloqueados pela linha): uma caixa de seleção em "VPN settings" (configurações de VPN), na parte de roteamento dividido inteligente, marcada por padrão. Vale só para o sentido de acessar serviços de fora a partir da China (você está na China e escolheu uma região de fora). Marcada, só os sites e serviços bloqueados passam pela VPN (com base numa lista de sites bloqueados atualizada sozinha todo dia, mais serviços como o Telegram, que conectam a endereços fixos); os sites chineses e os sites estrangeiros que já abrem normalmente na China (sites de empresas estrangeiras, downloads da Apple e da Microsoft, plataformas de jogos e afins) conectam direto, sem desvio. Desmarque para voltar ao comportamento anterior: sites chineses direto, todo o resto pela VPN. Se um site estrangeiro não abrir enquanto você está na China, desmarque (ou mude para Global temporariamente) e tente de novo; se abrir, o site está bloqueado mas ainda não está na lista, então mande o endereço ao atendimento. Firmwares instalados antes de outubro de 2026 ainda não mostram essa caixa (o novo padrão já vale pelas atualizações automáticas); para mudar, fale com o atendimento, que faz isso remotamente. O sentido de acessar a China a partir do exterior não é afetado por essa chave.
- **Automatically select the fastest line** (escolher automaticamente a linha mais rápida): fica abaixo da região, desligada por padrão, e é recomendada quando a qualidade da rede é ruim.

  | | Desligada (padrão) | Ligada |
  |---|---|---|
  | Qual linha é usada | Sempre a região que você escolheu | Escolhe automaticamente, entre as linhas disponíveis, a de menor latência e pouca perda de pacotes, depois testa de novo periodicamente e troca sozinha se piorar |
  | País de saída | A região escolhida | Com a região China escolhida: escolhe só entre linhas na China, e a saída continua na China; com uma região de fora escolhida: escolhe entre todas as linhas de fora, e **o país de saída pode ser diferente da região escolhida** (por exemplo, você escolheu Japão, mas na prática sai por Singapura) |
  | Indicada para | Situações que exigem um país fixo: assistir aos serviços de streaming de um país específico, bancos e contas sensíveis à região | Rede de casa instável ou uma região que trava com frequência, quando você só quer velocidade e não liga para o país de saída |

  Quando você aciona a chave, a página de administração mostra "Switching automatic selection…" (trocando a seleção automática) e bloqueia a página até a troca terminar. A rede cai rapidamente nesse meio-tempo, o que é normal. "Current exit" (saída atual) na página de administração mostra qual linha está realmente em uso.
- **Senha de administrador e senha do Wi‑Fi**: os valores de fábrica são padrões públicos; troque logo depois de entrar.

## TVs, TV boxes e aparelhos dos idosos da família

- Basta conectar ao Wi‑Fi deste roteador ou por cabo, e a versão da China continental de um app já toca; as versões internacionais (iQIYI, WeTV) têm outro catálogo, então instale a versão da China continental.
- Um aparelho está conectado mas não passa pela VPN, ou os sites bloqueados não abrem enquanto todo o resto funciona: o mais provável é que ele tenha um DNS privado próprio configurado ("DNS privado" do Android, DNS seguro do navegador), e o roteador não consegue ver qual site ele está procurando; desligue isso.
- Você quer que um aparelho sempre conecte direto (um computador de trabalho que precisa entrar na VPN da empresa): conecte-o ao Wi‑Fi do roteador principal ou do modem.

## Perguntas frequentes

**O plano Individual pode usar roteador?** Pode. Individual, Família e Empresa aceitam roteador, sem precisar trocar de plano.

**Quantas vagas de aparelho o roteador ocupa?** Uma; os aparelhos ligados a ele não entram na conta.

**O firmware tem porta dos fundos?** Ele é compilado a partir do OpenWrt, só com o acréscimo do componente que conecta à VPN e das regras de roteamento dividido; a VPN registra só a duração da conexão e o tráfego total, para cobrança.

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=router-08) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=router-08) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, válido por tempo indeterminado
