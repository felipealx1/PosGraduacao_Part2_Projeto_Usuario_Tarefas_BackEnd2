# PosGraduacao_Part2_Projeto_Usuario_Tarefas_BackEnd2
<body>
    <h1>Sistema de Gerenciamento de Usuários e Tarefas</h1>
    <p>Este é um sistema web desenvolvido em <strong>Java</strong> para gerenciar usuários e tarefas com base nos requisitos descritos. A aplicação utiliza <strong>MongoDB</strong> como banco de dados e implementa uma relação entre usuários e tarefas.</p>

<h2>Funcionalidades</h2>
    <h3>Usuários</h3>
    <ul>
        <li>Criar, visualizar, atualizar e excluir usuários.</li>
        <li><strong>Soft Delete:</strong> Os usuários excluídos não são removidos permanentemente, mas marcados como excluídos.</li>
    </ul>
    <h3>Tarefas</h3>
    <ul>
        <li>Criar, visualizar, atualizar e excluir tarefas.</li>
        <li><strong>Soft Delete:</strong> As tarefas excluídas não são removidas permanentemente, mas marcadas como excluídas.</li>
        <li>As tarefas possuem prioridade (<code>baixa</code>, <code>média</code> ou <code>alta</code>).</li>
        <li>Buscar tarefas pelo título.</li>
        <li>Buscar tarefas por intervalo de datas.</li>
        <li>Buscar todas as tarefas excluídas.</li>
        <li>Buscar todas as tarefas de um usuário, incluindo as excluídas.</li>
    </ul>

<h2>Estrutura do Banco de Dados</h2>
    <h3>Usuário</h3>
    <ul>
        <li><strong>id:</strong> Identificador único</li>
        <li><strong>nome:</strong> Nome completo do usuário</li>
        <li><strong>email:</strong> Endereço de email único do usuário</li>
        <li><strong>telefone:</strong> Número de telefone</li>
    </ul>
    <h3>Tarefa</h3>
    <ul>
        <li><strong>id:</strong> Identificador único</li>
        <li><strong>titulo:</strong> Título da tarefa</li>
        <li><strong>descricao:</strong> Descrição detalhada da tarefa</li>
        <li><strong>data_criacao:</strong> Data e hora de criação da tarefa</li>
        <li><strong>prioridade:</strong> Prioridade (<code>baixa</code>, <code>média</code>, ou <code>alta</code>)</li>
        <li><strong>usuario_id:</strong> Referência ao <code>id</code> do usuário que criou a tarefa</li>
    </ul>

<h2>Requisitos Implementados</h2>
    <ul>
        <li><strong>Validação:</strong> As entidades <code>Usuário</code> e <code>Tarefa</code> possuem validações para garantir a consistência dos dados.</li>
        <li><strong>CRUD com Soft Delete:</strong> Operações de criar, visualizar, atualizar e excluir são implementadas para ambas as entidades, utilizando <strong>Soft Delete</strong>.</li>
        <li><strong>Filtros Avançados:</strong>
            <ul>
                <li>Busca de todas as tarefas excluídas.</li>
                <li>Busca de todas as tarefas excluídas de um usuário específico.</li>
                <li>Busca de tarefas por título.</li>
                <li>Busca de tarefas por intervalo de datas.</li>
            </ul>
        </li>
    </ul>

<h2>Pré-requisitos</h2>
    <ul>
        <li><strong>Java JDK:</strong> Versão 11 ou superior</li>
        <li><strong>MongoDB:</strong> Local ou em nuvem</li>
        <li>Um cliente REST (ex.: Postman, Insomnia) para testar as rotas</li>
    </ul>
<h2>Endpoints Disponíveis</h2>
<h3>Usuários</h3>
<ul>
<li>
<code>POST /usuarios</code> - Criar um novo usuário.
<div>
<img src="Criar Usuário.png" alt="POST /usuarios Request Example">
</div>
</li>
<li>
<code>GET /usuarios</code> - Listar todos os usuários.
<div>
<img src="Visualizar Usuarios.png" alt="GET /usuarios Response Example">
</div>
</li>
<li>
<code>GET /usuarios/:id</code> - Obter detalhes de um usuário específico.
</li>
<li>
<code>PUT /usuarios/:id</code> - Atualizar informações de um usuário.
<div>
<img src="Atualizar Usuario.png" alt="PUT /usuarios/:id Request Example">
</div>
</li>
<li>
<code>DELETE /usuarios/:id</code> - Excluir um usuário (Soft Delete).
</li>
</ul>

<h3>Tarefas</h3>
    <ul>
        <li>
            <code>POST /tarefas</code> - Criar uma nova tarefa.
            <div>
                <img src="Criar Tarefas.png">
            </div>
        </li>
        <li>
            <code>GET /tarefas</code> - Listar todas as tarefas.
            <div>
                <img src="Listar Tarefas.png" alt="GET /tarefas Response Example">
            </div>
        </li>
        <li>
            <code>GET /tarefas/deletadas</code> - Listar todas as tarefas excluídas.
            <div>
                <img src="Visualizar Tarefas Deletadas.png" alt="GET /tarefas/deletadas Response Example">
            </div>
        </li>
      
 <li>
            <code>GET /tarefas/titulo/:titulo</code> - Buscar tarefas por título.
            <div>
                <img src="Visualizar Tarefas por Titulo.png" alt="GET /tarefas/titulo/:titulo Response Example">
            </div>
        </li>
        <li>
            <code>GET /tarefas/data</code> - Buscar tarefas por intervalo de datas.
            <div>
                <img src="Visualizar Tarefas por Data.png" alt="GET /tarefas/data Response Example">
            </div>
        </li>
        <li>
            <code>PUT /tarefas/:id</code> - Atualizar informações de uma tarefa.
            <div>
                <img src="Atualizar Tarefa.png" alt="PUT /tarefas/:id Request Example">
            </div>
        </li>
        <li>
            <code>DELETE /tarefas/:id</code> - Excluir uma tarefa (Soft Delete).
            <div>
                <img src="Deletar Tarefas.png" alt="DELETE /tarefas/:id Request Example">
            </div>
        </li>
    </ul>
    <h2>Tecnologias Utilizadas</h2>
    <ul>
        <li><strong>Java</strong> - Linguagem principal para desenvolvimento do backend.</li>
        <li><strong>Spring Boot</strong> - Framework para criação de APIs RESTful.</li>
        <li><strong>MongoDB</strong> - Banco de dados NoSQL.</li>
        <li><strong>Maven</strong> - Gerenciador de dependências.</li>
    </ul>