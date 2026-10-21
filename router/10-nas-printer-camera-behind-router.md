# 10 · O NAS, a impressora e as câmeras ligados ao roteador vão ser afetados?

Quando um roteador VPN entra em casa, a primeira preocupação costuma ser com o resto: o NAS, a impressora e as câmeras vão continuar funcionando, e o NAS vai arrastar todo o tráfego dele pela VPN?

## A resposta curta

Não. O roteamento dividido vem ligado por padrão: **o tráfego entre os aparelhos da casa e o tráfego para serviços na China nunca entram no túnel. Só os sites que precisam da VPN passam por ela.**

## Três tipos de tráfego, três caminhos

| Tráfego | Caminho | Exemplos |
|---|---|---|
| Entre aparelhos da casa | Fica na rede local, nunca toca no túnel | Copiar arquivos para o NAS, espelhar na TV, imprimir |
| Para serviços na China | Direto, pela sua própria internet | NAS sincronizando com uma nuvem chinesa, câmeras enviando para uma nuvem chinesa, downloads de sites chineses |
| Para sites bloqueados | Pelo túnel | YouTube, buscadores, ferramentas de IA |

Então copiar arquivos para o NAS de casa roda na velocidade total da rede local, e os backups dele para a nuvem chinesa usam toda a sua internet sem tocar na VPN.

Quando você está fora da China usando uma rota para a China, o sentido se inverte: os sites chineses da lista passam pelo túnel e todo o resto vai direto. Veja [03 · O que é o roteamento dividido](03-router-split-routing.md).

## Três situações comuns

**Acessar o NAS de fora (arquivos remotos, backup de fotos do celular)**
Duas formas:
- Use a Rede privada (Tailscale): coloque o NAS e o celular na mesma conta e acesse o NAS pelo nome do aparelho de qualquer lugar. Sem IP público e sem redirecionamento de portas. Veja [Rede privada x VPN](../network/03-private-network-vs-vpn.md).
- Continue fazendo como antes (acesso remoto do fabricante, redirecionamento de portas). O roteador não bloqueia.

**Downloads rodando no NAS**
Downloads de fontes chinesas vão direto e não são afetados. Downloads de sites estrangeiros que já abrem normalmente na China (downloads da Apple e da Microsoft, por exemplo) também vão direto por padrão; só os downloads de sites bloqueados passam pelo túnel e rodam na velocidade do túnel. Se você não quer que os downloads usem o túnel, ligue o NAS no roteador principal ou no modem, e ele deixa de passar por este roteador.

**Um notebook de trabalho que precisa da VPN da empresa**
Conecte-o ao Wi-Fi do roteador principal ou do modem, separado deste roteador. Duas VPNs empilhadas uma sobre a outra costumam quebrar o acesso à rede da empresa.

## Quando um aparelho não se comporta

- O aparelho está com "DNS privado" ou "DNS seguro" ligado. Aí ele resolve os nomes por conta própria, contornando o roteador, e o roteamento dividido não enxerga. Desligue essa configuração.
- Confira em qual Wi-Fi ele está. Se estiver no Wi-Fi do modem, ele nem passou por este roteador.

## Perguntas frequentes

**O NAS ocupa uma vaga de aparelho na minha conta?** Não. O roteador ocupa uma vaga, e o que está ligado a ele não é contado separadamente.

**Com a casa toda ligada, vou ficar sem dados?** As contas têm dados ilimitados, e o tráfego dentro da China nem entra no túnel.

**Posso deixar um aparelho fora da VPN para sempre?** Pode, ligue-o no roteador principal ou no modem. A página de administração também consegue passar o roteador inteiro para o modo "Direct" (direto), mas isso vale para todo mundo de uma vez.

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=router-10) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=router-10) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, válido por tempo indeterminado
