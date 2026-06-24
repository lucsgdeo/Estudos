# Introdução

Temos três princípios importantes:
- **Design**
![[Pasted image 20260623191930.png|316]]

- **Implementação**
![[Pasted image 20260623192019.png|326]]

- **Arquitetura**
![[Pasted image 20260623192043.png|324]]

Hoje, Vária linguagens utilizam a JVM

Garbage Collector é muito importante na JVM

É melhor ter vários objetos menores, pois melhora o gerenciamento de memória
- **Hipótese das gerações:** 95% dos objetos criados viram lixo rapidamente (*mortalidade infantil*); 

O Java usa um algoritmo de Garbage Collection chamado de **generation copying**. Neste algoritmo, a memória é dividida em duas partes (yong e old). Objetos são salvos primariamente na yong e, assim que fica cheia, o GC lê objetos inúteis e limpa sua referência de memória. Após isto, ele salva os objetos sobreviventes na memória old, fazendo assim com que a yong fique limpa. De tempos em tempos, ele também lê a old e remove todos os objetos desnecessários.

heap é o nome dado a area da memória reservada pela JVM.
- -xms: tamanho incial
- -xmx: tamanho máximo

Uma vez definido, o tamanho da heap nunca é devolvido ao sistema.
A memória é usada dinamicamente, mas se extrapolar o máximo permitido 
(-Xmx), ele lança um erro *OutOfMemoryError*

É muito importante saber como se trabalhar bem na memória de uma aplicação

**pg:** 41