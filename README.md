# Interface Gráfica - Blogging - React

Este projeto Front-End é uma aplicação web responsiva desenvolvida em React para gerenciar posts. Ela se conecta à [API REST de Posts](https://github.com/andretheodoro/api-post-rest) para criar, editar, listar e excluir publicações, oferecendo funcionalidades como autenticação, autorização e interface amigável.

## Repositório Github

Repositório disponível em:
https://github.com/andretheodoro/api-post-front

## Descrição

Após o sucesso do desenvolvimento da aplicação de blogging dinâmico utilizando a plataforma OutSystems e a implementação do back-end em Node.js, criamos uma interface gráfica robusta, intuitiva e eficiente para esta aplicação. Este desafio focará em desenvolver o front-end, proporcionando uma experiência de usuário excelente tanto para professores(as) quanto para estudantes.

## Objetivo

Desenvolver uma interface gráfica para a aplicação de blogging utilizando React. A aplicação desenvolvida é responsiva, acessível e fácil de usar, permitindo aos docentes e alunos(as) interagir com os diversos endpoints REST já implementados no back-end.

## Tecnologias Utilizadas

- React: Biblioteca para criação de interfaces de usuário.
- React Router: Para navegação entre páginas.
- Axios: Para consumo da API REST.
- React Icons: Ícones para estilização.
- Styled Components: Para estilização baseada em componentes.
- ESLint: Ferramentas de linting e formatação.

## Funcionalidades

- Login e Logout com gerenciamento de autenticação.
- Listagem de posts.
- Leitura de posts.
- Criação, edição e exclusão de posts.
- Interface responsiva para dispositivos móveis.
- Integração com API REST de Posts.

## Instalação e Execução

Siga os passos abaixo para configurar e executar o projeto:

**1. Clone o repositório**

   ```bash
   git clone https://github.com/andretheodoro/api-post-front.git
   cd api-post-front
   ```

**2. Instale as dependências**

   ```bash
   npm install
   ```

**3. Execute o projeto**

  ```bash
  npm run build
  ```
   ```bash
   npm run dev
   ```

**4. Acesse o aplicativo no navegador em http://localhost:5173/**

Observação: Para as funcionalidades desse projetos serem executadas corretamente, o projeto de API deve estar executando em paralelo.

**5. Configuração com Docker**

Este projeto está totalmente containerizado utilizando o Docker:

**5.1. Construa uma imagem Docker:**
  ```bash
  docker build -t post-app
  ```

**5.2. Executa a aplicação como um contêiner Docker, disponibilizando-a no endereço http://localhost:5173:**
  ```bash
  docker run -p 5173:5173 post-app
   ```

## Estrutura Geral do Projeto

```plaintext
src/
├── api/                 # Configuração e serviços da API
│   └── api.ts
├── pages/               # Páginas principais da aplicação
|   ├── /Auth            # Páginas responsáveis por validação de autenticação do usuário (professor)
|   ├── /Header          # Página responsável por renderizer o Header (Cabeçalho) padrão em todas as páginas
├── styles/              # Estilos globais e temas
├── api.ts               # Configuração de Axios e chamadas à API
├── App.tsx              # Arquivo principal do aplicativo
├── main.tsx             # Ponto de entrada da aplicação
├── Dockerfile           # Configurações do Docker
├── package.json         # Dependências e scripts
└── README.md            # Documentação
```

## Guia de Uso da Aplicação

**1. Login**
- Acesse a página de login.

![image](https://github.com/user-attachments/assets/9c8b3928-1a6e-43b5-9677-f90b2257a57f)

- Caso seja um professor, insira suas credenciais.
- Professores serão redirecionados para a página de gerenciamento de posts. Alunos irão para a página de visualização de posts.

**Professor:**

![image](https://github.com/user-attachments/assets/7a306bd2-0f36-45ef-933d-060612f076c3)

**Aluno:**

![image](https://github.com/user-attachments/assets/5efeebc3-8224-4aa7-b4df-930e2caa8962)

**2. Gerenciamento de Posts**

**Criar Post:** Professores podem criar posts preenchendo o formulário na página de criação.

![image](https://github.com/user-attachments/assets/bc540002-729e-49b9-bfb9-563229d4b009)

**Editar Post:** Professores podem atualizar informações de um post existente, clicando no ícone de lápis na página de lista de posts.

![image](https://github.com/user-attachments/assets/26c8f63f-b9be-45c5-989a-a36ead6fddf0)
![image](https://github.com/user-attachments/assets/66bd51f4-359b-4fe7-b435-598de826011f)

**Excluir Post:** Professores podem remover posts irrelevantes, clicando no ícone de lixeira na página de lista de posts.

![image](https://github.com/user-attachments/assets/691cbe11-1f30-4736-954b-e184001f7033)

**3. Visualizar Posts**

Alunos podem visualizar posts listados com detalhes, basta clicar sobre o card do post desejado.

![image](https://github.com/user-attachments/assets/1f39a823-da9c-4516-9abb-7490652c104e)

**4. Busca Posts por Palavra-Chave**

Alunos e Professores podem filtrar/buscar Posts de acordo com Palavras-Chaves desejadas. A busca será realizada através do título e conteúdo.
![image](https://github.com/user-attachments/assets/909a3ae3-4321-4e52-a65a-3f1e2afcc792)
