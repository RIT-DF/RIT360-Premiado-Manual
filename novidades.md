---
title: "Novidades"
nav_order: 8
permalink: /novidades/
source_docs: [CHANGELOG.md]
last_verified: 2026-08-09
status: publicado
---

# Novidades

O que há de novo no RIT360 Premiado, em linguagem simples. Cada item indica a **versão** do plugin em que a novidade chegou. Você vê a versão instalada no topo do painel, ao lado da logo (ex.: *RIT360 Premiado · v1.2.1*).

> Esta é uma versão amigável do histórico técnico. O registro completo para desenvolvedores fica no `CHANGELOG.md` do projeto.

---

## Versão 2.29 — Cada campanha com sua categoria no WooCommerce

**Prestação de contas:**

- **Toda campanha ganha uma categoria de produto no WooCommerce.** Ela entra como subcategoria dentro de "Campanhas premiadas" — você escolhe uma já existente ou cria uma nova ao montar a campanha, e se não escolher nada, o sistema usa o nome da campanha. Isso faz a receita chegar **já classificada por campanha** ao RIT360 Financeiro, em vez de cair sem categoria na prestação de contas segmentada.
- Campanhas que já existiam antes desta versão foram classificadas automaticamente — não é preciso voltar em nenhuma para corrigir. Veja [Criar a primeira campanha](/guias/criar-primeira-campanha/#categoria-campanha).

---

## Versão 2.28 — Avisos do plugin em lugar fixo

- **Os avisos do plugin (erros, confirmações, alertas) passaram a aparecer sempre no mesmo lugar**: logo abaixo do cabeçalho e acima da barra de abas. Antes, em algumas telas, um aviso podia aparecer encravado dentro do próprio cabeçalho — visualmente estranho, mas sem risco à informação.
- No card de resumo rápido da página pública, a frase de estimativa da data do sorteio (regra + data + ressalva) ficou mais compacta no celular: a data aparece em destaque, e a ressalva vem por baixo, menor.

---

## Versão 2.27 — O aviso de concurso divergente mostra os números oficiais

- **Quando o concurso trazido da Loteria Federal diverge do previsto para a campanha, o aviso passou a mostrar os cinco números premiados oficiais**, na ordem em que foram sorteados, lado a lado com o que a campanha usaria — mais um link para a página de resultados da Loteria Federal na Caixa (abre em nova aba). Antes, o aviso só dizia que os concursos divergiam, sem trazer o que conferir.
- **Uma ressalva honesta:** o portal da Caixa não tem endereço específico por concurso — é uma tela que busca o resultado por dentro. Por isso o link leva à página da modalidade, e a conferência de fato se faz pelos números exibidos na própria tela do plugin, não pelo link. Veja [Realizar o sorteio](/guias/realizar-sorteio/).

---

## Versão 2.26 — A data do sorteio da Loteria Federal deixou de ser um chute

**A mudança mais visível deste ciclo:** em campanhas de **Loteria Federal**, você não digita mais a data prevista do sorteio.

- **Agora você escolhe o concurso** — o 1º, 2º, 3º, 4º ou 5º concurso realizado **depois do encerramento das vendas**. Ninguém tem como adivinhar a data exata que a Caixa vai realizar o próximo concurso; o que faz sentido registrar é a regra, não uma data. O sistema calcula e mostra a data prevista, sempre rotulada como **estimativa, sujeita a alteração pela Caixa**.
- **O regulamento acompanha:** a cláusula de apuração passa a descrever o concurso escolhido por extenso, com a data prevista como conveniência, nunca como compromisso.
- **Métodos interna e manual continuam com data digitada**, exatamente como antes. Campanha de Loteria Federal criada antes desta versão também mantém a data que já tinha, até que alguém entre e escolha um concurso para ela.
- **Os e-mails pararam de cravar hora exata quando a data é estimativa.** Confirmação de compra, lembrete de sorteio, mudança de data e vendas encerradas passaram a trazer a regra do concurso, sem hora, evitando prometer uma precisão que não existe — e um e-mail já enviado não se corrige sozinho.

Veja [Criar a primeira campanha](/guias/criar-primeira-campanha/#concurso-loteria-federal) e [Configurar os e-mails](/guias/configurar-emails/).

---

## Versão 2.24 — Ajuste fino do regulamento, avisos que se comportam e transparência em qualquer tema

**Regulamento:**

- **Agora dá para ajustar o texto da apuração em uma campanha específica.** Antes, esse texto só podia ser mudado na biblioteca de cláusulas — e mexer lá afetava **todas** as campanhas de uma vez. Se uma rifa tem uma particularidade legítima, você personaliza só ela.
- **Quem não personaliza continua acompanhando a biblioteca**, inclusive quando ela é melhorada. Quem personaliza passa a ter texto próprio e deixa de receber essas melhorias — há um botão **Restaurar padrão** para voltar atrás quando quiser.
- **A descrição da apuração não pode ser apagada:** esvaziar o texto equivale a restaurar o padrão. É proteção, não limitação — nenhum regulamento deve ir ao ar sem dizer como o contemplado é escolhido. Veja [Personalizar o texto da apuração](/guias/publicar-regulamento/#personalizar-apuracao).

**O aviso de regulamento desatualizado ficou bem-educado:**

- **Ele some quando você republica.** Antes, o coordenador fazia exatamente o que o aviso pedia e ele continuava lá para sempre — o que ensina a ignorar avisos.
- **Ele só aparece nas telas do RIT360 Premiado.** Antes surgia em todo o WordPress: Posts, Mídia, Plugins, Usuários…

**Página pública:**

- **A seção Transparência funciona nos 6 temas.** Antes ela não era sequer oferecida em **Moderno (o padrão)**, Divertido e Simples: você marcava os indicadores, recebia confirmação, e o painel nunca aparecia. **Nesses três temas a seção nasce desligada** (para nenhuma campanha existente mudar de cara sozinha) — basta ligá-la em *Aparência da página*. E o admin agora **avisa** quando há indicadores marcados com a seção desligada. Veja [Painel de transparência](/guias/personalizar-pagina-publica/#painel-transparencia).

**Dois campos que saíram das telas:**

- A aba **Dados legais** não tem mais a caixa **"Apuração oficial pela Loteria Federal"**. Ela dava a entender que decidia o método de apuração, contradizendo a unificação feita na 2.22 — o método se define **só na aba Formulário**. Campanhas antigas não perdem nada.
- As **Configurações → Apuração** não têm mais a **"Regra de não-bate"**, que não tinha efeito nenhum desde a 2.21 (a apuração pela Loteria Federal sempre encontra um cartão).

---

## Versão 2.23 — O sorteio explicado por inteiro, e os campos que agora fazem o que prometem

A versão dedicada a uma pergunta simples: **o participante consegue conferir o resultado sozinho?**

**Regulamento (o mais importante):**

- Em campanhas de **Loteria Federal**, as cláusulas que descrevem a apuração passam a entrar **automaticamente** no regulamento: a regra explicada com um **exemplo numérico**, qual **concurso oficial** vale, como funciona com vários prêmios e o **prazo de conferência**. E **não dá mais para publicar sem elas**.
- Campanhas que publicaram o regulamento **antes** disso aparecem **sinalizadas com um aviso no painel**, sugerindo **republicar**. Como o regulamento é congelado por versão, ele não se corrige sozinho. Entenda o que fazer em [Publicar o regulamento](/guias/publicar-regulamento/#regulamento-apuracao-desatualizada).

**Apuração:**

- **Prazo de 5 dias corridos para conferir.** Havendo resultado apurado, a organização tem cinco dias para conferir e finalizar; passado o prazo, o sistema finaliza sozinho. **Só vale se o regulamento publicado daquela campanha declarar esse prazo** — ninguém pode ser submetido a uma regra que não estava no documento que leu.
- **Aviso de concurso divergente.** Se o resultado trazido da Loteria Federal não for o concurso previsto para a campanha, o sistema avisa **antes** de sortear.
- **Erro de consulta deixou de mentir.** Quando a consulta à Caixa falha, agora aparece uma mensagem pedindo para digitar o número à mão — antes a tela dizia "resultado buscado" mesmo sem ter trazido nada.
- **A busca automática do resultado passou a funcionar.** A opção existia em **Configurações → Apuração** e não fazia efeito nenhum; agora funciona de verdade (e a confirmação continua sendo sua). Tudo em [Realizar o sorteio](/guias/realizar-sorteio/).

**Campos que existiam na tela e não surtiam efeito — agora surtem:**

- **Organização:** o **favicon** vira o ícone da aba do navegador na página da campanha; o **texto institucional curto** e o **contato de dúvidas** aparecem na página pública. Veja [Configurar a organização](/guias/configurar-organizacao/).
- **Templates de cartão:** ganharam **quantidade recomendada**, **dica de uso** e **status Ativo/Inativo** — um template inativo deixa de ser oferecido ao criar campanha. Veja [Templates & Cartões](/modulos/templates-cartoes/).
- **Painel de transparência:** dois indicadores novos, **Participantes** e **Resultado do sorteio**. *(Nesta versão o painel ainda só aparecia em 3 dos 6 temas — corrigido na 2.24, veja acima.)*

**Correção de cartões:**

- Ao liberar um cartão ligado a um **pedido pago**, a confirmação agora mostra **o número do pedido e o e-mail do comprador** — você vê exatamente quem seria prejudicado antes de decidir. Veja [Corrigir cartões](/guias/corrigir-cartoes/).

---

## Versão 2.22 — Um lugar só para escolher o método de apuração

O **método de apuração** (Loteria Federal, apuração interna auditável ou registro manual) passou a ser definido **exclusivamente** na aba **Formulário** da campanha.

Antes existiam **dois seletores** — um no formulário e outro na aba Apuração — e eles podiam discordar entre si: a campanha ficava "certa" numa tela e "errada" na outra, o regulamento imprimia o método em branco e o número do cartão sumia para o comprador. Agora:

- A aba **Apuração** apenas **mostra** o método escolhido e indica onde alterá-lo.
- O campo é **obrigatório para publicar** a campanha.
- O mesmo valor governa o sorteio, o texto do regulamento e a exibição do número de sorteio ao comprador.

Veja [Realizar o sorteio](/guias/realizar-sorteio/) e [Criar a primeira campanha](/guias/criar-primeira-campanha/).

---

## Versão 2.21 — A apuração pela Loteria Federal ficou mesmo um sorteio

A regra antiga de apuração pela Loteria Federal **não distribuía a sorte por igual**: medindo o comportamento real, um único cartão chegava a concentrar a maior parte das chances numa rifa pequena. Isso foi corrigido.

A regra nova é fácil de conferir e não deixa margem para interpretação:

1. Os cartões **vendidos** entram em ordem — são **N** cartões.
2. Os **5 números** da extração oficial são **colados um no outro, na ordem em que saíram**, formando um número grande (**V**).
3. O **resto da divisão de V por N** aponta o cartão contemplado.

Numa planilha, a conta é `=MOD(V;N)+1`. Como o resto sempre cai dentro da lista, **o resultado sempre resolve** — acabaram a "regra de aproximação" e a configuração de dígitos. O **regulamento passou a descrever essa regra com um exemplo numérico**, para qualquer participante refazer a conta em casa.

---

## Versão 2.20 — As vendas param na hora certa (e alguém fica sabendo)

Uma correção importante para quem administra campanhas: **a data de fim das vendas passou a ser respeitada de fato**. Antes, o prazo era praticamente decorativo — a campanha podia continuar vendendo depois do fim do período.

- **A página pública avisa** que as vendas foram encerradas, informando **a data prevista do sorteio**.
- **A venda é barrada no momento da ação** (ao reservar e ao finalizar a compra), não só por um serviço em segundo plano que pode falhar. Quem reservou **dentro** do prazo continua conseguindo concluir dentro do tempo de reserva.
- **E-mail novo: "Vendas encerradas"**, enviado a **todos os coordenadores** da campanha assim que o período termina — com o resumo do que foi vendido, a data do sorteio e o **passo a passo do que fazer agora, conforme o método de apuração** daquela campanha. Veja [Configurar os e-mails](/guias/configurar-emails/).

---

## Versão 2.19 — Ninguém paga sem receber o cartão, e você conserta sozinho quando precisar

Duas frentes complementares: uma **evita** o problema, a outra dá a você a **saída** quando algo escapa.

**Para quem compra:**

- **O carrinho avisa quando a reserva expira.** Se o carrinho ficar parado além do tempo de reserva, aparece um aviso no próprio item — não mais uma surpresa depois do pagamento.
- **Ao finalizar, o sistema tenta garantir os mesmos cartões.** Se todos continuarem livres, a compra segue normalmente e você nem percebe. Se alguém já tiver escolhido algum, a compra é **interrompida antes de qualquer cobrança**, dizendo qual cartão se perdeu — é só voltar e escolher outro. Veja [Quando a reserva do cartão expira](/guias/reserva-expirada/).

**Para quem administra a campanha:**

- **Novo painel "Corrigir cartões"**, na tela da campanha. Busque um cartão pelo número ou pelo nome e veja o estado real dele — situação, reserva, pedido e histórico.
- **Vincule um cartão a um pedido pago** quando um comprador pagou e não recebeu — pela tela, sem depender de suporte técnico.
- **Libere um cartão preso** que não voltou para a venda sozinho.
- **Toda correção exige justificativa** e fica registrada com autor e data na [Trilha de auditoria](/modulos/auditoria/). Cartão vendido não tem ação por aqui, e depois do sorteio apurado a base de quem concorre fica protegida. Passo a passo em [Corrigir cartões](/guias/corrigir-cartoes/).

---

## Versão 2.18 — Compra de cartões sem confusão no carrinho

Ajustes no momento da compra, para o **comprador**:

- **Cartões de rifa são comprados separados de outros produtos.** Se você tiver outros produtos da loja no carrinho e tentar adicionar cartões — ou o contrário —, aparece um **aviso** pedindo para finalizar (ou esvaziar) a compra atual primeiro. Isso evita conflitos no checkout (entrega, conclusão do pedido e reservas dos cartões). **Cartões de campanhas diferentes continuam podendo ser comprados juntos**, no mesmo pedido.
- **O checkout não pede mais endereço de entrega.** Como o cartão é digital (não há nada para enviar pelo correio), o produto passou a ser **virtual**: a compra fica mais curta e o pedido se conclui sozinho após o pagamento.

---

## Versão 2.17 — E-mails com a cara da sua organização

Os e-mails que a campanha envia (confirmação de compra, resultado, lembrete etc.) ganharam um **visual próprio**, para não se confundirem com os e-mails padrão da loja:

- **Cabeçalho** com a **logo da sua organização** (ou o nome, se não houver logo) no topo, separada do texto por uma **linha fina na cor principal da OSC**.
- **Rodapé** com a **logo do RIT360** e o contato da organização.

É uma mudança **visual** — os textos e as variáveis dos e-mails continuam os mesmos. Não é preciso configurar nada: o novo layout vale automaticamente para todos os e-mails. Veja em [Configurar os e-mails](/guias/configurar-emails/).

---

## Versão 2.15 — Carrinho mais claro e o número do sorteio à mostra

Melhorias no que o **comprador** vê ao participar da campanha:

- **O carrinho mostra o que você está levando.** Cada cartão aparece pelo seu **nome** (e, nas campanhas apuradas pela **Loteria Federal**, com o **número de sorteio** ao lado), então dá para conferir exatamente quais cartões estão no pedido antes de pagar.
- **Quantidade travada, porque cada cartão é único.** Não existe "2x" o mesmo cartão: a quantidade de cada um fica **fixa em 1** no carrinho. Para desistir de um cartão, basta **removê-lo** — e ele **volta na hora** para o pool, liberando para outra pessoa.
- **Número de sorteio do começo ao fim.** Nas campanhas pela **Loteria Federal**, o número de sorteio de cada cartão agora aparece **em toda a jornada** — da **grade de escolha** ao **carrinho**, ao **e-mail**, ao painel **"Meus cartões"** e ao **resultado** — não só em alguns pontos. Veja em [Realizar o sorteio](/guias/realizar-sorteio/).

**Também nesta versão:**

- Na aba **Página pública** da campanha, o **termômetro de meta** ganhou a opção **"Exibir o termômetro só a partir de X%"** — você segura a barra fora do ar enquanto as vendas engatam e só a revela quando o progresso fica animador. Veja em [Personalizar a página pública](/guias/personalizar-pagina-publica/).
- A **vitrine de prêmios** da página pública passou a exibir os prêmios em **duas colunas**, com melhor aproveitamento do espaço.

---

## Versão 2.13 — Acessibilidade: tamanho do texto na página pública

A página pública de cada campanha agora tem um **controle de tamanho do texto** para quem visita: um box discreto no **canto superior direito do topo**, com os botões **A−**, **A** e **A+**.

- **A−** reduz, **A+** amplia e **A** volta ao padrão — quem enxerga menos ajusta a leitura sozinho.
- A preferência **fica guardada no navegador do visitante**: ao voltar, o tamanho escolhido é mantido.
- Aparece **automaticamente em todas as campanhas**, sem nenhuma configuração de sua parte.

Como fica para o público em [Personalizar a página pública](/guias/personalizar-pagina-publica/#acessibilidade--tamanho-do-texto).

---

## Versão 2.9 — Navegação por abas, mais direta

O painel do RIT360 Premiado ficou **mais fácil de navegar**. Em vez de vários submenus espalhados no menu lateral do WordPress, agora há **uma entrada única** ("RIT360 Premiado") e você troca de seção por uma **barra de abas** dentro da própria tela — Painel, Campanhas, Templates, Auditoria, Configurações e Shortcodes e API. Cada pessoa vê só as abas que pode acessar, e links antigos que você tenha salvo continuam funcionando.

---

## Versão 2.8 — Texto formatado nas observações

Dois campos de texto ganharam um **editor com formatação** (como um mini editor de texto): **Observações jurídicas** (aba Dados legais) e **Observações finais** (aba Prestação de contas). Agora dá para usar **negrito, itálico, listas e links**, e alternar entre os modos **Visual** e **Texto**. O que você formatar é salvo e, no caso das observações jurídicas exibidas na página pública, aparece formatado para o visitante.

---

## Versão 2.7 — Assistente de regulamento, de verdade

Montar o regulamento ficou um **passo a passo guiado**, e agora dá para **aproveitar as cláusulas prontas de verdade**:

- **Quatro etapas com barra de progresso.** *Dados da campanha* (entram sozinhos, você só confere) → *Cláusulas essenciais* → *Outras cláusulas* → *Revisão e publicação*. Dá para pular para qualquer etapa a qualquer momento.
- **“Inserir da biblioteca” — direto no campo.** Antes, as cláusulas da biblioteca eram só marcadas numa lista e você não conseguia editá-las. Agora, em cada campo há o botão **“+ Inserir da biblioteca”**: escolheu a cláusula, o **texto entra no campo pronto para você editar**.
- **Outras cláusulas em cartões.** Cláusulas gerais (LGPD, foro, destinação à causa…) e texto livre viram **cartões** que você adiciona, edita, **reordena** e remove — inclusive começando de um modelo da biblioteca ou de uma **cláusula em branco**.
- **Cada cláusula sabe onde entrar.** No **Banco de Cláusulas de Regulamento**, cada cláusula tem um **campo sugerido**, então “Inserir da biblioteca” já mostra as cláusulas certas para cada seção.
- **Texto que não muda pelas suas costas.** Ao inserir uma cláusula, o texto é **copiado e congelado** naquela campanha: mexer na biblioteca depois **não altera** os regulamentos já montados.

Passo a passo em [Publicar o regulamento](/guias/publicar-regulamento/).

---

## Versão 2.6 — Identidade visual da página pública, definida uma vez

A aparência das páginas públicas de campanha ficou **guiada por temas** e muito mais fácil de manter consistente com a sua marca:

- **Padrão da organização.** Uma aba nova, **Configurações → Identidade da página pública**, define como **todas** as campanhas nascem: o **tema** (galeria de 6 modelos — Sofisticado, Moderno, Clássico, Divertido, Emotivo, Simples — com **preview ao vivo já nas suas cores**), o **esquema de cores**, a **fonte** e as **seções** exibidas. Configure uma vez e não repita a cada campanha.
- **Claro, Escuro e Automático.** Você escolhe o esquema de cores da página. No **Automático**, a página segue o **aparelho de quem visita** — modo escuro no celular, página escura; modo claro, página clara.
- **Cores da marca na página inteira.** As cores da sua organização agora valem do topo ao rodapé (antes, só no topo), com o **contraste do texto garantido** para ficar sempre legível. A **logomarca aparece sempre sobre fundo branco**, para não sumir em nenhum esquema.
- **Herdar ou personalizar por campanha.** Na aba **Página pública** da campanha, um botão escolhe entre **Usar o padrão da organização** (herda tudo) ou **Personalizar esta campanha** (tema, esquema, fonte e seções só para aquela rifa).
- **Ligar e desligar seções.** Desmarcou uma seção, ela some da página. E seções sem conteúdo (um vídeo que você não cadastrou, por exemplo) são ocultadas sozinhas.

Passo a passo em [Personalizar a página pública](/guias/personalizar-pagina-publica/) e [Configurar a organização](/guias/configurar-organizacao/).

---

## Versão 2.5 — Lista de campanhas mais prática e fotos em lote

Dois ajustes que agilizam o dia a dia de quem gerencia várias campanhas:

- **Ações em ícones na lista de campanhas.** As ações de cada campanha viraram **ícones** com dica ao passar o mouse: **editar** (ou ver), **duplicar**, **excluir** e **arquivar**. Agora dá para **excluir campanhas em rascunho** (com confirmação) e **arquivar campanhas finalizadas** — elas saem da lista principal, e um checkbox **"Mostrar arquivadas"** as traz de volta quando você quiser. Veja em [Módulo Campanhas](/modulos/campanhas/).
- **Várias fotos do prêmio de uma vez.** Ao adicionar fotos do prêmio, a Biblioteca de Mídia agora aceita **selecionar várias imagens com clique simples** (sem Ctrl/Shift) e adicionar todas de uma vez em **Usar**. A primeira continua sendo a **principal**. Veja em [Criar a primeira campanha](/guias/criar-primeira-campanha/).

---

## Versão 2.4 — Conecte o plugin a outros sistemas (API e webhooks)

Agora dá para integrar o RIT360 Premiado a ferramentas como **n8n**, **Zapier**, planilhas e painéis:

- **API de leitura:** outros sistemas puxam dados das suas campanhas (vendas, cartões, resultado do sorteio, prestação de contas) usando uma **chave** que você gera.
- **Webhooks:** o plugin avisa um endereço seu automaticamente quando algo acontece (venda confirmada, sorteio concluído, campanha aberta/encerrada).
- **Privacidade em primeiro lugar:** por padrão, nada de dado pessoal cru — só números e dados mascarados. Para incluir nome/e-mail do comprador, há um escopo **opt-in** com aviso de responsabilidade (LGPD).

O menu **"Blocos e Shortcodes"** virou **"Shortcodes e API"**, com uma aba nova para gerenciar tudo isso. Passo a passo em [Integrar com outros sistemas](/guias/integrar-api-webhooks/).

**Também nesta versão:**

- O **regulamento** passou a exibir a **logo da organização** no topo (como já acontecia no relatório de prestação de contas e nos e-mails).
- As **redes sociais da organização** agora são uma **lista** (Instagram, Facebook, WhatsApp, YouTube…), cada uma com seu link — e podem **aparecer na página pública** da campanha, em ícones. Você escolhe a posição (rodapé, topo ou não exibir) em [Configurar a organização](/guias/configurar-organizacao/).
- A **criação de campanha** ficou mais didática: cada etapa traz uma explicação com **dicas e exemplos**, os campos principais têm sugestões, e a última etapa mostra um **resumo** e os **próximos passos** antes de você salvar. Veja em [Criar a primeira campanha](/guias/criar-primeira-campanha/).

---

## Versão 2.1 — Envie feedback direto do painel

Agora você fala com o suporte da RIT **sem sair do plugin**: o botão **💬 Feedback** no topo de todas as telas abre uma janela para enviar **problema, sugestão, elogio ou depoimento**.

- **Anexe** prints ou arquivos (png, jpg, pdf, zip) para ilustrar.
- Informe **seu e-mail** só se quiser retorno — é opcional.
- No **depoimento**, dá para incluir nome, organização e cargo, e autorizar a publicação.
- Apenas **dados técnicos do ambiente** acompanham a mensagem; **nenhum dado pessoal**.

O passo a passo está em [Enviar feedback](/guias/enviar-feedback/).

---

## Versão 1.13.0 — Loteria Federal para qualquer campanha

Agora dá para apurar pela **Loteria Federal** também as campanhas de **lista temática** (cartões que são nomes, não números).

- Cada cartão ganha um **número de sorteio** (a posição na lista, ex.: *Duna · 07*), que casa com o resultado oficial da Loteria Federal.
- Você ligava isso na aba **Dados legais** da campanha, em "Apuração oficial pela Loteria Federal". *(Mudou depois: desde a 2.22 o método se define na aba **Formulário**, e na 2.24 essa caixa foi removida.)* A partir daí o número aparece em todos os lugares onde o cartão é mostrado (grade de escolha, carrinho, e-mail, pedido, "Meus cartões" e resultado) — o participante sabe com que número concorre.
- Há também um sinalizador **"depende de autorização (SPA/MF)"**, que recomenda a Loteria e oferece uma **cláusula de regulamento** pronta.

Veja em [Realizar o sorteio](/guias/realizar-sorteio/).

---

## Versão 1.12.0 — Painel de gestão da campanha

Cada campanha ganhou um **Painel** — a primeira aba ao abrir a campanha — com a sua visão de gestão num relance:

- **Vendas** (vendidos, % da barra, reservados, disponíveis, pedidos), **Financeiro** (arrecadado, descontos, líquido, ticket médio), **Ritmo** (vendas dos últimos 7 dias, média por dia e uma **projeção de quando deve esgotar**) e **dias até o sorteio**.
- **Meta** e **conversão de reservas**; e, na fase de encerramento, um resumo das **pendências da prestação de contas**.
- Funciona bem no celular e não exige nenhuma configuração — está pronto em toda campanha.

Veja em [Painel da campanha](/guias/painel-da-campanha/).

---

## Versão 1.11.0 — Painel "Meus cartões" para o comprador

Agora o participante consulta **sem precisar de login** os cartões que comprou e o resultado do sorteio.

- Todo **e-mail de confirmação de compra** passa a trazer um link pessoal *"meus cartões"*. Quem perdeu o e-mail pode pedir o link de novo pelo formulário **"Receber o link por e-mail"** na própria página.
- O painel agrupa tudo **por campanha**: os **números** comprados, a **situação do pedido** e, depois do sorteio, o **resultado** — com destaque **"🎉 Você foi contemplado!"** e link para conferir a apuração.
- Sua organização publica esse painel no endereço pronto **`/meus-cartoes`**, ou embute em qualquer página pelo bloco/shortcode **Meus cartões**.
- Feito com privacidade em primeiro lugar: o link é pessoal e não adivinhável, e o formulário nunca revela se um e-mail comprou ou não.

Veja em [Painel "Meus cartões" do comprador](/guias/painel-meus-cartoes/).

---

## Versão 1.10.0 — Modelos radicais da página pública

Sua campanha ganha **6 modelos** de página que transformam de verdade o visual — não é só trocar a cor:

- **Moderno** (foco em conversão), **Sofisticado** (elegante, com a foto do prêmio no topo), **Clássico** (estilo jornal, duas colunas), **Emotivo** (a causa em primeiro plano, com contagem regressiva para o sorteio), **Divertido** (colorido e leve) e **Simples** (direto ao ponto).
- **As cores da sua organização** são aplicadas automaticamente sobre o modelo escolhido, e o sistema **ajusta o contraste** do texto para ficar sempre legível — inclusive colocando a sua logo numa moldura clara para não sumir no fundo.
- O seletor de modelos agora mostra uma **miniatura** de cada um (clique para ampliar), em **Editar campanha → Página pública → Template visual**.
- Novos elementos de engajamento: **contagem regressiva** até o sorteio e um resumo em **cards de fatos** (data, valor do cartão, prêmio, vendidos).

Veja em [Personalizar a página pública](/guias/personalizar-pagina-publica/).

---

## Versão 1.9.0 — Página pública mais envolvente e transparente

Quatro novidades para engajar quem visita a campanha e provar a lisura do sorteio. Cada uma funciona como **bloco** (Gutenberg) e como **shortcode**.

- **Termômetro de meta.** Defina uma meta de **cartões** e/ou de **arrecadação (R$)** e a página passa a exibir um termômetro com o progresso e um aviso de **meta atingida**. Configure na aba **Página pública** da campanha. (A meta em R$ só aparece se você não estiver ocultando os valores financeiros.)
- **Verificação pública do sorteio.** Um painel "Como conferir o sorteio" que qualquer pessoa pode usar para confirmar, no próprio navegador, que o resultado é honesto: o **lacre** é publicado antes, a **semente** é revelada depois, e o cálculo é refeito na hora. Um diferencial de confiança para a sua causa.
- **Vídeos de divulgação.** Cole um link do **YouTube** ou do **Vimeo** e o vídeo aparece embutido na página da campanha. Também dá para anexar um **link de vídeo** como evidência na prestação de contas.
- **Vitrine de campanhas.** Um endereço único (**`/campanhas`**) que lista todas as suas campanhas ativas em cards — ótimo para divulgar tudo de uma vez. Também embutível em qualquer página do seu site pelo bloco/shortcode **Vitrine**.

Veja como usar em [Personalizar a página pública](/guias/personalizar-pagina-publica/) e [Blocos e Shortcodes](/modulos/blocos-shortcodes/).

> **Correção 1.9.1** — ajuste para a **vitrine** carregar corretamente também quando o site usa o formato de links "Padrão" do WordPress.

---

## Versão 1.8.0 — Privacidade, minimização de dados e organização das telas

- **Ferramentas de privacidade (LGPD).** O plugin agora conversa com as ferramentas nativas do WordPress em **Ferramentas → Exportar dados pessoais** e **Apagar dados pessoais**: ao atender a um pedido de um titular por e-mail, o sistema **exporta** o consentimento de comunicações e a situação de contemplado, e **apaga** o consentimento quando solicitado. Os **documentos pessoais do contemplado são mantidos** por obrigação legal de prestação de contas do sorteio. (Os dados de compra ficam a cargo do WooCommerce.)
- **Menos dados guardados.** O campo de **dados bancários** da organização foi **removido** — não era usado em nenhum documento e guardar dado sensível sem necessidade é um risco desnecessário. Ele volta no futuro, junto da funcionalidade de recibos/repasse.
- **Aba renomeada e mais clara.** A antiga aba "Bancário e contato" virou **"Configurações Globais da Campanha"**, reunindo o contato de dúvidas e os padrões de reserva. O campo técnico "TTL" agora se chama **"Tempo de reserva do cartão (minutos)"**, com explicação.
- **Menu mais organizado.** No menu do plugin, **Configurações** passou para depois de **Auditoria**; e a aba **Usuários** ficou logo após **Identidade visual**.

## Versão 1.7.0 — Convide sua equipe e defina papéis

- **Nova aba Usuários, em Configurações.** Agora dá para **atribuir papéis pela tela**, sem depender de configuração técnica. O Administrador da organização abre **Configurações → Usuários**, encontra a pessoa (busca por nome, login ou e-mail) e marca o que ela pode fazer: **Administrador da campanha**, **Auditor** e/ou **Operador**. A alteração é salva na hora e fica registrada na auditoria. Veja [Gerenciar usuários e papéis](/guias/gerenciar-usuarios/).
- **Uma pessoa pode ter mais de um papel.** Os acessos se somam — útil para quem, por exemplo, opera as vendas e também acompanha as contas.
- **Responsáveis pela campanha mais fáceis de achar.** No formulário da campanha, a escolha dos responsáveis subiu para o **topo** da aba **Configurações**. E, com os papéis agora atribuíveis pela tela, a lista de responsáveis deixa de aparecer vazia.

## Versão 1.6.0 — Vários prêmios na mesma campanha

- **1º, 2º, 3º lugar na mesma rifa.** Agora uma campanha pode ter **mais de um prêmio**. Na etapa **Dados do Prêmio**, use **+ Adicionar prêmio** para incluir cada um na ordem em que serão sorteados. Todos são sorteados **da mesma base de cartões vendidos, sem repetir número** — cada prêmio vai para um cartão diferente. O regulamento lista todos os prêmios, o resultado público e os e-mails mostram um ganhador por prêmio, e a prestação de contas soma os custos de todos. Quem quiser um prêmio só não muda nada. Veja [Criar a primeira campanha](/guias/criar-primeira-campanha/) e [Realizar o sorteio](/guias/realizar-sorteio/).

## Versão 1.5.0 — Blocos e shortcodes para montar sua página

- **Monte a página da campanha no seu construtor.** Agora você pode compor a página da campanha no editor de blocos do WordPress (Gutenberg) ou em construtores como o Elementor, usando **8 componentes** prontos: seleção de cartões, painel de transparência, barra de progresso, resultado do sorteio, botão comprar, compartilhamento, regulamento e a rifa completa. Cada um funciona como **bloco** (categoria “RIT360 Premiado”) e como **shortcode**. Veja [Montar a página no construtor](/guias/montar-pagina-construtor/) e [Blocos e Shortcodes](/modulos/blocos-shortcodes/).
- **Nova página de referência.** No menu do plugin, a página **Blocos e Shortcodes** lista todos os componentes com exemplos prontos para copiar.

## Versão 1.4.1 — Correção na tela de Auditoria

- **Tabela de auditoria visível no computador.** Corrigido um problema em que a lista de auditoria não aparecia no desktop.

## Versão 1.4.0 — Mais proteção contra abusos

- **Reservas ainda mais protegidas.** Novas barreiras de segurança nas reservas públicas (limite por campanha e um desafio automático sob picos de acesso) reforçam a proteção contra uso abusivo — sem atrapalhar quem participa de verdade.

## Versão 1.3.0 — Trilha de auditoria consultável

- **Nova tela de Auditoria.** O plugin já registrava as ações sensíveis nos bastidores; agora há uma **tela de consulta** para elas: filtre por ação, tipo, origem, usuário e período, expanda cada registro e exporte em CSV. Ideal para o conselho fiscal e para a prestação de contas. Veja [Auditoria](/modulos/auditoria/).

## Versão 1.2.2 — Ajuste técnico

- Correção interna no carregamento do plugin (empacotamento), sem mudança visível no uso.

## Versão 1.2.1 — Mais segurança

- **Reservas públicas mais protegidas.** A página pública ficou mais resistente a abusos: há um limite de cartões que um mesmo visitante pode manter reservados ao mesmo tempo, evitando que alguém "trave" a rifa sem comprar.
- **Descadastro de e-mail à prova de engano.** O link de descadastro passou a pedir uma confirmação, para que verificadores automáticos de link (comuns em provedores de e-mail) não descadastrem ninguém por engano.
- **Confirmação de compra sem duplicidade.** Ajustes internos garantem que o e-mail de confirmação de compra não seja enviado duas vezes, mesmo se o pagamento notificar o sistema mais de uma vez.

## Versão 1.2.0 — Painel geral e apoio à RIT

- **Novo Painel com indicadores.** A tela inicial agora traz uma visão geral: valor apurado, resultado líquido, ranking de campanhas, ticket médio, próximos sorteios com contagem regressiva e um filtro de período. Tudo em números agregados, sem expor dados pessoais. Veja [Painel](/modulos/painel/).
- **Doação voluntária à RIT.** Um recurso opcional para destinar parte da margem ao projeto que mantém o plugin — com valor sugerido e registro das doações feitas. Totalmente opcional. Veja [Apoiar a RIT](/guias/apoiar-a-rit/).

## Versão 1.1.0 — Listas de cartões prontas

- **9 listas temáticas embarcadas.** Para você não precisar montar tudo do zero, o plugin passou a vir com listas prontas de cartões: Animais do Brasil, Artistas, Cidades do Brasil, Clássicos da literatura, Especialidades escoteiras, Ficção científica, Heróis dos quadrinhos, Músicas K-pop e Pessoas históricas. Veja [Montar os cartões](/guias/montar-cartoes/).

## Versão 1.0.0 — Primeira versão completa

A primeira versão formal do RIT360 Premiado, reunindo todo o ciclo de uma campanha premiada:

- **Configurações da organização** como fonte única de dados institucionais.
- **Campanhas** de ponta a ponta, com produto oculto no WooCommerce e formulário em etapas.
- **Templates e cartões** (números ou listas), com reserva anti-duplicidade.
- **Regulamento obrigatório e semi-automático**, versionado e carimbado.
- **Página pública mobile-first** com 5 templates visuais, transparência e compartilhamento.
- **Checkout, pedidos e descontos** integrados ao WooCommerce.
- **E-mails automáticos** e consentimento conforme a LGPD.
- **Apuração auditável** (interno reproduzível, Loteria Federal ou manual) e resultado público.
- **Prestação de contas** com checklist e relatórios em CSV, PDF e JSON.

---

Quer detalhes de como usar cada novidade? Comece pelos [Guias por tarefa](/guias/) ou explore os [Módulos](/modulos/).
