# 02 · Instalar o firmware por conta própria: do original ao nosso, passo a passo (com vídeo)

> Tutorial em vídeo (cerca de dois minutos e meio, narração em inglês ou chinês): https://www.leotun.com/pt/video/router-flash?utm_source=github&utm_content=router-02
>
> Versão no site: https://www.leotun.com/pt/guides/router-flash?utm_source=github&utm_content=router-02

Este guia é para quem já tem um roteador de um modelo da lista de compatíveis. Você tem um roteador ainda com o sistema original de fábrica, e vamos do momento em que você abre o site até a casa toda conectada — o que clicar em cada passo, o que vai aparecer e onde as pessoas costumam errar. A demonstração usa um GL.iNet GL-MT3000. Os outros modelos seguem os mesmos passos; só o painel original muda de cara. Se preferir não fazer isso você mesmo, um roteador já configurado dá menos trabalho: veja o [01](01-plug-and-play-router.md). Para escolher o modelo, veja o [07](07-which-router-to-buy.md).

## Antes de começar

- **Confira se o seu modelo é compatível.** Entre na conta, abra a seção **Roteador** e procure o seu modelo pela marca. A revisão de hardware depois do nome do modelo (v1, v2 etc.) também precisa bater.
- **Sua conta precisa estar ativa.** Os planos Individual, Família e Empresa podem usar roteador.
- **Tenha um cabo de rede à mão.** A porta WAN do roteador vai no seu modem ou no roteador principal. Durante a instalação, é melhor ligar também o computador ao roteador por cabo; é mais estável que o Wi-Fi.
- **Guarde uma cópia do firmware original.** Baixe o firmware original do seu modelo no site do fabricante, caso um dia queira voltar.

## Passo 1: gere o firmware no site

1. Entre na conta e clique em **Roteador** na barra de navegação.
2. Encontre o seu modelo e clique em **Firmware**, ou role até "Compilar Firmware" e escolha o modelo na lista de marcas.
3. Clique em **Iniciar Compilação**.

Algumas coisas para saber antes:

- **A compilação leva de 3 a 5 minutos.** O firmware é feito na hora para a sua conta; não é um arquivo pronto. Em horários de pico a compilação pode entrar numa fila. A página avisa quando isso acontece — é só esperar, não precisa clicar de novo.
- **Você recebe um e-mail quando estiver pronto.** O item em "Compilações Recentes" muda para "Concluído", e um aviso chega na sua caixa de entrada.
- **O idioma da interface do firmware segue o idioma do site.** Se você usa o site em português, as páginas de administração do roteador ficam em português. Para outro idioma, mude o idioma do site antes e depois compile.
- **O link de download vale por um dia.** Se vencer, é só compilar de novo.

## Passo 2: baixe e extraia

1. Em "Compilações Recentes", clique em **Baixar**. Você recebe um arquivo zip.
2. Abra a pasta Downloads e **extraia** o arquivo.
3. A pasta extraída contém o arquivo do firmware.

Qual arquivo usar:

| O seu roteador está rodando | Use o arquivo |
|---|---|
| Sistema original da GL.iNet (o caso do vídeo) | que termina em `sysupgrade.bin` |
| Sistema original de outra marca | com `factory` no nome |
| Já o nosso firmware, e você está atualizando | com `sysupgrade` no nome |

Se o zip tiver um arquivo só, é ele.

> ⚠️ **Este firmware é só seu.** Ele leva os dados da sua conta para que o roteador entre sozinho depois da instalação. Não mande o arquivo para ninguém nem publique.

## Passo 3: instale pelo painel original

Usando a GL.iNet como exemplo:

1. Ligue o computador ao roteador, abra o painel original no navegador (`http://192.168.8.1` na GL.iNet) e entre com a senha de administrador.
2. No menu da esquerda, abra **System** → **Upgrade** (sistema → atualização).
3. Vá para a aba **Firmware Local Upgrade** (atualização local de firmware).
4. Clique na área de envio e escolha o arquivo de firmware que você extraiu.
5. Espere a verificação mostrar **Pass** (aprovado).
6. **Desligue "Keep Settings" (manter configurações).** É o passo que as pessoas mais esquecem. Os dois sistemas não usam o mesmo formato de configuração, e manter as configurações antigas causa todo tipo de problema estranho.
7. Clique em **Install** (instalar).

A página muda para "Upgrading and rebooting…" (atualizando e reiniciando) com um anel de progresso. **Leva de dois a três minutos. Não tire o roteador da tomada nem feche a página nesse meio-tempo.** É normal a página parar de carregar quando o progresso termina — o roteador agora roda outro sistema, e tanto o endereço quanto o Wi-Fi mudaram. Veja o próximo passo.

Outras marcas: procure "Firmware Upgrade", "System Upgrade" ou "Local Upgrade" (ou o equivalente em português) no painel original, envie o arquivo e, de novo, não mantenha as configurações.

## Passo 4: entre no novo Wi-Fi

Depois da instalação, o nome antigo do Wi-Fi some e aparece um novo:

