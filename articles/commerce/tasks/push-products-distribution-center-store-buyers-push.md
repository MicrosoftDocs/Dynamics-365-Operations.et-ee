---
title: " Toodete jaotamine jaotuskeskusest kauplusse kesklaost jaotuse abil"
description: See protseduur tutvustab, kuidas luua ja töödelda jaotust kesklaost toodete laialisaatmiseks ühest kohast ühte või mitmesse kauplusesse.
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailBuyersPush, InventLocationIdLookup, InventItemIdLookupSimple, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dad74855ab9a9c225a5cd64a8c27663aedcd21e4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411708"
---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a> Toodete jaotamine jaotuskeskusest kauplusse kesklaost jaotuse abil

[!include [banner](../includes/banner.md)]

See protseduur tutvustab, kuidas luua ja töödelda jaotust kesklaost toodete laialisaatmiseks ühest kohast ühte või mitmesse kauplusesse. Kasutaja saab määrata mitu konfiguratsiooni ja lasta süsteemil soovitada, kuidas tooted laiali saata, või käsitsi sisestada, kuhu tooted saadetakse ja kui suure koguse iga kauplus saab. See protseduur ei sisalda andmete seadistust, mida kesklaost jaotamisel kasutada nagu täiendamise reeglid, organisatsioonihierarhiad ja kaupluse kaalud. See protsess kasutab demoettevõtte USRT-i andmeid.

1. Valige Buyer's push (Kesklaost jaotus).
2. Klõpsake valikut Uus.
3. Sisestage väljale Kirjeldus soovitud väärtus.
4. Sisestage või valige väärtus väljal Koht.
5. Sisestage või valige väljal Ladu ladu, milles on vajalikud kaubakogused käepärast.
6. Klõpsake vahekaarti Lisa.
7. Märkige loendis valitud rida.
8. Sisestage või valige väljal Item (Kaup) number või toode.
9. Klõpsake vahekaarti Lisa.
10. Märkige loendis valitud rida.
11. Sisestage või valige väljal Item number (Kauba number) tootevariant.
    * Tootevariandi sisestamisel luuakse iga variandi jaoks rida.  
12. Märkige loendis rida.
13. Sisestage väljale Jaotatud kogus, mitut valitud toodet soovite laiali saata.
14. Sisestage väljale Lisakogus jaotamiseks toodete kogus, mis on jaotamiseks piisavas koguses saadaval.
15. Sisestage väljale Distribution (Jaotus) asukoha kaal.
    * Saate teisi tüüpe valida teiste jaotusreeglite kasutamiseks.  
16. Sisestage väljale Täiendamise hierarhia väärtus.
17. Valige Jah väljal Respect assortments (Sortimendi tunnustamine).
18. Klõpsake valikut Arvuta kogused ja vaadake üle jaotise Ladu ridadesse lisatud kogused.
19. Klõpsake valikut Create order (Loo tellimus).
20. Klõpsake nuppu Jah.

