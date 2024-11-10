# HTML Semântico

O uso de **HTML semântico** é fundamental para a criação de páginas web acessíveis. Elementos semânticos fornecem significado e estrutura ao conteúdo, permitindo que navegadores, leitores de tela e outras tecnologias assistivas interpretem e apresentem a informação de maneira correta e útil. 

### **O que é HTML Semântico?**

- HTML semântico refere-se ao uso de elementos HTML que têm um significado claro e específico, ao invés de usar apenas `<div>` e `<span>` para agrupar conteúdo.
- Esses elementos ajudam a transmitir a estrutura e o propósito do conteúdo, melhorando a acessibilidade e a usabilidade.

### Atributo `lang` no HTML

O atributo `lang` é utilizado para especificar o idioma principal do conteúdo de uma página web. A implementação correta desse atributo é crucial para garantir que tecnologias assistivas, como leitores de tela, possam interpretar corretamente o idioma e fornecer a melhor experiência para o usuário.

**Por que o `lang` é importante para a acessibilidade?**

1. **Leitores de tela**: O atributo `lang` informa aos leitores de tela qual idioma está sendo utilizado na página. Com isso, essas ferramentas podem ajustar a pronúncia e entonação para que o conteúdo seja lido corretamente. Por exemplo, sem o atributo `lang` ou com um valor incorreto, um leitor de tela pode tentar ler o texto em inglês com um sotaque de outro idioma, tornando o conteúdo difícil ou impossível de entender.
2. **Sistemas de busca e SEO**: Embora não seja diretamente relacionado à acessibilidade, a definição correta do idioma também melhora a indexação de páginas por motores de busca. Isso facilita o acesso ao conteúdo por um público mais amplo.
3. **Consistência na experiência do usuário**: Além dos leitores de tela, outros componentes como tradutores automáticos e assistentes de navegação podem se beneficiar da declaração correta do idioma, proporcionando uma navegação mais eficiente e agradável.

Exemplo de uso:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Exemplo de página acessível</title>
</head>
<body>
    <h1>Bem-vindo ao nosso site!</h1>
    <p>Este é um exemplo de página com o atributo <code>lang</code> corretamente implementado.</p>
</body>
</html>
```

**Alterações de idioma ao longo da página**

Em situações onde diferentes trechos da página utilizam idiomas distintos, é possível aplicar o atributo `lang` a elementos específicos. Isso garante que leitores de tela mudem dinamicamente para o idioma correto ao ler esses trechos.

**Exemplo:**

```html
<p>Este texto está em português, mas aqui está uma palavra em <span lang="en">English</span>.</p>
```

### **Estrutura Lógica da Página**

- Use elementos de estrutura semântica como:
    - `<header>`: Define o cabeçalho de uma página ou seção.
    - `<nav>`: Usado para agrupar links de navegação.
    - `<main>`: Indica o conteúdo principal da página.
    - `<section>`: Define seções temáticas dentro de uma página.
    - `<article>`: Representa um conteúdo independente que pode ser distribuído ou reutilizado.
    - `<aside>`: Contém informações complementares que estão relacionadas ao conteúdo principal.
    - `<footer>`: Define o rodapé de uma página ou seção.
- Essa estrutura ajuda leitores de tela a entenderem a organização e a navegação do conteúdo.

### **Uso Adequado de Títulos**

- Utilize títulos (`<h1>`, `<h2>`, `<h3>`, etc.) de forma hierárquica para organizar o conteúdo.
- O `<h1>` deve ser usado apenas uma vez por página, normalmente para o título principal, seguido de subtítulos com `<h2>`, `<h3>`, etc. Isso facilita a navegação e a compreensão do documento por tecnologias assistivas.

🔗 **Links**

https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/Heading_Elements

https://www.w3schools.com/tags/tag_hn.asp

### **Listas Semânticas**

- Use listas semânticas para agrupar itens relacionados:
    - `<ul>`: Lista não ordenada.
    - `<ol>`: Lista ordenada.
    - `<li>`: Item de lista.
- Isso ajuda a identificar rapidamente a relação entre os itens e a estrutura dos dados.

### **Links e Botões**

- Utilize elementos de link (`<a>`) e botão (`<button>`) adequados para suas respectivas funções, evitando o uso de `<div>` ou `<span>` para esses propósitos.
- Os links devem ter textos descritivos que expliquem claramente seu destino ou ação.

### **Formulários Acessíveis**

- Utilize elementos de formulário semânticos, como `<form>`, `<input>`, `<label>`, `<select>`, `<textarea>`, etc.
- Assegure-se de que cada campo tenha um `<label>` associado, utilizando o atributo `for` para conectar o rótulo ao campo. Isso melhora a acessibilidade e a usabilidade.

### **Códigos de Resposta e Mensagens de Erro**

- Use elementos semânticos para indicar mensagens de erro ou confirmações:
    - `<div role="alert">`: Para mensagens de alerta que precisam ser percebidas imediatamente.
    - **Feedback visual** deve ser fornecido, e deve ser descrito com atributos ARIA, se necessário.

### **Evitar o Uso Excessivo de ARIA**

- Embora os atributos ARIA possam adicionar informações adicionais de acessibilidade, eles não devem ser usados para substituir HTML semântico. O HTML semântico deve ser priorizado sempre que possível.
- Use ARIA somente quando os elementos HTML não puderem transmitir a informação desejada.

🔗 **Links**

https://www.w3.org/TR/html-aria/

https://developer.mozilla.org/pt-BR/docs/Web/Accessibility/ARIA

### **Acessibilidade em Multimídia**

- Use elementos semânticos para incorporar áudio e vídeo, como `<audio>` e `<video>`.
- Sempre forneça **legendas** e **transcrições** para conteúdos multimídia, garantindo que usuários com deficiência auditiva possam acessar as informações.

### **Teste de Acessibilidade**

- Realize testes de acessibilidade em sua página utilizando ferramentas como o Lighthouse, WAVE, ou outras ferramentas de acessibilidade no navegador.
- Verifique se a estrutura semântica está sendo interpretada corretamente por tecnologias assistivas, garantindo que usuários possam navegar e compreender o conteúdo de maneira eficiente.
