---
title: " Püsikliendi preemiapunktide määratlemine"
description: See protseduur juhendab püsikliendi preemiapunktide määratlemisel.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyRewardPoints
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e40ebcbf3ab1befc641ae34571a8b974bd0425a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140872"
---
# <a name="define-loyalty-reward-points"></a> Püsikliendi preemiapunktide määratlemine

[!include [banner](../includes/banner.md)]

See protseduur juhendab püsikliendi preemiapunktide määratlemisel. Püsikliendi preemiapunktid tuleks seadistada enne püsikliendi programmi alustamist. Protseduur kasutab demoettevõtte USRT andmeid.

1. Avage Jaemüük ja kaubandus > Kliendid > Püsiklient > Püsikliendi preemiapunktid.
2. Klõpsake Uus.
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
    * Preemiapunktid aeguvad nende väljastamise järel teatud arvu päevade, kuude või aastate pärast. Väärtus „0” tähendab, et püsikliendi preemiapunktid ei aegu kunagi.  
10. Valige suvand väljal Expiration time unit (Realiseerimisaja ühik).
11. Klõpsake nuppu Salvesta.

