## Kody korekcyjne
Korekcja danych polega na znalezieniu wektora kodowego **najbardziej podobnego** do wektora niepoprawnego. Jest to tzw. dekodowanie MLD (ang. Maximum Likelihood Decoding).

Aby poprawnie skorygować **D** jednobitowych błędów, potrzebny jest kod o odległości **Hamminga 2D+1**. Wtedy poprawne słowa kodowe są na tyle odległe od siebie, że po D zmianach pierwotne słowo jest bliższe oryginałowi niż jakiekolwiek inne.
![[Pasted image 20250126142938.png]]
### Zasada korekcji błędów
##### Każdy n-elementowy wektor może zawierać tyle błędów i-bitowych ile wynosi kombinacja n po i:
$$\binom{n}{i} = \frac{n!}{(n-i)! \cdot i!}$$

Na każde z 2<sup>k</sup> poprawnych słów przypada n+1 słów kodowych (n złych i jedno poprawne) ich całkowita liczba nie może być większa od liczby wszystkich słów kodowych 2<sup>n</sup>.
$$(n+1)\times2^k ≤ 2^n $$
$$Ponieważ\;\;\;\;\;\; n=k+(n-k)$$
$$(n+1)≤ 2^{n-k}$$
Dla danej liczby bitów k określa to dolne ograniczenie liczby bitów kontrolnych 
(n-k) niezbędnych do korygowania pojedynczych błędów.
#### Granica Hamminga
$$2^{n-k} \geq \sum_{i=0}^{t} \binom{n}{i}$$
Jest to tzw. **granica Hamminga** która służy do oceny jakości kodów korekcyjnych. Kody binarne dla których zachodzi równość, nazywa się kodami doskonałymi (ang. perfect codes).
## Kod Reeda-Solomona
Kody Reeda-Solomona (w skrócie RS) **to rodzina kodów korekcyjnych** opracowana w 1960 roku przez Irvinga Reeda i Gusa Solomona. **Są to niebinarne**, **liniowe cykliczne kody korekcyjne działające w oparciu o rozszerzone pola Galois**.

Używane między innymi w:
- płyty
- telewizja cyfrowa
- macierze dyskowe
#### Ciała rozszerzone
Ciała skończone rozszerzone GF(q) tworzone są nad ciałami prostymi GF(p) lub ciałami rozszerzonymi niższego stopnia. Wartość m jest stopniem rozszerzenia ciała:
$$q=p^m$$
Ciało rozszerzone stopnia m generowane jest na bazie ciała prostego i wielomianu pierwotnego stopnia m.
#### Wielomiany nierozkładalne i pierwotne
Wielomian stopnia m jest nierozkładalny, jeżeli nie dzieli się przez dowolny wielomian stopnia większego od zera i mniejszego od m. Wielomiany takie odgrywają ważną rolę w teorii kodów korekcyjnych.

Wielomian nie rozkładalny stopnia m jest wielomianem pierwotnym, jeżeli wszystkie jego pierwiastki są elementami pierwotnymi rozszerzenia stopnia m.
#### Elementy ciał rozszerzonych
Ciała rozszerzone nie są ciałami liczbowymi, a ich elementy oznacza się zwykle z pomocą symboli, zazwyczaj z pomocą elementu algebraicznego α.