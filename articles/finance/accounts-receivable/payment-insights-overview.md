---
title: Kliendimaksete ülevaated (eelvaade)
description: Selles teemas kirjeldatakse makse ülevaadete võimalust, mis aitab parandada üksikute klientide tüüpiliste maksetavade mõistmist. Funktsioon aitab teil tuvastada asjaolud, mis õigustavad sissenõudmisprotsesside alustamist varem, kui te oleksite seda muidu teinud.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: d01f15223b4665caec16d6a4e51a5121a0ed94ea
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012160"
---
# <a name="customer-payment-insights-preview"></a>Kliendimaksete ülevaated (eelvaade)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Selles teemas kirjeldatakse makse ülevaadete võimalust, mis aitab parandada üksikute klientide tüüpiliste maksetavade mõistmist. Funktsioon aitab teil tuvastada asjaolud, mis õigustavad sissenõudmisprotsesside alustamist varem, kui te oleksite seda muidu teinud. 

## <a name="overview"></a>Ülevaade

Võib olla raske ennustada, millal kliendid oma arved ära maksavad. Selle ülevaate puudumine toob kaasa vähem täpset likviidsuse planeerimised, liiga hilja algavad kogumisprotsessid ja tellimused, mis väljastatakse kliendile, kes ei pruugi maksta. Funktsioon Kliendi makse ülevaated (eelversioon) aitab organisatsioonidel ennustada, millal kliendi arve tasutakse. See teave võib aidata organisatsioonidel luua sissenõudmisstrateegiaid, mis parandavad õigeaegselt maksmise tõenäosust. 

## <a name="predictions"></a>Ennustused

Makseennustused võimaldavad organisatsioonidel parandada oma äriprotsesse, aidates neil hõlpsasti tuvastada arveid, mis tõenäoliselt makstakse hilja, ja võtta asjakohaseid meetmeid, mis parandavad nende võimalusi saada õigeaegselt tasutud.

Masinõppe mudelit kasutades, mis kasutab varasemaid arveid, makseid ja kliendiandmeid, ennustab kliendimaksete ülevaated (eelvaade) veelgi täpsemalt, millal klient tasumata arve ära maksab.

Funktsioon Kliendi makse ülevaated (eelversioon) ennustab iga avatud arve jaoks kolme maksetõenäosust.

-   Õigeaegselt maksmise tõenäosus 
-   Makse hilja tegemise tõenäosus
-   Makse väga hilja tegemise tõenäosus

Et aidata organisatsioonidel mõista kogu maksesummat, mida nad võivad kliendilt oodata ühes kolmest vahemikust (õigeaegselt, hilja ja väga hilja), annab Klindi makse ülevaated (eelversioon) ka eeldatavate maksete koondvaate.

[![Maksete ennustuste koondvaade](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Lisaks määratakse igale arvele õigeaegse maksmise tõenäosus. Kui õigeaegselt maksmise tõenäosus on väiksem kui 50%, märgistatakse arved punase ringiga, et näidata need arved võivad vajada kättesaamiseks tähelepanu. 

[![Maksetõenäosuste loend](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Kliendi makse ülevaated (eelvaade) pakub ka ennustuse selgitamiseks konteksti puudutavat teavet, näiteks prognoose mõjutanud peamised tegurid, praegune äritegevuse olukord kliendiga ja üksikasjad seoses kliendi ajaloolise maksekäitumisega. Paljudes ettevõtetes on kogumistoiming reaktiivne tegevus; kogumistoiming ei alga enne, kui saabub arve tähtaeg. 

Kliendi makse ülevaadete (eelvaade) abil saavad organisatsioonid olla kogumiste osas palju proaktiivsemad. Nad ei pea enam kogumisprotsessi alustamiseks ootama, kuni saabub ülekande tähtaeg. Selle asemel saavad nad kasutada makse prognoosimise võimekust, et teha kindlaks, kas proaktiivne kogumine parandab õigeaegselt tasumise tõenäosust. Makse ennustus annab ettevõtetele ka teavet, mis on vajalik kogumisprotsessi varakult alustamise õigustamiseks.

## <a name="methodology"></a>Metoodika

Tehisintellektiga lahenduse arendamine ja kasutuselevõtmine on raske. Selleks on vajalik andmeteadlastest, valdkonna asjatundjatest ja inseneridest koosnevat meeskonda, kes töötavad pikka aega, et sõnastada, arendada, kasutada ja hallata kasutatavat tehisintellekti lahendust. Me muudame tehisintellektiga lahenduse rakenduses Finance juurutamise ja kasutamise lihtsaks. Meil on lisame tehisintellektiga lahendused rakendusse Finance, mis on ehitatud Microsoft AI Builderi peale. Lõppkasutaja saab ühe nupuvajutusega juurutada tehisintellektiga lahenduse ja hakata kaaluma nutikate ennustuste eeliseid. Kui organisatsioon ei ole ennustuste täpsusega rahul, saab lauskasutaja taas ühe nupuvajutusega siseneda AI Builderi laienduskogemusse ja seejärel valida või tühistada nende väljade valiku, mida kasutatakse ennustuste loomiseks. Kui valmis, saavad nad treenida ja avaldada muudatused ning uut treenitud mudelit hakatakse automaatselt rakenduses Finance ennustuste jaoks kasutama.

## <a name="how-to-get-customer-payment-insights-preview"></a>Kuidas hankida funktsioon Kliendi makse ülevaated (eelvaade)

Kui olete huvitatud funktsiooni Kliendi makse ülevaated (eelversioon) proovimisest, saatke meil lahendusele [Kliendi makse ülevaated (eelversioon)](mailto:fiap@microsoft.com).

## <a name="privacy-notice"></a>Privaatsusavaldus

Eelvaated 1) võivad kasutada vähem privaatsus- ja turbemeetmeid kui rakenduse Dynamics 365 Finance and Operations teenus, 2) ei ole hõlmatud selle teenuse teenusetaseme leppes, 3) ei tohi olla kasutusel isiklike andmete ega muude andmete töötlemiseks, mis on seaduste või määrustega kaitstud, ja 4) on piiratud toega.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]