## Systemy transakcyjne
Typowe transakcje w bazach danych zaczynają się od polecenia inicjalizującego (ang.begin transaction), kończą się poleceniem zatwierdzenia (ang. commit) lubwycofania/odtwarzania transakcji (ang.rollback/recovery).

Wyróżnia się dwa poziomy odtwarzania: 
1. wewnątrz transakcji,
2. na poziomie systemowym.

**Odtwarzanie wewnątrz transakcji** dotyczy przypadków takich jak: 
- złe parametry lub ich nieprawidłowy format; 
- brak dostępu do danych w wyniku błędu w bazie; 
- niemożliwość wykonania żądanej modyfikacji (np. brak pamięci).

Jeżeli w wyniku błędu zostanie np. uszkodzona zawartość pamięci RAM, stan bazy danych zostanie odtworzony przez powrót do punktu kontrolnego i powtórzenie (redo) transakcji zapamiętanych w raporcie.

W przypadku wieloużytkownikowych baz danych– gdy występuje współbieżny dostęp do danych i równoległe przetwarzanie transakcji, problem właściwego ich przetwarzania dodatkowo się komplikuje.