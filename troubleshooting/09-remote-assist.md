# 09 · Suporte remoto no seu computador e no seu roteador

Alguns problemas não ficam claros nem depois de uma dúzia de prints indo e voltando no grupo, mas o suporte consegue localizá-los em dois minutos olhando direto a tela. Este artigo explica quando vale pedir assistência remota, que programa usar no computador, como importar a configuração do servidor deste site, como passar os dados de conexão ao suporte com segurança, o que fica sob o seu controle durante a sessão, como retomar o acesso depois e o que você precisa fazer com um roteador que roda o firmware deste site.

## Quando vale pedir assistência remota

- Você já passou uma vez por [01 · Checklist para quando não conecta, fica lento ou cai](01-cannot-connect-slow-drops.md) e já perguntou informando a forma de conexão, a região, o texto exato do erro ou um print e o horário do problema, e mesmo assim não resolveu.
- Você não consegue descrever os passos: a configuração está escondida lá no fundo, você não lê o idioma do sistema ou o erro passa rápido demais para capturar.
- Você está ajudando um parente com o computador dele, não está do lado e não consegue explicar pelo telefone.

No caso abaixo, **não use assistência remota**; converse por texto no grupo:

- Computadores gerenciados de forma centralizada pela empresa. As políticas de grupo costumam proibir esse tipo de programa, e usar pode violar as regras da empresa.

## Que programa usar: RustDesk

