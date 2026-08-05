---
title: "Corrigir cartões"
nav_order: 8
parent: "Guias por tarefa"
permalink: /guias/corrigir-cartoes/
task: corrigir-cartoes
role: admin
routes: ["#/campanhas/:id"]
screenshots: [corrigir-01-painel, corrigir-02-detalhe-cartao-vendido, corrigir-03-vincular-pedido, corrigir-04-vinculo-aplicado, corrigir-05-pedido-com-cartoes, corrigir-06-recusa-pedido-com-cartoes, corrigir-07-liberar-cartao-preso, corrigir-08-auditoria]
source_docs: ["#177", "#176", CHANGELOG.md#2.19.0]
last_verified: 2026-08-04
status: publicado
---

# Corrigir cartões

Quase sempre a venda de cartões corre sozinha: a pessoa escolhe, paga e o cartão fica com ela. Mas rifa é dinheiro de gente real, e de vez em quando algo sai do trilho — um pagamento que entra sem o cartão aparecer no pedido, um cartão que fica "segurado" e não volta para a venda.

O painel **Corrigir cartões** existe para você resolver essas situações **pela tela do plugin**, sem depender de suporte técnico.

## Onde fica

Abra a campanha. Na **coluna da direita** do formulário, logo abaixo do quadro **Cartões**, está o painel **Corrigir cartões**. Você busca um cartão pelo **número (posição)** ou pelo **nome** dele e clica em **Detalhes**.

![Painel Corrigir cartões na tela da campanha](/assets/screenshots/corrigir-01-painel.png)

---

## Um comprador pagou e não recebeu o cartão

É o caso principal — e o motivo de esta ferramenta existir. O pagamento entrou, mas o pedido do WooCommerce não mostra nenhum cartão, e o cartão que a pessoa tinha escolhido voltou para a venda.

> Desde a versão 2.18, o sistema evita que isso aconteça: se a reserva expirar, ele tenta garantir os mesmos cartões na finalização e, se algum já tiver dono, interrompe a compra **antes de cobrar**. Ainda assim, pedidos antigos podem ter ficado nessa situação — e é aqui que você os conserta.

### Passo a passo

1. **Descubra qual cartão a pessoa escolheu.** Normalmente ela informa ("comprei o *Furão*"); se não, o e-mail de confirmação ou a conversa com o comprador ajudam.
2. **Anote o número do pedido** no WooCommerce (em **WooCommerce → Pedidos**). Ele precisa estar **pago** e ainda **sem cartões**.
3. Abra a campanha, busque o cartão no painel **Corrigir cartões** e clique em **Detalhes**.
4. Confira o estado: o cartão precisa estar **Disponível**. Se estiver, aparece o bloco **Vincular a um pedido pago**.
5. Informe o **nº do pedido** e escreva a **justificativa** (obrigatória) — em uma frase, o que aconteceu.
6. Marque **Notificar o comprador por e-mail** se quiser que ele receba a confirmação com o cartão. Clique em **Vincular cartão ao pedido**.

   ![Formulário de vínculo preenchido, com a justificativa](/assets/screenshots/corrigir-03-vincular-pedido.png)

7. Pronto. O cartão passa a **Vendido**, some da grade pública e o vínculo com o pedido aparece na tela — junto com o registro no histórico.

   ![Cartão vendido logo após o vínculo, com o registro no histórico](/assets/screenshots/corrigir-04-vinculo-aplicado.png)

8. **Confira no pedido.** Abra o pedido no WooCommerce: o item agora traz a linha **Cartões** com o nome do cartão.

   ![Pedido do WooCommerce exibindo a linha Cartões](/assets/screenshots/corrigir-05-pedido-com-cartoes.png)

### Se o sistema recusar

O plugin não deixa você criar um problema maior do que o que está resolvendo. As recusas mais comuns:

- **"O pedido já tem cartões vinculados."** Aquele pedido não é o pedido órfão — confira o número. Um pedido nunca recebe cartões duas vezes.

  ![Mensagem de recusa: o pedido já tem cartões vinculados](/assets/screenshots/corrigir-06-recusa-pedido-com-cartoes.png)

- **O cartão não está disponível.** Se ele já foi vendido ou está reservado, o formulário de vínculo nem aparece — outra pessoa pode ter comprado nesse meio-tempo. Nesse caso, converse com o comprador e ofereça outro cartão.
- **A apuração já está congelada.** Depois que a base do sorteio é fechada, nenhum cartão novo entra nela. O vínculo é bloqueado para não alterar quem concorre.

---

## Como ver o que aconteceu com um cartão

Antes de corrigir qualquer coisa, olhe o estado real do cartão. Busque, clique em **Detalhes** e você vê:

- a **situação** — Disponível, Reservado ou Vendido;
- a **reserva** ligada a ele (se houver) e quando ela expira;
- o **pedido** ligado a ele, com a situação e o e-mail do comprador;
- o **histórico de auditoria** do cartão.

![Detalhe de um cartão vendido](/assets/screenshots/corrigir-02-detalhe-cartao-vendido.png)

> ⚠️ **Cartão vendido não tem ação nesta tela**
>
> Quando o cartão já está **Vendido**, o painel mostra os dados mas não oferece nenhum botão. É proposital: mexer num cartão que alguém já pagou pode desfazer uma venda legítima e tirar da rifa quem tinha direito de concorrer. Essas situações exigem apuração caso a caso — fale com o suporte técnico antes de qualquer coisa.

---

## Um cartão ficou preso e não volta para a venda

Às vezes um cartão fica **Reservado** e não é liberado sozinho: o comprador desistiu no meio do caminho, ou a reserva morreu sem devolver o cartão ao pool. Enquanto isso, ninguém consegue comprá-lo.

1. Busque o cartão e abra os **Detalhes**. Ele estará como **Reservado**.
2. No bloco **Liberar cartão preso**, escreva a **justificativa** (obrigatória).
3. Clique em **Liberar cartão**. Ele volta na hora para a grade pública, disponível para qualquer pessoa.

![Formulário de liberação preenchido](/assets/screenshots/corrigir-07-liberar-cartao-preso.png)

### Se houver um pedido pago envolvido

Se o cartão preso estiver ligado a um **pedido já pago**, o plugin não libera de primeira. Aparece um **alerta** explicando a consequência — o comprador ficaria sem o cartão que pagou — e uma caixa **"Confirmo que quero liberar mesmo assim"**, que você precisa marcar antes de o botão habilitar. A operação fica registrada como **exceção**.

Antes de confirmar, pense duas vezes: quase sempre o certo é falar com o comprador, e não liberar o cartão dele.

> ⚠️ **Depois do sorteio apurado, cartão vendido não volta para a venda**
>
> Quando a apuração é fechada, a lista de quem concorre fica congelada. A partir daí, um cartão **vendido** não sai dessa lista de jeito nenhum — nem com confirmação. Em bom português: **quem concorreu continua concorrendo**, e o resultado do sorteio não pode ser alterado por uma correção feita depois. O plugin registra a tentativa e mantém a base intacta.

---

## A justificativa é obrigatória — e é assim de propósito

Toda correção exige que você escreva **por que** está fazendo aquilo. Sem texto, o botão não habilita.

O que você escreve fica guardado junto com **quem fez**, **quando** e **o que foi alterado**, na [Trilha de auditoria](/modulos/auditoria/). Numa rifa, alterar um cartão à mão é uma exceção — e exceção sem rastro vira dúvida na hora de prestar contas ao conselho, ao contador ou a um participante que perguntar.

![Trilha de auditoria com a justificativa registrada](/assets/screenshots/corrigir-08-auditoria.png)

> ✅ **Boas práticas**
>
> Escreva a justificativa pensando em quem vai ler daqui a seis meses sem lembrar do caso: *"Pedido #1294 pago em 02/08 sem cartão registrado; vinculado o cartão Furão, escolhido pelo comprador."* É melhor que *"correção"*.
