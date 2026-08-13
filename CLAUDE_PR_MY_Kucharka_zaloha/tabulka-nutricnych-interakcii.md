# Referenčná tabuľka nutričných interakcií (v1.1)

Účel: lookup tabuľka pre AI asistenta — namiesto opakovaného generovania
biochémie pri každom recepte. Používa sa v kroku sekcie 6 master promptu.

**Zmeny oproti v1.0:** riadky "Fytáty" a "Oxaláty" prepísané s presnými
percentami a primárnymi zdrojmi namiesto všeobecného opisu — pôvodné znenie
("namáčanie, klíčenie, fermentácia, varenie" / "varenie/blanšírovanie
oxaláty výrazne zníži") bolo vecne nepresné, keďže miešalo dokopy metódy
prípravy s výrazne odlišnou účinnosťou. Doplnený nový riadok "Cesnak/cibuľa
ako enhancer" (samostatný mechanizmus od vitamínu C). Zdroje overené cez
web search v konverzácii 13. augusta 2026, podľa dôkazovej hierarchie
sekcie 6 master promptu — prehľadové/experimentálne štúdie ako primárny
zdroj, NutritionFacts.org/Greger len ako navigácia k nim.

| Faktor v surovine | Suroviny (typicky) | Efekt | Zmiernenie / synergia |
|---|---|---|---|
| Fytáty | strukoviny, celozrnné obilniny, orechy | ↓ vstrebávanie Fe, Zn, Ca, Mg (fytát viaže dvojmocné katióny v čreve do nerozpustných komplexov) | **Namáčanie:** slabý až stredný efekt, ~4-51 % redukcia fytátu podľa suroviny/dĺžky (vysoko premenlivé). **Klíčenie:** účinnejšie, ~30-85 % redukcia. **Fermentácia** (najmä s baktériami produkujúcimi fytázu): najúčinnejšia metóda, bežne ~50-85 %, v kombinácii so sprouting/soaking až >85 %. Zdroj: prehľad ľudských intervenčných štúdií 1990-2024 (42 zaradených prác) potvrdzuje zníženú vstrebateľnosť Fe/Zn pri strave bohatej na fytát a zlepšenie pri redukcii fytátu (PMC11807532, 2024); konkrétne % z Lestienne et al. 2005, *Food Chem*; Mahgoub & Elhag 1998. **Vitamín C v tom istom jedle** (~50-80 mg) čiastočne kompenzuje fytátovú záťaž priamo pri vstrebávaní železa, nezávisle od redukcie samotného fytátu. |
| Cesnak/cibuľa ako enhancer | alliová zelenina (cesnak, cibuľa, pór) pridaná do jedla s fytátovou surovinou | žiadny priamy efekt na fytát, ale zlepšuje bioaccessibilitu Fe a Zn v tom istom jedle nezávislým mechanizmom od vitamínu C | Zdroj: Gautam, Platel & Srinivasan 2010, *J Agric Food Chem* — "Higher bioaccessibility of iron and zinc from food grains in the presence of garlic and onion." Praktické pre WFPB recepty: cesnak/cibuľa sú takmer vždy prítomné → tento efekt sa deje automaticky vo väčšine receptov kuchárky, netreba ho špeciálne pridávať, len si ho uvedomiť ako dôvod, prečo je báza cibuľa+cesnak nutrične výhodná, nie len chuťová. |
| Oxaláty | špenát, mangold, repa, rebarbora | ↓ vstrebávanie vápnika (aj vlastného vápnika v surovine) — oxalát viaže Ca²⁺ do nerozpustného kalcium-oxalátu | **Metóda prípravy má zásadný rozdiel, nie je jedno "varenie" ako kategória:** var v ponorenej vode (boiling) s následným scedením znižuje rozpustné oxaláty o 30-87 % (u špenátu konkrétne ~51 %, 978→477 mg/100g) — Chai & Liebman 2005, *J Agric Food Chem* 53:3027-3030, potvrdené viacerými nadväzujúcimi štúdiami. Parenie/dusenie (steaming) má oveľa slabší efekt, len ~5-15 % (rozsah v štúdiách 5-53 %) — jedlo nie je ponorené, oxalát odchádza len kondenzáciou/odkvapkávaním. Pečenie/opekanie nasucho — minimálny až žiadny efekt. **Dôležité pre eintopfy/guláše:** ak sa voda/vývar po varení nescedí, ale ostáva v jedle (bežný štýl tejto kuchárky), vyplavovací efekt sa nevyužije — oxalát sa vráti späť do pokrmu. Efekt boilingu platí len pri scedení. |
| Vápnik z nízko- vs. vysoko-oxalátovej zeleniny | kel, brokolica, bok choy (nízke oxaláty) vs. špenát, mangold (vysoké) | zásadný rozdiel vo vstrebateľnosti vápnika bez ohľadu na úpravu | Kel: frakčná absorpcia vápnika ~0,409 (41 %) — vyššia než z kravského mlieka (~0,321, 32 %). Vápnik v kelu je vo forme rozpustnej organickej soli (citrát/malát). Špenát: vápnik existuje prevažne ako nerozpustný kalcium-oxalát, rozpustnosť <2 % — vstrebateľnosť ostáva nízka aj po uvarení, keďže ide o chemickú formu viazania, nie len o množstvo oxalátu. Zdroj: Weaver, Heaney, Martin & Ebner 1988, *Am J Clin Nutr* 47:707-709 (kel vs. mlieko); Hanes, Purdue University disertácia (chemická forma Ca v špenáte/kelu). **Praktický záver pre recepty:** ak recept potrebuje vápnik z listovej zeleniny, uprednostni kel/brokolicu/bok choy pred špenátom/mangoldom — toto je silnejšia páka než akákoľvek úprava vysoko-oxalátovej zeleniny. |
| Taníny | čaj, káva, niektoré bobule/šupky strukovín | ↓ vstrebávanie nehémového železa (aj o desiatky %) | konzumovať s odstupom 1-2 h od hlavného jedla bohatého na Fe |
| Vitamín C | citrusy, paprika, kel, paradajky | ↑ vstrebávanie nehémového železa (aj 3-6×) | kombinuj so strukovinami/celozrnnými pri každom jedle, kde záleží na Fe |
| Polyfenoloxidáza (PPO) | banán, jablko, avokádo (vysoká aktivita) | rozkladá flavan-3-oly/flavanoly z bobúľ, kakaa pri mixovaní/kontakte (až -84 % vstrebávania, Ottaviani 2023) | nahraď PPO-ovocie nízko-PPO alternatívou (ananás, pomaranč, mango) alebo pridaj tesne pred podávaním |
| Karotenoidy (provitamín A) | mrkva, tekvica, sladký zemiak, paradajky | potrebujú aspoň malé množstvo tuku pre vstrebávanie | v oil-free recepte: pridaj lyžicu mletých orechov/semienok alebo pár plátkov avokáda |
| Vitamíny D, E, K (tukorozpustné) | zelená listová zelenina, celozrnné | potrebujú tuk pre vstrebávanie | ako vyššie — celé orechy/semienka namiesto oleja |
| Vápnik vs. železo (vysoká súčasná dávka) | tofu/sezam/mak + strukoviny v tom istom jedle | mierna vzájomná súťaž o vstrebávanie pri veľmi vysokých dávkach naraz | pri bežných porciách zanedbateľné; riešiť len pri zámerne vysokých dávkach oboch |
| Vláknina (rozpustná) | ovos, strukoviny, jablká | spomaľuje trávenie → znižuje glykemickú odpoveď celého jedla | žiadané pri cieli "sýte, kalorický efektívne" |

**Ako používať:** pri zostavovaní receptu skontroluj suroviny oproti stĺpcu 2.
Ak je zhoda a chýba zmiernenie/synergia zo stĺpca 4, pridaj krátku poznámku
s konkrétnym riešením do výstupu (sekcia 7 master promptu). Ak je zmiernenie
už v recepte prítomné, netreba nič dodávať.

**Dôležité pri oxalátoch/fytátoch — kontrola metódy, nie len suroviny:**
Pri písaní poznámky o oxalátoch/fytátoch vždy over, či tvrdenie zodpovedá
**skutočnej metóde prípravy v danom recepte** (var v ponorenej vode + scedenie
vs. dusenie/parenie/pečenie), nie všeobecnému tvrdeniu o surovine. Napr. "kel
má nízke oxaláty" je fakt o surovine (platí vždy), ale "varenie znižuje
oxaláty" platí len pri konkrétnej technike (var vo vode + scedenie) — ak
recept zeleninu len dusí/paruje/opeká, netvrď, že to oxaláty rieši.

*Dopĺňať priebežne o ďalšie páry podľa toho, aké suroviny sa reálne používajú.*
