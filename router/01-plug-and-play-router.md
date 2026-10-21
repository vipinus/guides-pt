# 01 · Primeiros passos com um roteador pré-configurado

## Três passos depois de tirar da caixa

1. **Ligue a energia e o cabo de rede**: conecte a porta WAN do roteador ao seu modem ou roteador atual e espere a luz indicadora estabilizar, cerca de um minuto.
2. **Conecte-se ao Wi-Fi**: o nome e a senha padrão do Wi-Fi estão impressos no cartão de instruções (o padrão de fábrica dos dois é o domínio do site). Depois de conectar, abra um navegador e vá ao endereço de administração `http://192.168.11.1`.
3. **Entre na sua conta**: na página de administração, digite o e-mail e a senha da sua conta e salve (contas Individual, Família e Empresa podem usar roteador). A partir daí, todo aparelho conectado a esse Wi-Fi passa pela VPN automaticamente.

## Troque as senhas padrão

A senha de administração e a senha do Wi-Fi de fábrica são públicas, então troque logo depois de entrar: página de administração → System (Sistema) → Administration (Administração); Wireless (Sem fio) → Interfaces → Wireless Security (Segurança sem fio).

## Modo de roteamento dividido

O padrão é o roteamento dividido: os domínios chineses da lista passam pela VPN, e todo o resto conecta direto. É o modo ideal se você está no exterior assistindo a vídeos chineses ou se os idosos da família usam a TV. Quando você está na China e escolhe uma região de fora, o sentido se inverte automaticamente: por padrão, só os sites e serviços bloqueados passam pela VPN, e os sites chineses e os sites estrangeiros que já abrem normalmente na China conectam direto; veja [03 · O que é o roteamento dividido do roteador](03-router-split-routing.md). Quando precisar temporariamente que tudo passe pela VPN, mude para "Global" e volte quando terminar.

## Perguntas frequentes

- **A luz indicadora está normal, mas os aparelhos conectados ficam sem internet**: confira o status da conta na página de administração; conta vencida ou senha errada aparecem ali.
- **Você quer trocar por outro roteador**: desvincule o antigo no site primeiro; veja [Vínculo de MAC e troca de roteador](05-mac-binding-and-replacing.md).

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=router-01) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=router-01) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, oferta permanente
