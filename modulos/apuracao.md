---
title: "Apuração"
nav_order: 7
parent: "Módulos"
permalink: /modulos/apuracao/
role: admin
routes: ["#/campanhas/:id"]
screenshots: [bp-21-apuracao, bp-33-verificacao, bp-19-config-apuracao]
last_verified: 2026-08-21
status: publicado
---

# Apuração

O módulo de apuração define o **ganhador** de forma auditável. Ele oferece três métodos e cuida da imutabilidade do resultado.

![Aba Apuração](/assets/screenshots/bp-21-apuracao.png)

## Onde o método é escolhido

O **método de apuração** é definido na aba **Formulário** da campanha (etapa *Configurações da Campanha*) — e **só ali**. A aba Apuração apenas **mostra** qual método está valendo e indica onde alterá-lo. Essa unificação chegou na versão **2.22.0**; antes havia dois seletores, que podiam discordar entre si e produzir uma campanha "certa" numa tela e "errada" na outra.

## Congelamento da base

Antes do sorteio, a lista de cartões vendidos é **congelada**: fica fixa, com uma "impressão digital" (hash). A partir daí, reembolsos e cancelamentos não devolvem mais o cartão ao pool — tudo fica registrado. No método interno, um **lacre** (`sha256` da semente) é publicado, provando que a semente foi definida antes do resultado (esquema *commit-reveal*).

## Três métodos

- **Apuração interna auditável** — semente lacrada + revelação ao finalizar. Sorteia sobre a base congelada completa, pulando reembolsados de forma determinística. **Qualquer auditor refaz a conta** e chega ao mesmo cartão.
- **Loteria Federal** — os **5 números** da extração oficial são concatenados na ordem em que saíram, formando um número **V**; o **resto da divisão de V pela quantidade de cartões vendidos (N)** aponta o contemplado na base ordenada. A conferência cabe numa planilha: `=MOD(V;N)+1`. Como o resto sempre cai dentro da lista, **o resultado sempre resolve** — não há mais regra de aproximação nem configuração de dígitos. **Desde a 2.26.0, a campanha não grava mais uma data digitada para este método** — o coordenador escolhe o **concurso** (1º a 5º após o fim das vendas) na etapa *Configurações da Campanha*, e o sistema deriva a data prevista, sempre como estimativa. Veja [Criar a primeira campanha](/guias/criar-primeira-campanha/#concurso-loteria-federal).
- **Registro manual** — resultado feito fora do sistema, registrado com justificativa e anexos.

## Automação da Loteria Federal

- **Busca do resultado** — o plugin consulta a extração oficial. Em **Configurações → Apuração** você pode ligar a **busca automática**, que pré-preenche o resultado assim que a campanha fica pronta para apurar; **a confirmação continua sendo humana**.
- **Aviso de divergência** — se o concurso trazido não for o previsto para a campanha, o sistema avisa **antes** de sortear. A regra vale sobre o número, e o número muda com o concurso. Desde a **2.27.0**, o aviso mostra os **cinco números premiados oficiais**, na ordem do sorteio, lado a lado com o que a campanha usaria, mais um link para a página de resultados da Caixa (que não tem endereço por concurso específico — por isso os números aparecem na própria tela).
- **Erro de consulta** — se a Caixa não responder, o sistema diz que não conseguiu consultar e pede o número manualmente (em vez de anunciar sucesso sem ter trazido nada).
- **Prazo de conferência** — havendo resultado apurado, a organização tem **5 dias corridos** para conferir; passado o prazo, o sistema finaliza sozinho. Essa finalização automática **só se aplica se o regulamento publicado daquela campanha declarar o prazo** — regulamento é texto congelado por versão, e ninguém pode ser submetido a uma regra que não estava no documento que leu.

![Configurações → Apuração](/assets/screenshots/bp-19-config-apuracao.png)

## Vários prêmios

Quando a campanha tem **mais de um prêmio** (1º, 2º, 3º…), a apuração produz **N contemplados distintos** sobre a **mesma base congelada**, sem repetir cartão — os prêmios saem em sequência a partir da mesma semente (no interno) ou repetindo a conta do resto da divisão, com o cartão já contemplado fora da base e a sequência dos números deslocada uma posição (na Loteria Federal). No método manual, você informa um cartão por prêmio. O resultado público, os relatórios e os e-mails passam a listar um ganhador por prêmio.

## Resultado imutável e público

Ao finalizar, o resultado **trava**. O(s) ganhador(es) aparece(m) na página pública com o cartão **mascarado** por padrão (protege os dados do contemplado). São disparados os e-mails de **resultado** (a todos) e de **ganhador** (um por contemplado). Reprocessar cria uma **nova versão** e exige o papel de Administrador do plugin — nada é apagado.

O passo a passo está em [Realizar o sorteio](/guias/realizar-sorteio/).

## Verificação pública (novo, 1.9.0)

No método **interno**, você pode publicar um painel **"Como conferir o sorteio"** na página da campanha (bloco/shortcode **Verificação do sorteio**). Antes da apuração, ele mostra o **lacre**; depois, revela a **semente** e o próprio navegador de quem visita **recalcula** e confirma que o cartão sorteado corresponde ao lacre — sem precisar confiar na sua palavra. É uma prova de idoneidade que fortalece a confiança na sua causa.

![Painel de verificação do sorteio](/assets/screenshots/bp-33-verificacao.png)

Como adicionar: veja [Blocos e Shortcodes](/modulos/blocos-shortcodes/) — o shortcode é `[rit360_premiado_verificacao id="ID"]`.

> ✅ **Boas práticas**
>
> Escolha e **descreva o método no regulamento** antes de abrir a campanha. Mudar a regra de apuração depois de vender cartões mina a confiança — e pode ter implicações legais.
