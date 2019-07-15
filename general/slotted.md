Slotted são declaradas usando a procedure def_slotted_exemplar(:nome, propriedades, _opcional :classe_pai), conforme mostrado no exemplo a seguir:

```
def_slotted_exemplar( 
    :nome_classe, 
    {
        {:nome_propriedade, valor_propriedade}
    } 
)

Exemplo de classe (slotted):

def_slotted_exemplar(
    :pessoa,  
    { 
        { :nome, ""},
        { :sobrenome,  ""},
        { :data_de_nascimento, _unset}
    } 
)

Exemplo de herança:

def_slotted_exemplar(
    :funcionario,
    {
        { :cargo, ""}
    },
    : pessoa
)
```

