---
title: "Quando a reserva do cartão expira"
nav_order: 12
parent: "Guias por tarefa"
permalink: /guias/reserva-expirada/
task: reserva-expirada
role: participante
routes: ["/carrinho", "/finalizar-compra"]
screenshots: [carrinho-aviso-reserva-expirada]
source_docs: ["#176", CHANGELOG.md#2.18.2]
last_verified: 2026-08-04
status: publicado
---

# Quando a reserva do cartão expira

Esta página é para **quem compra** — e para quem atende compradores na organização.

Ao escolher um cartão, ele fica **guardado** para você por alguns minutos, o tempo de concluir a compra (a organização define esse tempo; o padrão são **15 minutos**). Se o carrinho ficar parado além disso, a reserva **expira** e o cartão volta a ficar disponível para outras pessoas.

## O aviso no carrinho

Quando isso acontece, o carrinho passa a mostrar um aviso junto ao item, em vez de deixar você descobrir só depois de pagar:

> *"Sua reserva expirou. Ao finalizar a compra tentaremos garantir os mesmos cartões — se algum já tiver sido escolhido por outra pessoa, você será avisado antes de pagar."*

![Aviso de reserva expirada no carrinho](/assets/screenshots/carrinho-aviso-reserva-expirada.png)

## O que acontece quando você finaliza

Ver o aviso **não** significa que você perdeu o cartão. Ao clicar em finalizar, o sistema tenta reservar de novo exatamente os mesmos cartões:

- **Se todos continuarem livres**, a compra segue normalmente — você não precisa fazer nada e recebe os mesmos cartões que escolheu.
- **Se alguém já tiver escolhido algum deles**, a compra é **interrompida antes de qualquer cobrança**, com uma mensagem dizendo qual cartão foi perdido.

## O que fazer se um cartão for perdido

Volte ao carrinho e **escolha outros cartões** — os que continuam disponíveis aparecem na grade da campanha. Depois é só finalizar normalmente.

> 💠 **Nada é cobrado sem cartão**
>
> Se o cartão não pôde ser garantido, a compra nem chega ao pagamento. Você não é cobrado por um cartão que não recebeu, e não fica pendência nenhuma no seu nome.

## Como evitar

- Finalize a compra logo depois de escolher os cartões — a reserva é curta de propósito, para não travar números que ninguém vai comprar.
- Se precisar de mais tempo, não tem problema deixar o carrinho parado: você só corre o risco de precisar escolher de novo, nunca o de pagar sem receber.

> Para a organização: o tempo de reserva é ajustável em **Configurações → Configurações Globais da Campanha**, e cada campanha pode ter o seu. Veja [Configurar a organização](/guias/configurar-organizacao/). Se um pedido antigo tiver ficado pago sem cartão, conserte por [Corrigir cartões](/guias/corrigir-cartoes/).
