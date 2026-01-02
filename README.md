# 🚀 Service Order API – Laravel

API RESTful desenvolvida em **Laravel** para gerenciamento de **Ordens de Serviço**, permitindo o controle de clientes, usuários, técnicos, status, histórico e prazos de atendimento.

O projeto foi criado com foco em **boas práticas de arquitetura**, **segurança**, **manutenibilidade** e **escalabilidade**, simulando um cenário real de sistemas corporativos (ERP / Service Desk).

---

## 🧠 Objetivo do Projeto

Fornecer uma API robusta para:

- Gerenciar **Ordens de Serviço**
- Controlar **usuários e permissões**
- Registrar **histórico de ações**
- Facilitar integração com aplicações **web e mobile**

---

## 🛠️ Tecnologias Utilizadas

- **PHP 8.2**
- **Laravel 10**
- **PostgreSQL**
- **Laravel Sanctum (Auth)**
- **Eloquent ORM**
- **Migrations & Seeders**
- **Form Requests (Validações)**
- **API Resources**
- **Policies (Autorização)**
- **Docker (opcional)**

---

## 🧩 Arquitetura

O projeto segue princípios de **Clean Code** e **separação de responsabilidades**, utilizando:

- Controllers enxutos
- Services para regras de negócio
- Repositories para acesso a dados
- Requests para validação
- Resources para padronização das respostas

```
app/
 ├── Http/
 │   ├── Controllers/
 │   ├── Requests/
 │   ├── Resources/
 ├── Models/
 ├── Policies/
 ├── Services/
 ├── Repositories/
```

---

## 📦 Modelagem de Dados (Entidades)

### 👤 User
- name
- email
- password
- role (admin | technician)

### 🏢 Client
- name
- email
- phone

### 🧾 ServiceOrder
- title
- description
- status (open | in_progress | finished | canceled)
- priority
- due_date
- client_id
- technician_id

### 🕒 ServiceOrderHistory
- service_order_id
- user_id
- action
- description
- created_at

---

## 🔐 Autenticação

A autenticação é feita via **token** utilizando Laravel Sanctum.

### Login
POST /api/login

### Logout
POST /api/logout

### Usuário autenticado
GET /api/me

---

## 👨‍💻 Autor

**Jhoni Regis Souza da Costa**  
Desenvolvedor Full-Stack  
📧 jrscdev@gmail.com  
🔗 https://github.com/jhoni-costa
