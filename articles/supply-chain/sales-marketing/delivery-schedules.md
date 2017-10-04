---
title: Tarnegraafikud
description: "Tarnegraafikute abil saate jälgida tellimuse rea kogust, kui kasutate ühe müügitellimuse, müügipakkumise või ostutellimuse puhul mitut tarnet."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 701a8b2b94fecedcddada46ad6438448254c8e77
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017

---

# <a name="delivery-schedules"></a>Tarnegraafikud

[!include[banner](../includes/banner.md)]


Tarnegraafikute abil saate jälgida tellimuse rea kogust, kui kasutate ühe müügitellimuse, müügipakkumise või ostutellimuse puhul mitut tarnet.

Kasutage tarnegraafikuid, kui tellimuse- või pakkumiserea täielik kogus tuleb tarnida mitme saadetisena. Üksikud saadetised esitatakse tarneridadena. Kaks või enam tarnerida moodustavad ühe tarnegraafiku. Tarneridadel võivad olla erinevad tarnekuupäevad, kogused, tarneviisid ja laoala dimensioonid, nagu tegevuskoht ja ladu.  

**Tarnegraafiku rea näide**

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| Kogutellimus (algne tellimuserida) | 600 tooli                               |
| Nõutav tarnegraafik       | 100 tooli kuus                     |
| Nõutav tarne ajavahemik | 6 kuud, iga kuu esimesel päeval |

Selle stsenaariumi korral taotleb klient 600 tooli tarnet 100-tooliste partiidena kuue kuu jooksul. Tarnenõuete jälgimiseks loote te tarnegraafiku. Tarnegraafiku lehel loote kuus eraldi tarnerida. Iga tarnerida sisaldab 100 tooli ja näitab nende 100 tooli tarnekuupäeva. Sellisel juhul tasakaalustatakse iga rida kuue järjestikuse kuu esimesel kuupäeval.  

Tarnegraafiku loomisel muutub algse tellimusrea tüübiks automaatselt **Mitme tarnega tellimuserida**. Seda tüüpi rida nimetatakse äriandmete reaks ja see on tähistatud ikooniga. Tarnerida on tähistatud teistsuguse ikooniga. Tarnerea koguse muutmisel värskendatakse äriandmete rida tarnegraafiku lõplikule kogusele. Kui kaubandusleppes on määratletud tellimuse lõplik allahindlus, tagab tarnegraafik, et teie tellimus on sobilik tellimuse lõplikule allahindlusele, isegi kui tellimus on jaotatud eraldi tarneteks.  

Tarnegraafikuga tellimusi töödeldakse tarneridade järgi. Töötlemine hõlmab saatelehtede sisestamist, toote sissetulekuid ja arveldamist.  

Tarnegraafikuga tellimuste ja pakkumiste trükitud dokumentidel kuvatakse ainult tarneread. Algseid ridu (äriandmete ridu) neil ei kuvata. **Märkus.** Peale selle kuvatakse järgmiste tegevuste korral ainult tarneread.

-   Postita
-   Lehtede kopeerimine
-   Loendi lehekülgede ja aruannete sirvimine

Müügipakkumiste kinnitamisel kuvatakse tulemuseks saadavatel müügitellimustel kogu tarnegraafik, sh ka mitme tarnega tellimuseread. Samuti kuvatakse kogu tarnegraafik kõigil põhilehtedel, nagu müügitellimused, müügipakkumised ja ostutellimused.



