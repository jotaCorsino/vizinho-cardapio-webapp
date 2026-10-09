# Modelo de dados comerciais e métricas

**Objetivo:** construir desde cedo a base necessária ao dashboard, mesmo quando relatórios sofisticados forem entregues depois.

## Distinções fundamentais
- **Pedido enviado:** solicitação registrada; não é necessariamente venda.
- **Pedido aceito:** estabelecimento assumiu o atendimento.
- **Pedido concluído:** atendimento encerrado conforme regra operacional aprovada.
- **Pagamento confirmado:** operador registrou recebimento diretamente pelo estabelecimento, **não** é conciliação bancária.
- **Cancelado/recusado:** precisa de tratamento explícito em somas e rankings.

Não exibir simplesmente "faturamento recebido" ao somar pedidos enviados.

## Informações transacionais mínimas
Estabelecimento; pedido/protocolo; timestamps (em UTC, com fuso da loja para relatórios); modalidade entrega/retirada; itens com snapshots de nomes, categoria, quantidades, valores e descontos; totais/taxas; eventos de status; registro de recebimento manual quando aplicável; bairro somente se pertinente. Dados de contato e endereço devem ter retenção separada dos dados estatísticos.

## Indicadores
| Métrica | Cálculo proposto |
|---|---|
| Pedidos recebidos | Contagem de pedidos criados no período |
| Pedidos concluídos | Contagem dos que atingiram estado final válido |
| Taxa de cancelamento | Cancelados ÷ enviados, com período/denominador definidos |
| Valor dos pedidos concluídos | Soma dos totais de pedidos concluídos |
| Ticket médio concluído | Valor dos concluídos ÷ número de concluídos |
| Pagamentos confirmados | Soma dos recebimentos que operador marcou como pagos, com correções |
| Produtos mais vendidos | Quantidades de itens em pedidos elegíveis |
| Produtos com maior receita | Soma monetária atribuída a itens elegíveis |
| Picos por período | Pedidos agrupados por hora/dia no fuso do estabelecimento |

Para cada gráfico, explicitar evento de referência (criação, conclusão ou pagamento), período e tratamento de cancelamentos. O dashboard precisa ser reconciliável com transações, sem depender de nome ou telefone do comprador.

## Filtros e comparativos
Diário, semanal, mensal, trimestral, semestral, anual, período customizado e comparação entre períodos equivalentes. Evoluções: modalidade, categorias, tendências, bairros agregados, promoções e tempo entre etapas.

## Testes de aceite
Usar pedidos fictícios conhecidos para comparar somas, ticket médio e rankings; incluir cancelamento, pedido não pago, troca de status, limites de período, fuso horário e tentativa de consultar dados de outro estabelecimento.
