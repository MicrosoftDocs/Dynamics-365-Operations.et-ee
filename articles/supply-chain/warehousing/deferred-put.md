---
title: Laotöö töötlemise edasilükkamine
description: Selles teemas kirjeldatakse funktsioone, mis muudavad edasilükatud lao tööüksuse toimingute töötlemise saadavaks rakenduses  Dynamics 365 Supply Chain Management.
author: josaw1
manager: AnnBe
ms.date: 11/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-6-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b67b3899a506c02b581d04f51691cb4408ee012e
ms.sourcegitcommit: 0af4caa9f5ea6f6c1d1f4b30090e02e7f755df36
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/19/2019
ms.locfileid: "2815784"
---
# <a name="deferred-processing-of-warehouse-work"></a>Laotöö töötlemise edasilükkamine

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/pivate-preview-banner.md)]

Selles teemas kirjeldatakse funktsioone, mis muudavad edasilükatud lao tööüksuse asetamistoimingute töötlemise saadavaks rakenduses Dynamics 365 Supply Chain Management.

Edasilükatud töötlemise funktsioon võimaldab laotöötajatel jätkata muude töödega, kui asetamistoiminguid taustal töödeldakse. Edasilükatud töötlemine on kasulik, kui palju tööridu tuleb töödelda ja töötaja saab lasta selle töö töödelda asünkroonselt. See on kasulik ka siis, kui serveris võib olla töötlusaja ad-hoc plaaniväline suurenemine ja suurenenud töötlusaeg võib mõjutada kasutaja tootlikkust.

