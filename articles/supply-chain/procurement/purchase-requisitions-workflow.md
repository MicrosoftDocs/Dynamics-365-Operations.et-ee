---
title: ostutaotluse töövoog
description: Töövooprotsess viib ostutaotlused läbi ülevaatusprotsessi algsest olekust Mustand kuni lõplikku olekusse Kinnitatud. Kui ostutaotlus esitatakse ülevaatamiseks, käivitatakse töövoo protsess. Kui ostutaotlus on kinnitatud, saate luua ostutellimuse ostutaotluse ridade jaoks ja selle hankijale tellimuse täitmiseks esitada.
author: RichardLuan
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, WorkflowParticipantExpenToken
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2234
ms.assetid: dad3ba5a-2892-45d2-874a-300896f59b34
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67bad698584c4a49cc5ce82682bb32cd1e32bbd5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215909"
---
# <a name="purchase-requisition-workflow"></a>ostutaotluse töövoog

[!include [banner](../includes/banner.md)]

Töövooprotsess viib ostutaotlused läbi ülevaatusprotsessi algsest olekust Mustand kuni lõplikku olekusse Kinnitatud. Kui ostutaotlus esitatakse ülevaatamiseks, käivitatakse töövoo protsess. Kui ostutaotlus on kinnitatud, saate luua ostutellimuse ostutaotluse ridade jaoks ja selle hankijale tellimuse täitmiseks esitada.

Enne ostutaotluse ülevaatuseks edastamist peate konfigureerima töövoo. Töövooprotsess võib sisaldada üht või mitut ülevaatusetappi mis tahes järjestuses. Töövoo protsessi saab seadistada ka jättes vahele ülesannete ülevaate ja ostutaotluse automaatselt kinnitada. Saate konfigureerida töövoo töötlema ostutaotlust ühe dokumendina või suunata üksikud ostutaotluse read asjakohastele ülevaatajatele. Saate luua ka stsenaariumi, kus ostutaotlus suunatakse ühe dokumendina osadele ülevaatajatele ja valitud ostutaotluste read suunatakse teistele ülevaatajatele.  

Kui ostutaotluse read vaadatakse läbi ükshaaval, tuleb lõpule viia kõigi ostutaotluse ridade ülevaatusprotsess, enne kui töövooprotsess saab liikuda järgmisse etappi ja ostutaotluse ülevaatusprotsessi saab tervikuna lõpule viia. Kui ülevaatusprotsess on ostutaotluse ja kõigi selle ridade puhul lõpule viidud, värskendatakse ostutaotluse üldiseks olekuks **Kinnitatud**.  

Saate töövoo konfigureerida nii, et see esindaks ostutaotluste äriprotsesse teie organisatsioonis. Ostutaotluse töövooprotsessi seadistamisel võtke arvesse järgmisi küsimusi.

-   Millised kulud tuleb üle vaadata?
-   Millised kulud saab automaatselt kinnitada?
-   Kes peab läbi vaatama ja kinnitama kulude taotlused? Milline roll on neile kasutajatele määratud?
-   Millist protsessi tuleb järgida, kui ülevaataja pole saadaval?

Järgmised näited selgitavad kaht viisi ostutaotluse töövoo konfigureerimiseks.

## <a name="example-1-route-a-purchase-requisition-as-a-single-document-for-review"></a>Näide 1: Suuna läbivaatamiseks ostutaotlus ühe dokumendina 
Järgmine illustratsioon näitab, kuidas ostutaotlus saab läbi töövoo läbivaatamise protsessi liikuda ühe dokumendina. Ostutellimuse ridu ei suunata eraldi. Selles näites kuuluvad töövoo protsessi järgmised ülesanded:

-   **Nõude esitaja** – kasutaja, kes taotleb kaupu või teenuseid. Nõude esitaja saab valmistada ette ostutaotluse või teine töötaja saab selle nõude esitaja nimel ette valmistada ostutaotluse. See töötaja on ettevalmistaja. Ettevalmistaja vastutab ostutaotluse ülevaatuse protsessi käigus. Seda saab muuta ainult ostutaotluse ettevalmistaja.

**Märkus.** Töötajale tuleb anda kellegi teise nimel ostutaotluse loomiseks vajalikud õigused. Kasutage nende õiguste seadistamiseks lehte **Ostutaotluse luba**.

-   **Ostuagent** – kasutaja, kes vaatab hanke üle ja saab dokumendi kinnitada.
-   **Nõude esitaja ülemus** – kasutaja, kes teeb juhtiva ülevaatuse ja saab dokumendi kinnitada.

![Ostutaotluse töövoo ülevaatamise protsess](./media/purchreqworkflowoverview_submission.gif)  
Selles näites töövoo protsess ostutaotlusele järgib järgmiseid samme:

