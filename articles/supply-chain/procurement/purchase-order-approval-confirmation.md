---
title: Ostutellimuste kinnitamine
description: Selles teemas kirjeldatakse olekuid, mille ostutellimus pärast loomist läbib, ja muudatuste halduse lubamise mõju ostutellimustele.
author: RichardLuan
manager: tfehr
ms.date: 04/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchOrderInReview, PurchOrderApproved, PurchOrderInDraft, PurchOrderAssignedToMe, VendPurchOrderJournalListPage, PurchTableWorkflowDropDialog, VendPurchOrderJournal
audience: Application User
ms.reviewer: kamaybac
ms.custom: 93143
ms.assetid: cd12a944-c52c-4579-a301-7abe1d237c72
ms.search.region: Global
ms.search.industry: ''
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eafce0be07ae21e5bc2db2cf5bb694a9d71a6269
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018441"
---
# <a name="approve-and-confirm-purchase-orders"></a>Ostutellimuste kinnitamine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse olekuid, mille ostutellimus pärast loomist läbib, ja muudatuste halduse lubamise mõju ostutellimustele.

Pärast ostutellimuse koostamist võib olla vaja läbida heakskiitmise protsess. Kui hankija on tellimusega nõustunud, määratakse ostutellimuse olekuks **Kinnitatud**.

## <a name="approval-of-purchase-orders"></a>Ostutellimuste heakskiitmine
Ostutellimustel, mille puhul muudatuste haldust ei kasutata, on olek **Heaks kiidetud** kohe nende loomisel, samas kui ostutellimustel, mis kasutavad muudatuste haldust, on loomisel olek **Mustand**. Ostutellimusele, mis on loodud koondplaneerimise plaanitud tellimuse kinnitamisega, määratakse alati olek **Heaks kiidetud**, olenemata muudatuste halduse sätetest. Ostutellimus tekitab laokandeid ainult siis, kui see saavutab oleku **Heaks kiidetud**. Seetõttu ei kuvata neid varusid reserveerimiseks või märkimiseks kättesaadavana enne tellimuse vastuvõtmist.

Ostutellimuste muudatuste juhtimine lubatakse valiku **Muudatusehalduse aktiveerimine** seadistamisega lehel **Hankeparameetrid**. Kui muudatuste haldus on lubatud, peab ostutellimus läbima pärast lõpetamist heakskiitmise töövoo. Supply Chain Managementil on töövooprotsessi redaktor, kus saab määratleda heakskiitmise protsessi kajastamiseks töövoo. See töövoog võib sisaldada reegleid automaatseks heakskiitmiseks, reegleid, mis määravad, kes määratakse konkreetseid ostutellimusi heaks kiitma, ja reegleid pikka aega heakskiitmist oodanud töövoo eskaleerimiseks. Saate lubada muudatuste halduse protsessi kõigile hankijatele või konkreetsetele hankijatele. Samuti saate seadistada protsessi nii, et selle saab eraldi ostutellimuste puhul alistada.

Kui muudatuste haldus on lubatud, läbivad ostutellimused kuus heakskiitmise olekut, alates olekust **Mustand** kuni olekuni **Lõpetatud**. Pärast tellimuse heakskiitmist peavad kasutajad, kes soovivad seda muuta, kasutama toimingut **Taotle muudatust**.

| Kinnitamise olek | Kirjeldus                                                                      | Muudatuse taotlemine on lubatud |
|-----------------|----------------------------------------------------------------------------------|---------------------------|
| Mustand           | Ostutellimus on mustand ja seda pole ostutellimuse töövoos heakskiitmiseks esitatud.     | Ei                        |
| Ülevaatamisel       | Ostutellimus esitati ostutellimuse töövoos heakskiitmiseks. Heakskiit on ootel       | Ei                        |
| Tagasi lükatud        | Ostutellimus lükati heakskiitmise protsessi ajal tagasi.                                 | Ei                        |
| Kinnitatud        | Ostutellimus kiideti heaks.                                                             | Jah                       |
| Kinnitatud       | Ostutellimus kinnitati. Ostutellimust ei saa kinnitada enne, kui see on heaks kiidetud.        | Jah                       |
| Lõpetatud       | Ostutellimus muudeti lõplikuks. See on nüüd rahaliselt suletud ja seda ei saa enam muuta. | Ei                        |

## <a name="confirming-purchase-orders"></a>Ostutellimuste kinnitamine
Ostutellimused, mille heakskiitmise olek on **Heaks kiidetud**, võivad läbida enne kinnitamist lisatoimingud. Näiteks võib olla vaja saata hankijale ostupäring, et küsida hindade, allahindluste või tarnekuupäevade kohta. Sel juhul saate määrata ostutellimuse olekuks **Välisel ülevaatamisel**, kasutades toimingut **Ostupäring**.

Hankijad, kes on seadistatud kasutama hankijaportaali, saavad vaadata portaalis tellimusi üle ja neid heaks kiita või tagasi lükata. Selle ülevaatamisprotsessi käigus on ostutellimuse olek **Välisel ülevaatamisel**. Hankijaportaali on võimalik konfigureerida nii, et hankija kinnitus kinnitab tellimuse Supply Chain Managementis automaatselt. Teise võimalusena saate ostutellimuse käsitsi kinnitada, kui olete hankijalt kinnituse saanud. Kui hankija lükkab ostutellimuse tagasi, saadakse tagasilükkamine koos tagasilükkamise põhjuse ja muudatuste soovitustega. Sel juhul jääb ostutellimuse olekuks **Välisel ülevaatamisel**.

