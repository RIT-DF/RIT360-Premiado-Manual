---
title: "Licença"
nav_order: 13
parent: "Módulos"
permalink: /modulos/licenca/
role: admin
routes: ["#/licenca"]
screenshots: [bp-44-licenca]
last_verified: 2026-08-28
status: publicado
---

# Licença

> 💡 **Por que isso importa**
>
> O RIT360 Premiado **funciona sem licença** — não existe recurso pago que trave uma
> campanha. A licença serve para uma coisa só: **liberar as atualizações automáticas**,
> inclusive as de correção de bugs e segurança. Enquanto ela não estiver ativada, o site
> continua com a versão instalada, mas **não recebe nada de novo** — nem os ajustes
> urgentes. Ative logo depois de instalar.

## Onde fica

Menu **RIT360 Premiado → Licença**.

![Licença — nenhuma ativada](/assets/screenshots/bp-44-licenca.png)

## Como ativar

1. Abra **RIT360 Premiado → Licença**.
2. No bloco **Ativar licença**, cole a **chave de licença** (formato `V3RL-XXXX-XXXX-XXXX-XXXX`)
   no campo **Chave de licença**.
3. Clique em **Ativar**.

> ⚠️ **A chave completa só aparece nesta tela, no momento da ativação.** Depois disso, o
> sistema sempre mostra a versão mascarada (ex.: `V3RL-XXXX-...-B428`) — guarde a chave
> original (e-mail de compra, gerenciador de senhas) para o caso de precisar reativar em
> outro site.

## O que cada campo mostra

| Campo | O que significa |
|---|---|
| **Status** | *Nenhuma licença ativada*, *Ativa* ou o motivo de recusa. |
| **Chave** | A chave mascarada, depois de ativada. |
| **Expira em** | Data-limite da assinatura; passada ela, as atualizações voltam a parar. |
| **Ativações** | Quantos domínios já usam essa chave, sobre o limite contratado. |
| **Última verificação** | Quando o plugin conferiu, junto ao servidor da V3RTECH, se a licença continua válida. |

## Ativações por domínio

Uma mesma licença vale para **vários sites**, até o limite contratado — cada domínio ocupa
uma vaga. Para trocar de servidor, use **Desativar licença** no site antigo antes de
ativar no novo: **desativar libera a vaga** na hora.

> 💡 **Ambiente de teste não consome cota.** Um site de homologação/desenvolvimento
> reconhecido como tal pelo servidor de licenças não ocupa vaga de ativação.

## Quando dá errado

| Situação | O que fazer |
|---|---|
| Chave recusada | Confira se copiou a chave inteira, sem espaços, e se não trocou `O` por `0` ao digitar à mão. |
| Limite de ativações atingido | Desative a licença em um site que não usa mais essa chave, ou contrate mais ativações. |
| Licença expirada | Renove a assinatura e clique em **Verificar agora** para atualizar sem esperar a checagem automática. |
| Servidor de licenças indisponível | O plugin segue funcionando com a última verificação válida; tente de novo em alguns minutos, e fale com o suporte se persistir por mais de um dia. |

> ⚠️ **Licença vencida não desliga o plugin.** O que para é só a atualização automática —
> as campanhas continuam vendendo cartões e o site funciona normalmente.
