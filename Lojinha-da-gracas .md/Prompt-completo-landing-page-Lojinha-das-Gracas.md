# Prompt completo da landing page | Lojinha das Graças

## PROMPT PARA COPIAR

Crie ou reproduza com alta fidelidade a landing page da **Lojinha das Graças**, loja de artigos religiosos católicos e presentes. A página funciona como um ponto de entrada para quem chega pelo Instagram: apresenta a identidade da loja, oferece conversa pelo WhatsApp, encaminha para categorias do site de vendas, mostra um destaque de catálogo e fornece localização e redes sociais. O idioma de toda a interface é português brasileiro.

### 1. Escopo e arquitetura

- Entregue uma única página responsiva, estática e leve, sem login, carrinho, checkout, banco de dados ou catálogo interno. A página encaminha o visitante para a loja virtual e para os canais existentes.
- Na versão atual, o projeto usa `dist/index.html`, `dist/styles.css` e os arquivos de imagem em `dist/assets/`. O manifesto `.openai/hosting.json` define `static.directory` como `dist`. HTML semântico e CSS puro são suficientes; não acrescente um framework apenas por conveniência.
- O arquivo `dist/links.js` existe como rascunho antigo com destinos vazios, mas **não está carregado no HTML atual**. Os links ativos estão diretamente nos atributos `href` de `index.html`. Se refatorar links, mantenha os destinos corretos e elimine qualquer lógica antiga que substitua links por `#`.
- Estruture com `<main class="page">`, `<header class="hero">`, seções de categorias, destaque, valores, localização e `<footer>`. Use rótulos e textos alternativos descritivos nas imagens. Links externos abrem em nova aba com `rel="noopener noreferrer"`.
- Mantenha a experiência visual aprovada. Não invente seções, produtos, preços, avaliações, mapa incorporado, menu superior, chat flutuante ou formulário.

### 2. Layout e hierarquia visual

- O corpo da página tem fundo bege acinzentado `#e9dfd0`. A página central tem largura máxima de **720 px**, fundo creme `#fbf5ea`, altura mínima da tela e sombra discreta `#4e321923`. Mesmo em monitor largo, preserve essa coluna estreita, semelhante a uma landing page para link da bio. Em telas a partir de 800 px, deixe cerca de 35 px de respiro vertical no fundo externo.
- Ordem exata: (1) banner com logo e frase, (2) botão WhatsApp abaixo do banner, (3) três benefícios, (4) título “Encontre o que você procura”, (5) botão “Acessar nosso site”, (6) quatro cards de categorias, (7) destaque “Escolhidos com fé para momentos especiais” e botão “Ver catálogo”, (8) três valores da loja, (9) localização com “Como chegar”, (10) rodapé com Instagram e WhatsApp.
- Linguagem visual: devocional, acolhedora, delicada e premium, com creme, bege, dourado e marrom. Bordas arredondadas moderadas, sombras discretas, ornamentos finos, ícones de linha simples. Evite ícones genéricos em forma de bolinha para WhatsApp, sacola ou mapa.

### 3. Identidade, imagens e fontes

- **Logo oficial da página:** `assets/logo.png`, 1122 × 1402 px, com medalhão de Nossa Senhora e assinatura da Lojinha. Use o próprio arquivo; não redesenhe o rosto, a medalha ou as letras. Se o usuário fornecer uma versão oficial mais recente, substitua só após conferir qual é a correta.
- **Banner e destaque:** `assets/banner-horizontal.png`, 1672 × 941 px. Mostra Nossa Senhora das Graças em cenário devocional com terço, vela e flores. No banner, preserve a imagem e evite cortar o rosto, o terço ou a vela. A composição reserva espaço para logo e frase à esquerda.
- **Categorias:** “Imagens religiosas” usa o próprio `banner-horizontal.png`, enquadrando Nossa Senhora com vela e terço; “Terços” usa `assets/terco-categoria.png`, 1254 × 1254 px; “Kits especiais” usa `assets/kits-especiais.png`, 1254 × 1254 px; “Lembranças e presentes” usa `assets/lembrancas.png`, 1254 × 1254 px. Preserve a aparência de fotografias de produtos religiosos com tons quentes e cenário coerente.
- Fontes carregadas do Google Fonts: `DM Sans` pesos 400, 500, 600, 700 para corpo e textos funcionais; `Playfair Display` pesos 400, 500, 600 para títulos, nomes de categorias e botões principais; `Cormorant Garamond` pesos 400, 500 para a frase delicada dentro do banner. Fallback de serifas: Georgia. A frase do banner deve ter traço fino, peso 400, nunca negrito.
- O título do documento é `Lojinha das Graças | Artigos Religiosos & Presentes`. Descrição: `Artigos religiosos, terços, kits e presentes especiais. Conheça a Lojinha das Graças.` Cor de tema do navegador: `#f8f0e5`.

