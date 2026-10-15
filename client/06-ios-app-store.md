# 06 · O que fazer quando o iOS não deixa instalar um app

Se você não encontra o Hiddify, o Tailscale ou o Telegram no iPhone, ou vê a mensagem "Este app não está disponível no seu país ou região no momento", o app não sumiu: a App Store é dividida em lojas conforme a região do seu ID Apple, e a loja da China não oferece a maioria dos apps de rede. No iOS, instale pela App Store com um ID Apple de uma região que não seja a China; os passos estão nesta página. Recomendamos criar um novo em vez de mudar a conta que você já tem. Abaixo estão os passos, o truque para escolher "Nenhum" como forma de pagamento e por que você nunca deve usar uma conta compartilhada por outra pessoa.

## Por que isso acontece

A App Store é dividida em lojas conforme a região do ID Apple, e cada região oferece apps diferentes. A loja da China não tem nem o Hiddify nem o Tailscale, e o Telegram e o Discord aparecem e somem; o Cisco Secure Client e o OpenVPN Connect estão disponíveis na maioria das regiões. É uma diferença de catálogo, não um problema dos apps, e uma conta de outra região consegue instalá-los.

No iPhone, tanto o Hiddify quanto a Rede privada (Tailscale) deste site são instalados pela App Store; basta seguir os passos abaixo para usar um ID Apple de outra região. Os instaladores para Android, Windows e macOS são fornecidos diretamente por este site e não são afetados.

## Opção 1 (recomendada): criar um novo ID Apple fora da região China

1. Saia da conta atual da App Store: Ajustes → seu perfil no topo → Mídia e Compras → Encerrar Sessão. Isso desconecta só a App Store, não o iCloud, então fotos, backups e contatos não são afetados.
2. Na App Store, encontre um app gratuito, toque em "Obter" e siga o aviso para "Criar Novo ID Apple". Escolha como região Estados Unidos, Hong Kong, Japão ou Singapura, e "Nenhum" como forma de pagamento. Esse "Nenhum" só aparece quando você cria a conta durante o download de um app gratuito; o cadastro direto pela web muitas vezes não oferece essa opção.
3. Entre na App Store com a conta nova, procure Hiddify, Tailscale e Telegram e baixe.
4. Depois de instalados, você pode voltar para a sua conta original; os apps já instalados continuam funcionando e recebendo atualizações normalmente. Troque de novo sempre que precisar instalar um app novo.

## Opção 2: mudar a região da conta que você já tem

Entre em account.apple.com e mude o país ou região. Antes é preciso cancelar todas as assinaturas e zerar o saldo, em alguns casos também cadastrar uma forma de pagamento local, e voltar atrás dá o mesmo trabalho. Não recomendado, a não ser que você já pretenda mudar de região por muito tempo.

## O que nunca fazer

- Não use um ID Apple compartilhado por outra pessoa, incluindo "contas compartilhadas" de grupos ou da internet. O dono da conta pode bloquear seu aparelho remotamente, e um iPhone bloqueado só ele consegue desbloquear; depois que a autenticação de dois fatores é ativada, não dá para desativar, e o risco e qualquer disputa ficam com você. O suporte deste site também não fornece nenhuma conta compartilhada.
- Não instale perfis de configuração de origem desconhecida nem instaladores "assinados com certificado corporativo". São formas comuns de driblar a loja, e também uma porta de entrada para instalar certificados e sequestrar o tráfego.

## Depois de instalar

Hiddify: volte à página do Hiddify deste site e escaneie o código, ou toque no botão "assinatura sing-box" para copiar, depois vá ao Hiddify e adicione. Tailscale: saia primeiro da conta oficial e siga os passos da página da Rede privada para informar o endereço do servidor de controle deste site. Telegram, Discord: vá à página de Contato deste site e escaneie o código para entrar no grupo.

## Perguntas frequentes

**Preciso de cartão de crédito para criar a conta em outra região?** Não. Pelo caminho da Opção 1 (criar a conta durante o download de um app gratuito) dá para escolher "Nenhum" como forma de pagamento.

**A conta nova afeta meu iCloud e minhas fotos?** Não. Você troca de conta só na App Store; o iCloud continua na sua conta original.

**No iPad é igual?** Sim, o iPadOS segue as mesmas regras da App Store.

**Celulares Android também têm esse problema?** Não. Os instaladores para Android, Windows, macOS e Linux são distribuídos diretamente por este site e não dependem de loja de apps.

## Leia também

- [Página de contato: cards de download dos clientes e os três grupos](https://www.leotun.com/pt/contact?utm_source=github&utm_content=client-06)
- [Hiddify: importar escaneando o código](https://www.leotun.com/pt/singbox?utm_source=github&utm_content=client-06)
- [Rede privada (Tailscale): passos para entrar](https://www.leotun.com/pt/mesh?utm_source=github&utm_content=client-06)
- [Como falar com a gente e não perder o contato](https://www.leotun.com/pt/guides/stay-in-touch?utm_source=github&utm_content=client-06)

Versão deste artigo no site: https://www.leotun.com/pt/guides/ios-app-store?utm_source=github&utm_content=client-06

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=client-06) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=client-06) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 24 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, oferta permanente
