---
title: Hankija maksete loomine maksesoovituse abil
description: "See teema annab ülevaate maksesoovituse valikutest ja sisaldab mõningaid näiteid selle kohta, kuidas maksesoovitused toimivad. Maksesoovitusi kasutatakse sageli hankija maksete loomiseks, kuna maksesoovituse päringu abil saab hankija arveid kiiresti kriteeriumide (nt tähtaeg ja skonto) alusel maksmiseks valida."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14312
ms.assetid: 585d5b0b-1b79-4a03-ab18-528918070377
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: b46037b9509f329e18f0da69d530f6b1f88c8888
ms.lasthandoff: 03/31/2017


---

# <a name="create-vendor-payments-by-using-a-payment-proposal"></a>Hankija maksete loomine maksesoovituse abil

See teema annab ülevaate maksesoovituse valikutest ja sisaldab mõningaid näiteid selle kohta, kuidas maksesoovitused toimivad. Maksesoovitusi kasutatakse sageli hankija maksete loomiseks, kuna maksesoovituse päringu abil saab hankija arveid kiiresti kriteeriumide (nt tähtaeg ja skonto) alusel maksmiseks valida. 

Organisatsioonid kasutavad hankija maksete loomiseks sageli maksesoovitusi, kuna maksesoovituse päringu abil saab hankija arveid kiiresti tähtaja, skonto või muu kriteeriumi alusel maksmiseks valida. 

Maksesoovituse päring sisaldab mitmeid vahekaarte, millest igaühel on erinevad võimalused makstavate arvete valimiseks. Selle **parameeter** vahekaart sisaldab organisatsiooni vastu enim kasutatavad suvandid. Kohta ning **kaasamiseks** FastTab, saate määrata, millised arved või hankijate hulka makse määratledes erinevate näitajate vahemikud. Näiteks kui soovite maksta ainult teatud hulga müüjad, saate määratleda filtri hankija vahemiku. Seda funktsiooni kasutatakse sageli arvete konkreetse makseviisi valimiseks. Näiteks kui määratlete filtri kui **makseviisi** = **kontrollida**, ainult arved, et makseviisi valitakse maksetaotluste alusel, tingimusel, et need vastavad ka muud päringus määratud kriteeriumidele. Vahekaart **Täpsemad parameetrid** sisaldab lisavalikuid, millest kõik ei pruugi olla teie organisatsioonile vajalikud. Näiteks sisaldab see vahekaart tsentraliseeritud maksete arvete maksmise suvandeid.

## <a name="parameters"></a>Parameetrid
-   **Valige arvete** – arved määratud kuupäevavahemikku jäävate ning **alates** ja **siiani** välja poolt tähtaja, allahindluse kuupäeva või mõlema. Skonto kuupäev kasutamisel otsib süsteem esmalt arved, skonto kuupäeva vahel on alates ja kuni kuupäevad. Seejärel määratleb süsteem seansi kuupäeva kasutades, kas arve on skonto saamiseks sobilik ning ega skonto kuupäev juba möödunud ole.
-   **Alguskuupäevast**** lõppkuupäevani** – maksmiseks valitakse arved, mille tähtaeg või skonto kuupäev jääb sellesse kuupäevavahemikku.
-   **Maksekuupäev** – kui kuupäev on määratletud, luuakse kõik maksed sellel kuupäeval. Välja **Varaseim maksekuupäev** ignoreeritakse.
-   **Varaseim maksekuupäev** – sisestage varaseim maksekuupäev. Näiteks on **alates** ja **seni** väljade Määrake vahemik 1. septembrist kuni September 10 ja minimaalne makse kuupäev on 5. September. Sel juhul on makse tähtajaks, 5. September tähtaeg: 1. September – 5. September kõik arved. Tähtaeg: 5. September – 10. September kõik arved on siiski makse kuupäev, mis on võrdne iga arve maksetähtaeg.
-   **Summa limiit** – sisestage kõikide maksete suurim kogusumma.
-   **Luua makseid ilma arve eelvaade** – kui see valik on seatud **Jah**, maksete luuakse kohe selle **hankijamaksete** lehel. Selle **maksesoovituse** lehe jäetakse vahele. Seetõttu luuakse maksed kiiremini. Makseid saab endiselt muuta lehel **Hankija maksed**. Teise võimalusena saate nuppu **Valitud makse arvete redigeerimine** kasutades naasta lehele **Maksesoovitus**.

