---
title: Hankija maksete loomine maksesoovituse abil
description: See teema annab ülevaate maksesoovituse valikutest ja sisaldab mõningaid näiteid selle kohta, kuidas maksesoovitused toimivad.
author: abruer
ms.date: 04/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14312
ms.assetid: 585d5b0b-1b79-4a03-ab18-528918070377
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 71e87b1102e21e035c25af4c63245eaaa59e4babb82bcf59c5cfba48f7d114f3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749048"
---
# <a name="create-vendor-payments-by-using-a-payment-proposal"></a>Hankija maksete loomine maksesoovituse abil

[!include [banner](../includes/banner.md)]

See teema annab ülevaate maksesoovituse valikutest ja sisaldab mõningaid näiteid selle kohta, kuidas maksesoovitused toimivad. Maksesoovitusi kasutatakse sageli hankija maksete loomiseks, kuna maksesoovituse päringu abil saab hankija arveid kiiresti kriteeriumide (nt tähtaeg ja skonto) alusel maksmiseks valida. 

Organisatsioonid kasutavad hankija maksete loomiseks sageli maksesoovitusi, kuna maksesoovituse päringu abil saab hankija arveid kiiresti tähtaja, skonto või muu kriteeriumi alusel maksmiseks valida. 

Maksesoovituse päring sisaldab mitmeid vahekaarte, millest igaühel on erinevad võimalused makstavate arvete valimiseks. Vahekaart **Parameeter** sisaldab valikuid, mida suurem osa organisatsioonist kõige sagedamini kasutab. Kiirkaardil **Kaasatavad kirjed** saate määrata, millised arved või hankijad tuleb maksesse kaasata, määratledes erinevate näitajate vahemikud. Näiteks kui soovite maksta ainult teatud hankijatele, saate määratleda nende hankijate jaoks filtri. Seda funktsiooni kasutatakse sageli kindla maksemeetodi jaoks arvete valimiseks. Näiteks kui määratlete filtri, kus **Makseviis** = **Tšekk**, valitakse makseks ainult selle makseviisiga arved, eeldusel, et need vastavad ka teistele päringus määratud kriteeriumidele. Vahekaart **Täpsemad parameetrid** sisaldab lisavalikuid, millest kõik ei pruugi olla teie organisatsioonile vajalikud. Näiteks sisaldab see vahekaart tsentraliseeritud maksete arvete maksmise suvandeid.

## <a name="parameters"></a>Parameetrid
-   **Arvete valimise alus** – väljadega **Alguskuupäev** ja **Lõppkuupäev** määratud kuupäevavahemikku jäävaid arveid saab valida tähtaja, skonto kuupäeva või mõlema alusel. Kui kasutate skonto kuupäeva, otsib süsteem esmalt arveid, mille skonto kuupäev jääb algus- ja lõppkuupäeva vahele. Seejärel määratleb süsteem seansi kuupäeva kasutades, kas arve on skonto saamiseks sobilik ning ega skonto kuupäev juba möödunud ole.
-   **Alguskuupäevast** **lõppkuupäevani** – maksmiseks valitakse arved, mille tähtaeg või skonto kuupäev jääb sellesse kuupäevavahemikku.
-   **Varaseim maksekuupäev** – sisestage varaseim maksekuupäev. Näiteks määravad väljad **Alguskuupäev** ja **Lõppkuupäev** ajavahemiku 1. septembrist 10. septembrini ning minimaalne maksekuupäev on 5. september. Sellisel juhul on kõigil maksetel tähtajaga 1.–5. september maksekuupäevaks 5. september. Arvetel tähtajaga 5.–10. september on aga maksekuupäevaks iga arve tähtaja kuupäev.
-   **Summa limiit** – sisestage kõikide maksete suurim kogusumma.
-   **Maksete loomine ilma arve eelvaateta** – kui selle suvandi sätteks on valitud **Jah**, luuakse maksed kohe lehel **Hankija maksed**. Leht **Maksesoovitus** jäetakse vahele. Seetõttu luuakse maksed kiiremini. Makseid saab endiselt muuta lehel **Hankija maksed**. Teise võimalusena saate nuppu **Valitud makse arvete redigeerimine** kasutades naasta lehele **Maksesoovitus**.

