# Portal de Notícias - Projeto de Estudo

## Descrição

Este é um projeto de estudo focado no desenvolvimento de um portal de notícias responsivo utilizando **HTML5** e **CSS3**, com ênfase especial no aprendizado e aplicação prática do **CSS Grid Layout**. O projeto simula um site de notícias de tecnologia chamado "TechNews" com layout moderno e funcional.
https://jupereira25.github.io/PortaldeNoticias/

## Objetivos do Projeto

- **Aprender CSS Grid**: Compreender e aplicar os conceitos fundamentais do CSS Grid Layout
- **Desenvolver Layout Responsivo**: Criar uma interface adaptável e bem estruturada
- **Praticar HTML Semântico**: Utilizar tags HTML5 apropriadas para melhor acessibilidade
- **Implementar Design System**: Criar um sistema de design consistente com variáveis CSS

## Estrutura do Projeto

```
Portal de noticias/
├── assets/
│   ├── icon/          # Ícones SVG (menu, busca, setas)
│   ├── images/        # Imagens das notícias (19 imagens)
│   └── tech-news-logo.svg
├── styles/
│   ├── global.css     # Estilos globais e variáveis CSS
│   ├── utility.css    # Classes utilitárias (Grid, espaçamentos)
│   ├── header.css     # Estilos do cabeçalho
│   ├── sections.css   # Estilos das seções principais
│   └── index.css      # Arquivo principal que importa todos os estilos
└── index.html         # Estrutura HTML principal
```

## Design System

### Cores
- **Primária**: `#60A5FA` (azul claro)
- **Secundária**: `#1D4ED8` (azul escuro)
- **Fundo**: `#0F172A` (azul muito escuro)
- **Texto**: `#F1F5F9` (branco)
- **Bordas**: `#1E293B` (azul escuro)

### Tipografia
- **Família**: Archivo (Google Fonts)
- **Hierarquia**: H1 (24px), H2 (16px), H3 (14px), Texto (16px), Texto pequeno (14px)

## CSS Grid - Foco do Estudo

### 1. **Grid Container Principal**
```css
main {
    display: grid;
    grid-template-columns: 2fr 1.4fr;  /* Layout de 2 colunas com proporções diferentes */
    grid-template-areas: 
        "featured featured"    /* Seção destacada ocupa ambas as colunas */
        "weekly weekly"        /* Seção semanal ocupa ambas as colunas */
        "ai aside";            /* Seção IA e sidebar lado a lado */
}
```

### 2. **Grid Areas**
O projeto utiliza **Grid Areas** para organizar o layout de forma semântica:
- `featured`: Seção principal com notícia em destaque
- `weekly`: Seção "Mais lidas da semana"
- `ai`: Seção de Inteligência Artificial
- `aside`: Barra lateral com anúncios e conteúdo adicional

### 3. **Classes Utilitárias de Grid**
```css
.grid {
    display: grid;
}

.grid-flow-col {
    grid-auto-flow: column;  /* Fluxo automático em coluna */
}

.grid-cols-2 {
    grid-template-columns: 1fr 1fr;  /* 2 colunas de tamanho igual */
}

.gap-16 {
    gap: 16px;  /* Espaçamento entre elementos */
}
```

### 4. **Aplicações Práticas do Grid**

#### Header com Navegação
```html
<nav id="primary" class="grid grid-flow-col">
    <!-- Menu, Logo e Busca distribuídos automaticamente -->
</nav>
```

#### Seção Destacada
```html
<section id="featured" class="grid grid-flow-col gap-16">
    <!-- Notícia principal + grid de 2x2 para notícias menores -->
    <div class="grid grid-cols-2 gap-16">
        <!-- 4 notícias em grid 2x2 -->
    </div>
</section>
```

#### Seção Semanal
```css
#weekly > div {
    grid-template-columns: repeat(4, 292px);  /* 4 colunas fixas */
}
```

## Layout Responsivo

O projeto utiliza um sistema de grid que se adapta a diferentes tamanhos de tela:
- **Container principal**: Máximo de 1280px com padding lateral
- **Grid responsivo**: Proporções flexíveis usando `fr` units
- **Imagens adaptáveis**: `max-width: 100%` e `object-fit: cover`

## Seções Principais

### 1. **Header**
- Menu de navegação com ícones
- Logo centralizado
- Barra de busca
- Menu secundário com categorias de tecnologia

### 2. **Seção Destacada**
- Notícia principal em destaque
- Grid 2x2 com 4 notícias menores
- Overlay gradiente sobre as imagens

### 3. **Mais Lidas da Semana**
- 4 notícias em linha horizontal
- Tags de categoria posicionadas sobre as imagens

### 4. **Inteligência Artificial**
- Artigos com layout texto + imagem
- Grid de 2 colunas com espaçamento consistente

### 5. **Sidebar**
- Área de anúncios
- Seção "Viu isso aqui?" com 5 artigos

## Tecnologias Utilizadas

- **HTML5**: Estrutura semântica
- **CSS3**: Estilos e layout
- **CSS Grid**: Sistema de layout principal
- **CSS Variables**: Sistema de design consistente
- **Google Fonts**: Tipografia Archivo

## Conceitos de Grid Aprendidos

1. **Grid Container vs Grid Items**
2. **Grid Template Areas** para layouts complexos
3. **Grid Auto Flow** para distribuição automática
4. **Fractional Units (fr)** para proporções flexíveis
5. **Grid Gap** para espaçamento consistente
6. **Grid Areas** para organização semântica

## Como Executar

1. Clone ou baixe o projeto
2. Abra o arquivo `index.html` em um navegador moderno
3. Explore o layout e inspecione os elementos para ver o Grid em ação

## 🎓 Aprendizados

Este projeto demonstra como o CSS Grid pode ser usado para:
- Criar layouts complexos de forma simples
- Organizar conteúdo de forma semântica
- Manter consistência visual
- Facilitar a manutenção do código
- Criar interfaces responsivas e modernas

## Próximos Passos

- Implementar responsividade para dispositivos móveis
- Adicionar funcionalidades JavaScript
- Criar sistema de navegação entre páginas
- Implementar sistema de busca funcional
- Adicionar animações e transições

---

**Projeto desenvolvido como material de estudo para aprofundar conhecimentos em CSS Grid Layout e desenvolvimento web moderno.** 
