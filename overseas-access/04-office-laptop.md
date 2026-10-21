# 04 · Computador da empresa: sem direitos de administrador e já com a VPN corporativa

Um computador da empresa tem três restrições: você não pode instalar programas não aprovados, não tem direitos de administrador e muitas vezes ele já está conectado à VPN da empresa. Uma VPN para o aparelho inteiro, nesse caso, ou não instala ou briga com a VPN da empresa. A ferramenta certa é o Proxy Web: uma extensão de navegador que manda só as requisições desse navegador pela linha, enquanto a intranet da empresa, o programa de e-mail e a VPN corporativa ficam exatamente como estão, e não é preciso ser administrador. Este artigo mostra como configurar, o que dá para fazer, o que não fazer e como conviver com a política de TI da empresa.

## Por que o Proxy Web

- Nenhum aplicativo para instalar: é só uma extensão de navegador, e a maioria das empresas permite extensões, mas não programas.
- Sem direitos de administrador: a extensão roda no espaço do usuário e não mexe nas configurações de rede do sistema.
- Convive com a VPN da empresa: a VPN corporativa controla as rotas do sistema, enquanto o Proxy Web fica só na camada do navegador, então um não atrapalha o outro; as páginas da intranet continuam passando pela VPN da empresa.
- Por design, não há conexão para cair: o proxy funciona por requisição, sem conexão longa, então você também não sente as oscilações da rede da empresa.

## Configure em dois passos

1. Instale a extensão ZeroOmega (a continuação do SwitchyOmega) no navegador; a página Proxy deste site tem o link de instalação para cada navegador.
2. Entre neste site e, na página Proxy, clique em "Importar todas as regiões" (copia o link de restauração da extensão) e cole em "Import/Export" (importar/exportar) → "Restore from online" (restaurar a partir de link on-line) na extensão. Regiões e endereços são importados de uma vez; depois disso, clique no ícone da extensão, escolha uma região e digite a conta e a senha deste site na janela de login que o navegador mostrar.
3. Recomendamos um perfil de navegador separado (ou outro navegador) só para o proxy, deixando o navegador de trabalho na rede local, para os dois não se misturarem.

## Para que serve e quando usar outra forma

- Serve: pesquisar, abrir Google, GitHub, Stack Overflow, sites de documentação de fora, a versão web do ChatGPT e webmail.
- Use outra forma: apps de vídeo, programas de desktop e ferramentas de linha de comando não usam as configurações de proxy do navegador por padrão (na linha de comando, você pode colocar o endereço do proxy na variável de ambiente http_proxy; veja o artigo sobre Linux).
- Use outra forma: assistir a sites de vídeo chineses (para quem está fora da China). Os sites de vídeo também verificam IPv6 e DNS, que o Proxy Web não cobre; nesse caso é preciso uma VPN para o aparelho inteiro.

## Convivendo com a política de TI

Tudo num computador da empresa pode ser auditado pela empresa, e as extensões não são exceção. Leia primeiro a política de uso aceitável da empresa: o que a maioria proíbe são programas não aprovados e contornar a política de segurança, e uma extensão de navegador acessando sites externos costuma ficar numa zona cinzenta; se não tiver certeza, pergunte à TI.

Não instale uma VPN para o aparelho inteiro (Cisco, Rede privada, Hiddify) num computador da empresa para contornar a política da empresa: elas mudam as rotas do sistema, o que dispara alertas no software de gestão de dispositivos e ainda leva o tráfego da intranet para fora. O Proxy Web afeta só um navegador e é o que traz menos risco.

Mantenha as contas de trabalho e as pessoais separadas: não entre em contas da empresa no navegador que usa o proxy, nem em contas pessoais no navegador da empresa.

## Perguntas frequentes

**E se a empresa proibir a instalação de extensões?** Aí use o seu próprio celular ou computador pessoal. Não use programas portáteis de origem desconhecida para driblar os controles.

**A extensão vai ver o tráfego da intranet da empresa?** Não. Pelas regras de roteamento dividido, os domínios da intranet conectam direto e não passam pelo proxy; no modo global eles só vão até o servidor do proxy e voltam, e o que o proxy vê é o nome do domínio, não o conteúdo. Por segurança, dê ao proxy um perfil de navegador só dele.

**O proxy funciona com a VPN da empresa ligada?** Funciona, os dois não entram em conflito. Pouquíssimas VPNs corporativas forçam todo o tráfego pela saída da empresa e desativam as configurações de proxy; nesse caso a extensão avisa que não consegue conectar, e a única opção é desligar a VPN da empresa.

**É igual num Mac da empresa?** É igual; as extensões do Chrome, do Edge e do Firefox têm versão para Mac. O Safari não tem essa extensão, então use outro navegador.

## Leia também

- [Página de configuração do Proxy: instalação da extensão e link de restauração](https://www.leotun.com/pt/httpproxy?utm_source=github&utm_content=overseas-access-04)
- [O que é o Proxy Web e quando usar](https://www.leotun.com/pt/guides/web-proxy?utm_source=github&utm_content=overseas-access-04)
- [Como mandar um servidor Linux e ferramentas de linha de comando pela linha](https://www.leotun.com/pt/guides/linux-server?utm_source=github&utm_content=overseas-access-04)
- [Qual forma de conexão serve para cada situação](https://www.leotun.com/pt/guides/choose-connection?utm_source=github&utm_content=overseas-access-04)

Versão deste artigo no site: https://www.leotun.com/pt/guides/office-laptop?utm_source=github&utm_content=overseas-access-04

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=overseas-access-04) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=overseas-access-04) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 15 créditos (cerca de 15 dias do plano Individual), oferta permanente
