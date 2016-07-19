build-lists: true

# Introdução ao Swift

### Salmo Junior

---

## Salmo Junior

Mineiro, Chapter Leader do CocoaHeads BH, dev iOS desde 2011, corinthiano, viajante e viciado em queijo.

![right](/Users/salmojunior/Downloads/IMG_1297.JPG)

<br><br><br><br><br><br><br><br>

junior.salmo@gmail.com
@salmojr
			
---

## Agenda

- Declaração e Tipos
- Controles de fluxo
- Struct, Class e Enums
- Níveis de acesso
- Optionals
- Functions, Tuples e Closures
- Extensions, Protocols e Generics

---

## Swift

---

## Swift

* Mais veloz
* Mais segura
* Linguagem "nova"
* Versão atual 2.2
* 3.0 a caminho

---

## Swift

Uma simples linha pode ser considerada um programa em swift.

```swift
print("Olá CocoaHeads Beagá")
```

---

## Declaração

---

## Declaração

As palavras-chave **let** e **var** são utilizadas para indicar elementos que armazenam valores.

* **var** para variáveis
* **let** para constantes

---

## Declaração

```swift
let name = "John"
var age = 25

age = 26

print("Sua idade é \(age)")
```

---

## Declaração

```swift
let name = "John"
let age = 25
let heigth = 1.79

let greeting = "Olá \(name), você tem \(age) anos e sua altura é" 
+ String(format:" %.2f", heigth)
```

---

## Tipos

---

## Tipos

Tipos básicos em Swift

```swift
Int		UInt
Float	Double
Bool	String
```

---

## Tipos

Swift é fortemente tipada. 
Para casos em que o tipo não é passado, ela tentará inferir o tipo ao receber o valor.

---

## Tipos

```swift
//Inferido
let name  = "John"  // String
let age = 25        //Int
let heigth = 1.79   //Double

//Explicito
var explicitInt: Int = Int()
let explicitFlout: Float = 4
let adress: String = "Avenida dos Andradas, 3000 - Sta. Efigênia"
```

---

## Tipos

```swift
//Declarando Arrays
var explicitArray: Array<String> = Array()
var intsArray = [Int]()
var peopleArray = ["John", "Anna"]

//Acessando e atribuindo valores
intsArray[0]
explicitArray.append("John")
explicitArray.last
```

---

## Tipos

```swift
//Declarando Dictionaries
var dictionary: Dictionary<String, Double> = Dictionary()
var personDictionary = [String:String]()

//Acessando Dictionaries
personDictionary = ["name": "John", "age":"29"]
personDictionary["name"] = "Joseph"
personDictionary.removeValueForKey("age")
```

---

## Controles de fluxo

---

## Controles de fluxo

For-in

```swift
for i in 1..>10{
    print(i)
}

for (key, value) in dictionary {
    print(" key: \(key) - Value: \(value)")
}
```

~~`for var x = 1; x <= 10; x++`~~

---

## Controles de fluxo

Do-while

```swift
var z = 10

repeat{
    print("Executei uma vez e sai.")
} while z < 10
```
---

## Struct e Class

---

## Struct e Class

Em Swift, **Class** e **Strutc** tem muito itens em comum

* Podem ter propriedades
* Definir métodos
* Definir inicializadores
* Serem extendidas e adotarem protocolos.
* Ter Subscripts 

---

## Struct e Class 

* Struct - Value Types
* Class - Reference Types

```swift
struct SomeStructure {
    // structure definition goes here
}

class SomeClass {
    // class definition goes here
}
```
---

## Struct 

```swift
struct Point { var x = 0, y = 0 }

var a = Point()
var b = a

b.x = -10

func f(p: Point) {
    var p = p
    p.x = -1
}

f(a)
//a = (x = 0,   y = 0)
//b = (x = -10, y = 0)
```

---

## Class 

```swift
class Point { var x = 0, y = 0 }

var a = Point()
var b = a

b.x = -10

func f(p: Point) {
    let p = p
    p.x = -1
}

f(a)
//a = (x = -1, y = 0)
//b = (x = -1, y = 0)
```

---

## Class 

Mas Classes tem funcionalidades a mais que Structs

* Herança
* Type Casting
* Desinicializadores
* Reference count

---

## Class 

