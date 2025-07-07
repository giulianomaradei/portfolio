# Giuliano Maradei - Portfolio (Vue)

Este é um portfólio pessoal construído com Vue.js, Nuxt.js e Tailwind CSS. É uma conversão 1:1 do projeto React original mantendo exatamente a mesma funcionalidade e aparência.

## Tecnologias Utilizadas

- **Vue.js 3** - Framework JavaScript progressivo
- **Nuxt.js** - Framework full-stack baseado em Vue
- **TypeScript** - Superset tipado do JavaScript
- **Tailwind CSS** - Framework CSS utilitário
- **Lucide Vue** - Ícones para Vue.js

## Características

- ✨ Design moderno e responsivo
- 🎨 Tema dark com esquema de cores retro
- 🚀 Animações suaves e interativas
- 📱 Totalmente responsivo
- 🔧 Formulário de contato funcional
- 🎯 Navegação suave entre seções

## Instalação

1. Clone o repositório
2. Instale as dependências:
```bash
npm install
```

3. Execute em modo de desenvolvimento:
```bash
npm run dev
```

4. Abra [http://localhost:3000](http://localhost:3000) no seu navegador

## Scripts Disponíveis

- `npm run dev` - Inicia o servidor de desenvolvimento
- `npm run build` - Constrói a aplicação para produção
- `npm run generate` - Gera o site estático
- `npm run preview` - Visualiza a versão de produção

## Estrutura do Projeto

```
portfolio/
├── components/          # Componentes Vue
│   ├── Header.vue      # Cabeçalho com navegação
│   ├── Hero.vue        # Seção principal
│   ├── About.vue       # Seção sobre
│   ├── Skills.vue      # Seção de habilidades
│   ├── Projects.vue    # Seção de projetos
│   ├── Contact.vue     # Seção de contato
│   └── Footer.vue      # Rodapé
├── assets/
│   └── css/
│       └── main.css    # Estilos globais
├── public/             # Arquivos estáticos
├── app.vue             # Componente principal
├── nuxt.config.ts      # Configuração do Nuxt
└── tailwind.config.ts  # Configuração do Tailwind
```

## Personalização

### Cores
As cores estão definidas no arquivo `assets/css/main.css` usando variáveis CSS. Você pode modificar:
- `--primary`: Cor principal
- `--background`: Cor de fundo
- `--foreground`: Cor do texto
- E outras variáveis do sistema de design

### Conteúdo
Para personalizar o conteúdo, edite os respectivos componentes Vue:
- Informações pessoais: `components/About.vue`
- Habilidades: `components/Skills.vue`
- Projetos: `components/Projects.vue`
- Contato: `components/Contact.vue`

## Deploy

Para fazer deploy da aplicação:

1. Construa a aplicação:
```bash
npm run build
```

2. O projeto será gerado na pasta `.output/`

3. Você pode hospedar em qualquer plataforma que suporte aplicações Nuxt.js

## Licença

Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

---

Built with ❤️ using Vue.js + TypeScript
