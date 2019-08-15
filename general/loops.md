### Loops

Loops são usados para implementar iteração, existem dois tipos de loop:

- loops infinitos, ou loops sem controle, onde o bloco é executado repetivamente até que seja explicitamente transferido para fora do loop;
- loops controlados onde existe um controle do mesmo por uma variavel.

### Loop infinito

Um simples loop infinito possui a seguinte forma:

```
_loop
    <bloco>
_endloop
```

### Loop finito

Loop finito são controlados por um iterador, no qual em cada iteração um novo valor é atribuido ao iterador.

Exemplo:

```
_for i _over range(1,5)
_loop
     write("2*",i," = ", 2*i)
_endloop
```

Acima criamos a procedure de iteraçao __range__ de 1 a 5 que nosso iterator assumirá 5 valores distintos a cada iteração, ou seja, meu bloco será repetido 5 vezes, o resultado é o seguinte:

```
2*1 = 2     # i vale 1 
2*2 = 4     # i vale 2
2*3 = 6     # i vale 3
2*4 = 8     # i vale 4
2*5 = 10    # i vale 5
```