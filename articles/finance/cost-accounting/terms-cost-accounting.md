---
title: Kuluarvestuse terminoloogia
description: See artikkel määratleb kuluarvestuses kasutatavad põhitingimused.
author: aprilolson
ms.date: 08/31/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostAccountingLedger
audience: Application User
ms.reviewer: twheeloc
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5827ad66b9eedaab88dbda97c1ebbcd15f6d9ac8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881929"
---
# <a name="cost-accounting-terminology"></a>Kuluarvestuse terminoloogia

[!include [banner](../includes/banner.md)]

See artikkel määratleb kuluarvestuses kasutatavad põhitingimused.

**Eraldamise alus**

Eraldamisalust kasutatakse tegevuste mõõtmiseks ja kvantifitseerimiseks, nt kasutatavad masina töötunnid, tarbitavad kilovatt-tunnid (kWh) või kasutatav pindala. Seda kasutatakse ühele või mitmele kuluobjektile kulude eraldamise alusena

**Kuluarvestus**

Kuluarvestus võimaldab koguda andmeid erinevatest allikatest, näiteks pearaamatust, alammoodulist, eelarvetest ja statistilisest teabest. Seejärel saate analüüsida, summeerida ja hinnata kuluandmeid, et haldus saaks teha parimad võimalikud otsused hinnavärskenduste, eelarvete, kulude kontrolli jne jaoks. Lähteandmeid, mida kasutatakse kuluanalüüsi jaoks, töödeldakse kuluarvestuses sõltumatult. Seetõttu ei mõjuta värskendused kuluarvestuses lähteandmeid. Siiski, kui kogute kuluandmeid erinevatest allikatest ja eriti kui impordite põhikontosid pearaamatust kuluelementidena, siis on andmete liiasus, kuna samad andmed eksisteerivad nii pearaamatus kui ka kuluarvestuses. See liiasus on vajalik, kuna kasutate välise aruandluse jaoks finantshaldust ja sisemise aruandluse jaoks kuluarvestust.

**Kuluarvestuse pearaamat**

See määratletakse kalendri, valuuta ja kuluelemendi dimensiooniga ning see kontrollib kulude mõõtmise protsesse ja poliitikaid. 

**Kulukirje**

Kulukirjed on pearaamatu kirjetest, kulu eraldamistest ja kulutöölehtedesse sisestatud kulukirjetest andmekonnektorite kaudu üleviimise tulemus.

**Kuluobjekt**

Igasugune objekti tüüp, mis on kulude juhtimiseks valitud. Kulud või tulud sisestatakse otse või eraldatakse kuluobjektidele. Mõned tüüpilised kuluobjektid on järgmised.

-  Tooted
-  Projektid
-  Osakonnad
-  Kulukeskused

Haldus kasutab kuluobjekte, et määrata kulude kogus, kuid samuti selleks, et juhtida tulususe analüüsi.

**Kuluelement**

Kasutatakse funktsioonina kulude jälgimiseks ja kategooriatesse jagamiseks. On kahte tüüpi kuluelemente: primaarsed ja sekundaarsed.

Primaarsed kuluelemendid tähistavad kuluvoogu finantsaruandlusest kuluarvestusse. Struktuur vastab tavaliselt pearaamatus kasumi ja kahjumi kontostruktuurile, kus kuluelement võib vastata põhikontole. Mitte kõiki põhikontosid ei pea ärinõuetest sõltuvalt tähistama kuluelementidena. 

Sekundaarsed kuluelemendid tähistavad sisemist kuluvoogu, kuna neid kulusid kasutatakse ainult kuluarvestuses. Neid kasutatakse kulu kokkuvõttereeglites kulude liitmiseks kirjeldavatesse vahemikesse, mida kasutatakse üldkulude arvutamiseks. 

**Kulu klassifikatsioon**

Kuluklassifikatsioon grupeerib kulusid nende jagatud omaduste järgi. Näiteks saab kulud grupeerida elementide, jälgitavuse ja käitumise alusel.

-   **Elementidega** – materjalid, tööjõud ja kulud.
-   **Jälgitavusega** – otsesed kulud ja kaudsed kulud. Otsesed kulud määratakse otse kuluobjektidele. Kaudsed kulud ei ole otseselt jälgitavad kuluobjektideni. Kaudsed kulud eraldatakse kuluobjektidele.
-   **Käitumisega** – fikseeritud, muutuv ja poolmuutuv.

**Kulukäitumine**

Kulukäitumine klassifitseerib kulud nende käitumise järgi seoses muudatustega peamistes äritegevustes. Kulude efektiivselt juhtimiseks peab haldus mõistma kulude käitumist. On kolme tüüpi kulukäitumise mustrit: fikseeritud, muutuv ja poolmuutuv.

- **Fikseeritud kulu** – fikseeritud kulu on kulu, mis ei varieeru lühiajaliselt hoolimata aktiivsustaseme muudatustest. Näiteks saab fikseeritud kulu olla äritegevuse põhiline tegevuskulu, nagu üür, mis ei saa mõjutada isegi tegevustaseme suurenemisel või vähenemisel.

