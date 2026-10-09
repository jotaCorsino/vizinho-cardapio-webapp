# Segurança e privacidade

**Baseline inicial.** O projeto ainda necessita validação jurídica e técnica antes de tratar pedidos reais.

## LGPD
**Não exigir cadastro não significa estar fora da LGPD.** Nome, telefone, endereço e observações podem ser dados pessoais tratados para concluir pedidos. Definir responsabilidades de plataforma e estabelecimento, bases e finalidades, transparência, retenção, exclusão e contratos de acordo com a operação real.

## Abordagem de minimização
- Sem conta/senha obrigatória para consumidores.
- Solicitar endereço somente quando for necessária a entrega.
- Guardar preenchimento recorrente no dispositivo **apenas de forma opcional e informada**, com remoção fácil; considerar risco de aparelhos compartilhados.
- Não armazenar cartões ou credenciais do consumidor.
- Reduzir retenção de contato/endereço no servidor; conservar indicadores comerciais sem identificação desnecessária depois do prazo apropriado.
- Tratar análises geográficas com agregação e cuidado com pequenos grupos.

## Controles essenciais
| Risco | Defesa e teste esperado |
|---|---|
| Vazamento entre restaurantes | Autorização por tenant em todos os endpoints; testes negativos de acesso cruzado |
| Falsificação de pedidos | Validação, rate limit, proteção contra automação abusiva e mecanismos adequados |
| Adulteração de preço | Servidor recalcula valores do catálogo vigente |
| Pedidos duplicados | Idempotência ou controle equivalente, integridade transacional |
| Injeção e XSS | Escape, validação, consultas parametrizadas e proteções de sessão/CSRF pertinentes |
| Exposição administrativa | Autenticação, menor privilégio, sessões seguras e recuperação controlada |
| Upload malicioso | Restrições e validação de imagens |
| Vazamento em logs | Redação de dados e controle de acesso |
| Perda de pedidos | Backup, observabilidade, teste de restauração e procedimento de incidente |

## Publicação
O repositório foi criado como **público**. Não versionar credenciais, chaves, arquivos de ambiente reais, dados de clientes, backups, nomes de usuários operacionais nem informações internas. Avaliar privacidade do repositório antes de incorporar infraestrutura comercial; possível case público sanitizado.

## Gate para piloto
HTTPS; gestão de segredos; isolamento tenant; validação e proteção de pedidos; testes negativos; política de retenção; responsabilidades LGPD esclarecidas; backups e restauração testados; riscos críticos resolvidos ou tratados antes de uso real.
