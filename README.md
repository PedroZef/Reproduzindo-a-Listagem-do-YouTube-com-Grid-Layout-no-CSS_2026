# 📺 Reproduzindo a Listagem do YouTube com Grid Layout no CSS

<p align="center">
  <a href="https://github.com/PedroZef/Reproduzindo-a-Listagem-do-YouTube-com-Grid-Layout-no-CSS_2026"><img src="https://img.shields.io/badge/status-conclu%C3%ADdo-brightgreen?style=flat-square" alt="Status Concluído"></a>
  <a href="https://developer.mozilla.org/pt-BR/docs/Web/HTML"><img src="https://img.shields.io/badge/HTML5-estrutura-e44d26?style=flat-square" alt="HTML5 Estrutura"></a>
  <a href="https://developer.mozilla.org/pt-BR/docs/Web/CSS"><img src="https://img.shields.io/badge/CSS3-grid_layout-1572b6?style=flat-square" alt="CSS3 Grid Layout"></a>
  <a href="https://www.dio.me"><img src="https://img.shields.io/badge/DIO-desafio_de_projeto-8a2be2?style=flat-square" alt="DIO Desafio de Projeto"></a>
</p>

<p align="center">
  <b>Interface Front-End Avançada: Recriação Fiel e de Alta Performance da Página Principal do YouTube BR utilizando HTML5 Semântico, CSS Grid Layout Responsivo e Controle de Estado Interativo 100% Puro (Zero-JS)proposto pela **Digital Innovation One — DIO**.</b>
</p>

---

## 📌 Visão Geral do Projeto

Este projeto consiste no desenvolvimento de uma interface web de alta fidelidade baseada na plataforma **YouTube BR**, desenvolvida como um **Desafio de Projeto da DIO (Digital Innovation One)**.

Como Desenvolvedor **de Tecnologia Full Stack**, o objetivo foi elevar o projeto a um padrão de produção profissional, demonstrando o uso avançado das especificações modernas do **CSS Grid Layout**, **Flexbox**, **Design System parametrizado com CSS Variables** e controle de estado interativo **100% livre de JavaScript** (*Pure CSS Architecture*).

### ✨ Principais Recursos Entregues

- 🎨 **Tema Dinâmico (Modo Escuro / Claro):** Alternância visual instantânea manipulada por estado CSS (*Checkbox Hack*) e variáveis no `:root`.
- 📐 **Grade de Vídeos com CSS Grid Auto-Adaptável:** Disposição fluida e responsiva via `repeat(auto-fill, minmax(280px, 1fr))` sem necessidade de frameworks pesados.
- 🛝 **Carrossel da Barra de Categorias sem JS:** Navegação lateral entre grupos de categorias controlada por botões radio CSS (*Radio Hack*).
- 📱 **Experiência Multi-Device (Mobile-First a Ultra-Wide):** Suporte completo para telas pequenas com barra inferior nativa móvel (*Mobile Bottom Nav*) e telas desktop expandidas.
- ♿ **Acessibilidade Web (WCAG 2.1 AA):** HTML semântico com WAI-ARIA (`role="banner"`, `role="navigation"`, `role="main"`, `aria-label`), navegação total via teclado e foco visível adaptado.
- 💎 **Acabamento Visual de Alta Qualidade:** Logo oficial com tag "BR", avatares dinâmicos, badges "Ao vivo", botões com gradientes modernos e scrollbars personalizadas.

---

## 🔍 Análise Final do Projeto Passo a Passo (para o GitHub)

### 🔹 Passo 1: Estrutura de Arquivos e Otimização de Assets

- **Higienização do Repositório:** Organização rigorosa em diretórios específicos (`css/`, `assets/icons/`, `assets/img/`).
- **Otimização de Carregamento:** Ícones vetoriais em formato SVG leve, reduzindo o tempo de renderização inicial da página.
- **Carregamento Otimizado de Imagens:** Aplicação da diretiva `loading="lazy"` nas thumbnails para maximizar os índices de performance no Google Lighthouse (LCP/FCP).

### 🔹 Passo 2: Arquitetura HTML5 Semântica e Acessibilidade (WCAG 2.1 AA)

- **Marcação Estrutural Padrão W3C:**
  - `<header role="banner">`: Cabeçalho superior contendo busca, ações e avatar.
  - `<aside role="navigation">`: Menu lateral de navegação principal (Sidebar).
  - `<main role="main">`: Container principal de conteúdo.
  - `<nav class="category-bar">`: Barra de filtros de categorias.
  - `<section class="video-section">` e `<article class="video-card">`: Encapsulamento semântico dos vídeos.
  - `<footer class="app-footer">`: Rodapé com direitos autorais.
- **Leitores de Tela e Teclado:** Presença de `aria-label`, `title` e pseudo-estilos de `:focus-visible` em todos os elementos interativos.

### 🔹 Passo 3: Com CSS Grid, Flexbox e Design System

- **Grid de Vídeos Responsivo sem Breakpoints Rígidos:**
  ```css
  .video-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 24px 16px;
  }
  ```
- **Arquitetura de Variáveis CSS (`:root`):** Parametrização completa de cores, fundos, sombras e bordas para garantir flexibilidade e fácil manutenção.

### 🔹 Passo 4: Gestão de Estado 100% Zero-JS (CSS Checkbox & Radio Hacks)

- **Alternância de Tema:** Acionamento via `<input type="checkbox" id="theme-toggle">` oculto. O seletor `#theme-toggle:checked ~ .app-container` redefine as variáveis globais de cor instantaneamente.
- **Navegação no Carrossel:** Controle da posição do container de categorias por meio de seletores `:checked` em botões radio (`#cat-p1`, `#cat-p2`).

