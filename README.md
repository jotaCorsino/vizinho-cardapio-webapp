# Vizinho — Cardápio Webapp

> Plataforma web de cardápios digitais, recebimento de pedidos e inteligência comercial para estabelecimentos do setor alimentício.

**Estado:** `FUNDACAO_DOCUMENTAL` · **Início do projeto:** 09/10/2026 · **Método:** [ÓRBITA](https://github.com/jotaCorsino/orbita-development-model)  
**Repositório canônico:** [jotaCorsino/vizinho-cardapio-webapp](https://github.com/jotaCorsino/vizinho-cardapio-webapp)  
**Produto:** Vizinho (nome de trabalho) · **Versão de software:** nenhuma — desenvolvimento funcional não iniciado

## O que é o Vizinho?

O Vizinho pretende oferecer a restaurantes, pizzarias, hamburguerias, lanchonetes e estabelecimentos semelhantes seu próprio canal digital de vendas. Cada estabelecimento poderá compartilhar um link ou QR Code para um cardápio personalizado, receber pedidos diretamente em um painel operacional e consultar indicadores de desempenho em um dashboard.

Para o consumidor, a proposta é uma jornada rápida e responsiva, sem criação de conta. Para o estabelecimento, é uma assinatura que inclui acesso ao sistema, hospedagem e manutenção. O Vizinho **não pretende intermediar pagamentos**, processar cartões ou oferecer logística própria na primeira versão.

O software será planejado como **uma plataforma multiestabelecimento**, com separação lógica rigorosa dos dados de cada cliente. A arquitetura técnica específica ainda depende de decisões registradas na documentação.

## Quem utiliza?

- **Consumidor:** navega pelo cardápio, monta o carrinho e envia pedidos sem abrir conta.
- **Estabelecimento:** configura a página e o cardápio, recebe e acompanha pedidos, consulta desempenho de vendas.
- **Administração do Vizinho:** cadastra e administra estabelecimentos, planos e configurações operacionais autorizadas.

## Frentes do produto

1. **Cardápio digital:** página personalizada, produtos, categorias, promoções e carrinho.
2. **Central de pedidos:** recebimento, acompanhamento, atualização de status e apoio à operação.
3. **Dashboard comercial:** volume de pedidos, valores registrados, ticket médio, produtos mais vendidos e comparações temporais, com definições explícitas de métricas.
4. **Operação SaaS:** administração de estabelecimentos, isolamento de dados, hospedagem e suporte.

A experiência pode ser inspirada em padrões comuns de aplicativos de delivery, sem copiar identidade visual ou elementos proprietários de terceiros.

## Regras e restrições iniciais

- **Sem conta obrigatória para consumidores.** O preenchimento recorrente poderá ser facilitado por armazenamento opcional no dispositivo.
- **Sem pagamento na plataforma no MVP.** O pagamento acontece diretamente ao estabelecimento, por ocasião de entrega ou retirada; detalhes do fluxo ainda precisam ser homologados.
- **LGPD continua aplicável:** mesmo sem cadastro, o fluxo de pedidos pode tratar nome, telefone e endereço. Minimização, transparência, segurança e retenção proporcional serão requisitos.
- **Indicadores devem ser honestos:** pedido enviado não equivale automaticamente a venda concluída ou valor efetivamente recebido.
- **Isolamento multi-tenant desde a base:** cada estabelecimento só pode consultar e alterar seus próprios dados.
- **Nada de dados reais ou segredos no GitHub**, especialmente porque este repositório foi criado como público.

## Documentação canônica

| Documento | Finalidade |
|---|---|
| [Visão do produto](docs/01-VISAO-DO-PRODUTO.md) | Problema, usuários e proposta de valor |
| [Escopo do MVP](docs/02-ESCOPO-MVP.md) | Capacidades incluídas, excluídas e aceites |
| [Arquitetura inicial](docs/03-ARQUITETURA-INICIAL.md) | Componentes e limites técnicos, sem engessar a stack |
| [Requisitos funcionais](docs/04-REQUISITOS-FUNCIONAIS.md) | Jornada e contratos funcionais essenciais |
| [Segurança e privacidade](docs/05-SEGURANCA-E-PRIVACIDADE.md) | Riscos transversais, LGPD e controles mínimos |
| [Decisões e pendências](docs/06-DECISOES-E-PENDENCIAS.md) | Premissas e escolhas ainda abertas |
| [Dados e métricas](docs/07-DADOS-E-METRICAS.md) | Eventos, status, métricas e histórico comercial |
| [Operação e modelo comercial](docs/08-OPERACAO-E-COMERCIAL.md) | Hipóteses de oferta e operação SaaS |
| [Governança ÓRBITA](docs/09-GOVERNANCA-ORBITA.md) | Papéis, gates, branches e evidências |
| [Roadmap](ROADMAP.md) | Etapas, dependências e status |

## Processo de desenvolvimento

O projeto adota o **Método ÓRBITA**: **Planejar → Executar → Evidenciar → Homologar**.

- **Responsável humano:** define direção, prioridades e homologação.
- **Agente de planejamento (ChatGPT):** mantém a fundação documental, prepara tarefas e revisa evidências.
- **Agente de implementação (Codex):** implementa apenas tarefas autorizadas em working copy local, testa e apresenta evidências.
- **GitHub:** mantém documentação, código e histórico persistentes.

A primeira atividade do Codex **não será implementar o aplicativo**, e sim fazer o **bootstrap local seguro** da pasta `vizinho-cardapio-webapp` com o repositório remoto já documentado. Depois disso, cada funcionalidade seguirá uma tarefa delimitada e um gate de homologação.

**Estado atual:** ideia e documentação inicial em preparação; nenhuma funcionalidade implementada, nenhum deploy, nenhum cliente em produção.

## Nota sobre o status da documentação

Esta fundação descreve **propostas de planejamento**, não decisões técnicas automaticamente homologadas. Pontos marcados como pendentes devem ser confirmados pelo responsável antes de se tornarem requisitos fechados. O escopo pode evoluir mediante registro de decisão e atualização do roadmap.

---

**Iniciado em:** 09/10/2026 · **Desenvolvimento assistido por IA sob governança humana**.
