# 03 · Usar sites do governo e de serviços públicos da China

## O que acontece

A Plataforma Nacional de Serviços do Governo, os sites de serviços dos governos provinciais e municipais, a receita federal eletrônica, as consultas de previdência social e do fundo habitacional (housing provident fund), o CHSI (o sistema oficial de diplomas), o 12306 (venda de passagens de trem): do exterior, ou eles não abrem, ou abrem mas o código de verificação nunca chega ou o reconhecimento facial falha.

## Primeiro descubra em que camada está o problema

| Sintoma | Causa | Solução |
|---|---|---|
| A página nem abre ou dá tempo esgotado | O site só aceita IPs da China continental, ou os pacotes estão sendo descartados na linha internacional | Troque para um IP chinês |
| Abre, mas o código de verificação por celular nunca chega | O SMS precisa ir para um número de celular chinês | Mantenha um chip chinês e ative o roaming internacional para receber SMS |
| O código chega, mas o reconhecimento facial falha | Você está usando a versão de uma loja de apps de fora, ou é a permissão da câmera | Instale a versão chinesa do app e libere a câmera |
| Aparece "o ambiente de rede atual está anormal" | O controle de risco detectou sinais de proxy | Tente de novo com outra região de entrada, ou use a opção do roteador (ela parece mais com uma banda larga doméstica) |

## O caso do 12306

O 12306 é extremamente sensível ao IP, e com um IP de fora às vezes nem a página inicial abre. Depois de trocar para um IP chinês: o cadastro exige um número de celular chinês, a compra exige um documento com nome real, e o pagamento passa por um cartão de banco chinês ou pelo Alipay. Você precisa dos três para conseguir comprar. Nos picos de corrida por passagens, ele também limita a quantidade de pedidos de um mesmo IP, então não abra várias janelas atualizando sem parar.

## CHSI e verificação de diploma

O CHSI em si não é muito rígido com IPs de fora; o problema principal é a lentidão. Mas o SMS de verificação dele também só vai para números chineses. Antes de fazer uma verificação de diploma, quem estuda ou mora no exterior deve confirmar primeiro que o número chinês ainda recebe SMS.

## Uma sugestão

Tarefas com o governo muitas vezes aparecem só uma ou duas vezes por ano, e procurar uma linha em cima da hora toda vez dá muito trabalho. Deixar a linha para a China configurada como um ponto de entrada fixo e voltar quando terminar dá menos trabalho do que configurar tudo de novo a cada vez.

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=china-access-03) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=china-access-03) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 24 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, oferta permanente
