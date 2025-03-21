### Web API com Nodejs e Express
Dois times foram alocados para trabalhar no projeto do Sr. Atira, e você foi alocado como desenvolvedor backend. E a seguir está o detalhamento dos requisitos do sistema.

#### Casos de uso
- Como usuário, quero cadastrar uma nova tarefa.
- Como usuário, quero excluir uma tarefa existente.
- Como usuário, quero marcar uma tarefa como feita.
- Como usuário, quero ser capaz de visualizar todas as tarefas.

#### Requisitos
- A API deve seguir o padrão de comunicação REST.
- É dispensado o uso de um Sistema Gerenciador de Banco de Dados. Sendo assim, um banco de dados pode ser simulado utilizando as estruturas de dados disponíveis da linguagem escolhida (In-memory).
- Uma tarefa é representada por um: **título**, **descrição** e **status** (concluída ou não)

#### Endpoints
- POST /tasks → Criar uma nova tarefa.
- GET /tasks → Listar todas as tarefas.
- PUT /tasks/:id → Atualizar uma tarefa.
- DELETE /tasks/:id → Remover uma tarefa.
