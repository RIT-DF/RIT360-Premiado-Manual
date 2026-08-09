---
title: "Página pública"
nav_order: 5
parent: "Módulos"
permalink: /modulos/pagina-publica/
role: admin
routes: ["#/organizacao", "#/campanhas/:id", "/campanha/:slug"]
screenshots: [bp-10-pagina-publica-admin, bp-11-pagina-publica-site, tema-01-org-identidade, publica-tamanho-texto, publica-vendas-encerradas, publica-transparencia]
last_verified: 2026-08-09
status: publicado
---

# Página pública

Cada campanha tem um **hotsite próprio**, mobile-first, no endereço `/campanha/nome-da-campanha`. É a vitrine da sua rifa.

![Página pública da campanha](/assets/screenshots/bp-11-pagina-publica-site.png)

## O que a página traz

- O(s) **prêmio(s)** com galeria de fotos — quando a campanha tem vários prêmios, todos aparecem em ordem (1º, 2º, 3º…).
- A **história da causa** (texto rico).
- O **progresso das vendas** e o **painel de transparência** (indicadores que você escolhe — incluindo **Participantes** e **Resultado do sorteio**, a partir da 2.23.0). ⚠️ O painel só é exibido nos temas **Clássico, Emotivo e Sofisticado**; veja [Painel de transparência](/guias/personalizar-pagina-publica/#painel-transparencia).
- A **seleção de cartões** (manual ou automática).
- O **regulamento**.
- A **barra de compartilhamento** (WhatsApp, Facebook, X, LinkedIn, copiar link).
- O **resultado** do sorteio, quando a campanha é apurada — com um ganhador por prêmio, sempre mascarado por padrão.
- Um **aviso de vendas encerradas** (a partir da 2.20.0), assim que o período de vendas termina, informando **a data prevista do sorteio**. Quem chega à página depois do prazo entende na hora o que aconteceu, em vez de tentar comprar e receber um erro.

  ![Aviso de vendas encerradas na página pública](/assets/screenshots/publica-vendas-encerradas.png)
- Um **controle de acessibilidade de tamanho do texto** (**A− / A / A+**) no canto superior direito do topo, que o visitante usa para ampliar ou reduzir a leitura. Aparece sozinho em toda campanha. Detalhes em [Personalizar a página pública](/guias/personalizar-pagina-publica/#acessibilidade--tamanho-do-texto).

## Configuração (guiada por temas)

A aparência é **guiada por temas** e definida em dois níveis:

- **Padrão da organização** — em **Configurações → Identidade da página pública**, você escolhe o **tema** (Sofisticado, Moderno, Clássico, Divertido, Emotivo, Simples), o **esquema de cores** (Claro / Escuro / Automático), a **fonte** e as **seções** que aparecem por padrão. As **cores da organização** valem na página inteira.

  ![Aba Identidade da página pública](/assets/screenshots/tema-01-org-identidade.png)

- **Por campanha** — na aba **Página pública** da campanha, você escolhe **Usar o padrão da organização** (herda tudo) ou **Personalizar esta campanha** (tema/esquema/fonte/seções só para aquela rifa). Aqui também ficam os indicadores de **transparência**, a **meta/termômetro**, o **vídeo** e o **compartilhamento/Open Graph**.

  ![Aba Página pública no admin](/assets/screenshots/bp-10-pagina-publica-admin.png)

## Identidade da organização na página

A partir da versão **2.23.0**, três dados da organização que já existiam nas Configurações passaram a aparecer de fato na página pública: o **favicon** (o ícone da aba do navegador), o **texto institucional curto** e o **contato de dúvidas da campanha**. Não é preciso configurar nada de novo — se os campos estiverem preenchidos em [Configurar a organização](/guias/configurar-organizacao/), eles passam a valer.

## Shortcodes para page builders

Quer usar partes da campanha em outra página do site? Há shortcodes prontos, por exemplo:

- `[rit360_premiado_rifa id="123"]` — a campanha completa.
- `[rit360_premiado_comprar id="123"]` — a seleção de cartões.
- `[rit360_premiado_regulamento id="123"]` — o regulamento.
- `[rit360_premiado_painel id="123"]` — o painel de transparência.

## Segurança e privacidade

A página pública usa uma **lista de exposição explícita**: nunca mostra identificadores internos, o token da página nem dados pessoais. O valor arrecadado só aparece se você **optar** por exibi-lo.

O passo a passo está em [Personalizar a página pública](/guias/personalizar-pagina-publica/).

> ⚠️ **Atenção — 404 no endereço da campanha**
>
> Se `/campanha/nome` retornar "não encontrado", vá em **Configurações → Links permanentes** do WordPress e clique em **Salvar** para regenerar as regras. O plugin tenta fazer isso automaticamente, mas o permalink "simples" do WordPress pode exigir o passo manual.
