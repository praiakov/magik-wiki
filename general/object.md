### Objeto

Em Magik tudo é objeto, por exemplo o número 6 é um objeto inteiro e pode invocar mensagens ([método](method_procedure.md)), por exemplo:

```
MagikSF > 6.cubed
MagikSF > 36
```

Retorna o cubo de 6, que é 36.

Objetos nada mais são que a representaçao de uma classe, no exemplo acima o 6 que é um objeto inteiro pertencente a classe integer.

Alguns exemplos: 

Objeto | Classe 
 --- | --- 
2.0, 3.0e5 | float 
1, 2, 3 | integer
_true, _false | true and false 
%a, %g |  character 
{8, 4, 7, 3, 8, 6} | simple_vector  
“To be or not to be” | char16_vector

As classes de objetos se dividem em três categorias:
### enumerated
Um inteiro é um exemplo de classe enumerated.

### indexed
Um simples vetor é uma instância de uma classe indexed.

### slotted
Similar ao class no C#, uma abstração do mundo real ou não que possuem características em comun e comportamentos, em magik é definido como slotted [slotted exemplar](slotted.md).
