# JavaScript Fundamentals: Data Types

Omówienie podstawowych typów w JavaScript.

## Typy w JavaScript 
**Wyróżniamy osiem typów podstawowych**. JavaScript jest językiem dynamicznie typowanym (*ang. dynamically typed*) - umożliwia **przypisanie do jednej zmiennej wartości różnych typów**.

## Numbers
#### Reprezentacja liczb
>Reprezentuje **integer** i **floating point numbers**. 

#### Special numeric values
>Zawiera *special numeric values*: `Infinity` (większe od każdej liczby), `-Infinity` (mniejsze od każdej liczby), `NaN` (błąd przetwarzania *ang. computational error*).  

#### Bezpieczeństwo operacji matematycznych
>**Operacje matematyczne są bezpieczne**, co oznacza, że nigdy nie otrzymamy błędu krytycznego kończącego wykonywanie skrypt *ang. fatal error*. W najgorszym przypadku dostaniemy `NaN`.

#### Przedział liczbowy
>Integer ∈ <-<sup>53</sup>-1, 2<sup>53</sup>-1>

## BigInt
#### Reprezentacja liczb
>Umożliwia pracę z liczbami o losowej długości.  
Aby go użyć należy dołączyć *n* na końcu liczby.

```javascript
const bigInt = 1234567890123456789012345678901234567890n;
```

## String
#### Sposób zapisu
W JavaScript, są 3 typy quotes.
1. Double quotes: "Hello".
2. Single quotes: 'Hello'.
3. Backticks: \`Hello\`.  

## Boolean
Przechowuje wartości logiczne `true` i `false`.  
Jest zwracany jako wynik **operacji porównania** (*ang. comparisons*).

## Null
Oddzielny typ reprezentujacy *"nothing"*, *"empty"*, *"value unknown"*.

## Undefined
Oznacza wartość nie posiadajacą przypisania (*ang. not assigned*), gdy zmienna jest zadeklarowana, ale nie posiada 
przypisanej wartości.

```javascript
let a; // undefined
```

#### Undefined a null
>Należy unikać przypisywania `undefined` do zmiennych, ponieważ jest on zarezerwowany
dla zmiennych zadeklarowanych, ale nie jeszcze niezdefiniowanych - bez przypisanej
wartości. W zamian należy użyć `null`.

## Objects and Symbols
Obiekty są wykorzystywane do **przechowywania kolekcji danych**.  
Symbole do **tworzenia unikalnych identyfikatorów** dla obiektów.

## Opertor typeof
Zwraca string z nazwą typu.

```javascript
typeof undefined // "undefined"

typeof 0 // "number"

typeof 10n // "bigint"

typeof true // "boolean"

typeof "foo" // "string"

typeof Symbol("id") // "symbol"

typeof Math // "object"  (1)

typeof null // "object"  (2)

typeof alert // "function"  (3)
```

1. `Math` to wbudowany obiekt.
2. `null` nie jest obiektem, to oficjalnie rozpoznany błąd. Nie został usunięty ze względu na kompatybilność.
3. `alert` W JavaScript nie ma takiego typu, funkcje należą do  
obiektów. `typeof` traktuje je inaczej zwracając tę *"function"*.

## Pytania
1. Ile typów wyróżniamy w JavaScript?
2. JavaScript jest statycznie czy dynamicznie typowany? Co to oznacza?
3. Jakie rodzaje liczb reprezentuje Number?
4. Jakie dodatkowe wartości znajdują się w Number? Jak je nazywamy?
5. Co wydarzy się gdy wykonamy niedozwolone operacje matematyczne?
6. W jakim przedziale liczbowym mieści się typ Number?
7. Jak rozpoznać liczbę typu BigInt?
8. Ile rodzaji quotes wyróżniamy w JavaScript? (wymień)
9. Co oznacza null a co undefined?
10. Kiedy używamy null a kiedy undefined?
11. W jakim celu wykorzystywane są obiekty oraz symbole?
12. Co zwraca operator `typeof`?
13. Jakie wartości są zwracane przez `typeof`?
14. Podaj wyjątki w przypadku użycia tego operatora.