---
title: Kuluarvestuse terminoloogia
description: "See teema määratleb põhimõisted, mida kasutatakse kuluarvestuses."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMCostControlWorkspaceConfiguration
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7ce12337c22542aea2002ffc5abd09e4f4d770c1
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="cost-accounting-terminology"></a>Kuluarvestuse terminoloogia

[!include[banner](../includes/banner.md)]


See teema määratleb põhimõisted, mida kasutatakse kuluarvestuses.

**Kuluarvestus**

Kuluarvestus võimaldab koguda andmeid erinevatest allikatest, näiteks pearaamatust, alammoodulist, eelarvetest ja statistilisest teabest. Seejärel saate analüüsida, summeerida ja hinnata kuluandmeid, et haldus saaks teha parimad võimalikud otsused hinnavärskenduste, eelarvete, kulude kontrolli jne jaoks. Lähteandmeid, mida kasutatakse kuluanalüüsi jaoks, töödeldakse kuluarvestuses sõltumatult. Seetõttu ei mõjuta värskendused kuluarvestuses lähteandmeid. Kui kogute kuluandmeid erinevatest allikatest ja eriti kui impordite põhikontosid pearaamatust rakenduses Microsoft Dynamics 365 for Operation kuluelementidena, siis on andmete liiasus, kuna samad andmed eksisteerivad nii pearaamatus kui ka kuluarvestuses. See liiasus on vajalik, kuna kasutate välise aruandluse jaoks finantshaldust ja sisemise aruandluse jaoks kuluarvestust.

**Kuluarvestuse pearaamat**

Kuluarvestuse pearaamat on spetsialiseeritud raamistik, mis määrab, kuidas protsessid, väärtused ja kogused sisestatakse ja esitatakse kuluarvestuses konkreetse ala jaoks. Kuluarvestuse pearaamat määratleb protsessid ja reeglid kulude mõõtmiseks kuluobjektidel. See käsitleb kulukandeid ja haldab dokumente, mis salvestab muudatused väärtustes ja kogustes, mida kulukanded toodavad.

**Kulukirje**

Kulukirjed on pearaamatu kirjetest, kulu eraldamistest ja kulutöölehtedesse sisestatud kulukirjetest andmekonnektorite kaudu üleviimise tulemus.

**Kuluobjekt**

Kuluobjektid on mis tahes tüüpi objekt, millele kulud on eraldatud. Siin on mõned tüüpilised kuluobjektid.

-   Tooted
-   Projektid
-   Ressursid
-   Osakonnad
-   Kulukeskused
-   Geograafilised piirkonnad

Haldus kasutab kuluobjekte, et määrata kulude kogus, kuid samuti selleks, et juhtida tulususe analüüsi.

**Kuluelement**

Kuluelemente kasutatakse funktsioonina, et jälgida ja kategoriseerida, kuhu kulud voolavad. On kahte tüüpi kuluelemente: primaarsed kulud ja sekundaarsed kulud. **Esmased kulud** Esmase kulu elemendid tähistavad kulude voogu finantsaruandlusest kuluarvestusse. Kuluelemendi struktuur vastab pearaamatus kasumi ja kahjumi kontostruktuurile, kus kuluelement võib vastata põhikontole. Mitte kõiki põhikontosid ei pea ärinõuetest sõltuvalt tähistama kuluelementidena. Siin on mõned näited primaarsetest kuluelementidest.

-   Müüdud kaupade kulud
-   Kaudsed materjalikulud
-   Personalikulud
-   Energiakulud

**Teisene kuluelement** 

Sekundaarsed kuluelemendid tähistavad kulude sisevoolu, kuna neid kulusid luuakse ja kasutatakse ainult kuluarvestuses. Sekundaarsed kuluelemendid aitavad tagada, et kulude allikat saab jälgida. Neid kuluelemente kasutatakse kulude eraldamises ja üldkulude arvutustes. Siin on mõned näited sekundaarsetest kuluelementidest.

-   Tootmiskulud
-   Tootmine, materjal ja turustamise üldkulud

**Kulu juhtseade**

Kulude juhtseade tähistab kulustruktuuri. See peab olema seotud kuluobjekti dimensioonidega kuluarvestuse pearaamatus.

**Versioon**

Versioone kasutatakse erinevate väljundite stimuleerimiseks, kuvamiseks ja võrdlemiseks. Vaikimisi kuvatakse kõik tegelikud kulud ühes alusversioonis, mis on tuntud kui *tegelik*. Eelarvete ja arvutuste jaoks saate töötada nii paljude versioonidega kui vaja. Näiteks saate importida eelarve andmed originaalversiooni ja seejärel muuta eelarvet muudetud versioonis. Arvutuste puhul saate luua mitu versiooni. Nendes erinevates versioonides saate seejärel luua arvutused, kasutades erinevaid arvutusreegleid, mis rakendatakse kulueraldamisele.

**Väljavõte**

