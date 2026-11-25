### Gerador procedural de mapas regionais para RPG — perspectiva 2.5D

O **Atlas das Terras Selvagens** é um gerador procedural de regiões para campanhas de RPG de mesa, especialmente Dungeons & Dragons. Ele cria cenários com florestas, campos, água, estradas, construções e locais de aventura, apresentados em uma perspectiva 2.5D inspirada em jogos como *Project Zomboid*.

O projeto funciona diretamente no navegador e não precisa de instalação de bibliotecas ou servidor.

## Como abrir

1. Baixe o arquivo `geradorRPG.html`.
2. Abra-o com dois cliques ou clique com o botão direito e escolha um navegador (Chrome, Firefox, Edge etc.).
3. Aguarde o mapa inicial aparecer.

Não é necessário instalar Python, Node.js ou qualquer dependência. O gerador foi desenvolvido com HTML, CSS e JavaScript nativos.

## Como gerar e explorar um mapa

### Gerar uma região

- **Gerar região:** cria novamente o mapa usando o número informado no campo de semente.
- **Sortear:** escolhe uma nova semente aleatória e gera outra região.
- **Semente:** é o número usado para reproduzir a geração. Mantendo a mesma semente e as mesmas configurações, o gerador produz o mesmo cenário.

### Navegar pelo mapa

- **Arrastar com o mouse:** movimenta a visualização.
- **Roda do mouse:** aproxima ou afasta o mapa.
- **+ Zoom / − Zoom:** controla a aproximação pelos botões.
- **Centralizar:** retorna a visualização para o enquadramento inicial.

### Personalizar a região

Abra a seção **Configurações da região** para ajustar:

- Largura e altura do mapa em células.
- Densidade de árvores.
- Quantidade de construções.
- Quantidade de ruínas e masmorras.
- Quantidade de lagos e rochas.

Também é possível ativar ou desativar estradas, árvores, construções, água e riachos, nomes dos locais de aventura e sombras. As alterações atualizam o mapa automaticamente.

## Como funciona a geração procedural

O mapa é criado por código, sem depender de um mapa pronto. A semente inicial alimenta um gerador pseudoaleatório reproduzível. A partir dela, o sistema:

1. Calcula variações suaves de terreno para formar áreas baixas, campos e regiões elevadas.
2. Distribui áreas de água, manchas de floresta e vegetação.
3. Posiciona árvores e rochas.
4. Distribui construções, como casas, estalagens e celeiros.
5. Cria pontos de interesse, incluindo masmorras e ruínas.
6. Traça estradas entre alguns núcleos de construções e desenha pequenos cursos de água.

A geração utiliza regras e probabilidades. Por isso, os elementos e suas posições variam de acordo com a semente e com as configurações escolhidas.

## Como funciona o visual 2.5D

Apesar da aparência inclinada, o projeto **não utiliza um motor 3D**. O cenário é desenhado em um elemento `Canvas` 2D.

Cada célula do terreno é projetada como um losango isométrico. Árvores, construções, rochas e outros objetos recebem camadas, faces laterais, sombras e detalhes. A ordem em que os elementos são desenhados ajuda a criar a sensação de profundidade e sobreposição.

Essa abordagem é chamada de **2.5D**: o desenho é bidimensional, mas simula volume e perspectiva.

## Sistema de rolagem de dados

O painel **Dados de RPG**, localizado à direita do mapa em telas maiores, permite rolar:

- d4
- d6
- d8
- d10
- d12
- d20
- d100

Antes de rolar, ajuste a quantidade de dados e o modificador. Clique no dado desejado para realizar a rolagem. O painel apresenta os resultados individuais, a soma e o modificador aplicado.

No caso de uma rolagem de apenas um d20, os resultados naturais 1 e 20 recebem destaque. O histórico mantém as últimas 20 rolagens e pode ser apagado pelo botão **Limpar**.

O botão **Rolar d20 com modificador** executa diretamente uma rolagem de d20 usando a quantidade e o modificador definidos nos campos.

## Tecnologias utilizadas

- **HTML5:** estrutura da página.
- **CSS3:** layout, aparência e adaptação para telas menores.
- **JavaScript:** geração procedural, controles, navegação e rolagem de dados.
- **Canvas 2D:** desenho do mapa e simulação visual da perspectiva 2.5D.

## Limitações atuais

- O mapa é uma representação visual para criação e inspiração de cenários; não é um tabuleiro com movimentação ou regras de combate.
- A perspectiva é simulada em 2D, não é uma cena 3D navegável.
- O histórico de dados existe durante a sessão atual da página; ao recarregar o navegador, ele é reiniciado.
- O projeto não possui, nesta versão, funções de salvar ou exportar o mapa como imagem.

## Licença

MIT.
