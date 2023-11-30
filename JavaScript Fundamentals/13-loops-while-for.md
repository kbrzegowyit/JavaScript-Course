# JavaScript Fundamentals: Loops

Opracowanie dotyczące pętli for i while.

## Zasada diałania pętli `for`
|Part|Example|Note|  
|----|-------|----|
|begin|`let i = 0`|Wykonywane tylko przy wejściu do pętli.|
|condition|`i < 3`|Sprawdzane przed każdą iteracją. `false` przerwanie pętli.|
|body|`alert(i)`|Wykonywane dopóki warunek jest prawdziwy.|
|iteration|`i++`|Wykonywane po body, po każdej iteracji.|

## Label dla for i while
```javasctipt
labelName: for (...) {
    for (...) {
        if (condition) break/continue labelName;
    }
}
```

## Pytania
1. Jak działa pętal `for` w JavaSctipt?
2. Jak działa label dla pętli w JavaSctip?
