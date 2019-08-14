Herança é o mecanismo que herda características e comportamentos de uma __superclasse_.

Por exemplo, a classe __funcionario__ (subclasse) é uma especialziação de __pessoa__ (superclasse), herda seus atributos e comportamentos.

```
#criação do slotted Pessoa
def_slotted_exemplar(:pessoa,
    {
        {:nome, ""},
        {:sobrenome, ""}
    }
)
```

```
_method pessoa.andar()
    write("andando...") 
_endmethod
```

```
#criação do slotted funcionario que herda todas as características, assim como seu métodos da classe pessoa
def_slotted_exemplar(:funcionario
    {
        {:cargo, ""}
    },
    :pessoa
)
```

Assim como podemos acessar o método __andar__ definido na superclasse __pessoa__, também temos acesso na subclasse __funcionario__.

>MagikSF> funcionario.andar()

_Obs:Para sobrescever o método na subclasse basta definir subclasse.metodo(), a sobrescrita é implicita._



