Expressões case
===============

Se você já programou em outras linguagens imperativas (C, C++, Java, etc.), sabe do que estou falando. É pegar uma variável e executar blocos de código específicos para cada valor pré-definido e possivelmente definir um bloco padrão no caso dela ter um valor inesperado.

Haskell pega o conceito e o expande. Como o próprio nome sugere, expressões case são, bom, expressões, e muito semelhante com expressões if/else e associações <i>let</i>. Não só podemos testar expressões baseadas em seu valor, como podemos também usar pattern matching. Hmmmmm, pegar uma variável, procurar por um pattern, executar blocos de código para cada resultado... onde já vi isso? Ah claro, pattern matching em parâmetros de funções! Mas isso é só um atalho para executar uma expressão case. Esses dois códigos fazem a mesma coisa, então pode escolher qual você prefere:


Como vê, a sintaxe de expressões case são extremamente simples:


[code]expression[/code] é testada por alguns patterns. Pattern matching funciona exatamente como se presume: o primeiro pattern que verificar-se verdadeiro é executado. Se todo o case for executado e nenhum pattern se encaixar, acontece um runtime error.

Enquanto pattern matching dentro dos parâmetros só podem ser feitos ao definir funções, expressões case podem ser colocadas praticamente em qualquer lugar. Olha só:


Elas são úteis para usar pattern matching no meio de expressões. Já que pattern matching em definições de função são um atalho para expressões case, poderíamos ainda ter feito desse jeito: