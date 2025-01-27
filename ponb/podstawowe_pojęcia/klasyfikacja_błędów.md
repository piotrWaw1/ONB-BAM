#### Trwałość błędów
1. **Błędy trwałe (permanent)** – uszkodzenie i jego efekty nie zanikają z upływem czasu.
	`np: defekt fizyczny`
2. **Błędy przemijające (transient)** – błąd pojawia się chwilowo lub jednorazowo, po jakimś czasie zanika.
	`np: przekłamanie bitu w komórce pamięci RAM, chwilowe zakłócenie elektromagnetyczne`
3. **Błędy okresowe (intermittent)** – efekty błędu mogą się pojawiać i zanikać.
	`np: efekty przegrzewania układów, tzw. „zimny lut”, zmiany temperatury`
#### Dotkliwość błędów
1. **Błędy pomijalne** – w praktyce system poprawnie realizuje swoje funkcje pomimo błędu. 
2. **Błędy łagodne** – mające niewielkie znaczenie lub łatwe do ominięcia.
	`np. wadliwą funkcję może zrealizować inny blok procesora` 
3. **Błędy krytyczne** – uniemożliwiające realizację mniej istotnych funkcji. 
4. **Błędy katastrofalne (poważne)** – prowadzące do poważnych, nieodwracalnych strat. 
	`np. utraty danych, śmierci człowieka`
#### Obszar aktywności błędów
1. **Błędy wewnętrzne** – błędy sprzętu cyfrowego i analogowego, zasilaczy, oprogramowania, itp. 
2. **Błędy zewnętrzne** – zakłócenia elektromagnetyczne, wiatr słoneczny, promieniowanie, itp. 
3. **Błędy zgodne** – ten sam błąd jest odbierany jednakowo przez wszystkie moduły systemu. 
4. **Błędy niezgodne (bizantyjskie)** – daje różne efekty (lub ich brak) wróżnych modułach systemu.