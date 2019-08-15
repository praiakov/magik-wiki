### Slotted

Slotted são declaradas usando a procedure def_slotted_exemplar(:nome, propriedades, _opcional :classe_pai), conforme mostrado no exemplo a seguir:

```
def_slotted_exemplar( 
    :nome_classe, 
    {
        {:nome_propriedade, _opcional valor_propriedade}
    } 
)

```

Usando herança:

```
def_slotted_exemplar(
    :funcionario,
    {
        { :cargo, ""}
    },
    : pessoa
)
```

Exemplo de slotted:

```
def_slotted_exemplar(
    :pessoa,  
    { 
        { :nome, ""},
        { :sobrenome,  ""},
        { :data_de_nascimento, _unset}
    } 
)

```

### Criando instância de uma classe (slotted)

Neste exemplo estamos inicializando o slotted com valores, para criarmos um novo objeto classe __pessoa__ criamos um método no qual passamos nome e sobrenome como parametros, no escopo desse método retornamos o clone desse slot usando o prefixo ___clone__ que tem o objetivo de construir um novo objeto, e inicializamos esse objeto __init()__ passando nossos parametros como argumentos.

```
_method pessoa.new(nome, sobrenome)
    >> _clone.init(nome, sobrenome)
_endmethod
$
```

Outra opção é criar o método de instância e inicializador em métodos distintos.

```
_method pessoa.new()
    >> _clone
_endmethod
```

```
_method pessoa.init(nome, sobrenome)
    .nome << nome;
    .sobrenome << sobrenome
    >> _self
_endmethod
```

### Getters e setters

Os slots podem serem acessados diretamente usando a seguinte sintaxe:

```
.<slot_nome>
```

Exemplo GET:

```
_method pessoa.get_slots()
    >> .nome, .sobrenome
_endmethod 
```

Atualizando os valores do objeto. 
Exemplo SET:

```
_method pessoa.set_slots(novoNome, novoSobrenome)
    .nome << novoNome
    .sobrenome << novoSobrenome 
_endmethod
```

Outra forma de acesso aos slots é utilizando __define_slot_access__, sua sintaxe é a seguinte:

```
    slotted_format_mixin.define_slot_access( name, flag, _optional flavour, owner_name )
```

Abaixo a tabela de modificadores de acesso:

| flag  | flavour | get | set | boot |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| :read or :readable  | __:public__ or _false_  | public | no method | no method |
| :read or :readable  | __:private__ or _true_  | private | no method | no method |
| :write or :writable  | __:public__  | public | public | public |
| :write or :writable  | __:readonly__  | public | private | private |
| :write or :writable  | __:private__ | private | private | private |

Exemplo:

```
employee.define_slot_access(:nome, :write)
``` 
