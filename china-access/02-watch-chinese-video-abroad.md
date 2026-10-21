# 02 · Assistir vídeos chineses no exterior

> Versão no site (mais completa): https://www.leotun.com/pt/guides/overseas-video?utm_source=github&utm_content=china-access-02

## Por que você não consegue assistir

As plataformas compram direitos só para a China continental, e os IPs de fora são bloqueados em geral. Não é defeito técnico, e trocar o IP é a única solução.

## Diferenças entre as plataformas

| Plataforma | Versão web | App | Observações |
|---|---|---|---|
| iQIYI | Trocar o IP basta | Trocar o IP basta | A edição internacional, iQIYI, é outro app, com menos conteúdo; não instale o errado |
| Tencent Video | Trocar o IP basta | Trocar o IP basta | O mesmo vale para a edição internacional, WeTV |
| Youku | Trocar o IP basta | Trocar o IP basta | |
| Mango TV | Trocar o IP basta | Trocar o IP basta | |
| Bilibili | A maior parte do conteúdo dá para ver mesmo assim | Igual | Só algumas séries de anime e documentários têm restrição de região |
| Yangshipin / CCTV | Trocar o IP basta | Igual | Os canais ao vivo são os mais sensíveis ao IP |

**A armadilha do app internacional**: buscar o nome chinês do iQIYI numa loja de fora da China normalmente leva à edição internacional do iQIYI, cujo catálogo é completamente diferente. Para ver o catálogo chinês, você precisa instalar a edição chinesa do app; no iPhone é preciso um ID Apple da região China, e no Android dá para instalar o APK direto.

## Conectado, mas ainda aparece restrição de direitos autorais

Se o IP de saída já é da China continental e o site ainda mostra restrição de direitos autorais, em nove de cada dez casos o **IPv6 ou o DNS local do aparelho está contornando a linha**. Desde setembro de 2026, as três formas de conexão da LeoTun para o aparelho inteiro bloqueiam o IPv6 do lado da linha; configurações do Hiddify importadas antes de setembro precisam ser apagadas e importadas de novo lendo o QR code. Para os passos de investigação, veja [IPv6 e DNS são os que escapam](../troubleshooting/03-ipv6-and-dns-leak.md).

## Assistir na TV

TVs e TV boxes não instalam aplicativo, então há dois caminhos:

1. **A opção do roteador**: configure a linha para a China no roteador e ligue o roteamento dividido, e a TV assiste assim que se conecta a esse Wi-Fi. A casa toda se beneficia; veja [Para os idosos da família e a TV](../router/04-family-tv-and-router.md).
2. **Espelhar a tela**: ligue a linha para a China no celular e espelhe na TV. É simples, mas o celular precisa ficar ligado o tempo todo.

## Qualidade da imagem

O 1080p precisa de 5 Mbps estáveis ou mais. Se travar no pico da noite, escolha uma região com luz verde ou troque de forma de conexão; se continuar travando, a causa costuma ser a internet local. Escolher um ponto de entrada perto de você e com rota otimizada para o continente funciona melhor do que trocar de plataforma.

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=china-access-02) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=china-access-02) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, oferta permanente
