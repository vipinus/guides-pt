# 05 · Como identificar apps de VPN arriscados

Todo o seu tráfego passa pelas mãos de um app de VPN, e ele pode olhar o que quiser. Dois tipos de coisa no mercado pedem cuidado especial: um é o que no meio chamam de "VPN vermelha", que tem ligação com órgãos de controle, exige a sua identidade real em nome da conformidade e entrega os registros; o outro é o "acelerador" grátis de origem desconhecida, que ganha dinheiro com os seus dados, com o seu aparelho ou com algo que instala nele. O que os dois têm em comum é que "funcionam bem no uso"; o problema está onde você não vê. Abaixo estão dez sinais que você mesmo pode conferir, o que fazer se já instalou um deles e uma autoverificação de três minutos.

## Por que um app de VPN é mais arriscado que um app comum

Uma VPN trabalha no nível do sistema: ela recebe o tráfego de todos os programas do aparelho, inclusive daqueles que você nem sabe que estão rodando em segundo plano. Um app comum vaza os dados que ele mesmo coletou; uma VPN vaza tudo o que você faz naquele aparelho. Por isso, o critério para escolher uma VPN precisa ser muito mais rígido do que para escolher um app comum.

"Usei e não aconteceu nada" não é prova de segurança. Registro, denúncia e injeção acontecem todos no servidor ou em segundo plano e não são percebidos pelo usuário; quando algo dá errado, muitas vezes é meses depois, e não dá para rastrear qual programa foi.

## Dez sinais

- Origem desconhecida: o instalador chega por um grupo de conversa, um drive na nuvem ou um QR code, sem site oficial nem página em loja de apps. Um cliente sério vem de uma loja de apps, do site oficial do desenvolvedor ou de uma página de lançamentos em que dá para conferir a assinatura.
- Pede para você instalar um certificado raiz: durante a instalação, ele pede para "confiar no certificado" ou "instalar o perfil" e exige confiar numa autoridade certificadora (CA). Com o certificado raiz instalado, ele consegue abrir todo o seu tráfego HTTPS, inclusive internet banking e e-mail. Uma VPN normal não precisa desse passo.
- Permissões demais: uma VPN pedindo contatos, SMS, registro de chamadas, localização exata e acesso às fotos. Uma VPN só precisa da permissão para criar o túnel; o resto não serve para nada a ela.
- Exige cadastro com nome real: o cadastro pede documento de identidade, reconhecimento facial ou vincular um número de celular da China continental. É assim que a chamada VPN "em conformidade" liga a sua identidade aos registros do seu tráfego; um serviço sério só precisa de um e-mail.
- Protocolo proprietário + cliente fechado: você só pode usar o app dele, e ele não aceita nenhum protocolo padrão (AnyConnect, OpenVPN, WireGuard, Hiddify), então você não consegue usar um cliente de código aberto de terceiros para conferir o que ele transmite de fato.
- Grátis, sem fonte de renda visível: sem plano pago, sem anúncios, sem clientes empresariais, e mesmo assim funciona ano após ano. A banda de saída na China continental é cobrada pelo uso, e um serviço que não cobra sempre recupera o dinheiro em outro lugar.
- Sem empresa, sem suporte, sem histórico: não dá para encontrar quem opera, não há ninguém para contatar, o domínio foi registrado há menos de um ano, e ele vive trocando de nome e de fachada.
- Tráfego estranho em segundo plano: o aparelho fica enviando dados mesmo quando você não está usando, e a bateria e o pacote de dados acabam rápido. Ele pode estar usando o seu aparelho como saída para outras pessoas ou sincronizando os seus dados.
- A divulgação insiste em "oficial", "registrado", "legal e em conformidade" e sugere que todo o resto é ilegal: é o discurso mais típico de uma "VPN vermelha", e a conformidade dela consiste em registrar e denunciar.
- As notas na loja de apps são só de um lado, as avaliações parecem todas iguais e o número de downloads não bate com o número de avaliações: são falsas.

## Como conferir

