---
title: Tarnegraafikud
description: Tarnegraafikute abil saate jälgida tellimuse rea kogust, kui kasutate ühe müügitellimuse, müügipakkumise või ostutellimuse puhul mitut tarnet.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b9d7636a9a246b069fbd419d1d857ca47c73ff6ddd9b620f077b0ab15c23c67
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721267"
---
# <a name="delivery-schedules"></a>Tarnegraafikud

[!include [banner](../includes/banner.md)]

Tarnegraafikute abil saate jälgida tellimuse rea kogust, kui kasutate ühe müügitellimuse, müügipakkumise või ostutellimuse puhul mitut tarnet.

Kasutage tarnegraafikuid, kui tellimuse- või pakkumiserea täielik kogus tuleb tarnida mitme saadetisena. Üksikud saadetised esitatakse tarneridadena. Kaks või enam tarnerida moodustavad ühe tarnegraafiku. Tarneridadel võivad olla erinevad tarnekuupäevad, kogused, tarneviisid ja ladustamisdimensioonid, nagu koht ja ladu.  

**Tarnegraafiku rea näide**

| Kaup                              | Väärtus                                    |
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





[!INCLUDE[footer-include](../../includes/footer-banner.md)]