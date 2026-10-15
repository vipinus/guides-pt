# 03 · Proxy Web: configure a extensão ZeroOmega em dois passos

> Versão no site (mais completa): https://www.leotun.com/pt/guides/web-proxy?utm_source=github&utm_content=client-03

O Proxy Web manda só **este navegador** pela linha; os outros programas do sistema ficam como estão. Não há cliente para instalar, não precisa de direitos de administrador e não existe estado "conectado", então, por definição, não há conexão para cair. Serve para computador da empresa, para uma máquina que já está ligada à VPN corporativa, ou quando você quer que só um navegador use a linha. Para saber quando usar e quando é preciso uma VPN, veja o [Guia de rede 02](../network/02-choose-your-connection-method.md).

## Dois passos

1. **Instale a extensão**: instale o ZeroOmega (a continuação do SwitchyOmega) no Chrome / Edge / Firefox. A [página do Proxy no site](https://www.leotun.com/pt/httpproxy?utm_source=github&utm_content=client-03) tem o link de instalação para cada navegador.
2. **Importe**: entre no site e, na página do Proxy, clique na bandeira da região que você quer (ou clique em "Copiar o link de importação de todas as regiões" para importar todas de uma vez); isso copia o link de configuração. Abra "Import/Export" (importar/exportar) na extensão, cole o link em "Restore from online" (restaurar da internet) e clique em "Restore" (restaurar). Regiões, endereços e método de criptografia entram de uma vez, sem digitar nada à mão.

Depois disso, clique no ícone da extensão, escolha uma região e digite o usuário e a senha da sua conta do site na janela de login que o navegador mostrar. Para trocar de região, clique em outra no menu do ícone; para voltar à conexão direta, escolha "Direct" (direto).

## Nestes casos, use uma forma que cubra o computador inteiro

- Apps e players de vídeo e música: a maioria não usa o proxy do navegador, e o resultado é "as páginas abrem, mas os vídeos não tocam".
- Apps de celular, jogos e programas de computador. As configurações de proxy de programas como o Dropbox só aceitam HTTP / SOCKS5 sem criptografia, enquanto na prática um proxy precisa ser criptografado, então o Proxy Web deste site não pode ser colocado ali. Use o Hiddify para assumir o computador inteiro; veja o [10](10-app-proxy.md).
- Assistir Tencent Video ou iQIYI do exterior: os sites de vídeo também verificam IPv6 e DNS, que o Proxy Web não cobre; use uma VPN para o aparelho inteiro.

## Perguntas frequentes

| Sintoma | Causa |
|---|---|
| A janela de login fica aparecendo | A conta venceu ou a senha está errada |
| Alguns sites não abrem e outros abrem normalmente | As regras de "auto switch" (troca automática) da extensão mandaram esses sites direto; teste uma vez o modo de proxy global |
| Na China, só os sites HTTPS abrem | O HTTP simples é alterado no caminho e só as conexões criptografadas passam; hoje em dia quase todo site é HTTPS |
| Lento | Troque de região; o proxy e a VPN usam o mesmo conjunto de servidores |

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=client-03) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=client-03) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 24 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, oferta permanente
