---
title: "Dúvidas frequentes"
nav_order: 7
permalink: /faq/
last_verified: 2026-08-09
status: publicado
---

# Dúvidas frequentes

## Sobre a ferramenta

### O que é o RIT360 Premiado?
Um plugin para WordPress, integrado ao WooCommerce, que permite a Organizações da Sociedade Civil criar, vender, divulgar, apurar e prestar contas de campanhas premiadas (sorteios e rifas eletrônicas) — com transparência e governança.

### Preciso de quê para usar?
Um WordPress com **WooCommerce ativo** (8.0+), o plugin instalado e um meio de pagamento configurado no WooCommerce (Pix, cartão, boleto). Veja os [Primeiros passos](/primeiros-passos/).

### O RIT360 Premiado processa o pagamento?
Não. O pagamento é feito pelo **checkout do WooCommerce**, com o meio que sua organização já usa. O plugin cuida dos cartões, do sorteio e da prestação de contas.

### Quanto custa?
O plugin é **software livre** (licença GPL). Há um recurso **opcional** de [doação voluntária à RIT](/guias/apoiar-a-rit/) para apoiar o projeto — mas ele funciona integralmente sem qualquer doação.

## Legalidade e segurança

### Usar o plugin deixa minha campanha "legal" automaticamente?
Não. O plugin **apoia** a conformidade (regulamento obrigatório, apuração auditável, prestação de contas), mas **não substitui** aconselhamento jurídico nem protocola autorizações. A responsabilidade pela regularidade é da organização. Leia [Requisitos legais de um sorteio](/boas-praticas/requisitos-legais/) e o [Aviso legal](/legal/aviso/).

### Preciso de autorização do governo para fazer uma rifa?
Depende da modalidade e do valor. Sorteios no Brasil são regulados (Lei 5.768/1971, Decreto 70.951/1972) e alguns exigem autorização prévia do Ministério da Fazenda. Consulte um profissional para o seu caso.

### Como o sorteio é confiável?
Você escolhe: sorteio pela **Loteria Federal**, **apuração interna auditável** (qualquer pessoa refaz a conta e confere o resultado) ou **registro manual**. Antes de sortear, a base de cartões é **congelada** e fica imutável. Veja [Apuração](/modulos/apuracao/).

### Onde escolho o método de apuração?
Na aba **Formulário** da campanha (etapa *Configurações da Campanha*), no campo **Método de apuração** — e **só ali**. A aba Apuração apenas mostra o que foi escolhido. Antes da versão 2.22 havia dois seletores, que podiam discordar entre si.

### Como funciona a apuração pela Loteria Federal?
Os cartões vendidos entram em ordem (são **N**); os **5 números** da extração oficial são colados um no outro, na ordem em que saíram, formando um número **V**; o **resto da divisão de V por N** aponta o cartão contemplado. Numa planilha: `=MOD(V;N)+1`. Como o resto sempre cai dentro da lista, o resultado sempre resolve — não existe "regra de aproximação". O **regulamento traz essa explicação com um exemplo numérico**.

### O sistema pode finalizar o sorteio sozinho?
Sim, mas com uma condição. Havendo resultado apurado, a organização tem **5 dias corridos** para conferir e finalizar; passado o prazo, o sistema finaliza sozinho. Isso **só vale se o regulamento publicado daquela campanha declarar o prazo** — o regulamento é congelado por versão, e ninguém pode ser submetido a uma regra que não estava no documento que leu. Campanhas antigas continuam esperando você, a menos que o regulamento seja republicado.

