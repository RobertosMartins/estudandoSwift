## Array

Serve para armazenar na ordem uma coleção de variáveis, como se fosse um "caixa" com vários compartilhamentos para variáveis do MESMO tipo. Elas podem ser variáveis(mutáveis = podem ser alteradas) o imutáveis(lista de constantes).

```swift
var arrayNumeros = [Int]() //Instância um array que receberá o tipo Inteiro, também podemos usar Array<String>()
 
arrayNumeros.append(100)   // Adiciona valor
arrayNumeros.append(200)
arrayNumeros.remove(at: 0)  // Remove o primeiro 100
print("arrayNumeros tem apenas \(arrayNumeros.count) item.")

arrayNumeros = []           // Zera a lista, mas continua esperando números
print(arrayNumeros.count)   // apresenta o número de elemetos 0 zero
```
### Unindo dois arrays

```swift
let agenteNumeroSecreto = Array(repeating: 0, count: 2)
let numeroIdentificadorAgente = [7]
print("James Bond")
print(agenteNumeroSecreto + numeroIdentificadorAgente)
```
### Criando Arrays com Literal
```swift
let hamburguersBigMac = Array(repeating:"Hamburguer",count:2)
let itensBigMac = ["Alface", "Queijo","Molho Especial","Cebola", "Picles","Pão com Gergelim"] // Todos os itens setados na inicialização do array são do tipo String
print(hamburguersBigMac + itensBigMac) 
```
### Métodos

- append - Adiciona um item na lista. Também pode ser usado 
```swift 
lista += ["outros item"]  
```
- insert - Adiciona um item em uma determinada posição na lista. 
```swift
lista.insert("Item", at: 0) //posição 
```
- remove -   Remove o itens de acordo com o index (at:0) 
- removeAll() - Remove todos os itens
- isEmpty - Verifica se a lista esta vazia (Bool)
```swift
let hamburguersBigMac = Array(repeating:"Hamburguer",count:2)
let itensBigMac = ["Alface", "Queijo","Molho Especial","Cebola", "Picles","Pão com Gergelim"]
var bigMac = hamburguersBigMac + itensBigMac  //Foi retirado o let = constante e trocado por var

bigMac = [];  // Esta linha zera os itens da lista, caso queria que seja retornado o else comente 
if bigMac.isEmpty {
   print("Cade meu BigMac???") 
} else {
   print("Obrigado Volte Sempre!") 
   ```
 - Recuperar um item pelo index  
 ```swift
 var primeiroItem = bigMac[0]  // Hamburguer
 ```
- Troca o valor de um item
 ```swift
 if(bigMac[6] == "Picles"){
print("Troca o Picles por ketchup, por favor")
}
bigMac[6] = "Ketchup"
print(bigMac) //["Hamburguer", "Hamburguer", "Alface", "Queijo", "Molho Especial", "Cebola", "Ketchup", "Pão com Gergelim"]
  ```
- Adicionar valor no final do Array 
```swift
bigMac[bigMac.count] = "Mostarda"
```
- removeLast - Remove um item do final
- enumerated() - Cria uma matriz de chave e valor para cada items.
```swift
for (index, value) in bigMac.enumerated() {
    print("Item \(index + 1): \(value)")
}
```
### Iterar sobre os itens do Array (Percorrer sobre cada item dentro do Array)
```swift
for item in bigMac {
    print(item) // Alface Queijo Molho Especial Cebola Picles Pão com Gergelim
}
```
## Set

Também é uma coleção de variáveis do mesmo tipo e que adiciona valores DISTINTOS, porém de forma NÃO ORDENADA.

#### Como eu garanto que um valor é Único no Set???

De acordo com a documentação oficial o tipo do valor de um elemento no set deve ser hashable na ordem que é adicionado para que seja único.

Hashable - Quer dizer que o tipo em um set tem um valor inteiro único que o determina 

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
