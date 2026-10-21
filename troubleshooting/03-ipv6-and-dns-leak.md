# 03 · Conectado, mas o site de vídeo ainda mostra aviso de direitos autorais: IPv6 e DNS são os que escapam

> Versão no site (mais completa): https://www.leotun.com/pt/guides/overseas-video?utm_source=github&utm_content=troubleshooting-03

Você já passou do passo 1 de [02 · Conectado para acessar a China, mas ainda não consigo assistir](02-still-blocked-after-connecting.md) — o IP de saída aparece como China continental —, mas o site continua dizendo "não pode ser reproduzido por restrições de direitos autorais". Em nove de cada dez casos ainda existe no aparelho um caminho que não passa pela VPN: **IPv6** ou **DNS**. O site de vídeo decide de onde você é pelo endereço que vê, e enquanto um caminho vazar, o que ele vê continua sendo estrangeiro.

## Por que os vazamentos acontecem

- Os aparelhos modernos têm um endereço IPv4 e um IPv6, e os navegadores preferem o IPv6. Se a VPN só assume o IPv4, as requisições IPv6 saem direto pela sua internet de casa.
- O "DNS seguro" embutido no navegador, o "DNS privado" do Android ou outra ferramenta de rede mesh rodando ao mesmo tempo (Tailscale e similares) assumem a resolução de nomes antes da VPN.

"Conectado" só quer dizer que o túnel foi estabelecido. Não quer dizer que todo o tráfego passa por ele.

## Verificação em cinco passos

1. **Confira o IPv6.** Depois de conectar, pesquise "test ipv6" e abra uma página de teste. Se o campo IPv6 mostrar um endereço do país onde você está → o problema é aqui, vá para o passo 2. Se os dois campos mostrarem China continental, ou o IPv6 estiver indisponível → vá para o passo 3.
2. **Desligue o IPv6 ou passe para um cliente que bloqueie IPv6.** Windows: nas propriedades do adaptador de rede, desmarque "Protocolo IP Versão 6". macOS: Ajustes de Rede → TCP/IP → configure o IPv6 como "Somente link-local". Celular: desligue o Wi‑Fi e teste uma vez nos dados móveis; a internet de casa costuma ter IPv6, enquanto os dados móveis das operadoras muitas vezes não têm.
3. **Confira o DNS.** No Chrome, Configurações → Privacidade e segurança → desative "Usar DNS seguro"; no Android, desative o "DNS privado"; feche outras VPNs, ferramentas de rede mesh e extensões de proxy.
4. **Feche o app por completo e abra de novo; na versão web, limpe os dados do site.** As plataformas guardam em cache a checagem de região anterior.
5. **Mude para outro ponto de entrada e tente de novo.** O endereço de uma determinada saída pode ter acabado de ser marcado pela plataforma.

## Como a LeoTun lida com isso

Desde setembro de 2026, as três formas de conexão da LeoTun (Hiddify, Cisco AnyConnect, OpenVPN) recusam o IPv6 diretamente dentro do túnel e enviam configurações de DNS que forçam a resolução dentro do túnel — não é preciso mudar nada no seu aparelho. **Configurações do Hiddify importadas antes de setembro não têm essa regra. Apague e escaneie o QR code para importar de novo.**

A opção com roteador nem chega a vazar: a rede local inteira sai pelo roteador, então o IPv6 e o DNS dos aparelhos nunca chegam ao lado de fora.

## Casos em que o aviso ainda aparece

| Caso | Sintoma | Solução |
|---|---|---|
| A saída não é a China continental | A consulta de IP mostra Hong Kong / Taiwan / Japão | Mude para um ponto de entrada da China; para a Tencent e o iQIYI, endereços de Hong Kong e Taiwan também contam como estrangeiros |
| Regras de roteamento personalizadas colocam os domínios de vídeo como "direto" | As páginas abrem, mas os vídeos não tocam | Faça os domínios chineses passarem pelo nó; quem está fora da China não deve ativar "direto para a China" |
| Você está usando o Proxy Web | Funciona no navegador, não nos apps | Para assistir vídeos é preciso um túnel no aparelho inteiro; o Proxy Web só cobre o navegador |

---
Organizado pela equipe [LeoTun](https://www.leotun.com/pt?utm_source=github&utm_content=troubleshooting-03) · Dúvidas? Veja a [página de contato](https://www.leotun.com/pt/contact?utm_source=github&utm_content=troubleshooting-03) (grupos, e-mail e suporte estão todos lá) · Cadastre-se e ganhe 4 horas de teste grátis; convide um amigo que pague e cada um ganha 20 dias do plano Individual, válido por tempo indeterminado
