# Elementos Clicáveis

Elementos clicáveis, como botões, links e ícones interativos, são essenciais para a navegação e a funcionalidade de qualquer interface. Garantir que esses elementos sejam acessíveis é crucial para permitir que todos os usuários, independentemente de suas habilidades físicas ou cognitivas, possam interagir com a aplicação.

### **Tamanho da Área Clicável**

- A área de clique deve ser grande o suficiente para facilitar a interação, especialmente em dispositivos móveis. Botões e links muito pequenos podem ser difíceis de clicar, especialmente para pessoas com dificuldades motoras.
- Diretrizes sugerem que a área mínima de toque seja de **44x44 pixels** em interfaces móveis.

### **Identificação Visual Clara**

- **Botões e links** devem ser facilmente identificáveis, utilizando estilos visuais consistentes (como cores, bordas, ícones) para indicar sua interatividade.
- **Links** devem ser destacados visualmente, não apenas por cor, mas também por sublinhado ou negrito. Isso é importante para usuários com daltonismo ou baixa visão que podem não distinguir cores facilmente.

### **Foco e Navegação por Teclado**

- Todos os elementos clicáveis devem ser acessíveis via **navegação por teclado**, o que significa que o usuário deve ser capaz de usar a tecla `Tab` para navegar entre eles.
- O estado de foco deve ser **visível** e destacado de maneira clara para garantir que os usuários saibam qual elemento está ativo no momento.
    - Exemplo: adicionar uma borda ou alterar o fundo ao receber o foco:
        
        ```css
        button:focus {
           outline: 2px solid blue;
        }
        ```
        

### **Atributos ARIA e Papéis Semânticos**

- Elementos clicáveis personalizados (como botões construídos com `div` ou `span`) devem usar o atributo **ARIA** correto para garantir que leitores de tela reconheçam sua função.
    - Exemplo: Para criar um botão com `div`, use `role="button"` e implemente os atributos ARIA relevantes.
- Sempre prefira usar elementos HTML semânticos como `<button>` para botões e `<a>` para links, que já possuem comportamentos acessíveis integrados.

### **Rótulos Acessíveis (aria-label)**

- Elementos clicáveis devem ter **rótulos acessíveis** que descrevem claramente sua função ou destino. Isso é especialmente importante para ícones ou botões sem texto visível.
    - Exemplo: `<button aria-label="Enviar formulário"></button>`.

### **Texto de Botões e Links**

- O texto dos botões e links deve ser **claro e descritivo**, indicando a ação que será realizada ao clicar. Evite rótulos vagos como "Clique aqui" ou "Saiba mais".
    - Exemplo: Em vez de usar "Clique aqui", use "Veja nossos produtos".

### **Feedback de Ação**

- Forneça um **feedback claro** quando um botão ou link for clicado, como mudar a cor do botão, desabilitar temporariamente ou exibir uma mensagem de confirmação, para garantir que os usuários saibam que sua ação foi registrada.

### **Evitar Apenas Cores para Diferenciação**

- Não dependa apenas de cores para indicar que um elemento é clicável. Combine cores com outras pistas visuais, como ícones, texto ou sublinhado, para garantir que usuários com deficiência visual possam identificar elementos clicáveis.

### **Evitar Funções Dependentes de Eventos de Hover ou Foco**

- Elementos clicáveis que dependem apenas do evento **hover** ou **focus** podem ser inacessíveis para usuários de teclado e dispositivos de toque. Sempre certifique-se de que a ação possa ser realizada por clique ou através de navegação por teclado.

### **Estado Desabilitado**

- Quando um botão ou elemento clicável está desabilitado, ele deve ser claramente distinguível do estado ativo, usando estilos visuais como menor opacidade ou cores diferentes. Além disso, desabilitar um botão não deve remover o foco dele para garantir que seja acessível por leitores de tela.

### **Suporte a Leitores de Tela**

- Verifique se leitores de tela conseguem identificar e descrever corretamente os elementos clicáveis. Use rótulos ARIA adequados e teste com ferramentas como o NVDA ou JAWS para garantir a compatibilidade.