### 4. Cores exatas da versão atual

Use os códigos abaixo para conservar a composição. Alguns são variações de superfície, borda, texto, gradiente ou sombra, e não cores independentes de marca.

| Elemento | Código e aplicação |
| --- | --- |
| Fundo externo e página | `#e9dfd0` externo; `#fbf5ea` creme da página e do rodapé |
| Texto base e texto da frase | `#4b2916` no corpo; `#4b2e1a` na frase fina |
| Texto escuro do rodapé | `#45291b` e `#4b2d20`; círculos sociais `#4b281d`; texto branco `#fff` |
| Área atrás do banner e sobreposição | `#f3e6d4`; gradiente lateral com `#f9eee0`, `#f9eee0d9`, `#f9eee063`, terminando em transparente |
| Botões dourados | gradiente a 140° entre `#bb8938` e `#936013`; sombra `#98611b2e`; texto branco `#fff` |
| Botão de site vazado | borda `#b27a26`, fundo `#fff9ee`, texto `#684016`, ícone globo `#9a681e` |
| Linha de título e ícones de benefícios | linha `#b98944`; ícones `#af7a33`; texto de apoio `#79522b` |
| Cards de categoria | superfície `#fffaf2`; círculo de seta `#6d4619`; sombra `#8f6d3a20` |
| Destaque do catálogo | fundo `#f1e2c7`, borda `#e7d1ae`, descrição `#704b29` |
| Três valores | círculos com borda `#bd8a3e`, símbolo `#a66d22`, texto `#86551e` |
| Localização | fundo `#f5e9d2`, borda `#e1ccaa`, gradiente radial `#f9edd3` a `#c59a5e`, estrela `#fff9e9`, sombra da estrela `#68451e66`, descrição `#78532f` |
| Ornamentos do rodapé | dourado `#b27b2d`; linhas `#d8bb82` e `#dfc799` |
| Acessibilidade e efeitos | contorno de foco `#5b3412`; sombra do container `#4e321923`; sombra sutil do logo `#fff8ed` |

### 5. Seções, conteúdo e dimensões

**Banner:** `hero-scene` tem 390 px de altura no layout padrão e 260 px até 530 px de largura de tela. Imagem de fundo HTML em `object-fit: cover`, com enquadramento à direita. Adicione sobreposição de degradê claro à esquerda para legibilidade. Posicione o logo no alto à esquerda, com 190 px de largura no padrão; em telas até 530 px, 125 px de largura. A frase dentro do banner fica abaixo do logo, próxima ao limite inferior da imagem, à esquerda, e diz exatamente: “Artigos religiosos feitos / com carinho para momentos / especiais de fé.” Use `Cormorant Garamond` 400, cor `#4b2e1a`, cerca de 1.45 rem e linha 1.04 no padrão; cerca de 1.02 rem e largura 45% no celular. A frase deve ter aspecto fino. **O botão de WhatsApp fica fora e imediatamente abaixo da imagem do banner**, nunca sobreposto ao cenário.

**Botão e benefícios:** botão dourado largo com ícone reconhecível do WhatsApp em SVG, texto “Falar no WhatsApp” em Playfair Display e pequena seta à direita. Altura mínima aproximada de 62 px no padrão e 52 px no celular. Logo abaixo, três itens com SVG de caminhão, coração e capela, nesta ordem: “Atendimento próximo e personalizado”, “Produtos escolhidos com muito carinho” e “Para os seus momentos de fé”. Mantenha os três lado a lado no celular, respeitando a legibilidade.

**Categorias:** título central em maiúsculas “ENCONTRE O QUE VOCÊ PROCURA”, ladeado por traços dourados finos. Em seguida, botão vazado “Acessar nosso site”, com ícone de globo. Grade de quatro cards na ordem: “Imagens religiosas”, “Terços”, “Kits especiais”, “Lembranças e presentes”. Cada card tem foto acima e rótulo abaixo com um círculo marrom contendo uma seta. No layout padrão, quatro colunas com espaço de 14 px, foto de 165 px; até 530 px, quatro colunas com espaço de 7 px e foto de 110 px; abaixo de 350 px, duas colunas e fotos de 150 px. Use `object-fit: cover`, com enquadramento ajustado para manter Nossa Senhora visível no primeiro card.

**Destaque do catálogo:** card arredondado bege claro, imagem devocional à esquerda e conteúdo à direita. Título exato: “Escolhidos com fé para momentos especiais”. Descrição: “Produtos que acompanham as suas celebrações e tornam cada momento ainda mais significativo.” Botão dourado “Ver catálogo” com ícone de sacolinha à esquerda e seta à direita. Este botão leva à página inicial da loja virtual, não ao WhatsApp. Layout padrão aproximadamente 48% imagem e 52% conteúdo; no celular, 43% e 57%, mantendo o card horizontal. Imagem com 280 px de altura no padrão e 205 px em telas até 530 px.

