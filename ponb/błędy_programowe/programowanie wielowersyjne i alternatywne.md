### Programowanie wielowersyjne
Wszystkie wersje programu zazwyczaj uruchamiane są równocześnie (współbieżnie), wynik ustalany jest w drodze głosowania. Kod wykonywany jest przez **jeden lub wiele procesorów**.
### Programowanie alternatywne
Yo jedna z najstarszych technik podwyższania niezawodności oprogramowania, polega na opracowaniu **kilku alternatywnych wersji programu**.

Podczas pracy systemy **uruchamiana jest jedna wersja** i przez test akceptacyjny badana jest poprawność generowanych przez nią wyników. W przypadku **negatywnego wyniku testu**, **uruchamiana jest następna wersja kodu** i weryfikowana przez test akceptacyjny, itd.

**Przy braku akceptacji dla wszystkich dostępnych wersji kodu generowany jest błąd.**

Każda wersja kodu może mieć swoją wersję testu akceptacyjnego, w praktyce zazwyczaj istnieje jeden test wspólny dla wszystkich wersji. W szczególnym przypadku rolę testu może spełniać inna wersja programu.

### Programowa redundancja hybrydowa
To **połączenie** techniki **wielowersyjnej z programowaniem alternatywnym**.

1. **Programowanie alternatywne z konsensusem** (consensus recovery block): jeżeli głosowanie zawiedzie, wykonuje się testy akceptacyjne dla otrzymanych wyników. Dla błędów przemijających obliczenia mogą być zainicjowane ponownie.
2. **Głosowanie zaakceptowanych wyników** (acceptance voting)– symetryczny wariant redundancji hybrydowej. Wszystkie wersje programu uruchamiane są jednocześnie, następuje głosowanie tylko dla wyników które przeszły test akceptacyjny (może nie być żadnego wyniku).