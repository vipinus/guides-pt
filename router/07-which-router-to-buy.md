# 07 · Vale a pena ter um roteador? Como escolher entre os quatro modelos

> Versão no site (mais completa): https://www.leotun.com/pt/guides/router?utm_source=github&utm_content=router-07

O roteador resolve o problema de "aparelhos demais, e alguns nem conseguem instalar um aplicativo": a VPN é configurada uma vez no roteador, e a TV, o videogame, a caixa de som inteligente e o celular do parente idoso passam todos por ela automaticamente, sem instalar nada. Basta um roteador que aceite outro firmware e dez minutos de instalação. **Contas Individual, Família e Empresa podem usar roteador.**

## Quando usar e quando não usar

| Use | Não use |
|---|---|
| Você tem em casa aparelhos que não instalam aplicativo, como TV box, videogame, Apple TV ou caixa de som inteligente | Você só tem um celular e um computador e vive viajando a trabalho; instalar o aplicativo é mais leve |
| A família é grande e você não quer ensinar aparelho por aparelho | Você mora em alojamento ou divide apartamento e não controla a rede |
| Você tem aparelhos que precisam ficar conectados 24 horas (NAS, envio de câmeras) | O seu roteador principal é um modem travado pela operadora e não dá para ligar um segundo roteador; nesse caso, um roteador portátil é o meio-termo |
| Um escritório na China ou uma família inteira acessando serviços de fora de forma estável a partir da China, com roteamento dividido no roteador e nada para os aparelhos perceberem | |

## Instalar o firmware ou comprar pronto

Os dois caminhos terminam rodando o mesmo firmware. A diferença é quem faz a instalação e quem se responsabiliza quando algo dá errado.

- **Instalar por conta própria**: você já tem um roteador compatível com OpenWrt (mais de 1000 modelos). O firmware é compilado on-line no site e o link chega por e-mail em 3 a 5 minutos; depois siga o [02 · Instalar o firmware por conta própria](02-flash-firmware-yourself.md) passo a passo (tem vídeo). Serve para quem se sente à vontade com configurações técnicas e quer economizar o aparelho.
- **Comprar pronto**: enviamos um GL.iNet com o firmware já instalado; para os três passos depois de tirar da caixa, veja o [01](01-plug-and-play-router.md). Serve para quem não quer mexer em nada, ou para dar a parentes que não entendem de tecnologia.

Nos dois caminhos o firmware atualiza os componentes sozinho, sem precisar instalar de novo; e quando os endereços das linhas mudam, você também não precisa mudar a configuração.

## Quatro roteadores, conforme o uso

| Modelo | Tipo | Preço | Incluso | O que é | Ideal para |
|---|---|---|---|---|---|
| GL-MT300N-V2 | Mini | US$ 200 | 12 meses de serviço | Do tamanho da palma da mão, alimentado por USB (funciona com power bank); Wi‑Fi só em 2,4 GHz, portas de 100 Mbps | Uma pessoa viajando: cabo ou Wi‑Fi de hotel, um celular e um notebook navegando e assistindo em 1080p. Não serve como roteador principal de casa |
| **GL-MT3000** | Portátil | US$ 300 | 24 meses de serviço | Wi‑Fi 6 dual band com porta 2.5G, um pouco maior que a palma da mão | O roteador principal de uma casa pequena (TV, TV box, vários celulares e computadores) e pequeno o bastante para ir na mochila |
| GL-MT6000 | De mesa | US$ 400 | 24 meses de serviço | Duas portas 2.5G mais quatro portas gigabit, antenas externas, o maior poder de processamento | Casas grandes, muitos aparelhos (uma dúzia ou mais), internet acima de 1 gigabit, 4K e videogame, ou um escritório pequeno. Fica fixo como único roteador |
| GL-XE3000 | Móvel | US$ 400 | 24 meses de serviço | 5G/4G e bateria embutidos; com um chip (SIM) vira uma rede independente, e também aceita cabo | Lugares sem internet fixa: motorhome, obra, feira, aluguel por temporada; ou como reserva da internet de casa |

Os meses inclusos são no plano Individual; no Família viram metade e no Empresa um quarto, o mesmo valor em qualquer caso. Frete grátis para o mundo todo, normalmente em 3 a 14 dias, com devolução em até 30 dias.

### Escolha rápida por situação

