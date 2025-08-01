#TIN #Turingove_stroje #5_prednaska
> [!PDF|255, 208, 0] [[TIN-studijni-text.pdf#page=110&annotation=3700R|TIN-studijni-text, p.109]]
> > Vícepáskové Turingovy stroje

Má viac pásiek a čítacích hláv, ale rovnakú konečnú stavovú jednotku.

V jednom kroku najprv zvlášť na každej páske prečíta symbol, vykoná akciu a potom v závislosti na prečítaných symboloch zmení stav riadiacej jednotky.

> [!PDF|187, 97, 229] [[TIN-studijni-text.pdf#page=110&annotation=3703R|TIN-studijni-text, p.109]]
> > δ  : (Q  \ {qF  })  ×  Γ1  ×  Γ2  ×  ...  ×  Γk  −→  Q  ×  Γ′1  ×  Γ′2  ×  ...  ×  Γ′k
> 
> kde Γ′ i = Γi ∪ {L, R}

## Porovnanie s obyčajným TS
> [!PDF|187, 97, 229] [[TIN-studijni-text.pdf#page=112&annotation=3709R|TIN-studijni-text, p.111]]
> > Pro každý  k-páskový TS  M  existuje jednopáskový TS  M  ′  takový, že L(M  ) =  L(M  ′)

![[TIN-studijni-text.pdf#page=112&rect=64,241,290,366&color=important|TIN-studijni-text, p.111]]

Symbol na páske nemusí pozostávať len z jednoho znaku, teraz bude mať práve 2k znakov ak máme k pások:
- Jeden znak pre znak na páske
- Jeden znak pre označenie pozície hlavy:
	- 1 ak sa hlava nachádza na tejto pozícii
	- inak blank

### Jeden krok výpočtu
> [[TIN-studijni-text.pdf#page=113&annotation=3781R|TIN-studijni-text, p.112]]

Hlava takéhoto TS bude na zažiatku každého kroku 
výpočtu na začiatku v ľavo:
1. vyberie sa, ktorá k-páska sa má spracovať
2. budeme sa posúvať doprava, kým nenarazíme na 1 značiacu pozíciu k-hlavy na danej k-páske
3. prečítame symbol na vybranej k-páske
4. spracujeme akciu, posun k-hlavy sa realizuje prepisom pomocného symbolu značiaceho pozíciu k-hlavy
5. na konci sa hlava TS posunie znovu na najľavejšiu pozíciu

> [!PDF|187, 97, 229] [[TIN-studijni-text.pdf#page=113&annotation=3706R|TIN-studijni-text, p.112]]
> > Zvětšení paměťových možností TS nerozšiřuje jejich schopnosti přijímat jazyky!

