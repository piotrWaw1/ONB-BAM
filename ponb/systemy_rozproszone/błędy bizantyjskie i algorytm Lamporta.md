## Błędy bizantyjskie
Jest to dość złożony problem, znany też jako problem generałów bizantyjskich. **Błędy złośliwe**, **generowane przez zdrajcę**, nazywane są błędami bizantyjskimi.

Aby tolerować t błędów złośliwych, system **musi składać się z 3t+1** węzłów przetwarzania informacji, każdy musi być **połączony z co najmniej 2t+1 innymi węzłami** niezależnymi kanałami. Algorytm uzgadniania wyników **zajmuje minimum t+1 rund** wysyłanych komunikatów między uczestnikami.
## Algorytm Lamporta
1) Wyślij wynik (informację o liczebności swojego oddziału) do wszystkich pozostałych uczestników (generałów); 
2) Zbierz wyniki od pozostałych uczestników (generałów), dołącz swój wynik; 
3) Przekaż zebrany wektor wyników do wszystkich pozostałych uczestników (generałów); 
4) Wyznacz wyniki na drodze głosowania.
### Przykład:
![[Pasted image 20250126132839.png]]