# Item 2 da atividade

## Item 2.a: quadro e processo de trabalho

### Quadro no GitHub Projects

O quadro usa as colunas Backlog, Pronto para a Sprint, Em desenvolvimento, Em revisão/testes e Concluído. Para evitar trabalho demais em aberto, aplica-se limite de duas histórias em desenvolvimento e duas em revisão/testes.

Cards iniciais:

1. US01 - Cadastrar usuário: como visitante, quero criar uma conta com nome, e-mail e senha para acessar o sistema.
2. US02 - Fazer login: como usuário cadastrado, quero entrar com e-mail e senha para acessar minha conta.
3. US03 - Listar projetos: como usuário, quero visualizar meus projetos para escolher em qual trabalhar.
4. US04 - Criar projeto: como usuário, quero criar um projeto com nome e descrição para organizar o trabalho.
5. US05 - Criar tarefa no projeto: como membro, quero registrar uma tarefa com título e responsável para tornar o trabalho visível.
6. T01 - Configurar integração contínua: executar os testes automaticamente em cada mudança proposta.

Cada história deve conter critérios de aceitação, prioridade e estimativa. Um card entra em Pronto para a Sprint quando estiver pequeno e compreendido; passa por desenvolvimento em par, testes e revisão antes de Concluído. A coluna final exige o atendimento da Definition of Done.

> Link do GitHub Projects: `PENDENTE - inserir a URL real após criar e publicar o quadro no repositório da entrega.`

O link não pode ser inventado: ele depende do repositório e da conta GitHub em que a entrega será publicada.

### Práticas de XP

1. Programação em pares: piloto e navegador alternam papéis para produzir e revisar o código continuamente.
2. Desenvolvimento orientado a testes (TDD): quando aplicável, escreve-se primeiro um teste que falha, depois o código mínimo que o faz passar e, por fim, refatora-se.
3. Integração contínua: mudanças pequenas são integradas frequentemente e validadas por uma execução automatizada.
4. Design simples: implementa-se a solução mais simples que atende às histórias atuais, evitando antecipação (YAGNI).
5. Refatoração contínua: a estrutura interna é melhorada sem alterar o comportamento, apoiada por testes.
6. Propriedade coletiva do código: qualquer integrante pode melhorar qualquer parte, respeitando revisão, testes e padrões acordados.
7. Pequenas versões: cada Sprint busca um incremento utilizável e potencialmente entregável.

### Integração entre XP e Scrum

Scrum organiza o trabalho: o Product Owner ordena o Product Backlog; a equipe define a Meta e seleciona itens na Sprint Planning; Daily, Review e Retrospective promovem inspeção e adaptação. XP orienta como construir com qualidade dentro desse ciclo. Histórias e critérios são refinados antes da Sprint; durante a implementação, pares usam TDD, integração contínua, design simples e refatoração. A pequena versão resultante é inspecionada na Review. Problemas técnicos e de colaboração alimentam a Retrospective.

Para cobrir as responsabilidades do framework sem aumentar agora a equipe, um dos cinco profissionais de desenvolvimento assume também a responsabilidade de Scrum Master, facilitando eventos e ajudando a remover impedimentos. O Product Owner responde por valor e ordenação do backlog; os Developers respondem pelo plano e pela qualidade do incremento. O acúmulo será reavaliado nas retrospectivas caso prejudique qualquer uma das responsabilidades.

Um item só integra o incremento quando cumpre a Definition of Done: critérios aceitos, testes passando, código integrado e revisado, documentação essencial atualizada e incremento demonstrável. O quadro visualiza o fluxo, mas não substitui os eventos nem os papéis do Scrum.

### Fluxo semanal

