[[Prístupy]]
[[Výkazy]]

Bolo by ideálne keby je základná funkčnosť integrácie hotová do 9.7.

  

Cieľom integrácie je pridať novú dopravnú metódu Packeta, ktorá umožní výber výdajných miest pri výbere dopravy v Odoo. Otvorí sa klasický packeta widget, kde sa zvolí adresa a táto adresa sa následne dostane do Odoo.

  

K dispozícii máme verziu 16.0, ktorá už má tieto funkcionality zapracované, avšak na verziu 16.0., neaktualizoval by som už tento existujúci model, ale zobral si z neho len to potrebné a prerobil to len na našu základnú funkčnosť - bez nejakej integrácie odosielania objednávky do Packety a pod.

  

[https://apps.odoo.com/apps/modules/16.0/packeta_integration](https://apps.odoo.com/apps/modules/16.0/packeta_integration)

  

Vývoj bude prebiehať na našom testovacom prostredí test.implemento.sk

  
  
  

**Nižšie posielam inštrukcie na vývoj a údaje na prístup cez SSH alebo FTP:**  
  
  
**Prístupové údaje  
**IP: 216.137.181.47  
port: 7822  
meno: developer  
heslo: b1255256sa21dd2a434  
  
Prístup funguje cez SSH aj cez FTP. Odporúčam pracovať cez IDE (napr. VSC) a využiť Remote SSH rozšírenie, vďaka ktorému budeš mať pripojenie aj úpravu súborov v jednom.  
  
**Štruktúra na serveri**  
V testovacom Odoo je modul umiestnený v prieč_in_ku: _/odoo/addons/developer/_

- V tomto prieč_in_ku už máš pripravenú “kostru” modulu, od ktorej sa môžeš odraziť.
- Každá zmena, ktorú urobíš v tomto prieč_in_ku, sa automaticky prejaví v testovacom Odoo (po reštarte kontajnera a upgrade modulu).  
    

**Práca v IDE (napr. Visual Studio Code)**

- Na_in_štaluj si rozšírenie Remote - SSH.
- Pridaj nové SSH pripojenie so zadanými údajmi (IP, port, používateľ, heslo).
- Po prihlásení nastav adresár na: /odoo/addons/developer/  
    
- V tomto prieč_in_ku už uvidíš súčasný “základ” modulu. Tu môžeš pridávať nové súbory, upravovať a pod.  
    
- **Nakoľko si prihlásený cez SSH, môžeš rovno využívať aj term_in_ál vo VSC, kde môžeš po úprave jednoducho reštartovať Odoo príkazom: sudo docker restart odoo-web-1  
    **

**Alternatíva namiesto IDE: FTP + SSH klient**Ak preferuješ _in_é riešenie:

- **FTP**: Pripoj sa na rovnaké údaje - IP, port, používateľ/heslo a upravuj súbory priamo vo svojom prieč_in_ku.
- **SSH klient (napr. PuTTY)**: Na FTP si upravíš a na reštart kontajnera prejdeš do putty a spustíš príkaz: **sudo docker restart odoo-web-1**

**  
Reštart Odoo a upgrade modulu  
  
Reštart kontajnera (v SSH alebo prostredníctvom term_in_álu v IDE):**

- sudo docker restart odoo-web-1

**Upgrade modulu**

- Prihlás sa do Odoo
- Prejdi do Aplikácie - nájdi si svoj modul, ktorý chceš aktualizovať, klikni v pravom hornom rohu na 3 bodky - Aktualizovať
- Alebo využi rozšírenie do vyhľadávača [https://chromewebstore.google.com/detail/odooterm_in_al/fdidojpjkbpfplcdmeaaehnjfkgpbhad](https://chromewebstore.google.com/detail/odooterminal/fdidojpjkbpfplcdmeaaehnjfkgpbhad)   
    V ktorom môžeš modul reštartovať príkazom upgrade -m <názov modulu> a nemusíš stále chodiť do aplikácií a ručne aktualizovať

**Prístup k testovaciemu Odoo  
**[test.implemento.sk  
](http://test.implemento.sk/)Používateľ: adm_in  
_Heslo: asdasdasd







Packeta dokumentácia - [https://docs.packeta.com/docs/introduction](https://docs.packeta.com/docs/introduction)  
[https://docs.packeta.com/docs/pudo-delivery/examples/packeta-pudos](https://docs.packeta.com/docs/pudo-delivery/examples/packeta-pudos)


Api key: 1f2ee18044b3d839
Api password: 1f2ee18044b3d8396d0e8dd94ff49f5b