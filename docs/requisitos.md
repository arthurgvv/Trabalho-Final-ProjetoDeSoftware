# Requisitos do Sistema

Projeto: Finesse Sportz

---

## Atores

| Ator | Descricao |
|---|---|
| Cliente | Usuario que consulta produtos, personaliza camisas e realiza pedidos. |
| Administrador | Usuario interno que gerencia produtos, estoque, pedidos e relatorios. |
| Gateway de Pagamento | Servico externo responsavel por autorizar ou recusar pagamentos. |
| Transportadora | Servico externo ou setor responsavel pela entrega dos pedidos. |

---

## Requisitos Funcionais

| Codigo | Requisito | Ator Principal |
|---|---|---|
| RF01 | O sistema deve permitir cadastro de clientes. | Cliente |
| RF02 | O sistema deve permitir login e logout. | Cliente, Administrador |
| RF03 | O sistema deve listar camisas disponiveis no catalogo. | Cliente |
| RF04 | O sistema deve permitir filtros por tamanho, cor, time, modalidade e preco. | Cliente |
| RF05 | O sistema deve permitir visualizar detalhes de uma camisa. | Cliente |
| RF06 | O sistema deve permitir personalizar camisa com nome e numero. | Cliente |
| RF07 | O sistema deve permitir adicionar itens ao carrinho. | Cliente |
| RF08 | O sistema deve calcular subtotal, desconto, frete e total. | Cliente |
| RF09 | O sistema deve permitir aplicar cupom de desconto. | Cliente |
| RF10 | O sistema deve permitir finalizar pedido. | Cliente |
| RF11 | O sistema deve integrar com gateway de pagamento. | Cliente |
| RF12 | O sistema deve permitir acompanhamento do status do pedido. | Cliente |
| RF13 | O sistema deve permitir cadastro e edicao de produtos. | Administrador |
| RF14 | O sistema deve permitir controle de estoque por variacao. | Administrador |
| RF15 | O sistema deve permitir atualizacao de status do pedido. | Administrador |
| RF16 | O sistema deve gerar relatorios de vendas e estoque. | Administrador |
| RF17 | O sistema deve sinalizar estoque baixo. | Administrador |

---

## Requisitos Nao Funcionais

| Codigo | Requisito |
|---|---|
| RNF01 | O sistema deve ser responsivo para desktop e dispositivos moveis. |
| RNF02 | A API deve responder em ate 2 segundos nas operacoes comuns. |
| RNF03 | Senhas devem ser armazenadas com hash seguro. |
| RNF04 | Rotas administrativas devem exigir perfil de administrador. |
| RNF05 | O sistema deve registrar logs de operacoes criticas. |
| RNF06 | O banco de dados deve manter integridade referencial. |
| RNF07 | A aplicacao deve permitir execucao local com Docker Compose. |
| RNF08 | O sistema deve ser documentado com Markdown e PlantUML. |

---

## Casos de Uso Principais

| Codigo | Caso de Uso | Descricao |
|---|---|---|
| UC01 | Comprar camisa | Cliente escolhe camisa, adiciona ao carrinho e finaliza pedido. |
| UC02 | Personalizar camisa | Cliente informa nome e numero antes de adicionar ao carrinho. |
| UC03 | Gerenciar catalogo | Administrador cadastra e altera produtos. |
| UC04 | Gerenciar estoque | Administrador atualiza quantidades por variacao. |
| UC05 | Confirmar pagamento | Gateway informa aprovacao ou recusa de pagamento. |
| UC06 | Acompanhar pedido | Cliente consulta andamento do pedido. |
| UC07 | Gerar relatorio | Administrador visualiza indicadores comerciais. |

---

## Backlog Inicial

| Prioridade | Item |
|---|---|
| Alta | Cadastro e login de cliente. |
| Alta | Catalogo de produtos. |
| Alta | Carrinho e fechamento de pedido. |
| Alta | Controle de estoque por tamanho e cor. |
| Alta | Regras de personalizacao. |
| Media | Cupons e descontos. |
| Media | Dashboard administrativo. |
| Media | Relatorios de vendas. |
| Baixa | Integracao avancada com transportadora. |
| Baixa | Notificacoes por e-mail. |
