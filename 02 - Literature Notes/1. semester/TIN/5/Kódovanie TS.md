#TIN #Turingove_stroje #Medze_rozhodnutelnosti #5_prednaska
> [!PDF|255, 208, 0] [[TIN-studijni-text.pdf#page=125&annotation=3743R|TIN-studijni-text, p.124]]
> > Kódování TS

Je potrebné zakódovať stavy, symboly z Γ a prechodové funkcie δ.

Kódovanie stavov :
- usporiadame stavy do posrupnosti q0, qF , q, p, ..., t
- stav q_j zak=odujeme ako 0^j
- qo = ε, q1 = 0, q2 = 00, q3 = 000, ...
[[TIN-studijni-text.pdf#page=125&annotation=3759R|TIN-studijni-text, p.124]]

Kódovanie symbolov a príkazov L a R:
- symboly do postupnosti a1, a2, a3, ..., an
- ∆ → ε, L → 0, R → 00, a_i → 0^(i+2)
- a1 = 000, a2 = 0000, a3 = 00000, ...
[[TIN-studijni-text.pdf#page=125&annotation=3751R|TIN-studijni-text, p.124]]

Kódovanie prechodov:
- kódujeme ako štvoricu p x q y
- p je aktuálny stav
- x je symbol pod hlavou
- q je následujúci stav
- y je nový symbol alebo posun L alebo R
- na oddelenie sa používa znak 1

Kódovanie celého TS:
- kódy jednotlivých prechodov oddelené znakom 1
![[TIN-studijni-text.pdf#page=125&rect=141,123,380,181&color=note|TIN-studijni-text, p.124]]