## <a name="advanced-options"></a>Täpsemad suvandid
- **Hankija saldo kontrollimine** – kui määrate suvandi **Jah**, kontrollib süsteem enne mistahes arve maksmist hankija deebetsaldo olemasolu. Kui hankijal on deebetsaldo, siis makset ei looda. Näiteks võib hankijal olla kreeditarveid või makseid, mis on küll sisestatud, kuid pole veel tasakaalustatud. Neil juhtudel ei tuleks hankijale maksta. Selle asemel tuleks kreeditarved ja maksed tasakaalustada tasumata arvetega.
- **Kustuta negatiivsed maksed** – valik toimib erinevalt üksikute arvete ja maksekriteeriumile vastavate arvete summa maksmise puhul. Käitumine on määratletud makseviisiga.
- **Makse iga arve jaoks** – kui valiku **Kustuta negatiivsed maksed** suvandi väärtuseks on määratud **Jah** ning hankijal on olemas tasakaalustamata arve ja makse, valitakse maksmiseks ainult arve. Olemasolevat makset ei tasakaalustata arvega. Kui valiku **Kustuta negatiivsed maksed** suvandi väärtuseks on määratud **Ei** ning arve ja makse pole tasakaalustatud, valitakse maksmiseks nii arve kui makse. Maksele luuakse makse ja tagasimakse (negatiivne makse).
- **Makse arvete summa jaoks** – kui valiku **Kustuta negatiivsed maksed** suvandi väärtuseks on määratud **Jah** ning hankijal on tasakaalustamata arve ja makse, valitakse maksmiseks nii tasakaalustamata arve kui ka makse ning nende summade liitmisel saadakse makse kogusumma. Erand tehakse ainult siis, kui summa tulemuseks on tagasimakse. Sellisel juhul ei valita ei arvet ega makset. Kui valiku **Kustuta negatiivsed maksed** suvandi väärtuseks on määratud **Ei** ning arvet ja makset ei tasakaalustata, valitakse maksmiseks nii arve kui ka makse ning nende summade liitmisel saadakse makse kogusumma.
- **Prindi ainult aruanne** – kui soovite maksesoovituse tulemuste aruannet vaadata ilma makseid loomata, seadke selle suvandi väärtuseks **Jah**.
- **Lisa hankija arve teistelt juriidilistelt isikutelt** – kui teie organisatsioonil on tsentraliseeritud makseprotsess ja maksesoovitus peaks sisaldama arveid teistelt otsingukriteeriumisse kaasatud juriidilistelt isikutelt, määrake suvandi väärtuseks **Jah**.
- **Soovita iga juriidilise isiku jaoks eraldi hankija makset** – kui suvandi väärtuseks on määratud **Jah**, luuakse eraldi makse igale juriidilisele isikule hankija kohta. Maksel olev hankija on iga juriidilise isiku arvel olev hankija. Kui suvandi väärtuseks on määratud **Ei** ja samal hankijal on arveid mitmete juriidiliste isikute juures, luuakse üks makse valitud arvete kogusummas. Maksel olev hankija on antud juriidilise isiku hankija. Kui antud juriidilisel isikul hankija konto puudub, kasutatakse esimese tasutava arve hankija kontot.
- **Makse valuuta** – see väli määrab valuuta, milles kõik maksed luuakse. Kui valuuta pole määratletud, tasutakse iga arve selle valuutas.
- **Makse nädalapäev** – saate sisestada makse tegemise nädalapäeva. Seda välja kasutatakse ainult siis, kui makseviisiks on seatud arvete kogusumma makse jaoks kindlal nädalapäeval.
- **Vastaskonto tüüp** ja **Vastaskonto** – nende väljadega saate määratleda kindla kontotüübi (nt **Pearaamat** või **Pank**) ja vastaskonto (nt kindel pangakonto). See arve makseviis määratleb vastaskonto vaiketüübi ja vastaskonto, kuid saate nende väljade abil ka alistada vaikeväärtused.
- **Maksekuupäeva kokkuvõte** – seda kasutatakse ainult siis, kui välja **Periood** väärtus makseviisis on **Kokku**. Kuupäev on määratletud, luuakse kõik maksed sellel kuupäeval. Välja **Varaseim maksekuupäev** ignoreeritakse.
- **Lisafiltrid** – kiirkaardil **Kaasatavad kirjed** saate määratleda täiendavad kriteeriumivahemikud. Näiteks kui soovite maksta ainult teatud hankijatele, saate määratleda nende hankijate jaoks filtri. Seda funktsiooni kasutatakse sageli kindla maksemeetodi jaoks arvete valimiseks. Näiteks kui määratlete filtri, kus **Makseviis** = **Tšekk**, valitakse makseks ainult selle makseviisiga arved, eeldusel, et need vastavad ka teistele päringus määratud kriteeriumidele.

## <a name="scenarios"></a>Stsenaariumid

| Hankija | Arve | Arve kuupäev | Arve summa | Tähtaeg | Skonto kuupäev | Skonto summa |
|--------|---------|--------------|----------------|----------|--------------------|----------------------|
| 3050   | 1001    | 15. juuni      | 500,00         | 15. juuli  | 29. juuni            | 10,00                |
| 3050   | 1002    | 20. juuni      | 600,00         | 20. juuli  | 4. juuli             | 12,00                |
| 3075   | 1003    | 15. juuni      | 250,00         | 29. juuni  |                    | 0,00                 |
| 3100   | 1004    | 17. juuni      | 100,00         | 17. juuli  | 1. juuli             | 1,00                 |

