# JavaScript Fundamentals: Comparisons
Opracowanie dotyczące zasad porównywania wartości w języku JavaScript.

## Wynik porównań
`Boolean` jest zwracany jako wynik każdego porównania.

## Porównania `string`
Porównywanie litera po literze (*ang. letter by letter*). JavaScript używa porządku
*“dictionary”* (or *“lexicographical”*).  

#### Algorytm
`a` - znak ze string-u pierszego.  
`b` - znak ze string-u drugiego.

Porównujemy od początku napisów znak po znaku.
1. Jeżeli a > b ⇒ string pierwszy.
2. Jeżeli a < b ⇒ string drugi.
3. Jeżeli a == b ⇒ porównaj następny znak.
4. Jeżeli brak znaków ⇒  **string-i są równe,** w przeciwnym razie **dłuższy jest większy**.

## Porównywaie różnych typów
<font color='red'>Podczas porównywania różnych typów, oba konwertowane są do `number`.</font>

## Strict equality
Są to następujące porównania `===`, `!==`.  
W pierszej kolejności sprawdzane są **typy zmiennych**.  
Jeżeli są różne automatycznie zwracana jest wartość `false` bez konwertowania ich.

## `null` and `undefined`
- `===` ⇒ false
- `==` ⇒ true
- `>`, `<`, `>=`, `<=` ⇒ false (konwersja do `number`, `undefined` - `NaN`, `null` - `0`)

Porównanie tych typów z innymi typami:
- `>`, `<`, `>=`, `<=` ⇒ oba typy konwertowane do `number` i porównywane.
- `==` ⇒ zawsze false, bo tylko **undefined == null ⇒  true**
 
## Pytania
1. Jaką wartość zwracają porównania w JavaScript?
2. Jak porywnywane są `string`-i?
3. Jak porywnywane są zmienne różnych typów?
4. Co w przpadku strict equality?
5. Jakie wartości daje porówanie `null` i `undefined` z innymi typami?
