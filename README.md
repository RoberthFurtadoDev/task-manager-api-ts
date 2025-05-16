📝 To-Do List API com Node.js + TypeScript
Bem-vindo ao projeto To-Do List API! Esta é uma API simples desenvolvida com Node.js, TypeScript e SQLite, que permite gerenciar tarefas (CRUD completo). Ideal para aprender ou mostrar em portfólios.

🚀 Funcionalidades
✔️ Criar uma nova tarefa
✔️ Listar todas as tarefas
✔️ Atualizar uma tarefa existente
✔️ Deletar uma tarefa
✔️ Banco de dados SQLite integrado
✔️ TypeScript para tipagem segura

🛠️ Tecnologias Utilizadas
Node.js (Runtime JavaScript)

TypeScript (Superset tipado do JavaScript)

Express (Framework para APIs REST)

SQLite (Banco de dados leve)

SQLite3 (Driver para conexão com SQLite)

📥 Como Executar o Projeto
Pré-requisitos
Node.js (v18+)

npm ou yarn

Git (opcional)

Passo a Passo
Clone o repositório

bash
git clone https://github.com/seu-usuario/todo-api-node-ts.git
cd todo-api-node-ts
Instale as dependências

bash
npm install
Execute em modo desenvolvimento

bash
npm run dev
O servidor iniciará em: http://localhost:3000

(Opcional) Build para produção

bash
npm run build  # Compila o TypeScript para JS
npm start      # Roda o servidor em produção
🔍 Endpoints da API
Método	Rota	Descrição	Exemplo de Request Body (JSON)
GET	/tasks	Lista todas as tarefas	-
POST	/tasks	Cria uma nova tarefa	{ "title": "Estudar TS", "completed": false }
PUT	/tasks/:id	Atualiza uma tarefa	{ "title": "Estudar Node", "completed": true }
DELETE	/tasks/:id	Deleta uma tarefa	-
📂 Estrutura do Projeto
todo-api-ts/
├── src/
│   ├── database.ts       # Configuração do SQLite
│   ├── models/           # Tipos e interfaces (Task.ts)
│   ├── controllers/      # Lógica das rotas (TaskController.ts)
│   ├── routes/           # Definição das rotas (taskRoutes.ts)
│   └── server.ts         # Ponto de entrada da API
├── tsconfig.json         # Configuração do TypeScript
├── package.json          # Dependências e scripts
└── database.sqlite       # Banco de dados gerado automaticamente
🧪 Testando a API
Use ferramentas como:

Postman

Insomnia

curl (linha de comando)

Exemplo com curl:

bash
# Listar tarefas
curl http://localhost:3000/tasks

# Criar tarefa
curl -X POST http://localhost:3000/tasks -H "Content-Type: application/json" -d '{"title":"Ler documentação", "completed":false}'
🚀 Próximos Passos (Melhorias Possíveis)
Adicionar autenticação (JWT)

Escrever testes automatizados (Jest)

Containerizar com Docker

Integrar um frontend (React/Vue)

📄 Licença
Este projeto está sob a licença MIT.

# task-manager-api-ts
