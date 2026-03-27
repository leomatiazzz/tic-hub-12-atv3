# 🛒 TICommerce

Repositório da **Atividade 3** da trilha Full-Stack (TIC-HUB-12): uma loja virtual de tecnologia e games construída com Vue 3 + TypeScript.

## ✅ O que já foi implementado

- Catálogo com 6 produtos (incluindo **Ghost of Yötei**)
- Carrinho funcional com adicionar, remover, limpar e totalização
- Cálculo de desconto por item e economia total no carrinho
- Correção da regra de total para evitar multiplicação duplicada de quantidade
- Integração de **PrimeVue** no projeto
- Uso de componentes PrimeVue no catálogo: **Card** e **Button**
- Configuração de **Tailwind CSS v4**
- Novo card de produto com visual escuro, imagem em fundo branco e hover suave
- Padronização tipográfica com fonte **Quicksand** em toda a aplicação

## 🧰 Tecnologias utilizadas

- Vue 3
- TypeScript
- Vite
- Vue Router
- Pinia
- PrimeVue
- PrimeIcons
- Tailwind CSS v4
- ESLint + Prettier

## 📋 Pré-requisitos

- Node.js `^20.19.0` ou `>=22.12.0`
- npm

## 🚀 Como executar

### 1. Clonar o projeto

```bash
git clone https://github.com/leomatiazzz/tic-hub-12-atv2.git
cd tic-hub-12-atv2
```

### 2. Instalar dependências

```bash
npm install
```

### 3. Rodar em desenvolvimento

```bash
npm run dev
```

Observação: o Vite usa por padrão `http://localhost:5173`, mas pode mudar de porta se ela já estiver em uso.

## 📦 Scripts

```bash
npm run dev        # servidor de desenvolvimento
npm run build      # type-check + build de produção
npm run preview    # pré-visualizar build local
npm run lint       # linting (oxlint + eslint)
npm run format     # formatação com prettier
```

## 📁 Estrutura principal

```text
src/
├── components/
│   ├── card/
│   │   ├── ProductCard.vue
│   │   └── ProductCardPrime.vue
│   └── cart/
├── mock/
│   └── products.mock.ts
├── model/
│   ├── cart.model.ts
│   └── product.model.ts
├── views/
│   ├── HomeView.vue
│   └── AboutView.vue
├── assets/
│   ├── base.css
│   └── main.css
└── main.ts
```

## 🎯 Próximos passos sugeridos

- Migrar dados mockados para API real
- Adicionar autenticação de usuário
- Evoluir o checkout com etapas e pagamento
- Criar painel administrativo de produtos e pedidos

## 👤 Autor

**Léo Matias**

- GitHub: [leomatiazzz](https://github.com/leomatiazzz)
- LinkedIn: [leomatias](https://www.linkedin.com/in/leomatias/)
- Instagram: [@leomvtias](https://www.instagram.com/leomvtias)