## <a name="advanced-options"></a>Täpsemad suvandid
-   **Hankija saldo kontrollimine** – kui määrate suvandi **Jah**, kontrollib süsteem enne mistahes arve maksmist hankija deebetsaldo olemasolu. Kui hankija on deebetsaldo, luuakse makset. Näiteks, on hankija kreeditarvete või makseid, mis on konteeritud, kuid ei ole veel tasutud. Neil juhtudel ei tuleks hankijale maksta. Selle asemel tuleks kreeditarved ja maksed tasakaalustada tasumata arvetega.
-   **Kustuta negatiivsed maksed** – valik toimib erinevalt üksikute arvete ja maksekriteeriumile vastavate arvete summa maksmise puhul. Käitumine on määratletud makseviisiga.
-   **Makse iga arve jaoks** – kui valiku **Kustuta negatiivsed maksed** suvandi väärtuseks on määratud **Jah** ning hankijal on olemas tasakaalustamata arve ja makse, valitakse maksmiseks ainult arve. Olemasolevat makset ei tasakaalustata arvega. Kui valiku **Kustuta negatiivsed maksed** suvandi väärtuseks on määratud **Ei** ning arve ja makse pole tasakaalustatud, valitakse maksmiseks nii arve kui makse. Maksele luuakse makse ja tagasimakse (negatiivne makse).
-   **Makse arvete summa jaoks** – kui valiku **Kustuta negatiivsed maksed** suvandi väärtuseks on määratud **Jah** ning hankijal on tasakaalustamata arve ja makse, valitakse maksmiseks nii tasakaalustamata arve kui ka makse ning nende summade liitmisel saadakse makse kogusumma. Erand tehakse ainult siis, kui summa tulemuseks on tagasimakse. Sellisel juhul ei valita ei arvet ega makset. Kui selle ** Kustuta negatiivsed maksed ** määrangu **nr**, ning arve ja tasumist ei ole tasakaalustatud, arve ja makse valikul makse ja summad lisatakse koos esitada arve kogusumma.
-   **Prindi ainult aruanne** – kui soovite maksesoovituse tulemuste aruannet vaadata ilma makseid loomata, seadke selle suvandi väärtuseks **Jah**.
-   **Lisa hankija arve teistelt juriidilistelt isikutelt** – kui teie organisatsioonil on tsentraliseeritud makseprotsess ja maksesoovitus peaks sisaldama arveid teistelt otsingukriteeriumisse kaasatud juriidilistelt isikutelt, määrake suvandi väärtuseks **Jah**.
-   **Soovita iga juriidilise isiku jaoks eraldi hankija makset** – kui suvandi väärtuseks on määratud **Jah**, luuakse eraldi makse igale juriidilisele isikule hankija kohta. Maksel olev hankija on iga juriidilise isiku arvel olev hankija. Kui suvandi väärtuseks on määratud **Ei** ja samal hankijal on arveid mitmete juriidiliste isikute juures, luuakse üks makse valitud arvete kogusummas. Maksel olev hankija on antud juriidilise isiku hankija. Kui antud juriidilisel isikul hankija konto puudub, kasutatakse esimese tasutava arve hankija kontot.
-   **Makse valuuta** – see väli määrab kõigi maksete loodud valuuta. Kui valuuta ei ole määratletud, iga arve tasuda arve valuutat.
-   **Makse nädalapäev** – saate sisestada makse tegemise nädalapäeva. Seda välja kasutatakse ainult siis, kui makseviisiks on seatud arvete kogusumma makse jaoks kindlal nädalapäeval.
-   **Vastaskonto tüüp** ja **vastaskonto** – nende väljade määratleda kindlat tüüpi kontole (näiteks **pearaamatu** või **panga**) ja Vastaskonto (nt eraldi pangakonto). Arve maksmise meetod määratleb vaikimisi vastaskonto tüübi ja vastaskonto, kuid nende väljade abil saate alistada vaikeväärtused.
-   **F3** -edasi on **kaasamiseks** FastTab, saate määratleda kriteeriumid täiendavad vahemikud. Näiteks kui soovite maksta ainult hankijakoodide vahemiku, saate määratleda filtri hankija vahemiku. Seda funktsiooni kasutatakse sageli arvete konkreetse makseviisi valimiseks. Näiteks kui määratlete filtri kui **makseviisi** = **kontrollida**, ainult arved, et makseviisi valitakse maksetaotluste alusel, tingimusel, et need vastavad ka muud päringus määratud kriteeriumidele.

## <a name="scenarios"></a>Stsenaariumid
| Hankija | Arve | Arve kuupäev | Arve summa | Tähtaeg | Skonto kuupäev | Skonto summa |
|--------|---------|--------------|----------------|----------|--------------------|----------------------|
| 3050   | 1001    | 15. juuni      | 500,00         | 15. juuli  | 29. juuni            | 10,00                |
| 3050   | 1002    | 20. juuni      | 600,00         | 20. juuli  | 4. juuli             | 12,00                |
| 3075   | 1003    | 15. juuni      | 250,00         | 29. juuni  |                    | 0,00                 |
| 3100   | 1004    | 17. juuni      | 100,00         | 17. juuli  | 1. juuli             | 1,00                 |

