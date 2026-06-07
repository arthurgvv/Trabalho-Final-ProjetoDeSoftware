# Regras de Negocio

Projeto: Finesse Sportz

Este documento descreve as regras de negocio da Finesse Sportz, minha loja real de camisas esportivas. As regras definem como o sistema deve se comportar para manter consistencia nas vendas, personalizacoes, estoque, pagamento e entrega.

---

## RN01 - Cadastro de Cliente

Todo cliente deve possuir nome, e-mail unico, telefone e senha para realizar pedidos.

## RN02 - Produto Ativo no Catalogo

Somente produtos com status ativo podem aparecer no catalogo publico da loja.

## RN03 - Estoque por Variacao

O estoque deve ser controlado por produto, tamanho, cor e modelo. Nao basta verificar apenas o produto principal.

## RN04 - Bloqueio de Venda sem Estoque

O sistema nao deve permitir a inclusao no carrinho de uma quantidade maior que o estoque disponivel.

## RN05 - Personalizacao de Camisa

O cliente pode personalizar a camisa com nome e numero. O nome deve ter no maximo 20 caracteres e o numero deve estar entre 0 e 99.

## RN06 - Acrescimo por Personalizacao

Toda camisa personalizada recebe acrescimo fixo no preco do item.

## RN07 - Calculo do Total do Pedido

O total do pedido deve considerar subtotal dos itens, acrescimos de personalizacao, descontos, cupom e frete.

## RN08 - Cupom de Desconto

Um cupom so pode ser aplicado se estiver ativo, dentro da validade e se o pedido atingir o valor minimo definido.

## RN09 - Frete Gratis

Pedidos acima de R$ 300,00 podem receber frete gratis, desde que nao exista regra promocional mais restritiva.

## RN10 - Reserva de Estoque

Ao iniciar o pagamento, o estoque dos itens deve ser reservado temporariamente para evitar venda duplicada.

## RN11 - Confirmacao do Pedido

Um pedido so deve ser confirmado quando o pagamento for aprovado.

## RN12 - Cancelamento de Pedido

Pedidos comuns podem ser cancelados antes do envio. Pedidos personalizados nao podem ser cancelados depois que entram em producao.

## RN13 - Fluxo de Status do Pedido

O pedido deve seguir uma sequencia valida de status:

```text
Criado -> Aguardando pagamento -> Pago -> Em producao -> Separado -> Enviado -> Entregue
```

Em caso de problema, o pedido pode ir para:

```text
Cancelado
Pagamento recusado
```

## RN14 - Permissao Administrativa

Somente usuarios administradores podem cadastrar produtos, alterar precos, atualizar estoque e visualizar relatorios.

## RN15 - Preco do Produto

O preco de venda deve ser maior que zero. Alteracoes de preco nao devem modificar pedidos ja fechados.

## RN16 - SKU Unico

Cada variacao de produto deve possuir um SKU unico para facilitar o controle de estoque.

## RN17 - Alerta de Estoque Baixo

Quando uma variacao atingir quantidade menor ou igual ao limite minimo configurado, o sistema deve sinalizar estoque baixo.

## RN18 - Registro de Pagamento

Todo pagamento deve registrar valor, forma de pagamento, status, data da tentativa e identificador externo da transacao.

## RN19 - Historico do Cliente

O cliente deve conseguir visualizar seus pedidos anteriores, mas nao pode acessar pedidos de outros clientes.

## RN20 - Relatorios Administrativos

Relatorios devem apresentar dados consolidados de vendas, produtos mais vendidos, pedidos pendentes e itens com estoque baixo.
