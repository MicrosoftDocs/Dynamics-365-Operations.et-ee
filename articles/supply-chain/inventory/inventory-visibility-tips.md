---
title: Varude nähtavuse näpunäideed
description: Käesolevas teemas antakse mõned näpunäideed, mida peaksite kaaluma varude nähtavuse lisandmooduli häälestamisel ja kasutamisel.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: f5fb4c7cb941b352bbc6e2fcf5347244e1c8a40c
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920851"
---
# <a name="inventory-visibility-tips"></a>Varude nähtavuse näpunäideed

[!include [banner](../includes/banner.md)]

Siin on mõned näpunäideed, mida peaksite arvestama varude nähtavuse lisandmooduli häälestamisel ja kasutamisel.

- Praegu toetab varude nähtavuse lisandmoodul ainult keskkondi, mis loodi elutsükli Microsoft Dataverse Microsoft Dynamics teenuste (LCS) abil. Kui teie keskkond on loodud mõnel muul viisil (nt halduskeskuse abil) ja kui see on teie keskkonnaga lingitud, peate esmalt paluma lao nähtavuse tootemeeskonnal vastendamise probleemi Dataverse Power AppsDynamics 365 Supply Chain Management lahendada. Saate võtta töörühmaga ühendust [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com). Meeskond annab teile teada, millal teie keskkond on valmis varude nähtavuse installima.
- Kui teil on rohkem kui üks LCS-keskkond, looge iga Azure Active Directory keskkonna Azure AD jaoks erinev () rakendus. Kui kasutate sama rakenduse ID-d ja rentniku ID-d varude nähtavuse lisandmooduli installimiseks erinevates keskkondades, ilmneb loa probleem vanemates keskkondades. Kehtib ainult installitud varude nähtavuse lisandmooduli viimane eksemplar.
- Varude nähtavust ei toetata praegu pilve majutatud keskkondades. Seda toetatakse ainult Tier-2+ keskkondades.
- Rakendusliides (API) toetab praegu kuni 100 üksiku kauba `ProductID` väärtusepäringut. Iga `SiteID` päringu puhul saab määrata ka mitu `LocationID` väärtust. Maksimaalne limiit on määratletud kui `NumOf(SiteID) * NumOf(LocationID) <= 100`.
- Andmeallikas `fno` on reserveeritud tarneahela haldamiseks. Kui varude nähtavuse lisandmoodul on integreeritud tarneahela halduskeskkonnaga, on soovitatav mitte kustutada andmeallikaga `fno` seotud [konfiguratsioone](inventory-visibility-configuration.md#data-source-configuration).
- Sektsiooni [konfiguratsioon koosneb praegu kahest](inventory-visibility-configuration.md#partition-configuration) põhidimensioonist `SiteId` (ja ), mis `LocationId` näitavad, kuidas andmeid jaotatakse. Sama sektsiooni toimingutega saab madalama hinnaga jõudlust parandada. Lahendus sisaldab vaikimisi seda sektsiooni konfiguratsiooni. Seetõttu *ei pea te seda ise määratlema*. Ärge kohandage sektsiooni vaikekonfiguratsiooni. Selle kustutamisel või muutmisel võib põhjustada ootamatu tõrge.
- Sektsiooni konfiguratsioonis määratletud alusdimensioone ei tohi määratleda tooteindeksi [hierarhia konfiguratsioonis.](inventory-visibility-configuration.md#index-configuration)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
