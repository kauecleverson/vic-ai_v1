# Documentação  

```plaintext
vic-ai/                      # Diretório raiz do projeto
```

1. **Frontend /**
Principal diretório que contém todos os arquivos relacionados à interface do usuário.

   - **index.html**
     - Arquivo HTML principal
     - Ponto de entrada da aplicação
     - Estrutura base da página
     - Links para CSS e scripts

   - **assets /**
     - Arquivos estáticos
     - **images /** -> Imagens, logos, ícones
     - **fonts /** -> Fontes personalizadas
     - **icons /** -> Ícones SVG ou outros formatos
     - **media /** -> Arquivos de mídia (vídeos, áudios)

   - **styles /**
     - Arquivos CSS da aplicação
     - **main.css** -> Estilos globais
     - **chat.css** -> Estilos específicos do chat
     - **sidebar.css** -> Estilos da barra lateral
     - **components/** -> Estilos de componentes reutilizáveis

   - **scripts /**
     - Arquivos JavaScript do frontend
     - **main.js** -> Inicialização e configurações
     - **chat.js** -> Lógica do chat
     - **api.js** -> Comunicação com backend
     - **utils/** -> Funções utilitárias

2. **Backend /**
Diretório que contém toda a lógica do servidor.

   - **server.js**
     - Arquivo principal do servidor
     - Configuração do servidor HTTP
     - Middleware de CORS
     - Configurações globais

   - **routes /**
     - Definição das rotas da API
     - Roteamento de requisições
     - **api.js** -> Rotas da API
     - **auth.js** -> Rotas de autenticação (se necessário)

   - **controllers /**
     - Lógica de negócios
     - Processamento das requisições
     - **aiController.js** -> Controle das IAs
     - **chatController.js** -> Controle do chat

   - **services /**
     - Serviços externos e integrações
     - Lógica complexa isolada
     - **aiService.js** -> Integração com IAs
     - **authService.js** -> Serviço de autenticação

   - **config /**
     - Configurações do backend
     - Variáveis de ambiente
     - **config.js** -> Configurações gerais
     - **.env** -> Variáveis de ambiente

3. **package.json**
   - Arquivo de configuração do Node.js
   - Dependências do projeto
   - Scripts de execução
   - Informações do projeto

### Benefícios desta Estrutura:

1. **Separação de Responsabilidades**
   - Frontend e backend claramente separados
   - Cada diretório tem uma função específica
   - Facilita manutenção e escalabilidade

2. **Organização**
   - Estrutura intuitiva e fácil de navegar
   - Arquivos relacionados agrupados
   - Reduz conflitos em trabalho em equipe

3. **Modularidade**
   - Componentes independentes
   - Fácil adicionar/remover funcionalidades
   - Reuso de código simplificado

4. **Manutenibilidade**
   - Código organizado e previsível
   - Facilita debugging
   - Documentação implícita pela estrutura

5. **Escalabilidade**
   - Estrutura preparada para crescimento
   - Fácil adicionar novas funcionalidades
   - Suporta complexidade crescente

### Fluxo de Dados:

```plaintext
Cliente -> Frontend (scripts/api.js) 
        -> Backend (routes/api.js) 
        -> Controllers (processamento) 
        -> Services (integração IA) 
        -> Resposta retorna pelo mesmo caminho
```

Esta estrutura segue princípios de clean architecture e permite um desenvolvimento organizado e escalável, mesmo sem o uso de frameworks. Cada camada tem sua responsabilidade específica e se comunica de forma clara com as demais.

Claro! Vou explicar a função de cada arquivo do frontend de forma detalhada:

**1. index.html**
- Arquivo principal que estrutura toda a aplicação
- Define o esqueleto básico do site
- Carrega todos os recursos externos (CSS e JavaScript)
- Organiza a estrutura em header, main e sidebar
- Define os containers principais para o chat e suas funcionalidades

**2. Diretório assets/**
- **images/** -> Armazena todas as imagens do projeto
  - Logo principal
  - Avatares
  - Backgrounds
  - Imagens de conteúdo
- **icons/** -> Ícones utilizados na interface
  - Ícones de navegação
  - Ícones de ações do chat
  - Ícones da sidebar
- **media/** -> Arquivos de mídia
  - Vídeos da sidebar
  - Outros conteúdos multimídia

**3. Diretório styles/**
- **main.css**
  - Define variáveis globais (cores, fontes, tamanhos)
  - Reset de estilos padrão
  - Estilos base da aplicação
  - Layout principal
  - Configurações de responsividade

- **chat.css**
  - Estilos específicos da área do chat
  - Formatação das mensagens
  - Estilos da área de input
  - Botões de ação
  - Animações do chat

- **sidebar.css**
  - Estilos da barra lateral
  - Formatação das seções de vídeos e maquetes
  - Estilos de listas e itens
  - Estados interativos

**4. Diretório scripts/**
- **api.js**
  - Gerencia toda comunicação com o backend
  - Métodos para envio de mensagens
  - Tratamento de respostas
  - Gestão de erros de comunicação
  - Configurações de requisições

- **chat.js**
  - Lógica principal do chat
  - Gerenciamento de mensagens
  - Manipulação do DOM para o chat
  - Controle de eventos do usuário
  - Integração com a API
  - Funcionalidades de scroll e visualização

- **main.js**
  - Ponto de entrada do JavaScript
  - Inicialização da aplicação
  - Configurações globais
  - Carregamento inicial
  - Gestão de temas
  - Inicialização de outros componentes

**Fluxo de Funcionamento:**
1. O usuário acessa a aplicação através do index.html
2. Os estilos são carregados na ordem: main.css, chat.css, sidebar.css
3. Os scripts são carregados na ordem: api.js, chat.js, main.js
4. main.js inicializa a aplicação
5. chat.js gerencia as interações
6. api.js faz a comunicação com o backend

Esta estrutura foi pensada para:
- Manter o código organizado e modular
- Facilitar a manutenção
- Permitir escalabilidade
- Seguir boas práticas de desenvolvimento
- Manter a performance
- Facilitar o trabalho em equipe

Cada arquivo tem uma responsabilidade única e bem definida, seguindo o princípio da responsabilidade única (SOLID), mesmo sem usar frameworks.

## Backend

Vou explicar detalhadamente a estrutura do backend:

**1. server.js**
- Arquivo principal que inicia o servidor Node.js
- Configuração do servidor HTTP
- Gerenciamento de CORS
- Middleware global
- Configuração de rotas base
- Tratamento de erros global
- Inicialização do servidor na porta especificada

**2. Diretório routes/**
- **api.js**
  - Define todas as rotas da API
  - Roteia requisições para os controllers apropriados
  - Validação básica de requisições
  - Gestão de middlewares específicos por rota
  - Organização dos endpoints por funcionalidade

- **auth.js** (se implementado)
  - Rotas de autenticação
  - Login/Logout
  - Registro de usuários
  - Recuperação de senha
  - Validação de tokens

**3. Diretório controllers/**
- **aiController.js**
  - Lógica de negócio para interação com IAs
  - Processamento de mensagens
  - Validação de dados
  - Formatação de respostas
  - Tratamento de erros específicos

- **chatController.js**
  - Gerenciamento de sessões de chat
  - Histórico de conversas
  - Processamento de contexto
  - Formatação de mensagens

**4. Diretório services/**
- **aiService.js**
  - Integração com APIs de IA (GPT, Gemini, Claude)
  - Gerenciamento de chaves de API
  - Formatação de prompts
  - Cache de respostas
  - Tratamento de limites de requisição

- **authService.js** (se implementado)
  - Lógica de autenticação
  - Geração/validação de tokens
  - Criptografia de senhas
  - Gestão de sessões

**5. Diretório config/**
- **config.js**
  - Configurações globais da aplicação
  - Constantes do sistema
  - Configurações de ambiente
  - Parâmetros de APIs

- **.env**
  - Variáveis de ambiente
  - Chaves de API
  - Configurações sensíveis
  - Parâmetros de ambiente (dev/prod)

**Fluxo de Dados:**
1. Requisição chega ao server.js
2. É direcionada para a rota apropriada em routes/
3. Controller recebe e processa a requisição
4. Service executa a lógica de negócio
5. Resposta retorna pelo mesmo caminho

**Benefícios desta Estrutura:**

1. **Separação de Responsabilidades**
- Cada camada tem função específica
- Facilita manutenção
- Código mais organizado
- Melhor testabilidade

2. **Escalabilidade**
- Fácil adicionar novas funcionalidades
- Estrutura preparada para crescimento
- Modular e extensível

3. **Segurança**
- Validações em camadas
- Configurações sensíveis isoladas
- Tratamento adequado de erros
- Proteção contra vulnerabilidades comuns

4. **Performance**
- Cache de respostas
- Otimização de requisições
- Gerenciamento eficiente de recursos
- Processamento assíncrono quando apropriado

5. **Manutenibilidade**
- Código organizado
- Fácil localização de funcionalidades
- Padrões consistentes
- Documentação implícita pela estrutura

Esta arquitetura segue princípios de:
- Clean Architecture
- SOLID
- DRY (Don't Repeat Yourself)
- Separation of Concerns
- Single Responsibility

E permite:
- Fácil implementação de testes
- Integração com diferentes IAs
- Monitoramento e logging
- Escalabilidade horizontal
- Manutenção simplificada
- Trabalho em equipe eficiente

A estrutura é flexível e pode ser expandida conforme necessário, mantendo a organização e clareza do código.