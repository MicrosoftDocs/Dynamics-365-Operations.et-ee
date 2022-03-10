---
title: Arve põhiandmed ostureskontro süsteemi arvete kausta abil
description: See teema kirjeldab, kuidas kasutada arvete loomiseks arveregistrit.
author: abruer
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4768ee6ddbaba8ae5bab5e2f9f7df9239efeb90
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358285"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>Arve põhiandmed ostureskontro süsteemi arvete kausta abil

[!include [banner](../../includes/banner.md)]

See teema kirjeldab, kuidas kasutada arvete loomiseks arveregistrit. Seejärel kasutage arve sobitamiseks ostutellimusega arvete kausta ja lõpetage kulu hankija arve lehel.


## <a name="create-a-purchase-order"></a>Ostutellimuse loomine
1. Avage navigeerimispaanil **Moodulid > Ostureskontro > Ostutellimused > Ostutellimused**.
2. Ostutellimuse loomiseks valige **Uus**.
3. Väljal **Tarnija konto** valige ripploendist tarnija. Näiteks valige tarnija **1001**.
4. Valige nupp **OK**.
5. Väljal **Üksuse number** valige ripploendist teenuse üksuse number. Näiteks, valige **S0001**. Netosumma on 75,00.  See on summa, mida arvele eeldame.  
6. Valige toimingupaanil **Osta**.
7. Valige **Kinnita**.

## <a name="create-and-post-and-invoice"></a>Arve loomine ja sisestamine
1. Minge navigeerimispaanil jaotisse **Moodulid > Ostureskontro > Arved > Arveregister**.
2. Valige suvand **Uus**.
3. Avage otsing, et valida arveregistri nimi, mida soovite kasutada.
4. Valige selle arveregistri nimi, mida soovite kasutada.
5. Registri avamiseks ja kuluridade sisestamiseks valige **Read**.
6. Valige otsingus hankija. Näiteks valige tarnija **1001**.
7. Sisestage arve number väljale **Arve**.
8. Sisestage väärtus väljale **Kirjeldus**.
9. Sisestage number väljale **Kreedit**.
10. Väljal **Ostutellimus** avage ripploend, et valida varem loodud ostutellimus.
11. Väljal **Kinnitaja** tõstke esile kinnitaja ja klõpsake kinnitaja valimiseks **Vali**.
12. Valige **Sisesta**.

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>Arve avamine kaustast ja selle vastendamine ostutellimusega arve protsessi lõpetamiseks
1. Avage navigeerimispaanil **Moodulid > Ostureskontro > Arved > Arvekaust**.
2. Valige **Ostutellimus**, et luua arvete kaustast tarnija arve.
3. Valige arve, mida soovite vaadata.
4. Vastenduse lõpetamiseks valige **Vastenduse oleku värskendamine**.
5. Toimingupaanil valige **Suvandid**.
6. Valige **Muuda vaadet**.
7. Valige **Ruudustiku vaade**.
8. Valige **Sisesta**.
9. Sulgege leht.
10. Navigeerimispaanil avage **Moodulid > Ostureskontro > Tarnijad > Tarnijad**.
11. Valige ostutellimusel olnud hankija. Näiteks valige tarnija **1001**.
12. Valige toimingupaanil **Tarnija**.
13. Valige **Kanded**.
14. Valige loodud arve. Arve registri juurdekasv tühistati ja sisestati asjakohasele kulu kontole.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
