**JCT**
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