1.  Ettevalmistaja esitab ostutaotluse ülevaatamiseks.
2.  Ostuagent saab teatise. Teatisega nõutakse, et ostuagent kontrolliks ostutaotluse teabe õigsust. Kui vajalik teave on puudu, siis saab ostuagent selle lisada või ostutaotluse ettevalmistajale teabe lisamiseks tagastada. Kui kogu vajalik teave on olemas, saab ostutaotlus liikuda ülevaatusprotsessi järgmisse etappi.
3.  Nõude esitaja ülemus vaatab ostutaotluse üle. Ostutaotlus võidakse suunata nõude esitaja ülemusele, kui näiteks ostutaotluse summa ületab nõude esitaja kulutuste piirangu ostutaotluste puhul. Selle nõude esitaja juhataja saate kinnitada või ostutaotluse tagasi lükkamiseks või ettevalmistaja muutmiseks tagastada.

## <a name="example-2-route-the-individual-purchase-requisition-lines-for-review"></a>Näide 2: Suuna üksikud ostutaotluse read ülevaatamisele.
Järgmine joonis selgitab, kuidas saab üksikuid ostutaotluse ridu töövoo kaudu suunata. Üldjuhul on protsess iga rea puhul samasugune kui ühe dokumendina ülevaadatava ostutaotluse protsess. Siiski peab iga rida eraldi läbima töövooprotsessi, enne kui töövoo saab kogu ostutaotluse puhul lõpule viia.  

Selles näites sisestab töötaja taotluse plakatite ja t-särkide turunduskampaania jaoks. Plakatite kulu jaotatakse turunduse- ja müügiosakonna vahel. Kui plakatite või t-särkide kulu ületab osakonnajuhatajate allkirjastamise piirmäära, siis peab ostutaotluse üle vaatama ka grupi haldur.  

Selles näites kuuluvad töövoo protsessi järgmised ülesanded:

-   **Nõude esitaja** – kasutaja, kes taotleb kaupu või teenuseid. Nõude esitaja saab valmistada ette ostutaotluse või teine töötaja saab selle nõude esitaja nimel ette valmistada ostutaotluse. See töötaja on ettevalmistaja. Ettevalmistaja vastutab ostutaotluse ülevaatuse protsessi käigus. Seda saab muuta ainult ostutaotluse ettevalmistaja.

**Märkus.** Töötajale tuleb anda kellegi teise nimel ostutaotluse loomiseks vajalikud õigused. Kasutage nende õiguste seadistamiseks lehte **Ostutaotluse luba**.

-   **Ostuagent** – kasutaja, kes vaatab hanke üle ja saab dokumendi kinnitada.
-   **Nõude esitaja ülemus** – kasutaja, kes teeb juhtiva ülevaatuse ja saab dokumendi kinnitada.
-   **Osakonnajuhataja** – kasutaja, kes vaatab kulu üle ja saab dokumendi kinnitada.
-   **Grupihaldur**– kasutaja, kes teeb allkirjahalduri ülevaatuse ja saab dokumendi kinnitada.

![Ostutaotluse rea töövoo ülevaatamise protsess](./media/purchreqlineworkflowoverview.gif)  
Selles näites töövoo protsess ostutaotluse ridadele järgib järgmiseid samme:

1.  Ettevalmistaja esitab ostutaotluse ülevaatamiseks. Iga rida suunatakse ülevaatajale, kes on konfigureeritud seda töövooprotsessis vastu võtma.
2.  Ostuagent saab teatise. Teates nõutakse, et ostuagent kontrolliks ostutaotlusel ja ostutaotluse ridadel oleva teabe õigsust. Kui ostuagent avab ostutaotluse, on näha kõik read, kuid visuaalne näidik näitab, millised read on saadetud ostuagendile ülevaatamiseks. Kui vajalik teave on puudu, siis saab ostuagent selle lisada või ostutaotluse rea ettevalmistajale teabe lisamiseks tagastada. Kui kogu vajalik teave on olemas, saab ostutaotluse rida liikuda ülevaatusprotsessi järgmisse etappi. Ostutaotluse read saavad ülevaatuse protsessi läbida üksteisest sõltumatult.
3.  Nõude esitaja rea haldur vaatab üle ja kiidab heaks ostutaotluse read. Kinnitus võidakse suunata nõude esitaja ülemusele, kui näiteks ostutaotluse real olev summa ületab nõude esitaja kulutuste piirangu ostutaotluste ridade puhul. Haldur saab kinnitada või tagasi lükata ühe või mõlemad ostutaotluse read.
4.  Osakonnajuhataja turundusosakonnas vaatab üle ostutaotluse read nii plakatite kui ka t-särkide kohta. Müügiosakonna juhataja vaatab üle ostutaotluse rea ainult plakatite jaoks, sest see on ainuke kulu, mis on kantud müügiosakonnale.
5.  Grupihaldur vaatab üle ja kinnitab ostutaotluse rea t-särkide kohta ainult siis, kui grupihalduri kinnitus on nõutav, näiteks kui ostutaotluse real olev summa ületab osakonnajuhataja kinnituspiirangu. Grupihaldur ei pea kinnitama ostutaotluse rida plakatitele.

