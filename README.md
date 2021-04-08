# DBS_zadanie_4

## Používateľ
Obsahuje potrebné údaje pre prácu s účtami, teda prihlasovacie údaje po prípade informácie o prepojených učtoch s Google alebo Facebook

## Postavy
Tabuľka spája všetkych hrdinov teda postavy s účtami používateľov a obsahuje informáciu či je jedna z postáv aktuálne používaná.

## Priatelia, Tými, IgnoreList, Pozvánky
Tabuľky podobného systému kde každá obsahuje ID všetkých používateľov ktorých sa dané kamarátstvo alebo vytvorenie týmu týka.
Pre tým je zvýraznený primárny hráč ktorý bude určovať aktivity.
V pozvánke je len odosielajúci a prijimajúci hráč a poznámka či bola pozvánka potvrdená alebo zamietnutá.

## Správy
Podobne ako pozvánka obsahuje odosielateľa a prijímateľa, text správy ako aj timestamp vytvorenia správy.
Prijímateľ je buď hráč alebo skupina.

## Tipy
Tabuľka rád (hintov) ktoré sa budú zobrazovať počas loadingov a informujú hráča o možných zaujimavostiach, radách ku hre a podobne.

## Hrdina
Má v sebe uložené všetky potrebné informácie ohľadom životov, útoku, obrany, skúsenosti a mnoho ďaľších.
Hrdina sa odkazuje na tabuľku tried za pomoci kľuča ukazujúceho na triedu aktuálnej postavy.
Taktiež sa odkazuje na tabuľku inventáru kde sú uložené všetky podstatné informácie k predmetom ktoré má hráč u seba.
V tabuľke sú uložené aj všetky schopnosti získané hrdinom ako ID schopnosti oddelené čiarkami.
Rovnakým spôsobom sú uložené aj všetky prejdené úlohy, monštrá zabité aktuálnym hrdinom a prejdené lokácie.

## Triedy hrdinov
Musí obsahovať názov triedy a potrebné informácie pre levelovanie postavy.
Medzi tie patria informácie o počte skúseností pre získanie ďaľšieho levelu ako aj hodnotu o koľko sa zvýši každý atribút po zvýšení levelu.
Obsahuje aj záznam z tabuľky schopností kde ukazuje na prvú schopnosť stromu pre danú triedu.

## Schopnosti
Schopnosti môžu byť buď aktívné, a teda ich použitie stojí energiu, doplnia životy alebo spravia poškodenie, a pred znovupoužitím treba počkať.
Samozrejme schopnosti môžu byť aj pasívne, teda je to len priamy prírastok k atribútom.
Každá schopnosť ukazuje na 0 až 3 schopnosti ktoré sa odomykajú kúpením danej schopnosti.

## Inventár
Uchováva zoznam všetkých zbraní, brnení koristi ako aj zoznam počtu koristí.
Zoznam je znova reprezentovaný ako string obsahujúci ID jednotlivých predmetov oddelených čiarkami.
Taktiež je tu uložená informácia o aktuálne používanom brnení a zbrani.

## Zbrane a Brnenia
Každý záznam popisuje jedinečné brnenie alebo zbraň.
Určuje množstvo atribútov ktoré sú pri používaní predmetu pridané ako aj poškodenie a dosah pre zbraň a zníženie utrpeného poškodenia pre pancier.
Zbrane aj brnenia majú určenú limitáciu minimálneho levelu pre použitie zbrane a pre každý predmet je určená priemerná cena pri kúpe a predaji.
