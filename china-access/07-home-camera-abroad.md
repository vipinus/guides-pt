# 07 · Ver as câmeras da sua casa na China a partir do exterior

> Versão no site (mais completa): https://www.leotun.com/pt/guides/home-camera?utm_source=github&utm_content=china-access-07

## Três casos, cada um com uma solução diferente

| Que tipo de sistema de câmeras você tem em casa | Dá para ver direto do exterior? | Solução |
|---|---|---|
| App do fabricante com nuvem (EZVIZ, Xiaomi, TP-Link, Imou e outros) | Na maioria das vezes sim; em algumas regiões é restrito ou lentíssimo | Passe para um IP chinês e use a edição chinesa do app |
| Um gravador de vídeo em rede (NVR) que só dá para ver na rede local de casa | Não, não existe ponto de entrada público | Coloque um aparelho de casa numa rede privada e faça o aparelho no exterior entrar na rede local de casa por ela |
| App do fabricante, mas o da loja estrangeira é um sistema separado, com servidores próprios | As contas não batem | Instale a edição chinesa do app e use a conta chinesa |

## Caso um: nuvem do fabricante

A câmera envia a imagem para o servidor do fabricante, e o app puxa do servidor. A rota de uma rede de fora até o servidor de um fabricante chinês é ruim, o que aparece como carregamento lento e transmissão cortada. Depois de passar para um IP chinês, você fica numa rota dentro da China, e melhora bastante.

Observe que o app com o mesmo nome numa loja estrangeira normalmente conecta a servidores de fora, e as contas não são intercambiáveis. Instale a edição chinesa do app; para problemas com a região da loja, veja o [guia de instalação](../client/06-ios-app-store.md).

## Caso dois: o gravador só está na rede local

É o caso mais comum e também o mais difícil. O NVR não tem IP público, e redirecionamento de portas quase nunca é possível na internet doméstica da China. O caminho que funciona é uma **rede privada**:

1. Deixe um aparelho sempre ligado em casa; um computador, um NAS, um Raspberry Pi ou um roteador compatível servem. Instale nele o aplicativo da rede privada, coloque-o na sua rede privada e ligue o "compartilhar rede local".
2. Coloque também o celular ou o computador no exterior na mesma rede privada.
3. A partir daí, o aparelho no exterior acessa o NVR direto pelo endereço dele na rede local de casa, como se você estivesse em casa.

A "Rede privada" da LeoTun é exatamente esse tipo de rede privada. Não há limite de aparelhos em que você instala com uma conta, e o número on-line ao mesmo tempo segue o plano: Individual 2, Família 4, Empresa 8. Um aparelho em casa mais alguns no exterior cabe certinho no plano Família.

## Caso três: as contas não batem

Um aparelho comprado na China fica vinculado a uma conta chinesa, e o app da loja estrangeira não consegue entrar nela. A única solução é instalar a edição chinesa do app. Não vincule o aparelho de novo, porque isso derruba a conta da sua família.

## Um lembrete sobre privacidade

A imagem das câmeras da sua casa só deveria circular entre os seus aparelhos e a sua casa. A opção da rede privada prefere uma conexão direta entre os aparelhos e só passa por retransmissão quando a conexão direta não é possível, e a imagem não fica guardada em nenhum servidor; já a opção da nuvem do fabricante passa pelo fabricante. Em qualquer caso, não use "ferramentas de túnel" de origem desconhecida, o que equivale a entregar as câmeras da sua casa a outra pessoa.

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=china-access-07) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=china-access-07) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 24 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, oferta permanente
