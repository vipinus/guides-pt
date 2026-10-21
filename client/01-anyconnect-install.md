# 01 · Cisco AnyConnect: instalar, conectar e atualizar em todas as plataformas

> Versão no site (mais completa): https://www.leotun.com/pt/guides/anyconnect-china?utm_source=github&utm_content=client-01

O AnyConnect é o cliente de VPN corporativa da Cisco. Hoje o nome oficial é **Cisco Secure Client**; funciona do mesmo jeito. Você não precisa de arquivo de certificado nem de perfil importado: digite o endereço, sua conta e sua senha, e já conecta. Para saber se funciona na China e para o que mudar quando não conecta, veja [Acessar serviços de fora a partir da China, guia 02](https://github.com/vipinus/guides-zh-CN/blob/main/overseas-access/02-anyconnect-in-china.md) (em chinês).

## Instalação

| Plataforma | O que instalar | Onde baixar |
|---|---|---|
| Windows 10 ou mais recente | Cisco Secure Client 5.x | [A página da Cisco no site](https://www.leotun.com/pt/anyconnect?utm_source=github&utm_content=client-01) |
| Windows 7 / 8 | AnyConnect 4.9 (a última versão compatível; não recebe mais atualizações) | Mesmo lugar |
| macOS | Cisco Secure Client 5.x | Mesmo lugar |
| iOS | Cisco Secure Client | App Store; se a loja não mostrar, instale o OpenConnect, que é de código aberto e usa o mesmo protocolo |
| Android | Cisco Secure Client | Google Play, ou o APK na página do site |
| Linux | O instalador na página do site, ou o openconnect do repositório da sua distribuição | Mesmo lugar |

No Windows também existe o OpenConnect-GUI, de código aberto; a mesma conta funciona nele.

## Conectar em quatro passos

1. Abra o cliente e digite o endereço do servidor no campo de endereço. Usuários da LeoTun podem **clicar na bandeira de uma região** no site para copiar o endereço daquela região.
2. Digite sua conta (o e-mail do cadastro) e sua senha.
3. Quando aparecer "Connected" (conectado), abra uma página que mostre o seu IP para confirmar que a saída está na região escolhida.
4. Para mudar de região, use outro endereço. O cliente guarda os endereços já usados, então da próxima vez é só escolher na lista.

## Atualização

Não precisa desinstalar antes: instale a versão nova por cima da antiga e os endereços salvos continuam lá. No celular, atualize pela loja de apps. Depois de uma grande atualização do sistema operacional, atualize primeiro o cliente e só depois investigue problemas de conexão.

## Mensagens comuns

| Mensagem | Significado |
|---|---|
| Login failed | Conta ou senha erradas, ou a conta venceu |
| Untrusted server certificate | Provavelmente o relógio do sistema está errado, ou a rede atual está interceptando conexões criptografadas; tente outra rede |
| Connection attempt has failed | Este endereço está temporariamente inacessível; troque de região |

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=client-01) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=client-01) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, oferta permanente
