# Coleções

As coleções são estruturas de dados indexadas que podem ser acessadas usando índices e chaves. Portanto as coleções tem capacidade de colecionar objetos.

### simple vector

É uma coleção indexada de objetos, possui um tamanho fixo, seus elementos são acessados por indíce.

```
MagikSF > a << simple_vector(10)
MagikSF > a[1] << "Um"   # atribuido o valor 'um' ao indice 1 do vector
```

### rope

Uma outra coleção indexada, no qual difere de __simple_vector__ pois possui um tamanho flexível, podendo aumentar ou diminuir.

```
MagikSF > a << rope.new(2)
MagikSF > a[3] << "Três" # atribuido o valor 'três' ao indice 3 da coleção
```
_Obs: Essa coleção é flexível, pode adicionar mais itens a lista, rope.size + 1. No exemplo acima declaramos um rope de 2 posições e atribuimos o valor 'três' na terceira posição, caso tente atribuir na quarta ocorrerá uma exceção_

### stack (pilha)

Baseia no princípio LIFO (last in/first out), elementos são adicionados no fim (topo) da pilha e também removidos do topo.

```
MagikSF > a << stack.new()
MagikSF > a.push(1) # adicionamos o elemento 1 na pilha
MagikSF > a.push(2) # adicionamos o elemento 2 na pilha
MagikSF > a.push(3) # adicionamos o elemento 3 na pilha
MagikSF > print(a)  # agora nossa pilha tem os seguintes elementos, onde 3 é o último elemento da mesma, logo será o primeiro a sair.
stack:
3
2
1
MagikSF > a.pop()   # removemos o último elemento de nossa pilha
MagikSF > print(a)  # agora nossa pilha está representada da seguinte maneira
stack:
2
1
```

### queues (fila)

Outra coleçção ordenada, que parte do princípio FIFO (first in/ first out), ou seja, o primeiro elemento adicionado é o primeiro a sair também.

```
MagikSF > a << queue.new()
MagikSF > a.add(1) # adicionamos o elemento 1 na fila
MagikSF > a.add(2) # adicionamos o elemento 2 na fila
MagikSF > a.add(3) # adicionamos o elemento 3 na fila
MagikSF > print(a) # agora nossa fila tem os seguintes elementos, onde 1 é o primeiro elemento da mesma, logo será o primeiro a sair da coleção.
queue:
1
2
3
MagikSF > a.next() # o primeiro elemento é retirado da coleção
MagikSF > print(a) # agora nossa fila está representada da seguinte maneira
MagikSF >  
queue:
2
3
```