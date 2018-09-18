F(x) -> max(min)
 - x from X (domain)
 - distance ρ(x,y): **X**\***X** -> **R+**
 - neighborhood Nε(x): { y from X, ρ(x,y) ≤ ε }

Hill climbing (Steepest Ascend):
```
Select random x from X
found <- true
while found:
    for all y from Nε(x):
        find y*: F(y*) = max F(y), y from Nε(x)
    if F(y*) > F(x):
        x <- y*
	else:
        found <- false
return x
```

Kernigan-Linn (adaptive hill climbing, infinite space)
```
Select random x from X
Select ε > 0
while ε > threshold:
    for attempt = 1..maxAttempts:
        select random y from Nε(x)
        find y*: F(y*) = max F(y), y from Nε(x)
    if F(y*) > F(x):
        x <- y*
        ε <- 2*ε # Increase ε to be sure we don't have too small neighborhood
    else:
        # We can't claim that there is no better point since we didn't check all points
        # So, we can't return here, we need to find out a way to increase probability of selecting a random point, which turns out to have better objective.
        # E.g., the less ε selected the more probability that we will found point, which leads to the hill
        ε <- ε/2    

return x
```

Hill Climbing (Find First)
```
Select random x from X
found <- true
while found:
	found <- false
    for all y from Nε(x):
        if F(y) > F(x):
            x <- y
            found <- true
            break
        else:
            
return x
```
