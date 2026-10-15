# 09 · Instalar o Hiddify em todas as plataformas: Windows, macOS, Linux, Android, iOS

O cliente usado na seção Hiddify deste site é o Hiddify, de código aberto, que já traz o núcleo sing-box embutido, então não há mais nada para configurar depois de instalar. As cinco plataformas usam o mesmo app, mas os obstáculos na primeira abertura mudam: no Windows ele pode ser bloqueado ou apagado pelo antivírus; no Mac pode aparecer que ele "está danificado", e ainda é preciso autorizar uma extensão de rede; no Linux é preciso rodar um comando de autorização antes de o modo VPN funcionar; e no iPhone ele não aparece na loja da China. Este artigo mostra, para cada plataforma, onde baixar, como instalar e o que fazer na primeira abertura, e termina com os passos mais curtos para importar uma assinatura e conectar.

## Onde baixar

| Plataforma | Instalador | Onde baixar |
|---|---|---|
| Windows | Instalador (.exe), só x64 | Área de download da página do Hiddify |
| macOS | .dmg, um pacote só para Apple Silicon e Intel | Área de download da página do Hiddify |
| Linux | .deb (família Debian / Ubuntu), só x64 | Área de download da página do Hiddify |
| Android | .apk, em duas versões: ARM64 e x86-64 | Área de download da página do Hiddify, ou Google Play |
| iPhone / iPad | Hiddify Proxy & VPN na App Store | App Store; exige um ID Apple de fora da região China |

A área de download da página do Hiddify recomenda automaticamente o pacote para o seu sistema atual, e os pacotes para os outros sistemas ficam listados abaixo. Ao lado de cada linha há também um ícone "Site oficial" que leva à página oficial de lançamentos do Hiddify, para você comparar as versões. Os três sistemas de computador (Windows, macOS, Linux) também têm tutoriais em vídeo.

Os instaladores de computador são cópias sem modificação dos pacotes oficiais do Hiddify, nem alterados nem reempacotados. Antes de liberar a instalação você pode conferir por conta própria: envie o instalador ao VirusTotal e veja o resultado; para saber como, veja [Solução de problemas 06](../troubleshooting/06-antivirus-false-positive.md).

## Windows

1. Baixe o instalador na área de download da página do Hiddify e dê dois cliques para instalar. (Nos nossos testes atuais, a Segurança do Windows não acusa nada; se o antivírus que você instalou acusar, veja as perguntas frequentes no fim de [Solução de problemas 06](../troubleshooting/06-antivirus-false-positive.md).)

## macOS

1. Baixe o .dmg na área de download da página do Hiddify, abra e arraste o Hiddify para "Aplicativos".
2. Em "Finder" → "Aplicativos", segure Control e clique no ícone do Hiddify, escolha "Abrir" e clique em "Abrir" de novo na janela.
3. Se mesmo assim não abrir: "Ajustes do Sistema" → "Privacidade e Segurança", clique em "Abrir Mesmo Assim" na seção "Segurança" e digite sua senha para confirmar.
4. Se aparecer que ele "está danificado e não pode ser aberto": o arquivo não está danificado; é o Gatekeeper do sistema bloqueando. Abra o "Terminal", rode o comando abaixo, aperte Return e digite sua senha de login, depois abra o Hiddify de novo:

```bash
sudo xattr -dr com.apple.quarantine /Applications/Hiddify.app
```

Esse comando só remove a marca de quarentena que indica que o arquivo foi baixado, e vale só para este app. **Não** use `sudo spctl --master-disable` para desligar o Gatekeeper da máquina inteira.

Na primeira vez que você clicar em conectar depois de instalar, o sistema também vai pedir autorização para uma "extensão de rede". Se pular esse passo, o ícone fica girando e nunca conecta:

- **macOS 15 Sequoia ou mais recente**: "Ajustes do Sistema" → "Geral" → "Itens de Início e Extensões", role até "Extensões" no fim, mude a visualização para "Por Categoria", clique no ⓘ ao lado de "Extensões de Rede", ative a chave do Hiddify e digite a senha ou use a digital quando pedir.
- **macOS 13 Ventura / 14 Sonoma**: primeiro abra o Hiddify e clique em conectar uma vez, e vai aparecer "Extensão do Sistema Bloqueada"; depois vá a "Ajustes do Sistema" → "Privacidade e Segurança", role até "O carregamento do software do sistema do desenvolvedor … foi bloqueado", clique em "Permitir" e digite a senha.

Num Mac fornecido pela empresa, se esses botões estiverem em cinza, uma política de gerenciamento de dispositivos os bloqueou; fale com a TI ou use os clientes Cisco, OpenVPN ou Rede privada.

## Linux

1. Baixe o .deb na área de download da página do Hiddify e dê dois cliques para instalar pela central de programas, ou abra um terminal na pasta de download e rode (Debian, Ubuntu e derivados):

```bash
sudo apt install ./downloaded-file-name.deb
```

2. Conectar logo depois da instalação dá "operation not permitted" (operação não permitida) e o modo VPN não inicia, porque o deb oficial não vem com essa permissão. Abra um terminal e rode o comando abaixo para autorizar o Hiddify, depois abra o Hiddify de novo:

```bash
echo /usr/share/hiddify/lib | sudo tee /etc/ld.so.conf.d/hiddify.conf && sudo ldconfig && sudo setcap cap_net_admin,cap_net_raw+ep /usr/share/hiddify/hiddify
```

