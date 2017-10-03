--- 
title: "Ostutellimuse loomine ühekordse tarnija jaoks"
description: "Selles protseduuris selgitatakse, kuidas luua ostutellimus ühekordsele hankijale."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 580dfe3680c36a32a24999bc8c266a38a07177fd
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Ostutellimuse loomine ühekordse tarnija jaoks

[!include[task guide banner](../../includes/task-guide-banner.md)]

Selles protseduuris selgitatakse, kuidas luua ostutellimus ühekordsele hankijale. Hankija luuakse automaatselt koos ostutellimusega, hankija kontot pole vaja käsitsi luua. Ostutellimused loob tavaliselt ostuagent. Selles juhendis toodud näidet saab kasutada demoandmete ettevõtte USMF puhul. Eeltingimuseks on, et ühekordse hankija konto on seadistatud lehel Ostureskontro parameetrid.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Ostutellimuse loomine ühekordse tarnija jaoks
1. Avage Hanked > Ostutellimused > Kõik ostutellimused.
2. Klõpsake valikut Uus.
3. Tehke väljal Ühekordne hankija valik Jah.
    * Hankija konto luuakse automaatselt ja määratakse ostutellimusele. Hankija konto luuakse lehe Ostureskontro parameetrid vahekaardil Üldine määratud malli põhjal.  
4. Sisestage väljale Nimi hankija nimi.
5. Klõpsake nuppu OK.
    * Ostutellimuse saab nüüd lõpetada ja seda saab töödelda, nagu iga teist tellimust. Selle tegemiseks pole mingeid erijuhiseid. Arvel kajastub tellimusega koos loodud hankija kontol toimuv kanne ja seejärel töödeldakse makse. Kui see on tehtud, võib hankija konto kustutada. Seda teeb tavaliselt ostureskontro osakond.  


