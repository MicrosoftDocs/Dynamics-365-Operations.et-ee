---
title: Rakenda mõõtühiku sätted
description: See artikkel hõlmab mõõtühiku sätteid ja kirjeldab nende rakendumist üksuses Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: ca95bd31af8f244f60f12120bc6df121f48cc7ea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884811"
---
# <a name="apply-unit-of-measure-settings"></a>Rakenda mõõtühiku sätted

[!include [banner](includes/banner.md)]

See artikkel hõlmab mõõtühiku sätteid ja kirjeldab nende rakendumist üksuses Microsoft Dynamics 365 Commerce.

Toodet saab müüa erinevates üksustes, näiteks "igaüks", "paar" ja "tosin." Commerce peakorteris saab müügi mõõtühiku määrata tootele ja näidata e-kaubanduse saidil. Näiteks kui jaemüüja müüb toodet nii eraldi kui ka kümnete kaupa, saab saadaolevaid mõõtühikuid näidata koos muu tooteteabega.

Järgmise illustratsiooni näites on üksuse mõõtühik **ea** (iga) Commerce peakorteri toote jaoks konfigureeritud.

![Näide tootest, mis on konfigureeritud mõõtühikuga Commerce peakorteris.](./media/Productunit-headquarters.PNG)

> [!NOTE]
> Mõõtühiku rakendamise ja näitamise tugi on saadaval Commerce versioonis 10.0.19.

## <a name="unit-of-measure-settings"></a>Mõõtühiku sätted

Mõõtühiku kuvasätted määratakse Commerce saidi koostajas jaotises **Saidisätted \> Laiendid \> Kuva toodete mõõtühik**. Toetatud sätteid on kolm:

- **Ära kuva** – Kui see säte on valitud, ei näita e-kaubanduse sait toote mõõtühikuid. See on vaikesäte.
- **Kuva toote ostukogemuses** – Kui see säte on valitud, kuvatakse mõõtühik toote üksikasjades, ostukorvis, tellimuse kinnituses, tellimuste ajaloos ja tellimuse üksikasjade lehtedel.
- **Kuvage toote sirvimise ja ostukogemuse ajal** – Kui see säte on valitud, näidatakse mõõtühikuid toote ostukogemuse lehtedel ja ka toote sirvimise ajal. Osana sellest käitumisest näidatakse mõõtühikuid otsingutulemustes ja tootekogumi moodulites.

> [!IMPORTANT]
> Mõõtühiku kuvasätted on saadaval Commerce versioonis 10.0.19. Kui uuendate rakenduse Commerce'i varasemat versiooni, peate faili appsettings.json käsitsi värskendama. Juhiste saamiseks vt [SDK ja mooduliteegi värskendused](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-unit-of-measure-settings"></a>Mõõtühiku sätteid kasutavad moodulid

Mõõtühiku sätteid kasutavad moodulid hõlmavad ostuboksi, soovinimekirja, ostukorvi, ostukorvi ikooni, otsingutulemuste konteinerit, tootekogumit, tellimuse kinnitust ja tellimuse üksikasju.

Järgmises näites on toote üksikasjade lehel (PDP) kuvatud toote mõõtühik (**ea**).

![Mõõtühikuid näitava PDP näide.](./media/Productunit-PDP.png)

Järgmise illustratsiooni näites näitab tootekogumismoodul toote mõõtühikut (**ea**).

![Mõõtühikuid näitava tootekogumi mooduli näide.](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Ostukorvimoodul](add-cart-module.md)

[Ostukastimoodul](add-buy-box.md)

[Kontohalduse lehed ja moodulid](account-management.md)

[SDK ja mooduliteegi värskendused](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
