# 06 · Liberar sites de vídeo chineses no exterior com um roteador

## Por que usar um roteador em vez de instalar um cliente em cada aparelho

- TVs, TV boxes, projetores e videogames não instalam cliente, então o roteador é o único jeito.
- Com muita gente em casa, configurar cada aparelho de cada pessoa não é realista; configure o roteador uma vez, e tudo passa a valer assim que o aparelho entra no Wi-Fi.
- O roteamento dividido é feito no roteador, então os sites e os aparelhos locais continuam conectando direto; só os domínios de vídeo chineses passam pela linha para a China, e a velocidade não é afetada.

## Do que você precisa

| Item | Observações |
|---|---|
| Um roteador compatível | Um pré-configurado funciona ao tirar da caixa; se for instalar o firmware por conta própria, veja [Como instalar o firmware](02-flash-firmware-yourself.md) |
| Uma conta | Os planos Individual, Família e Empresa aceitam o recurso de roteador. Depois de se cadastrar, peça primeiro o teste grátis para conferir todo o processo: conta nova fica no plano Individual, com 4 horas de teste |
| Uma rede de origem | O modem ou o roteador que você já tem em casa; o roteador novo fica atrás dele |

## Pronto em cinco passos

1. Ligue a porta WAN do roteador novo à rede de origem, conecte a energia e espere um minuto.
2. Conecte o celular ao Wi-Fi do roteador novo, abra o endereço de administração `http://192.168.11.1` e entre na sua conta.
3. Escolha **Split routing** (roteamento dividido) como modo. Os domínios de vídeo chineses estão na lista e vão passar automaticamente pela linha para a China.
4. Passe a TV e a TV box para esse Wi-Fi, ou ligue-as por cabo a uma porta LAN do roteador novo.
5. Abra o iQIYI, o Tencent Video ou o Yangshipin (a CCTV); se tocar normalmente, está pronto.

## A lista é pública

Os domínios de vídeo da lista de roteamento dividido ficam num repositório público: <https://github.com/vipinus/openwrt-2026-video-domains>. Se uma plataforma não tocar, você pode ver se o domínio dela está na lista e enviar uma sugestão se não estiver.

## Qualidade de imagem e banda

1080p precisa de 5 Mbps estáveis, e 4K precisa de 25 Mbps ou mais. Se travar no horário de pico da noite, escolha uma região com luz verde; se continuar travando, a causa costuma ser a banda larga local. Como região de entrada, escolha uma perto de você e com boa rota até a China continental; teste duas ou três e decida pelo que trava menos.

## Perguntas frequentes

- **Toca no celular, mas não na TV**: a TV ainda está no Wi-Fi antigo, ou o app da TV é a versão internacional.
- **Algumas plataformas tocam e outras não**: o domínio daquela plataforma não está na lista de roteamento dividido. Mude para "Global" temporariamente para confirmar e depois envie o domínio para o repositório da lista.
- **A casa inteira fica lenta com um roteador antigo**: o processador não dá conta do tráfego criptografado; troque por um modelo com mais desempenho, veja [Primeiros passos com um roteador pré-configurado](01-plug-and-play-router.md).

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=router-06) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=router-06) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 15 créditos (cerca de 15 dias do plano Individual), oferta permanente