Taustal töötlemine saavutatakse SysOperationi raamistiku abil. Lisateavet lugege teemast [SysOperationi raamistiku ülevaade](https://docs.microsoft.com/dynamicsax-2012/developer/sysoperation-framework-overview).

## <a name="configuring-the-work-processing-policies"></a>Töö töötluspoliitikate konfigureerimine

Edasilükatud töötlemise kasutamiseks peate konfigureerima ja kasutama töö töötlemise poliitikat.

Poliitikad on konfigureeritud lehel **Töö töötlemise poliitikad**. Järgmises tabelis kirjeldatakse selle lehe välju.

| Väli                           | Kirjeldus |
|---------------------------------|-------------|
| Töö töötlemise poliitika nimi     | Töö töötlemise poliitika nimetus. |
| Töötellimuse tüüp                 | Töökäsu tüüp, millele poliitika rakendatakse. |
| Toiming                       | Toiming, mida töödeldakse poliitika abil. |
| Töö töötlemise meetod          | Meetod, mida kasutatakse töörea töötlemiseks. Kui meetodiks on määratud **Viivitamatu**, meenutab käitumine käitumist, kui töö töötlemise poliitikaid kasutatakse rea töötlemiseks. Kui meetodiks on määratud **Edasilükatud**, kasutatakse edasilükatud töötlemist, siis kasutatakse pakett-töö raamistikku. |
| Edasilükatud töötlemise lävi   | Väärtus **0** (null) näitab, et läve pole. Sel juhul kasutatakse edasilükatud töötlemist, kui seda saab kasutada. Kui konkreetne lävearvutus jääb allapoole läve, kasutatakse meetodit Viivitamatu. Muul juhul kasutatakse meetodit edasilükatud, kui seda saab kasutada. Müügi ja ülekandega seotud töö puhul arvutatakse lävi seotud allika koormusridade arvuga, mida töö jaoks töödeldakse. Täiendustöö puhul arvutatakse lävi tööridade arvuga, mida töö abil täiendatakse. Kui määrate müügi läveks näiteks **5**, ei kasuta vähemate kui viie allika koormusreaga väiksemad tööd edasilükatud töötlemist, kuid suuremad tööd kasutavad seda. Lävi toimib ainult siis, kui töö töötlemise meetodiks on määratud **Edasilükatud.** |
| Edasilükatud töötlemise partii grupp |Pakktööde grupp, mida kasutatakse töötlemiseks. |

Edasilükatud put-töötlemise jaoks toetatakse järgmisi töökäsutüüpe: müügitellimus, ülekandetellimuse väljastamine ja täiendamine.

## <a name="assigning-the-work-creation-policy"></a>Töö loomise poliitika määramine

Töö loomise poliitikat saab määrata laohalduse parameetrites. Seda saab määrata ka üksikute ladude tasandil. Kui poliitika on määratud laole, rakendatakse seda ainult selle lao jaoks loodavatele töödele. Kui laotasemel pole ühtegi poliitikat määratud, rakendatakse laohalduse parameetrite poliitikat.

## <a name="viewing-the-deferred-put-processing-tasks"></a>Edasilükatud asetamise töötlemise ülesannete kuvamine

Edasilükatud asetamise töötlemise ülesandeid saate vaadata lehel **Edasilükatud asetamise töötlemise ülesanded**.

Vaikimisi kuvatakse **Täidetud** ülesanded.

| Väli            | Kirjeldus |
|------------------|-------------|
| Olek           | Ülesande olek. |
| Pakett-töö olek | Seotud pakett-töö olek. Kui pakett-töö on töödeldud, sisaldab pakett-töö ajalugu pakett-töö logi ja teavet. |

Siin on võimalike olekute selgitus.

- **Ootel** – seotud pakett-töö ootab töötlemist pakktöötlusserveris.
- **Nurjus** – töötlemine nurjus. Ülesannet saab uuesti töödelda tegevusega  **Töötle edasilükatud asetamist** või selle saab tühistada, kasutades tegevust **Loobu edasilükatud asetamisest**.
- **Lõpule viidud** – töö on lõpule viidud.

## <a name="impact-on-closed-work-dates"></a>Mõju suletud töö kuupäevadele

Edasilükatud asetamise töötlemise kasutamisel on suletud töö kuupäev määratud edasilükatud asetamise töötlemise ülesande kuupäeva/kellaajana. Suletud töö kuupäeva kasutatakse, sest see on parim hinnang sellele, millal asetamise toiming lõpule viidi.

## <a name="reprocessing-a-failed-task"></a>Nurjunud tööülesande uuesti töötlemine

Nurjunud ülesannet saate uuesti töödelda, valides selle lehel ja valides **Töötle edasilükatud asetamist.** Uuesti töötlemine vastab olukorrale, kus kasutaja lõpetab mobiilsest seadmest kõrvalepaneku, nagu see oleks seadistatud koheseks töötlemiseks.

## <a name="canceling-failed-tasks"></a>Nurjunud ülesannete tühistamine

Tühistada saab ainult nurjunud ülesandeid. Ülesande tühistamisel saate selle määrata uuele kasutajale. Teise võimalusena võib ülesanne jääda määratuks kasutajale, kes tööd töötles. Tühistamine vastab olukorrale, kus töö tuuakse tagasi mobiilsesse seadmesse, nagu viimane komplekteerimisetapp oleks just lõpule viidud ja töö tuleb kõrvale panna. Kuid kasutaja saab siiski määrata, et töö on „erinev”, sest see on ainult kõrvalepaneku etapis ja asukoht vastab asukohale, kus esimene tööd töödelnud kasutaja oli selle määranud lõplikuks asetamise asukohaks.

Kui ülesanne on tühistatud, siis edasilükatud asetamise töötlemise blokeerimise põhjus ei blokeeri enam tööd. Seda saab mobiilse seadmega uuesti töödelda.

Ülesande kirje kustutatakse tööülesande tühistamisel.

## <a name="configuring-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>Mobiilse seadme menüü konfigureerimine viivitatud töötlemise poliitika vahelejätmiseks

Saate konfigureerida mobiilse seadme menüükäsu nii, et edasilükatud töötlemise poliitikat ei kasutataks. Töö töödeldakse siis nii, nagu edasilükkunud töötlemise poliitikat ei kasutata. See funktsioon võimaldab juhendajal kasutada konkreetset menüükäsku, kus edasilükatud asetamist ei kasutata. Selle konfigureerimiseks määrake välja **Edasilükatud asetamise töötlemise poliitika** väärtuseks **Alista sätted ja töötle asetamist sünkroonselt**. 

## <a name="restrictions-when-the-deferred-put-processing-isnt-applied"></a>Piirangud, kui edasilükatud asetamise töötlemist ei rakendata

On mitu stsenaarium, mille korral edasilükatud asetamise töötlemist ei rakendata isegi siis, kui poliitika on konfigureeritud. Järgmisena on toodud mõned näited.

- Kasutatakse käsitsi töötamise lõpuleviimist.
- Töö viiakse lõpule automaatset lõpuleviimisega.
- Kasutatakse auditimalle.


## <a name="monitoring-the-deferred-processing-tasks-from-the-outbound-work-monitoring-workspace"></a>Edasilükatud töötlemisülesannet jälgimine väljamineva töö jälgimise tööruumist

Tööruumis **Väljaminev töö jälgimine** on kaks paani, mis aitavad teil jälgida edasilükatud asetamise töötlemise ülesandeid.

- **Nurjunud edasilükatud asetamise töötlusülesanded** – sellel paanil kuvatakse nurjunud ülesannete arv. Nurjunud tööülesannete korral peab laohalduri need kas uuesti töötlema või need tühistama, kuna neid ei töödelda automaatselt uuesti.
- **Ootel edasilükatud asetamise töötlemise ülesanded** – see paan näitab nende ülesannete arvu, mis on olekus **Ootel** olnud rohkem kui 10 minutit. Kui paan näitab numbrit, võib see viidata pakktöötluse käigus ilmnenud probleemile. **Ootel** ülesandeid saate käsitsi töödelda. Kui ülesande pakett-töö töödeldakse hiljem, siis see lihtsalt nurjub, kuna seda on juba töödeldud. Mingit mõju ei ole.

## <a name="deleting-completed-tasks"></a>Lõpule viidud ülesannete kustutamine

Saate kustutada edasilükatud asetamise ülesandeid, mis on lõpule viidud, valides need ja kustutades need lehelt.
