---
title: "Montar os cartões"
nav_order: 2
parent: "Guias por tarefa"
permalink: /guias/montar-cartoes/
task: montar-cartoes
role: admin
routes: ["#/templates", "#/campanhas/:id"]
screenshots: [bp-07-templates, bp-06-campanha-cartoes]
source_docs: [PRD_Bussola_Premiada.md#8.4, PRD_Bussola_Premiada.md#8.5]
last_verified: 2026-08-09
status: publicado
---

# Montar os cartões

Os **cartões** são as unidades que as pessoas compram — o equivalente aos "números da rifa". No RIT360 Premiado eles podem ser **números** (1, 2, 3…) ou **nomes de uma lista temática** (animais, cidades, personagens). Este guia mostra como preparar a lista e gerar os cartões.

## Dois tipos de cartão

- **Numérico** — cartões numerados automaticamente. Simples e clássico.
- **Lista** — cada cartão é um nome de uma lista temática. Deixa a rifa mais divertida e memorável ("comprei o *Onça-pintada*!").

## Listas prontas (templates)

O plugin já vem com **9 listas temáticas** prontas para usar, sem você precisar montar nada:

Animais do Brasil · Artistas · Cidades do Brasil · Clássicos da literatura · Especialidades escoteiras · Ficção científica · Heróis dos quadrinhos · Músicas K-pop · Pessoas históricas.

Você as encontra na seção **Templates**.

![Seção Templates](/assets/screenshots/bp-07-templates.png)

## Criar sua própria lista

1. Abra a aba **Templates** na barra de abas do plugin.
2. Crie um novo template do tipo **Lista** e informe os nomes — ou **importe um CSV** (o plugin remove duplicados e espaços em excesso automaticamente).
3. Preencha, se quiser, a **quantidade recomendada** de cartões e uma **dica de uso** (ex.: *"ideal para rifas de até R$ 5.000"*). São opcionais e servem para orientar quem for montar a próxima campanha.
4. Deixe o **status** em **Ativo**. Templates marcados como **Inativo** não aparecem para escolha ao criar ou editar campanha — é o jeito de aposentar uma lista sem apagá-la.
5. Salve. A lista fica disponível para qualquer campanha.

> 💡 **Exemplo**
>
> Uma escola pode criar uma lista com os **nomes das turmas** ou dos **professores homenageados**; uma paróquia, com nomes de **santos**. A lista temática vira parte da graça da campanha.

## Gerar os cartões da campanha

Os cartões são gerados **dentro da campanha**, na aba de cartões do formulário, e só enquanto ela está em **rascunho**:

1. Abra a campanha (ou crie uma — veja [Criar a primeira campanha](/guias/criar-primeira-campanha/)).
2. Defina a **quantidade de cartões** e o **valor unitário** na aba **Configurações da Campanha**.
3. Escolha o **template** (numérico ou uma lista) e clique em **gerar**. O plugin cria os cartões únicos e **congela o valor** de cada um naquele momento.

![Geração de cartões na campanha](/assets/screenshots/bp-06-campanha-cartoes.png)

> ⚠️ **Atenção**
>
> Os cartões só podem ser gerados (ou regerados) enquanto a campanha está em **rascunho**. Depois de publicada e com vendas, o pool de cartões não é mais alterado — é isso que garante a integridade da rifa. Se precisar de mais cartões, planeje a quantidade certa antes de publicar.

> ✅ **Boas práticas**
>
> Se a lista temática tiver menos nomes que a quantidade de cartões desejada, o plugin não terá nomes suficientes. Garanta que a lista tenha **pelo menos** tantos nomes quanto a quantidade de cartões — ou use o tipo numérico.
