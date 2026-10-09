# Governança pelo Método ÓRBITA

**Referência:** https://github.com/jotaCorsino/orbita-development-model/tree/main/onboarding

## Identidade
Projeto Vizinho — Cardápio Webapp; slug técnico vizinho-cardapio-webapp; projeto de planejamento ChatGPT; implementação Codex; pasta local homônima; GitHub jotaCorsino/vizinho-cardapio-webapp; branch canônica main.

## Responsabilidades
- **Humano:** decide objetivos, prioridades, mudanças e homologação.
- **ChatGPT — planejamento:** analisa, documenta, prepara tarefas, revisa evidências.
- **Codex — implementação:** executa tarefas autorizadas, testa e reporta.
- **GitHub:** estado persistente de documentação, código, decisões e histórico.

## Primeiro ciclo de projeto novo
1. Criar a fundação documental diretamente no GitHub.
2. Apresentá-la e receber homologação do responsável.
3. Responsável cria/abre pasta local no Codex.
4. **Primeira tarefa do Codex é apenas bootstrap local**: validar pasta, Git, origin, baixar/sincronizar main de forma segura e relatar branch/HEAD/status. Não implementar funções.
5. Somente após bootstrap homologado, primeira tarefa funcional.

## Estados de tarefa
PLANEJADA → AUTORIZADA → EM_IMPLEMENTACAO → EM_VALIDACAO → AGUARDANDO_HOMOLOGACAO → CONCLUIDA.

Cada tarefa informa ID, base, objetivo, escopo incluído/excluído, restrições, riscos de segurança, critérios de aceite e evidências. Sem avanço automático nem aumento silencioso de escopo.

## Evidências
Arquivos alterados, testes e falhas, verificação de segurança, limitações, branch, commit, PR e qualquer divergência. Implementação/teste não equivalem à homologação.

## Git e segurança
main representa o estado aceito; branches feat/, fix/, docs/ ou chore/ para mudanças significativas. Não fazer force push, reset destrutivo, exclusão de dados ou merge sem autorização adequada. Repositório público não recebe segredos nem dados reais. Testes multi-tenant negativos serão fundamentais.

## Homologação
APROVADO, APROVADO COM RESSALVAS, CORREÇÃO NECESSÁRIA ou REPLANEJAMENTO NECESSÁRIO.

**Status atual:** fundação inicial para revisão, bootstrap não executado, aplicação não iniciada.