3. **Rode de novo depois de cada atualização do Hiddify**: a autorização fica presa ao arquivo do programa, e a atualização substitui o arquivo, então a autorização se perde.

O pacote deb é x64; em aparelhos Linux ARM use o OpenVPN, e a mesma conta funciona.

## Android

1. Baixe o .apk na área de download da página do Hiddify. A página recomenda automaticamente a arquitetura do seu celular; a grande maioria dos celulares é ARM64. Se você tem acesso ao Google Play, também pode instalar direto pela loja.
2. Se aparecer um aviso sobre "fontes desconhecidas" ou um alerta do app de segurança durante a instalação, permita.
3. Na primeira vez que você tocar em conectar, o sistema pede permissão de VPN; toque em permitir.

## iPhone / iPad

1. Procure "Hiddify" na App Store e instale; é gratuito.
2. Se não encontrar, ou se aparecer "Este app não está disponível no seu país ou região no momento": no iOS, instale pela App Store com um ID Apple de fora da região China (o Hiddify está nas lojas dos Estados Unidos, Hong Kong, Taiwan, Japão e Singapura). Recomendamos criar um novo: na App Store, toque em "Obter" em qualquer app gratuito → "Criar Novo ID Apple", escolha uma região como Hong Kong ou Estados Unidos e "Nenhum" como forma de pagamento. Você troca de conta só na App Store, e o iCloud não é afetado. Para o passo a passo completo, veja [06 · O que fazer quando o iOS não deixa instalar um app](06-ios-app-store.md).
3. Na primeira vez que você tocar em conectar, o sistema pede permissão de VPN; toque em permitir.

**Não** use um ID Apple compartilhado por outra pessoa; ela pode bloquear seu aparelho remotamente.

## Depois de instalar: importe uma assinatura e conecte

1. Entre no site e abra a página do Hiddify.
2. Clique na bandeira da região desejada e aparece um QR code; ou clique em "Importar todas as regiões · seleção automática" no topo da página para importar de uma vez todas as regiões fora da China e deixar o cliente escolher sozinho. **A região China é importada separadamente**: para assistir vídeos ou usar o banco da China estando no exterior, clique na bandeira da China para importar.
3. Abaixo do QR code há três botões, agrupados por tipo de assinatura. O Hiddify usa o primeiro (ele mostra Hiddify / sing-box / GUI.for.SingBox / Karing, com o subtítulo "assinatura sing-box"), e é o mesmo botão no celular e no computador. Celular: toque nele, vá ao Hiddify e adicione conforme o aviso, ou escaneie o código com o Hiddify em outro aparelho. Computador: clique para copiar um endereço https:// e, no Hiddify, clique em "+" → "Add from clipboard" (adicionar da área de transferência).
4. Clique em conectar.

Para a diferença entre os três botões, como importar no Clash e em outros clientes e se a assinatura vence, veja [02 · Como importar um link de assinatura (Hiddify, Clash, Shadowrocket)](02-singbox-subscription-links.md). Se importou e não conecta, veja [Solução de problemas 04](../troubleshooting/04-singbox-import-not-connecting.md).

## Perguntas frequentes

**Vocês modificaram os instaladores?** Não. Os instaladores de computador são cópias sem modificação dos pacotes oficiais do Hiddify. Cada linha da página do Hiddify tem um link para a página oficial de lançamentos, para você comparar as versões, e você ainda pode enviar o arquivo ao VirusTotal para conferir.


**Já rodei o comando xattr no Mac e continua sem conectar?** O mais provável é que a "extensão de rede" não tenha sido autorizada; siga a seção do macOS acima e ative a chave do Hiddify nos Ajustes do Sistema.

**Depois de atualizar o Hiddify no Linux, o modo VPN parou de novo?** É esperado; rode o comando de autorização mais uma vez depois da atualização.

**Funciona em computadores Windows ou Linux com ARM?** Sim, com outra forma de acesso como o OpenVPN, e a mesma conta funciona; os pacotes do Hiddify para computador hoje são só x64.

**Não quer se incomodar com as liberações?** Cisco (Cisco Secure Client), OpenVPN (OpenVPN Connect) e a Rede privada (Tailscale) abrem com dois cliques; o antivírus não acusa, o Mac não diz que estão "danificados", e a conta é a mesma.

## Leia também

- [Página do Hiddify: downloads do cliente e QR codes de cada região](https://www.leotun.com/pt/singbox?utm_source=github&utm_content=client-09)
- [Como importar um link de assinatura (Hiddify, Clash, Shadowrocket)](https://www.leotun.com/pt/guides/singbox-subscription?utm_source=github&utm_content=client-09)
- [Cliente acusado pelo antivírus / Mac diz que está danificado: confira primeiro, depois libere](https://www.leotun.com/pt/guides/antivirus-false-positive?utm_source=github&utm_content=client-09)
- [O que é a autorização de "extensão de rede" no macOS e como permitir](https://www.leotun.com/pt/guides/macos-network-extension?utm_source=github&utm_content=client-09)
- [O que fazer quando o iOS não deixa instalar um app](https://www.leotun.com/pt/guides/ios-app-store?utm_source=github&utm_content=client-09)

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=client-09) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=client-09) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 24 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, oferta permanente
