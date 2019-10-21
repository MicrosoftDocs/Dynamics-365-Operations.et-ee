---
title: Tööjõu ja kulude standardsete kulude konfigureerimine
description: Selles teemas selgitatakse, kuidas seadistada töö jaoks standardne kulu ja projekti kulutused.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60ab8eb94d4a8a0fb2c1e732ec7b25bfd5e7611e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185401"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Tööjõu ja kulude standardsete kulude konfigureerimine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles teemas selgitatakse, kuidas seadistada töö jaoks standardne kulu ja projekti kulutused. Ülesandes kasutatakse USSI andmekomplekti.

1. Navigeerimispaanil avage **Moodulid > Projektihaldus ja raamatupidamine > Seadistus > Hinnad > Omahind (tund)**.
2. Valige suvand **Uus**.
3. Väljale **Jõustumiskuupäev** sisestage kuupäev.
4. Väljale **Omahind** sisestage arv. Saate teatud projektikategooria jaoks standardse omahinna häälestada või häälestada omahinna töötaja koodi, projekti numbri, kategooria, kuupäeva või mis tahes nende kombinatsiooni alusel. Rakendatakse kõrgeima üksikasjatasemega omahind.  
5. Valige käsk **Salvesta**.
6. Navigeerimispaanil avage **Moodulid > Projektihaldus ja raamatupidamine > Seadistus > Hinnad > Müügihind (tund)**.
7. Valige suvand **Uus**.
8. Väljale **Jõustumiskuupäev** sisestage kuupäev.
9. Väljal **Kehtib** valige sobiv variant.
10. Väljale **Hinnakujundus** sisestage arv. Saate häälestada standardse müügihinna tunnikannetele või projekti kategooriale. Saate häälestada ka müügihinnad töötaja koodi, projekti numbri, kategooria, kande kuupäeva või nende mis tahes kombinatsioonide alusel. Tegelik müügihind, mis rakendatakse, kui töötaja sisestab kande tunnitöölehele, on kõrgeima üksikasjatasemega müügihind. Näiteks kui nii üldine kui ka töötajapõhine müügihind on häälestatud, kasutatakse töötajapõhist müügihinda.  
11. Valige käsk **Salvesta**.
12. Sulgege leht.
13. Navigeerimispaanil avage **Moodulid > Projektihaldus ja raamatupidamine > Seadistus > Hinnad > Omahind (kulu)**.
14. Valige suvand **Uus**.
15. Väljale **Jõustumiskuupäev** sisestage kuupäev.
16. Väljale **Omahind** sisestage arv. Täita saab mitut välja, kuid see on kirje salvestamiseks vajalik miinimum.  
17. Valige käsk **Salvesta**.
18. Navigeerimispaanil avage **Moodulid > Projektihaldus ja raamatupidamine > Seadistus > Hinnad > Müügihind (kulu)**.
19. Valige suvand **Uus**.
20. Väljale **Jõustumiskuupäev** sisestage kuupäev.
21. Väljal **Kehtib** valige sobiv variant.
22. Väljale **Hinnakujundus** sisestage arv. Tegelik müügihind, mis seotakse, kui töötaja sisestab kanded kulude töölehele, on kõrgeima üksikasjatasemega müügihind. Näiteks kui nii üldine kui ka töötajapõhine müügihind on häälestatud, kasutatakse töötajapõhist müügihinda.  
23. Valige käsk **Salvesta**.

