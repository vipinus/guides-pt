# 10 · Como estudantes no exterior devem configurar uma VPN para a China

O que um estudante chinês no exterior precisa não é "uma linha para a China sempre ligada", e sim conseguir um IP chinês de forma confiável em algumas situações específicas: acompanhar séries e ouvir música, entrar no internet banking e em apps do governo, garantir passagens e ingressos, e de vez em quando ver remotamente os aparelhos da família em casa. Cada situação exige algo diferente da linha, e as redes das universidades têm limites próprios. Este artigo explica, situação por situação, do que você precisa, como configurar e quando desconectar, e termina com uma lista que dá para fazer em dez minutos antes do começo do semestre.

## Séries, música e lives: basta um IP chinês, mas o IPv6 precisa ser fechado

Tencent Video, iQIYI, os animes do Bilibili, NetEase Cloud Music e QQ Music decidem a região pelo IP de origem, e conectar na linha para a China basta. A armadilha em que os estudantes mais caem é que as redes das universidades e dos alojamentos costumam ter IPv6: o aparelho prefere o IPv6, que não passa pela linha, então o site de vídeo continua vendo um endereço de fora e mostra "restrição de direitos autorais".

A solução é usar uma linha ou um aplicativo que bloqueie o IPv6 dentro do túnel, ou desligar o IPv6 no aparelho. As três formas de conexão da LeoTun já bloqueiam o IPv6 do lado da linha, sem precisar mexer no aparelho; para investigar em detalhe, veja "Tencent Video ou iQIYI bloqueados no exterior? Resolva em 5 passos".

A qualidade da imagem depende da banda internacional. Das 20h às 23h no horário de Pequim é o pico, o que corresponde à manhã até o meio-dia na Europa e à noite até a madrugada nas Américas; se o 1080p ficar carregando nesse horário, troque para outra saída na China.

## Internet banking, Alipay e apps do governo: entre pela linha para a China e desconecte ao terminar

Os apps de banco, o Alipay, o CHSI e a Plataforma Nacional de Serviços do Governo tratam IPs de fora de formas diferentes: alguns recusam o login de cara, alguns colocam várias etapas extras de verificação, e alguns deixam entrar mas acionam o controle de risco numa transferência. O que eles têm em comum é que registram o IP do seu login, e ficar pulando entre exterior e China é o que mais faz você ser marcado.

O que fazer: quando precisar fazer essas coisas, conecte primeiro na linha para a China e depois abra o app; ao terminar, feche o app e só então desconecte a linha. Não use o mesmo app trocando toda hora entre a linha para a China e a rede local.

Código de verificação por SMS que não chega não tem nada a ver com a linha; é questão de roaming de um número chinês no exterior. Antes de sair da China, ative o roaming internacional do número ou mude para um plano que receba códigos no exterior.

## 12306 e venda de ingressos de shows: conecte antes e não troque na hora de pagar

O 12306 (o sistema de venda de passagens de trem da China) às vezes pede verificação extra quando vê um IP de fora, e numa disputa por passagens uma verificação a mais significa perder a passagem. Alguns minutos antes de abrir a venda, conecte na linha para a China, entre e selecione os dados dos passageiros, e envie assim que der a hora. Quando o pagamento redirecionar para o Alipay ou para o internet banking, mantenha a linha como está.

O mesmo vale para plataformas de ingressos como Damai e Maoyan.

## Três limites das redes de universidade e alojamento

- IPv6: veja acima; use uma linha que bloqueie o IPv6.
- UDP restrito ou limitado: muitas redes de universidade limitam ou até bloqueiam o tráfego UDP. O hysteria2 que o Hiddify usa roda sobre UDP, e nessas redes acaba sendo menos estável que o AnyConnect, que roda sobre TLS; uma conta pode usar os dois, então, se o UDP não funcionar, mude para o AnyConnect.
- Página de login (portal cativo): depois de entrar no Wi‑Fi da universidade, conclua a autenticação no navegador primeiro e só então ligue a linha. Se o aplicativo da linha estiver configurado para "conectar automaticamente ao iniciar", ele vai tentar conectar antes da autenticação e falhar; espere um pouco mais ou reconecte manualmente.

