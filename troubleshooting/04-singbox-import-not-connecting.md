# 04 · Importei no Hiddify, mas não conecta

> Versão no site (mais completa): https://www.leotun.com/pt/guides/singbox-subscription?utm_source=github&utm_content=troubleshooting-04

Encontre o seu erro na tabela. Para saber como importar, veja [Como importar um link de assinatura (Hiddify, Clash, Shadowrocket)](../client/02-singbox-subscription-links.md).

| Sintoma | Causa | O que fazer |
|---|---|---|
| "Unable to fetch subscription" (não foi possível obter a assinatura), 401 | A conta venceu ou a senha foi trocada (trocar a senha invalida as configurações antigas na hora; é de propósito) | Entre no site e confira a validade; depois de renovar ou trocar a senha, escaneie o QR code de novo |
| Importa, mas a conexão dá timeout | O endereço daquela região acabou de mudar, ou aquele ponto de entrada está sofrendo interferência da operadora | Toque em "Update subscription" (atualizar assinatura) no cliente para baixar a configuração mais recente; mude para outra região — cada região é uma configuração separada e uma não afeta a outra |
| Conectado, mas sem internet | As regras de roteamento do próprio cliente estão mandando o tráfego para "direto" | Mude a saída padrão para aquele nó, ou apague as regras que você mesmo adicionou |
| Ao escanear aparece "QR code inválido" | Quando a janela abre, o QR code é o do Hiddify / sing-box, e outros clientes que escaneiam direto dão esse erro; ou foi escaneado do print de outra pessoa | Clique antes no botão do seu cliente, que troca o QR code para o tipo certo, e depois escaneie ou cole: clientes da família Clash clicam em "Assinatura Clash"; Shadowrocket / NekoBox / v2rayN e afins clicam em "Link de compartilhamento". O QR code contém as suas próprias credenciais, e o de outra pessoa não funciona |
| Velocidade baixa | A região escolhida está com carga alta, ou a sua internet local não combina com a região | Veja as luzes vermelha, amarela e verde na lista de regiões do site e mude para uma região com luz verde; se continuar lento, mude de região conforme a sua operadora |
| Um cliente da família Clash não importa o link de compartilhamento | Clash Meta, Clash Verge, FlClash, Stash e afins não importam uma única linha hysteria2:// como perfil | Clique no botão "Assinatura Clash" e cole a URL na lista de assinaturas do cliente; o Clash original e o Clash for Windows não têm hysteria2 no núcleo, então use um cliente com núcleo mihomo |
| O link de compartilhamento não importa ou não conecta | O link usa um formato estendido que alguns clientes não entendem | Passe para o Hiddify |

## Preciso importar de novo depois de renovar, trocar de plano ou mudar a senha?

- **Renovar ou trocar de plano (Individual / Família / Empresa)**: Não. A configuração atual continua funcionando.
- **Mudar a senha**: A configuração antiga para de funcionar na hora; escaneie o QR code de novo. Se você perder o celular ou o link vazar, use isso para cortar o acesso.
- **Conta vencida**: A configuração retorna 401. Depois de renovar, não precisa de configuração nova; é só reconectar.
- **Importado antes de setembro de 2026**: Falta a regra que recusa o IPv6, então assistir vídeos chineses fora da China vai mostrar aviso de restrição de direitos autorais. Apague e importe de novo; veja o [03](03-ipv6-and-dns-leak.md).

## Quando falar com o suporte

Informe três coisas ao suporte: o nome e a versão do cliente, a região e o texto exato do erro ou um print.

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=troubleshooting-04) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=troubleshooting-04) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 24 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, válido por tempo indeterminado
