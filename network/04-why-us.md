# 04 · O que nos diferencia de outras VPNs

As VPNs do mercado se dividem, grosso modo, em três tipos: as grandes marcas internacionais voltadas para o mundo todo, os provedores de linhas de proxy populares entre quem fala chinês (vendem assinaturas de proxy revendidas) e os mais variados programas grátis. A LeoTun opera servidores próprios desde 2006 e faz uma coisa só: manter a conexão estável nos dois sentidos para quem está na China continental e para chineses que moram fora. Este artigo nos coloca lado a lado com os três tipos de produto, item por item, mostrando para quem cada um serve e como trabalhamos, para você ver tudo claramente antes de pagar.

## Nosso posicionamento em uma frase

Somos um serviço **otimizado especificamente para a rede da China continental**, não um revendedor de linhas internacionais. A qualidade das saídas internacionais da China Telecom, da China Unicom e da China Mobile varia muito; ajustamos para cada operadora separadamente e recomendamos regiões diferentes para cada uma. Temos nós de entrada dentro da China, para que quem tem uma internet mediana também tenha um ponto de entrada estável. Seguimos ajustando portas e protocolos conforme a rede na China muda, em vez de configurar uma vez e esquecer.

No sentido contrário, quem está fora da China e precisa acessar serviços chineses só escolhe a região China com a mesma conta: os sites chineses saem por um IP da China, enquanto os sites de fora continuam saindo fora da China. Acessar a China do exterior e acessar o exterior a partir da China são os dois sentidos da mesma coisa.

## Comparado com as grandes marcas internacionais

- Pontos fortes delas: dezenas de países, milhares de servidores, apps maduros, políticas de não registro auditadas por terceiros. Se você está na Europa ou nas Américas e só quer criptografia no Wi‑Fi público ou assistir ao streaming de outro país, são uma boa escolha.
- Pontos fracos delas: o produto não foi pensado para a rede chinesa. A assinatura de um protocolo proprietário é fixa, e quando ela é identificada na China o app inteiro para de funcionar; elas não têm nós de saída dentro da China, então, para assistir vídeos chineses no exterior, ou não oferecem o recurso ou usam IPs de Hong Kong ou Taiwan, que o Tencent Video e o iQIYI bloqueiam do mesmo jeito.
- O que nós fazemos: usamos só protocolos padrão (AnyConnect, OpenVPN, Hiddify, Tailscale, Proxy Web por HTTPS), com aplicativos que vêm dos fabricantes ou da comunidade de código aberto. O que pode ser bloqueado é só um endereço específico, e basta trocar o endereço; o aplicativo não cai junto.
- O que escolhemos não ter: 24 regiões, cada uma com várias máquinas, e a menos ocupada é escolhida automaticamente quando você conecta; os aplicativos são as versões oficiais dos fabricantes e da comunidade de código aberto, configurados por QR code ou importação com um clique; não temos relatório de auditoria de terceiros; o que registramos e o que não registramos está escrito na página Sobre, e contamos com deixar isso explícito, não com um selo.

## Comparado com os provedores de linhas de proxy

- Pontos fortes dos provedores de linhas: baratos, muitos nós, funcionam assim que você cola um link de assinatura, e quem gosta de mexer em aplicativos curte a liberdade.
- Pontos fracos dos provedores de linhas: a maioria é de pessoas ou equipes pequenas que alugam máquinas fora da China e revendem tráfego, sem ponto de entrada próprio na China, e a qualidade da saída varia com as linhas alugadas; sumir com o dinheiro, mudar de nome e fechar são coisas comuns, e pagar um ano não garante que você vai usar o ano inteiro; a configuração dos aplicativos fica quase toda por conta do usuário, e ninguém se responsabiliza quando algo dá errado.
- O que nós fazemos: as máquinas são nossas, e as saídas na China são máquinas nossas, registradas com nome real em provedores de nuvem do continente; uma conta tem seis formas de conexão, e a solução de roteador para a casa toda e o grupo de suporte 24 horas são coisas que os provedores de linhas não têm; operamos de 2006 até hoje, e contas, validade e preços não mudaram antes nem depois da troca de nome.
- Nossos preços: plano Individual US$ 4 por mês, Família US$ 8, Empresa US$ 16, o que cobre máquinas próprias, seis formas de conexão e o grupo de suporte 24 horas; você só escolhe a região, e por trás de cada região o sistema escolhe a máquina menos ocupada, sem precisar testar velocidade e escolher nós por conta própria.

## Comparado com programas grátis

- Pontos fortes do grátis: não custa nada e serve para uma consulta de vez em quando.
- Pontos fracos do grátis: a banda de saída no continente é cobrada pelo uso, então um serviço grátis só se sustenta amontoando usuários, limitando a velocidade ou vendendo dados; as extensões de navegador só passam as requisições das páginas, e vídeo, apps e o DNS do sistema não passam por elas; instaladores de origem desconhecida já são um risco por si só, veja "Como identificar apps de VPN arriscados".
- O que nós fazemos: o teste grátis de 24 horas não pede cartão de crédito e serve para conferir o serviço; pagar por dia (créditos) é para quem usa de vez em quando; quando um amigo convidado paga, cada um ganha 20 dias (base do plano Individual), uma fonte permanente de tempo grátis.
- Como organizamos: o tempo grátis vem do teste de 24 horas e dos bônus por convite; para uso contínuo, você paga por mês, por ano ou por dia.

