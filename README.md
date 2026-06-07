# Finesse Sportz - Sistema Web de Venda de Camisas Esportivas

> Sistema web para venda, gestao de camisas esportivas da minha loja, **Finesse Sportz**.

<table>
  <tr>
    <td width="800px">
      <div align="justify">
        Este <strong>README.md</strong> apresenta a documentacao completa do projeto <strong>Finesse Sportz</strong>, desenvolvido como trabalho final de Projeto de Software. O objetivo do sistema e apoiar a venda de camisas esportivas, permitindo cadastro de produtos, controle de estoque por tamanho e cor, personalizacao de camisas, fechamento de pedidos, pagamento, acompanhamento de status e gestao administrativa. O projeto esta <strong>pronto para entrega</strong>, com requisitos, regras de negocio, arquitetura e diagramas UML organizados em PlantUML.
      </div>
    </td>
    <td>
      <div align="center">
        <img src="./docs/assets/finessepreto.png" alt="Logo Finesse Sportz" width="180px"/>
      </div>
    </td>
  </tr>
</table>

---

## Status do Projeto

![Status](https://img.shields.io/badge/Status-Pronto-brightgreen?style=for-the-badge)
![Versao](https://img.shields.io/badge/Versao-1.0.0-blue?style=for-the-badge)
![Documentacao](https://img.shields.io/badge/Documentacao-Completa-success?style=for-the-badge)
![PlantUML](https://img.shields.io/badge/PlantUML-10%20diagramas-orange?style=for-the-badge)
![Java](https://img.shields.io/badge/Java-17-red?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.x-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Licenca](https://img.shields.io/badge/Licenca-MIT-green?style=for-the-badge)

O projeto esta pronto como entrega academica de documentacao, modelagem e arquitetura. A proposta apresenta o sistema, as regras de negocio, os requisitos, a arquitetura e os principais diagramas UML.

---

## Indice

- [Links Uteis](#links-uteis)
- [Sobre o Projeto](#sobre-o-projeto)
- [Funcionalidades Principais](#funcionalidades-principais)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Arquitetura](#arquitetura)
  - [Exemplos de Diagramas](#exemplos-de-diagramas)
- [Instalacao e Execucao](#instalacao-e-execucao)
  - [Pre-requisitos](#pre-requisitos)
  - [Variaveis de Ambiente](#variaveis-de-ambiente)
  - [Instalacao de Dependencias](#instalacao-de-dependencias)
  - [Inicializacao do Banco de Dados PostgreSQL](#inicializacao-do-banco-de-dados-postgresql)
  - [Como Executar a Aplicacao](#como-executar-a-aplicacao)
- [Deploy](#deploy)
- [Estrutura de Pastas](#estrutura-de-pastas)
- [Demonstracao](#demonstracao)
- [Testes](#testes)
- [Documentacoes Utilizadas](#documentacoes-utilizadas)
- [Autores](#autores)
- [Contribuicao](#contribuicao)
- [Agradecimentos](#agradecimentos)
- [Licenca](#licenca)

---

## Links Uteis

- **Repositorio do Projeto:** [Trabalho-Final-ProjetoDeSoftware](https://github.com/arthurgvv/Trabalho-Final-ProjetoDeSoftware)
  > Repositorio GitHub contendo a documentacao, arquivos PlantUML, regras de negocio e relatorio do projeto.
- **Documentacao do Professor:** [Template README](https://github.com/joaopauloaramuni/laboratorio-de-desenvolvimento-de-software/blob/main/TEMPLATES/template_README.md)
  > Template usado como base para organizacao deste README.
- **Referencia de Estrutura:** [trabalhoFinal_ProjetoDeSoftware](https://github.com/Davii13/trabalhoFinal_ProjetoDeSoftware/tree/main)
  > Projeto usado como referencia de organizacao para a entrega final.
- **PlantUML:** [https://plantuml.com](https://plantuml.com)
  > Ferramenta utilizada para criar os diagramas UML do projeto.
- **Regras de Negocio:** [docs/regras-de-negocio.md](./docs/regras-de-negocio.md)
- **Requisitos:** [docs/requisitos.md](./docs/requisitos.md)
- **Arquitetura:** [docs/arquitetura.md](./docs/arquitetura.md)
- **Mapa de Endpoints:** [docs/api-endpoints.md](./docs/api-endpoints.md)

---

## Sobre o Projeto

O **Finesse Sportz** e um sistema web pensado para minha loja real de camisas esportivas. A ideia surgiu da necessidade de organizar melhor vendas, estoque, pedidos e personalizacoes, evitando processos manuais e reduzindo erros no atendimento ao cliente.

O sistema resolve problemas como:

- venda de produtos sem estoque disponivel;
- dificuldade para controlar tamanho, cor e modelo;
- falta de visibilidade sobre pedidos em andamento;
- controle manual de camisas personalizadas;
- ausencia de relatorios para acompanhar vendas e estoque;
- dificuldade para aplicar cupons, descontos e regras de frete.

O projeto foi desenvolvido em contexto academico, mas representa uma necessidade real da loja Finesse Sportz. Ele pode ser usado como base para uma futura implementacao completa do sistema.

---

## Funcionalidades Principais

- **Autenticacao Segura:** cadastro, login, controle de sessao e permissao por perfil.
- **Catalogo de Produtos:** listagem de camisas esportivas com filtros por time, modalidade, tamanho, cor e preco.
- **Personalizacao de Camisas:** cadastro de nome e numero na camisa, com regras de tamanho e valor adicional.
- **Carrinho de Compras:** inclusao, edicao e remocao de itens antes do fechamento do pedido.
- **Checkout:** calculo de subtotal, desconto, frete e total.
- **Controle de Estoque:** verificacao de disponibilidade por produto, tamanho e cor.
- **Pagamento:** integracao planejada com gateway externo de pagamento.
- **Acompanhamento de Pedido:** status como aguardando pagamento, pago, em producao, enviado e entregue.
- **Painel Administrativo:** gestao de produtos, variacoes, pedidos, estoque, cupons e relatorios.
- **Relatorios:** acompanhamento de vendas, produtos mais vendidos, pedidos pendentes e estoque baixo.
- **Notificacoes:** envio planejado de confirmacoes de pedido, pagamento e entrega.

---

## Tecnologias Utilizadas

As tecnologias abaixo representam a proposta tecnica para uma implementacao futura do sistema.

### Front-end

- **Framework/Biblioteca:** React 18
- **Linguagem/Superset:** TypeScript
- **Estilizacao:** Tailwind CSS
- **Gerenciamento de Estado:** Context API ou Zustand
- **Build Tool:** Vite
- **Rotas:** React Router
- **Cliente HTTP:** Axios

### Back-end

- **Linguagem/Runtime:** Java 17
- **Framework:** Spring Boot 3.x
- **Banco de Dados:** PostgreSQL 16
- **ORM:** Spring Data JPA / Hibernate
- **Autenticacao:** Spring Security + JWT
- **Validacao:** Bean Validation

### Mobile

- Nao faz parte do escopo inicial.
- Pode ser planejado futuramente com React Native ou Flutter.

### Infraestrutura & DevOps

- **Containerizacao:** Docker
- **Orquestracao:** Docker Compose
- **Cloud:** Render, Railway, Vercel ou VPS
- **CI/CD:** GitHub Actions
- **Documentacao:** Markdown + PlantUML
- **Versionamento:** Git + GitHub

---

## Arquitetura

A arquitetura proposta segue uma abordagem distribuida, baseada em **API Gateway** e **microsservicos**. Essa escolha foi feita para separar responsabilidades, facilitar a manutencao e deixar claro o papel de cada parte do sistema.

Principais componentes:

- **Frontend Web:** interface para clientes e administradores.
- **API Gateway / BFF:** entrada das requisicoes, autenticacao, logs e roteamento.
- **Auth Service:** cadastro, login, perfis e tokens JWT.
- **Catalogo Service:** produtos, times, modalidades e variacoes.
- **Estoque Service:** disponibilidade, reserva e baixa de estoque.
- **Pedidos Service:** carrinho, pedidos, status e cancelamentos.
- **Pagamento Service:** comunicacao com gateway de pagamento.
- **Notification Service:** notificacoes de pedido, pagamento e entrega.
- **Relatorio Service:** indicadores administrativos.
- **PostgreSQL:** persistencia relacional dos dados.

Padroes adotados:

- API Gateway
- Service Layer
- Repository
- DTO
- MVC
- Autenticacao JWT
- Webhook para retorno de pagamento

### Exemplos de Diagramas

Os diagramas principais estao organizados em PlantUML na pasta [CodigosPlantUML](./CodigosPlantUML).

| Diagrama | Arquivo |
| :---: | :--- |
| **Atores** | [CodigosPlantUML/actors.puml](./CodigosPlantUML/actors.puml) |
| **Casos de Uso** | [CodigosPlantUML/use_cases.puml](./CodigosPlantUML/use_cases.puml) |
| **Arquitetura Geral** | [CodigosPlantUML/architecture.puml](./CodigosPlantUML/architecture.puml) |
| **Componentes** | [CodigosPlantUML/components.puml](./CodigosPlantUML/components.puml) |
| **Classes** | [CodigosPlantUML/classes.puml](./CodigosPlantUML/classes.puml) |
| **Comunicacao do Fluxo Completo** | [CodigosPlantUML/diagrama_comunicacao_fluxo_completo.puml](./CodigosPlantUML/diagrama_comunicacao_fluxo_completo.puml) |
| **Sequencia de Pedido e Pagamento** | [CodigosPlantUML/diagrama_sequencia_pedido_pagamento.puml](./CodigosPlantUML/diagrama_sequencia_pedido_pagamento.puml) |
| **Estados do Pedido** | [CodigosPlantUML/estados.puml](./CodigosPlantUML/estados.puml) |
| **Entidade-Relacionamento** | [CodigosPlantUML/diagrama_entidade_relacionamento.puml](./CodigosPlantUML/diagrama_entidade_relacionamento.puml) |
| **Implantacao** | [CodigosPlantUML/implantacao.puml](./CodigosPlantUML/implantacao.puml) |

---

## Instalacao e Execucao

Como esta entrega tem foco em documentacao, modelagem e arquitetura, os comandos abaixo representam a proposta para uma implementacao futura da aplicacao.

### Pre-requisitos

- **Java JDK:** versao 17 ou superior.
- **Node.js:** versao 18 ou superior.
- **Gerenciador de Pacotes:** npm ou yarn.
- **Docker:** recomendado para executar PostgreSQL localmente.
- **PlantUML:** recomendado para visualizar os diagramas.

---

### Variaveis de Ambiente

Crie arquivos `.env` ou configure variaveis de ambiente para back-end e front-end.

#### 1 Back-end (Spring Boot)

| Variavel | Descricao | Exemplo |
| :--- | :--- | :--- |
| `SERVER_PORT` | Porta onde a API sera executada. | `8080` |
| `SPRING_DATASOURCE_URL` | URL JDBC do PostgreSQL. | `jdbc:postgresql://localhost:5432/finesse_sportz` |
| `SPRING_DATASOURCE_USERNAME` | Usuario do banco de dados. | `postgres` |
| `SPRING_DATASOURCE_PASSWORD` | Senha do banco de dados. | `postgres` |
| `JWT_SECRET` | Chave secreta para assinatura dos tokens. | `finesse-sportz-secret-key` |

#### 2 Front-end (React, Vite)

| Variavel | Descricao | Exemplo |
| :--- | :--- | :--- |
| `VITE_API_URL` | URL base da API. | `http://localhost:8080/api` |
| `VITE_APP_NAME` | Nome da aplicacao. | `Finesse Sportz` |

#### 3 Exemplos de Variaveis de Ambiente na Vercel

```env
VITE_API_URL=https://api.finessesportz.com/api
VITE_APP_NAME=Finesse Sportz
```

---

### Instalacao de Dependencias

Clone o repositorio:

```bash
git clone https://github.com/arthurgvv/Trabalho-Final-ProjetoDeSoftware.git
cd Trabalho-Final-ProjetoDeSoftware
```

#### Front-end (React)

```bash
cd frontend
npm install
cd ..
```

#### Back-end (Spring Boot)

```bash
cd backend
./mvnw clean install
cd ..
```

---

### Inicializacao do Banco de Dados PostgreSQL

Exemplo de execucao local com Docker:

```bash
docker run --name finesse_sportz_db \
  -e POSTGRES_USER=postgres \
  -e POSTGRES_PASSWORD=postgres \
  -e POSTGRES_DB=finesse_sportz \
  -p 5432:5432 \
  -d postgres:16
```

Caso o back-end utilize Flyway ou Hibernate, as tabelas podem ser criadas automaticamente na inicializacao da aplicacao.

---

### Como Executar a Aplicacao

#### Terminal 1: Back-end (Spring Boot)

```bash
cd backend
./mvnw spring-boot:run
```

O back-end ficara disponivel em:

```text
http://localhost:8080
```

#### Terminal 2: Front-end (React, Vite)

```bash
cd frontend
npm run dev
```

O front-end ficara disponivel em:

```text
http://localhost:5173
```

#### Execucao Local Completa com Docker Compose

```bash
docker-compose up --build -d
```

Para parar os containers:

```bash
docker-compose down
```

---

## Deploy

Proposta de deploy para uma versao futura:

1. Build do front-end:

```bash
cd frontend
npm run build
```

2. Build do back-end:

```bash
cd backend
./mvnw clean package
```

3. Configurar variaveis de ambiente no provedor escolhido.

4. Publicar:

- Front-end em Vercel ou Netlify.
- Back-end em Render, Railway ou VPS.
- Banco PostgreSQL em Railway, Neon, Supabase ou Render.

---

## Estrutura de Pastas

```text
.
|-- .gitignore
|-- CONTRIBUTING.md
|-- LICENSE
|-- README.md
|
|-- CodigosPlantUML/
|   |-- README.md
|   |-- actors.puml
|   |-- architecture.puml
|   |-- classes.puml
|   |-- components.puml
|   |-- diagrama_comunicacao_fluxo_completo.puml
|   |-- diagrama_entidade_relacionamento.puml
|   |-- diagrama_sequencia_pedido_pagamento.puml
|   |-- estados.puml
|   |-- implantacao.puml
|   `-- use_cases.puml
|
|-- Problema/
|   `-- problema-finesse-sportz.md
|
|-- Relatorio/
|   `-- relatorio-finesse-sportz.md
|
`-- docs/
    |-- api-endpoints.md
    |-- arquitetura.md
    |-- regras-de-negocio.md
    |-- requisitos.md
    |-- assets/
    |   |-- finessepreto.png
    |   `-- profile.jpg
    `-- diagramas/
        |-- arquitetura.puml
        |-- casos-de-uso.puml
        |-- classes.puml
        |-- estado-pedido.puml
        |-- modelo-dados.puml
        |-- rotas-api.puml
        `-- sequencia-pedido.puml
```

---

## Demonstracao

A entrega atual e focada em documentacao e modelagem. As demonstracoes abaixo indicam as telas previstas para uma implementacao futura.

### Aplicativo Mobile

Nao faz parte do escopo inicial do projeto.

| Tela | Situacao |
| :---: | :--- |
| Aplicativo Mobile | Planejado apenas para versoes futuras. |

### Aplicacao Web

| Tela | Descricao |
| :---: | :--- |
| **Home / Catalogo** | Listagem das camisas esportivas disponiveis. |
| **Detalhe do Produto** | Visualizacao de modelo, tamanho, cor, preco e disponibilidade. |
| **Personalizacao** | Insercao de nome e numero na camisa. |
| **Carrinho** | Revisao dos itens antes do fechamento. |
| **Checkout** | Calculo de frete, desconto e pagamento. |
| **Painel Administrativo** | Gestao de produtos, estoque, pedidos e relatorios. |

### Exemplo de Saida no Terminal (API)

Exemplo de consulta de produtos:

```bash
curl -X GET "http://localhost:8080/api/produtos"
```

Saida esperada:

```json
{
  "total": 2,
  "produtos": [
    {
      "id": "1",
      "nome": "Camisa Brasil I 2024",
      "tamanho": "M",
      "cor": "Amarela",
      "preco": 199.90,
      "estoque": 12
    },
    {
      "id": "2",
      "nome": "Camisa Real Madrid Home",
      "tamanho": "G",
      "cor": "Branca",
      "preco": 229.90,
      "estoque": 8
    }
  ]
}
```

---

## Testes

### Testes Unitarios e de Integracao

Testes planejados para a implementacao:

```bash
npm run test
```

```bash
./mvnw test
```

Itens que devem ser testados:

- validacao de estoque;
- calculo de total do pedido;
- regra de personalizacao;
- cupom de desconto;
- transicao de status do pedido;
- permissao de administrador.

### Testes End-to-End (E2E)

```bash
npm run test:e2e
```

Fluxos previstos:

- cliente compra camisa comum;
- cliente compra camisa personalizada;
- administrador cadastra produto;
- administrador atualiza estoque;
- cliente acompanha pedido.

---

## Documentacoes Utilizadas

- **Template README:** [template_README.md](https://github.com/joaopauloaramuni/laboratorio-de-desenvolvimento-de-software/blob/main/TEMPLATES/template_README.md)
- **Referencia de Projeto:** [trabalhoFinal_ProjetoDeSoftware](https://github.com/Davii13/trabalhoFinal_ProjetoDeSoftware/tree/main)
- **PlantUML:** [Documentacao Oficial](https://plantuml.com)
- **React:** [Documentacao Oficial](https://react.dev)
- **Vite:** [Documentacao Oficial](https://vitejs.dev)
- **Spring Boot:** [Documentacao Oficial](https://spring.io/projects/spring-boot)
- **PostgreSQL:** [Documentacao Oficial](https://www.postgresql.org/docs)
- **Docker:** [Documentacao Oficial](https://docs.docker.com)
- **Conventional Commits:** [Guia Oficial](https://www.conventionalcommits.org/en/v1.0.0/)

---

## Autor

| 👤 Nome | 🖼️ Foto | GitHub | LinkedIn | Email |
|--------|--------|--------|----------|-------|
| Arthur Gonçalves | <img src="./docs/assets/profile.jpg" width="100px" style="border-radius:50%;"> | <a href="https://github.com/arthurgvv"><img src="https://img.shields.io/badge/GitHub-000?style=for-the-badge&logo=github&logoColor=white"></a> | <a href="https://www.linkedin.com/in/arthur-goncalves-62b15232a/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"></a> | <a href="mailto:arthurgvkj@gmail.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white"></a> |

---

## Contribuicao

Como este projeto e uma entrega academica individual, contribuicoes externas nao fazem parte do escopo principal. Ainda assim, a estrutura segue boas praticas de versionamento.

Para contribuicoes futuras:

1. Faca um `fork` do projeto.
2. Crie uma branch para sua feature:

```bash
git checkout -b feature/minha-feature
```

3. Commit suas mudancas usando Conventional Commits:

```bash
git commit -m "feat: adiciona nova funcionalidade"
```

4. Envie a branch:

```bash
git push origin feature/minha-feature
```

5. Abra um Pull Request.

---

## Agradecimentos

Agradeco ao professor pela proposta do trabalho e pelo template de documentacao, que ajudou a organizar o projeto de forma clara e profissional.

Tambem deixo registrado o uso do projeto [trabalhoFinal_ProjetoDeSoftware](https://github.com/Davii13/trabalhoFinal_ProjetoDeSoftware/tree/main) como referencia de estrutura para esta entrega.

---

## Licenca

Este projeto e distribuido sob a [Licenca MIT](./LICENSE).

---

## Status Final

Projeto pronto para entrega.

Documentacao, regras de negocio, requisitos, arquitetura, relatorio e diagramas PlantUML foram organizados no repositorio.
