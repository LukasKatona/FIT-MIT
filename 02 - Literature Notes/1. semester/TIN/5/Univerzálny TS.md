#TIN #Turingove_stroje #Medze_rozhodnutelnosti #5_prednaska
> [!PDF|255, 208, 0] [[TIN-studijni-text.pdf#page=125&annotation=3737R|TIN-studijni-text, p.124]]
> > Univerzální TS

Umožnuje vo vstupnom reťazci špecifikovať nie len dáta ale aj zakódovaný TS.
[[TIN-studijni-text.pdf#page=125&annotation=3743R|TIN-studijni-text, p.124]]

Kód TS aj vstupný reťazec sa zakóduje podľa [[Kódovanie TS]] a tieto dve veci sa oddelia #.

![[TIN-studijni-text.pdf#page=126&rect=66,609,343,653&color=note|TIN-studijni-text, p.125]]

Univerzálny TS môžeme navrhnuť ako trojpáskový TS:
1. prvá páska obsahuje zadanie, neskor výstup
2. druhá páska je pracovná
3. tretia páska obsahuje aktuálny stav a aktuálnu pozíciu hlavy, ktorá je kódovaná ako 0^i
[[TIN-studijni-text.pdf#page=126&annotation=3765R|TIN-studijni-text, p.125]]

Simulácia:
1. stroj skontroluje, či vstup odpovedá zadaniu, pokiaľ nie tak abnormálne zastaví
2. na druhú pásku umiestni vstupný reťazec w a na tretiu pásku uloží počiatočný stav a pozíciu hlavy, ľavý okraj pásky
3. na druhej páske vyhľadá aktuálny symbol pod hlavou, na prvej páske vyhľadá prechod preveditelný z aktuálneho stavu uloženého na páske 3 pre tento vstupný symbol, pokiaľ neexistuje možný prechod, stroj abnormálne zastaví
4. stroj prevedie zmeny na páske 2 a 3 podla simulovaného prechodu
	1. prepis symbolu
	2. zmena aktuálneho stavu, pozícia hlavy
5. pokiaľ nebol dosiahnutý koncový stav prejde sa na krok 3, inak sa vymaže obsah prvej pásky a vloží sa na ňu obsah druhej pásky
[[TIN-studijni-text.pdf#page=126&annotation=3768R|TIN-studijni-text, p.125]]