> [!NOTE]
> Süsteemi valuuta peab olema seatud, kui ostutaotluse päise töövoo jaoks on vaja allkirjastamise piirangutega seotud kinnitusi.

## <a name="configuring-a-workflow-for-purchase-requisitions"></a>Ostutaotluste töövoo konfigureerimine
Ostutaotluse suunamiseks ülevaatamiseks, konfigureerige ostutaotluse töövoo protsessid. Määratud töövoo konfiguratsioon juhib suhtlust kaupade taotleja (nõude esitaja) ja ülevaataja ning töövoo kinnitaja vahel. Ostutaotluse suunamine sõltub töövoo konfiguratsioonis määratletud tingimustest. Näiteks määravad need tingimused, millal tuleks ostutaotlus suunata, millisele kasutajale või rollile see tuleks suunata ja milliseid tegevusi saavad kasutajad teha.  

Selles teemas olevad näited selgitavad, kuidas saab ostutaotluse suunata töövoo kaudu üksiku dokumendina või üksikute ostutaotluse ridadena. Samuti saate konfigureerida ostutaotluste jaoks töövoo, mis kajastab teie organisatsiooni jaoks määratletud ostutaotluste sisemist kontrolliülevaatust.  

Osalejad või ülevaatajad, kellele on töövoos ülesanne määratud, saavad olla konkreetse kasutajagrupi liikmed, kindla turberolliga kasutajad, juhtimishierarhias edastajaga seostatud kasutajad, nimetatud kasutajad või teatud kulukohustustega kasutajad.

### <a name="purchase-requisition-expenditure-reviewers"></a>Ostutaotluse kulu läbivaatajad

Kulude ülevaataja konfiguratsioonid võimaldavad teil kulusid ülevaatamiseks dünaamiliselt suunata kasutaja põhjal, kes on määratud projektirollile või finantsdimensioonile, kus kulu tekib. Töövooprotsess kasutab määratud projektirolli või finantsdimensiooni omanikku määramaks, kellele tuleb kulu suunata.  

Saate määratleda ühe või mitu kulude ülevaataja konfiguratsiooni ja seejärel valida töövoo loomisel konfiguratsiooni. Saate konfigureerida kulude ülevaataja väärtused igale organisatsiooni juriidilise isikule. Pärast kulude ülevaataja konfiguratsioonide määratlemist saate määrata oma töövooülesandele konfiguratsiooni.  

Te ei pea kulude ülevaataja konfiguratsioone määratlema. Selle asemel saate töövoo määratlemisel määrata ülevaatajatena konkreetsed kasutajad või kasutajagrupid. Kui teil on keeruline organisatsioon, võivad kulude ülevaatajad aga suurendada kinnitamisprotsessi tõhusust. Samuti kui seadistate kulude ülevaatajad, ei pea te värskendama töövoo ülevaatajate määranguid iga kord, kui mõni ülevaataja muudab töörolle.  

Saate seadistada kulude ülevaatajad lehel **Ostutaotluse kulude ülevaatajad**. Looge kulude ülevaataja konfiguratsioon ja sisestage väärtused igale oma organisatsiooni juriidilisele isikule. Projektile määratavate taotluste puhul saate määrata rolli, kes vastab taotluste ülevaatamise eest: projektijuht, projekti revident või projekti müügijuht. Kulud suunatakse kasutajale, kes on sellele rollile määratud. Saate kulu suunata ka finantsdimensiooni omanikule, valides vastava finantsdimensiooni suvandi vahekaardil **Organisatsiooni jaotused**.  

Töövoos seadistatud kulu ülevaataja kasutamiseks peate asjakohase töövooelemendi välja **Määramine** atribuutides valima suvandi **Osaleja tüüp** sätteks **Kulu osalejad**.

<a name="additional-resources"></a>Lisaressursid
--------

[Tarbimistaotluse loomine](tasks/create-requisition-consumption.md)

[Äriprotsessi töövoogude määratlemine ostutaotluste jaoks](https://www.microsoft.com/download/details.aspx?id=101821)

[Hangete töövood](procurement-sourcing-workflows.md)

[Ostutaotluste ülevaade](purchase-requisitions-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]