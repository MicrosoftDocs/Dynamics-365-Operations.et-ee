---
title: Topeltkirjutuse mooduli tõrkeotsingu probleemid Finance and Operationsi rakendustes
description: Selles teemas antakse tõrkeotsingu teavet, mis aitab lahendada Finance and Operationsi rakenduste topelkirjutuse mooduliga seotud probleeme.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2241e7e6219f95115f55bc45a4d94550276e1e21
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683619"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>Topeltkirjutuse mooduli tõrkeotsingu probleemid Finance and Operationsi rakendustes

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

See teema annab teavet rakendustekomplekti Finance and Operations ja Dataverse’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta. Täpsemalt annab see teema tõrkeotsingu teavet, mis aitab lahendada Finance and Operationsi rakenduste **Topelkirjutuse** mooduliga seotud probleeme.

> [!IMPORTANT]
> Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat. Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Te ei saa laadida topeltkirjutuse moodulit Finance and Operationsi rakenduses

Kui te ei saa avada lehte **Topeltkirjutus**, valides tööruumis **Andmehaldus** paani **Topeltkirjutus**, on andmete integratsiooni teenus tõenäoliselt maas. Looge tugiteenusepilet andmete integratsiooni teenuse taaskäivitamise taotlemiseks.

## <a name="error-when-you-try-to-create-a-new-table-map"></a>Tõrge uue tabeli vastenduse loomise katsel

**Probleemi lahendamiseks nõutav identimisteave:** sama kasutaja, kes topeltkirjutuse seadistas.

Teile võidakse kuvada järgmine tõrketeade, kui proovite konfigureerida uut üksust topeltkirjutuse jaoks. Vastendust võib luua ainult kasutaja, kes seadistas topeltkirjutuse ühenduse.

*Vastuse oleku kood ei näita edu: 401 (autoriseerimata)*


## <a name="error-when-you-open-the-dual-write-user-interface"></a>Tõrge topeltkirjutuse kasutajaliidese avamisel

Teile võidakse kuvada järgmine tõrketeade, kui püüate tööruumist **Andmehaldus** topeltkirjutusele juurde pääseda.

*login.microsoftonline.com keeldus ühenduse loomisest.*

Probleemi lahendamiseks logige sisse Microsoft Edge InPrivate-aknas, Chromiumi inkognito-aknas või Google Chrome'i inkognito-aknas. Samuti peate kolmanda osapoolte küpsiste blokeerimise tühistama või tühjendama.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>Tõrge keskkonna linkimisel topeltkirjutusega või uue tabeli vastendamisel

**Probleemi lahendamiseks nõutav roll:** nii Finance and Operationsi rakenduste kui ka teenuse Dataverse süsteemiadministraator.

Vastenduste linkimisel või loomisel võib ilmneda järgmine tõrge.

*Vastuse oleku kood ei näita edu: 403 (tokenexchange).<br> Seansi ID: \<your session id\><br> Juurtegevuse ID: \<your root activity id\>*

See tõrge võib ilmneda juhul, kui teil pole topeltkirjutuse või vastenduste loomiseks piisavaid lube. See tõrge võib ilmneda ka siis, kui teenuse Dataverse keskkond lähtestati ilma topeltkirjutuse linkimist tühistamata. Keskkondi saavad linkida kõik kasutajad, kes on süsteemiadministraatorid nii Finance and Operationsi rakendustes kui ka teenuses Dataverse. Uusi tabeli vastendusi saavad lisada ainult kasutajad, kes seadistasid topeltkirjutuse ühenduse. Pärast seadistamist saab iga süsteemiadministraatori rolliga kasutaja olekut jälgida ja vastendusi redigeerida.

## <a name="error-when-you-stop-the-table-mapping"></a>Tõrge tabeli vastendamise peatamisel

Kui proovite peatada tabeli vastendust, võidakse kuvada järgmine tõrketeade.

*\[Keelatud\], \[{„olek”:403,„allikas”:„”,„sõnum”:„Loa vahetuse tõrge: kasutajal pole juurdepääsu ühendusele dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx”}\], Kaugserver tagastas tõrke: (403) keelatud.*

See tõrge ilmneb siis, kui lingitud Dataverse'i keskkond ei ole saadaval.

Probleemi lahendamiseks looge andmeintegratsiooni meeskonnale pilet. Manustage võrgujälitus, et andmeintegratsiooni meeskond saaks märgistada vastendused olekusse **Ei tööta** tagaserveris.

## <a name="error-while-trying-to-start-an-table-mapping"></a>Tabeli vastendamise alustamise katsel ilmnes tõrge

Kui proovite seada vastenduse olekut väärtusele **Töötab**, võite saada järgmise tõrketeate.

*Esialgset andmete sünkroonimist ei saa lõpule viia. Tõrge: topeltkirjutuse tõrge – lisandmooduli registreerimine nurjus: topeltkirjutuse otsingu metaandmete koostamine pole võimalik. Tõrkeobjekti viide pole seatud objekti eksemplarile.*

Selle tõrke parandus sõltub tõrke põhjusest.

+ Kui vastendusel on sõltuvaid vastendusi, siis veenduge, et selle tabeli vastendusest sõltuvad vastendused oleksid lubatud.
+ Vastendusel võivad puududa lähte- või sihtväljad. Kui väli on puudu Finance and Operationsi rakenduses, järgige jaotises [Puuduva üksuse välja probleem vastendusel](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps) toodud samme. Kui väli on teenuses Dataverse puudu, klõpsake vastendusel nuppu **Värskenda tabeleid**, et väljad täidetaks vastenduses automaatselt.
