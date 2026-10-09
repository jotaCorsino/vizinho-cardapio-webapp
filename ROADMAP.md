# Roadmap — Vizinho

**Planejamento inicial de 09/10/2026.** Etapas propostas; não indicam código implementado.

| Fase | Objetivo | Estado | Gate |
|---|---|---|---|
| F00 — Fundação | Visão, requisitos, arquitetura, métricas, riscos e organização | AGUARDANDO_HOMOLOGACAO | Revisão humana dos documentos |
| F01 — Bootstrap | Vincular com segurança pasta local ao GitHub | PLANEJADA | Evidências de origin, HEAD, branch e status |
| F02 — Base SaaS | Aplicação inicial, banco, autenticação e isolamento multi-tenant | PLANEJADA | Testes de base e acesso cruzado |
| F03 — Cardápio | Identidade do estabelecimento, catálogo e experiência móvel | PLANEJADA | Fluxo de gestão/exibição homologado |
| F04 — Checkout | Carrinho, entrega/retirada, pedido sem conta e integridade | PLANEJADA | Pedido seguro, preço correto e sem duplicação silenciosa |
| F05 — Central | Receber, visualizar e atualizar pedidos | PLANEJADA | Operação com dados fictícios homologada |
| F06 — Dashboard | Indicadores e comparações históricas | PLANEJADA | Métricas reconciliadas com base de pedidos |
| F07 — Preparação piloto | Testes integrados, privacidade, segurança e recuperação | PLANEJADA | Aprovação explícita para uso real |
| F08 — Piloto | Teste controlado em estabelecimento real | PLANEJADA | Avaliação humana do resultado e próximos passos |

**Dependência principal:** F00 → F01 → F02 → F03 → F04 → F05 → F06 → F07 → F08, com possibilidade de reordenar mediante homologação. Os campos necessários ao dashboard devem ser planejados desde F02/F04.

## Regras
Tarefas pequenas e numeradas, critérios de aceite verificáveis, branches específicas e evidências de testes. Não iniciar a próxima tarefa sem o gate humano pertinente.

## Próximo passo
Revisar e homologar F00; preparar a tarefa exclusiva de bootstrap F01 para o Codex.
