## Set

Também é uma coleção de variáveis do mesmo tipo e que adiciona valores DISTINTOS, porém de forma NÃO ORDENADA.

#### Como eu garanto que um valor é Único no Set???

De acordo com a documentação oficial o tipo do valor de um elemento no set deve ser hashable na ordem que é adicionado para que seja único.

Hashable - Quer dizer que o tipo de um elemento do set tem um valor inteiro único que o determina.(Identificador) 

#### Pegadinha quantos itens eu vou mostrar no Set e quantos vou mostrar no Array

```swift

var letrasSet = Set<Character>()

letrasSet.insert("a")
letrasSet.insert("B")
letrasSet.insert("a")

for letra in letrasSet {
    print(letra) 
}

print("Quantidade de itens dentro do SET \(letrasSet.count) items.")
print("-------------------------------------------------------------------.")

var letrasArray = Array<Character>()
letrasArray.append("a")
letrasArray.append("B")
letrasArray.append("a")

for letra in letrasArray {
    print(letra) 
}
print("Quantidade de itens dentro dO ARRAY \(letrasArray.count) items.")
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
### Operação entre Sets
![Imagem das operações com Set](https://docs.swift.org/swift-book/_images/setVennDiagram_2x.png)

### Exemplo
```swift
let numerosPares: Set = ["0","2","4","6","8","10"]
let numerosImpares: Set = ["1","3","5","7","9"]
let numeroPrimos: Set = ["2","3","5","7"]

var numerosUnidos: Set<String> = numerosPares.union(numerosImpares)
// [0, 1, 2, 3, 4, 5, 6, 7, 8, 9,10]

print(numerosPares.isSubset(of: numerosUnidos))
// true - Os números pares estão CONTIDO no conjunto união

print(numerosUnidos.isSuperset(of: numerosPares))
// true - Os números Unidos CONTÉM os numeros pares

print(numerosPares.isDisjoint(with: numeroPrimos))
// false - Pois no conjunto dos números primos tem o elemento 2 que é o mesmo que no números Unidos
```

 [⏭️ **Dictionaries**](https://github.com/RobertosMartins/estudandoSwift/blob/master/dictionaries.md)
