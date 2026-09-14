---
title: "Painel da campanha"
nav_order: 7
parent: "Guias por tarefa"
permalink: /guias/painel-da-campanha/
task: painel-da-campanha
role: admin
routes: ["#/campanhas/:id"]
screenshots: [bp-39-painel-campanha, bp-40-painel-campanha-mobile, bp-41-painel-campanha-prestacao]
source_docs: [CHANGELOG.md#1.12.0, ARCHITECTURE.md#adr-015]
last_verified: 2026-09-14
status: publicado
---

# Painel da campanha

Toda campanha tem um **Painel** — a primeira aba quando você abre a campanha para editar. É a sua visão de gestão: mostra, num relance, como a campanha está indo. Novo na versão **1.12.0**.

## Onde fica

Em **Campanhas**, clique numa campanha. A aba **Painel** já abre por padrão, antes do formulário.

![Painel da campanha com os indicadores](/assets/screenshots/bp-39-painel-campanha.png)

## O que o painel mostra

Os indicadores vêm agrupados:

- **Vendas** — cartões vendidos (com uma barra de **% vendido**), reservados no momento, disponíveis e número de pedidos.
- **Financeiro** — arrecadado (bruto), descontos concedidos, valor líquido e o **ticket médio por comprador**. Aqui você vê os valores completos, sem máscara.
- **Ritmo e prazos** — quantos cartões saíram nos **últimos 7 dias**, a **média por dia**, uma **projeção de quando deve esgotar** (some quando ainda não há vendas suficientes) e os **dias que faltam para o sorteio**.
- **Meta** — se você configurou uma meta (de cartões e/ou de arrecadação) na aba **Página pública**, o painel mostra o **percentual atingido**. O número bate com o termômetro que o público vê.
- **Conversão de reservas** — quantas reservas viraram pedido pago e quantas expiraram.
- **Prestação de contas** — quando a campanha entra na fase de encerramento, aparece um resumo das **pendências do checklist** de documentos.

![Seção de prestação de contas no painel de uma campanha concluída](/assets/screenshots/bp-41-painel-campanha-prestacao.png)

O painel é **mobile-first** — abre bem no celular para você acompanhar de qualquer lugar.

![Painel da campanha no celular](/assets/screenshots/bp-40-painel-campanha-mobile.png)

## Dicas

- O painel só aparece depois que a campanha existe. Numa **campanha em rascunho** (ainda sem vendas), ele exibe um aviso para publicar e começar a vender.
- Este painel é focado em **uma** campanha. Para comparar várias campanhas e ver o resultado consolidado da organização, use o **Painel geral** (a home do RIT360 Premiado).
- Os números são só de leitura. Para exportar relatórios detalhados, use a aba **Prestação de contas**.
