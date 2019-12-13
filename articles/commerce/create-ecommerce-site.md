---
title: E-kaubanduse saidi loomine
description: Selles teemas kirjeldatakse ülesandeid, mis on seotud uue e-kaubanduse saidi loomisega rakenduses Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fd87a51b73deae64867b0420c00db9fce7c79336
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697125"
---
# <a name="create-an-e-commerce-site"></a>E-kaubanduse saidi loomine

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse ülesandeid, mis on seotud uue e-kaubanduse saidi loomisega rakenduses Dynamics 365 Commerce.

## <a name="overview"></a>Ülevaade

Oma e-kaubanduse saidi arendamise alustamiseks peate kõigepealt looma saidi autorluse keskkonnas uue saidi. Enne uue saidi loomist peab olema rakenduses Dynamics 365 Retail loodud vähemalt üks veebipood. 

## <a name="set-up-your-site"></a>Saidi seadistamine

Oma saidi seadistamiseks tehke järgmist.

1. Valige Microsofti teenuse Lifecycle Services (LCS) saidi autorluse keskkonna link. 
1. Valige saidi autorluse keskkonna avalehel suvand **Uus sait**.
1. Sisestage dialoogiboksi **Uus sait** järgmine teave.

| Väli                               | Kirjeldus |
|-------------------------------------|-------------|
| Saidi nimi                           | Sisestage kuvatav nimi, mida tuleks saidi autorluse keskkonnas teie saidi jaoks kasutada. See nimi on nähtav ainult autorluse keskkonnas ja seda ei kuvata klientidele. |
| Saidi administraatori turberühm | Määrake Microsoft Azure Active Directory (Azure AD) turberühm, mis haldab kasutajaid, kellel on sellel saidil saidi administraatori roll. |
| Vaikekanal (tootmisüksuse number) | Valige veebipood, mille jaoks see sait toimib fassaadina. Kui soovite, et teie e-kaubanduse sait toetaks mitut veebipoodi, peate pärast saidi seadistamist seostama poed oma saidiga suvandis **Saidi sätted**. |
| Vaikekeel                            | Määrake selle veebipoe ja turu vaikekeel. Veebipood võib toetada mitut keelt. Kui soovite selle veebipoe või mõne muu veebipoe jaoks toetada mitut keelt, saate konfigureerida selle toe pärast saidi seadistamist suvandis **Saidi sätted**.  |
| Domeen                              | Valige domeeni nimi, mis toimib selle veebipoe jaoks domeenina. Kui te pole LCS-is ühtegi domeeni konfigureerinud, võite selle välja tühjaks jätta. Pärast domeeni LCS-is konfigureerimist peate lisama selle oma veebipoele suvandis **Saidi sätted**.  |
| Tee                              | Kui teie sait toetab antud domeeninime puhul rohkem kui ühte keelt, kasutage tee välja, et luua selle domeeni ja keele kombinatsiooni jaoks kordumatu saidi URL. Kui keel, mille väljal **Vaikekeel** määrasite, on ainus selle domeeni jaoks toetatav keel või see on pärast saidi täiendavate keelte jaoks lokaliseerimist jätkuvalt vaikekeel, soovitame jätta selle välja tühjaks. |


Pärast saidi loomist saate kontrollida, kas see on teie võrgupoega seotud, valides vahekaardi **Tooted**. Peaksite nägema veebipoele eraldatud toodete valikut. Saate kasutada ka lehe üleval vasakul ripploendit, et pääseda kategooriate põhjal eraldatud toodete juurde.

## <a name="additional-resources"></a>Lisaressursid

[E-poe ülevaade](online-store-overview.md)

[Uue e-kaubanduse saidi juurutamine](deploy-ecommerce-site.md)

[Veebisaidi seostamine kanaliga](associate-site-online-store.md)

[Domeeninime konfigureerimine](configure-your-domain-name.md)

[Sisuedastusvõrgu (CDN) toe lisamine](add-cdn-support.md)

[Asukohapõhise poetuvastuse lubamine](enable-store-detection.md)

[Kasutaja sisselogimiseks kohandatud lehtede seadistamine](custom-pages-user-logins.md)

[Autorluse avalehe ülevaade](authoring-home-overview.md)

[Uue saidilehe lisamine](add-new-page.md)
