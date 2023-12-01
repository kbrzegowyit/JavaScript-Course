# JavaScript Fundamentals: Functions

Opracowanie dotyczące funkcji w JavaScript.

## Function declaration

```javascript
function name(parameter1, parameter2, ... parameterN) {
 // body
}
```

## Default values

Jeżeli parametr funkcji zostanie pominięty podczas jej wywołania przyjmie wartość `undefined`.  

Możemy przygotować się na to używajac domyślnej wartości *(ang. default values)*.

```javascript
function showMessage(from, text = "no text given") {
  alert( from + ": " + text );
}

showMessage("Ann"); // Ann: no text given
```

## Zwracanie wartości

Jeżli funkcja nie zwraca żadnej wartości lub `return;`, to niejawnie zwraca `undefined`.

Jeżlei chcemy dodać rozbudowany, wieloliniowy return, to **należy użyć okrągłych nawiasów**;

```javascript
return (
  some + long + expression
  + or +
  whatever * f(a) + f(b)
)
```

<font color='red'>Dodanie nowej lini po `return` i wartości nie zadziała.</font>

## Nazewnictwo funkcji *(ang. naming functions)*

- Nazwa funkcji to zazwyczaj **czasownik** *(ang. verb)*.
- Powinna ona być **zwięzła** *(ang. brief)* i **dokładna** *(ang. accurate)* najbardziej jak to możliwe.
- Ważne, aby opisywała to co robi funkcja.
- Należy przestrzegać zasady **jedna funkcja - jedna akcja** *(ang. one function - one action)*.

Popularne prefiksy:
- "get…" – return a value,
- "calc…" – calculate something,
- "create…" – create something,
- "check…" – check something and return a boolean, etc.

Jeżeli np. funkcja `getAge` jeszcze dodatkowo wyświetla wiek, jest to błędem. 
Powinna tylko zwracać wartść.

## Pytania
1. Jak wyglada deklaracja funkcji w JavaScript *(ang. function declaration)*?
2. Opisz zasadę działania i sposób użycia domyślnych wartości w kontekscie funkcji w JavaScript.
3. Jaką wartość zwraca funkcja bez `return` lub z `return;`?
4. Czego należy unikać i o czym pamiętać podczas wartość zwracana jest wyrażona wieloliniowo?
5. Opisz najważniejsze zasady dotyczące nazewnictwa funkcji.

