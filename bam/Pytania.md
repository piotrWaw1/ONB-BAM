# Podstawy bezpieczeństwa aplikacji mobilnych
1. **Jakie są kluczowe elementy modelowania zagrożeń w aplikacjach mobilnych?**
	`Identyfikacja zasobów, analiza potencjalnych zagrożeń i podatności, ocena ryzyka oraz zaplanowanie mechanizmów zabezpieczeń.`
1. **Jakie są różnice między szyfrowaniem symetrycznym a asymetrycznym w kontekście aplikacji mobilnych?**
	`Szyfrowanie symetryczne używa jednego klucza do szyfrowania i deszyfrowania, co jest szybsze, ale wymaga bezpiecznego udostępnienia klucza. Asymetryczne wykorzystuje parę kluczy (publiczny i prywatny), co ułatwia bezpieczną wymianę danych, ale jest wolniejsze.`
3. **Czym jest zasada najmniejszych uprawnień i jak można ją zastosować w aplikacjach mobilnych?**
	`Polega na przyznawaniu użytkownikom i komponentom systemu tylko tych uprawnień, które są absolutnie niezbędne. W aplikacjach mobilnych stosuje się ją, ograniczając dostęp do zasobów, takich jak lokalizacja czy kontakty, wyłącznie wtedy, gdy jest to konieczne do działania aplikacji.`
4. **Jakie są różnice między bezpieczeństwem aplikacji mobilnych na Androidzie i iOS?**
	`Android umożliwia większą kontrolę przez użytkowników, ale jest bardziej podatny na zagrożenia z powodu otwartego ekosystemu. iOS ma bardziej restrykcyjne mechanizmy weryfikacji aplikacji i większą izolację procesów, co zwiększa bezpieczeństwo, ale zmniejsza elastyczność.`
5. **Jakie zagrożenia wynikają z niewłaściwego zarządzania sesjami w aplikacjach mobilnych?**
	`Mogą prowadzić do przejęcia konta przez atakującego (np. poprzez kradzież tokena sesji), eskalacji uprawnień czy nieautoryzowanego dostępu do danych użytkownika.`
# Bezpieczeństwo danych
6. Jakie techniki można wykorzystać do szyfrowania danych w aplikacji mobilnej?
	`Można wykorzystać algorytmy symetryczne (AES), asymetryczne (RSA) oraz funkcje skrótu (SHA). Dodatkowo stosuje się zabezpieczone magazyny danych, takie jak Keystore na Androidzie czy Keychain na iOS.`
7. Co to jest i jak działa protokół SSL/TLS?
	`SSL/TLS to protokoły zapewniające bezpieczną komunikację w sieci poprzez szyfrowanie transmisji danych. Działa, ustanawiając szyfrowane połączenie między klientem a serwerem z użyciem certyfikatów i mechanizmów uwierzytelnienia.`
8. Dlaczego przechowywanie danych w formie czystego tekstu jest ryzykowne?
	`Dane w czystym tekście mogą być łatwo przechwycone i odczytane przez atakujących w przypadku włamania, co zwiększa ryzyko naruszenia prywatności i bezpieczeństwa. Są łatwo dostępne w pamięci użądzenia za pomocą android adb.`
9. Jak bezpiecznie przechowywać dane uwierzytelniające w aplikacji mobilnej?
	`Należy używać zabezpieczonych magazynów, takich jak Android Keystore lub iOS Keychain, unikać przechowywania haseł w kodzie aplikacji oraz stosować mechanizmy szyfrowania. Zamiast danych przechowywać token uwierzytelniający z dadą ważności.`
10. Jakie są dobre praktyki dotyczące zarządzania kluczami szyfrującymi?
	`Klucze powinny być przechowywane w dedykowanych, zabezpieczonych magazynach, często rotowane, oraz dostęp do nich powinien być ograniczony zgodnie z zasadą najmniejszych uprawnień. Ważne jest także ich regularne audytowanie i unikanie twardego kodowania w aplikacji.`
# Uwierzytelnianie i autoryzacja
11. Co to jest uwierzytelnianie dwuskładnikowe (2FA)?
	`2FA to metoda zabezpieczenia, która wymaga dwóch różnych form weryfikacji tożsamości użytkownika, np. hasła (coś, co znasz) i kodu SMS lub odcisku palca (coś, co masz).`
12. Jak działa OAuth 2.0 w aplikacjach mobilnych?
	`OAuth 2.0 umożliwia aplikacjom uzyskanie dostępu do zasobów użytkownika na innych serwerach bez przechowywania hasła. Działa poprzez tokeny dostępu wydawane przez serwer autoryzacyjny po uwierzytelnieniu użytkownika.`
13. Jakie są różnice między uwierzytelnianiem biometrycznym a tradycyjnym?
	`Uwierzytelnianie biometryczne wykorzystuje unikalne cechy użytkownika, takie jak odcisk palca czy rozpoznawanie twarzy, podczas gdy tradycyjne opiera się na hasłach lub PIN-ach. Biometria jest wygodniejsza, ale w razie jej naruszenia trudniej ją zmienić niż hasło.`
14. Jakie ryzyko niesie za sobą przechowywanie tokenów uwierzytelniających w pamięci urządzenia?
	`Tokeny mogą zostać przechwycone przez atakujących w przypadku wycieku danych lub ataków malware, co może prowadzić do nieautoryzowanego dostępu do konta użytkownika.`
