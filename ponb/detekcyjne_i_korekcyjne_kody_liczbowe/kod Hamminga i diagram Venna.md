## Kod Hamminga
Algorytm Hamminga pozwala na budowanie kodów korekcji błędów (liniowego kodu Hamminga) dla dowolnego rozmiaru słowa informacyjnego. Kody tego typu mogą **korygować** **pojedyncze błędy**.

Słowom-bitowe uzupełniane jest przez r bitów parzystości, prowadząc do utworzenia nowego o długości r+m. Bity numerowane są począwszy od 1, zaczynając od najbardziej znaczącego. **Bity których numer jest potęgą 2 to bity parzystości**.
![[Pasted image 20250126141229.png]]
Kody Hamminga mają odległość D=3, dlatego błędy podwójne mogą być mylone z błędem pojedynczym innego ciągu kodowego.

Dołączenie dodatkowego bitu parzystości (dla kompletnego słowa) zwiększa odległość Hamminga do 4 i pozwala wykrywać błędy podwójne. Ten system kodowania znany jest jako SEC/DED (Single Error Correction, Double Error Detection).

## Diagram Venna
![[Pasted image 20250122154109.png]]
