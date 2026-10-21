# 02 · O Cisco AnyConnect funciona na China?

> Versão no site (mais completa): https://www.leotun.com/pt/guides/anyconnect-china?utm_source=github&utm_content=overseas-access-02

Funciona. O AnyConnect é o protocolo de VPN corporativa da Cisco. Empresas do mundo todo dependem dele para o trabalho remoto, e as filiais de empresas estrangeiras na China usam todo dia, então proibi-lo de vez sai caro demais. **O que é bloqueado de fato é um endereço de servidor específico, não o protocolo.** Por isso, "funcionar ou não" depende de o provedor ter endereços suficientes e trocá-los rápido o bastante.

## Por que ele resiste a bloqueios melhor que apps de VPN proprietários

| | AnyConnect | App de VPN proprietário |
|---|---|---|
| Assinatura do tráfego | TLS padrão, igual a acessar um site HTTPS | Protocolo próprio, com assinatura fixa |
| Quando é identificado | Só aquele endereço para de conectar | O app inteiro para de funcionar |
| Aplicativo | Publicado pela Cisco; a alternativa de código aberto OpenConnect existe para todas as plataformas | Some quando é removido da loja de apps |

A LeoTun roda máquinas próprias em 24 regiões. Quando um endereço é marcado, ele é trocado por um novo, o domínio é apontado de novo automaticamente, e o endereço salvo no seu aplicativo não precisa mudar.

## Como instalar

1. Baixe o instalador para o seu sistema na página Cisco do site. Windows 10 ou mais novo, macOS, iOS, Android e Linux estão todos cobertos; o Windows 7/8 só pode usar a versão 4.9, a última que os suporta.
2. Abra o aplicativo e digite o endereço do servidor no campo de endereço; no site, clique na bandeira de uma região para copiá-lo.
3. Digite a sua conta e a sua senha e conecte. Não precisa de arquivo de certificado nem de importar configuração.
4. Quando aparecer "Connected" (conectado), confira o seu IP de saída.

## Se não conectar, siga esta ordem

1. **Troque de região.** Se outra região conectar, só aquele servidor está temporariamente inacessível.
2. **Troque de rede.** Se a internet fixa falhar, passe para os dados móveis, e vice-versa; a interferência nas diferentes operadoras não acontece ao mesmo tempo.
3. **Leia o erro.** `Login failed` indica conta ou senha erradas, ou conta vencida; `Untrusted server certificate` quase sempre é o relógio do sistema errado ou a rede atual interceptando o TLS, então troque de rede; só `Connection attempt has failed` significa que o endereço está inacessível.
4. **Atualize o aplicativo.** Isso importa principalmente depois de uma grande atualização do sistema.
5. **Troque de forma de conexão.** A mesma conta pode usar OpenVPN ou Hiddify para conectar aos mesmos servidores, e o bloqueio dos três protocolos é independente; veja [02 · Qual forma de conexão serve para cada situação](../network/02-choose-your-connection-method.md).

## Atualizar o Cisco AnyConnect

A Cisco mudou o nome para Cisco Secure Client; o uso é o mesmo. Não precisa desinstalar antes: instale a versão nova por cima da antiga e os endereços salvos são mantidos. No celular, atualize pela App Store / Google Play; se a busca na loja não encontrar, use o OpenConnect, de código aberto, que usa o mesmo protocolo e a mesma conta (para trocar a região da loja no iOS, veja o [Guia de aplicativos 06](../client/06-ios-app-store.md)).

## Perguntas frequentes

**Velocidade baixa é sinal de limitação?** Troque de região primeiro: olhe as luzes vermelha, amarela e verde na lista de regiões do site e escolha uma verde. Se continuar lento, a causa costuma ser a internet local: banda larga compartilhada de condomínio, ou uma operadora e uma região que não combinam (China Unicom no norte: Japão ou Coreia; China Telecom no sul: Sudeste Asiático ou Austrália; outros provedores: os pontos de entrada na China).

**Por que o mesmo endereço às vezes vai bem e às vezes mal?** O endereço é um nome de domínio, e as máquinas por trás dele são trocadas automaticamente conforme bloqueios e carga. Esperar um ou dois minutos e tentar de novo costuma resolver: você pegou a troca no meio.

**Ele desconecta sozinho depois de muito tempo conectado?** Não por causa do tempo. Quando a conta vence, o servidor desconecta você; renove e conecte de novo.

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=overseas-access-02) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=overseas-access-02) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 15 créditos (cerca de 15 dias do plano Individual), oferta permanente
