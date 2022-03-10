---
title: Laovaru tasemete lähtestamine laos
description: See protseduur näitab, kuidas värskendada vabu kaubavarusid käsitsi, kasutades varude liikumise töölehte.
author: yufeihuang
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 264dabf9c1c10c3d2cee3e0c942abbfa249f21f5
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565875"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a>Laovaru tasemete lähtestamine laos

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas värskendada vabu kaubavarusid käsitsi, kasutades varude liikumise töölehte. (Vabu kaubavarusid saab värskendada ka kannete importimisega andmeüksustes.) Saate käitada seda juhendit demoettevõttes USMF, kus kõik eeltingimused, nagu töölehe nimi, kaubaseadistus, sisestusprofiilid ja kontod,on saadaval. Juhend soovitab kindlaid väärtusi kasutatavale kaubale ja dimensioonidele. Teise kauba valimisel peate võib-olla sisestama väärtused teiste dimensioonide kohta.

1. Minge jaotisse Varude haldus > Töölehe sisestused > Kaubad > Liikumine.
2. Klõpsake valikut Uus.
3. Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.
4. Valige suvand IMov.
    * Soovitatav on kasutada erinevate äritegevuste jaoks erinevaid töölehtede nimemalle.  
5. Klõpsake loendis valitud real olevat linki.
6. Määrake väljal vastaskonto väärtus 140 200.
    * See on vastaskonto, mis on töölehe ridade vaikekonto. Vaikekonto saab tühistada, et määrata igale reale erinevad vastaskontod.  
7. Klõpsake nuppu OK.
8. Klõpsake valikut Uus.
9. Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.
10. Valige kaup A0001.
11. Klõpsake loendis valitud real olevat linki.
12. Klõpsake vahekaarti Varude dimensioonid.
13. Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.
14. Valige tegevuskoht 1.
15. Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.
16. Valige ladu 13.
17. Klõpsake loendis valitud real olevat linki.
18. Klõpsake väljal Asukoht otsingu avamiseks ripploendi nuppu.
19. Valige asukoht 13.
20. Sisestage arv väljale Kogus.
21. Klõpsake nuppu Salvesta.
22. Klõpsake valikut Sisesta.
23. Märkige või tühjendage ruut Kanna kõik sisestusvead üle uuele töölehele.
    * Selle suvandi lubamisel kopeeritakse kõik read, mille sisestamine ei õnnestu, uuele töölehele. Logiteabe abil saate probleemid lahendada ja seejärel read uuesti sisestada.  
24. Klõpsake nuppu OK.
25. Sulgege leht.
26. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]