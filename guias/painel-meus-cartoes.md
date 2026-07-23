---
title: "Painel Meus cartões"
nav_order: 11
parent: "Guias por tarefa"
permalink: /guias/painel-meus-cartoes/
task: painel-meus-cartoes
role: admin
routes: ["/meus-cartoes", "#/blocos"]
screenshots: [bp-36-meus-cartoes-painel, bp-37-meus-cartoes-painel-mobile, bp-38-meus-cartoes-formulario, publica-consulte-numeros]
source_docs: [CHANGELOG.md#1.11.0, CHANGELOG.md#2.15.2, ARCHITECTURE.md#adr-014]
last_verified: 2026-07-23
status: publicado
---

# Painel "Meus cartões" do comprador

O **"Meus cartões"** é uma página para o **participante** consultar, **sem precisar de login**, os cartões que comprou e o resultado do sorteio. Reduz as mensagens de suporte ("quais números eu comprei?", "ganhei?") e reforça a confiança na campanha. Novo na versão **1.11.0**.

## Como o comprador acessa

Há dois caminhos, e os dois dispensam senha:

- **Pelo link no e-mail.** Todo e-mail de **confirmação de compra** passa a trazer um link *"meus cartões"*. É um link pessoal e seguro (não é adivinhável) que abre direto o painel do comprador.
- **Pelo formulário "Receber o link por e-mail".** Se a pessoa não tem o e-mail à mão, ela abre a página, informa o **e-mail usado na compra** ou o **número do pedido** e clica em **Enviar link**. O sistema envia o link de acesso para o e-mail daquela compra.

  ![Formulário para receber o link por e-mail](/assets/screenshots/bp-38-meus-cartoes-formulario.png)

> Por segurança e privacidade, a resposta do formulário é **sempre a mesma** ("Se houver compras nesse e-mail, enviamos o link…"), independentemente de o e-mail ou o pedido existir ou não — assim ninguém consegue descobrir quem comprou testando endereços.

### "Consulte seus números" na própria página da campanha

A mesma consulta aparece **embutida na página pública da campanha**, na seção **"Consulte seus números"** — quem já participou informa o **e-mail** ou o **número do pedido** ali mesmo, sem sair da página, e recebe o link por e-mail. Essa seção pode ser ligada ou desligada em [Personalizar a página pública](/guias/personalizar-pagina-publica/) (item **Painel do comprador**).

![Seção "Consulte seus números" na página pública da campanha](/assets/screenshots/publica-consulte-numeros.png)

## O que o comprador vê

O painel agrupa tudo **por campanha**. Para cada campanha em que a pessoa participou, aparece:

- os **cartões** dela, em etiquetas — o número, ou o nome nas listas temáticas (e, nas campanhas apuradas pela **Loteria Federal**, o nome acompanhado do **número de sorteio**, ex.: *Gato-do-mato · 047*);
- a **situação do pedido** (por exemplo, "Concluído");
- quando o sorteio já aconteceu, o **resultado** — com destaque **"🎉 Você foi contemplado!"** se um dos cartões dela ganhou, o número sorteado e um link para **conferir a apuração**;
- um atalho para **ver a campanha e o regulamento**.

![Painel Meus cartões com o resultado do sorteio](/assets/screenshots/bp-36-meus-cartoes-painel.png)

A página é **mobile-first** — funciona bem no celular, que é por onde a maioria vai abrir o link do e-mail.

![Painel Meus cartões no celular](/assets/screenshots/bp-37-meus-cartoes-painel-mobile.png)

## Como publicar a página (para a organização)

Você tem três formas de disponibilizar o "Meus cartões" — escolha a que combina com o seu site:

1. **Endereço pronto `/meus-cartoes`.** A página já existe automaticamente no endereço do seu site terminando em **`/meus-cartoes`** (ex.: `suaosc.org.br/meus-cartoes`). É para lá que o link dos e-mails aponta. Não precisa configurar nada.
2. **Bloco Gutenberg.** No editor de qualquer página, clique em **adicionar bloco** ("+"), procure por **"RIT360 Premiado"** e escolha **Meus cartões** na categoria RIT360 Premiado. Útil para embutir o painel numa página do seu próprio layout (por exemplo, uma página "Participe" com menu e rodapé do site).
3. **Shortcode.** Cole `[rit360_premiado_meus_cartoes]` em qualquer página ou post.

Diferente dos outros blocos da campanha, o "Meus cartões" **não** pede o ID de uma campanha: ele mostra as campanhas do próprio comprador, a partir do link pessoal.

## Dicas

- Se o seu WordPress usa links "simples" (sem nome amigável na URL), o endereço do painel funciona como `suaosc.org.br/?bp_meus_cartoes=1`. O link enviado nos e-mails já sai no formato certo automaticamente.
- Quem estiver **logado** na sua loja WooCommerce continua vendo os cartões direto no pedido, em **Minha conta → Pedidos** — e agora com um atalho "Ver meus cartões e resultado".
