---
title: "Auditoria"
nav_order: 11
parent: "Módulos"
permalink: /modulos/auditoria/
role: auditor
routes: ["#/auditoria"]
screenshots: [bp-24-auditoria]
source_docs: [PRD_Bussola_Premiada.md#9.3]
last_verified: 2026-07-05
status: publicado
---

# Auditoria

A **Trilha de auditoria** registra as ações sensíveis realizadas no plugin — quem fez o quê, quando e de onde. É a memória da campanha para fins de governança, transparência e prestação de contas.

![Trilha de auditoria](/assets/screenshots/bp-24-auditoria.png)

## Onde fica

No menu **RIT360 Premiado**, abra **Auditoria**. O acesso é controlado pela permissão `audit.view` — o papel **Auditor** enxerga a trilha sem poder alterar nada.

## O que é registrado

Ações relevantes ao longo do ciclo da campanha, por exemplo: publicação e alteração de regulamento, congelamento da base e finalização do sorteio, exportação de relatórios (com marca de mascaramento), mudanças de permissão, registro/remoção de doações à RIT, reagendamento de sorteio, entre outras. Cada registro guarda a **ação**, o **tipo e o identificador do objeto**, a **origem**, o **usuário** e a **data/hora**.

Também entram aqui as **correções manuais de cartões** feitas em [Corrigir cartões](/guias/corrigir-cartoes/) — vínculo de um cartão a um pedido pago, liberação de cartão preso e as liberações excepcionais. Nesses casos, o registro guarda ainda a **justificativa** que quem corrigiu escreveu, visível ao expandir a linha.

## Filtrar e consultar

A tela tem filtros por **Ação**, **Tipo de objeto**, **Origem**, **ID do objeto**, **Usuário**, **período** (de/até) e uma **busca** livre. Preencha o que precisar e clique em **Aplicar** (ou **Limpar** para recomeçar). Cada linha pode ser **expandida** para ver os detalhes do evento, e a lista é paginada.

## Exportar

O botão **⬇️ Exportar CSV** gera um arquivo com os registros filtrados — útil para anexar a uma prestação de contas ou entregar ao conselho fiscal/auditor externo.

> ✅ **Boas práticas**
>
> Dê um acesso de **Auditor** ao conselho fiscal ou ao contador da organização. Eles acompanham a lisura das campanhas pela trilha de auditoria, sem risco de alterar dados. É transparência que fortalece a confiança na sua OSC.

> 💠 **Privacidade**
>
> A trilha registra **ações**, não o conteúdo pessoal dos participantes. Ainda assim, trate a exportação com cuidado e compartilhe apenas com quem tem necessidade legítima. Veja a [Política de Privacidade](/legal/privacidade/).