- Segunda-feira: na primeira semana ocorre a Sprint Planning; nas demais, refinamento curto do backlog. A equipe confirma objetivos técnicos e forma pares.
- Todos os dias úteis: Daily Scrum de 15 minutos; desenvolvimento em pares, TDD, refatoração e integração de mudanças pequenas ao longo do dia.
- Durante a semana: Product Owner esclarece critérios; cards avançam conforme evidência real, respeitando limites de trabalho em progresso.
- Sexta-feira: verificação do incremento e integração, sem criar uma “fase de testes” isolada. Na segunda sexta-feira acontecem Sprint Review e Retrospective.

## Item 2.b: Sprint e comparação entre métodos

### Cronograma da Sprint

| Quando | Atividade e duração | Participantes | XP e resultado esperado |
|---|---|---|---|
| Dia 1, 9h | Sprint Planning - 2 h | Todo o Scrum Team: Product Owner, Scrum Master e Developers | Definir Meta da Sprint, selecionar histórias, esclarecer critérios, dividir histórias grandes e combinar pares. |
| Dias 1–10, 9h | Daily Scrum - 15 min | Developers; Scrum Master e PO participam se estiverem trabalhando em itens da Sprint | Inspecionar progresso rumo à meta, ajustar o plano e expor impedimentos. |
| Dias 1–9 | Desenvolvimento | Desenvolvedores | Pares alternados, TDD, design simples, refatoração, propriedade coletiva e integração contínua. |
| Dias 2–9 | Refinamento - até 1 h por semana | Product Owner e desenvolvedores | Preparar itens futuros sem alterar silenciosamente o escopo da Sprint. |
| Dia 5, 16h | Checagem intermediária - 30 min | Desenvolvedores e PO | Demonstrar progresso quando útil, validar dúvidas e reduzir risco; não é evento obrigatório do Scrum. |
| Dia 10, 14h | Sprint Review - 1 h | Scrum Team e cliente/stakeholders | Demonstrar o incremento funcionando, colher feedback e adaptar o Product Backlog. |
| Dia 10, 15h15 | Sprint Retrospective - 1 h | Todo o Scrum Team | Inspecionar processo e qualidade; escolher uma melhoria concreta para a próxima Sprint. |

Ao final, espera-se um incremento potencialmente entregável com as histórias aceitas, código integrado, testes passando e documentação essencial atualizada. Cards incompletos não contam como entrega e retornam ao Product Backlog para nova priorização; não recebem “percentual de pronto”.

### Comparação entre Scrum e Kanban

| Aspecto | Scrum | Kanban | Combinação proposta |
|---|---|---|---|
| Quando usar | Produto complexo que se beneficia de metas, feedback e cadência fixa | Trabalho contínuo, demanda variável ou suporte, em que fluxo e tempo de atendimento predominam | Scrum dá cadência e objetivo; Kanban torna o fluxo da Sprint visível. |
| Organização | Sprints com duração fixa e Meta da Sprint | Fluxo contínuo, sem iterações obrigatórias | Mantêm-se Sprints de duas semanas e acompanha-se cada item no quadro. |
| Papéis | Define Product Owner, Scrum Master e Developers | Não prescreve papéis específicos | Preservam-se responsabilidades Scrum e políticas explícitas no quadro. |
| Mudanças | Sprint Backlog é adaptado sem colocar em risco a Meta | Itens podem ser puxados conforme capacidade e política | A equipe puxa trabalho selecionado para a Sprint e negocia alterações que ameacem a meta. |
| Controle | Inspeção em eventos e compromisso com metas | Limites de WIP e métricas de fluxo, como lead time e cycle time | Eventos avaliam produto/processo; limites de WIP evitam iniciar trabalho demais. |
| Entrega | Incremento utilizável ao menos por Sprint | Pode ocorrer continuamente | Integração contínua permite entregar cedo; a Review inspeciona o incremento agregado. |

Essa combinação é frequentemente chamada de Scrumban, mas aqui o nome importa menos que as políticas: meta e eventos do Scrum, fluxo puxado e WIP limitado do Kanban, com práticas técnicas de XP sustentando a qualidade.
