## Kody cykliczne

#### Definicja
Kody cykliczne to rodzina kodów parzystości mająca tę właściwość, że każde **cykliczne przesunięcie słowa** kodowego jest także słowem kodowym.

Binarny kod cykliczny (n, k) jest **generowany przez dowolny wielomian binarny stopnia (n-k)** będący podzielnikiem wielomianu x<sup>n</sup>+1, gdzie n=q<sup>m</sup>-1, a m jest liczbą naturalną.

Dodawanie wielomianów binarnych nad ciałem GF(2) polega na **wykonaniu operacji XOR na ich binarnych reprezentacjach**.

Każdy kod cykliczny **można przedstawić** w postaci **ilorazowej** (systematycznej):
$$A(x) = I(x) \;◊\; \text{Re} \left[ \frac{x^{n-k} I(x)}{G(x)} \right]$$
Gdzie: 
- Re  →   reszta z dzielenia; 
- ◊    →   łączenie (konkatenacja) słowa informacyjnego i reszty.

**Dzielenie wielomianów binarnych nad ciałem** GF(2) – **analogiczne** do dzielenia **zwykłych wielomianów** (wielomian wyższego rzędu przez wielomian niższego rzędu), ale z **odejmowaniem z pomocą operacji XOR**.

**Kod cykliczny generowany przez wielomian stopnia n-k wykrywa wszystkie błędy pojedyncze oraz serię błędów o długości nie większej niż n-k.**

## CRC
#### Definicja
Słowo kodowe składa się z części informacyjnej i kontrolnej (konkatenacja reszty zdzielenia). Część kontrolna dodawana jest do słowa w trakcie kodowania.

Słowo kodu (bity informacyjne i kontrolne) jest całkowicie podzielne przez wielomian generujący CRC.

Kody parzystości, w tym cykliczne, bardzo dobrze nadają się do przesyłania i pamiętania informacji. Dodatkową zaletą jest prostota budowy koderów i dekoderów takich kodów.

Przykładowe zastosowania kodów parzystości i CRC: 
- Transmisja danych: RS232, sieci Ethernet, USB, Bluetooth, IrDA 
- Przechowywanie danych: dyski twarde, pamięci flash, karty pamięci SD i MMC 
- Software: MPEG-2, H.264, PNG, ZIP
Wybór generatora CRC (wielomianu) zależy od charakteru błędów mogących wystąpić.
### Wady
Wybór generatora CRC (wielomianu) zależy od charakteru błędów mogących wystąpić.