Herança

```swift
class Train: Vehicle {
    override func makeNoise() {
        print("Choo Choo")
    }
}
```

---

## Class 

Inicialização (Designated e Convenience)

```swift
class RecipeIngredient {
    private var quantity: Int
    
    init(name: String, quantity: Int) {
        self.quantity = quantity
    }
    convenience init(name: String) {
        self.init(name: name, quantity: 1)
    }
}
```

---

## Class 

Desinicialização

```swift
class Person{
    let name:String;
    init(name:String){
        self.name = name;
        println("\(name) is being initialized.");
    }
    deinit{
        println("\(name) is being deInitialized.");
    }
}
```

---

## Enums

---

## Enums

Enums em Swift são um pouco mais robustos do que estamos acostumados. Eles podem por exemplo:

* Ser de vários tipos
* Receber paramêtros
* Conformar com protocolos
* Ter propriedades e funções 

---

## Enums

```swift
enum Suit {
    case Spades, Hearts, Diamonds, Clubs
    func simpleDescription() -> String {
        switch self {
        case .Spades:
            return "spades"
        case .Hearts:
            return "hearts"
        case .Diamonds:
            return "diamonds"
        case .Clubs:
            return "clubs"
        }
    }
}
let hearts = Suit.Hearts
let heartsDescription = hearts.simpleDescription()
```

---

## Enums

Enum de caracteres

```swift
enum CompassPoint: Character {
    case North = "N"
    case South = "S"
    case East  = "E"
    case West  = "W"
}

let compassPoint = CompassPoint.West
print("Value = \(compassPoint.rawValue)")
```

---

## Enums

Case com paramêtros

```swift
enum Types {
    case Str(String)
    case Num(Double)
}

var type = Types.Str("hello")
type = .Num(1.0)
```

---

## Enums 

```swift
enum TrainStatus {
    case OnTime
    case Delayed(minutes: Int)
    
    func description() -> String {
        var message: String
        
        switch self {
        case .OnTime:
            message = "Train is on time."
        case .Delayed(let minutes):
            message = "Train is delayed by \(minutes) minute(s)"
        }
        
        return message
    }
}
```

---

## Níveis de acesso

---

## Níveis de acesso

Existem 3 tipos de níveis de acesso

* Public
* Internal
* Private
* ~~Protected~~

---

## Níveis de acesso

```swift
public class SomeClass {
    private var someProperty: Int = 0
    
    internal func someFunc() -> Int {
        return someProperty
    }
}
```

---

## Optionals

---

## Optionals

Forma "elegante" de trablhar com valores nulos (`nil`).

```swift
enum Optional<T> {
  case None
  case Some(T)
}
```

---

## Optionals

Definimos que uma **var** pode ser **nil** atribuindo o símbolo **?**.

```swift
var possibleString: String?
var possibleNum: Int?
```

---

## Optionals

Validando se existe valor utilizando **if-let**

```swift
var possibleNum: Int?

possibleNum = Int("ABC")

if let num = possibleNum {
	//Seguro utilizar "num", existe um valor
}
```

---

## Optionals

Validando se existe valor utilizando **guard-let**

```swift
func someFunc(possibleNum: Int?) {
    guard let num = possibleNum else { return }

    print("Número = \(num)")
}
```

---

## Optionals

Evite fazer **forced unwrapping**

```swift
var possibleNum: Int?

possibleNum = Int("ABC")

print(possibleNum!) // Crash
```

---

## Functions

---

## Functions

Blocos independentes de código que executam uma tarefa específica.

```swift
func sayHello(personName: String) -> String {
    let greeting = "Hello, " + personName + "!"
    return greeting
}

print(sayHello("Anna"))
```
---

## Functions

Os **métodos**  tem a mesma sintaxe das funções, com a diferença que precisam estar ligados a algum tipo.

```swift
class SomeClass {
    static func someTypeMethod() {
        //method implementation goes here
    }
}

SomeClass.someTypeMethod()
```

---

## Functions

Definindo ações de clenup

```swift
func processFile(filename: String) throws {
    if exists(filename) {
        let file = open(filename)
        defer {
            close(file)
        }
        while let line = try file.readline() {
            // Work with the file.
        }
    }
}
```

---

## Tuples

---

## Tuplas

