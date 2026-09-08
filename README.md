# DSMovie — Catálogo e Interface de Avaliação de Filmes

[![React](https://img.shields.io/badge/React-17.0.2-61DAFB?style=flat-square&logo=react&logoColor=black)](https://react.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-4.4.2-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot-2.6.4-6DB33F?style=flat-square&logo=springboot&logoColor=white)](https://spring.io/projects/spring-boot)
[![Java](https://img.shields.io/badge/Java-17-ED8B00?style=flat-square&logo=openjdk&logoColor=white)](https://www.oracle.com/java/)
[![Bootstrap](https://img.shields.io/badge/Bootstrap-5.1.3-7952B3?style=flat-square&logo=bootstrap&logoColor=white)](https://getbootstrap.com/)
[![Status](https://img.shields.io/badge/Status-Portfolio_Project-blue?style=flat-square)](#)

Aplicação web desenvolvida com front-end SPA em **React 17 + TypeScript** e infraestrutura back-end em **Java 17 + Spring Boot 2.6**, estruturada para catálogo e avaliação de filmes.

---

## 🎯 Objetivo

Criar uma aplicação web para navegação e pontuação de títulos cinematográficos, exercitando a criação de componentes desacoplados no front-end React com TypeScript, rotas dinâmicas e infraestrutura inicial de microsserviço Spring Boot com configuração de CORS e segurança.

---

## ✨ Funcionalidades Implementadas

### Front-end (React + TypeScript)
- **Componente de Pontuação em Estrelas (`MovieStars`)**: Algoritmo visual que avalia a nota numérica do filme e renderiza estrelas fracionadas (cheia, meia ou vazia) via SVGs vetoriais.
- **Card de Exibição (`MovieCard` & `MovieScore`)**: Apresentação de poster, título, contagem de votos e botão para avaliação.
- **Roteamento Dinâmico (`React Router v6`)**: Navegação SPA entre a tela de listagem (`Listing`) e o formulário de avaliação (`Form/:movieId`).
- **Formulário de Avaliação (`Form`)**: Campos para preenchimento de e-mail e seleção de nota (1 a 5).
- **Barra de Navegação e Paginação**: Componentes visuais de cabeçalho (`Navbar`) e controle paginado (`Pagination`).

### Back-end (Spring Boot)
- **Configuração de Segurança e CORS (`SecurityConfig.java`)**: Configuração de filtros de segurança HTTP baseada em `WebSecurityConfigurerAdapter` com suporte a CORS (`CorsConfigurationSource`) habilitado para comunicação com o front-end.
- **Estrutura de Dependências (`pom.xml`)**: Configurado com Spring Data JPA, Spring Security, Spring Web, runtime H2 Database e driver PostgreSQL.

---

## 🏗️ Arquitetura do Projeto

```text
dsmovie/
├── backend/
│   ├── src/main/java/com/devsuperior/dsmovie/
│   │   ├── config/
│   │   │   └── SecurityConfig.java       # Políticas de CORS e liberação de endpoints
│   │   └── DsmovieApplication.java       # Ponto de entrada Spring Boot
│   ├── src/main/resources/
│   │   └── application.properties        # Configurações de ambiente e profiles
│   ├── src/test/java/.../
│   │   └── DsmovieApplicationTests.java  # Teste de inicialização do contexto
│   ├── mvnw / mvnw.cmd                   # Maven Wrapper executável
│   └── pom.xml                           # Gerenciamento de dependências Maven
│
└── frontend/
    ├── src/
    │   ├── assets/img/                   # SVGs vetoriais de estrelas e ícones
    │   ├── components/
    │   │   ├── MovieCard/                # Card com poster e botão de avaliação
    │   │   ├── MovieScore/               # Pontuação numérica e total de votos
    │   │   ├── MovieStars/               # Renderização dinâmica de estrelas
    │   │   ├── Navbar/                   # Barra de navegação com link de contato
    │   │   └── Pagination/               # Componente de controle de páginas
    │   ├── pages/
    │   │   ├── Form/                     # Interface do formulário de avaliação
    │   │   └── Listing/                  # Listagem em grid responsivo com cards
    │   ├── App.tsx                       # Configuração de rotas com React Router v6
    │   └── index.tsx                     # Ponto de montagem da SPA React no DOM
    └── package.json                      # Dependências npm
```

---

## 🚀 Como Executar

### Pré-requisitos
- **Java 17 JDK** instalado
- **Node.js 16+** e **npm** instalados

### 1. Back-end (Spring Boot)
```bash
cd backend

# No Windows PowerShell:
./mvnw.cmd spring-boot:run

# Ou se possuir Maven instalado globalmente:
mvn spring-boot:run
```
O servidor inicializará na porta padrão `8080`.

### 2. Front-end (React)
Em um novo terminal:
```bash
cd frontend

# Instalar dependências
npm install

# Iniciar aplicação em modo de desenvolvimento
npm start
```
Acesse `http://localhost:3000` no navegador.

---

## 🧪 Testes

### Back-end
```bash
cd backend
./mvnw.cmd test
```
*Executa o teste de integridade do contexto Spring Boot (`contextLoads`).*

---

## 📌 Status

- **Maturidade**: Projeto de Portfólio / Estudo Avançado.
- **Competências em evidência**: React 17 com TypeScript, React Router v6, Bootstrap 5, configuração de segurança em Spring Boot com CORS e Maven.

---

## 👨‍💻 Autor

Desenvolvido por **[Wallace Soares](https://github.com/wallacextreme)**.