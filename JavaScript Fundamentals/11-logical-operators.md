# [![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript) JavaScript Fundamentals: Logical operators
  
Opracowanie dotyczące operatorów logicznych w języku JavaScript.
Wyróżniamy cztery operatory logiczne: OR `||`, AND `&&`, NOT `!`, Nullish Coalescing `??`.

## OR `||`
1. Ewaluuje od prawej do lewej.
2. Konwertuje każdą wartość do `boolean`.
2. Jeżeli wartość jest *truthy*, zatrzymuje przetwarzanie i zwraca oryginalną wartość.
3. W przypadku, gdy wszustkie wartość są *falsy*, zwraca ostatnią.

## OR `&&`
Podobnie jak w przypadku OR.
1. Ewaluuje od prawej do lewej.
2. Konwertuje każdą do `boolean`.
3. Jeżeliw wartość jest *falsy*, zatrzymuje przetwarzanie i zwraca oryginalną wartość.
4. W przypadku, gdy wszystkie są *truthy*, zwraca ostatnią.

>AND `&&` posiada większą wartość pierwszeństwa (*ang. precedence*) niż OR `||`.  
Wyrażenie **a && b || c && d** jest tożsame z **(a && b) || (c && d)**.

## NOT `!`
Zasada działania jest dużo prostsza niż w przypadku poprzednich operatorów.
1. Konwetuje wartość do `boolean`.
2. Zwraca przeciwną wartość.

#### Konwersja do `boolean`
>Może służyć w celu konwertowania wartości do `boolean` (!!value).
#### Pierwszeństwo
>Posiada najwyższy stopień pierwszeństwa ze wszystkich operatorów logicznych.

## Pytania
1. Jak działa operator OR `||` w JavaScript?
2. Jak działa operator AND `&&` w JavaScript?
3. Który z w.w. operatorów ma większą wartość pierwszeństwa?
4. Jak działa operator NOT `!` w JavaScript?
5. Jaki stopień pierwszeństwa posiada ten operator względem pozostałych operatorów logicznych?
