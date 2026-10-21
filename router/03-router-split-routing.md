# 03 · O que é o roteamento dividido do roteador

> Versão no site (mais completa): https://www.leotun.com/pt/guides/router-firmware?utm_source=github&utm_content=router-03

## Em uma frase

Configure a VPN no roteador, e todos os aparelhos da casa passam por ela automaticamente assim que entram no Wi-Fi. Aparelhos que não instalam cliente, como TV boxes, videogames e impressoras, também podem usar.

## Que problema o roteamento dividido resolve

Se todo o tráfego passa pela VPN, aparecem dois problemas: os sites locais ficam lentos (dão uma volta) e os aparelhos locais ficam inacessíveis (impressora, NAS e a página de administração do roteador estão todos na rede local, mas o tráfego foi mandado para fora).

O roteamento dividido funciona dando ao roteador uma lista: os domínios da lista passam pela VPN, e todo o resto conecta direto. O sentido depende de onde você está e de qual lado quer acessar, e é decidido automaticamente pela região que você escolhe:

- **No exterior, com a região China escolhida (acessar a China)**: sites e apps chineses passam pela VPN, e todo o resto conecta direto.
- **Na China, com uma região de fora escolhida (acessar serviços de fora)**: por padrão, só os sites e serviços bloqueados passam pela VPN; os sites chineses e os sites estrangeiros que já abrem normalmente na China (sites de empresas estrangeiras, downloads da Apple e da Microsoft, plataformas de jogos e afins) conectam direto, sem desvio, tão rápido quanto sem o roteador.

## Três modos

| Modo | Para onde vai o tráfego | Quando usar |
|---|---|---|
| Global | Tudo passa pela VPN | Temporariamente, para investigar problemas |
| Split routing (roteamento dividido) | Os domínios da lista passam pela VPN, o resto conecta direto | No dia a dia |
| Direct (direto) | Nada passa pela VPN | Quando você não vai precisar por um tempo |

## Acessar serviços de fora a partir da China: só sites bloqueados

Desde 14 de outubro de 2026, o roteamento dividido no sentido de acessar serviços de fora a partir da China manda por padrão só os sites e serviços bloqueados pela VPN. Ele usa uma lista de sites bloqueados que se atualiza sozinha todo dia, mais serviços como o Telegram, que conectam a endereços fixos sem consultar um nome de site. Os sites que já abrem normalmente na China, chineses ou estrangeiros, conectam direto.

A chave fica na página de administração do roteador, em "VPN settings" (configurações de VPN), na parte de roteamento dividido inteligente: a caixa "Blocked sites only" (só sites bloqueados pela linha), marcada por padrão. Desmarque para voltar ao comportamento anterior: sites chineses direto, todo o resto pela VPN.

Firmwares instalados antes de outubro de 2026 ainda não mostram essa caixa; o novo padrão já vale para esses roteadores pelas atualizações automáticas. Para mudar, fale com o atendimento, que faz isso remotamente.

O sentido de acessar a China a partir do exterior não mudou.

## Armadilhas

- **Um site não abre com o roteamento dividido**: veja primeiro se ele está na lista. Sites fora da lista conectam direto, e se aquele site já não abria antes, o roteamento dividido não vai ajudar. Mude para "Global" temporariamente para confirmar.
- **Na China, um site estrangeiro não abre**: desmarque "Blocked sites only" na parte de roteamento dividido inteligente (ou mude para "Global" temporariamente) e tente de novo. Se abrir, o site está bloqueado mas ainda não está na lista; mande o endereço ao atendimento.
- **Os sites bloqueados não abrem, mas todo o resto funciona**: o mais provável é que o aparelho tenha um DNS criptografado ligado ("DNS privado" do Android, o "DNS seguro" do navegador), e o roteador não consegue ver qual site ele está procurando. Desligue essa opção.
- **A impressora ou o NAS ficam inacessíveis depois de conectar**: isso significa que os endereços da rede local também estão sendo mandados para fora. Confira se as regras de roteamento dividido excluem as faixas privadas como 192.168.x.x.
- **O desempenho do roteador** define o teto. O processador de um roteador antigo chega ao limite com tráfego criptografado, e isso aparece como a casa inteira ficando lenta. Nesse caso, o problema não é a linha da VPN.

## Uma conta, um roteador

A maioria dos serviços vincula o roteador à conta (pelo endereço MAC). Uma conta fica vinculada a um roteador, e para trocar de roteador você desvincula primeiro. Assim, a conta continua só sua.

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=router-03) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=router-03) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 15 créditos (cerca de 15 dias do plano Individual), oferta permanente