- **Muutuv kulu** – muutuv kulu muutub aktiivsustaseme muudatuste järgi. Näiteks spetsiifilised otsesed materjalikulud on seotud iga müüdava tootega. Mida rohkem tooteid müüakse, seda otsesemad materjalikulud tekivad.

- **Poolmuutuv kulu** – poolvarieeruvad kulud on osaliselt fikseeritud ja osaliselt muutuvad kulud. Näiteks Interneti juurdepääsutasu hõlmab standardset igakuist juurdepääsutasu ja lairibaühenduse kasutamise tasu. Standardne igakuine juurdepääsutasu on fikseeritud kulu, samalajal kui lairibaühenduse kasutamise tasu on muutuv kulu.

**Kulu juhtseade**

Kulu juhtseade tähistab kulustruktuuri. See struktuur määrab, kuidas kulud hierarhilises järjekorras kuluobjekti dimensioonide ja nende vastavate kuluobjektide vahel liiguvad. 

**Kulu jaotus**

Kasutatakse kulu jaotamiseks ühelt kuluobjektilt ühele või mitmele teisele kuluobjektile, rakendades asjakohast eraldusalust. Kulujaotus ja kulueraldus erinevad selle poolest, et kulujaotus toimub alati algse kulu esmase kuluelemendi tasemel ja puudub vastastikune töötlemine.

**Kulude eraldamine**

Kasutatakse kuluobjekti saldo eraldamiseks teistele kuluobjektidele, rakendades eraldamisalust. Finance toetab vastastikuse eraldamise meetodit. Vastastikuse eraldamise meetodi puhul tuvastatakse täiendavate kuluobjektide vahetatavad vastastikused teenused. Süsteem määrab automaatselt eraldamiste tegemise järjekorra ja kordab seda. Kuluobjekti saldo eraldatakse üksiku eraldamisalusena. Toetatakse eraldamisi kuluobjekti dimensioonide ja nende vastavate liikmete seas. Eraldamisjärjekorda reguleerib kulujuhtseade.

**Kulude eraldamise poliitika**

Kulude eraldamise poliitika määratleb summad ja kogused, mis tuleb eraldada. Eraldamise reeglid hõlmavad eraldamise allikareegleid, mis määravad eraldatavad kulud, ja eraldamise sihtreegleid, mis määravad, kuhu kulud eraldatakse Näiteks kõik asutuse teenuste kulud on eraldamise allikas, mida saab eraldada erinevatele osakondadele organisatsioonis (see on eraldamise sihtmärkidele).

**Kulude koondamine**

Kulude kokkuvõttereeglite eesmärk on koondada kulud kirjeldavatesse vahemikesse. Liitmise tase on kasutaja määratletud ja hõlmab sekundaarse kuluelemendi määramist. Kui kulude koondamist ei kasutata, eraldatakse kulu iga üksik element ühest kuluobjektist teise

**Kulumäära poliitika**

Kulumäära kasutatakse hinna arvutamiseks kuluobjekti kohta. Hinna elementide mõistmiseks määratlete kulumäära poliitikad. On kahte tüüpi kulumäärasid: ajalooline kulumäär ja plaanitud kulumäär. Ajalooline kulumäär on arvutatud määr, mida kasutatakse kuluobjekti eraldamise aluse jaoks kordistina. Määr arvutatakse eelmise perioodi kulu eraldamiste põhjal. Plaanitud määr on kasutaja määratletud määr.

**Dimensioonihierarhia**

On kaks dimensioonihierarhiat: kategoriseerimise hierarhia ja klassifikatsiooni hierarhia. Tüüpi Dimensiooni kategoriseerimishierarhia kasutatakse aruandluseks. See toetab ainult kuluelemendi dimensioone. Tüüpi Dimensiooni klassifitseerimishierarhia kasutatakse poliitikate määratlemiseks ja aruandluseks. See toetab kõiki dimensioone, nt kuluobjekte, kuluelemente ja statistilisi dimensioone. 

**Andmekonnektor**

Kuluarvestus toetab lähtesüsteemidest pärinevate andmete integreerimist andmekonnektorite kogumi kaudu. Saadaval on järgmised andmekonnektorid.

-  Imporditud kanded (eelnevalt konfigureeritud)
-  Dynamics 365 finantsid (eel konfigureeritud)
-  Dynamics AX (vajalik on konfigureerimine)

**Märkus.** Andmekonnektor Imporditud kanded põhineb andmeüksustel.

**Andmepakkuja**

Enamik lähtesüsteeme suudab edastada andmeid, mis vastavad kuluarvestuses vähemalt ühele andmeallikale. Lähtesüsteemidest pärinevate andmete sobitamiseks kuluarvestuse andmeallikaga tuleb konfigureerida andmepakkuja. Järgmises tabelis on loetletud andmepakkujate saadavus andmekonnektori ja andmeallika kaupa.

