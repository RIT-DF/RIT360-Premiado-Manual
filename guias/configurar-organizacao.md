---
title: "Configurar a organização"
nav_order: 1
parent: "Guias por tarefa"
permalink: /guias/configurar-organizacao/
task: configurar-organizacao
role: admin
routes: ["#/organizacao"]
screenshots: [bp-15-config-organizacao, bp-16-config-identidade, bp-28-config-globais-campanha]
source_docs: [PRD_Bussola_Premiada.md#8.1, CHANGELOG.md#2.6.0]
last_verified: 2026-08-09
status: publicado
---

# Configurar a organização

Os dados da sua organização são a **fonte única** que alimenta o regulamento, os e-mails e a página pública de todas as campanhas. Configure uma vez, com calma, e não precisará repetir a cada campanha.

## Onde fica

No menu **RIT360 Premiado**, abra **Configurações**. A tela tem várias abas no topo.

## Passo a passo

1. Abra **Configurações** e fique na aba **Configurações da Organização**.
   ![Aba Configurações da Organização](/assets/screenshots/bp-15-config-organizacao.png)
2. Preencha os **dados institucionais**: razão social, CNPJ, endereço e e-mail. Razão social, CNPJ e e-mail são obrigatórios — o plugin valida o CNPJ (aceita o formato numérico e o novo alfanumérico da Receita Federal).
   - **Redes sociais** (a partir da 2.4.0): em vez de um campo único, você monta uma **lista** — clique em **"+ Adicionar rede"**, escolha a rede (Instagram, Facebook, WhatsApp, YouTube…) e cole o link. No seletor **"Exibir as redes na página pública"**, escolha se elas aparecem no **rodapé**, no **topo** da página da campanha, ou **não exibir**.
     ![Editor de redes sociais da organização](/assets/screenshots/redes-01-editor.png)
3. Vá para a aba **Identidade visual** e envie a **logomarca** e o **favicon** pela Biblioteca de Mídia do WordPress. Ajuste as **cores da marca** — você pode escolher no seletor de cor ou digitar o valor hexadecimal (ex.: `#192444`). A partir da 2.6.0, essas cores valem na **página pública inteira** das campanhas (não só no topo).
   ![Aba Identidade visual](/assets/screenshots/bp-16-config-identidade.png)
   - **Identidade da página pública** (aba própria, a partir da 2.6.0): define o **padrão** visual das páginas públicas de campanha — o **tema** (galeria de 6 modelos com preview ao vivo nas suas cores), o **esquema de cores** (Claro / Escuro / Automático), a **fonte** e as **seções** exibidas. Toda campanha nova nasce com esse padrão e pode herdá-lo ou personalizá-lo. O passo a passo está em [Personalizar a página pública](/guias/personalizar-pagina-publica/).
4. Na aba **Configurações Globais da Campanha**, informe o **Contato de dúvidas da campanha** — o e-mail ou telefone que aparece **no regulamento, no rodapé da página pública da campanha e no e-mail de confirmação de compra**, para os participantes tirarem dúvidas. Se ficar em branco, o plugin usa o e-mail da organização. Ajuste também os **padrões de reserva de cartões** — o *Tempo de reserva do cartão* (por quantos minutos um cartão escolhido fica reservado para a pessoa concluir a compra — **padrão: 15 minutos**) e o *máximo de cartões por reserva*. Cada campanha pode sobrescrever esses padrões.
   ![Aba Configurações Globais da Campanha](/assets/screenshots/bp-28-config-globais-campanha.png)
5. **Salve** cada aba. O salvamento é por aba, então confirme antes de trocar de seção.

> **Três campos que passaram a funcionar (versão 2.23.0)**
>
> O **favicon** (aba *Identidade visual*), o **texto institucional curto** (aba *Configurações da Organização*) e o **contato de dúvidas** (aba *Configurações Globais da Campanha*) já existiam na tela, mas não surtiam efeito nenhum. Agora aparecem de verdade: o favicon é o ícone da **aba do navegador** na página pública da campanha, o texto institucional curto e o contato de dúvidas aparecem **na própria página pública**. Se você já tinha preenchido esses campos, não precisa fazer nada — eles simplesmente passam a valer.

## As outras abas

A tela de Configurações também guarda ajustes que você vai usar depois:

- **Banco de Cláusulas de Regulamento** — a biblioteca de cláusulas prontas que alimenta o regulamento das campanhas.
- **Apuração** — os padrões globais de sorteio (política do contemplado reembolsado, exposição pública do ganhador) e a opção de **buscar automaticamente o resultado da Loteria Federal**. Veja [Realizar o sorteio](/guias/realizar-sorteio/#busca-automatica).
  - O campo **"Regra de não-bate (método externo)"** que aparece nesta aba é de versões anteriores: desde a 2.21.0 a apuração pela Loteria Federal **sempre encontra um cartão**, então não há mais regra de aproximação a aplicar. Pode ignorá-lo.
- **PDF / Relatórios** — o motor de geração de PDF dos documentos.

> 💡 **Dica**
>
> Quando você publica o regulamento de uma campanha, o plugin tira uma **"foto" (snapshot)** dos dados da organização naquele instante. Ou seja: mudar os dados depois **não** altera regulamentos já publicados — cada documento preserva o que valia quando foi emitido. Por isso, preencha tudo corretamente **antes** de publicar campanhas.

> ✅ **Boas práticas**
>
> Confira o CNPJ e a razão social com o cartão CNPJ oficial. Esses dados vão para documentos legais e para o regulamento — um erro aqui se propaga para tudo.
