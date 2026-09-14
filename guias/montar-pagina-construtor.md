---
title: "Montar a página no construtor"
nav_order: 11
parent: "Guias por tarefa"
permalink: /guias/montar-pagina-construtor/
task: montar-pagina-construtor
role: admin
routes: ["#/blocos"]
screenshots: [bp-26-blocos-editor, bp-25-blocos-referencia]
source_docs: [PRD_Bussola_Premiada.md#8.24]
last_verified: 2026-09-14
status: publicado
---

# Montar a página da campanha no construtor

Se você quer um layout próprio — diferente da página pública pronta —, pode montar a página da campanha no **editor de blocos (Gutenberg)** ou em construtores como o **Elementor**, combinando os componentes do RIT360 Premiado. Disponível a partir da versão **1.5.0**.

> A partir da versão **2.4.0**, o menu **"Blocos e Shortcodes"** passou a se chamar **"Shortcodes e API"**. Os componentes deste guia continuam na aba **Shortcodes e Blocos**; a nova aba **API** trata de [integrações com outros sistemas](/guias/integrar-api-webhooks/).

> Prefere algo pronto e rápido? A [página pública da campanha](/guias/personalizar-pagina-publica/) já entrega tudo em uma rolagem. Este guia é para quem quer **compor** a página do seu jeito.

## Antes de começar

Anote o **ID da campanha** (aparece na lista de **Campanhas**). Você vai usá-lo nos shortcodes; nos blocos, é possível escolher a campanha em um menu.

## Com blocos (Gutenberg)

1. Crie ou edite uma **página** (ou post) no WordPress.
2. Clique em **adicionar bloco** (o “+”) e procure por **“RIT360 Premiado”**.
3. Escolha um componente na categoria **RIT360 Premiado** — por exemplo, **Seleção de cartões**, **Painel de transparência**, **Barra de progresso**, **Botão comprar**, **Compartilhamento** ou a **Rifa completa**.
4. Com o bloco selecionado, abra o painel de configurações à direita e **escolha a campanha** no menu suspenso (ou informe o ID manualmente).
   ![Escolhendo a campanha no bloco](/assets/screenshots/bp-26-blocos-editor.png)
5. Repita para adicionar quantos componentes quiser, na ordem que fizer sentido.
6. **Publique** a página. A aparência real dos componentes aparece para quem visita o site.

## Com shortcodes (Elementor e outros)

Em construtores que aceitam shortcodes, adicione o widget **Shortcode** e cole o código do componente, trocando o `id`:

```
[rit360_premiado_painel id="12"]
[rit360_premiado_selecao id="12"]
[rit360_premiado_compartilhar id="12"]
```

A lista completa de blocos e shortcodes, com exemplos copiáveis, está na página **Blocos e Shortcodes** do menu do plugin (e em [Blocos e Shortcodes](/modulos/blocos-shortcodes/)).

## Um exemplo de montagem

Uma página de campanha caprichada poderia ter, de cima para baixo:

1. Um texto de abertura com a história da causa (bloco de parágrafo comum).
2. **Botão comprar** — chamada logo no topo.
3. **Barra de progresso** — cria urgência mostrando o quanto falta.
4. **Seleção de cartões** — onde a pessoa escolhe e compra.
5. **Painel de transparência** — reforça a confiança.
6. **Regulamento** e **Compartilhamento** — no rodapé.

> ⚠️ **Atenção**
>
> Se a campanha não estiver disponível publicamente (rascunho, cancelada), o componente exibe uma mensagem no lugar do conteúdo. Publique a campanha antes de divulgar a página.
