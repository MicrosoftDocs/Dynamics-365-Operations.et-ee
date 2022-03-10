---
title: Kliendiportaali installimine, seadistamine ja värskendamine
description: See teema hõlmab kliendiportaali litsentside üksikasju ja seadistamise juhiseid.
author: Henrikan
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 187efe1372bf2400241f3d65751189247c001447
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8060609"
---
# <a name="install-set-up-and-update-the-customer-portal"></a>Kliendiportaali installimine, seadistamine ja värskendamine

[!include [banner](../includes/banner.md)]


## <a name="licensing-requirements"></a>Litsentsimisnõuded

Kliendiportaali kasutamiseks peavad teil olema järgmised litsentsid.

- **Power Appsi portaalid** – see litsents on vajalik kliendiportaali majutamiseks. Portaalide litsentsid põhinevad kasutusel. Lisateavet vt teemast [Power Appsi portaalide litsentsimisnõuded](/power-platform/admin/powerapps-flow-licensing-faq#portals).
- **Topeltkirjutus** – teil peavad olema vajalikud litsentsid, et võimaldada Supply Chain Managementi tabelite topeltkirjutust. Lisateavet vt teemast [topeltkirjutuse süsteeminõuded](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a>Topeltkirjutuse ja Power Appsi portaalide sõltuvused

Kliendiportaal sõltub Power Appsi portaalidest ja topeltkirjutusest, nagu on näidatud järgmisel pildil.

![Kliendiportaali sõltuvused.](media/customer-portal-elements.png "Kliendiportaali sõltuvused")

Erinevalt teenuse Supply Chain Management teistest funktsioonidest paikneb kliendiportaali mall Power Appsi portaalides. Seega on kliendiportaali funktsionaalsus ja võimalused piiratud Power Appsi portaalide ning topeltkirjutuse tabelites pakutavatega.

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a>Vajalikud seadistused kliendiportaali lubamiseks

Kui olete veendunud, et teil on vajalikud litsentsid, siis võite seadistada topeltkirjutamise, nagu on kirjeldatud jaotises [topeltkirjutamise esmase sünkroonimise juhised](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-entity-map.md).

Veenduge, et topeltkirjutamise puhul oleksid lubatud järgmised tabeli vastendused.

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

- [Power Appsi portaalide dokumentatsioon](/powerapps/maker/portals/overview)
- [Topeltkirjutuse dokumentatsioon](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

Portaalide tõhusaks haldamiseks peate mõistma Power Appsi portaalide ja Microsoft Dataverse'i töötsüklit. Lisateavet vt järgmistest allikatest.

- [Portaali töötsükkel](/powerapps/maker/portals/admin/portal-lifecycle)
- [Portaali uuendamine](/powerapps/maker/portals/admin/upgrade-portal)
- [Portaali konfiguratsiooni migreerimine](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Lahenduse töötsükli haldus: Dynamics 365 for Customer Engagementi rakendused](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]