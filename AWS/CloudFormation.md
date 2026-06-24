
--- 
# O que é

É um serviço de IaC, que se baseia em **Templates**, **Stacks** e **Change Sets**. Seu principal foco é a diminuição do tempo de desenvolvimento, onde o programador poderá subir toda a infraestrutura e provisionar todos os recursos necessários via código.

Com o Cloud Formation, é possível planejar os recursos através de um **template**, este será responsável por todas as informações necessárias do recurso que está sendo deployado. Depois de criar um template de um ou mais recursos, pode ser criado uma **stack**. A stack é a implementação destes recursos. Toda stack deve sempre ser baseada em um template.

O **change set** é utilizado quando é preciso atualizar algo dentro de uma stack. Ele é criado e o usuário pode analisar todas as alterações que são feitas e como será o impacto delas.

## Termos

- ***Template***: base dos recursos que serão provisionados (como EC2, Lambdas)
- ***Stack***: implementação de um template, aplicação/provisionamento de todos os recursos.
- ***Change Set***: informações sobre tudo aquilo que será alterado e como será seu impacto.

# Drift e Proteção

O **drift detection** é um conceito importante no CloudFormation. Basicamente, ele é o que identifica se algo foi alterado no projeto via console da AWS (e não está salvo no código). O maior foco de toda equipe de **SRE (Equipe responsável por garantir a integridade do projeto de infra no desenvolvimento)** é sempre manter o *drift* em **zero***.

Outro conceito importante é o **termination protection**. Ele é uma flag adicionada que garante que uma stack seja deletada acidentalmente. É muito importante em recursos críticos, como de rede ou banco de dados.

Temos também as **deletion policies** que servem para definir o comportamento de algum recurso se sua stack for deletada. Um exemplo é um banco de dados, onde você pode definir que ele não deve ser excluído caso sua stack seja. Pode também ser configurado para que seja feito um snapshot do recurso.