- Viaja sozinho, fica em hotel, orçamento apertado → GL-MT300N-V2
- Apartamento ou casa pequena em que a TV e a TV box precisam de vídeo chinês ou de fora → GL-MT3000
- Fica mais em casa, mas quer levar numa viagem de vez em quando → GL-MT3000
- Casa grande, muitos aparelhos, internet acima de 1 gigabit ou escritório compartilhado → GL-MT6000
- Sem internet fixa, ou passa a maior parte do tempo na estrada → GL-XE3000
- Para configurar para pais que não entendem de tecnologia → GL-MT3000, comprado já configurado: é ligar na tomada e funciona

## Por que o GL-MT3000 é a nossa primeira recomendação

- **Um aparelho, dois papéis.** Potente o bastante para ser o roteador principal de uma casa pequena, pequeno o bastante para viajar junto. É o único dos quatro que faz as duas coisas.
- **Não fica ultrapassado tão cedo.** Wi‑Fi 6 e porta 2.5G dão folga para a maioria das internets domésticas. O mini só tem Wi‑Fi em 2,4 GHz e portas de 100 Mbps, que viram gargalo em casa.
- **A conta fecha.** US$ 300 com 24 meses de serviço no plano Individual, contra US$ 200 com 12 meses no mini. Contando o serviço incluso, os US$ 100 a mais compram um aparelho claramente melhor e mais um ano.
- **É o que conhecemos melhor.** A nossa unidade de teste é esse modelo, os firmwares novos são testados nele primeiro, e o [vídeo tutorial de instalação](02-flash-firmware-yourself.md) usa ele. Quando você tiver um problema, temos o mesmo aparelho na mesa para comparar.

Quando não escolher: para casa grande, muitos aparelhos ou internet acima de 1 gigabit, vá direto no GL-MT6000; sem internet fixa, no GL-XE3000; se for só para uma pessoa em viagens e o preço pesar mais, o GL-MT300N-V2 basta.

## Os três problemas mais comuns no começo

- **Sinal de Wi‑Fi fraco, só 20 dBm**: o firmware ajusta a potência sem fio automaticamente conforme as regras do país em que você está, e só passa para o nível do seu país depois que o roteador fica on-line pela primeira vez. Logo depois de instalar, ligue um cabo de rede primeiro.
- **Os sites chineses ficaram lentos** (quando você está na China): o roteamento dividido está desligado e tudo está passando pela rota. Volte o modo para roteamento dividido: ao acessar serviços de fora a partir da China, por padrão só os sites bloqueados usam a rota, enquanto os sites chineses e os sites estrangeiros que já abrem normalmente na China vão direto.
- **Na China, um site estrangeiro não abre**: em "VPN settings" (configurações de VPN), na parte de roteamento dividido inteligente, desmarque "Blocked sites only" (só sites bloqueados pela linha), ou mude para "Global" temporariamente, e tente de novo; se abrir, o site está bloqueado mas ainda não está na lista, então mande o endereço ao atendimento.
- **Está fora da China e quer conteúdo chinês**: escolha Reverse Split (roteamento dividido invertido). Ele inverte o sentido: só os IPs da China continental passam pela rota para a China, e todos os outros sites usam a sua internet local direto. Vídeo, música e apps chineses veem um endereço chinês, enquanto os sites e o streaming locais não fazem desvio. O firmware escolhe o sentido conforme o lugar em que o roteador está, então raramente você precisa mudar. Veja [03 · Roteamento dividido no roteador](03-router-split-routing.md).
- **Um aparelho não passa pela VPN, ou os sites bloqueados não abrem enquanto todo o resto funciona**: esse aparelho tem um DNS privado próprio configurado ("DNS privado" do Android, DNS seguro do navegador), e o roteador não consegue ver qual site ele está procurando; desligue isso.

## Perguntas frequentes

**O roteador conta como um aparelho?** Ocupa uma vaga da conta (pelo plano: Individual 2, Família 4, Empresa 8 aparelhos on-line ao mesmo tempo), e os aparelhos ligados a ele não contam separadamente.

**Dá para usar para assistir vídeos da China estando no exterior?** Dá, escolha a região China para a linha. O roteador coloca a rede local inteira na VPN, e o IPv6 e o DNS dos aparelhos não conseguem escapar, então os avisos de "restrição de direitos autorais" aparecem menos do que quando um celular conecta sozinho. Veja o [06](06-unlock-chinese-video-with-router.md).

**O firmware tem porta dos fundos?** Ele é compilado a partir do OpenWrt, só com o acréscimo do componente que conecta à VPN e das regras de roteamento dividido; a VPN registra só a duração da conexão e o tráfego total, para cobrança, e não registra o que você acessa.

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=router-07) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=router-07) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 24 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, oferta permanente
