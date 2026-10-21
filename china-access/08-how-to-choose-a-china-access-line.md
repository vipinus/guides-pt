# 08 · Como escolher uma linha para a China: de onde vem o IP chinês e onde as grátis falham

> Versão no site (mais completa): https://www.leotun.com/pt/guides/choose-china-vpn?utm_source=github&utm_content=china-access-08

Uma linha para a China faz uma coisa só: faz os pedidos que você manda do exterior chegarem ao Tencent Video, ao NetEase Cloud Music ou ao seu banco on-line chinês com um IP da **China continental**. Por isso, olhe dois pontos antes de tudo: se a saída é mesmo um IP do continente e se algum tráfego do aparelho está passando por fora dela. Velocidade, preço e cliente vêm depois.

## De onde vem o IP chinês

O provedor precisa ter servidores próprios dentro da China continental. Os provedores de nuvem na China exigem cadastro com nome real para ligar uma máquina e cobram a banda pelo uso, então o custo é muito maior do que o de máquinas fora do país. É por isso que quase todo serviço sério para a China é pago, e que o número de saídas na China é limitado.

Um substituto comum é vender máquinas em Hong Kong, Taiwan ou Japão como se fossem "para a China". Esses endereços servem para algumas seções de Hong Kong, Macau e Taiwan do Bilibili, mas o Tencent Video, o iQIYI e o Youku continuam mostrando restrição de direitos autorais, e o internet banking e o 12306 também tratam você como alguém no exterior. **Como saber: depois de conectar, consulte onde o IP está registrado; só vale se aparecer "China · alguma província".**

## Cinco itens para conferir antes de escolher

| Item | Como conferir | Como fica quando falha |
|---|---|---|
| Região de saída | Consulte onde o IP está registrado depois de conectar | Endereços de Hong Kong, Taiwan, Japão ou Coreia |
| IPv6 e DNS | Pesquise "test ipv6" e abra uma página de teste | O campo IPv6 mostra o país em que você está → os sites de vídeo continuam bloqueando, veja [Solução de problemas 03](../troubleshooting/03-ipv6-and-dns-leak.md) |
| Cliente | Se usa um protocolo padrão (AnyConnect, OpenVPN, Hiddify) | Só existe um app proprietário, e quando ele sai da loja você fica sem nada |
| Banda | Toque um vídeo em 1080p entre 20h e 23h, horário de Pequim | Rápido de dia, carregando sem parar à noite |
| Vários aparelhos e roteador | Quantos aparelhos por conta e se um roteador pode ligar a casa inteira | Cada aparelho precisa ser comprado à parte |

## Por que as linhas grátis para a China vivem caindo

O problema não é ser "grátis", e sim a estrutura de custos. A banda de saída no continente é paga pelo uso, e um serviço grátis só pode escolher uma de três: espremer milhares de pessoas numa máquina só, e todo mundo trava no horário de pico; limitar tráfego e tempo, e um pedido de pagamento aparece no meio do caminho; ou ganhar dinheiro de outro jeito, injetando anúncios, coletando o histórico de navegação ou usando o seu aparelho como saída para outras pessoas.

As extensões de navegador grátis "para a China" têm mais um ponto cego: elas só passam pelo proxy os pedidos de páginas do navegador, e o player de vídeo, os apps e o DNS do sistema não passam por elas, por isso "a página abre, mas o vídeo não toca" é tão comum.

Para consultar alguma coisa de vez em quando, o grátis basta. Para acompanhar séries, ouvir música e usar o internet banking, o tempo que uma linha paga e estável economiza vale muito mais do que a assinatura. Peça primeiro o teste de 4 horas, teste uma vez no pico da noite e só então decida.

## Como estudantes no exterior, viajantes e famílias devem configurar

- **Estudantes no exterior**: as redes dos alojamentos quase sempre têm IPv6, então use um cliente que bloqueie o IPv6; para internet banking, CHSI e 12306, conecte na linha da China só quando precisar e desconecte ao terminar, para reduzir o controle de risco da conta.
- **Viagens curtas**: instale um cliente Cisco ou Hiddify no celular e importe escaneando o QR code; funciona assim que você desembarca.
- **Uma família inteira morando fora por muito tempo**: ligue à linha um roteador com o firmware instalado, e a TV, a TV box e os celulares dos parentes idosos não precisam de configuração; veja [Liberar sites de vídeo chineses com um roteador](../router/06-unlock-chinese-video-with-router.md).

## Um autoteste de 5 minutos

1. Conecte na linha da China; a consulta de IP mostra uma província da China continental.
2. A página de teste de IPv6 mostra que ele está indisponível, ou que também é um endereço do continente.
3. Abra no Tencent Video qualquer série exclusiva da China; ela toca.
4. Toque um vídeo em 1080p mais uma vez depois das 20h, horário de Pequim; ele não fica carregando repetidamente.
5. Troque para outra saída na China e repita os três primeiros passos.

## Perguntas frequentes

**Há diferença entre uma VPN para a China e um "acelerador" para a China?** Nenhuma diferença essencial. Um "acelerador" costuma ser um app personalizado por uma empresa de jogos ou de vídeo que cobre só certos aplicativos; uma VPN é um túnel para o aparelho inteiro.

**Dá para ver o Tencent Video com um nó de Hong Kong?** Não, a licença cobre só o continente.

**Quantos aparelhos por conta?** Na LeoTun, as conexões simultâneas seguem o plano: Individual 2 aparelhos, Família 4, Empresa 8. Um roteador conta como um aparelho, e os aparelhos ligados a ele não entram na conta. Se houver mais aparelhos on-line ao mesmo tempo do que o limite do plano, você pode subir de plano temporariamente (o tempo restante é convertido pelo valor equivalente) e voltar depois.

**Posso usar o Clash?** Pode. A LeoTun oferece uma assinatura sing-box, uma assinatura Clash e um link de compartilhamento hysteria2. Com Clash Meta, Clash Verge, FlClash, Stash e afins, clique no botão "Assinatura Clash" e cole a URL na lista de assinaturas do cliente; não precisa de conversor de assinatura, e não use o link de compartilhamento. O Clash original e o Clash for Windows não servem, porque o núcleo deles não tem hysteria2. Essa assinatura manda por padrão tudo, menos a sua rede local, pelo nó, então nada precisa mudar para vídeos chineses; se você acrescentar regras próprias, não ponha os domínios chineses como "direct" (direto).

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=china-access-08) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=china-access-08) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 15 créditos (cerca de 15 dias do plano Individual), oferta permanente
