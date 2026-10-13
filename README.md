# Testes de API com Newman & GitHub Actions

Projeto de portfólio focado em **automação de testes de API REST** utilizando **Postman**, **Newman** e **GitHub Actions**.

## 🎯 Objetivo

Demonstrar, de forma prática, conhecimentos de QA aplicados à automação de APIs, incluindo criação de cenários positivos e negativos, validações de contrato, payload, status HTTP e execução automatizada em pipeline de CI/CD.

## 🧪 O que este projeto demonstra

- Automação de testes de API REST com Postman/Newman
- Cenários positivos e negativos
- Validação de status HTTP
- Validação de estrutura e conteúdo da resposta
- Validação de tempo de resposta
- Uso de variáveis para configuração da API
- Execução automática em `push` e `pull_request`
- Geração de relatório JUnit no GitHub Actions

## 🌐 API utilizada

Os testes utilizam a **JSONPlaceholder**, uma API pública destinada a exemplos e testes.

Este projeto não utiliza credenciais privadas, dados reais de clientes ou endpoints corporativos.

## ✅ Cenários automatizados

| Cenário | Método | Resultado esperado |
| --- | --- | --- |
| Consultar um post existente | GET | HTTP 200 + validação do contrato |
| Filtrar posts por usuário | GET | HTTP 200 + validação dos itens retornados |
| Criar um post | POST | HTTP 201 + validação do payload |
| Consultar um post inexistente | GET | HTTP 404 |

## 📁 Estrutura

```text
.
├── .github/
│   └── workflows/
│       └── newman-tests.yml
├── tests/
│   └── collection.json
├── .gitignore
├── package.json
└── README.md
```

## ▶️ Executando localmente

Pré-requisito: Node.js instalado.

```bash
npm install
npm test
```

## 🔄 CI/CD

O workflow do GitHub Actions é executado automaticamente em alterações enviadas para a branch `main` e em pull requests. A pipeline instala as dependências, executa a collection com Newman e disponibiliza um relatório JUnit como artefato.

## 🛠️ Tecnologias e competências

`API Testing` · `Postman` · `Newman` · `REST API` · `JavaScript Assertions` · `GitHub Actions` · `CI/CD` · `Test Automation`

---

### English summary

QA portfolio project demonstrating REST API test automation with Postman, Newman and GitHub Actions, including positive/negative scenarios, response assertions and continuous testing in CI/CD.
