---
title: Finance and Operationsi rakendustes topeltirjutuse mooduliga seotud probleemide tõrkeotsing
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172756"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>Finance and Operationsi rakendustes topeltirjutuse mooduliga seotud probleemide tõrkeotsing

[!include [banner](../../includes/banner.md)]



See teema annab teavet rakendustekomplekti Finance and Operations ja Common Data Service’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta. Täpsemalt annab see teema tõrkeotsingu teavet, mis aitab lahendada Finance and Operationsi rakenduste **Topelkirjutuse** mooduliga seotud probleeme.

> [!IMPORTANT]
> Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat. Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Te ei saa laadida topeltkirjutuse moodulit rakendusse Finance and Operations

Kui te ei saa avada lehte **Topeltkirjutus**, valides tööruumis **Andmehaldus** paani **Topeltkirjutus**, on andmete integratsiooni teenus tõenäoliselt maas. Looge tugiteenusepilet andmete integratsiooni teenuse taaskäivitamise taotlemiseks.

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a>Tõrge uue üksuse vastenduse loomise katsel

**Probleemi lahendamiseks nõutav mandaat:** Azure AD rentniku admin

Teile võidakse kuvada järgmine tõrketeade, kui proovite konfigureerida uut üksust topeltkirjutuse jaoks.

*Vastuse oleku kood ei näita edu: 401 (autoriseerimata)*

See tõrge ilmneb, sest ainult Azure AD rentniku administraator saab lisada uue üksuse vastendamist.

Probleemi lahendamiseks logigesisse rakendusse Finance and Operations kui Azure AD administraatori rentnik. Peate minema lehele web.PowerApps.com ja kinnitama ühenduse uuesti.

## <a name="error-when-you-open-the-dual-write-user-interface"></a>Tõrge topeltkirjutuse kasutajaliidese avamisel

Teile võidakse kuvada järgmine tõrketeade, kui püüate tööruumist **Andmehaldus** topeltkirjutusele juurde pääseda.

*login.microsoftonline.com keeldus ühenduse loomisest.*

Probleemi lahendamiseks logige sisse Microsoft Edge InPrivate-aknas, Chromiumi inkognito-aknas või Google Chrome'i inkognito-aknas. Samuti peate kolmanda osapoolte küpsiste blokeerimise tühistama või tühjendama.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a>Tõrge keskkonna linkimisel topeltkirjutusega või uue üksuse vastendamisel

**Probleemi lahendamiseks nõutav mandaat:** Azure AD rentniku admin

Vastenduste linkimisel või loomisel võib ilmneda järgmine tõrge.

*Vastuse oleku kood ei näita edu: 403 (tokenexchange).<br> Seansi ID: \<teie seansi ID\><br> Juurtegevuse ID: \<teie juurtegevuse ID\>*

See tõrge võib ilmneda juhul, kui teil pole topeltkirjutuse või vastenduste loomiseks piisavaid lube. Keskkondade linkimiseks ja uute üksuste vastenduste lisamiseks peate kasutama Azure AD rentniku administraatorikontot. Kuid pärast häälestust saate kasutada mitte-administraatori kontot oleku jälgimiseks ja vastenduste redigeerimiseks.

## <a name="error-when-you-stop-the-entity-mapping"></a>Tõrge üksuse vastendamise peatamisel

Kui proovite peatada vastendust, võidakse kuvada järgmine tõrketeade.

*\[Keelatud\], \[{„olek”:403,„allikas”:„”,„sõnum”:„Loa vahetuse tõrge: kasutajal pole juurdepääsu ühendusele dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx”}\], Kaugserver tagastas tõrke: (403) keelatud.*

See tõrge ilmneb siis, kui lingitud Common Data Service'i keskkond ei ole saadaval.

Probleemi lahendamiseks looge andmeintegratsiooni meeskonnale pilet. Manustage võrgujälitus, et andmeintegratsiooni meeskond saaks märgistada vastendused olekusse **Ei tööta** tagaserveris.
