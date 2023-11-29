# JavaScript Fundamentals: Nullish coalescing operator '??'

Opracowanie dotyczące operatora logicznego `??`.

## Nullish coalescing operator `??`
Zwraca pierwszy argument różny od `null/undefined`.

```javascript
alert(null ?? undefined ?? 'Hello'); // 'Hello'
```

## `??` a `||`
`??` - zwraca pierwszą zdefiniowaną wartość (*ang. defined*).  
`||` - zwraca pierwszą prawdziwą wartość (*ang. truthy*)

## Precedence
Wartość pierwszeństwa `??` i `||` jest taka sama - 3.

>Jeżeli użyjemy jednocześnie `??` lub `||` lub `&&` otrzymamy **SyntaxError**.  
W celu uniknięcia tego błędy należy rodzielić poszczególne części nawiasami.

## Pytania
1. Jak działa operator Nullish `??` w JavaScript?
2. Czym różni się od OR `||`?
3. Jaką wartość precedence posiada?
4. Jaki wpływ ma to na łączenie go z pozostałymi operatorami logicznymi?