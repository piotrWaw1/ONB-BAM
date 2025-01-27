### Definicja
Kod Bergera to prosty kod systematyczny, gdzie część informacyjna długości k bitów rozszerzana jest o n-k bitów kontrolnych.

**Bity kontrolne** zawierają informację o liczbie jedynek w k-bitowym słowie części informacyjnej, zapisaną jako **zanegowany kod NKB**. Druga wersja kodu Bergera zapisuje **liczbę zer** w słowie kodowym jako NKB.
### Wzory
Dla kodu Bergera dla słów o długości k liczba bitów kontrolnych (n-k) wynosi:
$$n-k=log_2(k)+1$$

| k (bitów) | n-k (bitów) |
| --------- | ----------- |
| 8         | 4           |
| 16        | 5           |
| 32        | 6           |
| 64        | 7           |
