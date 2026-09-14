---
title: "Gerenciar usuários e papéis"
parent: "Guias por tarefa"
permalink: /guias/gerenciar-usuarios/
role: admin
routes: ["#/organizacao"]
screenshots: [bp-27-config-usuarios]
source_docs: [PRD_Bussola_Premiada.md#8.25, BP-135]
last_verified: 2026-09-14
status: publicado
---

# Gerenciar usuários e papéis

Cada pessoa que trabalha no RIT360 Premiado recebe um ou mais **papéis**, que definem o que ela pode ver e fazer. É pela aba **Usuários** que você atribui esses papéis — e é o que libera o acesso de cada membro da equipe ao painel com a permissão certa, nem mais, nem menos.

> Só o **Administrador da organização** (e o administrador do site) enxerga esta aba. Toda mudança de papel fica registrada na [Trilha de auditoria](/modulos/auditoria/).

## Antes de começar

A pessoa precisa **já ser um usuário do WordPress** do site. Se ela ainda não tem acesso, crie o usuário primeiro em **Usuários** do WordPress (menu do site, fora do plugin) — o RIT360 Premiado não cria usuários, apenas atribui papéis a quem já existe.

## Passo a passo

1. No menu do plugin, abra **Configurações** e vá até a aba **Usuários**.
   ![Aba Usuários em Configurações](/assets/screenshots/bp-27-config-usuarios.png)
2. Encontre a pessoa na lista. Se houver muitos usuários, use o campo **Buscar usuário** (por nome, login ou e-mail) e clique em **Buscar**.
3. Marque o(s) papel(is) que ela deve ter: **Administrador da campanha**, **Auditor** e/ou **Operador**. A alteração é **salva na hora** ao marcar ou desmarcar.
4. Para **remover** um papel, basta desmarcar. Desmarcar todos remove o acesso da pessoa ao plugin.

Entenda o que cada papel permite em [Papéis](/papeis/).

## Vários papéis na mesma pessoa

Você pode combinar papéis. Quem for, por exemplo, **Operador** e **Auditor** ao mesmo tempo soma as permissões dos dois. Em equipes pequenas isso é comum; em equipes maiores, prefira dar a cada pessoa só o que ela precisa.

## Perguntas comuns

- **Por que a lista de "Responsáveis pela campanha" estava vazia?** Porque ninguém tinha papel ainda. Depois de atribuir papéis aqui, as pessoas passam a aparecer para seleção no formulário da campanha (aba **Configurações**).
- **O administrador do site precisa de papel?** Não. Quem administra o WordPress já tem acesso total ao plugin — aparece na lista com a marca *(admin do site)* e não precisa de papel atribuído.
- **Removi meu próprio acesso sem querer.** Sem problema: o administrador do site sempre consegue voltar aqui e reatribuir os papéis.

> ✅ **Boas práticas**
>
> Dê ao conselho fiscal ou ao contador um acesso de **Auditor** — eles acompanham tudo com transparência, sem risco de alterar dados. Separe os papéis sempre que a equipe permitir: quem opera as vendas não precisa decidir o resultado do sorteio.
