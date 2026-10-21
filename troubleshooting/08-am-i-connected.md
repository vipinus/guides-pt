# 08 · Como confirmar que está mesmo conectado e por qual região está saindo

O cliente mostrar "Conectado" não quer dizer que os sites que você acessa estejam vendo o endereço da VPN. O jeito mais fácil de conferir está na própria barra superior deste site: o campo "Rede atual" mostra **você do jeito que este site está vendo agora** — de que país, de que estado/província e de que rede você está saindo. Este artigo explica como ler esse campo, como comparar antes e depois de conectar, como saber se cada uma das seis formas de conexão está conectada, o que significam as luzes vermelha, amarela e verde na lista de regiões e algumas coisas que você mesmo pode conferir quando está "conectado, mas ainda aparece o local".

## O que a "Rede atual" na barra superior mostra

| Posição | Conteúdo |
|---|---|
| No começo | A bandeira do país onde fica a saída; quando o país não é identificado, aparece um ícone de Wi‑Fi no lugar |
| No meio | O nome do estado/província, no idioma da interface (EUA, Canadá, Austrália e outros usam as siglas comuns, como CA, ON, NSW); Hong Kong, Macau e Singapura mostram direto o nome da região |
| No fim | O nome da rede: as três grandes operadoras da China, a rede educacional e afins aparecem na interface em chinês com nomes curtos como 电信 (China Telecom), 移动 (China Mobile), 联通 (China Unicom) e 教育网 (rede educacional); as demais mostram o nome da marca em inglês (por exemplo, Comcast, Bell) |

- **Quando o estado/província não é encontrado, aparece só "bandeira · nome da rede".** O nome do país não é usado para preencher; a bandeira já diz o país.
- No computador, passe o mouse sobre esse campo e aparece o nome completo da organização, o estado/província, o código do país e o **IP de saída**. Esse IP só é mostrado para você, e é a informação mais útil para ter em mãos ao falar com o suporte.
- O Chrome / Edge no Windows não têm fonte de bandeiras, então a bandeira aparece como duas letras (por exemplo, JP, US). O significado é o mesmo.
- No computador, ele só aparece na barra superior depois que você entra na conta; no celular, aparece sem login.

## Compare antes e depois de conectar e saiba na hora

1. **Com a VPN desligada**, abra este site e dê uma olhada: deve aparecer a operadora da sua banda larga ou dos seus dados móveis, e a bandeira deve ser a do país em que você está.
2. **Conecte a VPN** e volte ao navegador: a bandeira muda para a região que você escolheu, e o nome da rede costuma mudar para o nome de um data center ou de um provedor de nuvem, em vez da sua operadora.
3. Se os dois estiverem iguais, este navegador não está passando pela VPN quando acessa este site. Veja "Conectado, mas ainda aparece o local" abaixo.

**Não precisa ficar atualizando a página.** Esse campo confere de novo sozinho quando você volta para a janela do navegador, confere mais algumas vezes nos segundos seguintes quando detecta uma mudança de rede e também se atualiza a cada dez a vinte segundos enquanto a página está aberta. Se logo depois de conectar ainda aparecer o valor antigo, espere dez a vinte segundos ou troque de janela; se ainda não mudar, atualize à mão.

**Quando você está na China e escolheu um "ponto de entrada na China"**, é normal a barra superior mostrar um país estrangeiro: os pontos de entrada na China usam roteamento dividido, então os sites chineses saem de dentro da China e os sites estrangeiros saem pela rota de fora. Este site fica fora da China, então o que aparece, naturalmente, é a ponta de fora.

## Como saber se cada forma de conexão está conectada

| Forma | O que olhar no cliente | A barra superior deste site muda? |
|---|---|---|
| Cisco (AnyConnect) | O cliente mostra "Connected" (conectado) | Sim. Com o Cisco conectado, todo o tráfego passa pela VPN |
| Hiddify | O cliente mostra conectado | Muda no modo global; no roteamento automático, depende da lista |
| OpenVPN | O cliente mostra conectado | Sim. Por padrão, todo o tráfego passa pela VPN |
| Rede privada (Tailscale) | O cliente está on-line **e** há uma região escolhida como Exit Node (nó de saída) | Só muda quando há uma saída escolhida; com None (nenhuma), os aparelhos só se enxergam entre si e o tráfego não passa pela VPN |
| Proxy (Proxy Web) | Não existe estado "conectado"; veja qual modo de região está escolhido no ícone da extensão | Só muda no navegador com a extensão instalada; as regras de "auto switch" (troca automática) podem mandar este site direto |
| Roteador | Na página de administração, o status da conta está normal e a data de vencimento aparece | Olhe de um aparelho ligado ao Wi‑Fi desse roteador; no modo de roteamento dividido, depende da lista |

Roteamento dividido quer dizer que os sites da lista passam pela VPN e todo o resto vai direto. Se a barra superior mostra o local com o roteamento dividido ligado, isso não quer dizer necessariamente que você não está conectado: **mude para "global" temporariamente e olhe de novo**. Se mudar, a VPN está funcionando e este site só não está na lista.

## As luzes vermelha, amarela e verde na lista de regiões

Nas páginas do Cisco, do Hiddify, do Proxy e do OpenVPN há uma luzinha embaixo da bandeira de cada região, e a mesma luz aparece antes dos nomes das saídas no cliente da Rede privada. Ela é classificada automaticamente pela banda média em tempo real de cada servidor daquela região e se atualiza mais ou menos uma vez por minuto:

