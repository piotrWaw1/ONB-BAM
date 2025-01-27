## 1. Systemy z nadmiarowością bierną. 
Redundancja jest aktywna przez cały czas działania systemu.
## 2. Systemy z nadmiarowością dynamiczną (aktywną).
Aktywna jest tylko część identycznych podzespołów, reszta stanowi zapas. Z elementów zapasowych korzysta się w tedy, gdy jeden z elementów głównych ulegnie uszkodzeniu –**następuje dynamiczna rekonfiguracja**.
## 3. Systemy z nadmiarowością hybrydową
Elementy zapasowe są aktywne przez cały czas działania systemu, ale o wyniku działania decyduje tylko część tych elementów. Jeżeli aktywny element ulegnie uszkodzeniu, szybko może zostać zastąpiony podzespołem zapasowym.
## 4. Systemy z łagodną degradacją (gracefully degradating systems)
Podobne do systemów z nadmiarowością hybrydową. W razie uszkodzenia podzespołu jego funkcje przejmuje inny element, normalnie wykonujący inne funkcje. Systemy tolerują błędy kosztem zmniejszenia wydajności.