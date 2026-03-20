# 🛒 TICommerce

**Repositório da atividade 3 da Trilha Full-Stack do Programa TIC-HUB-12**

Uma aplicação web moderna e responsiva para compra de consoles, games e acessórios de tecnologia, desenvolvida com Vue 3, TypeScript e Vite.

## ✨ Funcionalidades

- 🎮 Catálogo de produtos com filtros
- 🛒 Carrinho de compras funcional
- 💰 Cálculo automático de descontos
- 🎯 Design responsivo e moderno
- ⚡ Performance otimizada com Vite
- 🎨 Interface intuitiva e atrativa

## 🛠️ Tecnologias Utilizadas

- **Vue 3** - Framework progressivo
- **TypeScript** - Type safety
- **Vite** - Build tool e dev server
- **Vue Router** - Roteamento
- **Pinia** - State management (estruturado para escalabilidade)
- **ESLint** - Linting e qualidade de código

## 📋 Pré-requisitos

- Node.js (v16 ou superior)
- npm ou yarn

## 🚀 Instalação e Setup

### 1. Clone o repositório

```bash
git clone https://github.com/leomatiazzz/tic-hub-12-atv2.git
cd tic-hub-12-atv2
```

### 2. Instale as dependências

```bash
npm install
```

### 3. Execute o servidor de desenvolvimento

```bash
npm run dev
```

A aplicação estará disponível em `http://localhost:5173`

## 📦 Scripts Disponíveis

### Desenvolvimento

```bash
npm run dev
```

Inicia o servidor de desenvolvimento com hot-reload.

### Build para Produção

```bash
npm run build
```

Compila e otimiza o projeto para produção.

### Linting

```bash
npm run lint
```

Verifica a qualidade do código com ESLint.

### Formatação de Código

```bash
npm run format
```

Formata o código automaticamente.

## 📁 Estrutura do Projeto

```
src/
├── components/        # Componentes reutilizáveis
│   ├── card/         # Cards de produtos
│   ├── cart/         # Componentes do carrinho
│   ├── icons/        # Ícones SVG
│   └── NavBar.vue    # Barra de navegação
├── views/            # Páginas da aplicação
│   ├── HomeView.vue  # Página inicial
│   └── AboutView.vue # Página sobre
├── model/            # Modelos de dados
├── enum/             # Enumerações
├── mock/             # Dados mockados
├── utils/            # Utilitários
├── router/           # Configuração de rotas
├── stores/           # State management (Pinia)
├── assets/           # Estilos e imagens
└── App.vue           # Componente raiz
```

## 🎯 Funcionalidades Principais

### Página Inicial

- Banner com apresentação da loja
- Catálogo de produtos em grid responsivo
- Botão de adicionar ao carrinho em cada produto
- Exibição de descontos e frete grátis

### Carrinho de Compras

- Visualização de itens adicionados
- Ajuste de quantidades
- Cálculo automático de totais e descontos
- Remoção de itens

### Página Sobre

- Informações do desenvolvedor
- Links para redes sociais (GitHub, LinkedIn, Instagram)

## 🎨 Design e Estilos

O projeto utiliza um design moderno com:

- **Paleta de cores**: Gradientes roxo/azul vibrantes
- **Tema escuro**: Interface dark mode para reduzir fadiga visual
- **Responsividade**: Adaptado para desktop, tablet e mobile
- **Animações**: Transições suaves e efeitos hover

## 👤 Autor

**Léo Matias** - Desenvolvedor Full Stack

### Conecte-se comigo:

- 🔗 [GitHub](https://github.com/leomatiazzz)
- 💼 [LinkedIn](https://www.linkedin.com/in/leomatias/)
- 📷 [Instagram](https://www.instagram.com/leomvtias)
