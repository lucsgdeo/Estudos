

# O que é?

O CDK é um framework que serve para modelar e criar recursos da AWS de maneira simples e organizada. Se baseia em Stacks, onde todo o deploy pode ser feito via código, pulando parte da complexidade que seria fazer esta tarefa via AWS Console e centralizando os recursos daquele serviço.

O CDK gera stacks no ClouFormation.

Toda classe que estender uma Stack *será uma nova Stack*.

# Outros pontos importantes

O Amazon CDK não faz deploy direto do código em Typescript. Para isto, ele passa por ***4 etapas***:

1. **Construction:** o código é executado e a Construction Tree é montada na memória.
2. **Preparation:** os constructions fazem os últimos ajustes e validações necessárias.
3. **Synthesis:** transforma a lógica em um template do CloudFormation.
4. **Deployment:** os templates são transformados em stacks e, finalmente, são instanciados os recursos dentro da AWS.

--- 
# Comandos

- `cdk init --language typescript`
- `cdk list`
- `cdk deploy --all`
- `cdk diff`
- `cdk destry --all`
- `cdk destroy --all`
