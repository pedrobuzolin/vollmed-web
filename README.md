# VollMed Web

Aplicação web para gerenciamento de uma clínica médica, desenvolvida com **Java e Spring Boot**, utilizando **Thymeleaf** para renderização das páginas no servidor.

O projeto complementa a aplicação backend da VollMed e explora o desenvolvimento de uma aplicação web completa utilizando o ecossistema Spring, incluindo autenticação, persistência de dados, validação, migrations e envio de e-mails.

---

## 🚀 Sobre o projeto

O **VollMed Web** é uma aplicação web voltada para o gerenciamento de uma clínica médica.

Diferentemente de uma API puramente REST, a aplicação utiliza **Spring MVC + Thymeleaf** para processar as requisições no servidor e gerar as páginas HTML dinamicamente.

O projeto foi desenvolvido com foco na prática de conceitos como:

* Desenvolvimento web com Spring Boot
* Spring MVC
* Renderização server-side com Thymeleaf
* Autenticação e autorização
* Persistência com Spring Data JPA
* MySQL
* Validação de dados
* Versionamento do banco de dados com Flyway
* Envio de e-mails
* Organização de aplicações web em camadas

---

## 🛠️ Tecnologias

| Tecnologia                   | Utilização                             |
| ---------------------------- | -------------------------------------- |
| **Java 17**                  | Linguagem principal                    |
| **Spring Boot 3.3.0**        | Framework principal                    |
| **Spring MVC**               | Desenvolvimento da aplicação web       |
| **Thymeleaf**                | Renderização das páginas HTML          |
| **Thymeleaf Layout Dialect** | Reutilização e organização dos layouts |
| **Spring Data JPA**          | Persistência dos dados                 |
| **Hibernate**                | ORM                                    |
| **MySQL**                    | Banco de dados relacional              |
| **Flyway**                   | Migrations do banco de dados           |
| **Spring Security**          | Autenticação e autorização             |
| **Bean Validation**          | Validação dos dados                    |
| **Spring Mail**              | Envio de e-mails                       |
| **Maven**                    | Gerenciamento de dependências e build  |

As dependências estão definidas no `pom.xml` do projeto.

---

## 📌 Funcionalidades

### 👨‍⚕️ Gerenciamento de médicos

A aplicação permite trabalhar com o cadastro e gerenciamento das informações dos médicos da clínica.

### 🧑‍🤝‍🧑 Gerenciamento de pacientes

O sistema também possui funcionalidades relacionadas ao cadastro e gerenciamento de pacientes.

### 📅 Gerenciamento de consultas

A aplicação permite trabalhar com informações relacionadas às consultas médicas, integrando médicos, pacientes e os respectivos agendamentos.

### 🔐 Autenticação e autorização

O acesso à aplicação é protegido utilizando **Spring Security**, permitindo controlar o acesso às funcionalidades de acordo com a autenticação do usuário.

A integração com Thymeleaf também utiliza o módulo `thymeleaf-extras-springsecurity6`, permitindo utilizar informações de segurança diretamente nas páginas HTML.

### ✉️ Envio de e-mails

O projeto utiliza o **Spring Mail** para integração com serviços de envio de e-mails.

### ✅ Validação

Os dados enviados pelos formulários são validados utilizando **Bean Validation**, permitindo impedir o processamento de informações inválidas.

### 🗄️ Persistência

Os dados são persistidos utilizando **Spring Data JPA**, com **Hibernate** como implementação ORM e **MySQL** como banco de dados.

### 🔄 Migrations

O **Flyway** é utilizado para controlar a evolução da estrutura do banco de dados por meio de migrations versionadas.

---

## 🏗️ Arquitetura

A aplicação segue uma organização em camadas baseada no ecossistema Spring:

```text
Browser
   │
   │ HTTP Request
   ▼
Spring MVC
   │
   ▼
Controller
   │
   ▼
Service / Domain
   │
   ▼
Repository
   │
   ▼
JPA / Hibernate
   │
   ▼
MySQL
```

Na renderização das páginas:

```text
Controller
    │
    ▼
Model
    │
    ▼
Thymeleaf
    │
    ▼
HTML
    │
    ▼
Browser
```

Essa abordagem permite separar responsabilidades entre apresentação, regras de negócio e persistência.

---

## 🔐 Segurança

A aplicação utiliza **Spring Security** para proteger as funcionalidades que exigem autenticação.

Além do controle de acesso no backend, o Thymeleaf pode utilizar as informações fornecidas pelo Spring Security para adaptar a interface de acordo com o usuário autenticado.

---

## 🗃️ Banco de dados

O projeto utiliza **MySQL** como banco de dados relacional.

O schema é controlado através do **Flyway**, evitando depender exclusivamente da criação automática das tabelas pela aplicação.

As migrations ficam versionadas junto ao código-fonte, permitindo acompanhar a evolução da estrutura do banco.

---

## ⚙️ Como executar

### Pré-requisitos

Antes de executar o projeto, tenha instalado:

* Java 17
* MySQL
* Git

O projeto possui **Maven Wrapper**, portanto não é necessário instalar o Maven separadamente.

### 1. Clone o repositório

```bash
git clone https://github.com/pedrobuzolin/vollmed-web.git
```

```bash
cd vollmed-web
```

### 2. Configure o banco de dados

Crie um banco MySQL e configure as credenciais utilizadas pela aplicação no arquivo de configuração.

Exemplo:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/vollmed
spring.datasource.username=root
spring.datasource.password=sua_senha
```

> Não utilize credenciais reais no repositório. Para ambientes reais, prefira variáveis de ambiente ou um mecanismo apropriado de gerenciamento de secrets.

### 3. Execute a aplicação

Linux/macOS:

```bash
./mvnw spring-boot:run
```

Windows:

```bash
mvnw.cmd spring-boot:run
```

Após a inicialização, acesse:

```text
http://localhost:8080
```

---

## 🧪 Testes

O projeto utiliza o **Spring Boot Test** para suporte aos testes automatizados.

Para executar os testes:

```bash
./mvnw test
```

No Windows:

```bash
mvnw.cmd test
```

---

## 📚 Conceitos praticados

Entre os principais conceitos trabalhados no projeto estão:

* Java
* Spring Boot
* Spring MVC
* Thymeleaf
* Server-Side Rendering
* Spring Security
* Autenticação
* Autorização
* Spring Data JPA
* Hibernate
* MySQL
* Flyway
* Bean Validation
* Spring Mail
* Maven
* Arquitetura em camadas
* Desenvolvimento de aplicações web

---

## 🎯 Objetivo profissional

Este projeto faz parte do meu portfólio de desenvolvimento **Backend Java**, demonstrando a construção de uma aplicação web utilizando o ecossistema Spring.

Além do desenvolvimento de APIs, o projeto explora uma abordagem **server-side**, utilizando Spring MVC e Thymeleaf para construir a camada web e integrá-la às regras de negócio, persistência, segurança e infraestrutura da aplicação.
