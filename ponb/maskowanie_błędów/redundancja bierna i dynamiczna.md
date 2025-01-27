## Redundancja bierna
Zaliczamy do niej techniki:
- **JCT**
	**Dwa identyczne moduły wykonują te same operacje, wynik jest porównywany.**
	Nie maskuje błędów pozwala tylko na ich **detekcję**. Sygnał błędu może rozpocząć **procedurę samotestowania** modułów i doprowadzić do wskazania wadliwego elementu.
	![[Pasted image 20250123194816.png]]
- **TMR** - potrójna nadmiarowość 
	Trzy moduły wykonują identyczne operacje, poprawny wynik ustalany jest **w drodze głosowania** następuje **maskowanie błędów**. 
	
	**Niezawodność układu głosującego (tzw. wybieraka) musi być dużo większa niż niezawodność powielonych modułów.**
	![[Pasted image 20250123195145.png]]
- **NMR** - redundancja N modułowa
	Aby tolerować więcej uszkodzeń w jednej chwili czasu, można użyć większej, nieparzystej liczby modułów n, oraz układu głosowania według zasady:
	$$  (\frac{n+1}{2})/n$$
	Układy NMR są bardzo kosztowne, ale pozwalają na tolerowanie błędów wielokrotnych.
	![[Pasted image 20250123200054.png]]
#### Największą wadą podstawowych technik TMR i NMR jest wymóg bardzo wysokiej niezawodności i prostoty układu głosującego.

## Redundancja dynamiczna
W przypadku uszkodzenia jednego z elementów, jest on zastępowany jednym z elementów zapasowych – następuje dynamiczna rekonfiguracja.
**Rekonfiguracja może mieć charakter trwały lub chwilowy w zależności od błędu.**
### TMR 
Po całkowitej rekonfiguracji, system powraca **do pełnej sprawności** i możliwości maskowania pojedynczych błędów.
![[Pasted image 20250123210454.png]]

### JCT -> TMR
Układ złożony z dwóch modułów (JCT) po wykryciu różnicy wyników, może w wyniku dynamicznej rekonfiguracji zostać **przekształcony w TMR**.
![[Pasted image 20250123210600.png]]