**Três valores:** três itens lado a lado com símbolos em círculos: coração, símbolo decorativo de atendimento e cruz. Textos: “Produtos selecionados com qualidade”; “Atendimento humano e personalizado”; “Artigos para os principais momentos da vida cristã”.

**Localização:** card horizontal com painel dourado à esquerda, estrela branca no centro e conteúdo à direita. Título “Visite nossa loja”. Descrição “Nossa loja física te espera com muito carinho.” Botão “Como chegar”, em Playfair Display, com ícone SVG de mapa à esquerda e seta à direita. Proporção aproximada de 45%/55% no padrão e 40%/60% no celular.

**Rodapé:** fundo creme, traço dourado horizontal dividido por flor de lis, texto “Acompanhe também nas nossas redes”, duas opções horizontais “Instagram” e “WhatsApp” com ícones brancos em círculos marrom escuro. Na base, outra pequena flor de lis entre linhas e a assinatura em duas linhas: “Lojinha das Graças” / “Artigos religiosos com fé e carinho.” Preserve esse detalhamento, espaçamento e alinhamento central.

### 6. Links funcionais atuais

| Elemento | Destino |
| --- | --- |
| Falar no WhatsApp | `https://wa.me/5598920075298?text=Ol%C3%A1%21%20Vim%20pelo%20Instagram%20e%20gostaria%20de%20conhecer%20a%20Lojinha%20das%20Gra%C3%A7as.` |
| Acessar nosso site e Ver catálogo | `https://lojinhas-das-gracas-git-main-jcleyton147-9458s-projects.vercel.app/` |
| Imagens religiosas | `https://lojinhas-das-gracas-git-main-jcleyton147-9458s-projects.vercel.app/?cat=Imagem%20Sacra` |
| Terços | `https://lojinhas-das-gracas-git-main-jcleyton147-9458s-projects.vercel.app/?cat=Ter%C3%A7o` |
| Lembranças e presentes | `https://lojinhas-das-gracas-git-main-jcleyton147-9458s-projects.vercel.app/?cat=Lembran%C3%A7as` |
| Kits especiais, temporariamente | `https://lojinhas-das-gracas-git-main-jcleyton147-9458s-projects.vercel.app/?cat=Lembran%C3%A7as` |
| Como chegar | `https://maps.app.goo.gl/a4UMZhVNKtknR1Nq6` |
| Instagram | `https://www.instagram.com/lojinhasradasgracas/` |
| WhatsApp no rodapé | `https://wa.me/5598920075298` |

O número comercial é **(98) 92007-5298**, com código de país 55 no `wa.me`. A categoria de kits ainda não tem subcategoria própria no site e usa o mesmo destino de Lembranças por decisão temporária. Troque somente quando a URL definitiva de kits for fornecida. A loja virtual ainda estava em cadastro de produtos. Confirme o acesso público do endereço da Vercel antes de usar a página em divulgação definitiva.

### 7. Responsividade e acabamento

- Preserve a ordem e os links em todos os tamanhos. Evite rolagem horizontal, cortes bruscos na imagem sacra, texto sobreposto, botões pequenos demais ou ícones distorcidos.
- Pontos de ajuste da versão atual: até 530 px, banner e tipografia compactos, cards em quatro colunas, destaque e localização ainda horizontais; abaixo de 350 px, categorias em duas colunas. Em telas acima de 800 px, centralize a página com respiro externo.
- Use `alt` nas imagens, foco visível para teclado, texto legível, `prefers-reduced-motion` para remover transições e ícones SVG `aria-hidden` quando acompanhados de texto. Hover pode elevar discretamente botões e cards em 2 px.
- Não substitua as imagens ou o logo aprovados por material gerado automaticamente. Não mova o botão de WhatsApp para dentro do banner. Não faça “Ver catálogo” abrir WhatsApp. Mantenha a fonte Playfair Display nos botões “Falar no WhatsApp”, “Ver catálogo” e “Como chegar”.
- Ao implementar, confira a página completa em celular e desktop, os destinos dos links, o enquadramento das imagens e a fidelidade visual ao print e aos arquivos originais. Se receber ajustes pontuais posteriores, modifique somente os elementos solicitados.

### 8. Entrega esperada

Entregue o código pronto para hospedagem estática, os assets no local correto e uma prévia visual da página inteira. Descreva objetivamente qualquer diferença inevitável em relação à versão de referência. Preserve a identidade da Lojinha das Graças e não apresente uma recriação livre como se fosse a página original.

## FIM DO PROMPT
