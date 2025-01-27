### Definicja
To podstawowa technika detekcji błędów programowych, polega na weryfikacji wyników i prawidłowości realizacji programu.

Dla pewnych aplikacji (głównie obliczeniowych) zdefiniowanie testów akceptacyjnych jest łatwe, np.: 
- **Sortowanie** **danych** – test akceptacyjny ogranicza się do sprawdzenia czy wynikowy zbiór danych jest posortowany zgodnie z założeniami. 
- **Układy** **równań** – rozwiązanie złożonego układu równań łatwo zweryfikować przez podstawienie wyników. 
- **Pierwiastek**– wynik obliczeń podniesiony do kwadratu powinien dać argument (odwrócenie operacji).

Proces **weryfikacji może dopuszczać pewien margines błędu**, wynikający z ograniczeń sprzętowych, np. długość rejestrów w obliczeniach zmiennoprzecinkowych.

### Asercja
**Asercja** jest prostą formą testu akceptacyjnego, programista umieszczając ją w kodzie programu zakłada, że predykat ów jest (lub powinien być) prawdziwy.

Jeżeli argument tej makrodefinicji jest równy zero (fałsz), na standardowe wyjście błędów programu wyprowadzany jest komunikat o błędzie i program jest przerywany.