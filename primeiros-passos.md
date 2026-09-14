---
title: "Primeiros passos"
nav_order: 2
permalink: /primeiros-passos/
role: admin
routes: ["#/", "#/organizacao", "#/campanhas"]
screenshots: [bp-01-dashboard, admin-abas-navegacao, admin-abas-navegacao-mobile, rit-menu-icone]
source_docs: [PRODUCT.md, PRD_Bussola_Premiada.md]
last_verified: 2026-09-14
status: publicado
---

# Primeiros passos

Este guia mostra o caminho completo, do zero à sua primeira campanha no ar, em uma sequência que faz sentido. Se preferir ir direto a uma tarefa específica, use os [Guias por tarefa](/guias/).

## O que o RIT360 Premiado faz

Ele cobre todo o ciclo de uma campanha premiada:

1. Você **configura os dados da organização** uma única vez (nome, CNPJ, contato, identidade visual).
2. **Cria uma campanha** com prêmio, quantidade de cartões e valor.
3. **Gera os cartões** (números ou nomes de uma lista temática).
4. **Publica o regulamento** obrigatório — o plugin monta boa parte dele para você.
5. **Divulga** por uma página pública mobile-first, pronta para compartilhar.
6. As vendas acontecem pelo **checkout do WooCommerce**; os cartões são reservados e confirmados automaticamente.
7. No dia, você **realiza o sorteio** de forma auditável e publica o resultado.
8. Ao final, **presta contas** com documentos e relatórios.

> 💡 **Por que essa ordem importa**
>
> Cada etapa se apoia na anterior: sem dados da organização, o regulamento fica incompleto; sem cartões, não há o que vender; sem regulamento publicado, a campanha não abre. Seguir a sequência evita retrabalho.

## Antes de começar

Você precisa de:

- Um site **WordPress** com o **WooCommerce ativo** (versão 8.0 ou superior). Sem o WooCommerce, o plugin se desativa sozinho e avisa.
- O plugin **RIT360 Premiado** instalado e ativado. A instalação inicial normalmente é feita pela RIT/V3RTECH no momento da implantação.
- Um **meio de pagamento** configurado no WooCommerce (Pix, cartão, boleto — o que sua organização já usa).

## Passo 1 — Abra o painel

No menu lateral do WordPress, clique em **RIT360 Premiado** (uma entrada única, com o mesmo ícone que os outros produtos da família RIT — é o que ajuda a reconhecer rápido qual é o nosso, numa lista com plugins de fabricantes diferentes). Você chega ao **Dashboard**, o cockpit da ferramenta: um resumo das campanhas, da arrecadação e dos próximos sorteios.

![Ícone do RIT360 Premiado no menu lateral do WordPress, igual ao dos outros produtos da família RIT](/assets/screenshots/rit-menu-icone.png)

![Painel do RIT360 Premiado](/assets/screenshots/bp-01-dashboard.png)

O painel do RIT360 Premiado usa o **cabeçalho e a barra de navegação da família RIT360**, os mesmos que você encontra nos outros produtos RIT — o que muda é só a moldura ao redor da tela; nenhuma função, campo ou permissão muda com isso.

No cabeçalho, ao lado da logo, aparece o nome da tela em que você está e a versão do plugin instalada; à direita ficam os botões **💬 Feedback** e **📖 Manual / Guia**, que leva sempre a esta documentação. Logo abaixo, a **barra de abas** leva a cada seção — **Dashboard, Campanhas, Templates, Auditoria, Configurações, Shortcodes e API e Licença** — e a aba em que você está aparece com um **traço âmbar** embaixo do nome. Cada pessoa vê só as abas que pode acessar; se você tinha um endereço antigo de alguma seção salvo nos favoritos, ele continua levando à tela certa.

Quando o WordPress tem algum aviso para mostrar naquela tela (um alerta do plugin, uma pendência), ele aparece numa **faixa própria**, logo abaixo da barra de abas e acima do conteúdo — não mais espalhado pela tela.

![Barra de abas de navegação, com a aba ativa sublinhada em âmbar e a faixa de avisos abaixo dela](/assets/screenshots/admin-abas-navegacao.png)

No **celular**, o cabeçalho e as abas se empilham em vez de ficar lado a lado — a navegação continua toda visível, sem precisar abrir um menu à parte.

![Cabeçalho e barra de abas no celular, com as abas quebrando em linhas](/assets/screenshots/admin-abas-navegacao-mobile.png)

## Passo 2 — Configure sua organização

Antes de criar campanhas, preencha os dados institucionais em **Configurações**. Eles alimentam automaticamente o regulamento, os e-mails e a página pública.

➡️ Siga o guia [Configurar a organização](/guias/configurar-organizacao/).

## Passo 3 — Prepare a lista de cartões (opcional, mas recomendado)

Você pode sortear **números** (1, 2, 3…) ou **nomes de uma lista temática** (animais, cidades, personagens). O plugin já vem com 9 listas prontas — mas você pode criar as suas.

➡️ Veja [Montar os cartões](/guias/montar-cartoes/).

## Passo 4 — Crie sua primeira campanha

Com a organização configurada, é hora de criar a campanha: prêmio, valor do cartão, quantidade e datas.

➡️ Siga [Criar a primeira campanha](/guias/criar-primeira-campanha/).

## Passo 5 — Publique o regulamento e abra a campanha

Nenhuma campanha entra no ar sem regulamento publicado. O plugin monta o texto a partir dos seus dados e de cláusulas prontas.

➡️ Veja [Publicar o regulamento](/guias/publicar-regulamento/).

## Passo 6 — Divulgue

Cada campanha ganha uma página pública própria, com botões de compartilhamento e painel de transparência.

➡️ Veja [Personalizar a página pública](/guias/personalizar-pagina-publica/).

## Passo 7 — Acompanhe, sorteie e preste contas

Durante a venda, acompanhe tudo pelo Painel. No dia, faça a apuração; depois, feche com a prestação de contas.

➡️ [Acompanhar as vendas](/guias/acompanhar-vendas/) · [Realizar o sorteio](/guias/realizar-sorteio/) · [Prestar contas](/guias/prestar-contas/)

> ✅ **Boas práticas para o começo**
>
> Rode uma **campanha-piloto pequena** primeiro — poucos cartões, prêmio modesto — só para percorrer o fluxo inteiro (criar, publicar, comprar um cartão de teste, sortear, prestar contas) antes de lançar a campanha "de verdade". Você ganha confiança e descobre ajustes sem pressão.
