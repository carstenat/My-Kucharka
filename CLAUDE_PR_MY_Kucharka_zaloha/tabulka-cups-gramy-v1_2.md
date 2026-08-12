# Referenčná tabuľka: gramy vs. cups/lyžice (v1.2 — rekonštruovaná)

**Dôležitá poznámka k tejto verzii:** pôvodný súbor `tabulka-cups-gramy-v1_1.md`
bol omylom vymazaný z Project files. Toto je jeho rekonštrukcia — štruktúra
(kategórie A-H) zodpovedá presne sekcii 8 master promptu "Rastlinný Nutričný
Kuchár" v1.12. Hodnoty nižšie boli buď (a) prevzaté priamo z citácií v samotnom
master prompte, (b) prevzaté z poznámok v `recipes.json` (napr. yield faktor
šošovice), alebo (c) čerstvo overené cez web search v konverzácii, kde táto
rekonštrukcia vznikla — nič nie je doplnené z pamäte bez overenia. Zoznam
surovín nižšie pokrýva to, čo sa reálne používa v tvojich 9 receptoch
(`recipes.json`), plus pár bežných referenčných príkladov citovaných priamo
v master prompte. Ak pôvodná tabuľka obsahovala ďalšie suroviny, ktoré tu
chýbajú, priebežne ich dopĺňaj podľa pravidla v sekcii 6 master promptu
("ak surovina chýba, over ju raz a pridaj").

Účel: lookup tabuľka pre AI asistenta — namiesto opakovaného generovania
g/cup prepočtov pri každom recepte. Používa sa v kroku sekcie 8 master promptu.

---

## Kategória A — Sypké husté/zrnité (múka, ryža, ovos, cukor)

| Surovina | g / 1 cup | Zdroj/poznámka |
|---|---|---|
| Pšeničná múka, hladká | 120 g (nabraté lyžicou a zarovnané) / 140 g (natlačené) | King Arthur Baking — citované priamo v master prompte, sekcia 8 |
| Ovsené vločky | ~81 g | bežná konvencia (nabrané, nezarovnané natlačením) |

---

## Kategória B — Suché strukoviny/zrná v celku (šošovica, cícer, quinoa)

| Surovina | g / 1 cup (suché) | Zdroj/poznámka |
|---|---|---|
| Šošovica, suchá (všeobecne) | ~190-200 g | overené cez web search, viacero zhodných zdrojov (density ~0,80-0,85 g/ml) |
| Šošovica červená, suchá | ~190 g | rovnaká kategória hustoty ako šošovica všeobecne — používaná v receptoch "gulas" a "sosovica-miso" |
| Cícer, suchý | ~190-200 g | overené cez web search |
| Quinoa, nevarená | ~170 g | overené cez web search (USDA FoodData Central) |

---

## Kategória C — Listová zelenina/bylinky (rukola, špenát, petržlen)

| Surovina | g / 1 cup | Zdroj/poznámka |
|---|---|---|
| Rukola, voľne nasypaná | ~20 g | USDA FoodData Central — citované priamo v master prompte, sekcia 8; použité v recepte "gulas" |
| Rukola, natlačená/baby | ~45 g | overené cez web search — viac než 2× rozdiel oproti voľne nasypanej, presne ako upozorňuje master prompt |

Pri tejto kategórii vždy explicitne označ "voľne nasypaná" alebo "natlačená" — rozdiel je príliš veľký na to, aby sa dal ignorovať.

---

## Kategória D — Nepravidelné kúsky/premenlivý tvar (sójové kocky/TVP, sušené huby, hrubo nasekané orechy)

Cup konverzia je nespoľahlivá — uvádzaj **iba gramy** (prípadne kusy/ks), cup nepridávaj.

| Surovina | Poznámka |
|---|---|
| Sójové kocky (TVP), sušené | Iba gramy — recept "gulas" používa 100 g. Cup prepočet zámerne nepridávaj (kategória D pravidlo). |
| Sušené paradajky (nie v oleji) | Iba gramy — recept "fazula" používa 40 g. |
| Sušené brusnice, nahrubo nasekané | Iba gramy — recept "pohanka-brusnice-mandle" používa 30 g. |

---