### 🔹 Passo 5: UX Responsiva Multi-device e Navegação Mobile

- Ocultamento da sidebar em telas menores e ativação da **Barra de Navegação Inferior Móvel** (estilo aplicativo nativo Android/iOS).
- Transições de hover suaves e animações CSS otimizadas para GPU (`transform`, `opacity`).

### 🔹 Passo 6: Checklist de Publicação no GitHub (Git Quality Gate)

- [X] Sintaxe HTML5 e CSS3 totalmente validadas.
- [X] Ausência de erros no console do navegador (Zero JS = Zero Runtime Errors).
- [X] Teste de acessibilidade por navegação via tecla `TAB`.
- [X] Teste de responsividade em breakpoints móveis (320px), tablets (768px) e desktops (1440px+).

---

## 🚀 Destaques do Desenvolvedor (Zero-JS)

### 1. Alternância de Tema com *CSS Checkbox Hack*

```css
/* Troca global de tema via seletor de irmão sem necessidade de JS */
#theme-toggle:checked ~ .app-container {
    color-scheme: light;
    --bg-primary: #f9f9f9;
    --bg-surface: #ffffff;
    --text-primary: #0f0f0f;
    --text-secondary: #606060;
    --border-color: #e5e5e5;
}
```

### 2. Navegação em Carrossel com *Radio Hack*

```css
/* Transição fluida de chips sem script */
#cat-p1:checked ~ .app-container .category-chips-track {
    transform: translateX(0);
}
#cat-p2:checked ~ .app-container .category-chips-track {
    transform: translateX(-400px);
}
```

---

## 🎨 Arquitetura e Design System

| Token CSS            | Descrição                               | Modo Escuro (Default) | Modo Claro  |
| :------------------- | :---------------------------------------- | :-------------------- | :---------- |
| `--bg-primary`     | Cor do fundo principal da aplicação     | `#0f0f0f`           | `#f9f9f9` |
| `--bg-surface`     | Cor dos elementos de superfície e header | `#0f0f0f`           | `#ffffff` |
| `--text-primary`   | Cor do texto principal                    | `#f1f1f1`           | `#0f0f0f` |
| `--text-secondary` | Cor dos metadados e visualizações       | `#aaaaaa`           | `#606060` |
| `--border-color`   | Bordas e divisores horizontais            | `#272727`           | `#e5e5e5` |
| `--accent-blue`    | Destaque e foco de acessibilidade         | `#065fd4`           | `#065fd4` |

---

## 📁 Estrutura de Arquivos

```
Reproduzindo-a-Listagem-do-YouTube-com-Grid-Layout-no-CSS_2026/
├── formato-geral.png       # Modelo visual dos Badges do Projeto (DIO, HTML5, CSS3, Status)
├── index.html              # Marcação HTML5 Semântica com WAI-ARIA
├── css/
│   └── style.css           # Estilização completa, variáveis, CSS Grid e Temas
├── assets/
│   ├── icons/              # Ícones em formato SVG otimizado
│   └── img/
│       ├── channels/       # Avatares de perfis dos canais
│       └── thumbs/         # Imagens de miniaturas dos vídeos
└── README.md               # Documentação técnica profissional do repositório
```

---

## 🔧 Como Executar o Projeto

Como a aplicação é construída com **HTML5 & CSS3 nativos**, não é necessária nenhuma etapa de instalação de dependências ou build via Node.js.

### Passo a Passo:

1. **Clonar o Repositório:**

   ```bash
   git clone https://github.com/PedroZef/Reproduzindo-a-Listagem-do-YouTube-com-Grid-Layout-no-CSS_2026.git
   ```
2. **Acessar a Pasta do Projeto:**

   ```bash
   cd Reproduzindo-a-Listagem-do-YouTube-com-Grid-Layout-no-CSS_2026
   ```
3. **Executar no Navegador:**

   - Abra o arquivo `index.html` diretamente em seu navegador web favorito (Chrome, Edge, Firefox, Safari) ou utilize a extensão **Live Server** no VS Code.

---

## 🛠️ Passo a Passo para Envio das Alterações ao GitHub

Para atualizar e enviar o projeto finalizado ao repositório remoto no GitHub:

```bash
# 1. Verificar os arquivos modificados
git status

# 2. Adicionar as alterações ao staging
git add .

# 3. Criar o commit padronizado
git commit -m "docs: simplifica cabeçalho do README.md de conjunto unico de badges no padrao"

# 4. Enviar para a branch principal no GitHub
git push origin main
```

---

## 👤 Autor

<table border="0">
  <tr>
    <td align="center" width="120">
      <img src="https://github.com/PedroZef.png" width="100px;" alt="Pedro Zeferino da Silva"/><br />
      <b>Pedro Zeferino</b>
    </td>
    <td>
      <b>Pedro Zeferino da Silva</b><br />
      <i>Desenvolvedor de Software Full Stack & Web</i><br /><br />
      Projeto desenvolvido como Desafio de Projeto na <b>DIO (Digital Innovation One)</b> para demonstrar domínio prático em layout responsivo avançado com CSS Grid, HTML semântico e boas práticas de arquitetura front-end.<br /><br />
      📫 <b>Entre em contato:</b><br />
      - 🌐 <b>GitHub:</b> <a href="https://github.com/PedroZef">@PedroZef</a><br />
      - 💼 <b>LinkedIn:</b> <a href="https://linkedin.com/in/pedro-zeferino">Pedro Zeferino da Silva</a>
    </td>
  </tr>
</table>

---

<div align="center">
  <sub>Desenvolvido com 💖 e dedicação por <b>Pedro Zeferino da Silva</b> • 2026</sub>
</div>