April maksab hankijatele 1. juulil. Ta kasutab ülesande tõhusamaks täitmiseks maksesoovitust.

### <a name="option-1-by-cash-discount"></a>1. võimalus: skonto järgi

April valib soovituse tüübiks **Skonto**. Ta sisestab kuupäevavahemiku 26. juuni kuni 10. juuli. Soovitusse kaasatakse järgmised arved.

-   1002, kuna skonto kuupäev, 4. juuli, jääb maksekuupäevade vahemikku;
-   1004, kuna skonto kuupäev, 1. juuli, jääb maksekuupäevade vahemikku.

Soovitusse ei kaasata järgmisi arveid:

-   1001, kuna skonto kuupäev 29. juuni on juba möödunud, seega ei ole see arve enam skonto jaoks sobilik;
-   1003, kuna arvel ei ole skonto kuupäeva.

### <a name="option-2-by-due-date"></a>2. võimalus: tähtaja järgi

April valib soovituse tüübiks **Tähtaja järgi**. Ta sisestab kuupäevavahemiku 26. juuni kuni 10. juuli. Soovitusse kaasatakse järgmised arved.

-   1003, kuna tähtaeg, 29. juuni, jääb maksekuupäevade vahemikku.

Soovitusse ei kaasata järgmisi arveid:

-   1001, kuna tähtaeg, 15. juuli, jääb maksekuupäevade vahemikust välja;
-   1002, kuna tähtaeg, 20. juuli, jääb maksekuupäevade vahemikust välja;
-   1004, kuna tähtaeg, 17. juuli, jääb maksekuupäevade vahemikust välja.

### <a name="option-3-by-due-date-and-cash-discount"></a>3. võimalus: tähtaja ja skonto järgi

April valib soovituse tüübiks **Tähtaeg ja skonto**. Ta sisestab kuupäevavahemiku 26. juuni kuni 10. juuli. Soovitusse kaasatakse järgmised arved.

-   1003, kuna tähtaeg, 29. juuni, jääb maksekuupäevade vahemikku.
-   1002, kuna skonto kuupäev, 4. juuli, jääb maksekuupäevade vahemikku;
-   1004, kuna skonto kuupäev, 1. juuli, jääb maksekuupäevade vahemikku.

Soovitusse ei kaasata järgmisi arveid:

-   1001, kuna skonto kuupäev 29. juuni on juba möödunud, seega ei ole see arve enam skonto jaoks sobilik, ning tähtaeg 15. juuli jääb kuupäevavahemikust välja.

## <a name="country-specific-considerations"></a>Riigi-/regioonikohased kaalutlused
### <a name="norway"></a>Norra

#### <a name="dimension-control"></a>Dimensiooni juhtimine

Dimensioonide juhtimine võimaldab teil juhtida loodud ridade rühmitamist maksesoovituse alusel ja määrata vaikedimensioone, võttes aluseks rakendatud arvete jaoks kasutatud finantsdimensioonid. Norra riigi kontekstis on iga makseviisi all finantsdimensiooni vahekaart, kus saate aktiveerida dimensiooni juhtimise ning lubada iga dimensiooni puhul rühmitamise. Võimalikud on järgmised valikud.

-   Väli **Dimensiooni juhtimine** keelatakse. Maksesoovitus käitub nagu mis tahes muu riigi puhul.
-   Väli **Dimensiooni juhtimine** aktiveeritakse ilma dimensioone täpsemalt määratlemata. Maksesoovitus luuakse ilma dimensioone arvesse võtmata. Loodud kanne ei päri rakendatud kirjest ühtki dimensiooni.
-   Väli **Dimensiooni juhtimine** aktiveeritakse ja dimensioonide täpsem määratlemine lubatakse. Nüüd saate määratleda, kuidas dimensioonid töölehele kopeeritakse. Näide. • Märkige ruut **Äriüksus**, et luua makseviisi puhul maksepakkumine äriüksuse kohta • Märkige ruut **Kulukeskus**, et luua makseviisi puhul maksepakkumine kulukeskuse kohta

> [[!NOTE]
> Kui valite kolmandas võimaluses rohkem kui ühe dimensiooni, luuakse maksesoovitus dimensiooni kombinatsioonile.

#### <a name="bank-account-selection"></a>Pangakonto valimine

Saate määratleda standardse debiteerimise maksekonto makseviisi kohta sõltumata riigikontekstist. See määratakse soovituse loodud makseridadel. Pangakonto funktsiooniga saate määratleda mitu dimensiooni ja valuutaga hallatavat debiteerimise pangakontot või nende kombinatsiooni, et kasutada erinevaid debiteerimise pangakontosid olenevalt kombinatsioonist. Saate seadistada need kombinatsioonid lehel **Makseviisid**, kasutades nuppu **Pangakontod**, mis on saadaval iga makseviisi puhul, mille **Sisestuskonto tüüp** = **Pank**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]