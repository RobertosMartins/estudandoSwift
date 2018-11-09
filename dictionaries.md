
## Dictionaries

Também é uma coleção de variáveis com chave e valor do mesmo tipo de forma NÃO ORDENADA. Pode ser comparado ao dicionário onde atráves de uma chave(palavra) é encontrado sua definição(Valor).

Key = Única

#### Exemplo
```swift

//var dicionarioInglesPortugues = [String : String]()
var dicionarioInglesPortugues = Dictionary<String,String>()
dicionarioInglesPortugues = ["red":"Hot Chili Peppersr","green":"Verde" ,"blue":"Azul"]

//Busca todas as keys(Chaves) presentes no dicionário
print(dicionarioInglesPortugues.keys)
//Busca todos os valores presentes no dicionário
print(dicionarioInglesPortugues.values)

if dicionarioInglesPortugues["red"] != "Vermelho" {
    print("Red "+"\(dicionarioInglesPortugues["red"]!)" + " não é uma cor é uma banda")
    dicionarioInglesPortugues.updateValue("Vermelho",forKey:"red")
}

for (key,value) in dicionarioInglesPortugues{
//Mostra todas as chaves e valores contidos no dictionary
print("|Chave:\(key)| Valor: \(value)|")
}

```
### Métodos

- insert - Adiciona um item no set. 
- count - Conta o numero de itens da lista.
- isEmpty - Verifica se a lista esta vazia (Bool)
- remove - Remove um item do set 
- contains - Verifica se um item esta contido na lista
```swift
letrasSet.contains("a") //true ou false
```
- sort() - Ordena os valores contidos no set
```swift
letrasSet.sorted() //Sorteia fora da ordem
letrasSet.sorted(by: >) //Ascendente
letrasSet.sorted(by: <) // Descendete
```

 [⏭️ **Dictionaries**](https://github.com/RobertosMartins/estudandoSwift/blob/master/dictionaries.md)
