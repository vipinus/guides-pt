# 03 · Qual região é mais rápida a partir da China: por operadora

> Versão no site (mais completa): https://www.leotun.com/pt/guides/pick-region?utm_source=github&utm_content=overseas-access-03

Com o mesmo serviço e o mesmo protocolo, a velocidade pode variar várias vezes de uma região para outra. A causa não é o servidor, e sim **a rota de saída da sua operadora até aquela região**. Por isso, na hora de escolher a região, olhe primeiro a operadora, depois o horário e só por último o servidor.

## Teste primeiro estas, conforme a operadora

| Sua rede | Teste primeiro | Observações |
|---|---|---|
| China Unicom no norte | Japão, Coreia do Sul | A saída da Unicom para o Japão e a Coreia do Sul costuma ser a mais direta |
| China Telecom no sul | Sudeste Asiático (Singapura), Austrália | A saída da Telecom para o sul é boa |
| China Mobile, Great Wall Broadband e outras | Entrada na China | O cliente se conecta só a um endereço dentro da China e o trecho internacional fica por nossa conta, então ele não sofre com a interferência na fronteira |
| Dados móveis | Varia conforme a operadora; teste separado da banda larga | No mesmo celular, a melhor região no Wi‑Fi e nos dados móveis muitas vezes é diferente |

A lista de regiões da LeoTun mostra a carga atual de cada região com **luzes vermelha, amarela e verde**; entre várias entradas para o Japão, escolha a que está com luz verde.

## Depois, o horário

Das 20h às 23h é o horário de pico. Nesse período, escolha uma região com luz verde ou troque a forma de conexão; se continuar lento, a causa costuma ser a banda larga local: internet de condomínio (banda larga compartilhada do conjunto residencial), ou operadora e região que não combinam; nesse caso, escolha de novo pela tabela acima.

## Por fim, o protocolo

- Rede com muita perda de pacotes (banda larga de prédio antigo, dados móveis): o hysteria2 do Hiddify aguenta bem a perda de pacotes e muitas vezes é o mais rápido.
- Rede de universidade ou de empresa que restringe UDP: o hysteria2 roda sobre UDP e vai ser estrangulado; use o AnyConnect, que roda sobre TLS.
- São seis formas de conexão numa conta só; sempre há uma que combina com a sua rede.

## Um teste de cinco minutos

1. Meça uma vez a velocidade local sem a linha, como teto.
2. Escolha duas regiões da tabela acima, conecte em cada uma e abra o mesmo site de teste de velocidade.
3. Às 21h, teste de novo as mesmas duas regiões.
4. Fique com a que não foi mal em nenhum dos testes como padrão, e a outra como reserva.

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=overseas-access-03) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=overseas-access-03) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 24 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, oferta permanente