## Voltar para a China nas férias: a mesma conta, no sentido contrário

Na China você precisa do Google, do e-mail da universidade e das bases de artigos; basta trocar a região da linha de China para Japão, Estados Unidos ou outra região de fora próxima, sem trocar de conta. As 24 regiões da LeoTun estão todas na mesma conta, e acessar a China do exterior e acessar o exterior a partir da China são os dois sentidos da mesma coisa.

Quando você conecta de dentro da China, os endereços do AnyConnect e do Hiddify mudam automaticamente para driblar os bloqueios, e os endereços salvos no aplicativo não precisam ser trocados; se não conectar, troque de região ou de protocolo.

## Lista de dez minutos antes do começo do semestre

1. Instale um aplicativo (AnyConnect ou Hiddify) no celular e outro no computador, e entre ou importe lendo o QR code em cada um.
2. Conecte na linha para a China pelo Wi‑Fi do alojamento e abra uma página de teste de IPv6 para confirmar que o IPv6 está indisponível ou mostra um endereço do continente.
3. Abra o Tencent Video e toque qualquer episódio para confirmar que não aparece restrição de direitos autorais.
4. Entre uma vez no app do seu banco para confirmar que consegue acessar, depois feche o app e desconecte a linha.
5. Anote o contato do suporte do seu provedor da linha; quando algo der errado, leia primeiro o guia de solução de problemas e depois pergunte.

## Perguntas frequentes

**Usar uma VPN para a China afeta a conta de rede do estudante na universidade?** Não. A linha só manda o seu tráfego para uma saída na China, e o que a rede da universidade vê é uma conexão criptografada. As regras de uso da maioria das universidades só proíbem downloads piratas e ataques, e acessar serviços do seu próprio país não está entre eles; se tiver dúvida, dê uma olhada na política de uso aceitável da universidade.

**Posso dividir uma conta com quem mora comigo?** Conforme o plano, uma conta pode ter 2 (Individual), 4 (Família) ou 8 (Empresa) aparelhos on-line ao mesmo tempo, e dividir com a família ou com quem mora com você está dentro das regras. Mas para coisas como internet banking é mais seguro cada um usar a própria conta, para evitar que várias pessoas troquem toda hora na mesma linha e acionem o controle de risco.

**Por que o Hiddify fica lento no alojamento enquanto o AnyConnect está normal?** O mais provável é que a rede da universidade restrinja UDP. O protocolo hysteria2 do Hiddify é baseado em UDP, e quando limitado fica lento ou cai; o AnyConnect roda sobre TLS, igual a acessar um site HTTPS, e não é afetado.

**Dá para jogar em servidores chineses por uma linha para a China?** Dá para entrar, mas a latência depende da sua distância física até a saída na China. Essa parte da latência é fixa; é aceitável em jogos por turnos e MOBAs, e perceptível em jogos de tiro.

**A conta continua útil depois que eu me formar e voltar para a China?** Continua. A mesma conta segue funcionando dentro da China com uma região de fora, para acessar Google, GitHub, o e-mail da universidade e as bases de artigos.

## Leia também

- [Tencent Video ou iQIYI bloqueados no exterior? Resolva em 5 passos](https://www.leotun.com/pt/guides/overseas-video?utm_source=github&utm_content=china-access-10)
- [Como escolher uma VPN com IP da China](https://www.leotun.com/pt/guides/choose-china-vpn?utm_source=github&utm_content=china-access-10)
- [Download do aplicativo AnyConnect](https://www.leotun.com/pt/anyconnect?utm_source=github&utm_content=china-access-10)
- [Aplicativo Hiddify e importação da assinatura](https://www.leotun.com/pt/singbox?utm_source=github&utm_content=china-access-10)

Versão deste artigo no site: https://www.leotun.com/pt/guides/students?utm_source=github&utm_content=china-access-10

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=china-access-10) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=china-access-10) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, oferta permanente