- **Nome do Wi-Fi: `www.anyfq.com`**
- **Senha do Wi-Fi: `www.anyfq.com`** (igual ao nome)

Computadores e celulares precisam **mudar para esse Wi-Fi** antes de conseguir acessar a internet ou abrir a página de administração do roteador. Um computador ligado ao roteador por cabo não precisa mudar nada.

O novo endereço de administração é `http://192.168.11.1` (digite você mesmo o `http://` do começo).

## Passo 5: espere ele conectar sozinho

Sem login, sem escolher região. **Com a conta ativa, o roteador conecta sozinho em até 10 minutos.** A partir daí, todo aparelho nesse Wi-Fi passa pelo serviço automaticamente — TVs, TV boxes e videogames inclusive.

Para confirmar que conectou, abra num aparelho ligado ao roteador um site que você normalmente não consegue acessar, ou veja o status na página de administração.

## Duas coisas que vale a pena fazer depois

1. **Troque as senhas padrão.** A senha do Wi-Fi e a senha de administrador vêm com valores padrão públicos. Troque as duas na página de administração.
2. **Sinal de Wi-Fi fraco logo depois da instalação é normal.** O roteador precisa entrar na internet uma vez e descobrir em que região está antes de subir a potência do sinal para o nível permitido ali. Ligue o cabo de rede e deixe ele entrar na internet primeiro.

## Trocar um roteador antigo por um novo

Uma conta fica vinculada a um roteador por vez. Se a sua conta já foi usada em outro roteador:

1. Entre na conta, abra a seção **Roteador** e, sob o título "Compilar Firmware", você verá o modelo **Vinculado**, com **Desvincular** ao lado.
2. Clique em Desvincular. Dá para fazer isso mesmo se o roteador antigo estiver quebrado ou longe.
3. Nada a fazer no roteador novo: ele **conecta automaticamente** e fica vinculado à sua conta.

Se você instalar o roteador novo antes de desvincular, também não tem problema. O roteador novo fica esperando e conecta sozinho assim que você desvincular.

Mais sobre as regras em [05 · Vínculo por MAC e troca de roteador](05-mac-binding-and-replacing.md).

## E se a minha conta vencer

Depois do vencimento, o roteador para de mandar o tráfego pelo serviço, e a rede da sua casa continua funcionando normalmente. **Depois de renovar, o roteador volta sozinho — sem precisar entrar de novo nem reinstalar o firmware.**

## Não conectou sozinho — como verificar

Se depois de uns dez minutos ainda não funcionar, verifique nesta ordem:

1. **A internet em si está funcionando?** Num aparelho ligado ao roteador, abra qualquer site comum. Se não abrir, o problema é o cabo ou o modem: confira se o cabo na porta WAN está bem encaixado.
2. **A conta venceu?** Entre no site e confira a data de vencimento. Depois de renovar, espere alguns minutos.
3. **A conta ainda está vinculada ao roteador antigo?** Na seção Roteador, veja o modelo vinculado. Se não for este roteador, clique em Desvincular.
4. **Reinicie o roteador uma vez.** Tire da tomada, espere dez segundos, ligue de novo e dê dois a três minutos.
5. **Entre manualmente.** Abra `http://192.168.11.1` e entre no roteador com o usuário `root` e a senha `www.anyfq.com`. Depois vá em **Services** → **VPN** (serviços → VPN), digite o e-mail e a senha da sua conta e salve.

Continua travado? Pergunte no grupo e diga o modelo do roteador e até onde você chegou na lista acima.

## Quando não vale a pena instalar por conta própria

O modelo não está na lista, a revisão de hardware não bate, ou é um roteador antigo sem modo de recuperação. Nesses três casos, um roteador já configurado dá menos trabalho.

## Se a instalação der errado

A maioria dos roteadores tem um modo de recuperação: tire da tomada, segure o botão de reset enquanto liga de novo, continue segurando por alguns segundos, depois ligue um computador por cabo e envie o firmware original seguindo as instruções do fabricante. Na GL.iNet, procure "uboot" na documentação. É para isso que serve o firmware original que você guardou antes.

## Perguntas frequentes

**Instalar o firmware anula a garantia?** Depende do fabricante. Os roteadores GL.iNet já são baseados num sistema de código aberto e podem voltar ao firmware original.

**Posso voltar ao firmware original?** Pode. Use o modo de recuperação descrito em "Se a instalação der errado" para enviar o firmware original.

**Um arquivo de firmware serve para dois roteadores?** Não. O firmware é gerado por conta, e uma conta fica vinculada a um roteador por vez.

**Preciso compilar de novo se trocar de conta?** Não. Saia da conta na página de administração e entre com a conta nova.

**Atualizações futuras exigem reinstalar?** As atualizações de rotina o roteador pega sozinho; você não precisa fazer nada. Só uma versão maior exige compilar de novo e instalar uma vez o arquivo sysupgrade, e o site avisa quando isso acontecer.

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=router-02) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=router-02) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 15 créditos (cerca de 15 dias do plano Individual), válido por tempo indeterminado
