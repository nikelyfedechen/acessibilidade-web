# Leitor de Telas

Leitores de tela são ferramentas assistivas fundamentais para usuários com deficiência visual, permitindo que o conteúdo de uma página web seja convertido em áudio ou braille. Para garantir que esses usuários tenham uma experiência fluida e completa, os desenvolvedores devem adotar práticas que tornem o conteúdo web compreensível e navegável por leitores de tela.

### **Uso de HTML Semântico**

- Utilizar **elementos HTML semânticos** adequados é a base para a acessibilidade com leitores de tela. Elementos como `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`, e `<aside>` permitem que os leitores de tela identifiquem corretamente a estrutura da página.
- Evite usar `div` ou `span` para estruturar o conteúdo quando existem alternativas semânticas mais apropriadas. Isso melhora a navegação e a compreensão da página pelos leitores de tela.

### **Ordem e Hierarquia de Títulos**

- Organize os **títulos (`<h1>`, `<h2>`, `<h3>`, etc.)** de forma hierárquica, respeitando uma ordem lógica. O `<h1>` deve ser o título principal, seguido por subtítulos em níveis decrescentes (`<h2>`, `<h3>`, etc.).
- A estrutura de títulos permite que usuários de leitores de tela naveguem rapidamente entre seções da página.

### **Atributos ARIA (Accessible Rich Internet Applications)**

- O uso de **atributos ARIA** deve ser feito com cuidado para adicionar informações de acessibilidade quando HTML semântico não for suficiente. Exemplos importantes incluem:
    - **`aria-label`**: Fornece uma descrição para elementos que não possuem texto visível.
    - **`aria-labelledby`**: Associa um elemento a um outro elemento que já contém uma descrição.
    - **`aria-live`**: Indica ao leitor de tela que uma área de conteúdo dinâmico deve ser anunciada quando alterada, como em alertas ou atualizações de chat.
    - **`aria-expanded`**, **`aria-controls`**: Descrevem o estado de elementos interativos, como menus suspensos ou caixas de acordeão.

### **Navegação por Teclado**

- Garantir que toda a interface seja **navegável por teclado** é crucial para a acessibilidade de leitores de tela. Usuários devem ser capazes de usar a tecla `Tab` para mover entre links, botões, campos de formulário e outros elementos interativos.
- Use o atributo **`tabindex`** para controlar a ordem de navegação por teclado. Certifique-se de que essa ordem seja lógica e intuitiva.

### **Rotulação de Formulários**

- Cada campo de formulário deve ter um **rótulo claro e associado** para que leitores de tela possam descrever corretamente o propósito do campo.
    - Use a tag `<label>` com o atributo `for` corretamente associado ao ID do campo de formulário.
    - Exemplo: `<label for="email">Email</label><input type="email" id="email">`.
- Utilize também **`aria-describedby`** para fornecer instruções adicionais ou mensagens de erro.

### **Imagens e Texto Alternativo**

- As **imagens** devem sempre conter um **texto alternativo (alt)** claro e descritivo. Esse texto será lido pelo leitor de tela para descrever a imagem.
- Para imagens complexas, como gráficos, fornecer uma descrição detalhada ao lado ou em um link separado.

### **Elementos Dinâmicos e Feedback ao Usuário**

- Conteúdo dinâmico, como pop-ups, modais, e alertas, deve ser corretamente identificado e descrito para usuários de leitores de tela.
- Use **`aria-live`** para anunciar atualizações importantes ou mensagens em tempo real.
- Garanta que os elementos dinâmicos tenham **foco** ao serem abertos, e que possam ser fechados facilmente com o teclado (geralmente com a tecla `Esc`).

### **Foco Visível e Ciclo de Foco**

- O foco deve ser **claramente visível** para que os usuários saibam qual elemento está ativo no momento. Estilos de foco (como uma borda ou sombra) ajudam a garantir que o elemento em foco seja notado.
- Mantenha um **ciclo de foco lógico**, evitando que os usuários fiquem "presos" em áreas não acessíveis da página.

### **Leitura Correta de Links e Botões**

- Os **links e botões** devem ter rótulos descritivos e explícitos sobre sua função. Frases como "Clique aqui" ou "Saiba mais" devem ser evitadas, pois não fornecem informações contextuais suficientes.
- Adicione rótulos acessíveis usando `aria-label` ou texto dentro do botão/link que descreva sua função claramente.

### **Evitar Conteúdo Invisível a Leitores de Tela**

- Garanta que nenhum conteúdo importante seja inserido apenas através de elementos visualmente ocultos, como `display:none` ou `visibility:hidden`, pois eles não são acessíveis para leitores de tela.
- Use o atributo **`aria-hidden="true"`** para esconder elementos irrelevantes para leitores de tela, como gráficos decorativos ou áreas redundantes.

### **Testes com Leitores de Tela**

- Teste suas páginas com **leitores de tela populares**, como NVDA (Windows), VoiceOver (Mac e iOS) e TalkBack (Android), para garantir que o conteúdo seja acessível e a navegação esteja clara e fluida.
- Além disso, verifique o comportamento em diferentes navegadores, já que alguns leitores de tela podem apresentar variações.

### Links

- [Basic screen reader commands for accessibility testing - TPGi](https://www.tpgi.com/basic-screen-reader-commands-for-accessibility-testing/)
- [Download NVDA](https://www.nvaccess.org/download/)
