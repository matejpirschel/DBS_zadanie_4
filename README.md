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
