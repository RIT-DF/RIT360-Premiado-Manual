---
title: "Prestação de contas"
nav_order: 8
parent: "Módulos"
permalink: /modulos/prestacao-contas/
role: admin
routes: ["#/campanhas/:id"]
screenshots: [bp-22-prestacao-contas]
last_verified: 2026-09-14
status: publicado
---

# Prestação de contas

Este módulo fecha o ciclo da campanha com transparência: reúne documentos, oferece um checklist e gera relatórios.

![Aba Prestação de contas](/assets/screenshots/bp-22-prestacao-contas.png)

## Documentos

Anexe os documentos classificando-os como **público** ou **privado**. O **documento do contemplado é sempre privado** (forçado pelo sistema). Um **checklist advisory** lembra os documentos recomendados: ata de apuração, recibo de entrega e comprovante do prêmio — não bloqueia a conclusão, mas orienta.

## Relatórios

Exporte o relatório completo da campanha em **CSV, PDF ou JSON**, reunindo campanha, organização, cartões, financeiro, apuração e compradores. Por padrão, os dados pessoais saem **mascarados**; desmascarar exige permissão específica e **toda exportação é registrada** no log de auditoria.

## Motor de PDF

A geração de PDF usa um motor configurável em **Configurações → PDF / Relatórios**. Os arquivos que podem conter dados pessoais são gravados em área temporária **não acessível pela web**.

O passo a passo está em [Prestar contas](/guias/prestar-contas/).

> ✅ **Boas práticas**
>
> Guarde sempre o **comprovante de entrega assinado pelo ganhador** e arquive o **PDF do relatório** da campanha. É o que demonstra, para o conselho e para os órgãos competentes, que a campanha foi conduzida com lisura.
