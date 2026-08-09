---
title: "Configurar os e-mails"
nav_order: 6
parent: "Guias por tarefa"
permalink: /guias/configurar-emails/
task: configurar-emails
role: admin
routes: ["#/emails"]
screenshots: [bp-12-emails-templates, bp-13-emails-config, bp-14-emails-logs]
source_docs: [PRD_Bussola_Premiada.md#8.18, PRD_Bussola_Premiada.md#8.19]
last_verified: 2026-08-09
status: publicado
---

# Configurar os e-mails

O RIT360 Premiado envia e-mails automáticos que dão segurança ao comprador e mantêm você informado. Este guia mostra como revisar os textos, o remetente e acompanhar os envios.

## Onde fica

No **Painel**, clique no atalho **✉️ E-mails**. A tela tem quatro abas: **Templates**, **Configurações**, **Consentimentos** e **Log de envio**.

## Os e-mails automáticos

O plugin já traz modelos prontos para os momentos-chave:

- **Confirmação de compra** — vai ao comprador, com a lista dos cartões adquiridos.
- **Nova venda** — avisa os administradores da campanha a cada venda.
- **Estoque esgotado** — avisa quando todos os cartões foram vendidos.
- **Lançamento da campanha** — comunicação promocional na abertura.
- **Lembrete de sorteio** — avisa os participantes que a data se aproxima (envio automático diário).
- **Vendas encerradas** (novo na 2.20.0) — assim que o período de vendas termina, **todos os coordenadores da campanha** recebem um aviso com o resumo do que foi vendido (quantidade, percentual e valor arrecadado), a data prevista do sorteio e um **passo a passo do que fazer agora, escrito conforme o método de apuração daquela campanha**. É o e-mail que evita a campanha encerrar e ninguém perceber.
- **Mudança de data** — avisa todos os compradores se o sorteio for remarcado.
- **Resultado do sorteio** e **Ganhador** — fecham o ciclo após a apuração.

## Revisar os textos

Na aba **Templates**, edite o assunto e o corpo de cada e-mail. Você pode usar **variáveis** como o nome da campanha e os cartões, que o plugin substitui no envio. O layout já traz um **cabeçalho com a logo (ou o nome) da sua organização**, uma linha na **cor da OSC** e um **rodapé com a logo do RIT360** — automático, sem configuração.

![Aba Templates de e-mail](/assets/screenshots/bp-12-emails-templates.png)

Use o botão de **enviar teste** para receber uma amostra e conferir como fica.

## Configurar o remetente

Na aba **Configurações**, defina o **nome e o e-mail do remetente**. Esse é o "De:" que o comprador vê.

![Aba Configurações de e-mail](/assets/screenshots/bp-13-emails-config.png)

## Consentimento e opt-out

O plugin separa e-mails **transacionais** (confirmação de compra — sempre enviados) de **promocionais** (lançamento — só para quem **consentiu**). O consentimento é capturado no checkout, com a caixa **não** pré-marcada, respeitando a LGPD. Cada e-mail promocional traz um link de **descadastro** de um clique.

A aba **Consentimentos** lista quem aceitou receber comunicações e permite exportar em CSV.

## Acompanhar os envios

A aba **Log de envio** registra cada e-mail enviado: destinatário, assunto e status (**Enviado**, **Falhou** ou **Ignorado — sem consentimento**). O log **não** guarda o corpo do e-mail, por privacidade.

![Aba Log de envio](/assets/screenshots/bp-14-emails-logs.png)

> ✅ **Boas práticas**
>
> Envie um **teste de cada e-mail** para você mesmo antes de abrir a campanha. Ver o e-mail chegando com o layout da sua organização evita surpresas e transmite profissionalismo ao comprador.

> 💡 **Dica**
>
> Configure os **responsáveis da campanha** no formulário da campanha — são eles que recebem os avisos administrativos (nova venda, esgotado), em vez de um endereço genérico.
