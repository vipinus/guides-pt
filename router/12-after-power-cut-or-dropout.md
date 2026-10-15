# 12 · O roteador volta sozinho depois de uma queda de energia ou de conexão?

Quem já montou um roteador com VPN por conta própria provavelmente já passou por isto: falta luz, ou a internet cai por um instante, e depois de reiniciar tudo parece normal, mas o túnel nunca volta até você entrar na página de administração e configurar de novo.

## A resposta curta

Sim, ele volta sozinho. Depois de uma queda de energia e reinício, de uma queda da banda larga ou do túnel caindo no meio do uso, o firmware reconecta por conta própria. Sem página de administração, sem entrar na conta de novo.

## Como ele faz isso

O firmware mantém um verificador rodando o tempo todo, que olha o túnel a cada meio minuto mais ou menos. Quando percebe que o túnel caiu, ele reconecta e recoloca o roteamento dividido no lugar.

No curto intervalo até o túnel voltar, os sites chineses continuam funcionando. A casa não fica sem internet só porque o túnel ainda não subiu.

As suas configurações também ficam guardadas: a região, o modo de roteamento dividido e a chave "Automatically select the fastest line" (escolher automaticamente a linha mais rápida) sobrevivem a reinícios e reconexões. Se você desligou o roteamento dividido, ele continua desligado.

## O que acontece em cada caso

| O que aconteceu | Depois |
|---|---|
| A luz volta depois de uma queda | O roteador liga e o túnel reconecta sozinho |
| A banda larga cai e volta | O túnel reconecta assim que a linha volta |
| O túnel cai no meio do uso | O verificador percebe e reconecta |
| A conta vence | O tráfego deixa de passar pelo túnel e a rede da casa segue funcionando. Depois da renovação, volta sozinho, sem precisar entrar de novo |
| Mudamos o endereço de um servidor | O roteador acompanha. Não há nada para reconfigurar |

## Não voltou depois de alguns minutos? Confira isto

1. **A banda larga em si está funcionando?** Abra um site chinês. Se não abrir, o problema é a linha ou o modem, não o túnel.
2. **A conta venceu?** O túnel não conecta depois do vencimento. Entre no site e confira.
3. **Teste outra região.** Troque de região na página de administração. Às vezes uma região está com um problema temporário.
4. **Reinicie o roteador.** Tire da tomada, espere dez segundos e ligue de novo.
5. Se nada disso resolver, mande ao suporte um print do status que aparece na página de administração.

## O primeiro boot logo depois de instalar o firmware

O primeiro boot é mais lento que o normal: o firmware procura atualizações de componentes e detecta o país para ajustar a potência do Wi-Fi. **Nesse primeiro boot, ligue um cabo de rede.** Wi-Fi fraco antes de ele ter ficado on-line uma vez é normal.

## Perguntas frequentes

**Serve para lugares onde falta luz com frequência?** Serve. Ele reconecta toda vez que a energia volta.

**Preciso reiniciar o roteador de tempos em tempos?** Não.

**As atualizações de componentes vão derrubar a minha conexão?** Não. As atualizações são verificadas e baixadas no boot e só passam a valer no boot seguinte. O roteador não vai reiniciar no meio do seu uso.

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=router-12) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=router-12) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 24 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, oferta permanente
