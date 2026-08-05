---
title: "Acompanhar as vendas"
nav_order: 7
parent: "Guias por tarefa"
permalink: /guias/acompanhar-vendas/
task: acompanhar-vendas
role: admin
routes: ["#/", "#/campanhas"]
screenshots: [bp-01-dashboard, bp-02-campanhas-lista]
source_docs: [PRD_Bussola_Premiada.md#8.23]
last_verified: 2026-07-05
status: publicado
---

# Acompanhar as vendas

Com a campanha no ar, o **Painel** é onde você acompanha tudo: quanto entrou, quais campanhas estão bombando e quais sorteios estão chegando.

## O Painel

Abra **RIT360 Premiado → Painel**. Ele traz uma visão consolidada de todas as campanhas.

![Painel com indicadores](/assets/screenshots/bp-01-dashboard.png)

Você encontra:

- **Filtro de período** — Tudo, mês atual (padrão), mês anterior, ano atual, ano anterior ou um período personalizado. O período é ancorado na **data do sorteio**.
- **Valor apurado e resultado líquido** — considerando as **campanhas encerradas** no período.
- **Ranking de campanhas** — por valor bruto e líquido.
- **Campanhas por status**, **ticket médio**, **máximo e mínimo de faturamento**, **média de compradores únicos** e mais.
- **Próximas de sortear** — as campanhas com sorteio à frente, com contagem regressiva.

> 💡 **Nota**
>
> Os indicadores financeiros (valor apurado, líquido) só contam campanhas **encerradas** no período. Se você acabou de lançar e ainda não encerrou nenhuma, é normal ver R$ 0,00 nesses cartões — os números aparecem conforme as campanhas se concluem.

## A lista de campanhas

Em **Campanhas**, você vê todas com seu status atual e acessa cada uma para ver o **progresso de vendas** (cartões vendidos, reservados, disponíveis).

![Lista de campanhas](/assets/screenshots/bp-02-campanhas-lista.png)

## Como as vendas funcionam nos bastidores

- Quando alguém escolhe cartões, eles ficam **reservados** por alguns minutos.
- Ao concluir o checkout, a reserva vira **pedido**; ao confirmar o pagamento, os cartões viram **vendidos**.
- Se a compra não é concluída no tempo de reserva, os cartões **voltam ao pool** automaticamente. O comprador é avisado no carrinho e, ao finalizar, o sistema tenta garantir os mesmos cartões — se algum já tiver dono, a compra é interrompida **antes de cobrar** (veja [Quando a reserva do cartão expira](/guias/reserva-expirada/)).
- Se mesmo assim algo sair do trilho — um pedido pago sem cartão ou um cartão preso —, resolva pelo painel **Corrigir cartões** da campanha. Veja [Corrigir cartões](/guias/corrigir-cartoes/).
- Pedidos cancelados, falhos ou reembolsados **liberam** os cartões de volta — exceto depois que a base do sorteio já foi congelada.

> ✅ **Boas práticas**
>
> Acompanhe o ritmo de vendas na metade da campanha. Se estiver lento, é hora de reforçar a divulgação (veja [Como divulgar e vender mais](/boas-praticas/vender-mais/)). O painel de transparência da página pública também ajuda a criar urgência mostrando quantos cartões faltam.
