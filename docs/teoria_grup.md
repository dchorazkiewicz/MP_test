# Wprowadzenie do Teorii Grup

Teoria grup to dziedzina matematyki zajmująca się badaniem struktur algebraicznych zwanych grupami. Grupy są fundamentalne w wielu dziedzinach matematyki i nauk ścisłych, takich jak fizyka, chemia i informatyka.

## Definicja Grupy

Grupa to para $(G, \cdot)$, składająca się ze zbioru $G$ oraz działania dwuargumentowego $\cdot$ na tym zbiorze, która spełnia cztery poniższe aksjomaty.

## Aksjomaty Grupy

1.  **Zamkniętość (Closure):**
    Dla dowolnych elementów $a, b$ należących do $G$, wynik ich działania $a \cdot b$ również należy do $G$.
    $$ \forall a, b \in G, \quad a \cdot b \in G $$

2.  **Łączność (Associativity):**
    Działanie jest łączne, co oznacza, że kolejność wykonywania działań (przy trzech lub więcej elementach) nie ma znaczenia.
    $$ \forall a, b, c \in G, \quad (a \cdot b) \cdot c = a \cdot (b \cdot c) $$

3.  **Element Neutralny (Identity Element):**
    W zbiorze $G$ istnieje unikalny element neutralny $e$, który dla każdego elementu $a$ z $G$ spełnia warunek:
    $$ \exists e \in G : \forall a \in G, \quad e \cdot a = a \cdot e = a $$

4.  **Element Odwrotny (Inverse Element):**
    Dla każdego elementu $a$ w $G$ istnieje element odwrotny $a^{-1}$ (również w $G$), taki że ich działanie daje element neutralny.
    $$ \forall a \in G, \quad \exists a^{-1} \in G : \quad a \cdot a^{-1} = a^{-1} \cdot a = e $$

## Przykład: Grupa liczb całkowitych z dodawaniem

Jednym z najprostszych przykładów grupy jest zbiór liczb całkowitych $\mathbb{Z}$ z działaniem dodawania $+$. Para $(\mathbb{Z}, +)$ jest grupą:

*   **Zamkniętość:** Suma dwóch liczb całkowitych jest zawsze liczbą całkowitą.
*   **Łączność:** Dodawanie jest łączne, np. $(2+3)+4 = 2+(3+4)$.
*   **Element neutralny:** Jest nim liczba $0$, ponieważ $a + 0 = a$.
*   **Element odwrotny:** Dla każdej liczby całkowitej $a$, elementem odwrotnym jest $-a$, ponieważ $a + (-a) = 0$.

---

## Podgrupy (Subgroups)

Podzbiór $H$ grupy $(G, \cdot)$ nazywamy **podgrupą**, jeśli sam tworzy grupę z tym samym działaniem $\cdot$. Formalnie, $H$ jest podgrupą $G$, jeśli:
1.  $H$ jest niepusty.
2.  Dla każdych dwóch elementów $a, b \in H$, element $a \cdot b^{-1}$ również należy do $H$.

**Przykład:** Zbiór liczb parzystych $(2\mathbb{Z}, +)$ jest podgrupą grupy liczb całkowitych $(\mathbb{Z}, +)$.

## Grupy Cykliczne (Cyclic Groups)

Grupa $G$ jest **cykliczna**, jeśli może być wygenerowana przez pojedynczy element, nazywany generatorem. Oznacza to, że każdy element grupy jest potęgą (lub wielokrotnością w notacji addytywnej) generatora $g$.

$$ G = \langle g \rangle = \{ g^n \mid n \in \mathbb{Z} \} $$

**Przykład:** Grupa $(\mathbb{Z}, +)$ jest cykliczna, a jej generatorem jest $1$ (lub $-1$). Grupa reszt z dzielenia modulo $n$, $(\mathbb{Z}_n, +_n)$, jest również grupą cykliczną generowaną przez $1$.

## Twierdzenie Lagrange'a

To jedno z fundamentalnych twierdzeń w teorii grup skończonych. Mówi ono, że jeśli $G$ jest grupą skończoną, a $H$ jest jej podgrupą, to **rząd podgrupy $H$ musi dzielić rząd grupy $G$**.

$$ |H| \quad | \quad |G| $$

**Wniosek:** Rząd dowolnego elementu grupy skończonej (czyli rząd podgrupy cyklicznej generowanej przez ten element) również musi dzielić rząd całej grupy. To potężne narzędzie, które mocno ogranicza strukturę możliwych podgrup. Na przykład, grupa rzędu $p$, gdzie $p$ jest liczbą pierwszą, nie może mieć żadnych nietrywialnych podgrup.