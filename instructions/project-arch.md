### 📌 Estrutura do Projeto Node.js

Este projeto segue a arquitetura em camadas, organizando o código de forma modular para facilitar manutenção e escalabilidade.

#### 🏛 Arquitetura do Projeto

A estrutura é baseada nos seguintes componentes:

#### 📂 Repository (Repositório)

O Repository é responsável pelo acesso ao banco de dados. Ele contém métodos específicos para buscar, criar, atualizar e excluir registros, garantindo que essa lógica fique separada das demais camadas.

Responsabilidades:

📌 Comunicação direta com o banco de dados.

📌 Centralizar consultas e operações relacionadas a dados.

📌 Facilitar mudanças no banco sem afetar outras partes do sistema.

#### ⚙ Service (Serviço)

O Service é a camada onde a lógica de negócios acontece. Ele atua como intermediário entre o Repository e o Controller, garantindo que as regras do sistema sejam aplicadas antes da manipulação dos dados.

Responsabilidades:

⚡ Aplicar regras de negócio.

⚡ Processar e validar os dados antes de enviá-los ao Repository.

⚡ Evitar regras de negócio dentro do Controller.

#### 🎯 Controller (Controlador)

O Controller gerencia as requisições e respostas da API. Ele recebe os dados do cliente, chama o Service para processá-los e retorna a resposta apropriada.

Responsabilidades:

🎯 Lidar com as requisições HTTP.

🎯 Delegar a lógica de negócio para o Service.

🎯 Retornar as respostas de forma padronizada.

#### 🌐 Route (Rotas)

A camada de Routes define os endpoints da API e direciona as requisições para os controllers corretos.

Responsabilidades:

🌍 Definir os caminhos da API.

🌍 Direcionar as requisições para o Controller correspondente.

🌍 Aplicar middlewares quando necessário.

#### 🔄 Fluxo de Funcionamento

🟢 O usuário faz uma requisição para um endpoint.

🟢 A Route direciona a requisição para o Controller correspondente.

🟢 O Controller chama o Service para aplicar regras de negócio.

🟢 O Service consulta ou manipula os dados através do Repository.

🟢 O Repository acessa o banco de dados e retorna a informação ao Service.

🟢 O Service retorna os dados processados ao Controller.

🟢 O Controller envia a resposta ao usuário.

Essa estrutura modular facilita a manutenção, tornando o código mais organizado e escalável. 🚀