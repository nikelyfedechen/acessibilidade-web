# Formulários

Formulários são um componente essencial na web, utilizados para coletar informações e interagir com os usuários. No entanto, eles podem representar um desafio significativo para pessoas com deficiência se não forem projetados e desenvolvidos corretamente. Garantir que os formulários sejam acessíveis é crucial para permitir que todos os usuários interajam com eles de maneira eficiente e sem barreiras.

### 1. Rótulos Claros e Associados

Cada campo de um formulário deve ser identificado claramente por um rótulo (`label`). Isso garante que o propósito de cada campo seja entendido corretamente por todos os usuários, incluindo aqueles que dependem de tecnologias assistivas como leitores de tela.

- Sempre utilize o elemento `<label>` para associar rótulos aos campos de formulário usando o atributo `for`, que deve corresponder ao valor do atributo `id` do campo.
- Evite usar placeholders como substitutos de rótulos. Eles podem desaparecer quando o usuário começa a digitar e não são suficientemente descritivos para algumas tecnologias assistivas.

Exemplo:

```html
<label for="email">E-mail:</label>
<input type="email" id="email" name="email">
```

### 2. Uso Adequado de Mensagens de Erro

Mensagens de erro são críticas para uma boa experiência de acessibilidade. Elas devem ser visíveis, claras e descritivas, informando ao usuário o que precisa ser corrigido e por quê.

- Utilize o atributo `aria-describedby` para associar uma mensagem de erro a um campo específico. Isso permite que tecnologias assistivas anunciem a mensagem de erro no momento certo.
- Garanta que as mensagens de erro tenham contraste suficiente para serem vistas por todos.

Exemplo:

```html
<label for="username">Nome de usuário:</label>
<input type="text" id="username" name="username" aria-describedby="username-error">
<span id="username-error" class="error">O nome de usuário é obrigatório.</span>
```

### 3. Campos de Formulário de Navegação Fácil

Certifique-se de que todos os campos de formulário possam ser acessados e preenchidos facilmente apenas com o uso do teclado. Isso é essencial para usuários com mobilidade reduzida.

- Utilize uma ordem lógica de navegação, que geralmente segue a sequência em que os campos aparecem visualmente na página.
- O uso adequado do atributo `tabindex` pode melhorar a navegação. Defina `tabindex="0"` para os elementos que devem ser focados e evite valores positivos, que podem interferir na ordem natural de navegação.

### 4. Botões de Envio Acessíveis

Botões de envio e outros controles de formulário devem ser claramente identificáveis e acessíveis para todos os usuários. Certifique-se de que esses elementos tenham:

- **Texto visível e descritivo**: Use texto claro como "Enviar" ou "Enviar formulário" em vez de ícones sem texto ou comandos vagos.
- **Área de clique adequada**: O botão deve ser grande o suficiente para ser clicado facilmente, especialmente em dispositivos móveis.

Exemplo:

```html
<button type="submit">Enviar</button>
```

### 5. Instruções e Textos de Ajuda

Forneça instruções claras e concisas sobre como preencher os campos do formulário. Textos explicativos adicionais podem ajudar os usuários a entender o que é necessário em cada campo.

- Utilize o atributo `aria-describedby` para associar instruções a campos específicos.
- Instruções adicionais devem ser visíveis ou fáceis de acessar para todos, evitando informações ocultas que dependam exclusivamente de interações com o mouse.

Exemplo:

```html
<label for="password">Senha:</label>
<input type="password" id="password" aria-describedby="password-help">
<span id="password-help">Sua senha deve ter ao menos 8 caracteres, incluindo uma letra maiúscula e um número.</span>
```

### 6. Feedback Visual Adequado

Formulários devem oferecer feedback visual claro para indicar estados de interação, como quando um campo está ativo ou contém um erro.

- Utilize cores e estilos que proporcionem um bom contraste para ajudar usuários com deficiência visual ou daltonismo a distinguir estados de foco ou erro.
- Além da cor, utilize outros indicativos como ícones ou texto para informar o estado de erro.

### 7. Validação de Formulários Inclusiva

Evite validações de formulário que dependam exclusivamente de mudanças visuais. Usuários com deficiências visuais ou cognitivas podem não perceber essas mudanças. Em vez disso:

- Informe o usuário sobre erros de maneira descritiva e audível (para leitores de tela).
- Utilize validações do lado do cliente e do lado do servidor para garantir que todos os erros sejam capturados e comunicados corretamente.

Exemplo:

```html
<label for="phone">Telefone:</label>
<input type="tel" id="phone" aria-describedby="phone-error">
<span id="phone-error" class="error" role="alert">Insira um número de telefone válido.</span>
```
