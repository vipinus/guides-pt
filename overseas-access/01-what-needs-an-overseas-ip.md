# 01 · Quais serviços exigem um IP de fora da China e como a linha funciona

O critério é o inverso do acesso à China a partir do exterior: quando o serviço vê que o seu IP de origem está na China continental, ou você nem consegue chegar aos servidores dele, ele não abre, fica limitado ou extremamente lento. A tabela abaixo está organizada por finalidade.

| Categoria | Exemplos | O que acontece sem a linha | O que você precisa além do IP |
|---|---|---|---|
| Trabalho | Google Workspace, Slack, Zoom, Teams, Notion | Não abre, ou cai o tempo todo | Uma conta da empresa |
| Desenvolvimento | GitHub, npm, Docker Hub, fontes do PyPI que não sejam espelhos, Stack Overflow | Tão lento que dá timeout | Nada |
| IA | ChatGPT, Claude, Gemini | Não abre | País de cadastro da conta, número de celular |
| Pesquisa | Google Acadêmico, bases de artigos científicos, e-mail da universidade | Não abre, ou extremamente lento | Uma conta da universidade |
| Jogos | Steam em regiões fora da China, PSN, Switch eShop, servidores internacionais | A loja não abre, latência alta | Uma conta da região daqueles servidores |
| Vídeo e música | YouTube, Netflix, Disney+, Spotify | Não abre | Uma conta paga, e a região da conta precisa bater com o IP |
| Redes sociais | X, Instagram, Telegram, Discord, WhatsApp | Não abre | Número de celular |

## Uma distinção importante

**"Exigir IP de fora da China" e "exigir uma conta estrangeira" são coisas diferentes.** Para GitHub e YouTube, trocar o IP basta; a Netflix exige uma conta paga com região compatível; o cadastro no ChatGPT exige um número de celular estrangeiro que receba o código de verificação. A linha resolve "se abre ou não"; a conta é com você.

## Como a linha funciona

O seu tráfego é primeiro criptografado e enviado a um servidor fora da China, que então acessa o destino. O que o destino vê é o IP desse servidor. Há três formas de fazer isso: um aplicativo cliente, o Proxy Web e um roteador. Para escolher, veja [Qual forma de conexão serve para cada situação](../network/02-choose-your-connection-method.md).

## Três enganos comuns

- **Trocar o DNS não resolve.** Não conseguir conectar é problema de caminho, não de resolução de nomes.
- **A velocidade depende do caminho entre os dois pontos.** Saindo da China, o gargalo é o trecho internacional e a saída da sua operadora, então escolher a região importa mais do que a configuração do servidor; veja o [03](03-which-region-is-fastest.md).
- **Enquanto você usa apps chineses, nem tudo precisa passar pela linha.** Ative o roteamento dividido: por padrão, só os sites bloqueados passam pela linha, enquanto os sites chineses e os sites estrangeiros que já abrem normalmente na China conectam direto, sem desvio; veja [Roteamento dividido no roteador](../router/03-router-split-routing.md).

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=overseas-access-01) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=overseas-access-01) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, válido por tempo indeterminado
