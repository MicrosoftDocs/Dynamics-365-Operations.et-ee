---
title: Privaatsuspoliitika lehe lisamine
description: Selles teemas kirjeldatakse, kuidas lisada privaatsuspoliitika rakenduses Microsoft Dynamics 365 Commerce oma saidile.
author: v-chgri
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fd39ff5f8c5d97f2d524043b65627dc7e87fcf64
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946001"
---
# <a name="add-a-privacy-policy-page"></a>Privaatsuspoliitika lehe lisamine

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lisada privaatsuspoliitika rakenduses Microsoft Dynamics 365 Commerce oma saidile.

## <a name="overview"></a>Ülevaade

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

1. Avage **Mallid \> Uus mall**.
1. Sisestage malli nimi ja valige seejärel **OK**.
1. Mallis lisage nõutavad moodulid nõutavatele lehekülje pesadele. Juhiste saamiseks liikuge üle punase hüüumärgi.

    Näiteks võib **HTML-i pea** pesa nõuda **vaikimisi välise skripti** moodulit.

1. Lisage **kehateksti** pesasse **vaikelehe** moodul.
1. Lisage **vaikelehe** mooduli **peamisesse** pessa **sisurikka ploki** moodul.
1. **Sisurikka ploki** moodulis lisage **sisurikka ploki üksuse** moodul.
1. Registreerige mall ja avaldage see.

### <a name="build-a-privacy-policy-page"></a>Privaatsuspoliitika lehe loomine

Privaatsusoliitika lehe loomiseks toimige järgmiselt.

1. Avage **Lehed \> Uus leht**.
1. Valige privaatsuspoliitika lehele mall.
1. Sisestage lehe nimi ja URL, seejärel valige **OK**. 
1. **Peamisesse** lehe pessa lisage **sisurikka ploki** moodul.
1. **Sisurikka ploki** moodulis lisage **sisurikka ploki üksuse** moodul.
1. **Sisurikka ploki** mooduli atribuutide paanil valige **lisa andmeallikas** ja seejärel valige **rikkaliku teksti sisu.**
1. RTF-redaktoris sisestage privaatsuspoliitika lehele sisu. Laiendage RTF-redaktorit täisekraani režiimile, nagu vajate.
1. Kui olete sisu sisestamise lõpetanud, valige veebibrauseris lehe eelvaate kuvamiseks **eelvaade**.
1. Täitke kõik järelejäänud täiendused leheküljele ja mooduli atribuutidele.
1. Registreerige privaatsuspoliitika leht ja avaldage see.

Privaatsuspoliitika lehe URL-i avaldamiseks järgige neid samme.

1. Avage **URL-** id ja valige privaatsuspoliitika lehele URL.
1. Avaldage valitud URL.

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a>Lingi loomine privaatsuspoliitika lehele jaluses

Saate lisada lingi privaatsuspoliitika lehele fragmenti. Sel viisil saate linki jagada ja värskendada selle mitme saidi lehekülgede vahel, viitades fragmendile. See näide näitab, kuidas lisada privaatsuspoliitika lehele jaluse fragmendile link.

Jaluse fragmendile lingi lisamiseks tehke järgmist.

1. Avage **Lehe fragmendid \> Uus lehe fragment**.
1. Valige **jaluse** moodul ja sisestage nimi väljale **lehekülje fragmendi nimi**.
1. **Jaluse kategooria** pesas lisage **jaluse üksuse** moodul.
1. Parempoolsel atribuutide paanil valige suvand **Lingi tekst**.
1. Dialoogiaknas **lingi tekst** sisestage lingi tekst ja lingi eesmärk privaatsuspoliitika lehele ja seejärel klõpsake **OK**.

    Privaatsuspoliitika lehe URL-i saamiseks minge lehele **Leheküljed**, minge lehele privaatsuspoliitika ja kopeerige URL atribuutide paanilt.

1. Salvestage lehe fragment, registreerige see ja avaldage.
1. Vaadake fragment üle ja kontrollige linki privaatsuse poliitika lehele.

Nüüd saab fragmenti viidata teiste saidi lehtede mallis. Kui seda fragmenti viidatakse malli **jaluse** moodulis, kuvatakse lingi viide kõigil lehekülgedel, mis on selle malli abil ehitatud.

## <a name="additional-resources"></a>Lisaressursid

[Vastavuse ülevaade](compliance-overview.md)

[Hõlbustusfunktsioonid ja -võimalused](accessibility.md)

[Küpsise vastavus](cookie-compliance.md)
