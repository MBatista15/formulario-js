<div align="center">

  # 📝 Interactive Form — Validação Dinâmica & UX

  **Um formulário interativo focado em validação de dados em tempo real, manipulação avançada de estado no DOM e experiência do usuário.**

  [![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/pt-BR/docs/Web/HTML)
  [![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/pt-BR/docs/Web/CSS)
  [![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript)
  [![Font Awesome](https://img.shields.io/badge/Font_Awesome-339AF0?style=for-the-badge&logo=fontawesome&logoColor=white)](https://fontawesome.com/)
  [![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero-brightgreen?style=for-the-badge)](https://github.com)
  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

  [💻 Ver Demo Online](https://seu-usuario.github.io/form-validation/) · [🐞 Reportar Bug](https://github.com/seu-usuario/form-validation/issues) · [✨ Sugerir Funcionalidade](https://github.com/seu-usuario/form-validation/issues)

</div>

---

## 📋 Sumário
- [Sobre o Projeto](#-sobre-o-projeto)
- [Funcionalidades](#-funcionalidades)
- [Decisões de Engenharia](#-decisões-de-engenharia)
- [Stack Tecnológica](#-stack-tecnológica)
- [Estrutura do Projeto](#-estrutura-do-projeto)
- [Acessibilidade & UX](#-acessibilidade--ux)
- [Autor](#-autor)

---

## 📌 Sobre o Projeto

O **Interactive Form** é um componente de captura e validação de informações desenvolvido com foco em interatividade e validação client-side.

A aplicação impede o envio de dados incorretos, oferecendo respostas visuais imediatas conforme o usuário preenche os campos (nome, e-mail, telefone, senha e mensagem).

> 🎯 **Foco Principal:** Experiência do usuário (UX), sanitização de dados com RegEx, manipulação dinâmica de classes CSS e zero dependência de bibliotecas de validação.

---

## ⚡ Funcionalidades

| Recurso | Detalhes de Implementação |
| :--- | :--- |
| **Validação Real-Time** | Feedback instantâneo dispara no evento `input` sem esperar pela submissão. |
| **Sanitização por RegEx** | Checagem de padrão sintático para e-mail e caracteres numéricos para telefone. |
| **Indicadores Visuais de Estado** | Alternância automática entre bordas/ícones verdes (`.success`) e vermelhos (`.error`). |
| **Placeholder Mensagem Dinâmica** | Atualização do texto de instrução dentro do input ao detectar dados incorretos. |
| **Modal de Confirmação** | Modal nativo de sucesso exibido apenas se todas as validações forem satisfeitas. |
| **Layout Responsivo** | Otimização de visualização para desktop e ocultação inteligente de elementos gráficos em telas menores. |

---

## 🏗️ Decisões de Engenharia

1. **Validação Granular (`input` + `submit`):**
   A validação ocorre tanto de forma reativa durante a digitação (`input`) quanto defensiva antes da submissão (`submit`), prevenindo que o formulário seja enviado com estados de erro não tratados.

2. **Gestão de Estado via CSS Contextual:**
   A lógica JS apenas injeta ou remove as classes `.error` e `.success` nos contêineres `.form-control`. Todo o comportamento visual (cores de borda, cor do placeholder e exibição de ícones) é gerenciado via regras CSS declarativas.

3. **Validação por Padrões (RegEx):**
   Implementação de Expressões Regulares otimizadas para validação de sintaxe de e-mail (`isEmail`) e comprimento flexível para contatos telefônicos (`isPhone`).

---

## 🛠️ Stack Tecnológica

- **HTML5:** Formulários semânticos (`novalidate`), tipos de input adequados (`email`, `tel`, `password`).
- **CSS3:** Estrutura via Flexbox, posicionamento absoluto para ícones, transições suaves de estado e Media Queries.
- **JavaScript (ES6+):** Manipulação de DOM (`querySelector`, `classList`), ouvintes de eventos e expressões regulares.
- **Font Awesome:** Biblioteca de ícones vetoriais integrada via CDN para os indicadores visuais.

---

## 📂 Estrutura do Projeto

```text
form-validation/
├── img/
│   └── bg.png          # Imagem lateral ilustrativa
├── style.css           # Estilização global, estados do formulário e modal
├── script.js           # Expressões regulares e lógica de validação de DOM
├── index.html          # Estrutura semântica da aplicação
└── README.md           # Documentação do projeto
```

---

## ♿ Acessibilidade & UX

- 🎯 Feedback Imediato: Redução de erros de digitação permitindo que o usuário corrija dados antes de submeter o formulário.

- 📱 Otimização Mobile: O layout altera sua estrutura para 100% de largura em telas com largura inferior a 920px.

- 🔐 Validação Segura: Impede comportamentos padrão de atualização da página através do e.preventDefault() até a aprovação de todos os critérios.

## 👤 Autor

Desenvolvido por Matheus Batista.

LinkedIn: [https://www.linkedin.com/in/matheus-batista-857a47236/]

GitHub: @MBatista15
