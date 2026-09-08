# DSMovie — Sistema de Avaliação de Filmes

[![React](https://img.shields.io/badge/React-17.0.2-61DAFB?style=flat-square&logo=react&logoColor=black)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-4.4.2-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot-2.6.4-6DB33F?style=flat-square&logo=springboot&logoColor=white)](https://spring.io/projects/spring-boot)
[![Java](https://img.shields.io/badge/Java-17-ED8B00?style=flat-square&logo=openjdk&logoColor=white)](https://www.oracle.com/java/)
[![Bootstrap](https://img.shields.io/badge/Bootstrap-5.1.3-7952B3?style=flat-square&logo=bootstrap&logoColor=white)](https://getbootstrap.com/)
[![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)

Aplicação web full stack para catálogo e avaliação colaborativa de filmes, desenvolvida com front-end SPA em **React + TypeScript** e back-end em **Java + Spring Boot**.

---

## 🎯 Objetivo

O **DSMovie** resolve a necessidade de centralizar a consulta e avaliação pública de obras cinematográficas. O usuário pode navegar por títulos paginados, visualizar médias de notas calculadas dinamicamente com estrelas fracionadas e enviar novas avaliações associadas ao seu endereço de e-mail.

---

## ✨ Principais Funcionalidades

- **Catálogo de Filmes**: Listagem responsiva com paginação e carregamento de cards de filmes.
- **Sistema de Pontuação Visual**: Renderização dinâmica de avaliação em estrelas (cheia, meia ou vazia) de acordo com a pontuação numérica.
- **Formulário de Avaliação**: Interface dedicada para envio de nota (1 a 5) vinculada ao e-mail do avaliador.
- **Segurança e CORS**: Back-end com configuração de segurança (`SecurityConfig`) e liberação de CORS para integração com o cliente React.
- **Navegação SPA**: Roteamento fluído com **React Router v6**.

---

## 🧰 Stack Tecnológica

### Front-end
- **React 17** (Single Page Application baseada em componentes funcionais)
- **TypeScript 4** (Tipagem estática em componentes, rotas e propriedades)
- **React Router DOM v6** (Gerenciamento de rotas e parâmetros de URL)
- **Bootstrap 5 & Custom CSS** (Design responsivo e layout em grid)
- **Testing Library & Jest** (Infraestrutura configurada para testes de UI)

### Back-end
- **Java 17**
- **Spring Boot 2.6.4**
  - `spring-boot-starter-web` (REST APIs)
  - `spring-boot-starter-data-jpa` (Mapeamento Objeto-Relacional e persistência)
  - `spring-boot-starter-security` (Configuração de endpoints e políticas de CORS)
- **Bancos de Dados**:
  - **H2 Database** (Runtime / Ambiente de desenvolvimento e testes locais)
  - **PostgreSQL** (Driver configurado para produção)
- **Maven** (Gerenciamento de dependências e automação de build)

---

## 🏗️ Arquitetura

```text
Cliente (Browser)
   │
   ▼
SPA React (TypeScript + React Router + Bootstrap 5)
   │ [Requisições HTTP / REST API]
   ▼
Spring Boot Application
   │
   ├── SecurityConfig (Filtros CORS e políticas de acesso)
   ├── Controllers / REST Endpoints
   ├── Services (Cálculo de médias e regras de negócio)
   └── Repositories (Spring Data JPA)
         │
         ▼
   Database (H2 em dev / PostgreSQL em prod)
```

---

## 📁 Estrutura do Projeto

```text
dsmovie/
├── backend/
│   ├── src/main/java/com/devsuperior/dsmovie/
│   │   ├── config/
│   │   │   └── SecurityConfig.java       # Configuração de CORS e segurança
│   │   └── DsmovieApplication.java       # Ponto de entrada Spring Boot
│   ├── src/main/resources/
│   │   └── application.properties        # Propriedades de ambiente
│   └── pom.xml                           # Dependências Maven
│
└── frontend/
    ├── src/
    │   ├── assets/img/                   # SVGs de estrelas e navegação
    │   ├── components/
    │   │   ├── MovieCard/                # Card com poster, título e ação
    │   │   ├── MovieScore/               # Exibição numérica e total de votos
    │   │   ├── MovieStars/               # Renderização dinâmica das estrelas
    │   │   ├── Navbar/                   # Barra de navegação com link de contato
    │   │   └── Pagination/               # Controle de paginação anterior/próxima
    │   ├── pages/
    │   │   ├── Form/                     # Página de formulário de avaliação
    │   │   └── Listing/                  # Listagem principal de títulos
    │   ├── App.tsx                       # Definição das rotas com React Router
    │   └── index.tsx                     # Bootstrap do React no DOM
    └── package.json                      # Dependências npm
```

---

## 🚀 Instalação e Execução

### Pré-requisitos
- **Java 17 JDK** instalado
- **Node.js 16+** e **npm** instalados
- **Maven** (opcional, wrapper incluído no projeto)

### 1. Executando o Back-end
```bash
cd backend

# No Windows PowerShell:
mvn spring-boot:run

# Ou utilizando o Maven Wrapper:
./mvnw spring-boot:run
```
O servidor iniciará em `http://localhost:8080`.

### 2. Executando o Front-end
Em outro terminal:
```bash
cd frontend

# Instalar dependências
npm install

# Iniciar servidor de desenvolvimento
npm start
```
A aplicação abrirá no navegador em `http://localhost:3000`.

---

## 🧪 Testes

### Front-end
```bash
cd frontend
npm test -- --watchAll=false
```

### Back-end
```bash
cd backend
mvn test
```

---

## 📌 Status

- **Status**: Concluído / Projeto de Portfólio.
- **Próximos passos**: Integração contínua (CI/CD) e deploy em nuvem (Railway/Render/Vercel).

---

## 👨‍💻 Autor

Desenvolvido por **[Wallace Soares](https://github.com/wallacextreme)**.