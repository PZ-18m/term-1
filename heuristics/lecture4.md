Hill climbing (changes):
```
Select random x from X
//found <- true
while true:
    for all y from Nε(x)\{x}:
        find y*: F(y*) = max F(y), y from Nε(x)\{x}
    //if F(y*) > F(x):
        x <- y*
	//else:
        // found <- false
return x
```

Hill climbing + Memory = Tabu Search (Explicit Memory):
```
Select random x from X
M <- {x} // Memory
while true:
    for all y from Nε(x)\M:
        find y*: F(y*) = max F(y), y from Nε(x)\M
    x <- y*
    M <- M U {y*}
return x
```

Tabu search (Implicit Memory)
1. Short-term Memory. 
Храним запрещенные переходы на несколько шагов (Tabu Tenure), после этого разрешаем их снова.
2. Long-term Memory.
