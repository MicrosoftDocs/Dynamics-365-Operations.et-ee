--- 
title: "Koormate ja saadetiste planeerimine koorma planeerimise töölaua abil"
description: "See protseduur näitab, kuidas kasutada müügitellimuse koorma loomiseks koorma planeerimise töölauda."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f840a4c15305af5f55451ae7f1cec2da25e685a4
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a>Koormate ja saadetiste planeerimine koorma planeerimise töölaua abil

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas kasutada müügitellimuse koorma loomiseks koorma planeerimise töölauda. Eeltingimusena loome esmalt müügitellimuse. See protseduur on osa transpordikoordinaatori igapäevatööst. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="create-a-sales-order"></a>Loo müügitellimus
1. Avage Müügireskontro > Tellimused > Kõik müügitellimused.
2. Klõpsake valikut Uus.
3. Klõpsake väljal Kliendi konto otsingu avamiseks ripploendi nuppu.
4. Valige konto US-004.
5. Klõpsake nuppu OK.
6. Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.
7. Valige kaup A0001.
    * A0001 on lubatud transpordihalduse puhul.  
8. Klõpsake loendis valitud real olevat linki.
9. Sisestage arv väljale Kogus.
10. Sisestage väljale Ladu väärtus 24.
    * Valige selle näite puhul ladu 24. See ladu võimaldab transpordihaldust ja täiustatud laohaldust.  
11. Klõpsake nuppu Salvesta.
12. Sulgege leht.

## <a name="create-a-new-load"></a>Uue koorma loomine
1. Avage Transpordihaldus > Plaanimine > Koorma plaanimise töölaud.
2. Klõpsake vahekaarti Müügiread.
    * Nüüd saate luua äsja loodud müügitellimuse koorma. Koormaid saab luua ostutellimuste, üleviimistellimuste ja müügitellimuste pakkumise ja nõudluse põhjal.  
3. Klõpsake toimingupaanil suvandit Pakkumine ja nõudlus.
4. Klõpsake suvandit Uude koormasse.
5. Klõpsake väljal Koorma malli ID otsingu avamiseks ripploendi nuppu.
    * Koorma mall määratleb kogu koorma maksimaalse kaalu ja mahu mõõtmed. Näiteks võib koorma mall tähistada konteineri või veoauto suurust.  
6. Klõpsake loendis valitud real olevat linki.
7. Klõpsake nuppu OK.

## <a name="rate-and-route-the-load"></a>Koorma hindamine ja marsruudi määramine
1. Klõpsake suvandit Hindamine ja marsruudivalik.
2. Klõpsake suvandit Marsruudi töölaua määr.
3. Klõpsake suvandit Kogumäär.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake käsku Määra.
6. Sulgege leht.
7. Sulgege leht.