O site recomenda o [RustDesk](https://rustdesk.com): ele é de código aberto (AGPL-3.0), então o código pode ser auditado por qualquer pessoa; e é você quem decide, com o seu próprio clique, quando a sessão começa e quando termina. Funciona em Windows, macOS, Linux, Android e iOS (o iPhone / iPad só controla outros aparelhos; não pode ser controlado).

Baixe na [página de contato](https://www.leotun.com/pt/contact#downloads), em "Central de downloads" → "Assistência remota", ou no site oficial rustdesk.com. Não use sites de download de terceiros que aparecem nas buscas. Os dois lados da sessão precisam instalar.

## O que autorizar depois de instalar

| Sistema | O que fazer |
|---|---|
| macOS | Em "Ajustes do Sistema → Privacidade e Segurança", marque o RustDesk tanto em "Gravação de Tela" quanto em "Acessibilidade", depois feche o app por completo e abra de novo. Dar só uma das duas leva a "dá para ver, mas não para controlar" ou a uma tela toda preta. Se aparecer "está danificado", veja o [06](06-antivirus-false-positive.md) |
| Android | Na hora de receber ajuda, toque em "Start service" (iniciar serviço) no RustDesk e permita a gravação da tela; para o suporte conseguir tocar na sua tela, ligue também o RustDesk em "Acessibilidade" no sistema |
| Windows / Linux | Normalmente funciona logo depois de instalar |

## Conectar ao nosso próprio servidor

A assistência remota passa pelo servidor RustDesk próprio deste site, que também conecta de forma confiável de dentro da China. **Os dois lados da sessão precisam importá-lo uma vez**; as duas pontas só se encontram quando usam o mesmo servidor:

1. Entre no site primeiro e, na [página de contato](https://www.leotun.com/pt/contact#downloads), vá em "Central de downloads" → "Assistência remota" → "Conectar ao nosso servidor" e clique em "Copiar".
2. No computador, abra no RustDesk "Settings → Network" (Configurações → Rede), clique antes em "Unlock network settings" (desbloquear configurações de rede) e depois em "ID/Relay server" (servidor de ID/relay); no celular é "Settings → ID/Relay server".
3. Na janela que aparece, clique no ícone da área de transferência no canto superior direito (no celular, toque em "Import", importar). A configuração é preenchida sozinha; clique em "OK".

**Não cole a configuração nos campos de texto**; isso causa "failed to lookup address". Essa configuração é só para uso com contas deste site. Não repasse para ninguém.

## Passar o ID e a senha de uso único ao suporte

Ao abrir o RustDesk, a tela principal mostra o ID desta máquina e uma senha de uso único. Antes de passar esses dados, confirme três coisas:

1. **Foi você quem pediu primeiro.** Você descreveu o problema num grupo oficial listado na [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=troubleshooting-09), e o suporte decidiu que era preciso assistência remota, antes de passar para o próximo passo. A nossa equipe de suporte não vai procurar você por conta própria, pedir que instale um programa de acesso remoto nem pedir um código de conexão; seja quem for que venha pedir, confirme antes no grupo oficial.
2. **Mande só pelos canais oficiais de suporte**: os contatos de atendimento humano listados na página de contato. Qualquer conversa no privado fora dos grupos dizendo ser "suporte da LeoTun" não é a gente.
3. **Não poste no grupo.** Um grupo é um lugar que muita gente vê; um ID mais uma senha é como deixar a chave do seu computador pendurada na porta.

## Durante a sessão

- Durante toda a sessão você vê na tela o que está sendo feito e pode desconectar na janela do RustDesk a qualquer momento.
- Se alguém pedir para você minimizar a janela, sair de perto do computador ou abrir o internet banking ou apps de pagamento, **desconecte na hora**.
- Quando for preciso digitar a senha da sua conta, digite você mesmo; não leia em voz alta para o suporte.

## Retomar o acesso depois

1. Clique em desconectar na janela do RustDesk e confirme que o outro lado ficou off-line.
2. Gere uma nova senha de uso único, para que a que você acabou de mandar perca a validade.
3. Feche o RustDesk. Se não for mais precisar, pode simplesmente desinstalar e baixar de novo na próxima vez.

## Roteadores: o que você precisa fazer

Com um roteador que roda o firmware deste site, você não precisa instalar nenhum programa de acesso remoto no roteador nem no computador, e não precisa mandar a senha de administração do roteador ao suporte. Você só precisa:

- Manter o roteador ligado, com o cabo de rede conectado e a conta logada no roteador.
- Informar ao suporte, no grupo oficial, a sua conta, o modelo do roteador e os sintomas; o suporte cuida do resto.
- Não ficar desligando e religando o roteador enquanto estão mexendo nele, a não ser que o suporte peça.

## Perguntas frequentes

**O suporte vai me mandar mensagem no privado por conta própria pedindo para instalar um programa de acesso remoto?** Não. Sempre que alguém procurar você sem você ter pedido, confirme a identidade dessa pessoa no grupo oficial primeiro.

**Aparece "failed to lookup address" ao importar?** O mais provável é que a configuração tenha sido colada nos campos de texto. Limpe esses campos, volte à janela "ID/Relay server" e importe clicando no ícone da área de transferência no canto superior direito.

**No macOS conecta, mas a tela fica preta, ou dá para ver e não para controlar?** As permissões estão incompletas. Marque tanto "Gravação de Tela" quanto "Acessibilidade", depois feche o app por completo e abra de novo.

**O que mais preciso fazer quando a sessão acabar?** Desconectar, gerar uma nova senha de uso único e fechar o programa. Com esses três passos feitos, o outro lado nunca mais consegue se conectar.

## Leia também

- [Como usar a assistência remota pelo RustDesk (guia no site)](https://www.leotun.com/pt/guides/rustdesk-certificate?utm_source=github&utm_content=troubleshooting-09)
- [O que fazer quando o Mac diz que o app "está danificado"](https://www.leotun.com/pt/guides/antivirus-false-positive?utm_source=github&utm_content=troubleshooting-09)
- [Página de contato: grupos de suporte, atendimento humano e e-mail](https://www.leotun.com/pt/contact?utm_source=github&utm_content=troubleshooting-09)
- [05 · Como falar com a gente e não perder o contato](05-how-to-reach-us.md)
- [01 · Checklist para quando não conecta, fica lento ou cai](01-cannot-connect-slow-drops.md)

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=troubleshooting-09) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=troubleshooting-09) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, oferta permanente
