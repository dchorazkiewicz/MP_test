# Wprowadzenie do Topologii: Przestrzenie Metryczne

Topologia to gałąź matematyki badająca właściwości przestrzeni, które są zachowywane przy ciągłych deformacjach. Fundamentalnym pojęciem, które formalizuje ideę "odległości" i prowadzi do topologii, jest metryka.

## 1. Definicja Przestrzeni Metrycznej

**Przestrzeń metryczna** to para $(X, d)$, gdzie $X$ jest niepustym zbiorem, a $d$ jest funkcją zwaną **metryką**, odwzorowującą pary elementów z $X$ w nieujemne liczby rzeczywiste:
$$ d: X \times X \to [0, \infty) $$
Funkcja ta musi spełniać trzy warunki (aksjomaty metryki) dla wszystkich $x, y, z \in X$:

1.  **Niezdegenerowanie i określoność dodatnia:**
    Odległość między dwoma punktami jest zerem wtedy i tylko wtedy, gdy są to te same punkty.
    $$ d(x, y) = 0 \iff x = y $$

2.  **Symetria:**
    Odległość od $x$ do $y$ jest taka sama jak od $y$ do $x$.
    $$ d(x, y) = d(y, x) $$

3.  **Nierówność trójkąta:**
    Droga z $x$ do $z$ nie może być dłuższa niż droga z $x$ do $y$ i następnie z $y$ do $z$.
    $$ d(x, z) \le d(x, y) + d(y, z) $$

---

## 2. Przykłady Metryk w Przestrzeni $\mathbb{R}^n$

Dla punktów $x = (x_1, \dots, x_n)$ i $y = (y_1, \dots, y_n)$ w $\mathbb{R}^n$ można zdefiniować wiele różnych metryk.

#### Metryka Euklidesowa ($d_2$)
Standardowa, "intuicyjna" odległość w linii prostej.
$$ d_2(x, y) = \sqrt{\sum_{i=1}^n (x_i - y_i)^2} $$

#### Metryka "Manhattan" / Taksobusowa ($d_1$)
Suma odległości wzdłuż każdej osi. Wyobraź sobie poruszanie się po siatce ulic w mieście.
$$ d_1(x, y) = \sum_{i=1}^n |x_i - y_i| $$

#### Metryka "Maksimum" / Czebyszewa ($d_\infty$)
Największa z odległości wzdłuż którejkolwiek z osi.
$$ d_\infty(x, y) = \max_{i=1,\dots,n} |x_i - y_i| $$

**Ważna uwaga:** Chociaż te metryki liczą odległość w różny sposób, wszystkie generują tę samą **topologię** na $\mathbb{R}^n$. Oznacza to, że pojęcia takie jak zbieżność ciągów czy otwartość zbiorów są dla nich równoważne.

---

## 3. Inne Przykłady Metryk

#### Metryka Dyskretna
Można ją zdefiniować na dowolnym zbiorze $X$. Jest to najprostszy, choć często "patologiczny" przykład metryki.
$$ d(x, y) = \begin{cases} 
0 & \text{if } x = y \\ 1 & \text{if } x \neq y 
\end{cases} $$

## 4. Od Metryki do Topologii

Metryka pozwala zdefiniować pojęcie **kuli otwartej** o środku w punkcie $x_0$ i promieniu $r > 0$:
$$ B(x_0, r) = \{ x \in X \mid d(x_0, x) < r \} $$
Zbiór $U \subseteq X$ nazywamy **otwartym**, jeśli dla każdego punktu $x \in U$ istnieje pewna kula otwarta o środku w $x$, która w całości zawiera się w $U$.
Rodzina wszystkich zbiorów otwartych w $(X, d)$ tworzy **topologię** indukowaną przez metrykę $d$.

---

## 5. Wizualizacja Kul Jednostkowych w $\mathbb{R}^2$

Poniższa grafika przedstawia, jak wyglądają kule jednostkowe (zbiory punktów {x \in \mathbb{R}^2 : d(0, x) = 1}) w różnych metrykach na płaszczyźnie.

<div style="text-align: center;">
<svg width="300" height="300" viewBox="-1.5 -1.5 3 3" xmlns="http://www.w3.org/2000/svg">
  <g transform="scale(1,-1)">
    <!-- Axes -->
    <line x1="-1.5" y1="0" x2="1.5" y2="0" stroke="black" stroke-width="0.02"/>
    <line x1="0" y1="-1.5" x2="0" y2="1.5" stroke="black" stroke-width="0.02"/>

    <!-- d_2: Euclidean metric (circle) -->
    <circle cx="0" cy="0" r="1" fill="none" stroke="blue" stroke-width="0.05"/>
    
    <!-- d_1: Manhattan metric (diamond) -->
    <polygon points="1,0 0,1 -1,0 0,-1" fill="none" stroke="red" stroke-width="0.05"/>

    <!-- d_inf: Maximum metric (square) -->
    <rect x="-1" y="-1" width="2" height="2" fill="none" stroke="green" stroke-width="0.05"/>

    <!-- Labels -->
    <g style="font-family: sans-serif; font-size: 0.15px;" transform="scale(1,-1)">
      <text x="0.75" y="-0.75" fill="blue">d₂</text>
      <text x="0.4" y="-0.4" fill="red">d₁</text>
      <text x="1.05" y="-1.05" fill="green">d ∞</text>
    </g>
  </g>
</svg>
</div>