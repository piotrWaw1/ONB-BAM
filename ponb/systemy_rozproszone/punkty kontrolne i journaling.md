## Punkty kontrolne
W przypadku programów podzielonych na moduły wykonywanych sekwencyjnie, konieczne jest weryfikowanie wyników częściowych. Wiąże się to z zapamiętaniem punktów kontrolnych.

Koncepcja punktów kontrolnych jest **podstawą techniki odtwarzania poprawnego stanu systemu**.

### Odtwarzanie wyprzedzające
W przypadku **odtwarzania wyprzedzającego** (ang. forward recovery) może wystąpić **zignorowanie błędu i przejście do kolejnej fazy programu**.
### Odtwarzanie wsteczne
Opiera się na **powrocie do określonych punktów programu** i **ponowieniu obliczeń**.

W zależności od tego, jak daleko należy się cofnąć, można wyróżnić odmiany tej techniki: 
1. Restart systemu.
2. Ponowienie określonej funkcji (ang. retry).
3. Powrót do punktu kontrolnego (ang. checkpoint).

## Journaling
Kolejne punkty kontrolne zapamiętują tylko sekwencje operacji które zmieniają stan pierwotny. Jest to tzw. odtwarzanie z dziennikiem (ang. journaling).
![[Pasted image 20250126133755.png]]
## Punkty kontrolne w systemach rozproszonych
**Migawka** **rozproszona** (ang. distributed snapshot), zwana też linią rekonstrukcji (ang. recovery line), polega na **zapisaniu spójnego, globalnego stanu całego systemu rozproszonego**.

Jeżeli proces odbiorczy ulegnie załamaniu, należy przywrócić go do poprawnego stanu z pomocą ostatniego punktu kontrolnego i ponowić (ang. replay) wszystkie komunikaty które po nim wystąpiły.