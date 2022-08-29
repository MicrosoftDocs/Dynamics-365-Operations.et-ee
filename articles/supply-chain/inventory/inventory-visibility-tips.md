---
title: Inventory Visibility nõuanded
description: See artikkel annab mõned näpunäideed, mida peaksite arvestama, kui seadistate ja kasutate varude nähtavuse lisandmoodulit.
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
ms.openlocfilehash: 3bdd161815a15d5c39b3c0afc176a288c8d9055a
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306081"
---
# <a name="inventory-visibility-tips"></a>Inventory Visibility nõuanded

[!include [banner](../includes/banner.md)]

Siin on mõned näpunäideed, mida peaksite arvestama varude nähtavuse lisandmooduli häälestamisel ja kasutamisel.

- Praegu toetab varude nähtavuse lisandmoodul ainult keskkondi Microsoft Dataverse, mis Microsoft Dynamics loodi elutsükli teenuste (LCS) abil. Kui teie Dataverse keskkond on loodud mõnel muul viisil (Power Apps nt halduskeskuse abil) Dynamics 365 Supply Chain Management ja kui see on teie keskkonnaga lingitud, peate esmalt paluma lao nähtavuse tootemeeskonnal vastendamise probleemi lahendada. Töörühmaga saate ühendust inventvisibilitysupp@microsoft.com [...](mailto:inventvisibilitysupp@microsoft.com). Meeskond annab teile teada, millal teie keskkond on valmis varude nähtavuse installima.
- Kui teil on rohkem kui üks LCS keskkond, looge iga Azure Active Directory keskkonna jaoks erinev (Azure AD) rakendus. Kui kasutate sama rakenduse ID-d ja rentniku ID-d varude nähtavuse lisandmooduli installimiseks erinevates keskkondades, ilmneb loa probleem vanemates keskkondades. Kehtib ainult installitud varude nähtavuse lisandmooduli viimane eksemplar.
- Varude nähtavust ei toetata praegu pilve majutatud keskkondades. Seda toetatakse ainult Tier-2+ keskkondades.
- Rakendusliides (API) toetab praegu kuni 100 üksiku kauba väärtusepäringut `ProductID`. Iga `SiteID` päringu `LocationID` puhul saab määrata ka mitu väärtust. Maksimaalne limiit on määratletud kui `NumOf(SiteID) * NumOf(LocationID) <= 100`.
- Hulgi-API saab tagastada maksimaalselt 512 kirjet iga taotluse kohta.
- Andmeallikas `fno` on reserveeritud tarneahela haldamiseks. Kui varude nähtavuse lisandmoodul on integreeritud tarneahela halduskeskkonnaga, on soovitatav mitte kustutada andmeallikaga `fno` seotud [konfiguratsioone](inventory-visibility-configuration.md#data-source-configuration).
- Varude nähtavus ei saa muuta andmeallika `fno` andmeid. Andmevoog on ühene viis, mis tähendab `fno`, et kõik andmeallika koguse muudatused peavad tulema teie tarneahela halduse keskkonnast. Seetõttu ei saa te API-d kasutada andmeallikale vaba kaubavaru muudatuse või reserveerimise `fno` taotluste saatmiseks.
- Kui lisate tarneahela halduse keskkonda veel ühe või mitu uut dimensioone, peate need lisama ka varude nähtavuse aknas. Kõik uute jne kogused peavad siiski tulema teie tarneahela halduskeskkonnast.
- Sektsiooni [konfiguratsioon koosneb](inventory-visibility-configuration.md#partition-configuration) praegu kahest põhidimensioonist (`SiteId` ja `LocationId`), mis näitavad, kuidas andmeid jaotatakse. Sama sektsiooni toimingutega saab madalama hinnaga jõudlust parandada. Lahendus sisaldab vaikimisi seda sektsiooni konfiguratsiooni. Seetõttu ei *pea te seda ise määratlema*. Ärge kohandage sektsiooni vaikekonfiguratsiooni. Selle kustutamisel või muutmisel võib põhjustada ootamatu tõrge.
- Sektsiooni konfiguratsioonis määratletud põhidimensioone ei tohi määratleda tooteindeksi [hierarhia konfiguratsioonis](inventory-visibility-configuration.md#index-configuration).
- Teie [tooteindeksi](inventory-visibility-configuration.md#index-configuration) hierarhia konfiguratsioon peab sisaldama vähemalt ühte indeksihierarhiat (`Empty` näiteks põhidimensiooni sisaldavat) muidu nurjuvad päringud tõrkega "Indekshierarhiat pole seatud."
- Andmeallikas on `@iv` eelmääratletud andmeallikas ja eesliitega määratletud füüsilised `@iv``@` koormused on eelmääratletud andmed. Need arvud on eraldamisfunktsiooni jaoks eelmääratletud konfiguratsioon, nii et ärge muutke ega kustutage neid või ilmneb eraldamisfunktsiooni kasutades ootamatuid tõrkeid.
- Saate lisada eelmääratletud arvutatud mõõtu uusi `@iv.@available_to_allocate` füüsilisi mõõte, kuid te ei tohi selle nime muuta.
- Kui taastate tarneahela halduse andmebaasi, võib taastatud andmebaas sisaldada andmeid, mis ei ole enam kooskõlas eelnevalt varude nähtavuse kaudu sünkroonitud andmetega Dataverse. Nende andmete vastuolud võivad põhjustada süsteemitõrkeid ja muid probleeme. Seetõttu on oluline enne tarneahela Dataverse halduse andmebaasi taastamist alati puhastada kõik seotud varude nähtavuse andmed. Üksikasju vt jaotisest [Varude nähtavuse andmete puhastamine Dataverse enne tarneahela halduse andmebaasi taastamist](inventory-visibility-setup.md#restore-environment-database).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
