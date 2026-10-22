# 12 · Como se preparar para viagens a trabalho e a turismo

Para uma viagem curta ao exterior ou uma viagem a trabalho para a China, você não precisa de roteador nem de estudar protocolos: instale o cliente Cisco (Cisco Secure Client) no celular, teste a conexão uma vez antes de sair e ele funciona assim que você desembarca. Os dois sentidos são a mesma coisa: fora da China, quando precisar de Google, e-mail da empresa e mapas, escolha uma região de fora próxima; na China, quando quiser ver vídeos chineses e entrar no internet banking chinês, escolha a região China. Este artigo cobre os dez minutos de preparação antes de sair, duas armadilhas comuns das redes de hotel e de aeroporto e como usar o internet banking e os apps de pagamento.

## Dez minutos antes de sair

1. Instale o Cisco Secure Client no celular (App Store / Google Play, ou o instalador da página do Cisco neste site), entre no site e clique numa bandeira para copiar o endereço de uma região e colar no cliente, depois conecte uma vez com o usuário e a senha da sua conta deste site para confirmar que funciona.
2. Copie os endereços de mais duas regiões e salve no cliente: uma perto do seu destino e uma de reserva. A rede lá vai ser diferente, e a melhor região muitas vezes não é a mesma.
3. Anote os quatro domínios (leotun.com → 7d24hrs.com → 7x24btc.com → anyfq.com) e a entrada de pelo menos um grupo de suporte, para ter a quem recorrer se algo der errado num lugar cuja rede você não conhece.
4. Instale também no notebook, ou use a extensão do Proxy Web; ela funciona mesmo quando o computador da empresa não deixa instalar cliente.

## Depois de desembarcar

- Se você trocou para um chip local ou ligou o roaming, o cliente conecta direto e não precisa reconfigurar nada; se os dados em roaming já saem do país de origem, conectar a linha serve só para acertar a região de saída.
- Fora da China, quando precisar de Google, Gmail, e-mail da empresa e mapas: escolha uma região de fora próxima, para ter a melhor velocidade.
- Na China, quando quiser ver Tencent Video e iQIYI, ouvir NetEase Cloud Music ou entrar no internet banking: escolha a região China. Os sites chineses saem por um IP chinês e os sites de fora continuam saindo fora, então conectar na região China estando na China não impede que você continue usando o Gmail.
- Se uma região de fora não conectar de dentro da China: troque de região, passe para os dados móveis e, se ainda falhar, troque para o Hiddify ou o OpenVPN; o bloqueio de cada um dos três protocolos é independente.

## Duas armadilhas das redes de hotel, aeroporto e café

- Portal de login (captive portal): depois de entrar no Wi‑Fi, conclua primeiro a autenticação no navegador e só depois ligue a linha. Um cliente configurado para conectar automaticamente vai tentar antes da autenticação e falhar; espere um pouco ou reconecte à mão.
- Restrição de UDP: muitas redes de hotel e de aeroporto limitam ou bloqueiam UDP. O Cisco roda sobre TLS e não é afetado, e é por isso que ele é a primeira recomendação para viagens; se você estiver usando o Hiddify ou a Rede privada e ficar lento ou cair, troque para o Cisco.

## Internet banking, pagamentos, 12306

Esses apps registram o IP de login, e pular de um lado para o outro entre o exterior e a China é o que mais aciona o controle de risco. Quando precisar resolver algo, conecte primeiro na região China e só depois abra o app; ao terminar, feche o app e só então desconecte. Durante a viagem, não use o mesmo internet banking alternando com frequência entre os dois tipos de rede.

Códigos de verificação por SMS que nunca chegam não têm nada a ver com a linha; é questão de roaming do número de celular. Antes de sair, ative o roaming do seu número chinês ou mude para um plano que receba códigos no exterior.

## Perguntas frequentes

**A viagem é de poucos dias. Preciso comprar um mês?** Não. Peça o teste grátis de 4 horas, ou recarregue créditos e pague por dia: o plano Individual gasta 1 crédito por dia, cerca de US$ 0,4 por dia, o que combina bem com poucos dias.

**O celular e o notebook podem conectar ao mesmo tempo?** Podem. Conforme o plano, uma conta tem 2 / 4 / 8 aparelhos on-line ao mesmo tempo (Individual / Família / Empresa), e o plano Individual dá exatamente um celular mais um notebook.

**Por que o Cisco é recomendado para viagens e não o Hiddify?** Numa rede desconhecida, a maior preocupação é o UDP restrito. O Cisco roda sobre TLS, como quem acessa um site HTTPS, e passa em quase qualquer lugar; o Hiddify é mais rápido em redes com muita perda de pacotes, mas não funciona quando o UDP é restrito. Instalar os dois e trocar quando um não funcionar é o mais garantido.

**Usar a região China no exterior deixa os sites locais mais lentos?** Os sites locais ficam mais fluidos com conexão direta: desconecte quando terminar o conteúdo chinês, ou conecte só quando precisar.

## Leia também

- [Cisco AnyConnect: download e configuração](https://www.leotun.com/pt/anyconnect?utm_source=github&utm_content=china-access-12)
- [Como estudantes no exterior devem configurar uma VPN para a China](https://www.leotun.com/pt/guides/students?utm_source=github&utm_content=china-access-12)
- [Como falar com a gente e não perder o contato](https://www.leotun.com/pt/guides/stay-in-touch?utm_source=github&utm_content=china-access-12)
- [VPN para a China: grátis ou pago](https://www.leotun.com/pt/guides/free-vs-paid?utm_source=github&utm_content=china-access-12)

Versão deste artigo no site: https://www.leotun.com/pt/guides/travel?utm_source=github&utm_content=china-access-12

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=china-access-12) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=china-access-12) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 15 créditos (cerca de 15 dias do plano Individual), oferta permanente