Väljavõtted on vaated juhtidele, kes vastutavad kulude kontrollimise eest. Väljavõtted on määratletud kulukontrolleriga ja need annavad kiirülevaate tegelikest ja eelarvestatud kuludest ning isegi hälvetest ja kalkulatsiooniversioonidest. Aitamaks tagada, et haldurid vaatavad ainult andmeid, mille eest nad vastutavad, kehtivad väljavõtetes ilmunud andmetele juurdepääsureeglid.

**Andmekonnektor**

Andmeid saab importida kuluarvestusse välissüsteemidest andmekonnektorite kaudu. Näiteks saate importida kontostruktuuridest, dimensioonidest, pearaamatu kirjetest ja eelarve kirjetest. Saate kasutada eelkonfigureeritud andmekonnektoreid või kohandatud konnektoreid, et andmeid importida ja luua andmeühendusi.

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

**Üldkulud**

Üldkulud viitavad ärijuhtimise käimasolevatele kuludele. Need on kulud, mida ei saa siduda otseselt spetsiifiliste äritegevustega. Siin on mõned näited üldkuludest.

-   Raamatupidamistasud
-   Kulum
-   Kindlustus
-   Viivis
-   Õigusabikulud
-   Maksud
-   Kommunaalkulud

**Kulude eraldamine**

Kulude eraldamine on kulude määramise ja eraldamise protsess, mis põhineb üldkulude juurpõhjustel. Eraldate kulusummad ja kogused ühest kuluobjektist ühte või mitmesse teise kuluobjekti. Näiteks kõik asutuse teenuste kulud eraldatakse erinevatele osakondadele, mis kasutavad ühist kontorihoonet.

**Kulude eraldamise poliitika**

Kulude eraldamise poliitika määratleb summad ja kogused, mis tuleb eraldada. Eraldamise reeglid hõlmavad eraldamise allikareegleid, mis määravad eraldatavad kulud, ja eraldamise sihtreegleid, mis määravad, kuhu kulud eraldatakse Näiteks kõik asutuse teenuste kulud on eraldamise allikas, mida saab eraldada erinevatele osakondadele organisatsioonis (see on eraldamise sihtmärkidele).

**Eraldamise alus**

Eraldamise alus on alus, mida saab kasutada selliste tegevuste mõõtmiseks ja hulga määramiseks nagu kasutatud masinatunnid, tarbitud kilovatt-tunnid, kulutatud otsesed tööjõutunnid või hõivatud pind ruutjalgades. Seda kasutatakse kulude eraldamiseks ühele või mitmele kuluobjektile.

**Eraldamispõhimõte**

Üks eraldamise põhimõtteid on eraldada kulu kulumäära alusel. Saate valida kulude eraldamise, kasutades tegeliku perioodi määra või ajaloolist määra. Eraldamine, mis kasutab vastastikust meetodit, aitab tagada, et eraldamise alus määratakse simultaansete võrrandite seeriaga enne, kui eraldamine on tehtud, kasutades tegeliku perioodi määra.

**Kulude koondamine**

Kulude koondamise eesmärk on kaasata kõik antud kuluobjekti kulud. Liitmise tase on kasutaja määratletud. Kulude koondamist kasutades saate liita kulude elemendid, mis tuleb eraldada ühest kuluobjektist teise. Kui kulude koondamist ei kasutata, eraldatakse kulude iga üksik element ühest kuluobjektist teise.

**Kulumäära poliitika**

Kulumäära kasutatakse hinna arvutamiseks kuluobjekti kohta. Hinna elementide mõistmiseks määratlete kulumäära poliitikad. On kahte tüüpi kulumäärasid: ajalooline kulumäär ja plaanitud kulumäär. Ajalooline kulumäär on arvutatud määr, mida kasutatakse kuluobjekti eraldamise aluse jaoks kordistina. Määr arvutatakse eelmise perioodi kulu eraldamiste põhjal. Plaanitud määr on kasutaja määratletud määr.

**Dimensioonihierarhia**

Dimensioonihierarhiaid kasutatakse aruandlusstruktuuridena, kui määratlete reeglid eraldamise, kulumäära ja kulude koondamise ning väljavõtete või andmete Microsoft Excelis kuvamise jaoks, ja määratlete juurdepääsu koondatud andmetele. On kaks dimensioonihierarhiat: kategoriseerimise hierarhia ja klassifikatsiooni hierarhia. Kategoriseerimise hierarhia määratletakse kuluelementide põhjal, samal ajal kui klassifikatsiooni hierarhia määratletakse kuluobjektide põhjal.

**Statistiline dimensioon**

Statistiline dimensioon on objektide arvu või summa avaldis, mida saab kasutada eraldamiste või kulumäära arvutuste alusena. See luuakse käsitsi või imporditakse lähtesüsteemidest. Statistiliste dimensioonide näited hõlmavad töötajate arvu, litsentsitud tarkvara arvu igas seadmes, iga masina energiatarvet või kulukeskuse ruutmeetreid.

**Statistiline kirje**

Statistilised kirjed hoiavad antud statistilise dimensiooni salvestatud summat või loendamisväärtust. Salvestatud summat või loendamisväärtust nimetatakse ka suurusjärguks.




