
# O que é?

Uma Lambda é um recurso da AWS que permite que funções sejam executadas com base em um trigger. Ou seja, é orientada a eventos, precisando ser acionada de alguma forma. 

Toda lambda precisa de um ambiente de execução (que chamamos de runtime). No caso do nosso projeto, ele já existe, é o nodejs.

Quando uma lambda é instanciada mais de uma vez ao mesmo tempo, nós falamos que temos *duas lambdas rodando de forma concorrente*.

Um ponto muito importante é que uma lambda DEVE ter acesso apenas aquilo que é realmente necessário para que ela funcione. Isso é chamado de ***princípio do privilégio mínimo***.

# Alguns conceitos importantes

- **Cold Start:** quando uma lambda é executada depois de muito tempo de inatividade. Isso faz com que a AWS tenha que gerar um novo container, o que gera latência no serviço.
- **Provisioned Concurrency:** configuração que mantém instâncias ativas de lambdas que não podem passar pelo *cold start*.
