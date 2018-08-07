---
title: "Laovaru tasemete korrigeerimine laos (üldine ladustamine)"
description: "See protseduur selgitab varude korrigeerimise töölehe loomise ja sisestamise protsessi laos olevate toodete laovarude korrigeerimiseks."
author: MarkusFogelberg
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
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9ca5841fe857990cae8d9551ccf79c3c0fd490ae
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a>Laovaru tasemete korrigeerimine laos (üldine ladustamine)

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur selgitab varude korrigeerimise töölehe loomise ja sisestamise protsessi laos olevate toodete laovarude korrigeerimiseks. Enne selle käivitamist peate seadistama varude korrigeerimiste jaoks varude töölehe nime. Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades. Neid ülesandeid täidab üldjuhul laotöötaja.


## <a name="create-an-inventory-adjustment-journal"></a>Varude korrigeerimise töölehe loomine
1. Avage Varude haldus > Töölehe sisestused > Kaubad > Varude korrigeerimine.
2. Klõpsake valikut Uus.
3. Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.
4. Klõpsake loendis soovitud varude korrigeerimise töölehe nime.
    * Osad muud väljad täidetakse teie valitud varude korrigeerimise töölehe nime seadistuse põhjal.  
5. Klõpsake nuppu OK.

## <a name="create-journal-lines"></a>Tööleheridade loomine
1. Klõpsake valikut Uus.
2. Märkige loendis kaubakoodi väli.
3. Valige kaup väljal Kaubakood. Kui kasutate demoettevõtte USMF andmeid, sisestage „D0001”.
4. Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.
5. Valige loendist tegevuskoht.
6. Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.
7. Valige loendist ladu.
    * Kui olete valinud kauba, mille puhul asukoht on kohustuslik dimensioon, peate siin määratlema asukoha.  
8. Sisestage arv väljale Kogus.
    * Omahinna väli määrab ühiku omahinna lao sissetulekutele. Kui kaubakoodi kohta pole kulu määratud või kui soovite seda käsitsi muuta, tehke seda siin.  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a>Varude korrigeerimise töölehe kinnitamine ja sisestamine
1. Klõpsake suvandit Kinnita.
2. Klõpsake nuppu OK.
3. Klõpsake valikut Sisesta.
    * Sellist tüüpi töölehe sisestamisel sisestatakse lao sissetulek või väljaminek, muudetakse laotaset ja -väärtust ning luuakse pearaamatu kanded.  
4. Klõpsake nuppu OK.
5. Sulgege vorm.
6. Sulgege leht.

