---
title: Uue toodetud kauba standardomahinna värskendamine
description: Selles artiklis antakse juhiseid uue toodetud kauba standardkulude värskendamise kohta.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79693
ms.assetid: ba64b70f-3f4c-4373-9a7d-8fd07c45a8cf
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 231f0ed5acc86dbe5368b3c7306dd89c8ba0b74901a7e1ccf8410c6585638efa
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733488"
---
# <a name="update-standard-costs-for-a-new-manufactured-item"></a>Uue toodetud kauba standardomahinna värskendamine

[!include [banner](../includes/banner.md)]

Selles artiklis antakse juhiseid uue toodetud kauba standardkulude värskendamise kohta. 

Järgmised juhised eeldavad, et kasutate kaheversioonilist lähenemist standardkulude värskendamiseks. Selles lähenemises sisaldab üks kuluarvutuse versioon standardkulusid, mis määratleti algselt külmutatud perioodiks, ja teine kuluarvutuse versioon sisaldab uute toodetud kaupade astmelisi värskendusi. Astmelised värskendused sisestatakse kulukirjetena teise kuluversiooni, ja lõpuks aktiveeritakse. Kaheversiooniline lähenemine nõuab teise kuluarvutuse versiooni määratlemist. Siin on juhised selle kuluarvutuse versiooni määratlemiseks.

-   Määrake kuluarvutuse tüüp **Standardkulu**.
-   Määrake kirjeldav identifikaator, mis näitab kuluarvutuse versiooni sisu, nt **2016-VÄRSKENDUSED**.
-   Veenduge väljagrupis **Luba hinna tüübid**, et valiku **Omahind** väärtuseks on määratud **Jah**.
-   Lubage kulukirjete sisestamine kõigi laoalade puhul (st jätke väli **Laoala** tühjaks). Laoala sisestamisel saab kulukirjeid sisestada ainult selle laoala jaoks.
-   Kasutage taandepõhimõtet **Aktiivne**.

Uute toodetavate kaupade lisamiseks kogu külmutatud perioodi jooksul tehke järgmist.

1.  Kasutage lehte **Kuluarvutuse versiooni seadistamine**, et lubada kulukirjete sisestamine teise kuluarvutuse versiooni, mis sisaldab astmelisi värskendusi. Ennetage ootel kulude aktiveerumist, kus aktiveerumine lubatakse pärast ootel kulude täielikku ja õiget määramist. Määrake tühi alguskuupäev kuluversiooni poliitikana, ja siis sisestage alguskuupäev iga kulukirje sisestamisel. Alguskuupäev peab näitama kuupäeva enne uute kaupade ostmist või tootmist.
2.  Uute ostetud kaupade eest kulukirjete sisestamiseks kasutage lehte **Kauba hind**. Sisestage igale kulukirjele kuluversioon, mis sisaldab astmelisi värskendusi, ja kasutage alguskuupäeva, mis eelneb uute toodetavate kaupade eeldatavale tootmiskuupäevale.
3.  Arvutage uute toodetud kaupade kulu lehel **Arvutus**. Avage leht **Arvutus** lehelt **Kuluarvutuse versiooni hooldus** ja valige siis astmelisi värskendusi sisaldav kuluarvutuse versioon. Kasutage valikukriteeriume uue toodetava kauba ja mõne selle toodetud komponendi määramiseks. Mitmetasemelises tootestruktuuris võib olla ka vajalik määrata mõni põhiüksus, mis sisaldab komponendina uusi toodetud kaupu. Sisestage koosluse kalkulatsioonile alguskuupäev, mis vastaks uute toodetud kaupade tootmise algusele. Alguskuupäev peab jääma kauba koosluse versiooni protsessiversiooni kehtivuskuupäevade raamesse. **Märkus:** puuduv kulukirje võib viidata uuele toodetud kaubale. Koosluse kalkulatsioonid võivad sisaldada ainult puuduva hinnaga kaupu.
4.  Kontrollige uute toodetud kaupade arvutatud kulude terviklikkust ja täpsust. Kasutage lehte **Lõpetatud** iga kauba kulukirje ja teabelogi hoiatusteadete ülevaatamiseks. Alternatiivina kasutage lehte **Arvutus** arvutatud kulude loendi ülevaatamiseks.
5.  Kasutage lehte **Kuluarvutuse versiooni seadistus** blokeerimislipu muutmiseks, et lubada teise kuluarvutuse versiooni ootel kulukirjete aktiveerimine.
6.  Kasutage lehte **Hindade aktiveerimine** (mille saab avada lehelt **Kuluarvutuse versiooni hooldus**) kõigi teises kuluarvutuse versiooni ootel kauba kulukirjete aktiveerimiseks. Ootel kulukirjeid saab aktiveerida ka eraldi kaupade kohta, klõpsates nuppu **Aktiveerimine** lehel **Kauba hind**.
7.  Kasutage lehte **Kuluarvutuse versiooni seadistus** blokeerimislippude muutmiseks, et vältida täiendavat andmete hooldust. Blokeerimispoliitikad takistavad uute ootel kulude sisestamist ja ootel kulude aktiveerimist.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]