---
title: Transpordihalduse ülevaade
description: See artikkel annab ülevaate transpordihalduse funktsioonidest tarneahela halduses.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench, TMSLoadBuildTemplateApply, WHSLoadTemplate, TMSTransportationStatus, TMSLoadSeal, TMSLoadBuildProposal, TMSLoadBuildWorkbench, TMSLoadBuildStrategy, TMSLoadBuildStrategyAttributeValue
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "30251"
- intro-internal
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 12f870c95f28e752c3c3b3dd4161d82815b9954a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897454"
---
# <a name="transportation-management-overview"></a>Transpordihalduse ülevaade

[!include [banner](../includes/banner.md)]

See artikkel annab ülevaate transpordihalduse funktsioonidest tarneahela halduses.

Moodul Transpordihaldus võimaldab kasutada ettevõtte transporti ning tuvastada ka hankijat ja marsruudilahendusi nii sissetulevate kui ka väljaminevate tellimuste puhul. Näiteks saate tuvastada kiireima marsruudi või soodsaima transpordihinna. Järgmine tabel kirjeldab peamisi stsenaariume transpordihalduse kasutamiseks.

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

## <a name="planning-transportation-in-supply-chain-management"></a>Transpordi plaanimine rakenduses Supply Chain Management
Transpordihalduse moodulis võib transpordi plaanimine põhineda tellimustel või saadetistel, mis nende tellimuste põhjal luuakse. Saadetised on alati mingil ajahetkel olemas, kuid neid pole transpordi plaanimiseks vaja. Üleviimistellimused kuuluvad väljamineva transpordi stsenaariumi ja neid saab plaanida koos müügitellimustega. 

![Koorma joonis.](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a>Sissetulev transport
Kui tellite hankijalt tellimuse kaubad ja kaubad tuleb lattu tarnida, peate soovi korral ise kaupade transpordi korraldama. Rakendust Supply Chain Management saab kasutada transpordi ja sissetuleva koorma vastuvõtmise plaanimiseks. Järgmisel joonisel on näidatud äriprotsessi voog sissetuleva koorma transpordi planeerimiseks. 

![Äriprotsessi voog sissetulevate koormate transportimiseks.](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a>Väljaminev transport
Saate planeerida ja töödelda väljaminevat koormat konkreetsete kaupade saatmiseks ettevõtte laost kliendile. Saate kasutada rakendust Supply Chain Management väljamineva koorma transportimise ja vedamise plaanimiseks. Järgmisel joonisel on näidatud äriprotsessi voog väljaminevate koormate planeerimiseks ja töötlemiseks. 

![Väljaminevate koormate plaanimine ja töötlemine.](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a>Koorma koostamine
Supply Chain Management pakub koorma koostamise strateegiat, mille nimi on Mahupõhine koorma koostamise strateegia. See strateegia võimaldab kasutada koorma mallil kõrguse ja kaalu kohta määratud maksimumväärtusi või alistada sätted, sisestades uusi väärtusi. Selle strateegia kasutamiseks valige see väljalt **Koorma koostamise strateegia** kiirkaardil **Seadistus** lehel **Koorma koostamise töölaud**. Lisaks saate lisada oma koorma koostamise strateegiaid, luues rakendusobjektide puul (AOT) uue klassi.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]