15. Jak działa mechanizm JWT (JSON Web Token) w kontekście aplikacji mobilnych?
	`JWT to tokeny zawierające dane użytkownika zakodowane w formacie JSON i podpisane cyfrowo. Są używane do uwierzytelniania i autoryzacji, pozwalając aplikacjom mobilnym na weryfikację tożsamości użytkownika bez ciągłego komunikowania się z serwerem. Składa się z tokenu i ładnunku zwaierającego dane.`
# Zarządzanie uprawnieniami
16. Dlaczego należy ograniczać uprawnienia aplikacji mobilnych?
	`Ograniczanie uprawnień minimalizuje ryzyko naruszenia prywatności użytkownika i zmniejsza potencjalne skutki złośliwych działań aplikacji lub jej podatności na ataki.`
17. Jak działa system uprawnień w Androidzie?
	`Android stosuje model oparty na deklaracjach w pliku manifestu i żądaniach podczas działania aplikacji. Użytkownik musi ręcznie zatwierdzić uprawnienia, a system grupuje je w kategorie (np. lokalizacja, kamera) w celu uproszczenia zarządzania.`
18. Co to jest Sandboxing i jak chroni aplikacje mobilne?
	`Sandboxing to mechanizm izolowania aplikacji w oddzielnych środowiskach, który zapobiega bezpośredniemu dostępowi do danych innych aplikacji lub systemu. Chroni to przed nieautoryzowanym dostępem i ogranicza skutki potencjalnych ataków.`
19. Jakie są najlepsze praktyki w zarządzaniu uprawnieniami aplikacji?
	`Przyznawaj uprawnienia zgodnie z zasadą najmniejszych uprawnień, proś o nie tylko wtedy, gdy są niezbędne, i edukuj użytkowników o ich celu. Regularnie audytuj aplikację, aby sprawdzić, czy wymagane uprawnienia są wciąż potrzebne.`
20. Jakie zagrożenia wiążą się z nadaniem aplikacji nadmiernych uprawnień?
	`Mogą prowadzić do wycieku danych użytkownika, inwigilacji lub złośliwego wykorzystania funkcji urządzenia (np. kamery lub mikrofonu) przez atakujących lub aplikacje o nieuczciwych intencjach.`
# Zabezpieczenia sieciowe
21. Dlaczego ważne jest szyfrowanie ruchu sieciowego w aplikacjach mobilnych?
	`Szyfrowanie chroni dane przesyłane między aplikacją a serwerem przed przechwyceniem i nieautoryzowanym dostępem, zapewniając poufność i integralność komunikacji.`
22. Co to jest atak typu Man-in-the-Middle (MitM)?
	`To rodzaj ataku, w którym napastnik przechwytuje i potencjalnie modyfikuje dane przesyłane między dwoma stronami, podszywając się pod jedną z nich bez ich wiedzy.`
23. Jak zabezpieczyć aplikację mobilną przed atakami typu MitM?
	`Używaj protokołów szyfrowanych, takich jak HTTPS z TLS, implementuj Certificate Pinning oraz weryfikuj certyfikaty serwera, aby upewnić się, że komunikacja odbywa się z zaufanym źródłem.`
24. Co to jest Certificate Pinning i jakie ma zastosowanie?
	`Certificate Pinning to technika, w której aplikacja zapisuje i używa konkretnego certyfikatu serwera, aby zapobiec podszywaniu się przez fałszywe certyfikaty. Chroni przed atakami MitM, szczególnie w przypadku luk w zaufanych urzędach certyfikacji.`
25. Dlaczego należy unikać używania nieszyfrowanych połączeń HTTP?
	`Nieszyfrowane połączenia HTTP są podatne na przechwycenie i modyfikację przez atakujących, co zagraża poufności i bezpieczeństwu danych przesyłanych przez aplikację.`
# Ataki i ochrona
26. Jakie są najczęstsze ataki na aplikacje mobilne (np. SQL Injection, XSS)?
	`Obejmują ataki, takie jak SQL Injection (wstrzykiwanie zapytań SQL do bazy danych), XSS (Cross-Site Scripting, wstrzykiwanie złośliwych skryptów), ataki typu Man-in-the-Middle (MitM), oraz kradzież danych uwierzytelniających i exploitowanie niezabezpieczonych API.`
27. Co to jest Reverse Engineering w kontekście aplikacji mobilnych?
	`Reverse Engineering to proces analizowania i dekompilacji aplikacji mobilnej w celu zrozumienia jej kodu, logiki lub mechanizmów zabezpieczeń. Może być stosowany przez atakujących do wykrycia podatności lub uzyskania dostępu do danych.`
28. Jakie techniki można zastosować, aby utrudnić Reverse Engineering aplikacji mobilnej?
	`Stosowanie obfuskacji kodu, szyfrowania krytycznych zasobów, weryfikacji integralności aplikacji, wykrywania debugowania i emulacji oraz minimalizacja wrażliwego kodu na urządzeniu (np. przesunięcie logiki na serwer).`
29. Jak działa analiza statyczna i dynamiczna aplikacji mobilnej?
	`Analiza statyczna bada kod aplikacji bez jej uruchamiania, np. dekompilując pliki APK/IPA. Analiza dynamiczna polega na obserwowaniu działania aplikacji w czasie rzeczywistym, np. monitorując ruch sieciowy lub wykorzystanie pamięci.`
30. Co to jest obfuskacja kodu i dlaczego jest stosowana?
	`Obfuskacja kodu to proces zaciemniania jego struktury, np. poprzez zmienianie nazw zmiennych i funkcji na niezrozumiałe. Utrudnia to Reverse Engineering, chroniąc aplikację przed analizą i potencjalnymi atakami.`
# Platforma Android
# Platforma iOS
# Testowanie bezpieczeństwa aplikacji mobilnych
# Zarządzanie bezpieczeństwem