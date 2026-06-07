# Arquitetura

Projeto: Finesse Sportz

---

## Visao Geral

A arquitetura proposta para o Finesse Sportz usa uma estrutura distribuida baseada em API Gateway e microsservicos. Essa decisao foi adotada para organizar melhor as responsabilidades do sistema e seguir a estrutura do trabalho de referencia usado como base.

O sistema e dividido em:

- Front-end Web
- API Gateway
- Auth Service
- Catalogo Service
- Estoque Service
- Pedidos Service
- Pagamento Service
- Notification Service
- Relatorio Service
- Banco de Dados PostgreSQL
- Integracoes externas de pagamento e email

---

## Camadas

### 1. Interface Web

Responsavel pela experiencia do usuario. Contem telas de catalogo, detalhe do produto, personalizacao, carrinho, checkout, historico de pedidos e painel administrativo.

Tecnologias propostas:

- React
- TypeScript
- Vite
- Tailwind CSS

### 2. API Gateway

Centraliza a entrada das requisicoes e encaminha cada chamada ao servico correto.

Responsabilidades:

- roteamento;
- autenticacao;
- validacao de token;
- controle de acesso;
- logs de requisicao;
- padronizacao de respostas.

### 3. Auth Service

Responsavel por cadastro, login, perfis de usuario e geracao de tokens JWT.

### 4. Catalogo Service

Gerencia produtos, times, modalidades, tamanhos, cores e variacoes.

### 5. Estoque Service

Controla quantidade disponivel, reserva temporaria, baixa de estoque e alerta de estoque baixo.

### 6. Pedidos Service

Orquestra carrinho, fechamento de pedido, status, cancelamento e regras relacionadas a pedidos personalizados.

### 7. Pagamento Service

Integra com gateway externo simulado para aprovar ou recusar pagamentos.

### 8. Notification Service

Envia confirmacoes de pedido, pagamento, envio e cancelamento.

### 9. Relatorio Service

Gera indicadores administrativos, como produtos mais vendidos, pedidos pendentes e estoque baixo.

---

## Fluxo Principal de Compra

1. Cliente acessa o catalogo.
2. Cliente escolhe camisa, tamanho e cor.
3. Cliente informa personalizacao, se desejar.
4. Sistema valida estoque.
5. Cliente adiciona item ao carrinho.
6. Sistema calcula total, frete e descontos.
7. Cliente finaliza pedido.
8. Sistema reserva estoque.
9. Gateway de pagamento aprova ou recusa pagamento.
10. Pedido aprovado segue para producao ou separacao.
11. Notification Service envia confirmacao.
12. Pedido e enviado e entregue.

---

## Padroes de Projeto e Boas Praticas

- API Gateway para centralizar comunicacao.
- Service Layer para regras de negocio.
- Repository para acesso a dados.
- DTO para trafego entre front-end e back-end.
- JWT para autenticacao.
- Controle de perfil Cliente/Admin.
- Webhook para retorno de pagamento.
- Logs para rastrear operacoes criticas.

---

## Decisoes Arquiteturais

| Decisao | Justificativa |
|---|---|
| Microsservicos | Separa responsabilidades e deixa a documentacao mais clara. |
| API Gateway | Centraliza seguranca, roteamento e entrada da aplicacao. |
| PostgreSQL | Banco relacional adequado para pedidos, pagamentos e estoque. |
| JWT | Permite autenticacao stateless. |
| PlantUML | Facilita versionar e revisar diagramas junto ao projeto. |

---

## Limitacoes Conhecidas

- A implementacao real pode comecar como monolito modular, caso o prazo seja curto.
- A integracao com pagamento e entrega pode ser simulada.
- Nao ha previsao inicial de aplicativo mobile nativo.
- Recomendacao de produtos pode ficar para versoes futuras.

