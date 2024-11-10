# Imagens

As imagens desempenham um papel fundamental na comunicação visual, mas quando não são acessíveis, podem representar uma barreira para usuários com deficiência visual ou cognitiva. Garantir que as imagens sejam acessíveis envolve fornecer descrições alternativas claras, contextuais e funcionais, permitindo que todos os usuários compreendam o conteúdo visual. 

### Pontos relevantes

### **Texto Alternativo (alt text)**

- O **texto alternativo** (atributo `alt`) é essencial para que leitores de tela possam descrever o conteúdo de uma imagem a usuários com deficiência visual.
- O `alt` deve ser **curto e descritivo**, fornecendo uma explicação clara sobre o que a imagem representa ou a sua função.
    - Exemplo: `<img src="grafico.jpg" alt="Gráfico mostrando aumento de vendas em 2024">`.
- **Imagens decorativas** que não adicionam significado ao conteúdo (por exemplo, fundos ou ícones meramente estéticos) devem ter o atributo `alt` vazio: `alt=""`.

### **Imagens Funcionais**

- Quando uma imagem atua como um link ou botão, o `alt` deve descrever a função da imagem, e não o seu conteúdo visual.
    - Exemplo: `<img src="botao-comprar.jpg" alt="Comprar agora">`.
- Isso garante que os usuários saibam o que acontecerá ao interagir com a imagem.

### **Imagens Complexas (Gráficos, Diagramas)**

- Para **imagens complexas**, como gráficos ou diagramas, o texto alternativo pode não ser suficiente. Nesse caso, forneça uma descrição detalhada em outro local, como em um texto próximo ou em um link para uma descrição completa.
    - Exemplo: `alt="Gráfico de barras comparando vendas"`, seguido de uma descrição textual mais completa na página.

### **Imagens de Texto**

- Evite o uso de **imagens contendo texto**, pois elas não são escaláveis e nem acessíveis para usuários de leitores de tela. Sempre que possível, use texto real em vez de imagens.
- Se o uso de imagem com texto for inevitável, inclua todo o texto no `alt`.

### **Legendas e Descrições**

- Para imagens que fazem parte de um conteúdo mais amplo, como fotos em artigos ou blogs, forneça uma legenda que contextualize a imagem. Isso é útil tanto para usuários com deficiência visual quanto para aqueles que podem ter dificuldades em interpretar imagens sozinhas.
- As **legendas** devem complementar o texto alternativo, não substituí-lo.

### **Ajuste de Tamanho e Responsividade**

- As imagens devem ser ajustadas para funcionar em diferentes tamanhos de tela. Use técnicas de **responsividade** como o atributo `srcset` e **media queries** para garantir que imagens sejam carregadas corretamente em dispositivos móveis e desktop, sem comprometer a acessibilidade.

### **Imagens e Contraste de Cores**

- Certifique-se de que as imagens contenham **bom contraste de cores** para facilitar a visualização por usuários com baixa visão. Isso é especialmente importante em gráficos e diagramas que dependem de distinção de cores para transmitir informações.

### **Compatibilidade com Leitores de Tela**

- Teste as imagens com **leitores de tela** para garantir que o `alt` seja lido corretamente e que o fluxo de navegação não seja interrompido ou confuso. Testar em diferentes ferramentas pode garantir uma experiência mais consistente.
