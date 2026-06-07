# Mapa de Endpoints da API

Projeto: Finesse Sportz

Os endpoints abaixo representam uma proposta inicial para a API REST do sistema.

---

## Autenticacao

| Metodo | Rota | Descricao | Perfil |
|---|---|---|---|
| POST | `/api/auth/register` | Cadastra cliente. | Publico |
| POST | `/api/auth/login` | Autentica usuario. | Publico |
| POST | `/api/auth/refresh` | Renova token de acesso. | Cliente/Admin |
| POST | `/api/auth/logout` | Encerra sessao. | Cliente/Admin |

---

## Produtos

| Metodo | Rota | Descricao | Perfil |
|---|---|---|---|
| GET | `/api/produtos` | Lista produtos ativos. | Publico |
| GET | `/api/produtos/{id}` | Busca detalhes do produto. | Publico |
| POST | `/api/produtos` | Cadastra produto. | Admin |
| PUT | `/api/produtos/{id}` | Atualiza produto. | Admin |
| PATCH | `/api/produtos/{id}/status` | Ativa ou inativa produto. | Admin |

---

## Estoque

| Metodo | Rota | Descricao | Perfil |
|---|---|---|---|
| GET | `/api/estoques` | Lista variacoes e quantidades. | Admin |
| POST | `/api/produtos/{id}/variacoes` | Cadastra variacao de produto. | Admin |
| PUT | `/api/estoques/{variacaoId}` | Atualiza quantidade em estoque. | Admin |
| GET | `/api/estoques/baixo` | Lista itens com estoque baixo. | Admin |

---

## Pedidos

| Metodo | Rota | Descricao | Perfil |
|---|---|---|---|
| POST | `/api/pedidos` | Cria pedido a partir do carrinho. | Cliente |
| GET | `/api/pedidos/meus` | Lista pedidos do cliente autenticado. | Cliente |
| GET | `/api/pedidos/{id}` | Consulta detalhes do pedido. | Cliente/Admin |
| PATCH | `/api/pedidos/{id}/cancelar` | Solicita cancelamento do pedido. | Cliente/Admin |
| PATCH | `/api/pedidos/{id}/status` | Atualiza status operacional. | Admin |

---

## Pagamentos

| Metodo | Rota | Descricao | Perfil |
|---|---|---|---|
| POST | `/api/pedidos/{id}/pagamento` | Inicia pagamento do pedido. | Cliente |
| POST | `/api/pagamentos/webhook` | Recebe retorno do gateway. | Gateway |
| GET | `/api/pagamentos/{id}` | Consulta status de pagamento. | Cliente/Admin |

---

## Cupons

| Metodo | Rota | Descricao | Perfil |
|---|---|---|---|
| POST | `/api/cupons/validar` | Valida cupom para um carrinho. | Cliente |
| POST | `/api/cupons` | Cadastra cupom. | Admin |
| PUT | `/api/cupons/{id}` | Atualiza cupom. | Admin |
| PATCH | `/api/cupons/{id}/status` | Ativa ou inativa cupom. | Admin |

---

## Relatorios

| Metodo | Rota | Descricao | Perfil |
|---|---|---|---|
| GET | `/api/relatorios/vendas` | Consulta resumo de vendas. | Admin |
| GET | `/api/relatorios/produtos-mais-vendidos` | Lista produtos mais vendidos. | Admin |
| GET | `/api/relatorios/pedidos-pendentes` | Lista pedidos pendentes. | Admin |
| GET | `/api/relatorios/estoque-baixo` | Lista alertas de estoque baixo. | Admin |