1. Veja o protocolo: se o site oficial diz qual protocolo usa e se dá para usar um cliente de terceiros. Com um serviço em que você pode se conectar usando clientes de código aberto ou padrão, como OpenVPN, AnyConnect, Hiddify e Tailscale, você mesmo consegue capturar os pacotes e ver o que é transmitido.
2. Veja as permissões: depois de instalar, vá às configurações do sistema para ver quais permissões ele pediu, desligue tudo o que não for VPN e veja se continua funcionando. Se parar, desinstale.
3. Veja os certificados: no iOS, Ajustes → Geral → VPN e Gerenciamento de Dispositivos; no Android, Configurações → Segurança → Criptografia e credenciais → Credenciais confiáveis → Usuário; no Windows, "Autoridades de Certificação Raiz Confiáveis" no gerenciador de certificados. Se houver um certificado instalado por ele, apague e desinstale o app.
4. Teste vazamentos: depois de conectar, abra uma página de teste de vazamento de DNS e uma de teste de IPv6 para ver se a resolução de nomes e o endereço passam pelos servidores dele; depois abra um site HTTPS e veja se o emissor do certificado é a autoridade certificadora original.
5. Confira quem está por trás: se o site oficial apresenta a empresa ou a equipe, há quantos anos opera e onde fica o suporte; se as regras de reembolso estão por escrito; se a política de privacidade diz com clareza o que é registrado.

## O que fazer se você já instalou um

1. Desinstale o programa e depois confira os lugares citados acima e apague os certificados e perfis que ele instalou.
2. Troque as senhas: internet banking, e-mail, contas que você usa com frequência, principalmente as que você acessou enquanto usava o app.
3. Nas contas com verificação em duas etapas ligada, confira o histórico de login e remova qualquer aparelho desconhecido.
4. Se foi instalado num roteador, restaure as configurações de fábrica e depois instale um firmware oficial ou confiável.

## Como deixamos você conferir

Todos os clientes da LeoTun vêm de fabricantes oficiais e de organizações de código aberto conhecidas: Cisco, OpenVPN, Hiddify e Tailscale, espelhados como são, sem modificações, e você pode trocar a cópia baixada deste site pelo cliente oficial ou de código aberto a qualquer momento. Os protocolos são todos padrão e podem ser conferidos por captura de pacotes.

O cadastro pede só um e-mail, sem número de celular e sem documento. Guardamos só as informações necessárias para a cobrança; não registramos o que você acessa, não injetamos anúncios e não vendemos dados.

Não instalamos certificados e não pedimos contatos nem localização. Se um dia o nosso cliente pedir para você instalar um certificado raiz, com certeza não somos nós.

## Perguntas frequentes

**Então nada grátis presta?** Os clientes da comunidade de código aberto (OpenVPN, Hiddify, Tailscale) são grátis e confiáveis; o risco está num "serviço grátis", não num "programa grátis". Num serviço grátis, veja do que ele vive.

**Estar numa loja de apps quer dizer que é seguro?** Estar na loja só mostra que ele passou pela revisão automática da loja; não quer dizer que o servidor não registre nada. Veja permissões, cadastro com nome real, protocolo e quem está por trás entre os dez sinais acima; a loja não confere isso por você.

**O que é a tal "VPN vermelha"?** É o nome usado no meio para uma VPN com ligação a órgãos de controle, que exige cadastro com nome real em nome da conformidade e guarda registros. Elas costumam se apresentar como "oficiais" e "legais" e funcionam normalmente no uso; o problema é que a sua identidade e todos os registros do seu tráfego ficam amarrados.

**Como saber se uma VPN registrou o meu conteúdo?** Do lado do usuário não dá para saber; o que dá é ver quantos meios de conferência ela oferece: se o protocolo é padrão, se o cliente é de código aberto, se a política de privacidade é específica, se dá para descobrir quem opera. Se não tiver nenhum dos quatro, trate como se registrasse.

**Firmware de roteador também tem esse tipo de risco?** Tem; um "firmware para furar o bloqueio" de origem desconhecida pode sequestrar toda a rede da casa. Instale só o OpenWrt oficial ou um firmware cujo código-fonte possa ser conferido; o firmware deste site é compilado a partir do OpenWrt, com o acréscimo apenas dos componentes para se conectar à linha e das regras de roteamento dividido.

## Leia também

- [O que nos diferencia de outras VPNs](https://www.leotun.com/pt/guides/why-us?utm_source=github&utm_content=network-05)
- [VPN para a China: grátis ou pago](https://www.leotun.com/pt/guides/free-vs-paid?utm_source=github&utm_content=network-05)
- [O que fazer quando o Tencent Video mostra restrição de direitos autorais no exterior](https://www.leotun.com/pt/guides/overseas-video?utm_source=github&utm_content=network-05)
- [Sobre nós: como o serviço é montado e o que registramos](https://www.leotun.com/pt/about?utm_source=github&utm_content=network-05)

Versão deste artigo no site: https://www.leotun.com/pt/guides/risky-vpn-apps?utm_source=github&utm_content=network-05

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=network-05) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=network-05) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 24 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, oferta permanente
