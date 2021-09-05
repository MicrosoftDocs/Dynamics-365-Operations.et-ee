---
title: Kliendimaksete prognoosimine
description: Selles teemas kirjeldatakse makse prognooside võimalust, mis aitab klientide tüüpilisi maksetavasid paremini mõista. Funktsioon aitab teil tuvastada asjaolud, mis peaksid kaasa tooma sissenõudmisprotsesside alustamise varem, kui te oleksite seda muidu teinud.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 21a773b37020aeff969469e29be68e7f7ef44d93
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386657"
---
# <a name="customer-payment-predictions"></a>Kliendimaksete prognoosimine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse makse prognooside võimalust, mis aitab klientide tüüpilisi maksetavasid paremini mõista. Funktsioon aitab teil tuvastada asjaolud, mis peaksid kaasa tooma sissenõudmisprotsesside alustamise varem, kui te oleksite seda muidu teinud.

## <a name="overview"></a>Ülevaade

Organisatsioonidel on tihti raske ennustada, millal kliendid oma arved ära maksavad. Ülevaate puudumine võib tuua kaasa järgmised probleemid.

- Vähem täpsemad rahavoogude prognoosid
- Sissenõudmise protsessid, mis algavad liiga hilja
- Tellimused vabastatakse klientidele, kes ei pruugi maksta

Kliendi makse prognoosid (eelversioon) aitab organisatsioonidel ennustada, millal kliendi arve tasutakse. Seetõttu saavad nad luua sissenõudmisstrateegiaid, mis aitavad suurendada tõenäosust, et neile makstakse õigeaegselt.

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

Minevikus on tehisintellektiga (AI) lahendust olnud keeruline arendada ja kasutusele võtta. Selleks protsessiks on olnud vaja meeskonda andmeteadlastest, valdkonna asjatundjatest ja inseneridest, kes teevad ületunde, et sõnastada, arendada, kasutada ja hallata kasutatavat tehisintellekti lahendust. Kliendi maksete prognoosid hõlbustavad AI lahenduse rakendamist ja kasutamist lahenduses Microsoft Dynamics 365 Finance. Microsoft paneb kaasa AI lahendused, mis on ehitatud Microsoft AI Builderi peale. Seetõttu saavad kasutajad kasutada AI lahendust ühe hiireklõpsuga, et kasutada ära intelligentsete prognooside eeliseid. Kui te ei ole ennustuste täpsusega rahul, saab lauskasutaja taas ühe nupuvajutusega siseneda AI Builderi laienduskogemusse ja seejärel valida või tühistada nende väljade valiku, mida kasutatakse ennustuste loomiseks. Kui olete valmis, saate mudelit "koolitada" ja muudatused avaldada. Äsja koolitatud prognoosimismudel võetakse kasutusele lahenduses Dynamics 365 Finance prognooside loomiseks.

## <a name="release-details"></a>Väljastuse üksikasjad

Finantsülevaadete avalik eelversioon on kasutuselevõtu proovimiseks saadaval Ameerika Ühendriikides, Euroopas ja Ühendkuningriigis. Microsoft lisab astmeliselt juurde täiendavate piirkondade tuge.

Avaliku eelvaate funktsioone saab ja tuleb sisse lülitada ainult Järgu 2 liivakasti keskkondades. Liivakasti keskkonnas loodud seadistust ja AI mudeleid ei pruugi saada migreerida töökeskkonda. Lisateavet leiate teemast [Microsoft Dynamics 365 eelversioonide täiendavad kasutustingimused](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
