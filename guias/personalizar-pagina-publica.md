---
title: "Personalizar a página pública"
nav_order: 5
parent: "Guias por tarefa"
permalink: /guias/personalizar-pagina-publica/
task: personalizar-pagina-publica
role: admin
routes: ["#/organizacao", "#/campanhas/:id", "/campanha/:slug"]
screenshots: [tema-01-org-identidade, tema-02-campanha-padrao-personalizar, publica-hero-modos, tema-03-publica-clara, tema-04-publica-escura, publica-tamanho-texto, bp-29-config-meta-video, bp-30-publica-termometro, bp-31-publica-video, publica-transparencia, publica-transparencia-secoes, publica-vendas-encerradas]
source_docs: [PRD_Bussola_Premiada.md#8.7, PRD_Bussola_Premiada.md#8.8, PRD_Bussola_Premiada.md#8.9, CHANGELOG.md#2.6.0, CHANGELOG.md#2.13.0, CHANGELOG.md#2.13.2]
last_verified: 2026-08-09
status: publicado
---

# Personalizar a página pública

Cada campanha ganha uma **página pública própria** (um hotsite), com endereço em `/campanha/nome-da-campanha`. É mobile-first, pronta para compartilhar e é onde as pessoas veem o prêmio, leem o regulamento, escolhem os cartões e compram.

A partir da **versão 2.6.0**, a aparência dessa página é **guiada por temas** e funciona em **dois níveis**:

1. **O padrão da sua organização** — você define uma vez, em Configurações, e ele vale para **todas** as campanhas novas.
2. **A personalização de cada campanha** — se uma rifa específica pedir um visual diferente, você sobrescreve o padrão só para ela.

Assim você configura a marca uma vez e não repete a cada campanha — mas continua livre para ajustar caso a caso.

## 1. Definir o padrão da organização

No menu **RIT360 Premiado → Configurações**, abra a aba **Identidade da página pública**. Aqui você escolhe como as páginas públicas vão nascer por padrão.

![Aba Identidade da página pública (padrão da organização)](/assets/screenshots/tema-01-org-identidade.png)

### Tema (a galeria de modelos)

O **tema** define a composição e o estilo da página inteira — não é só a cor. Você escolhe entre **6 temas**, cada um com uma **miniatura de preview ao vivo já nas cores da sua organização**:

- **Sofisticado** — elegante e institucional, transmite alto valor.
- **Moderno** — limpo e digital, com foco em conversão.
- **Clássico** — sóbrio e tradicional, com leitura de jornal.
- **Divertido** — lúdico e acolhedor, com cor e energia.
- **Emotivo** — foco na causa, nas histórias e no impacto.
- **Simples** — direto ao ponto: prêmio, preço e comprar.

Clique na miniatura do tema que combina com a sua campanha para selecioná-lo.

> 💡 As **cores da sua organização** (primária, secundária e destaque, definidas na aba **Identidade visual**) agora valem na **página inteira** — não só no topo. Os previews da galeria já mostram como cada tema fica com as suas cores aplicadas, e o contraste do texto é ajustado automaticamente para ficar sempre legível.

### Esquema de cores (claro / escuro / automático)

O **esquema** controla o fundo geral da página:

- **Claro** — fundo claro, texto escuro.
- **Escuro** — fundo escuro, texto claro.
- **Automático** — a página segue o **aparelho de quem visita**: quem está com o celular no modo escuro vê a versão escura; quem está no modo claro vê a clara. É a opção mais confortável para o público, porque respeita a preferência de cada pessoa.

### Fonte

A **tipografia** dá o tom do texto:

- **Moderna** (sem serifa) — mais clean e atual.
- **Clássica** (com serifa) — mais editorial e tradicional.
- **Arredondada** — mais leve e amigável.

### Seções exibidas por padrão

Ligue ou desligue as seções que aparecem na página: **Topo (destaque)**, **Barra de progresso**, **A causa**, **Transparência**, **Redes sociais**, **Resultado do sorteio**, **Vitrine do prêmio**, **Resumo rápido**, **Vídeo**, **Regulamento**, **Compartilhar** e **Painel do comprador**.

**Desligar uma seção faz ela sumir da página.** Além disso, seções **sem conteúdo** são ocultadas sozinhas — se você não cadastrou um vídeo, por exemplo, a seção de vídeo não aparece mesmo que esteja marcada.

Ao terminar, clique em **Salvar identidade da página**. Pronto: toda campanha nova nasce com esse padrão.

## 2. Personalizar uma campanha específica

Abra a campanha e clique na aba de topo **Página pública**. Logo no início, em **Aparência da página**, você escolhe entre duas opções:

![Aparência da página na campanha: usar o padrão ou personalizar](/assets/screenshots/tema-02-campanha-padrao-personalizar.png)

- **Usar o padrão da organização** — a campanha **herda tudo** o que você definiu em Configurações (tema, esquema, fonte e seções). É o recomendado na maioria dos casos: mude o padrão uma vez e todas as campanhas acompanham.
- **Personalizar esta campanha** — abre os mesmos controles (galeria de temas, esquema, fonte e seções), mas as escolhas valem **só para aquela rifa**. Use quando uma campanha específica precisa de um visual próprio, sem mexer no padrão das demais.

O restante da aba (topo/hero, transparência, meta/termômetro, vídeo, compartilhamento) continua sempre disponível, independentemente da opção escolhida.

### Posição da logo e da causa

Ainda em **Aparência da página**, dois seletores controlam **onde** dois elementos-chave aparecem:

- **Logomarca da organização** — escolha entre **Padrão (topo)**, **No topo (hero)**, **No rodapé**, **Topo e rodapé** ou **Não exibir**. Útil quando a arte do topo já traz a marca e você não quer repeti-la.
- **Destaque da causa (“Em prol”)** — **Destaque no topo** (um card chamando a atenção para a causa logo no começo) ou **Não exibir card da causa**.

### Topo da página (hero)

O **hero** é a primeira faixa da página — o "cartaz" da campanha. No card **Topo da página (hero)** você escolhe o **modo**:

- **Automático** — usa imagem + texto se houver uma imagem de hero; senão, mostra só o texto.
- **Só imagem (arte inteira, sem cortar)** — ideal quando você tem um cartaz pronto e quer que ele apareça inteiro, sem cortes.
- **Imagem + texto (título sobre a imagem)** — a imagem vira fundo e o título da campanha fica por cima.
- **Só texto** — sem imagem no topo, foco no título e na chamada.

> A **imagem do hero é separada das fotos do prêmio**: use o botão **Selecionar imagem** para enviar uma arte dedicada ao topo. Sem imagem, o modo cai automaticamente para "Só texto".

![Card Topo da página (hero), com os modos de exibição](/assets/screenshots/publica-hero-modos.png)

## O que mais dá para ajustar nesta aba

- **Painel de transparência** — escolha quais indicadores mostrar (total arrecadado, cartões vendidos, cartões restantes…). O financeiro fica **oculto por padrão** — ative só o que quiser expor. Veja abaixo: em alguns temas a seção precisa ser **ligada** antes.
- **Meta da campanha (termômetro)** — defina uma meta de **cartões** e/ou de **arrecadação (R$)** e a página mostra um termômetro com o progresso e um aviso quando a meta é atingida (veja abaixo).
- **Vídeo de divulgação** — cole um link do **YouTube** ou do **Vimeo** e o vídeo aparece embutido na página (veja abaixo).
- **Compartilhamento / Open Graph** — os botões de redes sociais e o card que aparece quando o link é compartilhado.

![Configuração da meta e do vídeo na aba Página pública](/assets/screenshots/bp-29-config-meta-video.png)

### Painel de transparência
{: #painel-transparencia }

O painel reúne, num quadro só, os números que dão credibilidade à campanha: quantidade de cartões, vendidos, data do sorteio, situação e — a partir da versão **2.23.0** — mais dois indicadores:

- **Participantes** — quantas pessoas diferentes compraram cartões. Mostra que a rifa tem gente de verdade, não só números.
- **Resultado do sorteio** — depois de apurado, o cartão contemplado; antes disso, *"Ainda não sorteado"*.

![Painel de transparência na página pública, com Participantes e Resultado](/assets/screenshots/publica-transparencia.png)

#### O painel funciona nos 6 temas (a partir da 2.24.0)

Até a versão 2.23, o painel de transparência **só existia em 3 dos 6 temas** — e ficava de fora justamente do **Moderno, que é o padrão**. Você marcava os indicadores, salvava sem erro nenhum, e o público não via o painel.

**Isso foi corrigido: agora o painel está disponível em todos os temas** — Sofisticado, Moderno, Clássico, Divertido, Emotivo e Simples. A escolha do tema não limita mais essa decisão.

> ⚠️ **Nos temas que antes não ofereciam o painel, ele nasce desligado**
>
> Para que nenhuma campanha existente mudasse de aparência sozinha, nos temas **Moderno, Divertido e Simples** a seção **Transparência** vem **desligada**. Se você usa um desses temas e quer o painel, **ligue a seção**: em **Aparência da página**, marque **Transparência** na lista de seções exibidas.
>
> Nos temas Clássico, Emotivo e Sofisticado nada muda — a seção continua ligada como sempre esteve.

**O plugin avisa quando os dois não combinam.** Se você marcar indicadores e a seção Transparência estiver desligada, aparece um alerta no próprio card, para você não descobrir isso pela página pública:

![Aviso no admin quando há indicadores marcados e a seção Transparência está desligada](/assets/screenshots/publica-transparencia-secoes.png)

### Termômetro de meta

Na seção **Meta da campanha**, marque **Exibir termômetro de meta** e informe:

- **Meta de cartões** — quantos cartões você quer vender (opcional).
- **Meta em R$** — quanto você quer arrecadar (opcional).
- **Exibir somente a partir de (% da meta atingida)** — o percentual mínimo para a barra começar a aparecer. Deixe **0** para exibir sempre.

Você pode preencher só uma das duas metas, ou as duas. A barra mostra o progresso com marcos em 25%, 50%, 75% e 100%, e exibe **🎯 Meta atingida!** quando chega lá.

> 💡 **Exibir a barra só depois de um avanço.** No começo, uma barra quase vazia pode desanimar quem visita a página. Use **"Exibir somente a partir de X%"** para a barra **só aparecer depois que a campanha atingir aquele percentual** — por exemplo, `50` faz a barra surgir apenas quando a meta chega à metade. Antes disso, a página simplesmente não mostra o termômetro. Se você definir as duas metas (cartões e R$), vale a que estiver **mais adiantada**.

> ⚠️ A **meta em R$** só aparece publicamente se os **indicadores financeiros não estiverem ocultos** (veja o Painel de transparência acima). Se você preferir não mostrar valores, deixe só a meta de cartões — o termômetro de cartões aparece normalmente.

![Termômetro de meta na página pública](/assets/screenshots/bp-30-publica-termometro.png)

### Vídeo de divulgação

Na seção **Vídeo de divulgação**, cole o endereço do vídeo (ex.: `https://youtu.be/...` ou `https://vimeo.com/...`). Só links do **YouTube** e do **Vimeo** são aceitos — não há upload de arquivo. O vídeo aparece embutido na página da campanha.

![Vídeo embutido na página pública](/assets/screenshots/bp-31-publica-video.png)

## Como fica para o público

A página reúne, em uma rolagem: o prêmio com as fotos, a história da causa, o progresso das vendas, a seleção de cartões, o regulamento e os botões de compartilhar. As **cores da sua organização** valem do topo ao rodapé, e a **logomarca aparece sempre sobre um fundo branco**, para se manter nítida tanto no esquema claro quanto no escuro.

**Esquema claro:**

![Página pública no esquema claro](/assets/screenshots/tema-03-publica-clara.png)

**Esquema escuro** (mesma campanha, mesmas cores — só muda o fundo):

![Página pública no esquema escuro](/assets/screenshots/tema-04-publica-escura.png)

### Acessibilidade — tamanho do texto

Toda página pública traz um **controle de tamanho do texto** para o visitante, no **canto superior direito do topo (hero)**: um pequeno box com os botões **A−**, **A** e **A+**.

- **A−** diminui o texto da página; **A+** aumenta; **A** volta ao tamanho padrão.
- A escolha vale para a leitura daquela pessoa (é confortável para quem enxerga menos) e **fica guardada no navegador dela** — ao voltar à página, o tamanho preferido é mantido.

Esse controle aparece **sozinho, em todas as campanhas**, sem nenhuma configuração de sua parte.

![Controle de tamanho do texto (A− / A / A+) no canto do topo da página](/assets/screenshots/publica-tamanho-texto.png)

## Compra: como o participante age

1. Escolhe os cartões — **manualmente** (clicando nos disponíveis) ou pedindo uma **seleção automática** (aleatória).
2. Os cartões ficam **reservados** por alguns minutos (o tempo que você definiu) enquanto ele finaliza.
3. Ele vai ao **checkout do WooCommerce** e paga pelo meio configurado (Pix, cartão, boleto).
4. Ao confirmar o pagamento, os cartões viram **vendidos** e ele recebe um **e-mail com os cartões**.

> 💡 **Dica**
>
> Quer inserir a seleção de cartões ou o regulamento em outra página do site (uma landing page, por exemplo)? Use os **shortcodes** do plugin, como `[rit360_premiado_rifa id="123"]`. Veja [Módulo Página pública](/modulos/pagina-publica/).

> ⚠️ **Atenção — permalinks**
>
> Se o endereço `/campanha/nome` abrir uma página "não encontrada" (404), normalmente é a configuração de **Links permanentes** do WordPress. O plugin tenta ajustar isso sozinho, mas se persistir, vá em **Configurações → Links permanentes** do WordPress e clique em **Salvar** (sem mudar nada) para regenerar as regras.

> ✅ **Boas práticas**
>
> Abra a página pública no **celular** antes de divulgar — a maioria dos seus compradores vai acessá-la assim. Confira se a foto do prêmio, o preço e o botão de comprar estão claros na primeira tela. Se usar o esquema **Automático**, vale testar com o aparelho no modo claro e no modo escuro.
