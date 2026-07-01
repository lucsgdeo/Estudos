
# O que é?

Um conceito muito importante no desenvolvimento é o tracing/tracer. Se consiste em trackear toda uma requisição feita. 

Como nos modelos de microsserviços e serverless uma requisição pode passar por diversos serviços diferentes até que apresente o resultado, o traçar o caminho dela é essencial para que o processo de debug e de entendimento seja efetuado. É muito importante saber seu ponto de origem e por onde "percorreu".

Dentro da AWS, usamos um serviço chamado de **X-Ray**, que é um serviço da Amazon que gera um *Service Map* - isto é - um mapa visual de todo o caminho de uma requisição.

Além de tudo já dito, é muito importante ter um **ID de Correlação**. Este ID irá no cabeçalho de todos os serviços que ele passar para que tenha um fácil rastreio dentro do **Cloud Watch**.

***"Fazer um rastro de uma requisição"***
