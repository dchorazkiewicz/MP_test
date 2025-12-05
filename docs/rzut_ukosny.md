# Rzut Ukośny: Analiza Matematyczna

Analiza ruchu ciała rzuconego pod kątem $\alpha$ do poziomu z prędkością początkową $v_0$ w jednorodnym polu grawitacyjnym, z pominięciem oporów powietrza.

## 1. Równania Kinematyczne Ruchu

Ruch rozkładamy na dwie niezależne składowe: poziomą (jednostajną) i pionową (jednostajnie opóźnioną).

#### Prędkość początkowa:
*   Składowa pozioma: $v_{0x} = v_0 \cos(\alpha)$
*   Składowa pionowa: $v_{0y} = v_0 \sin(\alpha)$

#### Prędkość w chwili $t$:
*   Składowa pozioma: $v_x(t) = v_{0x} = v_0 \cos(\alpha)$
*   Składowa pionowa: $v_y(t) = v_{0y} - gt = v_0 \sin(\alpha) - gt$

#### Położenie w chwili $t$:
*   Składowa pozioma: $x(t) = v_{0x} t = (v_0 \cos(\alpha)) t$
*   Składowa pionowa: $y(t) = v_{0y} t - \frac{1}{2}gt^2 = (v_0 \sin(\alpha)) t - \frac{1}{2}gt^2$

---

## 2. Równanie Toru Lotu

Aby uzyskać równanie toru lotu $y(x)$, eliminujemy czas $t$ z równań położenia.

Z równania na $x(t)$ wyznaczamy czas:
$$ t = \frac{x}{v_0 \cos(\alpha)} $$

Podstawiamy do równania na $y(t)$:
$$ y(x) = (v_0 \sin(\alpha)) \left( \frac{x}{v_0 \cos(\alpha)} \right) - \frac{1}{2}g \left( \frac{x}{v_0 \cos(\alpha)} \right)^2 $$

Po uproszczeniu otrzymujemy **równanie paraboli**:
$$ y(x) = x \tan(\alpha) - \frac{g}{2 v_0^2 \cos^2(\alpha)} x^2 $$

---

## 3. Kluczowe Parametry Lotu

#### Całkowity czas lotu ($T_c$)
Czas, po którym ciało wraca na poziom początkowy ($y=0$).
$$ (v_0 \sin(\alpha)) t - \frac{1}{2}gt^2 = 0 \implies t \left( v_0 \sin(\alpha) - \frac{1}{2}gt \right) = 0 $$
Rozwiązanie dla $t>0$:
$$ T_c = \frac{2 v_0 \sin(\alpha)}{g} $$

#### Maksymalna wysokość ($H_{max}$)
Wysokość osiągnięta w połowie czasu lotu ($t = T_c/2$), gdy składowa pionowa prędkości $v_y(t)$ jest równa zero.
$$ H_{max} = y\left(\frac{T_c}{2}\right) = y\left(\frac{v_0 \sin(\alpha)}{g}\right) $$
$$ H_{max} = \frac{v_0^2 \sin^2(\alpha)}{2g} $$

#### Zasięg rzutu ($R$)
Odległość w poziomie pokonana w całkowitym czasie lotu $T_c$.
$$ R = x(T_c) = (v_0 \cos(\alpha)) T_c = (v_0 \cos(\alpha)) \frac{2 v_0 \sin(\alpha)}{g} $$
Korzystając z tożsamości $\sin(2\alpha) = 2\sin(\alpha)\cos(\alpha)$:
$$ R = \frac{v_0^2 \sin(2\alpha)}{g} $$
*Maksymalny zasięg jest osiągany dla kąta $\alpha = 45^\circ$.*
