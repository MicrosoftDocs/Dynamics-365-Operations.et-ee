--- 
title: "Kaupade vastuvõtu registreerimine ostutellimusel"
description: "See protseduur näitab, kuidas kaupade sissetulekut otse ostutellimusel registreerida."
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9b2300a593c9e153ee598fa72e29907c82f2b79e
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Kaupade vastuvõtu registreerimine ostutellimusel

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas kaupade sissetulekut otse ostutellimusel registreerida. Võimalik on registreerida toote sissetulek ka laos ja siis hiljem ostutellimusel. Selle toimingu teeb tavaliselt ostuagent või ostureskontro koordinaator. Selles juhendis toodud näidet saab kasutada demoandmete ettevõtte USMF puhul. Näites on toimingud lihtsa ostutellimuse koostamiseks, et saaksite esitada protseduuri tegevusjuhisena. Kui kasutaksite protseduuri oma andmetega, tuleks alustada alamülesandest Kaupade vastuvõtu registreerimine.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Uue ostutellimuse koostamine kaupade vastuvõtmiseks
1. Avage Hanked > Ostutellimused > Kõik ostutellimused.
2. Klõpsake valikut Uus.
3. Sisestage väljale Hankija konto väärtus US-101.
4. Klõpsake nuppu OK.
5. Sisestage väljale Kauba kood väärtus M0001.
6. Sisestage väljale Kogus number 5.
7. Klõpsake toimingupaanil valikut Ost.
8. Klõpsake käsku Kinnita.

## <a name="record-receipt-of-goods"></a>Kaupade vastuvõtu salvestamine
1. Klõpsake toimingupaanil valikut Vastuvõtt.
2. Klõpsake valikut Toote sissetulek.
    * Koguse väli võimaldab teha erinevaid valikuid koguse kohta, mida soovite vastu võtta. Näiteks kui kogus on eelnevalt laos registreeritud, võite teha valiku Registreeritud kogus.  Selle näite puhul kasutage väärtust Tellitud kogus.   
3. Sisestage suvaline väärtus väljale Toote sissetulek.
    * Seda välja kasutatakse viite sisestamiseks, mida kasutatakse toote sissetuleku töölehe kandena.  
4. Laiendage jaotist Read.
5. Määrake koguse väärtuseks 4.
    * Siin saate määrata käsitsi koguse, mida iga tellimuse rea puhul vastu võetakse.  
6. Ahendage jaotist Read.
7. Klõpsake nuppu OK.
    * Kaup on nüüd ostutellimusel vastuvõetuks registreeritud ja seda kajastava dokumendina on loodud toote sissetuleku tööleht. Saate kasutada toimingut Toote sissetulek ostutellimuse juurde loodud töölehtede ülevaatamiseks, et näha, mis millal vastu võeti.  


