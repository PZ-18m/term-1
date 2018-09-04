Why some problems are hard to solve?

- Dimensionality problem. Размерность некоторых задач настолько большая, что применять типовой алгоритм оптимизации невозможно. 
  - binary optimization, e.g. SAT problem or Satisfiability problem. Есть некоторые выражение в виде конъюнктивной нормальной формы. I(x1, x2, ..., xn) = (x1 or ~x2) and (x1 or x3 or ~x4) and (~x2 or x4), xi = 0 or 1. Каждая скобка назывется clause. Задача - существует ли набор переменных x1*, x2*, ..., xn*, что I(x1*, x2*, ..., xn*) = TRUE.
  Эта задача равносильна I(x1*, x2*, ..., xn*) -> max (так как 1 - это максимальное значение). Это классический пример NP-hard задачи - сложность точного алгоритма решения экспоненциальная от размерности задачи. 
  - permutation problems, e.g. TSP (travelling salesman problem) - задача коммивояжера. Заданы координаты n городов и матрица расстояний между ними. Найти минимальный по длине цикл, проходящий через все города.
  - NLP (non-linear programming). I(x1, x2, ..., xn) -> max, ai <= xi <= bi, i=1..n. De Jong test suite - примеры функций для демонстрации особенностей различных решений задач нелинейного программирования. Например, I(x1, x2, ..., xn) = SUM(xi^2).
 - Input data. Проблема неполных данных, данных имеющих вероятностную природу.
	
Input data -> Model -> Algorithm -> Solution.
1. Input data -> Approximate model (some aspects of input data are dropped) -> Exact algorithm -> Approximate solution
2. Input data -> Exact model -> Approximate algorithm (metaheuristics) -> Approximate solution

	Какое решение лучше?
    
	**"No free lunch" theorem**. Мы находимся в центре темной квадратной комната с выходом в углу. Необходимо предложить алгоритм поиска выхода. 
	 1. Двигаться до стены по прямой, потом по стене до выхода
	 2. Двигаться по спирали до стены, потом по стене до выхода
	 3. Дойти до угла и остановиться. 
	Вывод - невозможно построить алгоритм, который является универсально лучшим остальных алгоритмов на всем множестве задач.

Метаэвристики:
| Эвристика             | Лаба |
|-----------------------------|---|
| Hill Climbing               | 1 |
| Steepest Ascend             | 1 |
| Kernigan-Lin                | ? |
| Tabu Search                 | 2 |
| Simulated Annealing         | 2 |
| Demon Algorithm             | 2 |
| Genetic Algorithm           | 3 |
| Scatter Search              | 3 |
| Path Relinking              | 3 |
| Artificial Immune System    | 3 |
| Clonal Selection            | 3 |
| Gravitational search        | 4 |
| Ant colony                  | 4 |
| GRASP                       | 4 |
| Bacterial forging (BFOA)    | 4 |
| Cultural Algorithm          | 4 |
