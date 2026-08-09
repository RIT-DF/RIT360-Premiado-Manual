---
title: "E-mails"
nav_order: 6
parent: "Módulos"
permalink: /modulos/emails/
role: admin
routes: ["#/emails"]
screenshots: [bp-12-emails-templates, bp-14-emails-logs]
last_verified: 2026-08-09
status: publicado
---

# E-mails

O módulo de e-mails cuida de toda a comunicação automática da campanha, com respeito à LGPD. Você o acessa pelo atalho **✉️ E-mails** no Painel.

![Templates de e-mail](/assets/screenshots/bp-12-emails-templates.png)

## Quatro abas

- **Templates** — edite assunto e corpo de cada e-mail, com variáveis substituídas no envio e o layout da sua organização. Botão de **enviar teste**.
- **Configurações** — nome e e-mail do remetente.
- **Consentimentos** — quem aceitou receber comunicações promocionais; exportável em CSV.
- **Log de envio** — cada envio com destinatário, assunto e status. Sem o corpo do e-mail, por privacidade.

![Log de envio](/assets/screenshots/bp-14-emails-logs.png)

## E-mails disponíveis

Confirmação de compra · Nova venda (admin) · Estoque esgotado · Lançamento da campanha · Lembrete de sorteio · **Vendas encerradas (coordenadores)** · Mudança de data · Resultado do sorteio · Ganhador.

O **Vendas encerradas** (novo na 2.20.0) sai quando o período de vendas termina, para **todos os coordenadores** da campanha: traz o resumo das vendas, a data prevista do sorteio e as **próximas ações conforme o método de apuração** escolhido.

## Transacional vs. promocional

- **Transacional** (ex.: confirmação de compra) — sempre enviado, é parte da transação.
- **Promocional** (ex.: lançamento) — só para quem **consentiu**. O consentimento é capturado no checkout com a caixa **não** pré-marcada, e cada promocional traz **descadastro** de um clique.

## Visual próprio da organização

Todos os e-mails do plugin usam um **layout institucional** que os diferencia dos e-mails padrão da loja: um **cabeçalho** com a **logo da sua organização** (ou o nome, se não houver logo) sobre fundo branco, separado do corpo por uma **linha na cor principal da OSC**, e um **rodapé** com a **logo do RIT360** e o contato da organização. É automático e vale para todos os e-mails — você não precisa configurar nada.

## Multicanal por design

A base de notificações foi construída para crescer: SMS e WhatsApp podem ser adicionados no futuro sem reescrever os e-mails.

O passo a passo está em [Configurar os e-mails](/guias/configurar-emails/).

> 💡 **Dica**
>
> Os avisos administrativos (nova venda, esgotado) vão para os **responsáveis da campanha** definidos no formulário — não para um endereço genérico. Configure-os para que as notificações cheguem a quem realmente acompanha a campanha.
