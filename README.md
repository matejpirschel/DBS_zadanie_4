# DBS_zadanie_4

## Používateľ
Obsahuje potrebné údaje pre prácu s účtami, teda prihlasovacie údaje poprípade informácie o prepojených učtoch s Google alebo Facebook.

## Postavy
Tabuľka spája všetkych hrdinov, teda postavy, s účtami používateľov a obsahuje informáciu, ktorá z postáv je aktuálne používaná.

## Priatelia, Tímy, IgnoreList, Pozvánky
Tabuľky podobného systému, kde každá obsahuje ID všetkých používateľov, ktorých sa dané kamarátstvo alebo vytvorenie tímu týka.
Pre tím je zvýraznený primárny hráč, ktorý bude určovať aktivity.
V pozvánke je len odosielajúci a prijímajúci hráč a poznámka, či bola pozvánka potvrdená alebo zamietnutá.

## Správy
Podobne ako pozvánka obsahuje odosielateľa a prijímateľa, text správy ako aj timestamp vytvorenia správy.
Prijímateľ je buď hráč, alebo skupina.

## Tipy
Tabuľka rád (hintov), ktoré sa budú zobrazovať počas loadingov a informujú hráča o možných zaujimavostiach, radách ku hre a podobne.

## Hrdina
Má v sebe uložené všetky potrebné informácie ohľadom životov, útoku, obrany, skúsenosti a mnoho ďaľších.
Hrdina sa odkazuje na tabuľku tried za pomoci kľuča ukazujúceho na triedu aktuálnej postavy.
Taktiež sa odkazuje na tabuľku inventáru, kde sú uložené všetky podstatné informácie k predmetom, ktoré má hráč pri sebe.
V tabuľke sú uložené aj všetky schopnosti získané hrdinom ako ID schopnosti oddelené čiarkami.
Rovnakým spôsobom sú uložené aj všetky prejdené úlohy, monštrá zabité aktuálnym hrdinom a prejdené lokácie.

## Triedy hrdinov
Musí obsahovať názov triedy a potrebné informácie pre levelovanie postavy.
Medzi tie patria informácie o počte skúseností pre získanie ďaľšieho levelu ako aj hodnotu o koľko sa zvýši každý atribút po zvýšení levelu.
Obsahuje aj záznam z tabuľky schopností, kde ukazuje na prvú schopnosť stromu pre danú triedu.

## Schopnosti
Schopnosti môžu byť buď aktívne, a teda ich použitie stojí energiu, doplnia životy, alebo spravia poškodenie a pred znovupoužitím treba počkať.
Samozrejme schopnosti môžu byť aj pasívne, teda je to len priamy prírastok k atribútom.
Každá schopnosť ukazuje na 0 až 3 schopnosti ktoré sa odomykajú kúpením danej schopnosti.

## Inventár
Uchováva zoznam všetkých zbraní, brnení, koristi, ako aj zoznam počtu koristí.
Zoznam je znova reprezentovaný ako string obsahujúci ID jednotlivých predmetov, oddelených čiarkami.
Taktiež je tu uložená informácia o aktuálne používanom brnení a zbrani.

## Nehratelna postava
Je to postava, u ktorej môže hrdina predávať alebo nakupovať predmety, poprípade si zvoliť úlohu, ktorú pôjde splniť
Obsahuje meno, popis, zozamy úloh a predmetov, ktoré sú u tejto postavi k dispozícii.
Taktiež má každá nehrateľná postava rôzne modifikátory predajných a nákupných cien zbraní a brnení. 

## Zbrane a Brnenia
Každý záznam popisuje jedinečné brnenie alebo zbraň.
Určuje množstvo atribútov, ktoré sú pri používaní predmetu pridané, ako aj poškodenie a dosah pre zbraň a zníženie utrpeného poškodenia pre pancier.
Zbrane aj brnenia majú určenú limitáciu minimálneho levelu pre použitie zbrane a pre každý predmet je určená základná cena pri kúpe a predaji.

## Korist 
Korisť je predmet, ktorý je možné získať zabitím príšery(napríklad lebka démona alebo zlatý prsteň). Tieto predmety môže hrdina následne predať u nehrateľnej postavy
Obsahuje informácie o názve, krátky popis, šancu na získanie, priemerný počet kusov koristi, ktoré zvyknú padnúť za zabitie démona a hodnotu danej koristi.

## Ulohy
Úlohy obsahujú svoj názov a popis, level, ktorý musí hrdina na odomknutie danej úlohy dosiahnuť, poprípade aký level musí predtým prejsť alebo akú príšeru zabiť, aby sa level odomkol.
Ďalej sú tam informácie o odporúčanom leveli hrdinu na vstup do úlohy, odmeny, ktoré dostane po jej splnení.
Taktiež je v tejto tabuľke zaznamenané, ktorí nepriatelia a v akých počtoch sa v úlohe postavia hrdinovi a na akej mape sa to bude odohrávať.

## Mapa a Levely
Mapa obsahuje záznamy o jednotlivých leveloch. Každý level má svoju výšku, šírku, svoje ID a informáciu o tom, ktorý level je potrebné prejsť, aby sa odomkol.
Levely zaznamenávajú, aký objekt sa nachádza na každom políčku levelu(spojenie x a y súradnice), typ určuje, či je na políčku spoluhráč, nepriateľ, príšera alebo objekt, poprípade nič, ID typu odkazuje na presný objekt na danom poli.

## Druhy textur
Táto tabuľka uchováva všetky druhy textúr, ktoré sa môžu vyskytnúť na mape.

## Log a Combat log
Logy zaznamenávajú údaje o všetkých bojoch, ktoré hrdina absolvoval. Presne odkazuje na to, ktorý hrdina v boji bol, aký mal vtedy level, akú mal zbraň a brnenie, počas akej úlohy tento boj nastal, combat log.
Zároveň odkazuje na démona, proti ktorému sa súboj odohral(z neho sa dá zistiť aj koľko xp za súboj hrdina získal)
Combat log ukazuje poradie v ktorom na seba nepriatelia útočili, poškodenia, ktoré dané útoky vykonali, poprípade aké typy útokov hrdina využil. 

## Link na fyzický diagram
https://dbdiagram.io/d/606f04aeecb54e10c33f567d
