--- 
title: " Püsikliendi preemiapunktide määratlemine"
description: "See protseduur juhendab püsikliendi preemiapunktide määratlemisel."
author: scott-tucker
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 56f11484d960ab22aefef359c18f71d54dc50071
ms.contentlocale: et-ee
ms.lasthandoff: 07/28/2017

---
# <a name="define-loyalty-reward-points"></a> Püsikliendi preemiapunktide määratlemine

[!include[task guide banner](../includes/task-guide-banner.md)]

See protseduur juhendab püsikliendi preemiapunktide määratlemisel. Püsikliendi preemiapunktid tuleks seadistada enne püsikliendi programmi alustamist. Protseduur kasutab demoettevõtte USRT andmeid.

1. Avage Jaemüük ja kaubandus > Kliendid > Püsiklient > Püsikliendi preemiapunktid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Reward point ID (Preemiapunkti ID).
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Valige suvand väljal Reward point type (Preemiapunkti tüüp).
    * Valige Kogus, kui soovite, et preemiapunktid ümardataks lähima täisarvuni. Kui soovite, et preemiapunktid ümardataks valuuta ümardamisreeglite järgi, valige Summa. Kui teete valiku Kogus, jätke selle protseduuri järgmine etapp vahele.  
6. Sisestage väärtus väljale Valuuta.
    * Summa tüüpi preemiapunktide kasutamisel on kõik väljastatavad punktid valitud valuutas. Koguse tüüpi preemiapunktide korral see väli ei kehti. Jätke see etapp vahele.  
7. Märkige ruut Redeemable (Lunastatav) või eemaldage sellest märge.
8. Sisestage number väljale Redeem ranking (Lunastusjärk).
    * Lunastusjärke kasutatakse, kui toodete eest maksmiseks saab kasutada kahte või enamat sobivat preemiapunkti. Kui kahel preemiapunktil on sama lunastusjärk, siis kasutatakse seda, mille punktide arv vajab langetamist.  
9. Sisestage väljale Expiration time value (Realiseerimisaja väärtus) number.
    * Preemiapunktid aeguvad nende väljastamise järel teatud arvu päevade, kuude või aastate pärast. Väärtus "0" tähendab, et püsikliendi preemiapunktid ei aegu kunagi.  
10. Valige suvand väljal Expiration time unit (Realiseerimisaja ühik).
11. Klõpsake nuppu Salvesta.


