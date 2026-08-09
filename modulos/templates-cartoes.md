---
title: "Templates & Cartões"
nav_order: 3
parent: "Módulos"
permalink: /modulos/templates-cartoes/
role: admin
routes: ["#/templates", "#/campanhas/:id"]
screenshots: [bp-07-templates, bp-06-campanha-cartoes, templates-status-inativo]
last_verified: 2026-08-09
status: publicado
---

# Templates & Cartões

Os **cartões** são o que se compra na campanha. Os **templates** são as listas que dão origem a eles.

![Seção Templates](/assets/screenshots/bp-07-templates.png)

## Templates (listas)

Um template pode ser **numérico** (gera cartões numerados) ou do tipo **lista** (cada cartão é um nome).

O plugin embarca **9 listas temáticas prontas**: Animais do Brasil, Artistas, Cidades do Brasil, Clássicos da literatura, Especialidades escoteiras, Ficção científica, Heróis dos quadrinhos, Músicas K-pop e Pessoas históricas. Elas são semeadas automaticamente e ficam prontas para uso — você não precisa montar nada.

Você também pode **criar suas próprias listas** ou **importar um CSV** (o plugin remove duplicados e espaços em excesso).

### Três campos que ajudam a escolher (2.23.0)

Cada template ganhou informações que orientam quem vai montar a próxima campanha:

- **Quantidade recomendada** — a sugestão de quantos cartões usar com aquele template. Opcional; serve de referência na hora de criar a campanha.
- **Dica de uso** — um texto livre curto explicando quando aquele template cai bem (por exemplo: *"ideal para rifas de até R$ 5.000"*).
- **Status: Ativo ou Inativo** — um template **inativo deixa de ser oferecido** na hora de criar ou editar uma campanha. Use isso para aposentar uma lista sem apagá-la: as campanhas que já a usaram continuam intactas, e ela some da lista de opções. Na listagem de templates, o estado aparece como uma etiqueta **Ativo** (verde) ou **Inativo** (cinza).

![Templates com status Ativo e Inativo](/assets/screenshots/templates-status-inativo.png)

## Cartões

Os cartões são gerados **dentro de cada campanha**, na aba de configurações, e só enquanto a campanha está em rascunho. Ao gerar, o plugin cria cartões únicos e **congela o valor** de cada um.

![Geração de cartões](/assets/screenshots/bp-06-campanha-cartoes.png)

## Como o cliente escolhe

Na página pública, o participante pode escolher **manualmente** os cartões disponíveis ou pedir uma **seleção automática** (aleatória). Os cartões escolhidos ficam **reservados** por alguns minutos enquanto ele finaliza a compra. Um mecanismo de **reserva atômica** garante que dois compradores nunca levem o mesmo cartão.

O passo a passo está em [Montar os cartões](/guias/montar-cartoes/).

> ✅ **Boas práticas**
>
> Listas temáticas tornam a rifa mais lúdica e comentável. Escolha um tema que **dialogue com a sua causa ou seu público** — uma OSC ambiental pode usar "Animais do Brasil", um grupo de leitura, "Clássicos da literatura".
