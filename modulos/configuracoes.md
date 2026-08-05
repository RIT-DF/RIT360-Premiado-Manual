---
title: "Configurações"
nav_order: 9
parent: "Módulos"
permalink: /modulos/configuracoes/
role: admin
routes: ["#/organizacao"]
screenshots: [bp-15-config-organizacao, bp-16-config-identidade, bp-27-config-usuarios, bp-28-config-globais-campanha, bp-19-config-apuracao, bp-20-config-pdf]
last_verified: 2026-07-05
status: publicado
---

# Configurações

A seção **Configurações** guarda os dados da organização e os padrões globais que valem para todas as campanhas. É organizada em abas.

![Aba Configurações da Organização](/assets/screenshots/bp-15-config-organizacao.png)

## As abas

- **Configurações da Organização** — razão social, CNPJ (validado, formato numérico e alfanumérico), endereço e e-mail. É a **fonte única** que alimenta regulamento, e-mails e página pública.
- **Identidade visual** — logomarca, favicon e cores da marca (seletor ou valor hexadecimal). Personaliza as páginas públicas.
  ![Aba Identidade visual](/assets/screenshots/bp-16-config-identidade.png)
- **Usuários** — atribui os **papéis** do plugin (Administrador da campanha, Auditor, Operador — um ou mais por pessoa) aos usuários do WordPress. Visível para o Administrador da organização e o administrador do site. Passo a passo em [Gerenciar usuários e papéis](/guias/gerenciar-usuarios/).
  ![Aba Usuários](/assets/screenshots/bp-27-config-usuarios.png)
- **Configurações Globais da Campanha** — o **contato de dúvidas** que aparece no regulamento e os **padrões de reserva de cartões** (*Tempo de reserva do cartão* — por quantos minutos um cartão escolhido fica reservado para a pessoa concluir a compra, **padrão: 15 minutos** — e *máximo de cartões por reserva*). Cada campanha pode sobrescrever esses padrões.
  ![Aba Configurações Globais da Campanha](/assets/screenshots/bp-28-config-globais-campanha.png)
- **Banco de Cláusulas de Regulamento** — a biblioteca de cláusulas prontas usada no regulamento.
- **Apuração** — os padrões globais de sorteio (método padrão, política do contemplado reembolsado).
  ![Aba Apuração](/assets/screenshots/bp-19-config-apuracao.png)
- **PDF / Relatórios** — o motor de geração de PDF dos documentos.
  ![Aba PDF / Relatórios](/assets/screenshots/bp-20-config-pdf.png)
- **Doação à RIT** — o apoio voluntário (veja [Doação à RIT](/modulos/doacao-rit/)).

## Snapshots

Quando um documento é emitido (como o regulamento), o plugin **congela** os dados da organização naquele instante. Mudanças posteriores não alteram documentos já publicados — cada um preserva o que valia quando foi emitido.

O passo a passo está em [Configurar a organização](/guias/configurar-organizacao/).

> ✅ **Boas práticas**
>
> Preencha e confira **tudo** aqui antes de criar campanhas. Esses dados se propagam para documentos legais — um erro no CNPJ ou na razão social aparece em todos os regulamentos emitidos depois.
