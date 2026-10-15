# 01 · Quais serviços exigem um IP chinês

Só existe um critério: quando o serviço vê que o seu IP de origem não é da China continental, ele recusa ou entrega um serviço limitado. A tabela abaixo está ordenada pelo rigor do bloqueio.

| Categoria | Exemplos | O que acontece sem IP chinês | O que é verificado além do IP |
|---|---|---|---|
| Vídeo | iQIYI, Tencent Video, Youku, Mango TV, alguns animes no Bilibili | Aparece que só está disponível no continente, ou você só vê o conteúdo gratuito | Região da loja de apps, onde a conta foi criada |
| Música | NetEase Cloud Music, QQ Music, Kugou | Muitas músicas ficam em cinza e não tocam | Nada |
| Serviços do governo | Plataforma Nacional de Serviços do Governo, sites de serviços das províncias, impostos, previdência social, fundo habitacional | A página não abre, ou o código de verificação nunca chega | Número de celular, reconhecimento facial |
| Educação | CHSI, site de diplomas, sistemas acadêmicos das universidades | Não abre, ou fica lentíssimo | Nada |
| Viagens | 12306, sites de companhias aéreas | Não abre, o pagamento falha | Número de celular, pagamento |
| Finanças | Internet banking, apps de banco, Alipay, WeChat Pay | O login é barrado pelo controle de risco, transferências falham | Chip (SIM), impressão digital do aparelho, rosto |
| Jogos | Jogos de PC e celular em servidores chineses | Você consegue entrar, mas a latência é alta e a conexão cai | Verificação de identidade real |
| Dia a dia | Meituan, Ele.me, DiDi, alguns recursos do Taobao | Erro de localização, pedidos falham | Localização, número de celular |
| Lives | Douyin, Kuaishou, Douyu | Não dá para assistir em algumas regiões | Nada |

## Uma distinção importante

**"Exigir IP chinês" e "exigir número de celular chinês" são coisas diferentes.** Vídeo e música só olham o IP, e trocar o IP basta. Serviços do governo, bancos e compra de passagens, além do IP, exigem que você receba um código por SMS e passe pelo reconhecimento facial. O IP resolve "se abre ou não"; a verificação seguinte depende do seu próprio número chinês e dos seus documentos.

## Como resolver o problema do IP

Mandar o tráfego primeiro para um servidor no continente, que então acessa o destino. Há três formas de fazer isso: um aplicativo cliente, o Proxy Web ou um roteador. Para escolher, veja [Qual forma de conexão serve para cada situação](../network/02-choose-your-connection-method.md) no repositório irmão.

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=china-access-01) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=china-access-01) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 24 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, válido por tempo indeterminado
