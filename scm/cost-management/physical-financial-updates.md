---
title: "Füüsilised ja finantsilised värskendamised"
description: "Käesolev teema annab ülevaate selle kohta, millised kande tüübid suurendavad või vähendavad laokoguseid."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d68006c756f6b29804cad1d05db9ced2bd33897d
ms.lasthandoff: 03/31/2017


---

# <a name="physical-and-financial-updates"></a>Füüsilised ja finantsilised värskendamised

Käesolev teema annab ülevaate selle kohta, millised kande tüübid suurendavad või vähendavad laokoguseid. 

Laokannete saab füüsiliselt uuendatud ja rahaliselt värskendada Microsoft Dynamics 365 toiminguteks. Mõnd tüüpi füüsilised ja finantsilised kanded suurendavad varude koguseid ja mõned teised tüübid vähendavad koguseid.

## <a name="physical-increases"></a>Füüsiline suurendamine
Kui füüsiline kanne on sisestatud, on kande kirje olek **Vastu võetud**. Järgmisi kandeid peetakse füüsilisteks tõusudeks:

-   Ostutellimuse sissetulek
-   Müügitellimuse saatelehe tagastus
-   Tootmistellimuse lõpetatuks kinnitamine
-   Kõrvalsaadus tootmistellimuse komplekteerimislehel

## <a name="financial-increases"></a>Rahaline suurendamine
Kui finantsilise sissetuleku kanne on sisestatud, on kogust suurendava kande kirje olek **Ostetud**. Järgmisi kandeid peetakse finantsilisteks tõusudeks:

-   Hankijaarve
-   Müügitellimuse arve tagastuseks
-   Tootmistellimuse omahinna arvutamine
-   Positiivse koguse laotöölehed, nt liikumine, kasum ja kaotus, inventuur, kooslus ja üleviimine

## <a name="transactions-that-increase-quantity"></a>Kanded, mis suurendavad kogust
Kogust suurendavad kanded sisestatakse jooksva keskmise omahinnaga. Dynamics 365 operatsioonide arvutab maksumus iga kõnealuste tehingute iga laodimensiooni, millega jälgitakse rahaliselt põhineva töötab keskmine omahind. Lisateavet jooksva keskmise omahinna kohta vt jaotisest [Jooksev keskmine omahind](running-average-cost-price.md).

## <a name="transactions-that-decrease-quantity"></a>Kanded, mis vähendavad kogust
Dynamics 365 operatsioonide kasutab arvutatud töötab keskmise omahinna kanne, mille kogus väheneb konteerimisel, sõltumata varude mudel, mis on seotud nimestikku. Kogust vähendav kanne ei tohi enne sisestamist teise kande juurde märgitud olla. Kui tegelik vaba laoseis muutub negatiivseks, Dynamics 365 operatsioonide kasutab määratletud kauba varude maksumuse ning **kauba** lehel. **Märkus.** Kui mitme asukoha funktsioon on lubatud, on see kulu asukohale lehel **Tellimuse vaikesätted** määratud varude kulu.

## <a name="physical-issues-vs-financial-issues"></a>Füüsilised väljaminekud vs rahalised väljaminekud
Kui füüsilise väljamineku kanne on sisestatud, on kande kirje olek **Maha arvatud**. Järgmisi kandeid peetakse füüsilisteks väljaminekuteks:

-   Tootmistellimuse komplekteerimislehe tööleht
-   Müügitellimuse saateleht
-   Ostutellimuse saatelehe tagastus

Kui finantsiline kanne on sisestatud, on kande kirje olek **Müüdud**. Järgmisi kandeid peetakse füüsilisteks väljaminekuteks:

-   Tootmistellimuse lõpetamine
-   Müügitellimuse arve
-   Hankija arve tagastus
-   Negatiivse koguse laotöölehed, nt liikumine, kasum ja kaotus, inventuur, kooslus ja üleviimine

Kogust vähendavad kanded sisestatakse jooksva keskmise omahinnaga. Seega on vajalik laosulgemisprotseduur väljaminekukannete tasakaalustamiseks sissetulekukannetega igale kaubale määratud laomudeli alusel.


