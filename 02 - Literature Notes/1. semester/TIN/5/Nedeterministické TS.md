#TIN #Turingove_stroje #5_prednaska
> [!PDF|255, 208, 0] [[TIN-studijni-text.pdf#page=113&annotation=3712R|TIN-studijni-text, p.112]]
> > Nedeterministické Turingovy stroje

Pre jednu vstupnú konfiguráciu existuje viac možných výpočtov a slovo je akceptované pokiaľ ho akceptuje aspoň jeden z možných výpočtov.

![[TIN-studijni-text.pdf#page=113&rect=66,176,430,271&color=important|TIN-studijni-text, p.112]]

## Porovnanie s obyčajným TS
> [!PDF|187, 97, 229] [[TIN-studijni-text.pdf#page=114&annotation=3726R|TIN-studijni-text, p.113]]
> > Pro každý NTS  M  existuje DTS  M  ′  takový, že  L(M  ) =  L(M  ′).

NTS budeme simulovať trojpáskovým DTS:
1. prvá páska obsahuje vstupný reťazec
2. druhá páska je pracovná, obsahuje kópiu prvej pásky, po neúspešnom pokuse prijatia sa zmaže a nahradí obsahom prvej pásky
3. obsahuje kódovanú voľbu postupnosti prechodov, pri neúspechu bude jej obsah nahradený ďalšou postupnosťou, ktorá sa bude skúšať

Postup simulácie:
1. kopírovanie obsahu pásky 1 do pásky 2
2. generovanie ďalšej postupnosti prechodov na páske 3
3. simulácie postupnosti prechodov z pásky 3 na páske 2
4. pokiaľ sa dostaneme do koncového stavu tak ukončujeme proces, pokiaľ nie tak sa vraciame na krok 1

Nedeterminizmus nám vlastne z lineárneho stavového priesotru vytvára strom, snažíme sa nájsť čo najlepšie riešeni, preto sa postupnosti prechodov budú generovať najprv od tých najkratších, vyskúšajú sa všetky možnosti a až potom sa skúsia postupnosti s vačším počtom prechodov, teda ide o IDS - Iterative Depth Search.

> [!PDF|187, 97, 229] [[TIN-studijni-text.pdf#page=115&annotation=3729R|TIN-studijni-text, p.114]]
> > Zavedením nedeterminismu do TS se nezvyšují jejich schopnosti přijímat jazyky!


