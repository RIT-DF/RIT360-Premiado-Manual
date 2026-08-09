---
title: "Realizar o sorteio"
nav_order: 8
parent: "Guias por tarefa"
permalink: /guias/realizar-sorteio/
task: realizar-sorteio
role: admin
routes: ["#/campanhas/:id", "#/organizacao"]
screenshots: [bp-05-campanha-config, bp-21-apuracao, apuracao-loteria-busca, apuracao-aviso-divergencia, bp-19-config-apuracao]
source_docs: [PRD_Bussola_Premiada.md#8.14, PRD_Bussola_Premiada.md#8.15, "#186", "#182", "#185"]
last_verified: 2026-08-09
status: publicado
---

# Realizar o sorteio

Chegou a data. O RIT360 Premiado faz a apuração de forma **auditável** — de um jeito que qualquer pessoa possa confiar no resultado. Você escolhe entre três métodos.

## Antes de tudo: onde o método é definido

> **Mudou na versão 2.22.0.** O método de apuração agora é definido em **um lugar só**: a aba **Formulário** da campanha (etapa *Configurações da Campanha*), no campo **Método de apuração**. Antes existiam dois seletores — um no formulário e outro na aba Apuração — e eles podiam discordar entre si.

O que você escolhe ali governa **tudo**: como o sorteio é feito, o que o regulamento diz sobre a apuração e se o comprador vê o **número de sorteio** do cartão. O campo é **obrigatório para publicar** a campanha.

![Campo Método de apuração na aba Formulário](/assets/screenshots/bp-05-campanha-config.png)

As três opções são:

- **Loteria Federal** — o resultado é definido pela extração oficial da Loteria Federal. É o método mais reconhecido pelo público e o que atende ao rito legal dos sorteios autorizados.
- **Apuração interna auditável** — o plugin sorteia usando uma semente secreta lacrada no congelamento. Ao finalizar, a semente é revelada e **qualquer pessoa pode refazer a conta** e chegar ao mesmo cartão. Autonomia total, sem depender de terceiros.
- **Registro manual** — para sorteios feitos fora do sistema (uma live, um evento). Você registra o resultado com **justificativa e anexos**.

Ao escolher **Loteria Federal**, cada cartão passa a ter um **número de sorteio** (a posição dele na lista) exibido para o participante em todos os lugares — na grade de escolha, no carrinho, no e-mail de confirmação, no pedido, no painel "Meus cartões" e no resultado. É esse número que casa com a extração oficial.

> 💡 **E a aba Dados legais?**
>
> Ela **não escolhe mais o método**. Até a versão 2.23 havia lá uma caixa "Apuração oficial pela Loteria Federal" que dava a entender o contrário; **na 2.24.0 ela foi removida**, para não haver dois lugares dizendo coisas diferentes. O método se define **só na aba Formulário**. Campanhas antigas não perdem nada — o valor antigo continua sendo respeitado nos bastidores.
>
> O que continua na aba Dados legais é o bloco **Autorização de sorteio (SPA/MF)**, com a opção **"Esta campanha depende de autorização de sorteio (SPA/MF)"**. Marcando-a, o plugin **recomenda** o método Loteria Federal — é o que atende ao rito legal dos sorteios autorizados — e disponibiliza uma cláusula de regulamento pronta sobre o assunto. Isto é apoio ao processo: a necessidade da autorização e a conferência do regulamento com um advogado continuam sendo responsabilidade da organização.

## Onde se apura

Abra a campanha e clique na aba de topo **Apuração**.

![Aba Apuração](/assets/screenshots/bp-21-apuracao.png)

No topo dessa aba há um campo **Método** que apenas **mostra** o que foi escolhido, com o lembrete de que a alteração se faz na aba Formulário. Não há mais seletor aqui — se o método estiver errado, volte ao formulário e corrija lá.

## Passo 1 — Congelar a base

Antes de sortear, você **congela** a lista de cartões vendidos. A partir daí:

- A base não muda mais — ninguém entra ou sai.
- Reembolsos e cancelamentos **não** devolvem mais o cartão ao pool (ficam registrados e auditados).
- Na apuração interna, é publicado um **lacre** (um código `sha256` da semente do sorteio), provando que a semente foi definida **antes** do resultado.

## Passo 2 — Obter o resultado

### Se o método for Loteria Federal

A regra é simples de conferir e não deixa margem para interpretação:

1. Os cartões **vendidos** são colocados em ordem — são **N** cartões.
2. Os **5 números** sorteados na extração oficial são **colados um no outro, na ordem em que saíram**, formando um número grande (**V**).
3. O **resto da divisão de V por N** aponta a posição do cartão contemplado na lista.

Quem quiser conferir em casa consegue: numa planilha, a conta é `=MOD(V;N)+1`. Como o resto da divisão sempre cai dentro da lista, **o resultado sempre resolve** — não existe mais "regra de aproximação" nem configuração de dígitos a extrair. (Em campanhas com **vários prêmios**, o processo se repete: o cartão já contemplado sai da base e a sequência dos números avança uma posição.)

Na aba Apuração, depois de congelar a base, aparecem cinco campos — **1º a 5º prêmio** — na ordem do sorteio. Clique em **Buscar resultado** para o sistema trazer a extração oficial e preencher os cinco, ou digite os números à mão a partir do resultado publicado pela Caixa. Depois é só **Sortear**. Duas coisas que o sistema faz por você:

- **Se o concurso trazido não for o esperado para esta campanha**, aparece um **aviso de divergência** antes de qualquer sorteio, comparando o concurso que veio com o que era previsto. Confira antes de prosseguir — a regra vale sobre o número, e o número muda com o concurso.

  ![Aviso de concurso divergente na aba Apuração](/assets/screenshots/apuracao-aviso-divergencia.png)

- **Se a consulta à Caixa falhar**, aparece uma **mensagem de erro** pedindo que você digite os números manualmente. (Até a versão 2.22.0 a tela dizia que o resultado tinha sido buscado mesmo quando nada tinha vindo — esse é justamente o defeito corrigido.)

![Campos dos 5 prêmios e o botão Buscar resultado, na aba Apuração](/assets/screenshots/apuracao-loteria-busca.png)

### Se o método for interno ou manual

No **interno**, o próprio plugin sorteia sobre a base congelada. No **manual**, você informa o cartão contemplado (um por prêmio, se houver vários) com justificativa e anexos.

## Passo 3 — Finalizar e publicar

Ao finalizar, o resultado é **travado** (imutável). O(s) contemplado(s) é(são) definido(s) e:

- O **resultado público** aparece na página da campanha, com o cartão ganhador **mascarado** por padrão (protege os dados pessoais do ganhador).
- São enviados os e-mails de **resultado** (a todos) e de **ganhador** (ao contemplado).

### Campanha com vários prêmios

Se a campanha tem **mais de um prêmio**, a apuração sorteia **todos de uma vez**, sobre a mesma base congelada, **sem repetir cartão** — o 1º, o 2º, o 3º… saem em sequência. A aba Apuração mostra a lista dos contemplados por prêmio, e cada ganhador recebe seu e-mail. Nos métodos **interno** e **Loteria Federal** o plugin resolve os N contemplados automaticamente; no **manual**, você informa um cartão para cada prêmio.

## O prazo de 5 dias para conferir
{: #prazo-conferencia }

> **Novidade da versão 2.23.0.** Assim que existe um resultado apurado da Loteria Federal, você tem **5 dias corridos** para conferir e finalizar. Se ninguém agir nesse prazo, **o sistema finaliza sozinho** — a aba Apuração mostra a data e a hora limite.

Isso evita que uma campanha fique parada indefinidamente esperando alguém clicar. Mas há uma condição importante, e ela é deliberada:

> ⚠️ **A validação automática só vale se o regulamento publicado daquela campanha declarar esse prazo.**
>
> O regulamento é um texto **congelado por versão**: o participante leu o que estava publicado quando comprou. Uma campanha cujo regulamento foi publicado **antes** da cláusula do prazo **não** é finalizada automaticamente — ela continua esperando você. Se quiser a automação nessas campanhas, é preciso **republicar o regulamento** (aba Regulamento), o que gera uma nova versão com a cláusula. Se preferir conferir tudo à mão, não faça nada: o comportamento antigo continua.

## Busca automática do resultado
{: #busca-automatica }

Nas **Configurações → Apuração** existe a opção **"Buscar automaticamente o resultado da Loteria Federal"**. Com ela ligada, o sistema tenta trazer o resultado sozinho assim que a campanha estiver pronta para apurar, sem você precisar clicar em *Buscar resultado* — ele **pré-preenche**, e quem confirma continua sendo você.

![Configurações → Apuração](/assets/screenshots/bp-19-config-apuracao.png)

> Até a versão 2.22.0 essa opção existia na tela mas **não fazia nada**. A partir da 2.23.0 ela funciona de verdade. Em qualquer caso — busca manual ou automática — vale o prazo de 5 dias descrito acima.

> ⚠️ **Atenção**
>
> Reprocessar um resultado já finalizado cria uma **nova versão** e exige o papel de **Administrador do plugin**. O resultado anterior não é apagado — fica registrado como substituído. Isso preserva a trilha de auditoria.

> ✅ **Boas práticas**
>
> Se a sua modalidade permite, o sorteio pela **Loteria Federal** é o método mais reconhecido e transparente para o público. A **apuração interna auditável** é uma excelente alternativa quando você quer autonomia mantendo a prova. Em qualquer caso, escolha o método **antes** de abrir a campanha e confira que o [regulamento](/guias/publicar-regulamento/) descreve exatamente o que será feito.