| Luz | Significado |
|---|---|
| Verde (fixa) | Livre |
| Amarela (piscando) | Em uso |
| Vermelha (piscando) | Ocupada |
| Sem luz | Não foi possível obter os dados naquele momento; não quer dizer que o servidor caiu |

No computador, passe o mouse sobre a luz para ver a carga média da região.

**O que fazer quando a luz está vermelha:**

- Vermelho não quer dizer quebrado; quer dizer só que há muita gente naquele momento. Se você já está conectado e a velocidade está boa, deixe como está.
- Se estiver lento, troque para uma região com luz verde. No Cisco, clique em outra bandeira na página para copiar o novo endereço; no Hiddify, importe a configuração de outra região; na Rede privada, troque em Exit Node; no Proxy, clique em outra região no ícone da extensão.
- Cada região tem várias máquinas por trás, e a menos ocupada é escolhida automaticamente quando você conecta. Não precisa escolher a máquina você mesmo.
- Das 20h às 23h é o horário de pico. Nesse período, escolha uma região com luz verde ou troque a forma de conexão; se continuar lento, a causa costuma ser a banda larga local (internet de condomínio, ou operadora e região que não combinam). Para escolher a região pela operadora, veja "Leia também".

## Conectado, mas ainda aparece o local

Em ordem do mais comum para o menos comum:

1. **As regras de roteamento mandam este site direto.** O roteamento automático do Hiddify, o "auto switch" da extensão do Proxy e o modo de roteamento dividido do roteador podem deixar este site fora da VPN. Mude para global temporariamente para conferir; quem usa o Proxy também pode acrescentar este site às regras.
2. **O Proxy Web cobre só aquele navegador.** Olhando de outro navegador ou de um app no celular, é claro que continua aparecendo o local.
3. **Nenhuma saída escolhida na Rede privada.** On-line ≠ passando pela VPN; quando o Exit Node está em None, os aparelhos só se enxergam entre si.
4. **Você está olhando do aparelho errado.** Na opção Roteador, é preciso olhar de um aparelho ligado ao Wi‑Fi daquele roteador, e não de um celular ligado ao Wi‑Fi do modem ou usando dados móveis.
5. **Outra VPN ou ferramenta de rede mesh está ligada ao mesmo tempo.** Uma VPN da empresa ou o acelerador de outro serviço vão brigar pelas rotas. Deixe só uma.
6. **Ainda não atualizou.** Espere dez a vinte segundos, troque de janela ou atualize à mão uma vez.

## A barra superior confere o IP; IPv6 e DNS se conferem à parte

A barra superior olha o endereço IPv4 da conexão que este site recebeu. Se ela mostra o certo, isso só quer dizer que este navegador passou pela VPN ao acessar este site:

- **IPv6 e DNS não aparecem nela.** Quando o navegador acessa este site por IPv6, o campo simplesmente não aparece; ele não vai fazer uma rede errada passar pela certa. Se um site de vídeo continuar mostrando aviso de restrição de direitos autorais, o mais provável é que o IPv6 ou o DNS esteja passando por fora da VPN; veja [03 · IPv6 e DNS são os que escapam](03-ipv6-and-dns-leak.md).
- **Os apps guardam a verificação de região.** A barra superior é consultada do zero toda vez e não é afetada por cache; mas os apps de vídeo e de música lembram a região anterior. Feche por completo e abra de novo; veja [02 · Conectei na China, mas ainda não consigo assistir](02-still-blocked-after-connecting.md).

## Perguntas frequentes

**O campo "Rede atual" sumiu da barra superior?** No computador, entre na conta primeiro. Se depois do login ainda não aparecer, o mais provável é que essa conexão tenha ido por IPv6 ou que não dê para consultar no momento; espere dez a vinte segundos ou atualize. Ele prefere não mostrar nada a mostrar algo errado.

**Mesma região, mas IP diferente em duas conexões?** Normal. Cada região tem várias máquinas por trás, e cada conexão pega a menos ocupada naquele momento. Uma conexão já estabelecida não é mudada de lugar no meio do caminho.

**O estado/província que aparece não é o que eu esperava?** A barra superior mostra o estado/província onde o IP de saída está localizado e só tem precisão até esse nível. Se a bandeira bate, a saída está no país ou na região que você escolheu.

**O que devo informar ao falar com o suporte?** Passe o mouse sobre aquele campo na barra superior e mande o que aparecer (incluindo o IP de saída), junto com a forma de conexão, a região escolhida e o horário em que o problema aconteceu.

## Leia também

- [Como resolver quando não conecta, fica lento ou cai](https://www.leotun.com/pt/guides/connect-issues?utm_source=github&utm_content=troubleshooting-08)
- [Qual região é mais rápida a partir da China](https://www.leotun.com/pt/guides/pick-region?utm_source=github&utm_content=troubleshooting-08)
- [Qual forma de conexão serve para cada situação](https://www.leotun.com/pt/guides/choose-connection?utm_source=github&utm_content=troubleshooting-08)
- [O que é o Proxy Web e quando usar](https://www.leotun.com/pt/guides/web-proxy?utm_source=github&utm_content=troubleshooting-08)
- [O que o firmware do roteador faz](https://www.leotun.com/pt/guides/router-firmware?utm_source=github&utm_content=troubleshooting-08)
- [O que fazer quando o Tencent Video mostra aviso de restrição de direitos autorais no exterior](https://www.leotun.com/pt/guides/overseas-video?utm_source=github&utm_content=troubleshooting-08)

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=troubleshooting-08) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=troubleshooting-08) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 15 créditos (cerca de 15 dias do plano Individual), oferta permanente
