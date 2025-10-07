# Sistema de Tarefas com Flask

Este projeto é um **sistema de gerenciamento de tarefas** desenvolvido em Python com **Flask**, **SQLite** e **SQLAlchemy**. Ele permite que usuários se cadastrem, façam login e gerenciem suas próprias tarefas.

## Objetivos do Projeto

- Introduzir a estrutura de um projeto Flask.
- Configurar Flask, SQLite e SQLAlchemy.
- Implementar cadastro e autenticação de usuários.
- Criar CRUD completo para gerenciamento de tarefas.

## Pré-requisitos

Antes de começar, verifique se você tem instalado:

- Python 3.8 ou superior
- pip
- (Opcional) ambiente virtual `venv`

## Instalação

1. **Clone o repositório**

```bash
git clone https://github.com/seu-usuario/projeto_tarefas.git
cd projeto_tarefas
```

## Crie e ative um ambiente virtual (opcional, mas recomendado)
```bash
python -m venv venv
```

### Windows
```bash
venv\Scripts\activate
```

### Linux/macOS
```bash
source venv/bin/activate
```

## Instale as dependências
```bash
pip install -r requirements.txt
```

O arquivo requirements.txt deve conter pelo menos:
```bash
Flask
Flask-SQLAlchemy
Flask-Login
Werkzeug
```

## Funcionalidades

### Cadastro de Usuários
- Rota ```/register ```(GET/POST)
- Senha armazenada com hash (```generate_password_hash```)
- Validação de e-mail único

### Login e Autenticação
- Rota ```/login``` e ```bash /logout ```bash
- Gerenciamento de sessão com Flask-Login
- Proteção de rotas privadas com @login_required

### CRUD de Tarefas
- Rota ```/tasks``` para listar tarefas do usuário logado
- Rota ```/add_task``` para adicionar tarefas
- Rota ```/update_task/<id>``` para atualizar status
- Rota ```/delete_task/<id>``` para excluir tarefas
- Templates dinâmicos para interface

## Executando o Projeto

No terminal, com o ambiente virtual ativado:
```bash
python app.py
```
Acesse no navegador:
```bash
http://127.0.0.1:5000/
```

## Testes
- Cadastre usuários e verifique no banco database.db.
- Faça login e logout para testar autenticação.
- Adicione, atualize e exclua tarefas para testar o CRUD.
