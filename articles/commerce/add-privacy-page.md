---
title: Privaatsuspoliitika lehe lisamine
description: See artikkel kirjeldab, kuidas lisada saidile privaatsuspoliitika lehekülge Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: a874272fe5158dd213a69c7ba996e0d28c7ed15a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272067"
---
# <a name="add-a-privacy-policy-page"></a>Privaatsuspoliitika lehe lisamine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas lisada saidile privaatsuspoliitika lehekülge Microsoft Dynamics 365 Commerce.

Privaatsuse vastavus hõlmab organisatsioonilisi meetmeid, mis teavitavad saidi kasutajaid nende andmete kogumisest ja käitlemisest. Kasutajad saavad seejärel otsustada, kuidas nad soovivad oma isiklikke andmeid töödelda ja võtta asjakohaseid meetmeid.

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a>Microsofti privaatsusavalduse ülevaatamine Dynamics 365 Commerce'is

Microsofti privaatsusavalduse ülevaatamiseks, kui olete sisse logitud Dynamics 365 Commerce, valige ülemises parempoolses nurgas nupp **spikker** (**?**) ja seejärel valige **Privaatsus ja küpsised.** Avatakse uus vahekaart, millel on link [Microsofti privaatsusavaldusele.](https://privacy.microsoft.com/privacystatement)

## <a name="build-a-privacy-policy-page-for-your-site"></a>Oma saidi privaatsuspoliitika loomine

Rakenduses Dynamics 365 Commerceon mitu võimalust, kuidas anda kasutajatele saidile juurdepääs teie privaatsuspoliitikale. Selles jaotises kirjeldatakse, kuidas luua privaatsuspoliitika lehte ja seejärel viidata leheküljele, kasutades jaluse fragmenti.

Järgnev juhend on näide, mis näitab, kuidas luua Commerce saidi üldise privaatsuspoliitika lehte. Olete vastutav privaatsuspoliitika lehekülje lahenduse projekteerimise ja rakendamise eest, mis vastab kõige paremini teie ettevõtte juriidilistele nõuetele.

Alustamiseks valige loomise tööriistade abil sait, mille jaoks soovite luua privaatsuspoliitika lehekülje.

### <a name="create-a-template"></a>Loo mall

> [!NOTE]
> Kui mall, mida saab kasutada privaatsuspoliitika jaoks, on juba loodud, minge edasi, et [luua privaatsuspoliitika lehekülg.](#build-a-privacy-policy-page)

Malli loomiseks tehke järgmist.

1. Avage **Mallid** ja valige lehe malli loomiseks **Uus**.
1. Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all **Reklaambänneri mall** ja valige seejärel **OK**.
1. Mallis lisage nõutavad moodulid nõutavatele lehekülje pesadele. Juhiste saamiseks liikuge üle punase hüüumärgi. (Näiteks võib **HTML-i pea** pesa nõuda **vaikimisi välise skripti** moodulit.)
1. Lisage **kehateksti** pesasse **vaikelehe** moodul.
1. Lisage **vaikelehe** mooduli **peamisesse** pessa **sisurikka ploki** moodul.
1. **Sisurikka ploki** moodulis lisage **sisurikka ploki üksuse** moodul.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

### <a name="build-a-privacy-policy-page"></a>Privaatsuspoliitika lehe loomine

Privaatsusoliitika lehe loomiseks toimige järgmiselt.

1. Avage **Lehed** ja seejärel uue lehe loomiseks **Uus**.
1. Valige privaatsuspoliitika lehe mall dialoogiboksis **Vali mall**.
1. Sisestage lehe nimi ja lehe URL, seejärel valige **OK**. 
1. **Peamisesse** lehe pessa lisage **sisurikka ploki** moodul.
1. **Sisurikka ploki** moodulis lisage **sisurikka ploki üksuse** moodul.
1. **Sisurikka ploki** mooduli atribuutide paanil valige **lisa andmeallikas** ja seejärel valige **rikkaliku teksti sisu.**
1. RTF-redaktoris sisestage privaatsuspoliitika lehele sisu. Laiendage RTF-redaktorit täisekraani režiimile, nagu vajate.
1. Kui olete sisu sisestamise lõpetanud, valige veebibrauseris lehe eelvaate kuvamiseks **eelvaade**.
1. Täitke kõik järelejäänud täiendused leheküljele ja mooduli atribuutidele.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

Privaatsuspoliitika lehe URL-i avaldamiseks järgige neid samme.

1. Avage **URL-** id ja valige privaatsuspoliitika lehele URL.
1. Valitud URL-i avaldamiseks valige **Avalda**.

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a>Lingi loomine privaatsuspoliitika lehele jaluses

Saate lisada lingi privaatsuspoliitika lehele fragmenti. Sel viisil saate linki jagada ja värskendada selle mitme saidi lehekülgede vahel, viitades fragmendile. See näide näitab, kuidas lisada privaatsuspoliitika lehele jaluse fragmendile link.

Jaluse fragmendile lingi lisamiseks tehke järgmist.

1. Avage **Fragmendid** ja valige seejärel lehe fragmendi loomiseks **Uus**.
1. Valige dialoogiboksis **Uus fragment** moodul **Jalus**.
1. Sisestage jaotises **Fragmendi nimi** fragmendi nimi ja seejärel valige **OK**.
1. **Jaluse kategooria** pesas lisage **jaluse üksuse** moodul.
1. Parempoolsel atribuutide paanil valige suvand **Lingi tekst**.
1. Dialoogiaknas **lingi tekst** sisestage lingi tekst ja lingi eesmärk privaatsuspoliitika lehele ja seejärel klõpsake **OK**.
1. Privaatsuspoliitika lehe URL-i saamiseks minge lehele **Leheküljed**, minge lehele privaatsuspoliitika ja kopeerige URL atribuutide paanilt.
1. Valige **Salvesta**, valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Vaadake fragment üle ja kontrollige linki privaatsuse poliitika lehele.

Nüüd saab fragmenti viidata teiste saidi lehtede mallis. Kui seda fragmenti viidatakse malli **jaluse** moodulis, kuvatakse lingi viide kõigil lehekülgedel, mis on selle malli abil ehitatud.

## <a name="additional-resources"></a>Lisaressursid

[Vastavuse ülevaade](compliance-overview.md)

[Hõlbustusfunktsioonid ja -võimalused](accessibility.md)

[Küpsise vastavus](cookie-compliance.md)

[Jälgitud sisumuudatustega seostatud kasutaja ID-de asendamine](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
