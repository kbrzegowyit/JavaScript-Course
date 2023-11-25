# JavaScript Fundamentals: Basic operators, maths
Opracowanie dotyczące opertorów w języku JavaScript.


## Pojęcia *operator*, *unary*, *bianry*, *operand*
- **operator** to np. `+`, `-`, `/`, `*`, itd..
- **operand** to elementy działania, do których stosowany jest dany operator. Np. `2 * 3`, operandy to **2** oraz **3**.
- **unary** to operator posiadajacy jeden operand.
- **binary** to operator posiadający dwa operandy.

## Dostępne operatory
Są to: `+`, `-`, `*`, `/`, `%`, `**`.

## Binary `+`
W przypadku `number`-ów **dodaje**, natomiast `string`-ów **konkatenuje**.  
Jeżeli choć jeden z operandów jest `string`-iem, całe wyrażenie zostanie przekonwertowane
do tego typu.  
**Operacje wykonywane są od lewej do prawej.**  

```javascript
alert(2 + 2 + '1' ); // "41" and not "221"

alert('1' + 2 + 2); // "122" and not "14"

```
<font color='red'>Jest to jedyny operator, który wspiera `string`, pozostałe konwertują wszystkie operandy do `number`.</font>

## Unary `+`
Wykonuje konwersję do `number`.

```javascript
let apples = "2";
let oranges = "3";

// both values converted to numbers before the binary plus
alert( +apples + +oranges ); // 5
```

**Unary `+` ma pierwszeństwo przed binary**, dlatego konwersja wykona się wcześniej.

## Assigment `=`
Zasadę działania najlepiej zobrazuje poniższy przykład.

```javascript
let c = 3 - (a = b + 1);
```
Wywołanie `let x = value` przypisuje `value` do `x`, a następnie **zwraca tę wartość**!

Istnieje możliwość łączenia przypisań tak jak to zostało przedstawione ponieżej.

```javascript
let a, b, c;

a = b = c = 2 + 2;
```

Jednak nie jest to zalecane, ponieważ nie urudnia to czytelność kodu.  

```javasctipt
let a, b, c;

c = 2 + 2;
b = c;
a = c;
```

## Operatory Inkrementacji/Dekrementacji
>Operatory te mogą być używane jedynie ze zmiennymi. Zastosowanie ich na konkretnej
liczbie np. `6++` spowoduje błąd.

Rozróżniamy *preinkrementację* i *postinkrementację*. Identycznie dla *dekrementacji*.
**Jednak ma to tylko znaczenie, gdy zwracamy wartość**.

#### Prenkrementacja/dekrementacja
Modyfikacja wartości → zwrócenie wartość.
#### Postinkrementacja/dekrementacja
Zwrócenie wartości → modyfikacja wartość.

#### Pierwszeństwo względem innych opertorów

Omawiane operatory mają pierwszeństwo przed większością operatorów arytmetycznych.

```javasctipt
let counter = 1;
alert( 2 * ++counter ); // 4

let counter = 1;
alert( 2 * counter++ ); // 2, because counter++ returns the "old" value
```

Powyższy zapis obniża czytelność kodu. Lepiej stosować zasadę **"one line - one action"**.

## Operatory bitowe
Podobnie jak w innych językach, tak i tu, występują operatory bitowe.

AND (`&`)
OR (`|`)
XOR (`^`)
NOT (`~`)
LEFT SHIFT (`<<`)
RIGHT SHIFT (`>>`)
ZERO-FILL RIGHT SHIFT (`>>>`)

## Operator przecinka
Ma bardzo niski poziom pierwszeństwa (*ang. precedence*). Dlatego należy używać go w otoczeniu
nawiasów okrągłych.

```javascript
let a = (1 + 2, 3 + 4); // pierwsze wyrażenie 1 + 2 nie jest zwracane, tylko ostatnie 3 + 4

alert( a ); // 7 (the result of 3 + 4)
```

## Pytania
1. Wyjaśnij czym są: operator (unary, binary) oraz operand.
2. Podaj dostępne operatory w JavaScript.
3. Opisz zachowanie operatora `+` w kontekście `string`-ów i `number`-ów.
4. Jak zachowuja się pozostałe operatory w przypadku operandów innego typu niż `number`?
5. Jak działa unary `+`? 
6. Wyjaśnij sposób działania operatora przypisania `=`.
7. Kiedy operacja związane z inkrementacją/dekrementacją wpływają na wynik działania programu?
8. Kiedy inkrementacja/dekrementacja zwróci błąd?
9. Jaka jest kolejność wykonania inkrementacji/dekrementacji względem innych operatorów arytmetycznych?
10. Wymień operatory bitowe w JavaScript? (opcjonalnie)
11. Jak działą operator przecinka?
12. Jakie jest jego pierwszeństwo?
