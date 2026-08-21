---
title: "Criar a primeira campanha"
nav_order: 3
parent: "Guias por tarefa"
permalink: /guias/criar-primeira-campanha/
task: criar-primeira-campanha
role: admin
routes: ["#/campanhas", "#/campanhas/nova"]
screenshots: [bp-02-campanhas-lista, bp-03-campanha-nova-dados, bp-04-campanha-premio, campanha-premio-midia-multipla, bp-05-campanha-config, campanha-concurso-loteria-federal, campanha-categoria-woocommerce]
source_docs: [PRD_Bussola_Premiada.md#8.2, PRD_Bussola_Premiada.md#8.3, "#137", "#197", "#202"]
last_verified: 2026-08-21
status: publicado
---

# Criar a primeira campanha

Com a organização configurada e (opcionalmente) os cartões planejados, é hora de criar a campanha. Ela é preenchida em um formulário de **três etapas**.

> A partir da versão **2.4.0**, cada etapa traz uma **explicação com dicas e exemplos**, e os campos principais têm sugestões — é só seguir. Na última etapa você vê um **resumo** e os **próximos passos** antes de salvar.
> ![Etapa com orientação e dicas](/assets/screenshots/campanha-etapas-orientacao.png)

> 💡 Antes de começar, se ainda não fez a conta do prêmio, preço e quantidade, leia [Como planejar uma campanha que vende](/boas-praticas/campanha-vencedora/). Vale muito o tempo.

## Onde fica

No menu **RIT360 Premiado**, abra **Campanhas** e clique em **Nova campanha**.

![Lista de campanhas](/assets/screenshots/bp-02-campanhas-lista.png)

## Etapa 1 — Dados da Campanha

Nome da campanha, descrição curta, descrição completa e a **causa beneficiada**. A descrição completa e a causa aceitam **texto formatado** (negrito, títulos, listas, links) — use isso para contar a história do projeto.

![Etapa Dados da Campanha](/assets/screenshots/bp-03-campanha-nova-dados.png)

## Etapa 2 — Dados do Prêmio

Cada prêmio tem título, descrição, **custo do prêmio** (não aparece ao público; ajuda no cálculo do resultado líquido) e as **fotos do prêmio**. Você pode enviar **várias fotos** por prêmio e definir a **principal** — ela é a que aparece no compartilhamento.

![Etapa Dados do Prêmio](/assets/screenshots/bp-04-campanha-premio.png)

### Adicionar várias fotos de uma vez

Clique em **Adicionar foto(s)** para abrir a **Biblioteca de Mídia** do WordPress. A partir da versão **2.5.0**, você pode **selecionar várias imagens de uma só vez**: dê um **clique simples** em cada foto que quiser (sem precisar segurar Ctrl ou Shift) — cada uma marcada recebe o "check" azul — e clique em **Usar**. Todas as imagens selecionadas entram na galeria do prêmio de uma vez.

![Selecionar várias fotos do prêmio na Biblioteca de Mídia](/assets/screenshots/campanha-premio-midia-multipla.png)

A **primeira foto** da galeria é sempre a **principal** (marcada com a etiqueta *Principal*) — é ela que aparece no compartilhamento. Para trocar, passe o mouse sobre outra foto e clique em **Tornar principal**; para tirar uma foto, use **Remover**. Você pode clicar em **Adicionar foto(s)** quantas vezes quiser para incluir mais imagens.

### Um ou vários prêmios

A campanha pode ter **mais de um prêmio** (1º, 2º, 3º lugar…). Use o botão **+ Adicionar prêmio** para incluir cada um, na ordem em que serão sorteados. O primeiro é o **prêmio principal**. Para tirar um prêmio da lista, use **Remover**.

Todos os prêmios são sorteados **da mesma base de cartões vendidos, sem repetir número** — ou seja, cada prêmio vai para um cartão diferente. Se preferir um prêmio só, é só deixar apenas o primeiro; a campanha funciona exatamente como antes.

> 💡 O que muda com vários prêmios: o **regulamento** lista todos os prêmios na ordem; o **resultado público** e os **e-mails** mostram um ganhador por prêmio; e a **prestação de contas** soma os custos de todos os prêmios ao calcular a margem.

> ✅ Capriche nas fotos e no título do prêmio — é o que mais influencia as vendas. Veja [Como escolher um prêmio que vende](/boas-praticas/escolher-premio/).

## Etapa 3 — Configurações da Campanha

Aqui ficam os números e as regras:

- **Valor unitário do cartão** e **quantidade de cartões** (obrigatórios).
- **Datas** de início/fim das vendas e — conforme o método de apuração — a data do **sorteio** ou o **concurso** que vai definir essa data (veja abaixo).
- **Tempo de reserva do cartão** (em minutos) — quanto tempo um cartão fica "segurado" no carrinho antes de voltar ao pool se a compra não for concluída.
- **Método de apuração** — **Loteria Federal**, **Apuração interna auditável** ou **Registro manual**.
- **Categoria da campanha** — a subcategoria que classifica a receita no WooCommerce (veja abaixo).
- **Descontos por quantidade** (opcional).

![Etapa Configurações da Campanha](/assets/screenshots/bp-05-campanha-config.png)

> **O método de apuração fica só aqui (versão 2.22.0).** Este é o **único** lugar onde o método é definido. Ele governa o sorteio (aba Apuração), o texto do regulamento e a exibição do **número de sorteio** do cartão para o comprador — e é **obrigatório para publicar** a campanha. Antes havia um segundo seletor na aba Apuração, que podia discordar deste; ele deixou de existir. Detalhes em [Realizar o sorteio](/guias/realizar-sorteio/).

### Loteria Federal: você escolhe o concurso, não a data
{: #concurso-loteria-federal }

> **Mudou na versão 2.26.0.** Se o método de apuração for **Loteria Federal**, você não digita mais a data do sorteio — você escolhe **qual concurso** vai valer.

Ninguém consegue saber com antecedência a data exata do próximo concurso da Loteria Federal: quem depende de um calendário da Caixa está sempre chutando. Por isso o que a campanha registra é uma **regra** — "o 3º concurso realizado depois do fim das vendas", por exemplo — nunca uma data fixa. É essa regra que vale para valer o sorteio e para o regulamento, mesmo que o calendário da Caixa mude depois.

Escolha entre o **1º e o 5º concurso** da Loteria Federal realizado **após o encerramento das vendas**. Cada opção mostra a **data prevista**, sempre rotulada como **estimativa, sujeita a alteração pela Caixa** — é só uma referência para você e para quem compra, calculada a partir do calendário de concursos da Caixa.

![Seletor de concurso da Loteria Federal, com a previsão de cada opção](/assets/screenshots/campanha-concurso-loteria-federal.png)

> 💡 **Exemplo**
>
> As vendas da "Rifa do Dia das Crianças" terminam em 05/10/2026. Você escolhe o **2º concurso** depois disso. O sistema mostra a previsão — hoje, 12/10/2026 — mas o que fica gravado é a regra "2º concurso após 05/10/2026". Se a Caixa antecipar ou atrasar um sorteio no meio do caminho, a previsão exibida se ajusta sozinha; a regra continua sendo a mesma.

> ⚠️ **Métodos interna e manual continuam com data digitada.** A mudança vale só para Loteria Federal. Campanha que já existia antes da 2.26.0 também mantém a data que já tinha — ela só passa a funcionar por concurso se você entrar na campanha e escolher um.

### Categoria da campanha no WooCommerce
{: #categoria-campanha }

> **Novidade da versão 2.29.0.** Toda campanha ganha uma **categoria de produto** no WooCommerce — o que faz a receita da campanha chegar **já classificada** ao RIT360 Financeiro, entrando direto na prestação de contas segmentada por campanha, em vez de cair sem categoria.

Você não precisa saber o que é "categoria de produto do WooCommerce" para usar este campo: pense nele como uma **gaveta** para a receita desta campanha, dentro da gaveta maior "Campanhas premiadas". Duas opções:

- **Escolher uma subcategoria já existente**, no seletor.
- **Criar uma nova**, digitando o nome em **Nova subcategoria…** e clicando em **Criar subcategoria**.

**Se você não escolher nada, o sistema usa o nome da campanha** como subcategoria — a campanha nunca fica sem categoria, mesmo que você pule este campo.

![Campo Categoria da campanha, com a hierarquia Campanhas premiadas e o seletor de subcategoria](/assets/screenshots/campanha-categoria-woocommerce.png)

> 💡 Campanhas que já existiam antes da 2.29.0 foram classificadas **automaticamente** na atualização — você não precisa voltar em nenhuma delas para corrigir isso.

## Salvar e completar

O botão de salvar fica sempre visível. Se algum campo obrigatório faltar, o formulário te leva direto à aba do primeiro erro.

Depois de salvar o rascunho, complete o restante nas **abas de topo** da campanha:

- **Regulamento** — obrigatório para publicar. Veja [Publicar o regulamento](/guias/publicar-regulamento/).
- **Dados legais** — número de autorização, processo, observações (opcional, mas recomendado). O campo **Observações jurídicas** tem um **editor de texto rico** (negrito, listas, links).
- **Página pública** — aparência (herdar o padrão da organização ou escolher tema/esquema/fonte), transparência e compartilhamento. Veja [Personalizar a página pública](/guias/personalizar-pagina-publica/).

## Publicar (abrir) a campanha

Quando tudo estiver pronto, use os botões de transição de estado para **Publicar (abrir)** — ou **Programar** para uma data futura. Um **checklist ao vivo** mostra o que ainda falta; o item "regulamento publicado" é **bloqueante**: sem ele, a campanha não abre.

> ⚠️ **Atenção**
>
> Enquanto a campanha está em **rascunho**, você pode ajustar quase tudo, inclusive regerar os cartões. Depois de publicada e com vendas, muitas coisas travam para proteger a integridade da rifa (quantidade de cartões, valor). Revise com cuidado antes de abrir.

Veja todos os estados possíveis em [Módulo Campanhas](/modulos/campanhas/).