April maksab hankijatele 1. juulil. Ta kasutab ülesande tõhusamaks täitmiseks maksesoovitust.

### <a name="option-1-by-cash-discount"></a>1. võimalus: skonto järgi

April valib soovituse tüübiks **Skonto**. Ta siseneb on kuupäev vahemikus, juuni 26-juuli 10. Ettepanek on kaasatud järgmised arved:

-   1002, kuna skonto kuupäev, 4. juuli, jääb maksekuupäevade vahemikku;
-   1004, kuna skonto kuupäev, 1. juuli, jääb maksekuupäevade vahemikku.

Soovitusse ei kaasata järgmisi arveid:

-   1001, kuna skonto kuupäev, 29. juuni, on juba möödunud, seega ei ole arve enam skontoks sobilik;
-   1003, kuna arvel ei ole skonto kuupäeva.

### <a name="option-2-by-due-date"></a>2. võimalus: tähtaja järgi

April valib soovituse tüübiks **Tähtaja järgi**. Ta siseneb on kuupäev vahemikus, juuni 26-juuli 10. Ettepanek on kaasatud järgmised arved:

-   1003, kuna tähtaeg, 29. juuni, jääb maksekuupäevade vahemikku.

Soovitusse ei kaasata järgmisi arveid:

-   1001, kuna tähtaeg, 15. juuli, jääb maksekuupäevade vahemikust välja;
-   1002, kuna tähtaeg, 20. juuli, jääb maksekuupäevade vahemikust välja;
-   1004, kuna tähtaeg, 17. juuli, jääb maksekuupäevade vahemikust välja.

### <a name="option-3-by-due-date-and-cash-discount"></a>3. võimalus: tähtaja ja skonto järgi

April valib soovituse tüübiks **Tähtaeg ja skonto**. Ta siseneb on kuupäev vahemikus, juuni 26-juuli 10. Ettepanek on kaasatud järgmised arved:

-   1003, kuna tähtaeg, 29. juuni, jääb maksekuupäevade vahemikku.
-   1002, kuna skonto kuupäev, 4. juuli, jääb maksekuupäevade vahemikku;
-   1004, kuna skonto kuupäev, 1. juuli, jääb maksekuupäevade vahemikku.

Soovitusse ei kaasata järgmisi arveid:

-   1001, kuna skonto kuupäev, 29. juuni, on juba möödunud, seega arve ei ole enam skontoks sobilik, ning tähtaeg, 15. juuli, jääb kuupäevavahemikust välja.

## <a name="country-specific-considerations"></a>Riigi-/regioonikohased kaalutlused
### <a name="norway"></a>Norra

#### <a name="dimension-control"></a>Dimensiooni juhtimine

Dimensioonide juhtimine võimaldab teil juhtida loodud ridade rühmitamist maksesoovituse alusel ja määrata vaikedimensioone, võttes aluseks rakendatud arvete jaoks kasutatud finantsdimensioonid. Norra riigi kontekstis on iga makseviisi all finantsdimensiooni vahekaart, kus saate dimensiooni juhtimise aktiveerida ning lubada ka iga dimensiooni puhul rühmitamise. Võimalikud on järgmised valikud.

-   Väli **Dimensiooni juhtimine** keelatakse. Maksesoovitus käitub nagu mis tahes muu riigi puhul.
-   Väli **Dimensiooni juhtimine** aktiveeritakse ilma dimensioone täpsemalt määratlemata. Maksesoovitus luuakse ilma dimensioone arvesse võtmata. Loodud kanne ei päri rakendatud kirjest ühtki dimensiooni.
-   Väli **Dimensiooni juhtimine** aktiveeritakse ja dimensioonide täpsem määratlemine lubatakse. Nüüd saate määratleda, kuidas dimensioonid töölehele kopeeritakse. Näiteks: Saabuva kõne märguanne on **äriüksusega** ruut Maksesoovituse loomine iga äriüksuse jaoks makse, Saabuva kõne märguanne on **CostCenter** ruut Maksesoovituse loomine kulukeskuse kohta meetodi makse

**Märkus.** Kui valite kolmandas võimaluses rohkem kui ühe dimensiooni, luuakse maksesoovitus dimensiooni kombinatsioonile.

#### <a name="bank-account-selection"></a>Pangakonto valimine

Saate määratleda standardse debiteerimise maksekonto makseviisi kohta sõltumata riigikontekstist. See määratakse soovituse loodud makseridadel. Pangakonto funktsiooniga saate määratleda mitu dimensiooni ja valuutaga hallatavat debiteerimise pangakontot või nende kombinatsiooni, et kasutada erinevaid debiteerimise pangakontosid olenevalt kombinatsioonist. Seadistage need kombinatsioonid **makseviiside** lehe abil selle **panga** nupp koos iga makseviisi jaoks saadaval **konto sisestamistüüp** = **panga**.


