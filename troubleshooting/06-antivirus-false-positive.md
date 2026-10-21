# 06 · O que fazer quando o Mac diz que o app "está danificado"

> Versão no site (mais completa): https://www.leotun.com/pt/guides/antivirus-false-positive?utm_source=github&utm_content=troubleshooting-06

Primeiro a conclusão: o arquivo não está estragado e ninguém mexeu nele. Quando você dá um duplo clique no Hiddify no Mac e aparece "está danificado e não pode ser aberto" ou "o desenvolvedor não pode ser verificado", é o Gatekeeper do sistema bloqueando; siga os passos abaixo para liberar.

Nos nossos testes atuais, instalar o Hiddify no Windows não dispara mais alerta de vírus. Se o antivírus que você instalou acusar mesmo assim, siga a mesma ordem daqui: primeiro verifique, depois libere.

## Por que ele é bloqueado

**Arquivos baixados de uma página da web recebem uma marca de quarentena.** Quando o Gatekeeper do macOS vê essa marca, bloqueia o app. A mensagem às vezes diz "está danificado" e às vezes "o desenvolvedor não pode ser verificado"; a causa é a mesma.

O que fazemos: o cliente de computador é um **espelho sem modificações** do pacote de lançamento do projeto de código aberto original. Não alteramos, não reempacotamos e não injetamos nada; só hospedamos no nosso próprio site de downloads para facilitar o download.

## Verifique você mesmo antes; não libere às cegas

Liberar um app significa que o sistema para de checá-lo, então a ordem é verificar primeiro e liberar depois.

**Envie para o VirusTotal para uma segunda checagem.** Arraste o instalador para o [virustotal.com](https://virustotal.com/gui/home/upload). Alguns mecanismos heurísticos acusando enquanto os grandes fabricantes todos aprovam é o padrão típico de falso positivo. Se a maioria dos mecanismos principais acusar, **não instale** — fale direto com a gente.

Continue só depois que passar na checagem. Se estiver em dúvida, fale com o suporte antes e nós conferimos o site de downloads.

## Três jeitos de liberar, do mais restrito ao mais amplo

Depois do duplo clique, pode aparecer "“Nome do cliente” está danificado e não pode ser aberto. Você deve movê-lo para o Lixo." ou "não pode ser aberto porque o desenvolvedor não pode ser verificado". Os três passos abaixo vão do mais restrito ao mais amplo; **se o primeiro funcionar, não use o terceiro**.

1. Encontre o app em "Aplicativos" no Finder, clique no ícone com a tecla Control pressionada (ou com o botão direito), escolha "Abrir" e clique em "Abrir" mais uma vez na janela que aparecer. Isso é uma liberação única, só para esse app.
2. Se o menu do botão direito não tiver um "Abrir" que funcione, vá em "Ajustes do Sistema" → "Privacidade e Segurança" e role até a parte de Segurança. Vai aparecer "O uso de “Nome do cliente” foi bloqueado porque não é de um desenvolvedor identificado". Clique em "Abrir Mesmo Assim" à direita e digite a sua senha para confirmar.
3. Se a mensagem for "está danificado", os dois primeiros passos normalmente não funcionam. Abra o "Terminal" e rode `sudo xattr -dr com.apple.quarantine` seguido do caminho do app (normalmente um `.app` dentro de `/Applications/`), tecle Return, digite a sua senha de login e abra o app de novo. O que esse comando faz é remover a marca de quarentena que indica a origem do download.

Na primeira abertura, o sistema também vai pedir a sua senha para autorizar a instalação de uma extensão de rede. Só depois que você concordar o app consegue assumir o tráfego.

Alguns lembretes:

- Use o comando `xattr` **só em arquivos cuja origem você já verificou**; veja na seção anterior como verificar.
- **Não** use `sudo spctl --master-disable` para desligar o Gatekeeper de forma geral. Isso desliga a proteção da máquina inteira, enquanto o "Abrir" pelo botão direito afeta só um app.
- Desde o macOS 15, a Apple apertou o caminho do "Abrir" pelo botão direito, e na maioria dos casos é preciso passar pelo passo dos "Ajustes do Sistema". É uma mudança no comportamento do sistema, não um problema do nosso pacote.
- Macs entregues pela empresa muitas vezes são gerenciados por um perfil MDM, e os três passos acima podem estar desativados. Não force; use uma das três opções abaixo.

## Não quer liberar? Use uma destas três

Os clientes delas **funcionam no macOS com um duplo clique** e não mostram nenhuma das mensagens acima. A conta é a mesma, sem pagar nada a mais:

- **Rede privada (cliente oficial do Tailscale)**: funciona assim que é instalado, boa para deixar ligada direto
- **OpenVPN Connect**: o instalador do próprio OpenVPN; é só importar a configuração
- **Cisco Secure Client**: um cliente de nível corporativo, que já vem instalado em muitos computadores de empresa

## Perguntas frequentes

**O programa de vocês tem vírus mesmo?**
Não. É um espelho sem modificações do pacote de lançamento oficial do projeto de código aberto original. Mas você não deve simplesmente acreditar na nossa palavra; o jeito de conferir por conta própria está acima: envie para o VirusTotal e veja como ficam os resultados dos mecanismos.

**No Windows ainda vai ser acusado?**
Hoje, nos nossos testes, a central de segurança que vem no Windows não acusa mais a instalação do Hiddify. Se o antivírus que você instalou acusar mesmo assim, envie primeiro para o VirusTotal para uma segunda checagem e, depois que passar, marque a pasta de instalação do Hiddify como confiável no antivírus. Não desligue a proteção em tempo real para instalar.

**Depois de instalar no Mac, ele não abre. O download veio corrompido?**
Não. Ele não abre porque o Gatekeeper está bloqueando. Resolva com os três jeitos de liberar acima.

**Devo instalar um antivírus no Mac junto?**
Não. O que está bloqueando no macOS é o Gatekeeper que vem no sistema, não um antivírus. Instalar um antivírus de terceiros não faz essa mensagem sumir e ainda pode criar novos bloqueios.

**Esse problema acontece no celular?**
No iOS, instalando pela App Store, esse problema não existe. O Android às vezes avisa sobre fontes desconhecidas; é só permitir.


---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=troubleshooting-06) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=troubleshooting-06) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, oferta permanente
