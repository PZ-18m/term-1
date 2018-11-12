Genetic Algorithms
John Holland
The fittest Survive

Population
P = {x1, x2, ..., xn}, xi from X
x1, x2, ..., xn - chromosomes

xi = (xi1, xi2, ..., xim), X = {0,1}^m

For each x from P define fitness(x)

Population -> children

GA:
 - Steady state
 Chromosome can live infinite amount of time
 - Generational approach
 New generation completely replaces old one


GA:
  Generate initial population P = {x1, x2, ..., xn} xi <- random(X)
  for all x from P evaluate fitness(x)
  Repeat
    par1, par2 <- parent_selection(P)
    ch1, ch2   <- crossover(par1, par2)
    ch1', ch2' <- mutation(ch1, ch2)
                  evalate_fitness(ch1', ch2')
           P   <- replacement(P U {ch1', ch2'})
  Until 
  Return best from P.


parent_selection:
 - Roullette Wheel