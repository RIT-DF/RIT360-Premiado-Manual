---
title: "Blocos e Shortcodes"
nav_order: 12
parent: "Módulos"
permalink: /modulos/blocos-shortcodes/
role: admin
routes: ["#/blocos"]
screenshots: [bp-25-blocos-referencia, bp-26-blocos-editor, bp-32-vitrine, bp-33-verificacao]
source_docs: [PRD_Bussola_Premiada.md#8.24, CHANGELOG.md#1.9.0]
last_verified: 2026-09-14
status: publicado
---

# Blocos e Shortcodes

Além da página pública pronta (o hotsite da campanha), você pode **montar a sua própria página** no construtor de páginas do WordPress — o editor de **blocos (Gutenberg)** ou construtores como o **Elementor** — combinando os componentes da campanha do jeito que quiser. Novo na versão **1.5.0**.

## Onde encontrar a referência

Na barra de abas do **RIT360 Premiado**, abra **Shortcodes e API** (na sub-aba **Shortcodes e Blocos**). Essa tela lista cada componente com o nome do bloco, o shortcode e um exemplo pronto para copiar.

![Página Blocos e Shortcodes no admin](/assets/screenshots/bp-25-blocos-referencia.png)

## Os componentes disponíveis

Cada um funciona como **bloco** e como **shortcode**:

| Componente | O que mostra | Shortcode |
|---|---|---|
| **Seleção de cartões** | Grade para o participante escolher e comprar cartões | `[rit360_premiado_selecao id="ID"]` |
| **Painel de transparência** | Indicadores públicos (vendidos, disponíveis, sorteio…) | `[rit360_premiado_painel id="ID"]` |
| **Barra de progresso** | Barra compacta com o % de cartões vendidos | `[rit360_premiado_progresso id="ID"]` |
| **Resultado do sorteio** | Cartão contemplado e ganhador, após a apuração | `[rit360_premiado_resultado id="ID"]` |
| **Botão comprar** | Botão de destaque que leva à seleção de cartões | `[rit360_premiado_botao id="ID"]` |
| **Compartilhamento** | Botões de WhatsApp, redes sociais e copiar link | `[rit360_premiado_compartilhar id="ID"]` |
| **Regulamento** | Resumo do regulamento, com “ver completo” | `[rit360_premiado_regulamento id="ID"]` |
| **Rifa completa (página)** | A página inteira da campanha em um bloco | `[rit360_premiado_rifa id="ID"]` |
| **Termômetro de meta** *(novo, 1.9.0)* | Progresso rumo à meta de cartões e/ou de arrecadação | `[rit360_premiado_meta id="ID"]` |
| **Verificação do sorteio** *(novo, 1.9.0)* | Prova pública de que o sorteio foi honesto (veja abaixo) | `[rit360_premiado_verificacao id="ID"]` |
| **Vitrine de campanhas** *(novo, 1.9.0)* | Lista várias campanhas ativas em cards (não usa `id`) | `[rit360_premiado_vitrine limit="12" order="ending" status="ativas"]` |
| **Meus cartões** *(novo, 1.11.0)* | Painel do comprador: cartões e resultado, sem login (não usa `id`) | `[rit360_premiado_meus_cartoes]` |

> Troque `ID` pelo número da campanha (você encontra o ID na lista de **Campanhas**).

### Meus cartões (painel do comprador)

O bloco/shortcode **Meus cartões** mostra ao **participante**, sem login, os cartões que ele comprou e o resultado do sorteio. Diferente dos outros, **não usa `id`**: ele exibe as campanhas do próprio comprador a partir de um link pessoal enviado por e-mail. Também está sempre disponível no endereço pronto **`/meus-cartoes`** do seu site. Veja o passo a passo em [Painel "Meus cartões" do comprador](/guias/painel-meus-cartoes/).

### Vitrine de campanhas

Diferente dos outros, a **vitrine** não é de uma campanha só — ela lista **várias campanhas** em cards (nome, causa, mini-termômetro, link). É o "link único" para divulgar todas as suas campanhas de uma vez. Ela também tem um endereço próprio pronto: **`/campanhas`** no seu site.

Atributos do shortcode/bloco:

- **`limit`** — quantas campanhas exibir (padrão 12, máximo 60).
- **`order`** — `ending` (mais próximas de sortear primeiro, padrão) ou `recent` (mais recentes).
- **`status`** — `ativas` (só campanhas abertas, padrão) ou `publicas` (todas as públicas).

No bloco de Gutenberg, esses três viram controles próprios no painel à direita (um deslizante para o limite e menus para ordem e filtro).

![Vitrine de campanhas](/assets/screenshots/bp-32-vitrine.png)

### Verificação do sorteio

O bloco/shortcode de **verificação** mostra, de forma pública, como conferir que o sorteio foi honesto. Antes da apuração, ele exibe o **lacre** (uma "impressão digital" da semente do sorteio, publicada com antecedência). Depois da apuração, revela a **semente** e o próprio navegador de quem visita **recalcula** e confirma que o resultado bate com o lacre — sem precisar confiar na sua palavra. Veja mais em [Módulo Apuração](/modulos/apuracao/).

![Painel de verificação do sorteio](/assets/screenshots/bp-33-verificacao.png)

## Usando os blocos (Gutenberg)

No editor de uma página ou post, clique em **adicionar bloco** (o “+”), procure por **“RIT360 Premiado”** e escolha o componente na categoria **RIT360 Premiado**. Com o bloco selecionado, abra o painel de configurações à direita e **escolha a campanha** no menu suspenso (ou informe o ID manualmente).

![Bloco do RIT360 Premiado no editor do WordPress](/assets/screenshots/bp-26-blocos-editor.png)

> 💡 **Nota**
>
> No editor, o bloco aparece como um marcador (“RIT360 Premiado · …”). A **aparência real** — a grade de cartões, o painel, a barra — aparece na **página publicada**, para quem visita o site.

## Usando os shortcodes (Elementor e outros)

Em construtores que aceitam shortcodes (como o Elementor, via o widget **Shortcode**), cole o shortcode do componente, ajustando o `id` da campanha. Também funciona direto no conteúdo de qualquer página/post.

## Segurança e privacidade

Os blocos e shortcodes usam exatamente a mesma proteção da página pública: só exibem campanhas **disponíveis publicamente** e nunca mostram dados privados. Se a campanha não estiver disponível (rascunho, cancelada, inexistente), o componente exibe uma **mensagem clara** no lugar.

> ✅ **Boas práticas**
>
> - Comece pela **Rifa completa** se quiser algo pronto rápido; use os componentes granulares quando quiser um layout próprio (por exemplo, a barra de progresso no topo da home e o botão comprar em vários pontos da página).
> - Sempre confira a página **no celular** antes de divulgar — a maioria dos participantes acessa pelo telefone.
