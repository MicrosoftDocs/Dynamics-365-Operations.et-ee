---
title: Vahemikuga intressikoodi loomine
description: Viivisekoodid saab seadistada nii, et arvutatakse erinevad viivisesummad väärtuste vahemiku põhjal.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Interest, CustInterestRange
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d77fc88f606f4e690583fbcda79f628a35f14f6a
ms.sourcegitcommit: 6a269db08e8bb3bb3405c9f4a512091d13c80faa
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119470"
---
# <a name="create-an-interest-code-with-a-range"></a>Vahemikuga intressikoodi loomine

[!include [banner](../../includes/banner.md)]
Viivisekoodid saab seadistada nii, et arvutatakse erinevad viivisesummad väärtuste vahemiku põhjal. See protseduur näitab, kuidas viivisekoodi ja sellele vahemikku lisada.

1. Minge väljadele **Kreedit ja > viivise > seadistage viivisekoodid**.
2. Klõpsake valikut **Uus**.
3. **Sisestage viivisekoodi** nimi väljale Viivisekood.
4. **Sisestage** viivisekoodi kirjeldus väljale Kirjeldus.
5. Valige **kuu**.
6. Laiendage jaotist **Tulud**.
7. Laiendage jaotist **Tulud valuuta järgi**.
8. Määrake väljal **Pearaamatu sisestuskonto** soovitud väärtused.
9. Valige väljal **Intress** vahemikust väärtus Kuud.
10. Klõpsake käsku **Lisa**.
11. Sisestage **kirjeldus** väljale Kirjeldus selle valuuta ja vahemiku kohta.
12. Klõpsake nuppu **Salvesta**.
13. Klõpsake nuppu **Vahemikud**.
14. Klõpsake valikut **Uus**.
15. Sisestage **väärtus Alates** väärtusena 0 ja seejärel intressi arvutamiseks kasutatav viivise protsent kuus. Meie näites on see 1,5.
16. Klõpsake valikut **Uus**.
17. Sisestage järgmiseks algväärtuseks 4, mis on esimene kuu, millest alates uut viivisesummat arvutatakse.
18. Sisestage viiviseprotsent kuus, mida kasutatakse viivise arvutamiseks alates 4. kuust. Selles näites on viiviseprotsent 2,0.
19. Klõpsake valikut **Uus**.
20. Sisestage järgmiseks algväärtuseks 7, mis on järgmine kuu, millest alates uut viivisesummat arvutatakse.
21. Sisestage viiviseprotsent kuus, mida kasutatakse viivise arvutamiseks alates 7. kuust. Selles näites on viiviseprotsent 2,5.
22. Seadistuse **lõpuleviimiseks** klõpsake nuppu Sule.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