### Apareceu um aviso dizendo que o regulamento está com a apuração desatualizada. E agora?
É um lembrete, não um bloqueio: a campanha continua funcionando. Ele aparece quando o regulamento foi publicado **antes** das novas cláusulas de apuração. Para resolver, abra a campanha, vá na aba **Regulamento** e **republique** — isso gera uma nova versão com o texto completo, e o aviso **some**. Se ele continuar, é porque **outra** campanha ainda está pendente: confira os nomes listados no próprio aviso. (Ele aparece apenas nas telas do RIT360 Premiado.) Veja [Publicar o regulamento](/guias/publicar-regulamento/#regulamento-apuracao-desatualizada).

### E a proteção de dados (LGPD)?
Os dados pessoais são tratados com privacy-by-design: relatórios saem **mascarados** por padrão, o documento do ganhador é sempre privado, o consentimento para e-mails promocionais é explícito e há trilha de auditoria. Veja a [Política de Privacidade](/legal/privacidade/).

## Campanhas e cartões

### Posso sortear nomes em vez de números?
Sim. Os cartões podem ser **números** ou **nomes de uma lista temática**. O plugin traz 9 listas prontas e você pode criar as suas. Veja [Montar os cartões](/guias/montar-cartoes/).

### Posso mudar a quantidade de cartões depois de publicar?
Não com vendas em andamento. Quantidade e valor são definidos no **rascunho** e travam após a publicação, para proteger a integridade da rifa. Planeje antes de abrir.

### Dois compradores podem levar o mesmo cartão?
Não. Há um mecanismo de **reserva atômica**: quando um cartão está no carrinho de alguém, ninguém mais o compra. Se a compra não é concluída no tempo de reserva — ou se a pessoa **remove o cartão do carrinho** —, ele volta ao pool na hora, livre para outra pessoa.

### Deixei o carrinho parado e apareceu "sua reserva expirou". Perdi o cartão?
Não necessariamente. Ao finalizar, o sistema tenta garantir **os mesmos cartões**: se continuarem livres, a compra segue normalmente. Se alguém já tiver escolhido algum, a compra é **interrompida antes de qualquer cobrança**, dizendo qual cartão se perdeu — aí basta voltar ao carrinho e escolher outro. Veja [Quando a reserva do cartão expira](/guias/reserva-expirada/).

### Um comprador pagou e não recebeu o cartão. Como resolvo?
Pelo painel **Corrigir cartões**, na tela da campanha: você busca o cartão, informa o número do pedido pago, escreve a justificativa e aplica — o cartão passa a vendido e o pedido passa a exibir a linha "Cartões". Passo a passo em [Corrigir cartões](/guias/corrigir-cartoes/).

### Por que não consigo mudar a quantidade de um cartão no carrinho?
Porque cada cartão é **único** — não existe "2 unidades" do mesmo número ou nome. No carrinho, cada cartão aparece pelo seu nome (e, nas campanhas apuradas pela **Loteria Federal**, pelo **número de sorteio**), com a quantidade **fixa em 1**. Para desistir de um cartão, **remova-o** do carrinho: ele é liberado imediatamente para outra pessoa.

### Posso comprar cartões junto com outros produtos da loja?
Não no mesmo pedido. Os **cartões de rifa são comprados separadamente** dos demais produtos da loja, para evitar conflitos no checkout (entrega, conclusão do pedido e reservas). Se você tiver outros produtos no carrinho e tentar adicionar cartões — ou o contrário —, aparece um **aviso** pedindo para finalizar ou esvaziar a compra atual primeiro. **Cartões de campanhas diferentes**, porém, podem ser comprados **juntos**, no mesmo pedido.

### O checkout pede endereço de entrega?
Não. O cartão é digital (você o recebe por e-mail), então o produto é **virtual** — o checkout **não pede endereço de entrega** e o pedido se conclui automaticamente após o pagamento.

### Posso ter mais de um prêmio na mesma campanha?
Sim. Na etapa **Dados do Prêmio**, use **+ Adicionar prêmio** para incluir 1º, 2º, 3º lugar… na ordem em que serão sorteados. Todos saem **da mesma base de cartões vendidos, sem repetir número** — cada prêmio vai para um cartão diferente. O regulamento, o resultado público e os e-mails passam a mostrar um ganhador por prêmio. Se quiser um prêmio só, deixe apenas o primeiro. Veja [Criar a primeira campanha](/guias/criar-primeira-campanha/).

### Posso oferecer desconto para quem compra vários cartões?
Sim — configure **descontos por quantidade** na campanha. Ótimo para aumentar o ticket médio.

### Como remarco a data do sorteio?
Pelo diálogo de reagendamento na campanha. O plugin exige **justificativa**, avisa **todos os compradores** por e-mail e registra a mudança. Datas de campanhas sorteadas/canceladas só mudam com permissão de Administrador do plugin.

## Página e divulgação

### A campanha tem endereço próprio?
Sim: `/campanha/nome-da-campanha`, um hotsite mobile-first. Veja [Página pública](/modulos/pagina-publica/).

### O endereço da campanha dá "página não encontrada" (404). O que faço?
Vá em **Configurações → Links permanentes** do WordPress e clique em **Salvar** (sem mudar nada) para regenerar as regras.

### Posso colocar a rifa dentro de outra página do site?
Sim, com **shortcodes** como `[rit360_premiado_rifa id="123"]`. Veja [Página pública](/modulos/pagina-publica/).

## E-mails

### Quais e-mails o plugin envia?
Confirmação de compra, aviso de nova venda, esgotado, lançamento, lembrete de sorteio, **vendas encerradas** (aos coordenadores), mudança de data, resultado e ganhador. Veja [Configurar os e-mails](/guias/configurar-emails/).

### A campanha encerrou as vendas e ninguém percebeu. Dá para ser avisado?
Sim — é automático. Quando o período de vendas termina, **todos os coordenadores** da campanha recebem o e-mail **"Vendas encerradas"**, com o resumo do que foi vendido, a data prevista do sorteio e o que fazer em seguida conforme o método de apuração. A página pública também passa a exibir o aviso de vendas encerradas com a data do sorteio.

### Um comprador não quer mais receber e-mails promocionais. Como funciona?
E-mails promocionais só vão para quem **consentiu**, e cada um traz um link de **descadastro de um clique**. E-mails transacionais (confirmação de compra) sempre são enviados.

## Ainda com dúvida?

Se algo não foi respondido aqui, fale com a equipe da [RIT](https://rit.org.br). E confira as [Novidades](/novidades/) para ver o que mudou nas versões recentes.
