# JIT vs AOT

Para que uma linguagem de programação possa ser executada por uma máquina primeiramente ela precisa ser traduzida para linguagem de máquina, tendo em vista
que um computador não vai saber 'ler' linhas de código escritas em java, python ou c++. Nesse artigo vamos ver duas técnicas de compilação (tradução para linguagem
de máquina).

## JIT (Just In Time)
Nessa abordagem o código de um programa só é traduzido/compilado quando ele for requisitado. Ou seja, enquanto um trecho de código não for usado, ele não será 
compilado.

JIT é uma combinação de duas abordagens de tradução para código interpretado pela máquina: AOT e intepretador. Usa da velocidade de um código **compilado** e da
flexibilidade de **interpretação** de código.

Esse tipo de abordagem causa um certo delay na execução inicial do da aplicação, uma vez que o código precisa ser carregado e compilado para bytecode. 

## AOT (Ahead Of Time)

Nessa abordagem a ideia é traduzir todo o código de alto nível para linguagem nativa antes de executar qualquer parte dele. Ou seja, pegando como exemplo um código
em c: toda a aplicação escrita em c vai ser traduzida para linguagem de máquina, transformada num arquivo binário resultante. E então esse arquivo vai poder ser
executado nativamente, fazendo com que a aplicação seja executada com fluidez sem precisar de sobrecarga de tempo de compilação em *runtime*.


## Use-case: JIT e AOT no Angular

O framework angular é escrito em typescript e, como sabemos, o código em typescript precisa ser convertido para javascript para que possa ser entedido pelo
browser. Angular nos dar duas possibilidades de compilação:
- JIT:
  O codigo é compilado no próprio browser e cada arquivo é compilado de forma separada.
- AOT:
  Compilado pela máquina. Todo o código é compilado junto: HTML, CSS nos scripts. Como a compilação é feita ainda na máquina antes de ir ao browser, o compilador
  não precisa der deployado, o que vai resultar em uma grande redução no tamanho.
  
