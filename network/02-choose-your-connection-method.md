# 02 · Qual forma de conexão serve para cada situação

Uma conta LeoTun tem seis formas de conexão: Rede privada (Tailscale), Cisco (AnyConnect), OpenVPN, Proxy (Proxy Web), Hiddify e Roteador. Cada forma tem as situações em que funciona melhor, e este artigo responde por situação: primeiro pelo aparelho que você usa, depois pela rede em que você está e por fim pelo que você quer fazer. Cada situação vem com uma recomendação, o motivo e uma alternativa. Guarde uma coisa: são seis formas numa conta só; sempre há uma que combina com a sua rede.

## Pelo aparelho: com o que você entra na internet

- Um celular, viagens a trabalho e a turismo: Cisco ou Hiddify. O Cisco conecta assim que você digita o endereço no app oficial e é o mais estável; o Hiddify é importado escaneando um QR code e é mais rápido quando há muita perda de pacotes. Alternativa: Rede privada.
- O seu próprio computador (Windows, Mac): Hiddify ou Rede privada. O Hiddify é rápido e tem uma chave de roteamento dividido embutida; a Rede privada fica on-line depois de um único login. Alternativa: Cisco.
- Computador da empresa, sem direitos de administrador: Proxy Web. Você só instala uma extensão no navegador, não precisa de direitos de administrador e não mexe nas configurações de rede da empresa.
- iPhone, aparelhos antigos: Cisco. Conecta com a VPN embutida no sistema ou com o cliente oficial, sem importar configuração, e tem a melhor compatibilidade.
- NAS (Synology, QNAP), servidores Linux: OpenVPN. Importe um arquivo .ovpn e ele conecta sozinho ao ligar; a maioria desses aparelhos já vem com cliente embutido.
- TVs, TV boxes, videogames, o celular de um parente idoso: Roteador. Tudo o que entra no Wi‑Fi passa pela linha, e nada precisa ser instalado no aparelho. Os três planos de conta podem usar.
- Muitos aparelhos de uma família inteira ou de um escritório: Roteador, configurado uma vez e valendo para todos; se você também quer acessar o NAS de casa estando fora, acrescente a Rede privada.

## Pelo ambiente de rede: em que rede você está

- Redes de alojamento ou de universidade, redes de empresa que restringem UDP: Cisco. Ele roda sobre TLS, como quem abre um site HTTPS, e é o mais estável em redes restritas; Hiddify, Rede privada e OpenVPN rodam todos sobre UDP e vão ficar lentos ou cair.
- Banda larga que cai com frequência, sinal de Wi‑Fi fraco: Proxy Web. Ele funciona por pedido, sem conexão permanente, então por definição não há conexão para cair.
- Banda larga de condomínios antigos, dados móveis, muita perda de pacotes: Hiddify. O protocolo dele foi feito para aguentar perda de pacotes e dá a melhor velocidade nesse tipo de rede.
- O computador já está ligado a uma VPN da empresa: Proxy Web. Duas VPNs de aparelho inteiro rodando juntas brigam pelas configurações de rede; o Proxy Web cuida só do navegador, então um não atrapalha o outro.
- China Mobile, Great Wall Broadband e outras bandas largas, ou trechos internacionais sempre instáveis: qualquer forma, escolhendo um ponto de entrada da região China. Costuma ser a opção mais estável nessas redes.

## Pelo objetivo: o que você quer fazer

- Você está no exterior e quer ver vídeos chineses: qualquer forma de aparelho inteiro (Cisco, Hiddify, Rede privada, OpenVPN, Roteador) com a região China escolhida; para a TV de casa, use o Roteador. Não use o Proxy Web para vídeo: ele não alcança o canal de rede do próprio aparelho, então o site de vídeo pode continuar vendo você como alguém no exterior.
- Jogos, chamadas de voz e de vídeo: Hiddify, Rede privada ou Roteador, escolhendo a região com menor latência. O Proxy Web cuida só do navegador; jogos e apps de chamada não passam por ele.
- Trabalho de escritório e pesquisa, só no navegador: o Proxy Web dá menos trabalho; se você precisa se conectar aos sistemas internos da empresa, confirme antes se a VPN da empresa pode rodar junto com a nossa e, se não puder, use o Proxy Web.
- Servidores, scripts, linha de comando: OpenVPN; num Linux de mesa você também pode usar a Rede privada ou o Hiddify.
- Acessar o NAS ou as câmeras de casa estando fora: Rede privada. Os aparelhos da mesma conta se enxergam, sem precisar abrir portas no roteador.

## Guia rápido das seis formas: para o que servem / para o que não servem

- Rede privada (Tailscale) — serve para: vários aparelhos, entrar uma vez e esquecer, acessar os aparelhos de casa de fora. Não serve para: redes que restringem UDP (ela só pode depender dos relays do Tailscale, que são lentos), rodar junto com outra VPN.
- Cisco AnyConnect — serve para: redes restritas, computadores da empresa, iPhone, aparelhos antigos; a melhor compatibilidade. Não serve para: quem está na China e não quer que todo o tráfego passe pela linha (é preciso rodar um script de roteamento dividido à parte).
- OpenVPN — serve para: NAS, servidores Linux, roteadores OpenWrt; importe um arquivo e ele conecta sozinho ao ligar. Não serve para: uso diário em celulares e computadores, em que é menos prático que o Cisco e o Hiddify; redes que restringem UDP.
- Proxy Web — serve para: sem direitos de administrador, já ligado a uma VPN da empresa, banda larga que cai com frequência. Não serve para: apps de vídeo, jogos, chamadas; ele cuida só do navegador.
- Hiddify — serve para: quem quer velocidade, redes com muita perda de pacotes; importa por QR code, o mesmo app em cinco plataformas, roteamento dividido embutido. Não serve para: redes que restringem UDP.
- Roteador — serve para: a família inteira, um escritório, aparelhos que não instalam cliente; o firmware tem roteamento dividido embutido e se atualiza sozinho. Não serve para: quem tem um aparelho só e vive na rua (você ainda precisa instalar um cliente para quando sair).

