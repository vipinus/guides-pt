# 07 · Acessar ferramentas de IA (ChatGPT, Claude, Gemini e outras)

## O que você vê

Quando você abre esses sites de dentro da China, os sintomas variam, e é fácil se enganar:

| Sintoma | Causa mais provável |
|---|---|
| A página não abre de jeito nenhum | Não dá para alcançá-la no nível da rede |
| A página abre, mas o login trava | O serviço de terceiros usado no login não está acessível |
| Dá para conversar, mas corta assim que você manda algo longo | A conexão está instável |
| A mensagem "não disponível no seu país" | O provedor está recusando pelo IP |
| Um aviso de que a conta foi bloqueada ou precisa de verificação | Veja "O ponto mais importante" abaixo |

## O ponto mais importante: estável importa mais que rápido

Esses serviços são especialmente sensíveis a **trocas frequentes de IP**. Se a sua conexão sai pelo Japão num momento e pelos Estados Unidos no outro, o que o provedor vê é "a mesma conta atravessando vários países em poucos minutos", o que dispara o controle de risco com facilidade: na melhor das hipóteses pedem uma nova verificação, na pior a conta é bloqueada.

Por isso, ao usar ferramentas de IA:

- **Escolha uma região e fique nela**; não troque toda hora
- Faça o cadastro e o uso do dia a dia na **mesma região** sempre que possível
- Se você se cadastrou pelos Estados Unidos, continue usando os Estados Unidos dali em diante

Isso importa muito mais que "qual região é mais rápida". Um pouco menos de velocidade só significa esperar um pouco mais; um problema com a conta significa começar do zero.

## Qual região escolher

Japão e Singapura são próximos, têm baixa latência e são os mais agradáveis para conversar no dia a dia. Mas há dois cuidados:

- Alguns serviços têm disponibilidade diferente conforme a região, então, antes de se cadastrar, confirme que o serviço abre normalmente por aquela região
- Se os recursos que você quer envolvem pagamento, é melhor que o país da sua forma de pagamento não contradiga a região escolhida

Se não tiver certeza, use o teste grátis para abrir cada serviço que pretende usar e dar uma olhada, e depois decida qual região usar a longo prazo.

## Roteamento por app no aplicativo é muito útil

As ferramentas de IA normalmente são usadas no navegador ou num app próprio. Coloque só esse na lista que passa pela linha e deixe os outros apps na rede local. As vantagens:

- Os apps chineses de delivery, transporte por aplicativo e pagamento não são afetados
- A sua região não é "trocada sem querer" por causa de outro app
- Economiza dados

## Linha de comando e API

Se você chama a API por ferramentas de linha de comando ou por código, observe que esses programas **não necessariamente leem o proxy do sistema**. Para esse caso, veja [05 · Linux e linha de comando](05-linux-server.md).

## Um lembrete

Não cole segredos da empresa, dados de clientes ou código não lançado nesses serviços. Isso não tem nada a ver com a linha que você usa: depois que o conteúdo é enviado, ele está nos servidores do outro lado.

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=overseas-access-07) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=overseas-access-07) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 24 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, oferta permanente
