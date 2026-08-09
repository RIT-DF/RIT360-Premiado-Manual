---
title: "Publicar o regulamento"
nav_order: 4
parent: "Guias por tarefa"
permalink: /guias/publicar-regulamento/
task: publicar-regulamento
role: admin
routes: ["#/campanhas/:id"]
screenshots: [reg-assistente-etapas, reg-outras-clausulas, reg-ordenar-clausulas, reg-banco-clausulas-target, bp-09-dados-legais, admin-aviso-republicar-regulamento]
source_docs: [PRD_Bussola_Premiada.md#8.10, PRD_Bussola_Premiada.md#8.11]
last_verified: 2026-08-09
status: publicado
---

# Publicar o regulamento

O regulamento é **obrigatório**: nenhuma campanha entra no ar sem um regulamento publicado. A boa notícia é que o RIT360 Premiado monta a maior parte dele para você — a partir dos dados da organização, dos dados da campanha e de uma biblioteca de cláusulas prontas.

> **A partir da versão 2.7.0**, a aba Regulamento virou um **assistente guiado em etapas**: você segue um passo a passo, e pode **puxar uma cláusula pronta da biblioteca direto para dentro do campo** para editá-la. A logo da organização (a mesma cadastrada em [Configurar a organização](/guias/configurar-organizacao/)) continua aparecendo no topo do documento.

## Onde fica

Abra a campanha e clique na aba de topo **Regulamento**. No topo há uma **barra de progresso** com as cinco etapas do assistente.

![Assistente de regulamento em etapas](/assets/screenshots/reg-assistente-etapas.png)

## As cinco etapas

1. **Dados da campanha** — dados da organização e da campanha (nome, CNPJ, prêmio, datas, quantidade, valor) entram **sozinhos**; você só confere. Ajuste-os, se preciso, na campanha e em **Organização**.
2. **Cláusulas essenciais** — as seções principais (critérios de participação, política de entrega etc.). Em cada campo há o botão **“+ Inserir da biblioteca”**: clique para trazer um **texto-modelo pronto** e então edite à vontade. Os campos com **\*** são obrigatórios.
3. **Outras cláusulas** — cláusulas gerais (LGPD, foro, destinação à causa…) e qualquer texto livre, em forma de **cartões** que você adiciona, edita e remove. Use **“+ Inserir da biblioteca”** para começar de um modelo, ou **“+ Cláusula em branco”** para escrever do zero.
4. **Ordenar cláusulas** — defina a **sequência** em que as cláusulas aparecem no documento final. Aqui as **essenciais e as outras aparecem juntas, numa lista só**, e você as reordena com as setas **↑ ↓**. As cláusulas de **Objeto** e **Apuração** ficam fixas no início.
5. **Revisão** — pré-visualização fiel ao que o público verá + o botão **Publicar**.

![Etapa Outras cláusulas, com cartões editáveis](/assets/screenshots/reg-outras-clausulas.png)

## Passo a passo

1. Na etapa **Cláusulas essenciais**, preencha cada seção. Para ir mais rápido, clique em **“+ Inserir da biblioteca”** no campo e escolha uma cláusula-modelo — o texto entra no campo **pronto para editar**.
2. Em **Outras cláusulas**, adicione as cláusulas gerais que se aplicam (também via “Inserir da biblioteca”) e **remova** o que não usar.
3. Na etapa **Ordenar cláusulas**, arraste a ordem com as setas **↑ ↓** até o documento ficar na sequência que você quer. Essenciais e outras cláusulas são ordenadas na mesma lista.

   ![Etapa Ordenar cláusulas, com essenciais e outras na mesma lista](/assets/screenshots/reg-ordenar-clausulas.png)
4. Na etapa **Revisão**, use a **pré-visualização** para conferir o texto final. Clique em **Salvar rascunho** quando quiser continuar depois.
5. Clique em **Publicar regulamento** e confirme.

> 💡 **Como as cláusulas sabem onde entrar**
>
> Cada cláusula da biblioteca tem um **campo sugerido**. Você define isso em **Configurações → Banco de Cláusulas de Regulamento**, no seletor **“Sugerir no campo”** de cada cláusula. É por isso que, ao clicar “Inserir da biblioteca” num campo, aparecem só as cláusulas daquele tema.
>
> ![Seletor de campo sugerido no Banco de Cláusulas](/assets/screenshots/reg-banco-clausulas-target.png)
>
> Ao inserir uma cláusula, o texto é **copiado** para a campanha e fica **congelado** ali: editar a biblioteca depois **não altera** os regulamentos já montados.

## Campanhas de Loteria Federal: as cláusulas de apuração entram sozinhas

> **Novidade da versão 2.23.0.** Se o **método de apuração** da campanha for **Loteria Federal**, o assistente já traz, prontas, as cláusulas que descrevem como o ganhador será encontrado. Você não precisa escrevê-las — e **não consegue publicar sem elas**.

São quatro cláusulas, na seção **Apuração** do documento:

- **Apuração pela Loteria Federal** — a regra explicada passo a passo, com a fórmula de conferência e um **exemplo numérico completo**, para qualquer participante refazer a conta.
- **Campanhas com mais de um prêmio** — como o sorteio se repete para o 2º, o 3º prêmio…
- **Concurso oficial utilizado** — qual extração vale (a primeira depois do fim das vendas), com o número previsto do concurso.
- **Conferência e divulgação do resultado** — o prazo de **5 (cinco) dias corridos** para a organização conferir e divulgar, e a validação automática pelo sistema depois disso.

Se você tentar publicar um regulamento de campanha Loteria Federal sem a descrição da apuração, o plugin **barra a publicação** e avisa o que falta. Isso existe porque, até a versão 2.22.0, o texto padrão remetia a regras que nunca chegavam a ser descritas no documento — o participante lia uma promessa vazia.

### "Este regulamento está com a apuração desatualizada"
{: #regulamento-apuracao-desatualizada }

Campanhas cujo regulamento foi publicado **antes** dessa mudança aparecem **sinalizadas com um aviso no painel do WordPress**, listando os nomes das campanhas afetadas.

![Aviso no painel do WordPress listando as campanhas a republicar](/assets/screenshots/admin-aviso-republicar-regulamento.png)

**O que fazer:** o texto publicado é **congelado por versão** e não se corrige sozinho. Abra a campanha, vá na aba **Regulamento** e **republique** — o plugin gera uma nova versão já com as cláusulas completas, e a anterior fica arquivada no histórico.

**É urgente?** Não é bloqueante: a campanha continua funcionando normalmente. Mas há uma consequência prática — enquanto o regulamento publicado não declarar o prazo de 5 dias, aquela campanha **não** é finalizada automaticamente pelo sistema (veja [Realizar o sorteio](/guias/realizar-sorteio/#prazo-conferencia)). Se a campanha já vendeu cartões, avalie republicar com calma: o regulamento é o documento que os participantes leram.

## O que acontece ao publicar

- O plugin tira um **snapshot** dos dados da organização — o regulamento fica "carimbado" com o que valia naquele momento.
- A primeira publicação vira a **versão 1**. Se você editar depois de publicado, uma nova versão (v2, v3…) é criada e a anterior é arquivada. Assim há **histórico** de tudo.
- O item "regulamento publicado" do checklist da campanha é atendido, liberando a abertura.

## Dados legais

Na aba **Dados legais** você registra número de autorização, processo e observações. São **opcionais**, mas se estiverem em branco o plugin **pede confirmação explícita** antes de publicar a campanha — um lembrete para você não esquecer.

![Aba Dados legais](/assets/screenshots/bp-09-dados-legais.png)

> ✅ **Boas práticas**
>
> Leia o regulamento inteiro na pré-visualização antes de publicar, como se fosse um participante. Ele é o documento que dá segurança jurídica à campanha e transmite seriedade ao público. Veja também [Requisitos legais de um sorteio](/boas-praticas/requisitos-legais/).

> 💡 **Dica**
>
> Se você duplicar uma campanha, o regulamento é copiado junto — ótimo para campanhas recorrentes que seguem o mesmo modelo.