## Escolher a região pela sua banda larga

A mesma forma de conexão pode ter velocidades várias vezes diferentes entre regiões; o motivo está na linha de saída da sua operadora até aquela região, não no servidor. China Unicom no norte: teste primeiro Japão e Coreia. China Telecom no sul: teste primeiro o Sudeste Asiático (Singapura, Malásia, Tailândia, Filipinas, Indonésia) ou a Austrália. Outras bandas largas (China Mobile, Great Wall Broadband e afins): teste primeiro o ponto de entrada da região China.

As luzes vermelha, amarela e verde na lista de regiões mostram a carga de cada região em tempo real; entre várias entradas para o Japão, escolha a que está com luz verde. Das 20h às 23h é o pico no país inteiro; nesse período, escolha uma região com luz verde ou troque a forma de conexão. Se continuar lento, a causa costuma ser a banda larga local (internet de condomínio, ou operadora e região que não combinam).

## Roteamento dividido: direto dentro da China, pela linha para o exterior

Só quem está na China continental precisa de roteamento dividido; quem está no exterior usa o modo global, e ligar o roteamento dividido faria alguns sites darem a volta à toa. No Hiddify, você muda para o roteamento dividido automático no cliente; no Proxy Web, muda para "Split routing" (roteamento dividido) na extensão; o roteador faz o roteamento dividido para todos os aparelhos da rede, e o firmware já vem com ele ligado; com Cisco e OpenVPN, todo o tráfego passa pela linha depois de conectar, e o script de roteamento dividido da seção "Cisco" está disponível; a Rede privada manda o aparelho inteiro pela linha.

Se um site não abrir com o roteamento dividido, mude primeiro para "Global" temporariamente para conferir: se abrir no global, ele não está na lista; se não abrir nem no global, o problema é do próprio site.

## Como trocar quando não funciona

1. Troque primeiro de região. Se outra região conectar, aquele servidor só está temporariamente fora de alcance.
2. Depois troque de rede. Se a banda larga não funcionar, passe para os dados móveis, e vice-versa; a interferência em operadoras diferentes não acontece ao mesmo tempo.
3. Depois troque de forma. Se as que rodam sobre UDP (Hiddify, Rede privada, OpenVPN) não funcionarem, troque para o Cisco, que roda sobre TLS; se as formas de aparelho inteiro vivem caindo, troque para o Proxy Web. O bloqueio de cada protocolo é independente.
4. Se ainda não funcionar, veja o guia de solução de problemas ou pergunte no grupo de suporte, informando a forma de conexão, a região, o texto exato do erro e o horário.

## Perguntas frequentes

**Qual das seis formas é a mais rápida?** Em redes com muita perda de pacotes, o Hiddify é o mais rápido; em redes limpas a diferença é pequena, e o gargalo é a região e o horário, não a forma.

**Qual usar para jogos e chamadas de voz?** Hiddify, Rede privada ou Roteador, escolhendo a região com menor latência. O Proxy Web cuida só do navegador; jogos e apps de chamada não passam por ele.

**Dá para usar as seis formas ao mesmo tempo?** Em aparelhos diferentes, dá; todas as formas da mesma conta dividem a cota de aparelhos on-line ao mesmo tempo (Individual 2, Família 4, Empresa 8). Não rode duas formas de aparelho inteiro ao mesmo tempo no mesmo aparelho (por exemplo, Rede privada e Cisco), porque elas vão brigar pelas configurações de rede.

**Preciso escolher entre roteador e cliente?** Não. Use o roteador em casa e ligue o cliente no celular quando sair; cada um conta como um aparelho.

**Qual usar no Linux?** Rede privada, OpenVPN e Hiddify têm cliente para Linux; o Cisco no Linux usa o OpenConnect, de código aberto; o OpenVPN no Linux pede o usuário e a senha da conta na primeira conexão. Para servidores e NAS, o OpenVPN dá menos trabalho.

## Leia também

- [O que nos diferencia de outras VPNs](https://www.leotun.com/pt/guides/why-us?utm_source=github&utm_content=network-02)
- [O que é a Rede privada (Tailscale)](https://www.leotun.com/pt/guides/tailscale-mesh?utm_source=github&utm_content=network-02)
- [Como usar o OpenVPN e quando escolher](https://www.leotun.com/pt/guides/openvpn-setup?utm_source=github&utm_content=network-02)
- [O que é o Proxy Web e quando usar](https://www.leotun.com/pt/guides/web-proxy?utm_source=github&utm_content=network-02)

Versão deste artigo no site: https://www.leotun.com/pt/guides/choose-connection?utm_source=github&utm_content=network-02

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=network-02) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=network-02) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 24 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, oferta permanente
