### Entrada/ Saída 

Em magik podemos ler e gravar arquivos txt/csv com as seguites classes.

# external_text_output_stream

```
file << external_text_output_stream.new("path")

file.write('id;status')
file.newline()
file.flush()

file.close()    
```

# external_text_input_stream

```
file << external_text_input_stream.new("path")

_loop
1   line << f.get_line()
    _if line _isnt _unset
        _then 
            write(line)
    _endif
_endloop

file.close()
```