Võimalik on luua ka tellimuse pro-forma kinnitus enne tegeliku kinnituse töötlemist. See valik loob lihtsalt aruande, mida saate hankijaga jagada. See ei loo mingit töölehe teavet.

Pärast seda, kui hankija on tellimusega nõustunud, on järgmine etapp ostutellimuse salvestamine kooskõlastatuna. Selle etapi saab läbida, kasutades toimingut **Kinnitus** või toimingut **Kinnita**. Mõlemad toimingud määravad tellimuse heakskiitmise olekuks **Kinnitatud**. Tellimuse kinnitamine käivitab kaks lisaprotsessi.

-   Luuakse tööleht süsteemis kinnitatud andmete täpse koopia salvestamiseks. Mõnikord on tellimustes vaja teha muudatusi ja pärast värskendatud tellimuse kinnitamist luuakse lisatöölehti. Nende töölehtede abil saate vaadata tellimuse mitmesuguste kinnitatud versioonide ajalugu.
-   Luuakse arvestuse jaotused ja toimub tellimuse ja eelarve kontrollimine, kui see funktsioon on lubatud. Kui kumbki kontrollimine nurjub, saate tõrketeate, mis ütleb, et enne ostutellimuse uut kinnitamist tuleb seda muuta.

Hankija võib nõuda mingisugust kinnitust, et ostu eest tasutakse. Selle garantii andmiseks on ostureskontro protsessides mitmesuguseid võimalusi. Näiteks toiming **Ettemaks** reserveerib ostutellimuse jaoks vahendid ja see ettemaks kajastatakse ostutellimusel.

## <a name="changing-purchase-orders"></a>Ostutellimuste muutmine
Mõnikord võib olla vaja ostutellimust muuta pärast seda, kui see on saavutanud kinnitusoleku **Heaks kiidetud** või **Kinnitatud**.

Kui ostutellimus loodi muudatuste halduse protsessi kasutades, saate teha muudatusi, kutsudes tellimuse tagasi või, kui tellimus on juba kinnitatud, siis kasutades toimingut **Taotle muudatust**. Sel juhul määratakse heakskiitmise olekuks uuesti **Mustand** ja saate siis tellimust muuta. Kui olete muudatuste tegemise lõpetanud, võib olla vaja ostutellimus uuesti heakskiitmiseks esitada. Saate konfigureerida muudatuste tüüpe, mis nõuavad uut heakskiitmist, kasutades poliitikareeglit **Ostutellimuste eelkinnituse reegel** lehel **Ostupoliitikad**.

Kui osa ostutellimuse rea tellitud kogusest on tarnitud, ei saa tellitud kogust muuta, kui ostutellimus on režiimis **Mustand**. Siiski saate muuta ostutellimuse real kogust **Tarne jääk**, mis on olekus **Mustand**.

Pärast seda, kui tellimus on kinnitatud, ei saa seda enam kustutada. Kuid tühistada saab kogu tellimuse koguse või järelejäänud koguse, eeldusel, et see kogus pole kätte saadud või arveldatud. Seejärel saate kasutada toimingut **Lõpeta** edasise töötlemise vältimiseks. 


## <a name="canceling-purchase-orders"></a>Ostutellimuste tühistamine

Ostutellimust saab tühistada, kasutades päises toodud tegevust **Tühista**.

Kui kogus on osaliselt registreeritud, vastu võetud või arveldatud, saate tühistada ainult järelejäänud koguse, mis ei ole registreeritud, saadud või arveldatud. Tellimuse kogust vähendatakse vastavalt. Kui rea kogust uuendatakse, uuendatakse ka rea olek. Näiteks oletagem, et rea algne kogus on 5, millest vastuvõetud kogus 3. Sel juhul saab tühistada ainult kaks. Seejärel uuendatakse rida olekusse **Vastuvõetud**.

Kui tellimuse reale on lisatud tarnejääk ja see ületab tellimuse real oleva koguse, ei tühista tegevus **Tühista** üleliigset kogust. Selle asemel jääb rida olekusse **Avatud tellimus**, kuna sellel on järelejäänud kogus. Näiteks oletagem, et rea algne kogus on 5 ja tarnejääk on 7. Kui tellimus tühistatakse, tühistatakse viis ja jääb kogus 2, nagu näete varude kannete alt.

Ostutellimuse rea kogu koguse tühistamiseks peate real tühistama tarnejäägi järelejäänud koguse. Seejärel uuendatakse rida olekusse **Tühistatud**.

Kui ostutellimus on muudatuste haldamise all, tuleb kõik muudatused, nt tellimuse tühistamine või tarnejääk, esitada töövoo süsteemile ja kinnitada enne protsessi lõpuleviimist ja varude kannete uuendamist vastavalt tühistamisele.

<a name="additional-resources"></a>Lisaressursid
--------

[Ostutellimuse ülevaade](purchase-order-overview.md)

[Ostutellimuste loomine](purchase-order-creation.md)

[Toote sissetulek ostutellimuste suhtes](product-receipt-against-purchase-orders.md)

[Hankija arvete ülevaade](../../finance/accounts-payable/vendor-invoices-overview.md)



