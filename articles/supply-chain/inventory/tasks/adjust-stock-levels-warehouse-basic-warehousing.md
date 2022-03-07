---
title: Laovaru tasemete korrigeerimine laos (üldine ladustamine)
description: See protseduur selgitab varude korrigeerimise töölehe loomise ja sisestamise protsessi laos olevate toodete laovarude korrigeerimiseks.
author: yufeihuang
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 02458d588c9925a1f4cb9afeada793dfc55a2071
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573821"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a>Laovaru tasemete korrigeerimine laos (üldine ladustamine)

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]