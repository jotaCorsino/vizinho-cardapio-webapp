# Escopo proposto do MVP

**Situação:** planejado; ainda sem homologação e sem autorização de implementação.

## Objetivo
Validar a jornada: **cardápio → carrinho → envio → atendimento do restaurante → conclusão → dashboard** em um piloto controlado.

## Dentro do MVP
1. Página pública com nome, logotipo, cores, descrição, horário e endereço web exclusivo por estabelecimento.
2. Categorias, produtos, descrição, imagens opcionais, preço, disponibilidade e promoções/destaques simples.
3. Carrinho com quantidades, observações e revisão do total.
4. Checkout sem conta de consumidor, para entrega ou retirada, com apenas dados necessários à modalidade.
5. Possibilidade de preenchimento recorrente opcional no próprio dispositivo, com explicação e exclusão.
6. Registro transacional de pedido, itens e preços da ocasião, protocolo e tratamento de reenvio.
7. Painel autenticado do estabelecimento: novos pedidos, detalhe, aceite e atualização de status.
8. Gestão de catálogo, horários e configuração básica do estabelecimento.
9. Dashboard inicial: pedidos, concluídos, cancelados, valores de concluídos, ticket médio, ranking de produtos e filtros temporais.
10. Administração básica de estabelecimentos, isolamento multi-tenant, backups e logs operacionais seguros.

## Aceite mínimo
- Pedido chega à loja correta sem login do consumidor.
- O backend verifica disponibilidade, preços e taxas; não confia no total calculado pelo navegador.
- Pedidos repetidos/acidentais têm tratamento previsível.
- Usuários de uma loja não acessam dados de outra.
- O dashboard bate com um conjunto conhecido de pedidos fictícios.
- Dados pessoais são retidos somente por prazo definido e justificável.
- O fluxo de status e notificação é testado com uma equipe piloto.

## Fora do MVP
Pagamento online, comissão por transação, logística própria, aplicativos Android/iOS, programa de fidelidade, IA preditiva, emissão fiscal, ERP/estoque completo, integração PDV/WhatsApp e cobranças de assinaturas automatizadas.

## Pontos abertos
Complexidade dos adicionais (pizzas, tamanhos e bordas), áreas/taxas de entrega, confirmação manual de pagamento, cancelamentos, notificações, impressão e infraestrutura.
