## 📋 To-Do List API
Uma API completa para gerenciamento de tarefas, construída com Node.js, TypeScript e SQLite

🌟 Recursos
✅ CRUD Completo

Criar, ler, atualizar e deletar tarefas
✅ Banco de Dados SQLite

Persistência de dados simples e eficiente
✅ TypeScript

Tipagem estática para maior segurança no código
✅ Arquitetura Organizada

Separação clara entre rotas, controladores e modelos
✅ Pronto para Produção

Configuração de build e scripts otimizados

🛠️ Tecnologias
Tecnologia	Descrição
Node.js	Ambiente de execução JavaScript
TypeScript	Superset tipado do JavaScript
Express	Framework para APIs REST
SQLite	Banco de dados embutido
Jest (opcional)	Framework para testes
🚀 Começando
Pré-requisitos
Node.js 18+

npm ou yarn

Git (opcional)

Instalação
Clone o repositório

bash
git clone https://github.com/seu-usuario/todo-api-ts.git
cd todo-api-ts
Instale as dependências

bash
npm install
Configure o ambiente
Crie um arquivo .env (opcional para configurações adicionais):

env
PORT=3000
Execute o servidor

bash
npm run dev
A API estará disponível em: http://localhost:3000

📚 Documentação da API
Endpoints
Método	Endpoint	Descrição	Body (JSON)
GET	/tasks	Lista todas as tarefas	-
POST	/tasks	Cria nova tarefa	{"title": "string", "completed": boolean}
PUT	/tasks/:id	Atualiza tarefa	{"title": "string", "completed": boolean}
DELETE	/tasks/:id	Remove tarefa	-
Exemplos de Requisição
Criar tarefa:

bash
curl -X POST http://localhost:3000/tasks \
-H "Content-Type: application/json" \
-d '{"title":"Estudar TypeScript","completed":false}'
Listar tarefas:

bash
curl http://localhost:3000/tasks
🏗️ Estrutura do Projeto
todo-api-ts/
├── src/
│   ├── config/          # Configurações do app
│   ├── controllers/     # Lógica das rotas (TaskController.ts)
│   ├── models/          # Definições de dados (Task.ts)
│   ├── routes/          # Rotas da API (taskRoutes.ts)
│   ├── services/        # Lógica de negócio (opcional)
│   ├── utils/           # Utilitários
│   └── server.ts        # Ponto de entrada
├── tests/              # Testes automatizados (opcional)
├── .env.example        # Modelo de variáveis de ambiente
├── .gitignore          # Arquivos ignorados pelo Git
└── tsconfig.json       # Configuração do TypeScript
🧪 Testes (Opcional)
O projeto pode ser extendido com testes usando Jest:

Instale as dependências:

bash
npm install --save-dev jest ts-jest @types/jest
Crie um teste em tests/task.test.ts:

typescript
import request from 'supertest';
import app from '../src/server';

describe('Task API', () => {
  it('should create a new task', async () => {
    const res = await request(app)
      .post('/tasks')
      .send({ title: 'Test Task', completed: false });
    expect(res.statusCode).toEqual(201);
  });
});
Execute os testes:

bash
npm test
🚢 Deploy
Opções recomendadas:
Render (simples e gratuito)

Railway (com banco de dados integrado)

Docker (para containerização)

Exemplo para Render:

Crie um novo serviço Web Service

Conecte ao seu repositório GitHub

Defina o comando de build: npm run build && npm start

🤝 Como Contribuir
Faça um fork do projeto

Crie uma branch (git checkout -b feature/nova-funcionalidade)

Commit suas alterações (git commit -m 'Adiciona nova funcionalidade')

Push para a branch (git push origin feature/nova-funcionalidade)

Abra um Pull Request