## Kategória E — Čerstvá nakrájaná zelenina/ovocie (kocky sladký zemiak, mrkva)

| Surovina | Poznámka |
|---|---|
| Sladký zemiak, kocky ~2 cm | Recept "gulas": 2 ks (~400 g) — pri štandardnej veľkosti kociek je cup rozumne konzistentný, ale gram ostáva primárny. |
| Brokolica, mini ružičky | Recept "panvica-tofu-fazula": 150 g. |

---

## Kategória F — Tekutiny (voda, vývar)

Cup = objem, bez problému. 1 cup = ~237 ml (US cup).

| Bežné množstvá v receptoch | Poznámka |
|---|---|
| Zeleninový/hubový vývar | Používa sa v ml priamo (napr. "pohanka-pilaf": 360 ml = 1½ hrnčeka), žiadny prepočet netreba. |

---

## Kategória G — Husté pasty/hotové nátierky (rozmixovaná fazuľová nátierka, hummus a pod.)

Hustota sa nedá odvodiť zo surových vstupov (mixovanie mení objem) — odhaduje sa samostatne, typicky blízko hustote vody (~1 g/ml).

| Recept | Odhad hustoty | Poznámka |
|---|---|---|
| "fazula" (biela fazuľa & sušené paradajky) | ~1 g/ml | portionWeight ~146 g ≈ ½-⅔ cup — hodnota z `recipes.json`, zatiaľ nie samostatne web-search overená; over pri ďalšom podobnom recepte. |
| "sosovica-miso" | ~1 g/ml | portionWeight 138-154 g ≈ ½-⅔ cup — z `recipes.json`. |
| "tofu-paprika" | ~1 g/ml | portionWeight ~135 g ≈ ½ cup — z `recipes.json`. |

---

## Kategória H — Yield faktor pri varení strukovín/obilnín (suchá → uvarená hmotnosť)

NIE JE to cup→gram prepočet ako kategórie A-G — je to prepočet suchá→uvarená hmotnosť, na odhad fyzickej hmotnosti hotovej porcie (nikdy nie na nutričný prepočet, ten sa vždy počíta zo suchej/surovej hmotnosti, pozri sekciu 7e master promptu).

| Surovina | Yield faktor (suchá → uvarená) | Zdroj/úroveň dôkazu |
|---|---|---|
| Šošovica červená, suchá → uvarená | ~2,3-2,6× | Použité v recepte "sosovica-miso" (`recipes.json`) — kuchárske zdroje, primeraná zhoda s web-search overením (viacero zdrojov uvádza dried lentils "expand to about 2.5 to 3 times their original volume when cooked", hmotnostný faktor je v podobnom ráde). |
| Pohanka (svetlá bio, nepražená) → uvarená v pare | ~3,0-3,6× | Použité v recepte "pohanka-pilaf" (`recipes.json`) — kuchárske zdroje, nie USDA, nižšia úroveň dôkazu. Autor receptu odporúča overiť váhou po uvarení pri budúcom použití. |

---

## Doplnkové referenčné hodnoty (surové/suché, na 100 g — pre kontext, nie primárny účel tejto tabuľky)

Tieto hodnoty pomáhajú pri kontrole per100g výpočtov (sekcia 9 master promptu), nie sú náhradou nutričnej databázy:

| Surovina | g/cup (surová/suchá) | Zdroj |
|---|---|---|
| Pohanka (groats), surová/nepražená | ~180-190 g | overené cez web search (Bob's Red Mill: 45 g/¼ cup = 180 g/cup; iný zdroj 190 g/cup) |
| Pohanka (groats), pražená (kasha) | ~164-173 g | overené cez web search — mierne odlišná hustota od nepraženej, nepoužívaj zamenené |

---

*Dopĺňať priebežne o ďalšie páry podľa toho, aké suroviny sa reálne používajú
v nových receptoch — presne ako pri `tabulka-nutricnych-interakcii.md`.*

*Táto tabuľka (v1.2) je rekonštrukcia po neúmyselnom vymazaní pôvodného
súboru. Ak sa niekde nájde záloha originálu (`tabulka-cups-gramy-v1_1.md`),
uprednostni ju pred touto verziou a over rozdiely.*
