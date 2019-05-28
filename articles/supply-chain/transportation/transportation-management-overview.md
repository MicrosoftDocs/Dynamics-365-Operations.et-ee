---
title: Transpordihalduse ülevaade
description: Selles teemas antakse ülevaade transpordihalduse funktsioonist rakenduses Microsoft Dynamics 365 for Finance and Operations.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 918167a3ab72b3d3665cf710d8e509417b94a056
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561153"
---
# <a name="transportation-management-overview"></a>Transpordihalduse ülevaade

[!include [banner](../includes/banner.md)]

Selles teemas antakse ülevaade transpordihalduse funktsioonist rakenduses Microsoft Dynamics 365 for Finance and Operations.

Moodul Transpordihaldus võimaldab kasutada ettevõtte transporti ning tuvastada ka hankijat ja marsruudilahendusi nii sissetulevate kui ka väljaminevate tellimuste puhul. Näiteks saate tuvastada kiireima marsruudi või soodsaima transpordihinna. Järgmine tabel kirjeldab peamisi stsenaariume transpordihalduse kasutamiseks rakenduses Microsoft Dynamics 365 for Finance and Operations.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Stsenaarium</th>
<th>Kuidas transpordihaldus võib abiks olla</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Saate kasutada transporditegevuste puhul väliseid logistikateenuste osutajaid.</td>
<td>Transpordihaldust saab kasutada sissetuleva ja väljamineva transpordi jaoks.</td>
</tr>
<tr class="even">
<td>Ettevõtte enda autopark on kohaletoimetamiseks/pealevõtmiseks kättesaadav ja transpordikulude eest esitatakse arve kliendile.</td>
<td>Väljaminevate protsesside puhul võib kasutada transpordihalduse moodulit transporditasude määratlemiseks ja nende eest klientidele arve esitamiseks. Kuid vedaja arve vastavusseviimise protsessi pole vaja.</td>
</tr>
<tr class="odd">
<td>Ettevõtte oma autopark on kohaletoimetamiseks/pealevõtmiseks kättesaadav, kuid transporditasude eest ei esitata klientidele arveid, kuna transport sisaldub toodete hinnas.</td>
<td>Paljusid transpordihalduse mooduli funktsioone pole vaja. Kuid võite kasutada transpordihaldust transpordihindade määratlemiseks ja müügihinna vastavaks korrigeerimiseks.</td>
</tr>
<tr class="even">
<td>Logistikateenust osutab samas firmas teine juriidiline isik.</td>
<td><ul>
<li>Transpordihaldust saab kasutada, käsitledes teist juriidilist isikut sarnaselt igale muule vedajale. Juriidiliste isikute vahelisi majanduskandeid ei saa automatiseerida. Seetõttu tuleb need kanded käsitsi töödelda (nt luues ostutellimuse).</li>
<li>Logistikateenuseid osutavad juriidilises isikus saab transpordihalduse moodulit kasutada transpordihindade määratlemiseks.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-finance-and-operations"></a>Transpordi plaanimine rakenduses Finance and Operations
Transpordihalduse moodulis võib transpordi plaanimine põhineda tellimustel või saadetistel, mis nende tellimuste põhjal luuakse. Saadetised on alati mingil ajahetkel olemas, kuid neid pole transpordi plaanimiseks vaja. Üleviimistellimused kuuluvad väljamineva transpordi stsenaariumi ja neid saab plaanida koos müügitellimustega. 

![Koorma joonis](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a>Sissetulev transport
Kui tellite hankijalt tellimuse kaubad ja kaubad tuleb lattu tarnida, peate soovi korral ise kaupade transpordi korraldama. Rakendust Finance and Operations saab kasutada transpordi ja sissetuleva koorma vastuvõtmise plaanimiseks. Järgmisel joonisel on näidatud äriprotsessi voog sissetuleva koorma transpordi planeerimiseks. 

![Äriprotsessi voog sissetulevate koormate transportimiseks](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a>Väljaminev transport
Saate planeerida ja töödelda väljaminevat koormat konkreetsete kaupade saatmiseks ettevõtte laost kliendile. Rakendust Finance and Operations saab kasutada transpordi ja väljamineva koorma lähetamise plaanimiseks. Järgmisel joonisel on näidatud äriprotsessi voog väljaminevate koormate planeerimiseks ja töötlemiseks. 

![Väljaminevate koormate plaanimine ja töötlemine](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a>Koorma koostamine
Finance and Operations pakub koorma koostamise strateegiat, mille nimi on Mahupõhine koorma koostamise strateegia. See strateegia võimaldab kasutada koorma mallil kõrguse ja kaalu kohta määratud maksimumväärtusi või alistada sätted, sisestades uusi väärtusi. Selle strateegia kasutamiseks valige see väljalt **Koorma koostamise strateegia** kiirkaardil **Seadistus** lehel **Koorma koostamise töölaud**. Lisaks saate lisada oma koorma koostamise strateegiaid, luues rakendusobjektide puul (AOT) uue klassi.



