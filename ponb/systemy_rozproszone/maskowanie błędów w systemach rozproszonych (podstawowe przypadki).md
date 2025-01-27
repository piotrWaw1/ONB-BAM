System rozproszony składa się z serwerów (węzłów) połączonych siecią (UDP), które można uogólnić do procesów.

W przypadku systemów rozproszonych istnieje pojęcie awarii częściowej (ang. partial failure). Odpowiednio zaprojektowany system rozproszony może sprawnie tolerować tego typu awarie.

### JCT z głosowaniem rozproszonym
![[Pasted image 20250125201945.png]]
Niezależne procesy serwerów nie są w stanie porównać swoich stanów. Aby była możliwa samodiagnoza, niezbędna jest wymiana komunikatów między serwerami.

### TMR z głosowaniem rozproszonym
W takiej sytuacji klient uznaje odpowiedź za wiarygodną, jeżeli 2 z 3 komunikatów są identyczne (głosowanie większościowe 2/3). Dla **samodiagnozy** serwery wymieniają dane między sobą
![[Pasted image 20250125202256.png]]
### NMR z głosowaniem rozproszonym
Każdy serwer powinien przesłać swoje wyniki do wszystkich pozostałych modułów, aby każdy z nich mógł przeprowadzić głosowanie.
Potrzebne jest 20 komunikatów wymieniających wyniki między modułami
