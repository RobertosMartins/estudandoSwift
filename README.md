# Estudando Swift 
O objetivo deste repositório e compartilhar conhecimentos básicos de swift

[Referência](https://docs.swift.org/swift-book/LanguageGuide/TheBasics.html)

[IDE On-line para executar os códigos ](http://online.swiftplayground.run/)

# Básico 

Swift é a linguagem de programação para dispositivos da apple.
* Type-safe - é um linguagem que assegura os tipos de valores que queremos trabalhar
```swift
var diasAno = 365  //OK
var diasAno = "trezentos e sessenta e cinco"  //Erro: O tipo informado anteriormente é um inteiro
```
* Padrão de nomeclatura lowerCamelCase


| Tipo| Exemplo      |
| ----|:------------:|
| Int| 100 |
| Double| 3,141516 |
| Float| 1,99 |
| Bool| true ou false |

*Float e Double. A diferença entre o float e o double é a precisão, ou seja, o quanto varia, o quanto consegue expressar um valor próximo do real, é o número de casas decimais que ele consegue suportar*

## Constants and Variables

**Variável** - Pode ser entendida como o nome dado a um espaço de memória que armazenará um valor TEMPORÁRIO.
```swift
var nome = 'Roberto'
```
**Constante** - Pode ser entendida como o nome dado a um espaço de memória que armazenará e não será alterado enquanto o seu sistema existir.
```swift
let numeroPI = 3,14
```
Obs: 
* Toda variável deve ser instânciada com um valor ou dever indicar seu tipo(**Annotation**)
* Dê preferência pelo uso de constantes, pois o swift otimiza o uso delas.

```swift
var inteiro:int  //Esta variavel receberá um inteiro
```
[Coleções](https://docs.swift.org/swift-book/LanguageGuide/CollectionTypes.html)

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

* Set  


* Dictionary





