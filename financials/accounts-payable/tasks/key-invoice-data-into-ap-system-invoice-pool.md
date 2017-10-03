--- 
title: "Arve põhiandmed ostureskontro süsteemi arvete kausta abil"
description: "See ülesande juhend näitab teile, kuidas kasutada arvete loomiseks arveregistrit."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 08f66db0f62d5d985177b1d4ec0161df0b9961b3
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>Arve põhiandmed ostureskontro süsteemi arvete kausta abil

[!include[task guide banner](../../includes/task-guide-banner.md)]

See ülesande juhend näitab teile, kuidas kasutada arvete loomiseks arveregistrit.  Seejärel kasutage arve sobitamiseks ostutellimusega arvete kausta ja lõpetage kulu hankija arve lehel.


## <a name="create-a-purchase-order"></a>Ostutellimuse loomine
1. Avage Ostureskonto > Ostutellimused > Ostutellimused.
2. Klõpsake ostutellimuse loomiseks suvandit Uus.
3. Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.
4. Valige hankija loendist. Näiteks hankija 1001.
5. Klõpsake nuppu OK.
6. Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.
7. Leidke loendist teenuste kaubakood. Valige näiteks S0001.
8. Klõpsake kaubakoodil ja valige see.
    * Netosumma on 75,00.  See on summa, mida arvele eeldame.  
9. Klõpsake tegumiribal valikut Ost.
10. Klõpsake käsku Kinnita.

## <a name="create-and-post-and-invoice"></a>Arve loomine ja sisestamine
1. Avage Ostureskontro > Arved > Arveregister.
2. Klõpsake valikut Uus.
3. Avage otsing, et valida arveregistri nimi, mida soovite kasutada.
4. Valige selle arveregistri nimi, mida soovite kasutada.
5. Registri avamiseks ja kuluridade sisestamiseks klõpsake nuppu Read.
6. Valige otsingus hankija. Näiteks klõpsake hankijat 1001.
7. Sisestage arve number väljale Arve.
8. Sisestage väärtus väljale Kirjeldus.
9. Sisestage arv väljale Kreedit.
10. Klõpsake väljal Ostutellimus otsingu avamiseks ripploendi nuppu.
11. Valige varem loodud ostutellimus.
12. Klõpsake väljal Kinnitaja otsingu avamiseks ripploendi nuppu.
13. Tõstke kinnitaja esile ja klõpsake nuppu Vali, et see kinnitaja valida.
14. Klõpsake valikut Sisesta.
15. Sulgege vorm.
16. Sulgege vorm.

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>Arve avamine kaustast ja selle vastendamine ostutellimusega arve protsessi lõpetamiseks
1. Avage Ostureskontro > Arved > Arvete kaust.
2. Klõpsake suvandit Ostutellimus, et luua kaustas olevast arvest hankija arve.
3. Valige arve, mida soovite vaadata.
4. Vastendamise lõpetamiseks klõpsake suvandit Värskenda vastendamise olek.
5. Klõpsake tegumiribal valikut Suvandid.
6. Klõpsake suvandit Muuda vaadet.
7. Klõpsake suvandit Ruudustikuvaade.
8. Klõpsake valikut Sisesta.
9. Sulgege vorm.
10. Avage Ostureskonto > Hankijad > Hankijad.
11. Valige ostutellimusel olnud hankija. Valige näiteks hankija 1001.
12. Klõpsake loendis valitud real olevat linki.
13. Klõpsake tegumiribal valikut Hankija.
14. Klõpsake suvandit Kanded.
15. Valige loodud arve.
    * Arve registri juurdekasv tühistati ja sisestati asjakohasele kulu kontole.  


