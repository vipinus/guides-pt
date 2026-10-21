# 01 · Como funciona o acesso à China a partir do exterior

## O que você vê

Você está fora da China, abre o iQIYI, o Bilibili ou o NetEase Cloud Music e recebe o aviso "Este conteúdo só está disponível na China continental"; o internet banking e o 12306 (site de passagens de trem) simplesmente não abrem, ou o código de verificação nunca chega.

## Só existe uma causa: onde o seu IP está registrado

Quando o seu aparelho entra na internet, a operadora dá a ele um endereço IP público. Existe um registro mundial desses endereços que mostra a que país e a que operadora cada um pertence. As plataformas chinesas de vídeo e música compram direitos só para a **China continental** e não podem, por contrato, transmitir para fora dela; por isso recusam assim que veem um IP estrangeiro.

Bancos e sites de passagens seguem outra lógica. Para eles a questão não é direito autoral, mas controle de risco: um login vindo de IP estrangeiro é tratado como alto risco e bloqueado de cara.

## Como resolver

Fazer com que o IP visto pelo servidor seja da China continental. Para isso, o seu tráfego vai primeiro para um servidor localizado no continente, que então acessa o site de destino por você. O site de destino vê o IP desse servidor e libera.

É isso que uma "linha para a China" faz: ela faz o seu tráfego sair por um IP da China continental.

## Três enganos comuns

- **Trocar o DNS não resolve.** O DNS só traduz nomes de domínio em endereços; o site de destino olha o seu IP de origem, não o DNS que você usa.
- **Algumas plataformas também olham a região do sistema.** Além do IP, algumas verificam o idioma do aparelho e a região da loja de apps; nesse caso, mude também a região do sistema.
- **A velocidade depende da qualidade do caminho entre os dois pontos.** O trecho internacional do exterior até o continente é o gargalo, então escolher um ponto de entrada perto de você e com rota otimizada até a China importa mais do que a configuração do próprio servidor.

## Leia também

- [Qual forma de conexão serve para cada situação](02-choose-your-connection-method.md)
- [Checklist para quando não conecta, está lento ou cai](../troubleshooting/01-cannot-connect-slow-drops.md)

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=network-01) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=network-01) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; cada amigo convidado que pagar rende 20 dias do plano Individual para você e para ele, oferta sem data para acabar
