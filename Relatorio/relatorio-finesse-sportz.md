# Relatorio - Finesse Sportz

## 1. Identificacao

- **Projeto**: Finesse Sportz
- **Tema**: Sistema web para empresa de camisas esportivas
- **Autor**: Arthur Gonçalves
- **Disciplina**: Projeto de Software

## 2. Resumo

O Finesse Sportz e uma proposta de sistema web para venda, personalizacao e gestao de camisas esportivas. O projeto documenta regras de negocio, requisitos, arquitetura e diagramas UML usando PlantUML.

## 3. Problema

Empresas de camisas esportivas precisam controlar produtos com muitas variacoes, como tamanho, cor, modelo e time. Quando o processo e manual, podem ocorrer vendas sem estoque, atrasos na producao de itens personalizados e dificuldade para acompanhar pedidos.

## 4. Solucao Proposta

A solucao proposta e um sistema web composto por catalogo, carrinho, checkout, controle de estoque, pagamento simulado e painel administrativo.

## 5. Arquitetura

A arquitetura proposta usa API Gateway e microsservicos, separando responsabilidades entre autenticacao, catalogo, estoque, pedidos, pagamento, notificacoes e relatorios.

## 6. Principais Regras de Negocio

- Produto so pode ser vendido se houver estoque disponivel.
- Camisa personalizada possui acrescimo de preco.
- Pedido so e confirmado apos pagamento aprovado.
- Pedido personalizado nao pode ser cancelado depois que entra em producao.
- Administrador gerencia produtos, estoque e relatorios.

## 7. Diagramas

Os diagramas principais estao na pasta `CodigosPlantUML`:

- Atores
- Casos de uso
- Arquitetura
- Componentes
- Classes
- Comunicacao
- Sequencia de pedido
- Estados do pedido
- Entidade-relacionamento
- Implantacao

## 8. Conclusao

O projeto apresenta uma visao completa para um sistema de e-commerce especializado em camisas esportivas, com regras de negocio coerentes e documentacao organizada para facilitar implementacao futura.
