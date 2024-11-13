# 🤖 VIC AI - Assistente Virtual de Ensino
> Projeto desenvolvido para auxiliar alunos e professores no processo de aprendizagem

<div align="center">

![VIC AI Logo](frontend/assets/images/logo.svg)

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![NodeJS](https://img.shields.io/badge/Node.js-43853D?style=flat&logo=node.js&logoColor=white)](https://nodejs.org/)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat&logo=openai&logoColor=white)](https://openai.com)
</div>

## 📋 Índice

- [🤖 VIC AI - Assistente Virtual de Ensino](#-vic-ai---assistente-virtual-de-ensino)
  - [📋 Índice](#-índice)
  - [📖 Sobre](#-sobre)
    - [Objetivos](#objetivos)
  - [🚀 Tecnologias](#-tecnologias)
  - [💡 Funcionalidades](#-funcionalidades)
  - [⚙️ Instalação](#️-instalação)
  - [🎮 Como Usar](#-como-usar)
  - [📁 Estrutura do Projeto](#-estrutura-do-projeto)
  - [📌 API Reference](#-api-reference)
  - [🤝 Contribuição](#-contribuição)
  - [✍️ Autores](#️-autores)
  - [📞 Contato](#-contato)
  - [📄 Licença](#-licença)

## 📖 Sobre

O VIC AI é um assistente virtual desenvolvido para apoiar o processo de ensino-aprendizagem no Colégio Victorino. Utilizando tecnologias modernas de Inteligência Artificial, o projeto visa facilitar a interação entre alunos e conteúdo educacional, oferecendo suporte personalizado e respostas em tempo real.

### Objetivos
- Auxiliar estudantes em suas dúvidas
- Fornecer material complementar
- Criar um ambiente interativo de aprendizagem
- Facilitar o acesso à informação educacional

## 🚀 Tecnologias

Este projeto foi desenvolvido utilizando:

- **Frontend**
  - HTML5
  - CSS3
  - JavaScript (Vanilla)

- **Backend**
  - Node.js
  - APIs de IA (OpenAI, Google Gemini, Claude)

## 💡 Funcionalidades

- 💬 Chat interativo em tempo real
- 📚 Acesso a conteúdo educacional
- 🎥 Biblioteca de vídeos didáticos
- 🏗️ Visualização de maquetes 3D
- 🤖 Integração com múltiplas IAs
- 📱 Interface responsiva

## ⚙️ Instalação

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/vic-ai.git

# Entre no diretório
cd vic-ai

# Instale as dependências
npm install

# Configure as variáveis de ambiente
cp .env.example .env
```

## 🎮 Como Usar

```bash
# Inicie o servidor
npm start

# Acesse no navegador
http://localhost:3000
```

## 📁 Estrutura do Projeto

```plaintext
vic-ai/
├── frontend/
│   ├── index.html
│   ├── assets/
│   ├── styles/
│   └── scripts/
├── backend/
│   ├── server.js
│   ├── routes/
│   ├── controllers/
│   ├── services/
│   └── config/
└── package.json
```

## 📌 API Reference

```http
POST /api/chat
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `message` | `string` | **Required**. Mensagem do usuário |

## 🤝 Contribuição

1. Fork o projeto
2. Crie sua Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a Branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## ✍️ Autores

- **Professor André Ricardo**
  - E-mail: andre.ricardo@colegiovictorino.com.br
  - Turma: 2º C Ensino Médio Técnico em Informática
  - Escola: Colégio Victorino

## 📞 Contato

Colégio Victorino:
- Website: [www.colegiovictorino.com.br](http://www.colegiovictorino.com.br)
- Email: contato@colegiovictorino.com.br
- Telefone: (11) 2025-5680

## 📄 Licença

Este projeto está sob a licença MIT - veja o arquivo [LICENSE.md](LICENSE.md) para mais detalhes.

---

<div align="center">
Desenvolvido com ❤️ por alunos 2º C do Colégio Victorino
</div>

---

**Nota:** Este projeto é uma iniciativa educacional e está em constante desenvolvimento. Sugestões e contribuições são sempre bem-vindas!