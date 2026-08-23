# Item 1 da atividade

## Item 1.a: processo e Manifesto Ágil

### Os quatro valores

Os valores do Manifesto Ágil não eliminam os itens à direita; orientam a equipe a valorizar mais os itens à esquerda. Na AgileTech, eles se aplicam assim:

1. Indivíduos e interações mais que processos e ferramentas. Com cinco desenvolvedores e um Product Owner, comunicação direta, decisões coletivas e colaboração diária tendem a resolver dúvidas mais depressa que processos formais. Ferramentas apoiam o trabalho, mas não substituem conversas objetivas.
2. Software em funcionamento mais que documentação abrangente. Como documentos extensos já ficaram desatualizados, a principal evidência de progresso deve ser um incremento executável e testado. Mantém-se documentação suficiente para decisões, uso e manutenção, sem transformá-la em um fim.
3. Colaboração com o cliente mais que negociação de contratos. Os requisitos vagos precisam ser refinados com o cliente e o Product Owner. Como o cliente tem pouco tempo, reuniões curtas, protótipos e critérios de aceitação explícitos aproveitam melhor sua disponibilidade e reduzem interpretações erradas.
4. Responder a mudanças mais que seguir um plano. Mudanças frequentes são esperadas nesse produto. Backlog priorizado, ciclos curtos e revisão a cada Sprint permitem incorporar aprendizado sem insistir em um plano que perdeu valor.

### Escolha da abordagem ágil

O modelo cascata pressupõe maior estabilidade e concentra validação e entrega nas etapas finais. Neste cenário, requisitos vagos e mutáveis aumentariam retrabalho: uma interpretação equivocada poderia atravessar análise, projeto e implementação antes de chegar ao cliente. A documentação extensa também consumiria tempo e voltaria a ficar obsoleta, enquanto a pressão de mercado pede valor demonstrável cedo.

Uma abordagem ágil trabalha em incrementos pequenos, priorizados por valor e avaliados frequentemente. Ela reduz o intervalo entre hipótese e feedback, permite repriorização e torna riscos visíveis cedo. Isso não significa ausência de planejamento ou documentação: ambos são contínuos e proporcionais ao que o produto necessita.

### Práticas para adoção imediata

- Backlog priorizado e histórias de usuário: o Product Owner ordena necessidades por valor, risco e urgência; histórias pequenas recebem critérios de aceitação antes do desenvolvimento.
- Sprints curtas com review: ciclos de duas semanas criam uma cadência de entrega; a review concentra o tempo limitado do cliente na inspeção de software real.
- Integração contínua e testes automatizados: cada mudança integrada passa por testes, reduzindo regressões e mantendo o incremento potencialmente entregável.
- Daily Scrum curta: quinze minutos para inspecionar o avanço rumo à Meta da Sprint e adaptar o plano, sem virar relatório ao gestor.
- Retrospectiva: ao fim de cada Sprint, a equipe escolhe uma melhoria concreta e acompanha seu resultado no ciclo seguinte.

## Item 1.b: programação em pares

Na programação em pares, duas pessoas trabalham juntas sobre o mesmo problema. O piloto escreve o código e mantém atenção na tarefa imediata; o navegador revisa continuamente, antecipa riscos e pensa no desenho. Os papéis são trocados com frequência. A prática oferece revisão em tempo real, compartilhamento de conhecimento, menos dependência de uma única pessoa e descoberta precoce de defeitos. Não dispensa testes nem revisão posterior quando necessária.

Em EAD, a prática enfrenta conexão instável, fusos e agendas diferentes, fadiga de videoconferência, equipamentos desiguais e menor acesso a sinais não verbais. Compartilhar teclado ou ambiente também pode exigir configuração e cuidado com credenciais. Sessões longas agravam o cansaço e podem deixar um participante apenas observando.

Duas adaptações viáveis são:

1. Pareamento remoto síncrono em blocos curtos: sessões de 45 a 60 minutos por compartilhamento de tela ou edição colaborativa, objetivo pequeno, papéis alternados a cada 15–20 minutos e pausas entre blocos. A agenda é combinada com antecedência.
2. Pareamento assíncrono por revezamento: uma pessoa implementa uma etapa pequena e registra contexto, dúvidas e testes; a outra revisa e continua em um commit separado. Um encontro breve resolve divergências. Preserva a colaboração quando os horários não coincidem, embora o feedback não seja instantâneo.

## Item 1.c: dificuldades essenciais de Brooks

As quatro dificuldades existem em software, mas três se destacam neste caso:

- Mutabilidade (mais relevante): requisitos e prioridades mudam frequentemente porque o produto e o mercado evoluem. Backlog reordenável, Sprints curtas e reviews tornam a mudança incremental e controlada.
- Invisibilidade (muito relevante): software e seu progresso não são naturalmente visíveis; requisitos vagos ampliam o problema. Quadro Kanban, metas de Sprint, incrementos demonstráveis e testes tornam estado, limites e resultados observáveis.
- Complexidade (muito relevante): regras e interações se acumulam mesmo em um sistema pequeno. Histórias pequenas, design simples, refatoração, testes e programação em pares ajudam a controlar essa complexidade sem fingir eliminá-la.
- Conformidade (relevante à medida que surgem integrações): o sistema web terá de respeitar interfaces, regras de negócio e possivelmente normas externas. Critérios de aceitação, Definition of Done, testes de integração e feedback especializado verificam essa adequação cedo.

Métodos ágeis mitigam essas dificuldades por inspeção e adaptação frequentes, comunicação e entregas incrementais. Eles não removem as dificuldades essenciais, especialmente a complexidade inerente ao domínio, mas reduzem descoberta tardia, trabalho especulativo e custo de correção.
