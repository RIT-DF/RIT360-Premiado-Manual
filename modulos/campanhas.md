---
title: "Campanhas"
nav_order: 2
parent: "Módulos"
permalink: /modulos/campanhas/
role: admin
routes: ["#/campanhas", "#/campanhas/nova", "#/campanhas/:id"]
screenshots: [bp-02-campanhas-lista, bp-03-campanha-nova-dados, bp-05-campanha-config]
source_docs: ["#136"]
last_verified: 2026-07-22
status: publicado
---

# Campanhas

É o coração do plugin. Aqui você cria, configura, publica e gerencia cada sorteio — do rascunho à conclusão.

![Lista de campanhas](/assets/screenshots/bp-02-campanhas-lista.png)

## Ações da lista

Na coluna à direita de cada campanha, as ações aparecem como **ícones**, cada um com uma **dica** (o texto surge ao passar o mouse):

- **✏️ Editar** (lápis) — abre a campanha. Em campanhas que já não podem ser editadas, o ícone vira um **👁 olho (Ver)**, só para consulta.
- **⧉ Duplicar** (cópia) — cria uma cópia da campanha (veja abaixo).
- **🗑 Excluir** (lixeira) — aparece **apenas em rascunhos**. Apaga a campanha de vez, com **confirmação** antes (a ação não pode ser desfeita).
- **🗄 Arquivar** (caixa) — aparece em **campanhas finalizadas** (vendas encerradas, concluídas ou canceladas). Ao confirmar, a campanha **sai da lista principal**.

### Arquivar e reexibir

Arquivar é a forma de **tirar da frente** as campanhas antigas sem perdê-las. Assim que existe alguma campanha arquivada, aparece no topo da lista o checkbox **"Mostrar arquivadas"** — marque-o para trazê-las de volta à visão.

> 💡 **Excluir × Arquivar.** Use **Excluir** só para descartar um rascunho que não vai usar. Para campanhas que já rodaram, prefira **Arquivar**: elas somem da lista do dia a dia, mas continuam guardadas (com histórico e prestação de contas) e reaparecem quando você quiser.

## O formulário em abas

Uma campanha se organiza em **abas de topo**:

- **Formulário** (3 etapas: Dados da Campanha · Dados do Prêmio · Configurações da Campanha). A etapa **Dados do Prêmio** aceita **um ou vários prêmios** (1º, 2º, 3º lugar…).
- **Regulamento** — obrigatório para publicar (veja [Regulamento](/modulos/regulamento/)).
- **Dados legais** — autorização, processo, observações.
- **Página pública** — template, transparência, compartilhamento (veja [Página pública](/modulos/pagina-publica/)).
- **Apuração** — o sorteio (veja [Apuração](/modulos/apuracao/)).
- **Prestação de contas** — documentos e relatórios (veja [Prestação de contas](/modulos/prestacao-contas/)).

O passo a passo de criação está em [Criar a primeira campanha](/guias/criar-primeira-campanha/).

## Corrigir cartões

Na **coluna da direita** do formulário há o painel **Corrigir cartões**: você busca um cartão pelo número ou pelo nome, vê o estado real dele (situação, reserva, pedido e histórico) e resolve os dois problemas mais comuns — **comprador pagou e não recebeu o cartão** e **cartão preso que não volta para a venda**. Toda correção exige justificativa e fica registrada na auditoria. Passo a passo em [Corrigir cartões](/guias/corrigir-cartoes/).

## Estados da campanha

Cada campanha percorre uma **máquina de estados** que protege a integridade da rifa. Os principais:

- **Rascunho** — edição livre, geração de cartões.
- **Programada** — abre sozinha em uma data futura.
- **Aberta** — vendendo.
- **Aguardando apuração** — vendas encerradas, base congelada.
- **Sorteada** — resultado definido.
- **Concluída** — prestação de contas feita.
- **Cancelada / Arquivada** — encerradas sem sorteio ou guardadas.

O sistema só permite as transições válidas e mantém uma **trilha de auditoria** de tudo.

## Duplicar campanha

Campanhas recorrentes? **Duplique** uma existente — inclusive o regulamento é copiado. Você ajusta só o que muda e ganha tempo.

> 💡 **Exemplo**
>
> Uma associação faz a "Rifa do Dia das Mães" todo ano. Basta duplicar a do ano anterior, trocar prêmio, datas e valor, revisar o regulamento e publicar.

> ⚠️ **Atenção**
>
> Quantidade de cartões e valor unitário são definidos no rascunho e travam após a publicação com vendas. Planeje esses números antes de abrir — veja [Como planejar uma campanha que vende](/boas-praticas/campanha-vencedora/).
