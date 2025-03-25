### Web API com Nodejs e Express
Dois times foram alocados para trabalhar no projeto do Sr. Atira, e você foi alocado como desenvolvedor backend. E a seguir está o detalhamento dos requisitos do sistema.

#### Casos de uso
- Como usuário, quero cadastrar uma nova tarefa.
- Como usuário, quero excluir uma tarefa existente.
- Como usuário, quero marcar uma tarefa como concluída.
- Como usuário, quero marcar um tarefa como não concluída.
- Como usuário, quero ser capaz de visualizar todas as tarefas.

#### Requisitos
- A API deve seguir o padrão de comunicação REST.
- A API deve ser desenvolvida em Node.js e Express.js. (Permitido o uso de typescript).
- É dispensado o uso de um Sistema Gerenciador de Banco de Dados. Sendo assim, um banco de dados pode ser simulado utilizando as estruturas de dados disponíveis da linguagem escolhida (In-memory).
- Uma tarefa é composta por um: **título**, **descrição** e **status** (concluída ou não)
- É permitido incrementar o projeto e ser criativo(a), adicionando funcionalidades como filtros... Desde que os requisitos mínimos sejam atendidos.

#### Endpoints
- POST /tasks → Criar uma nova tarefa.
- GET /tasks → Listar todas as tarefas.
- PUT /tasks/:id → Atualizar uma tarefa.
- PATCH /tasks/:id → Alterar o status de um tarefa.
- DELETE /tasks/:id → Remover uma tarefa.
