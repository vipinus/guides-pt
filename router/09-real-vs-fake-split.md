# 09 · Como funciona o roteamento dividido do roteador

> Versão no site (mais completa): https://www.leotun.com/pt/guides/router-smart-split?utm_source=github&utm_content=router-09

Todos se chamam "roteamento dividido inteligente", mas alguns roteadores simplesmente são chatos de usar. Para entender o que é o roteamento dividido, veja o [03](03-router-split-routing.md); este artigo trata só do que ele deveria fazer, dos sintomas que aparecem quando falta uma parte e de como o nosso roteador faz.

## Em uma frase

O que o roteamento dividido deveria fazer: cada site, **junto com as imagens, o vídeo e o login dele**, passa pela VPN ou conecta direto conforme onde ele fica, e **todos os aparelhos da casa seguem as mesmas regras**. Quando só uma parte disso é feita, aparecem os sintomas abaixo.

## Sintomas comparados

| O que você vê | O que está acontecendo por trás |
|---|---|
| Com o roteamento dividido ligado, os sites chineses ficam até mais lentos | Os sites chineses são tomados por estrangeiros e tudo faz um desvio pelo exterior e volta |
| A página abre, mas o vídeo fica carregando, as imagens não aparecem e o login trava | A lista só tem o site principal, e o vídeo, as imagens e o login do mesmo site vão por outro caminho |
| Você está no exterior com a linha para a China ligada, e o app de vídeo ainda diz "仅限中国大陆" (só na China continental) | Parte do tráfego não entrou na VPN, e o site viu um endereço de fora |
| Toca no celular mas não na TV ou na TV box; um computador simplesmente não passa pela VPN | Esse aparelho tem configurações de rede próprias e contorna o roteador |
| Apps de banco e de pagamento avisam de vez em quando sobre "login em outro local" | O tráfego do mesmo app sai pela China num momento e pelo exterior no outro |
| O roteamento dividido some enquanto você usa (depois de reiniciar ou reconectar, ou tudo passa pela VPN ou nada passa) | A configuração não foi guardada |

Nenhum desses **gera erro**. O roteador mostra "Conectado" o tempo todo, o que os torna os mais difíceis de investigar, e muita gente acaba achando que a linha é ruim.

## O que o roteamento dividido deveria fazer

- Um site vai por um caminho só junto com as páginas, as imagens, o vídeo e o login dele, sem ser repartido
- Ao decidir "chinês ou estrangeiro", ele fica do lado certo, e os sites chineses não fazem desvio
- Todos os aparelhos da casa seguem as mesmas regras, e mudar as configurações de rede no próprio aparelho não consegue contorná-las
- O sentido muda automaticamente com a região escolhida (acessar a China a partir do exterior e acessar serviços de fora a partir da China são dois conjuntos opostos de regras)
- A lista se atualiza sozinha, sem precisar instalar o firmware de novo
- As configurações ficam guardadas: iguais depois de reiniciar ou reconectar; e, uma vez desligado, ele não é religado escondido

## O roteamento dividido inteligente do nosso roteador

| | Como é feito |
|---|---|
| Chave | Ligado por padrão; escolher uma região na China = sentido de acessar a China a partir do exterior, escolher uma região de fora = sentido de acessar serviços de fora a partir da China, aplicado automaticamente. O sentido de acessar serviços de fora a partir da China também tem a caixa "Blocked sites only" (só sites bloqueados pela linha), em "VPN settings" (configurações de VPN) → roteamento dividido inteligente, marcada por padrão; desmarcada = sites chineses direto, todo o resto pela VPN. Firmwares instalados antes de outubro de 2026 ainda não mostram essa caixa; fale com o atendimento para mudar remotamente |
| Lista | Organizada por "site inteiro": as páginas vão junto com as fontes de vídeo, imagem e login que elas usam |
| Acessar serviços de fora a partir da China | Por padrão só os sites e serviços bloqueados passam pela VPN (com base numa lista de sites bloqueados atualizada sozinha todo dia, mais serviços como o Telegram, que conectam a endereços fixos); os sites chineses e os sites estrangeiros que já abrem normalmente na China (sites de empresas estrangeiras, downloads da Apple e da Microsoft, plataformas de jogos) conectam direto, sem desvio, na mesma velocidade de quando não há roteador |
| Aparelhos da casa | Controlados de forma uniforme; configurações de rede mudadas no próprio aparelho continuam seguindo as regras; não existe "porta dos fundos" para contornar o roteador |
| Atualizações | A lista e as regras se atualizam sozinhas quando o roteador liga; a lista de sites bloqueados também se atualiza sozinha todo dia |
| Memória | Mantida depois de reconectar ou reiniciar; uma vez desligado, continua desligado |
| Rede local | Impressoras, NAS e câmeras são acessados direto, como sempre |

**O único caso que precisa da sua ajuda**: quando um celular ou navegador está com uma configuração criptografada como "DNS privado" ou "DNS seguro" ligada, o aparelho criptografa as próprias consultas e o roteador não consegue vê-las. Se um aparelho se comportar de forma estranha, ou se os sites bloqueados não abrirem enquanto todo o resto funciona, desligue esse tipo de configuração primeiro.

## Confira você mesmo

1. Você está na China (acessando serviços de fora): Baidu e Taobao, e os sites estrangeiros que já abrem normalmente na China, como os downloads da Apple e da Microsoft, estão com a velocidade normal; os sites de fora bloqueados abrem e o vídeo toca.
2. Você está no exterior (acessando a China): escolha qualquer episódio no Tencent Video ou no iQIYI e ele toca, sem a mensagem "仅限中国大陆" (só na China continental); os sites locais de banco e de compras funcionam normalmente.
3. Teste todos os aparelhos, principalmente a TV e a TV box; para o que se comportar de forma estranha, confira primeiro o "DNS privado / DNS seguro" e depois confirme que ele está ligado ao Wi‑Fi deste roteador, e não ao do modem.
4. Um site não abre com o roteamento dividido: mude para "Global" temporariamente. Se abrir no Global mas não no roteamento dividido, ele ainda não está na lista; mande o endereço ao atendimento para incluí-lo, e ele chega com a atualização automática. Na China, você também pode desmarcar "Blocked sites only" na parte de roteamento dividido inteligente e tentar de novo; se abrir, ele também está bloqueado mas ainda não está na lista.

## Perguntas frequentes

**Preciso ligar o roteamento dividido inteligente por conta própria?** Não. Ele já está ligado assim que você entra na sua conta e escolhe uma região.

**Acessar a China a partir do exterior e acessar serviços de fora a partir da China precisam ser configurados separadamente?** Não. O sentido é decidido automaticamente pela região escolhida.

**Afeta impressoras ou NAS?** Não. Os aparelhos da rede de casa são acessados direto, como sempre.

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=router-09) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=router-09) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 15 créditos (cerca de 15 dias do plano Individual), oferta permanente