Valores compostos, que possibilitam uma variável ter N valores, podendo ser de tipos diferentes.

```swift
var user: (name: String, email:String, age:Int)
var point = (1, 1)
```

---

## Tuples

```swift
//Indicado - Nomeando paramêtros
var person = (firstName: "John", lastName: "Smith")
var firstName = person.firstName // John
var lastName = person.lastName // Smith

//Não indicado - Acessando por index
var person = ("John", "Smith")
var firstName = person.0 // John
var lastName = person.1 // Smith
```

---

## Tuples

```swift
//Método que retorna uma tuple
func calculateStatistics(scores: [Int]) -> (min: Int, max: Int, sum: Int) {
    var minValue = scores[0]
    var maxValue = scores[0]
    var sum = 0
    
    //...
    
    return (minValue, maxValue, sum)
}

let statistics = calculateStatistics([5, 3, 100, 3, 9])
print(statistics.sum)
```

---

## Tuples

```swift
var tupla = (8, 7, 3)

// Decompondo uma tupla
var (x, y, z) = tupla
print("x = \(x) - y = \(y) - z = \(z)")

// Decompondo uma tupla ignorando alguns argumentos
var (_,_,z) = tupla
print("z = \(z)")
```

---

## Closures

---

## Closures

Blocos independentes de código que podem atuar como variáveis ou funções. São equivalentes aos blocks em Objective-C e callbacks em outras linguagens.

```swift
//Sintaxe de uma closure
{ (parameters) -> return type in
    statements
}
```

---

## Closures

```swift
// Uma closure sem parâmetros que retorna uma String
var hello: () -> (String) = {
    return "Hello!"
}

hello() // Hello!
```

---

## Closures

```swift
// Uma closure que recebe um Int e retorna um Int
var double: (Int) -> (Int) = { x in
    return 2 * x
}

double(2) // 4

// Passando uma closure para uma variável 
var alsoDouble = double

alsoDouble(3) // 6
```

---

## Extensions

---

## Extensions

Adiciona novos comportamentos em Classes, Structs, Enums e Protocols já existentes.

```swift
extension Int {
    var simpleDescription: String {
        return "The number \(self)"
    }
}

print(7.simpleDescription)
```

---

## Extensions

```swift
extension Double {
    var abs: Double {
        get {
            return fabs(self)
        }
    }
}

var testDouble = -10
testDouble.abs // 10
```
---

## Protocols

---

## Protocols

Grupo de propriedades e métodos, sem implementação, que podem ser adotados por Classes, Structs e Enums.

```swift
protocol SomeProtocol {
	var simpleDescription: String { get }
	func doSomethingNonOptionalMethod()
}
```

---

## Protocols

```swift
struct TestStruct: SomeProtocol {
    func doSomethingNonOptionalMethod(){
    }
}

class TestClass: SomeProtocol {
    func doSomethingNonOptionalMethod() {
    }
}

enum TestEnum: SomeProtocol {
    func doSomethingNonOptionalMethod() {
    }
}
```

---

## Protocols

Limitando Protocols somente para Classes

```swift
protocol SomeProtocol: class {
    func doSomethingNonOptionalMethod()
}
```

---

## Protocols

Deixando o código mais organizado e legível

```swift
extension TestClass: SomeProtocol {
    func doSomethingNonOptionalMethod() {
    }
}
```

---

# Dúvidas?
![right, filtered](http://www.konkero.com.br/revistawp/wp-content/uploads/2013/10/Trabalha-como-aut%c3%b4nomo-Tire-11-d%c3%bavidas-sobre-como-contribuir-para-o-INSS.jpg)

---

## Dicas

- Comece brincando com o Playground
- Leia [The Swift Programming Language](https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/GuidedTour.html#//apple_ref/doc/uid/TP40014097-CH2-ID1)
- Fique de olho nas mudanças que estão vindo: [github.com/apple/swift-evolution](https://github.com/apple/swift-evolution)

---

# Faça parte da comunidade :grinning:

### Slack: [iosdevbr.herokuapp.com](http://iosdevbr.herokuapp.com/)
#### [www.cocoaheads.com.br](http://www.cocoaheads.com.br/)

---

# Obrigado!

### junior.salmo@gmail.com

#### @salmojr

