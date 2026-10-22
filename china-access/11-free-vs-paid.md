# 11 · VPN para a China: grátis ou pago

Primeiro, faça as contas: a parte mais cara de uma linha para a China é a banda na saída do continente, que os provedores de nuvem chineses cobram por tráfego, e não é barato. Uma opção grátis não faz milagre. Ela só pode escolher uma de três: espremer muita gente numa máquina, limitar tráfego e tempo, ou recuperar o dinheiro com os seus dados e com anúncios. Isso não quer dizer que grátis nunca serve; para uma consulta de vez em quando, dá conta. Mas para acompanhar séries, usar internet banking ou configurar para a família, um mês de linha paga costuma custar menos que um café, e o tempo que ela economiza vale muito mais que isso.

## Três motivos para os nós grátis caírem toda hora

- Lotados: centenas ou milhares de pessoas dividem uma máquina e uma linha internacional. De dia vai bem, e das 20h às 23h no horário de Pequim todo mundo fica vendo a rodinha girar.
- Limitados: cortam quando o tráfego acaba, cortam quando o tempo acaba, seguram a velocidade abaixo de 1080p e abrem uma janela no meio pedindo pagamento. Na verdade são versões de teste de produtos pagos que só não dizem isso.
- Vendidos: se sustentam inserindo anúncios, coletando o histórico de navegação ou usando o seu aparelho como nó de saída de outras pessoas. Isso é especialmente comum nas extensões de navegador grátis "para a China".

## Mais duas armadilhas das opções grátis que você não vê

Primeira: a saída não está necessariamente no continente. Muitos nós grátis "para a China" são, na verdade, endereços de Hong Kong, Taiwan ou Japão. Eles abrem páginas chinesas, mas o Tencent Video e o iQIYI continuam mostrando restrição de direitos autorais, e o internet banking também trata você como estrangeiro. Consulte uma vez onde o IP está registrado depois de conectar e você vai saber.

Segunda: IPv6 e DNS não são tratados. As opções grátis quase nunca bloqueiam o IPv6 dentro do túnel, e quando o seu aparelho tem IPv6 o site de vídeo continua vendo um endereço de fora. Esse é o motivo mais comum de "está conectado e mesmo assim não consigo assistir"; veja "Tencent Video ou iQIYI bloqueados no exterior? Resolva em 5 passos".

## Quando o grátis basta e quando vale pagar

Basta: abrir de vez em quando uma página chinesa para consultar algo ou ler notícias, sem exigir velocidade nem estabilidade, e sem entrar em nenhuma conta por ela.

Hora de pagar: você quer assistir séries e ouvir música, entrar no internet banking ou no Alipay, configurar para a TV e para os idosos da casa, ou garantir passagens num horário marcado. O que essas situações pedem é "funcionar sempre", e isso uma opção grátis não consegue dar.

Um teste simples: se você ficaria irritado quando cai, está na hora de pagar.

## Quanto gastar

O plano Individual da LeoTun custa 5 dólares por mês e inclui 24 regiões, 2 aparelhos on-line ao mesmo tempo e todas as formas de conexão (AnyConnect / OpenVPN / Hiddify / Proxy Web), e também funciona com roteador. Os planos Família e Empresa custam 2 e 4 vezes o Individual, respectivamente. Regiões, linhas e formas de conexão são exatamente iguais nos três planos, e a única diferença é o número de aparelhos on-line ao mesmo tempo (4 e 8).

Se você não quer comprar por mês, há dois caminhos: primeiro peça o teste grátis de 4 horas (sem cartão de crédito, uma vez por conta) e teste uma vez no pico da noite; ou pague por dia. Depois de recarregar créditos, o plano Individual consome 1 crédito por dia, e 28 créditos custam 10 dólares, o que dá cerca de 0,36 dólar por dia; comprar só alguns dias antes de uma viagem à China cai bem.

Quando um amigo que você convidou se cadastra e faz o primeiro pagamento, você e o amigo ganham 15 créditos cada (cerca de 15 dias no plano Individual), sem limite de pessoas. É uma fonte permanente de tempo grátis.

## Como conferir antes de pagar

1. Peça o teste, conecte na linha para a China e consulte se o IP está registrado na China continental.
2. Abra uma página de teste de IPv6 e confirme que o IPv6 está indisponível ou também é um endereço do continente.
3. Toque um episódio em 1080p depois das 20h no horário de Pequim e veja se ele fica carregando várias vezes.
4. Troque para outra saída na China e teste mais uma vez, para confirmar que não foi sorte.
5. Veja se ele usa protocolos padrão (AnyConnect, OpenVPN, Hiddify): os aplicativos vêm do fabricante ou da comunidade de código aberto, e se o provedor fechar, a configuração ainda pode ser usada em outro lugar; com um app proprietário, quando ele é derrubado não sobra nada.

## Perguntas frequentes

**Existe VPN para a China realmente grátis e estável?** Estável por muito tempo, não; a estrutura de custos decide isso. Estável e grátis só existe no período de teste de um produto pago. Usá-lo para conferir o serviço é o certo; contar com ele para uso contínuo não é realista.

**Uma VPN grátis vai roubar as minhas senhas?** Ela não vê o conteúdo HTTPS dentro do túnel, mas vê quais domínios você acessa e pode inserir conteúdo em páginas sem criptografia. Os proxies grátis em forma de extensão de navegador têm permissões ainda mais amplas. Não entre no internet banking por uma linha grátis.

**O que compensa mais, pagar por dia ou por mês?** Se você usa 12 dias ou mais por mês, o mensal compensa mais; se usa alguns dias de vez em quando, o diário. Os créditos não expiram, e uma recarga dura bastante.

**O teste pede cartão de crédito?** Não. Peça na página inicial depois de se cadastrar: 4 horas com todos os recursos, uma vez por conta.

**Paguei e continua caindo. O que eu faço?** Troque primeiro de região, depois de forma de conexão (os três protocolos podem ser usados na mesma conta); se ainda não resolver, leia o guia de solução de problemas ou fale com o suporte. Parte do motivo de pagar é ter alguém que se responsabilize.

## Leia também

- [Preços e teste grátis](https://www.leotun.com/pt?utm_source=github&utm_content=china-access-11)
- [Como escolher uma VPN com IP da China](https://www.leotun.com/pt/guides/choose-china-vpn?utm_source=github&utm_content=china-access-11)
- [Tencent Video ou iQIYI bloqueados no exterior? Resolva em 5 passos](https://www.leotun.com/pt/guides/overseas-video?utm_source=github&utm_content=china-access-11)
- [Como estudantes no exterior devem configurar uma VPN para a China](https://www.leotun.com/pt/guides/students?utm_source=github&utm_content=china-access-11)

Versão deste artigo no site: https://www.leotun.com/pt/guides/free-vs-paid?utm_source=github&utm_content=china-access-11

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=china-access-11) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=china-access-11) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 15 créditos (cerca de 15 dias do plano Individual), oferta permanente
