# Estrutura de Projeto sugerida com Arquitetura MVC adptada.

### 📁 O que é a arquitetura MVC?

A arquitetura MVC significa Model-View-Controller (Modelo-Visão-Controlador) e é uma abordagem para organizar projetos de maneira eficiente, separando responsabilidades. Isso facilita o desenvolvimento, a manutenção e a colaboração em equipe.

Imagine um restaurante:

Model (Modelo): O cardápio — define os pratos disponíveis (dados e regras de negócio).

View (visualização): O prato final — é o produto final que o usuário consome (resposta da API em Json).

Controller (Controlador): O garçom — faz a ponte entre o pedido do cliente e a cozinha (processamento da lógica).

### 📂 Estrutura de pastas usando MVC

```
/src/
│── /models/       # Modelos de dados e lógica de negócios
│── /controllers/  # Lógica para lidar com requisições e respostas, as respostas fazem o papel do View, dispensando um pasta própria.
│── /routes/       # Definição e organização das rotas da aplicação
│── app.js         # Arquivo principal do projeto
│── package.json   # Informações do projeto e dependências
```

### 🔧 Função de cada pasta:

Models: Define a estrutura dos dados, como um modelo de tarefa com título, descrição e status. Aqui, também são tratadas as regras de negócio.

Controllers: Recebe as requisições, processa com base nos Models e retorna a resposta adequada ao cliente (geralmente no formato JSON para APIs RESTful).

Routes: Define os caminhos que a aplicação pode seguir (URLs) e qual Controller deve lidar com cada um deles.

### ✅ Benefícios de usar MVC:

Organização: Código mais estruturado e fácil de entender.

Manutenção facilitada: Alterações localizadas sem afetar todo o projeto.

Reutilização: Componentes podem ser reaproveitados em diferentes partes do sistema.

### 📌 Resumo:

A arquitetura MVC ajuda a manter a organização e a eficiência em projetos Node.js, especialmente para quem está começando ou trabalha em equipe. Dominar essa estrutura é um passo importante para evoluir como desenvolvedor!

---
<a href="./desafio.md">Página anterior</a>
