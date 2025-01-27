### Definicja
To tablice dyskowe wykorzystujące redundancję do zwiększenia szybkości lub niezawodności działania dysków.
### RAID 0
Zbudowany jest z N dysków bez redundancji. Cele jest zwiększenie wydajności.
Przy odpowiednich buforach pamięciowych można wykonywać operację jednocześnie na N dyskach i przyspieszyć operację N-razy.
### RAID 1
Każdy dysk posiada swoją kompletną kopię. Wszystkie zapisy realizowane są jednocześnie na dysku podstawowym i zapasowym. Odczyt realizowany jest z jednego dysku.
### RAID 2
Do N dysków pierwotnych dodaje się k dysków, które przechowują dane korekcyjne (zazwyczaj kod Hamminga) wyznaczane np. dla sektorów o tych samych adresach z dysków podstawowych.
### RAID 3
Uproszczenie struktury RAID2. W tym modelu jest tylko jeden dysk redundancyjny (Dp) zawierający parzystość poprzeczną (bity parzystości) odpowiednich danych z dysków podstawowych.

**Model RAID3 pozwala na wymianę uszkodzonego dysku na nowy w trakcie pracy systemu (tzw.hotswap)!**
### RAID 4
Organizacja dysków w modelu RAID4 jest taka sama jak dla RAID3.

- **RAID3** ma strukturę **drobnoziarnistą**, jest zorientowany na **dużą szybkość transmisji danych**. 
- **RAID4** posiada strukturę **gruboziarnistą**, która pozwala na **równoczesny** **dostęp do różnych zbiorów** (plików).
### RAID 5
To udoskonalenie struktury RAID3– sektory redundancyjne z bitami parzystości są rozłożone równomiernie na N+1 dyskach.
### RAID 6
To macierz RAID5 uzupełniona o dodatkowy dysk i dodatkowy rekord parzystości dla każdego bloku danych (Q). Blok Q kodowany jest inaczej niż blok P (np. z pomocą kodu Reeda-Solomona).