## Seis formas de conexão, uma conta

Rede privada (Tailscale): entre uma vez, fique on-line para sempre e troque de região pelo menu. Cisco AnyConnect: a melhor compatibilidade, já vem no sistema ou tem aplicativo oficial. OpenVPN: para roteadores, NAS e Linux. Proxy Web: só o navegador passa por ele e, por design, não há conexão para cair. Hiddify: aguenta perda de pacotes e tem a melhor velocidade. Roteador: acesso para a casa toda, incluindo TVs, TV boxes e os aparelhos dos parentes idosos.

Cada rede tem a forma que funciona melhor nela, por isso você leva as seis: com a mesma conta você troca quando quiser, do Hiddify para o AnyConnect quando a rede da universidade restringe UDP, para o Proxy Web quando a internet está instável. Para escolher, veja "Qual forma de conexão serve para cada situação".

## Regras da conta

- As contas têm três planos, Individual, Família e Empresa, com 2, 4 e 8 aparelhos on-line ao mesmo tempo, respectivamente; regiões, tráfego e formas de conexão são iguais nos três. Não há limite de aparelhos em que você instala, só de conexões simultâneas. Se passar do limite do plano, você pode subir de plano temporariamente (o tempo restante é convertido pelo valor equivalente) e voltar quando terminar.
- Você pode trocar entre os três planos a qualquer momento, com o tempo restante convertido pelo valor equivalente (Família e Empresa custam 2 e 4 vezes o Individual); os três planos funcionam com roteador, e o Individual basta para uma pessoa só.
- O reembolso é proporcional ao tempo usado, pode ser pedido a qualquer momento e é feito manualmente; não prometemos um prazo exato para o dinheiro cair.
- Velocidade: garantimos YouTube sem travar, mesmo no horário de pico da noite, desde que a sua internet seja boa: China Unicom no norte ou China Telecom no sul. A exceção é a banda larga compartilhada de condomínio (a internet coletiva que alguns prédios na China revendem aos moradores). Se uma região estiver lenta, troque de região ou de forma de conexão.
- As configurações do Hiddify e do OpenVPN levam os dados da sua conta, e trocar a senha invalida as configurações antigas: se perder o celular ou um link vazar, uma troca de senha recupera tudo, e depois é só importar de novo.

## Como trabalhamos

- Guardamos só as informações necessárias para a cobrança. Não registramos o que você acessa, não inserimos anúncios e não vendemos dados.
- Todos os aplicativos vêm de fabricantes oficiais e de organizações de código aberto conhecidas: Cisco, OpenVPN, Hiddify e Tailscale, espelhados exatamente como são, sem modificação; a configuração é por QR code ou importação com um clique.
- A região China roda em máquinas no continente, e os IPs de saída dela ficam todos na China continental.

## Perguntas frequentes

**Vocês são mais seguros que as grandes marcas internacionais?** A força da criptografia é equivalente; os dois usam protocolos padrão. A diferença está no modelo de confiança: as grandes marcas contam com relatórios de auditoria; nós guardamos só o necessário para a cobrança, e todos os aplicativos vêm de fabricantes oficiais e de organizações de código aberto conhecidas.

**Por que não oferecem centenas de nós como os provedores de linhas?** Mais nós não significa mais estabilidade. Por trás de cada região nossa há várias máquinas, e ao conectar o sistema escolhe a menos ocupada, sem você precisar testar velocidade e escolher nós; quando um endereço é bloqueado ele é trocado automaticamente, e o endereço no seu aplicativo não precisa mudar.

**Dá para ficar mais barato?** O plano Individual custa US$ 4 por mês, e quanto mais tempo você compra, maior o desconto (5% → 10% → 20%); por dia, com créditos, sai por cerca de US$ 0,32; quando um amigo convidado paga, cada um ganha mais 20 dias (base do plano Individual), sem limite de pessoas. O cadastro ainda vem com teste grátis de 24 horas.

**Como posso conferir o que vocês dizem?** Pegue o teste de 24 horas, conecte na região China no horário de pico da noite e assista a um episódio no Tencent Video, conecte numa região de fora e abra o YouTube, e confira a localização registrada do IP e uma página de teste de IPv6. A lista de verificação está em "Como escolher uma VPN para a China".


## Leia também

- [Qual forma de conexão serve para cada situação](https://www.leotun.com/pt/guides/choose-connection?utm_source=github&utm_content=network-04)
- [Como identificar apps de VPN arriscados](https://www.leotun.com/pt/guides/risky-vpn-apps?utm_source=github&utm_content=network-04)
- [VPN para a China: grátis ou pago](https://www.leotun.com/pt/guides/free-vs-paid?utm_source=github&utm_content=network-04)
- [Sobre nós: como é feito e o que registramos](https://www.leotun.com/pt/about?utm_source=github&utm_content=network-04)

Versão deste artigo no site: https://www.leotun.com/pt/guides/why-us?utm_source=github&utm_content=network-04

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=network-04) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=network-04) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 24 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, oferta permanente
