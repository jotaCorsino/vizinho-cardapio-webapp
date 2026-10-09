# Arquitetura inicial (conceitual)

**Estado:** proposta, sem stack homologada.

## Modelo
Uma única aplicação SaaS com múltiplos estabelecimentos (**multi-tenant**). Cada estabelecimento publica página/cardápio, recebe pedidos e acessa somente seus próprios relatórios. Uma administração de plataforma mantém os tenants.

## Componentes
- **Web público:** cardápio, carrinho, checkout sem conta.
- **Web administrativo do estabelecimento:** catálogo, configurações, pedidos e dashboard.
- **Administração Vizinho:** provisionamento e operação da plataforma.
- **Backend/API:** autenticação administrativa, autorização por tenant, precificação, checkout e status.
- **Banco transacional:** estabelecimentos, usuários, produtos, pedidos, itens, eventos e dados minimizados.
- **Operação:** arquivos/imagens, backups, monitoramento, tarefas agendadas e notificações.

## Fluxo crítico
O navegador monta carrinho e dados do pedido → servidor identifica o estabelecimento → valida itens, disponibilidade, preço, descontos e taxa → registra pedido com tratamento de duplicidade → painel da loja recebe o registro → equipe atualiza o status → métricas derivam dos fatos transacionais.

## Isolamento e integridade
Toda leitura/escrita administrativa exige comprovar permissão no estabelecimento correto. Não confiar no identificador enviado pelo cliente. Itens do pedido devem preservar snapshot de nome/preço, mesmo que catálogo seja alterado. Usar transações e estratégia de idempotência.

## Entidades candidatas
Estabelecimento, usuário/papel, configuração, categoria, produto, opção/adicional, pedido, item do pedido, histórico de status, confirmação de pagamento, agregados analíticos e plano/assinatura. Dados de contato/entrega exigem segregação e política de retenção.

## Stack a avaliar
Laravel/PHP + MySQL/MariaDB + frontend responsivo é uma alternativa, **não uma decisão**. Avaliar infraestrutura quanto a fila de pedidos, notificações, jobs, backups, deploy, testes e performance. Preferir monólito modular no MVP; evitar microserviços antes de necessidade comprovada. Polling controlado pode ser suficiente na primeira central de pedidos.

## Pendências
Escolher stack/hospedagem, estrutura de banco, autenticação, pipeline, uploads e política de indisponibilidade antes de iniciar a implementação funcional.
