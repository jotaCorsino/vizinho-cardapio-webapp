# Requisitos funcionais

**Estado:** candidatos com IDs de rastreabilidade; nenhum autoriza trabalho sozinho.

| ID | Requisito |
|---|---|
| RF-001 | Exibir página personalizada do estabelecimento por URL própria |
| RF-002 | Consultar categorias, produtos, imagens, disponibilidade e destaques |
| RF-003 | Montar carrinho com quantidades e observações |
| RF-004 | Calcular valores finais no servidor |
| RF-005 | Escolher entrega ou retirada conforme configuração |
| RF-006 | Finalizar sem criar conta de consumidor |
| RF-007 | Coletar apenas dados necessários ao pedido |
| RF-008 | Permitir lembrar e apagar dados locais opcionalmente |
| RF-009 | Confirmar envio de pedido com protocolo |
| RF-010 | Respeitar horário e disponibilidade comercial |
| RF-011 | Autenticar administradores/operadores do estabelecimento |
| RF-012 | Gerir categorias, produtos, preços e promoções simples |
| RF-013 | Configurar horários, apresentação e modalidade de atendimento |
| RF-014 | Listar novos pedidos apenas do próprio estabelecimento |
| RF-015 | Gerenciar status com transições válidas |
| RF-016 | Registrar eventos de mudança de status |
| RF-017 | Registrar pagamento recebido manualmente, se homologado |
| RF-018 | Consultar pedidos e métricas por períodos |
| RF-019 | Analisar produtos e categorias mais vendidos |
| RF-020 | Administrar estabelecimentos na plataforma |
| RF-021 | Impedir leitura e alteração de dados entre estabelecimentos |
| RF-022 | Registrar falhas técnicas sem expor dados pessoais nos logs |

## Regras de operação a detalhar
Fluxo inicial sugerido: enviado → aceito → em preparo → pronto → entregue/retirado → concluído, com alternativas de recusa e cancelamento. Confirmação de pagamento não deve ser presumida a partir de conclusão do atendimento.

## Cenários negativos obrigatórios
Preço adulterado no navegador; pedido duplicado; cliente tentando alterar status; usuário da loja A tentando ler a loja B; loja fechada; item indisponível; erros de conexão; dados de entrega indevidos; cancelamento que altere indicadores.

## Evolução
Cada RF será refinado em tarefa ÓRBITA com escopo incluído/excluído, riscos, testes e critérios verificáveis de aceite.
