---
title: "Transpordihalduse ülevaade"
description: "Selles teemas antakse ülevaade transpordihalduse funktsioonidest rakenduses Microsoft Dynamics 365 for Operations."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 3136fd95c4c56495a391668d6c854a6ae1e36479
ms.lasthandoff: 03/31/2017


---

# <a name="transportation-management-overview"></a>Transpordihalduse ülevaade

Selles teemas antakse ülevaade transpordihalduse funktsioonidest rakenduses Microsoft Dynamics 365 for Operations.

Moodul Transpordihaldus võimaldab hallata ettevõtte transporti ning tuvastada ka hankijat ja marsruudilahendusi nii sissetulevate kui ka väljaminevate tellimuste puhul. Näiteks saate tuvastada kiireima marsruudi või soodsaima transpordihinna. Järgmine tabel kirjeldab peamisi stsenaariume transpordihalduse kasutamiseks rakenduses Microsoft Dynamics 365 for Operations.

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

## <a name="planning-transportation-in-dynamics-365-for-operations"></a>Transpordi plaanimine rakenduses Dynamics 365 for Operations
Transpordihalduse moodulis võib transpordi plaanimine põhineda tellimustel või saadetistel, mis nende tellimuste põhjal luuakse. Saadetised on alati mingil ajahetkel olemas, kuid neid pole transpordi plaanimiseks vaja. Üleviimistellimused kuuluvad väljamineva transpordi stsenaariumi ja neid saab plaanida koos müügitellimustega. 

![Koormus joonis](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a>Sissetulev transport
Kui tellite hankijalt, kaubad tuleb tarnida lao, võiksite korraldada kaupade transpordi ise. Saate planeerida transpordi ja sissetuleva koormuse saamist Dynamics 365 toiminguteks. Järgmisel joonisel on näidatud äriprotsessi voog sissetuleva koorma transpordi planeerimiseks. 

![Äriprotsessi voog sissetulevate koormate transportimiseks](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a>Väljaminev transport
Saate planeerida ja töödelda väljaminevat koormat konkreetsete kaupade saatmiseks ettevõtte laost kliendile. Saate kasutada rakendust Dynamics 365 for Operations väljamineva koorma transportimise ja vedamise plaanimiseks. Järgmisel joonisel on näidatud äriprotsessi voog väljaminevate koormate planeerimiseks ja töötlemiseks. 

![Planeerimine ja töötlemise väljaminev](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a>Koorma koostamine
Dynamics 365 for Operations pakub koorma koostamise strateegiat, mille nimi on Mahupõhine koorma koostamise strateegia. See strateegia võimaldab kasutada koorma mallil kõrguse ja kaalu kohta määratud maksimumväärtusi või alistada sätted, sisestades uusi väärtusi. Selle strateegia kasutamiseks valige see väljalt **Koorma koostamise strateegia** kiirkaardil **Seadistus** lehel **Koorma koostamise töölaud**. Lisaks saate lisada oma koorma koostamise strateegiaid, luues rakendusobjektide puul (AOT) uue klassi.


