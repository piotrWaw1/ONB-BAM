Jest to technika do **tolerowania trwałych błędów sprzętowych**. Prosta replikacja kodu pozwala wykrywać i tolerować błędy sprzętowe, jeżeli **kopie kodu wykonywane są przez różne moduły urządzenia** (procesory, rdzenie, bloki wykonawcze procesora itp.).

### Redundancja drobnoziarnista
Koncepcja sprowadza się do realizacji obliczeń przy częściowym wykorzystaniu zasobów układowych, tak aby w kolejnych fazach powtarzania wykorzystywać różne ich fragmenty.

Do technik tego typu należą: 
- **RESO** (recomputing with shifted operands);
	- Obliczenia powtarzane są kilka razy dla tych samych argumentów, ale przesuniętych o kilka bitów. 
	- **Technika pozwala zamaskować dowolną liczbę błędów, pod warunkiem że wadliwe bity są od siebie oddalone co najmniej o 3 pozycje.**
	- Operację przesuwania bitów można zastąpić podziałem argumentów na części (mniej i bardziej znaczące). Dwie części dla wykrywania, trzy dla maskowania błędów.
- **RESWO** (recomputing with swapped operands); 
	- Polega na ponownym wykonaniu operacji z zamienionymi częściami argumentów.
	- Technika może być także zastosowana do odejmowania, mnożenia, dzielenia it.
- **REDWC** (recomputing with duplication with comparison).
	- Jest modyfikacją techniki RESWO, gdzie operację wykonuje się na młodszych i starszych częściach argumentów niezależnie
	- Porównanie połówek wyników może posłużyć do wykrycia błędu.

Techniki **RESWO** i **REDWC** także mogą służyć do **maskowania błędów**: na drodze programowej lub sprzętowej, po podziale arytmometru na trzy części.
### Redundancja kodu ED<sup>4</sup>I
Opiera się ona na porównaniu wyników generowanych przez program pierwotny i program zmodyfikowany.

Modyfikacja programu polega na zastąpieniu wszystkich stałych i zmiennych programu ich odpowiednikami pomnożonymi przez stałą k. Wynik programu pierwotnego porównywany jest z przeskalowanym wynikiem programu zmodyfikowanego.

W zależności od wartości współczynnika k program pierwotny i zmodyfikowany używają w różnym stopniu zasobów systemowych. Ten sam błąd najczęściej prowadzi do niezgodności wyników.

Jeżeli w kodzie występują rozgałęzienia (instrukcje warunkowe), konieczna jest modyfikacja wyrażeń tak, aby zachować ten sam przepływ sterowania co w programie pierwotnym.