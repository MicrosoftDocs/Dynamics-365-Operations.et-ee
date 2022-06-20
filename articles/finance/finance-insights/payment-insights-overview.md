---
title: Kliendimaksete prognoosimine
description: See artikkel kirjeldab makseprognooside võimalusi, mis aitab teil paremini mõista kliendi makseviise. Funktsioon aitab teil tuvastada asjaolud, mis peaksid kaasa tooma sissenõudmisprotsesside alustamise varem, kui te oleksite seda muidu teinud.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 5d16b42b4538a18ca3dd9d3bac25ed1af1441ace
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903156"
---
# <a name="customer-payment-predictions"></a>Kliendimaksete prognoosimine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab makseprognooside võimalusi, mis aitab teil paremini mõista kliendi makseviise. Funktsioon aitab teil tuvastada asjaolud, mis peaksid kaasa tooma sissenõudmisprotsesside alustamise varem, kui te oleksite seda muidu teinud.

## <a name="overview"></a>Ülevaade

Organisatsioonidel on tihti raske ennustada, millal kliendid oma arved ära maksavad. Ülevaate puudumine võib tuua kaasa järgmised probleemid.

- Vähem täpsemad rahavoogude prognoosid
- Sissenõudmise protsessid, mis algavad liiga hilja
- Tellimused vabastatakse klientidele, kes ei pruugi maksta

Kliendi makseprognoosid aitavad organisatsioonidel prognoosida, millal kliendiarve tasutakse. Seetõttu saavad nad luua sissenõudmisstrateegiaid, mis aitavad suurendada tõenäosust, et neile makstakse õigeaegselt.

## <a name="predictions"></a>Ennustused

Makseprognoosid võimaldavad organisatsioonidel oma äriprotsesse parandada, aidates neil tuvastada arveid, mida võidakse maksta hilinemisega. Organisatsioon saab seda teavet kasutada selliste toimingute sooritamiseks, mis parandavad õigeaegselt maksmise tõenäosust.

Kliendi makseprognooside funktsioon kasutab masinõppemudelit, et täpsemalt ennustada, millal klient tasub tasumata arve. See masinõppemudel sisaldab ajaloolisi arveid, makseid ja kliendi andmeid.

Iga avatud arve puhul määrab funktsioon kolm makse tõenäosust.

- Tõenäosus, et makse tehakse õigeaegselt
- Tõenäosus, et makse tehakse hilinemisega
- Tõenäosus, et makse tehakse suure hilinemisega

Funktsioon sisaldab ka oodatavate maksete summeeritud vaadet.

[![Maksete ennustuste koondvaade.](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Igale arvele määratakse õigeaegselt maksmise tõenäosus. Arved, mille õigeaegselt maksmise tõenäosus on väiksem kui 50%, märgistatakse punase ringiga näitamaks, et arved võivad vajada inkassaatori tähelepanu.

[![Maksetõenäosuste loend.](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Kliendimaksete prognooside funktsioon pakub ka kontekstilist teavet prognoosi selgitamiseks. See teave sisaldab peamisi tegureid, mis mõjutasid prognoosi, praegust äritegevuse seisu kliendiga ja üksikasju kliendi ajaloolise maksekäitumise kohta.

Paljudes ettevõtetes on sissenõudmisprotsess olnud reaktiivne tegevus. Teisisõnu ei käivitu sissenõudmisprotsess enne arvete maksetähtaja saabumist. Kliendi maksete prognooside abil saavad organisatsioonid olla sissenõudmise osas palju proaktiivsemad. Nad ei pea enam sissenõudmisprotsessi alustamiseks ootama, kuni saabub ülekande tähtaeg. Selle asemel saavad nad kasutada makse prognoosimise võimekust, et teha kindlaks, kas proaktiivne sissenõudmine parandab õigeaegselt tasumise tõenäosust.

## <a name="methodology"></a>Metoodika

Minevikus on tehisintellektiga (AI) lahendust olnud keeruline arendada ja kasutusele võtta. Selleks protsessiks on olnud vaja meeskonda andmeteadlastest, valdkonna asjatundjatest ja inseneridest, kes teevad ületunde, et sõnastada, arendada, kasutada ja hallata kasutatavat tehisintellekti lahendust. Kliendi makseennustused lihtsustavad AI lahenduse juurutamist ja kasutamist Microsoft Dynamics 365 Finances. Microsoft on Microsofti üles ehitatud eelpakkimis-AI lahendused AI Builder. Seetõttu saavad kasutajad kasutada AI lahendust ühe hiireklõpsuga, et kasutada ära intelligentsete prognooside eeliseid. Kui te pole prognooside täpsusega rahul, saab võimsuse kasutaja (ühe hiireklõpsuga) AI Builder uuesti sisestada laienduse kogemuse ja seejärel valida või tühjendada prognooside loomiseks kasutatavad väljad. Kui olete valmis, saate mudelit "koolitada" ja muudatused avaldada. Dynamics 365 Finance prognooside loomiseks komplektetakse automaatselt just valitud mudel.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
