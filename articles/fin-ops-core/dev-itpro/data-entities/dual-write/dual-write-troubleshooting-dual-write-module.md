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
ms.openlocfilehash: f99f3760e75ec1bbf2ccdea497cf2eec3e28e233
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997370"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>Topeltkirjutuse mooduli tõrkeotsingu probleemid Finance and Operationsi rakendustes

[!include [banner](../../includes/banner.md)]

See teema annab teavet rakendustekomplekti Finance and Operations ja Common Data Service’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta. Täpsemalt annab see teema tõrkeotsingu teavet, mis aitab lahendada Finance and Operationsi rakenduste **Topelkirjutuse** mooduliga seotud probleeme.

> [!IMPORTANT]
> Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat. Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Te ei saa laadida topeltkirjutuse moodulit Finance and Operationsi rakenduses

Kui te ei saa avada lehte **Topeltkirjutus** , valides tööruumis **Andmehaldus** paani **Topeltkirjutus** , on andmete integratsiooni teenus tõenäoliselt maas. Looge tugiteenusepilet andmete integratsiooni teenuse taaskäivitamise taotlemiseks.

## <a name="error-when-you-try-to-create-a-new-entity-map"></a>Tõrge uue üksuse vastenduse loomise katsel

**Probleemi lahendamiseks nõutav identimisteave:** sama kasutaja, kes topeltkirjutuse seadistas.

Teile võidakse kuvada järgmine tõrketeade, kui proovite konfigureerida uut üksust topeltkirjutuse jaoks. Vastendust võib luua ainult kasutaja, kes seadistas topeltkirjutuse ühenduse.

*Vastuse oleku kood ei näita edu: 401 (autoriseerimata)*


## <a name="error-when-you-open-the-dual-write-user-interface"></a>Tõrge topeltkirjutuse kasutajaliidese avamisel

Teile võidakse kuvada järgmine tõrketeade, kui püüate tööruumist **Andmehaldus** topeltkirjutusele juurde pääseda.

*login.microsoftonline.com keeldus ühenduse loomisest.*

Probleemi lahendamiseks logige sisse Microsoft Edge InPrivate-aknas, Chromiumi inkognito-aknas või Google Chrome'i inkognito-aknas. Samuti peate kolmanda osapoolte küpsiste blokeerimise tühistama või tühjendama.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a>Tõrge keskkonna linkimisel topeltkirjutusega või uue üksuse vastendamisel

**Probleemi lahendamiseks nõutav roll:** nii Finance and Operationsi rakenduste kui ka teenuse Common Data Service süsteemiadministraator.

Vastenduste linkimisel või loomisel võib ilmneda järgmine tõrge.

*Vastuse oleku kood ei näita edu: 403 (tokenexchange).<br> Seansi ID: \<your session id\><br> Juurtegevuse ID: \<your root activity id\>*

See tõrge võib ilmneda juhul, kui teil pole topeltkirjutuse või vastenduste loomiseks piisavaid lube. See tõrge võib ilmneda ka siis, kui teenuse Common Data Service keskkond lähtestati ilma topeltkirjutuse linkimist tühistamata. Keskkondi saavad linkida kõik kasutajad, kes on süsteemiadministraatorid nii Finance and Operationsi rakendustes kui ka teenuses Common Data Service. Uusi üksuse vastendusi saavad lisada ainult kasutajad, kes seadistasid topeltkirjutuse ühenduse. Pärast seadistamist saab iga süsteemiadministraatori rolliga kasutaja olekut jälgida ja vastendusi redigeerida.

## <a name="error-when-you-stop-the-entity-mapping"></a>Tõrge üksuse vastendamise peatamisel

Kui proovite peatada vastendust, võidakse kuvada järgmine tõrketeade.

*\[Keelatud\], \[{„olek”:403,„allikas”:„”,„sõnum”:„Loa vahetuse tõrge: kasutajal pole juurdepääsu ühendusele dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx”}\], Kaugserver tagastas tõrke: (403) keelatud.*

See tõrge ilmneb siis, kui lingitud Common Data Service'i keskkond ei ole saadaval.

Probleemi lahendamiseks looge andmeintegratsiooni meeskonnale pilet. Manustage võrgujälitus, et andmeintegratsiooni meeskond saaks märgistada vastendused olekusse **Ei tööta** tagaserveris.

## <a name="error-while-trying-to-start-an-entity-mapping"></a>Üksuse vastendamise alustamise katsel ilmnes tõrge

Kui proovite seada vastenduse olekut väärtusele **Töötab** , võite saada järgmise tõrketeate.

*Esialgset andmete sünkroonimist ei saa lõpule viia. Tõrge: topeltkirjutuse tõrge – lisandmooduli registreerimine nurjus: topeltkirjutuse otsingu metaandmete koostamine pole võimalik. Tõrkeobjekti viide pole seatud objekti eksemplarile.*

Selle tõrke parandus sõltub tõrke põhjusest.

+ Kui vastendusel on sõltuvaid vastendusi, siis veenduge, et selle üksuse vastendusest sõltuvad vastendused oleksid lubatud.
+ Vastendusel võivad puududa lähte- või sihtväljad. Kui väli on puudu Finance and Operationsi rakenduses, järgige jaotises [Puuduva üksuse välja probleem vastendusel](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps) toodud samme. Kui väli on puudu teenuses Common Data Service, klõpsake vastendusel nuppu **Värskenda üksuseid** , et väljad täidetaks vastenduses automaatselt.
