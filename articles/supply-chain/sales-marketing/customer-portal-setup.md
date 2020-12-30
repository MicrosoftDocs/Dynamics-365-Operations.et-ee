---
title: Kliendiportaali installimine, seadistamine ja värskendamine
description: See teema hõlmab kliendiportaali litsentside üksikasju ja seadistamise juhiseid.
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e61fc5f7151a0bb61d496d47f4ad4e727a2a1d65
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529526"
---
# <a name="install-set-up-and-update-the-customer-portal"></a>Kliendiportaali installimine, seadistamine ja värskendamine

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a>Litsentsimisnõuded

Kliendiportaali kasutamiseks peavad teil olema järgmised litsentsid.

- **Power Appsi portaalid** – see litsents on vajalik kliendiportaali majutamiseks. Portaalide litsentsid põhinevad kasutusel. Lisateavet vt teemast [Power Appsi portaalide litsentsimisnõuded](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).
- **Topeltkirjutus** – teil peavad olema vajalikud litsentsid, et võimaldada Supply Chain Managementi üksuste topeltkirjutust. Lisateavet vt teemast [topeltkirjutuse süsteeminõuded](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a>Topeltkirjutuse ja Power Appsi portaalide sõltuvused

Kliendiportaal sõltub Power Appsi portaalidest ja topeltkirjutusest, nagu on näidatud järgmisel pildil.

![Kliendiportaali sõltuvused](media/customer-portal-elements.png "Kliendiportaali sõltuvused")

Erinevalt teenuse Supply Chain Management teistest funktsioonidest paikneb kliendiportaali mall Power Appsi portaalides. Seega on kliendiportaali funktsionaalsus ja võimalused piiratud Power Appsi portaalide ning topeltkirjutuse üksuste pakutavatega.

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a>Vajalikud seadistused kliendiportaali lubamiseks

Kui olete veendunud, et teil on vajalikud litsentsid, siis võite seadistada topeltkirjutamise, nagu on kirjeldatud jaotises [topeltkirjutamise esmase sünkroonimise juhised](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).

Veenduge, et topeltkirjutamise puhul oleksid lubatud järgmised üksuse vastendused.

- Müügitellimuse päis
- Müügitellimuse üksikasjad
- Kontod
- Kontaktid
- Tooted

Pärast seadistuse lõpule viimist saate valmistada ette kliendiportaali malli.

## <a name="provision-the-customer-portal"></a>Kliendiportaali ettevalmistamine

Enne alustamist veenduge, et oleksite [nõutud seadistused](#required-setup) juba lõpule viinud. Seejärel toimige kliendiportaali ette valmistamiseks järgmiselt.

1. Avage [make.powerapps.com](https://make.powerapps.com/).
2. Veenduge, et kasutaksite keskkonda, kus te topeltkirjutamise lubasite.
3. Kerige vahekaardil **Loo** allapoole kuni jaotiseni **Alusta mallist** ja valige seejärel mall nimega **Kliendiportaal**.
4. Järgige ekraanil toodud juhiseid.

Pärast ettevalmistuse lõpule viimist saate avada kliendiportaali lehel **Avaleht** jaotises **Teie rakendused**.

> [!NOTE]
> Kui keskkonnas, kus te töötate, ei ole paigaldatud topeltkirjutamise lahendust, siis kuvatakse teile tõrketeade ja kliendiportaali ei saa ette valmistada.

## <a name="update-the-customer-portal"></a>Kliendiportaali uuendamine

Kliendiportaalile võidakse hiljem lisada uusi funktsioone. Kõik Microsofti tehtavad lahenduse põhikomponentide muudatused ilmuvad teie keskkonda automaatselt. Samas ei kajastu teie keskkonnas ettevalmistatud veebisaidil automaatselt konfiguratsiooniandmetes tehtud muudatused. Need muudatused tuleb rakendada käsitsi, hankides uuest mallist koodi ja ühendades selle ettevalmistatud veebisaidiga.

## <a name="additional-resources"></a>Lisaressursid

Kliendiportaali seadistamise ja kohandamise lähemalt tundma õppimiseks peaksite alustama alltoodud alustehnoloogiaid käsitleva dokumentatsiooni läbivaatamisest.

- [Power Appsi portaalide dokumentatsioon](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [Topeltkirjutuse dokumentatsioon](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

Portaalide tõhusaks haldamiseks peate mõistma Power Appsi portaalide ja Common Data Service'i töötsüklit. Lisateavet vt järgmistest allikatest.

- [Portaali töötsükkel](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [Portaali uuendamine](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [Portaali konfiguratsiooni migreerimine](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Lahenduse töötsükli haldus: Dynamics 365 for Customer Engagementi rakendused](https://www.microsoft.com/download/details.aspx?id=57777)