|  **Andmeallikad** |  **Imporditud kannete andmekonnektor** | **Dynamics 365 Finance andmeühendus**  | **Dynamics AX-i andmekonnektor**  |
|---|---|---|---|
| Kuluelemendi dimensiooniliikmed  |  Jah | Jah  | Jah  |
|  Kuluobjekti dimensiooniliikmed |  Jah | Jah  | Jah  |
|  Statistilise dimensiooni liikmed | Jah  | Ei  | Ei  |
|  Pearaamat | Jah  | Jah  | Jah  |
|  Eelarvekanded  | Jah  | Jah  | Jah  |
|  Statistilised mõõdud | Jah  | Jah  | Jah  |

**Valem**

Valemi jaotamise aluste abil saate määratleda täpsemad valemid õige eraldamisaluse saavutamiseks. Valemi eraldamise aluseid saab käsitsi luua. Valemi määratlemiseks saab kasutada järgmisi tehtemärke.

|  **Sümbolid** | **Tekst**  |
|---|---|
|  ( ) | Sulud  |
|  < |  Väiksem kui |
|  > |  Suurem kui |
|  + |  Lisa |
|  – |  Lahutamine |
| *  | Korrutamine  |

Tavalisi IF-lauseid ei toetata. Kuid saate luua lauseid ja kinnitada, kas need on tõesed.

|  **Lause kinnitamine** | **Tulemus**  |
|---|---|
|  a > b| Tõene  |
|  a > b |  Väär |

**Üldkulud**

Üldkulud viitavad ärijuhtimise käimasolevatele kuludele. Need on kulud, mida ei saa siduda otseselt spetsiifiliste äritegevustega. Siin on mõned näited üldkuludest.

-   Raamatupidamistasud
-   Kulum
-   Kindlustus
-   Viivis
-   Õigusabikulud
-   Maksud
-   Kommunaalkulud

**Üldkulu määr**

Määrad määratletakse kuluobjekti ja kuluelemendi kohta. Määrasid on kahte tüüpi: rahandusperiood ja kasutaja määratud. Rahandusperioodi määrad arvutatakse üldkulude arvutusega. Kasutajapõhine määr on kasutaja määratletud ja seda saab kasutada kulude eraldamiseks kuluobjektide vahel eelnevalt määratletud määraga üldkulude arvutuses.

**Avaldatud**

Kui määrate sellel väljal väärtuse Jah, näeb kasutaja, kellele on määratud üks järgmistest rollidest, aruannet kulujuhtimise tööruumis.

-  Kuluarvestuse haldur
-  Kuluarvestaja
-  Kuluarvestuse ametnik
-  Kuluobjekti kontroller

Kui määrate sellel väljal väärtuse Ei, näevad ainult kasutajad, kellele on määratud üks järgmistest rollidest, aruannet kulujuhtimise tööruumis.

-  Kuluarvestuse haldur
-  Kuluarvestaja
-  Kuluarvestuse ametnik

**Statistiline dimensioon**

Statistilist dimensiooni ja selle liikmeid kasutatakse mitterahaliste kirjete registreerimiseks ja juhtimiseks kuluarvestuses. Statistilise dimensiooni liikmeid saab kasutada kahel eesmärgil:

-  eraldamisalusena poliitikates nagu kulu jaotus või kulu eraldamine;
-  mitterahalise tarbimise registreerimiseks.

Statistiline dimensioon on tegevuste arvu või summa avaldis, mida saab kasutada eraldamiste või kulumäära arvutuste alusena. See luuakse käsitsi või imporditakse lähtesüsteemidest. Statistiliste dimensioonide näited hõlmavad töötajate arvu, litsentsitud tarkvara arvu igas seadmes, iga masina energiatarvet või kulukeskuse ruutmeetreid.

**Avaldis**

Väljavõtted on vaated juhtidele, kes vastutavad kulude kontrollimise eest. Väljavõtted on määratletud kulukontrolleriga ja need annavad kiirülevaate tegelikest ja eelarvestatud kuludest ning hälvetest. Juht saab minna vajaduse korral süvitsi üksikasjadesse. Aitamaks tagada, et haldurid vaatavad ainult andmeid, mille eest nad vastutavad, kehtivad väljavõtetes ilmunud andmetele juurdepääsureeglid.

**Versioon**

Versioone kasutatakse erinevate väljundite stimuleerimiseks, kuvamiseks ja võrdlemiseks. Vaikimisi kuvatakse kõik tegelikud kulud ühes alusversioonis, mis on tuntud kui *tegelik*. Eelarvete ja arvutuste jaoks saate töötada nii paljude versioonidega kui vaja. Näiteks saate importida eelarve andmed originaalversiooni ja seejärel muuta eelarvet muudetud versioonis. Arvutuste puhul saate luua mitu versiooni. Nendes erinevates versioonides saate seejärel luua arvutused, kasutades erinevaid arvutusreegleid, mis rakendatakse kulueraldamisele.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
