---
title: Varude nähtavuse nõuanded
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
ms.openlocfilehash: 1f6ade36ac184a3c8bf790fc0d899ea01d90c8d2
ms.sourcegitcommit: f5fd2122a889b04e14f18184aabd37f4bfb42974
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/10/2022
ms.locfileid: "7952411"
---
# <a name="inventory-visibility-tips"></a>Varude nähtavuse nõuanded

[!include [banner](../includes/banner.md)]

Siin on mõned näpunäideed, mida peaksite arvestama varude nähtavuse lisandmooduli häälestamisel ja kasutamisel.

- Praegu toetab varude nähtavuse lisandmoodul ainult keskkondi, mis loodi elutsükli Microsoft Dataverse Microsoft Dynamics teenuste (LCS) abil. Kui teie keskkond on loodud mõnel muul viisil (nt halduskeskuse abil) ja kui see on teie keskkonnaga lingitud, peate esmalt paluma lao nähtavuse tootemeeskonnal vastendamise probleemi Dataverse Power AppsDynamics 365 Supply Chain Management lahendada. Saate võtta töörühmaga ühendust [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com). Meeskond annab teile teada, millal teie keskkond on valmis varude nähtavuse installima.
- Kui teil on rohkem kui üks LCS-keskkond, looge iga Azure Active Directory keskkonna Azure AD jaoks erinev () rakendus. Kui kasutate sama rakenduse ID-d ja rentniku ID-d varude nähtavuse lisandmooduli installimiseks erinevates keskkondades, ilmneb loa probleem vanemates keskkondades. Kehtib ainult installitud varude nähtavuse lisandmooduli viimane eksemplar.
- Varude nähtavust ei toetata praegu pilve majutatud keskkondades. Seda toetatakse ainult Tier-2+ keskkondades.
- Rakendusliides (API) toetab praegu kuni 100 üksiku kauba `ProductID` väärtusepäringut. Iga `SiteID` päringu puhul saab määrata ka mitu `LocationID` väärtust. Maksimaalne limiit on määratletud kui `NumOf(SiteID) * NumOf(LocationID) <= 100`.
- Hulgi-API saab tagastada maksimaalselt 512 kirjet iga taotluse kohta.
- Andmeallikas `fno` on reserveeritud tarneahela haldamiseks. Kui varude nähtavuse lisandmoodul on integreeritud tarneahela halduskeskkonnaga, on soovitatav mitte kustutada andmeallikaga `fno` seotud [konfiguratsioone](inventory-visibility-configuration.md#data-source-configuration).
- Varude nähtavus ei saa muuta andmeallika `fno` andmeid. Andmevoog on ühene viis, mis tähendab, et kõik andmeallika `fno` koguse muudatused peavad tulema teie tarneahela halduse keskkonnast. Seetõttu ei saa te API-d kasutada andmeallikale vaba kaubavaru muudatuse või reserveerimise `fno` taotluste saatmiseks.
- Kui lisate tarneahela halduse keskkonda veel ühe või mitu uut dimensioone, peate need lisama ka varude nähtavuse aknas. Kõik uute jne kogused peavad siiski tulema teie tarneahela halduskeskkonnast.
- Sektsiooni [konfiguratsioon koosneb praegu kahest](inventory-visibility-configuration.md#partition-configuration) põhidimensioonist `SiteId` (ja ), mis `LocationId` näitavad, kuidas andmeid jaotatakse. Sama sektsiooni toimingutega saab madalama hinnaga jõudlust parandada. Lahendus sisaldab vaikimisi seda sektsiooni konfiguratsiooni. Seetõttu *ei pea te seda ise määratlema.* Ärge kohandage sektsiooni vaikekonfiguratsiooni. Selle kustutamisel või muutmisel võib põhjustada ootamatu tõrge.
- Sektsiooni konfiguratsioonis määratletud alusdimensioone ei tohi määratleda tooteindeksi [hierarhia konfiguratsioonis.](inventory-visibility-configuration.md#index-configuration)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
