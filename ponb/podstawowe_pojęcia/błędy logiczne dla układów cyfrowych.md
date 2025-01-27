#### Wszystkie błędy:
1. **zwarcie/przerwa** – błędy typu stuck-at
2. **zmostkowania** – zwarcia między sygnałami lub wewnątrz struktury bramki logicznej
3. **błędy synchronizacji**
4. **złe poziomy sygnałów** – sygnał może zostać przekłamany (z 0 na 1, z 1 na 0) lub osiągnąć stan nieokreślony
5. **stan wysokiej impedancji** – uszkodzenia tranzystorów mogą doprowadzić do tego że bramka „pamięta” poprzedni stan i układ kombinacyjny zamienia się w sekwencyjny.

## Stuck-at
Błędy typu **stuck-at** reprezentują **przyłączenie stałego sygnału (0 lub 1)** do **dowolnego punktu układu** cyfrowego.

Są dwa rodzaje błędów typu stuck-at:
- **stuck-at-0** - zwarcie do masy
- **stuck-at-1** - zwarcie do zasilania
## Błędy synchronizacji
Błędy synchronizacji (Jitter) przypominają problemy z **hazardem statycznym** i **dynamicznym**, ale powodowane są **przez uszkodzenia i inne błędy**.

Problem ten jest szczególnie uciążliwy w magistralach równoległych przesyłających dane.