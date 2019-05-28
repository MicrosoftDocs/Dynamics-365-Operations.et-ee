---
title: Füüsilised ja finantsilised värskendamised
description: Käesolev teema annab ülevaate selle kohta, millised kande tüübid suurendavad või vähendavad laokoguseid.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ba628dbf63d3b124583e6b873530f1459b07562
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547882"
---
# <a name="physical-and-financial-updates"></a>Füüsilised ja finantsilised värskendamised

[!include [banner](../includes/banner.md)]

Käesolev teema annab ülevaate selle kohta, millised kande tüübid suurendavad või vähendavad laokoguseid. 

Laokandeid saab füüsiliselt värskendada ja finantsiliselt värskendada rakenduses Microsoft Dynamics 365 for Finance and Operations. Mõnd tüüpi füüsilised ja finantsilised kanded suurendavad varude koguseid ja mõned teised tüübid vähendavad koguseid.

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
Kogust suurendavad kanded sisestatakse jooksva keskmise omahinnaga. Finance and Operations arvutab jooksva keskmise omahinna, mis põhineb iga finantsiliselt jälgitava varude dimensiooni iga kande kulul. Lisateavet jooksva keskmise omahinna kohta vt jaotisest [Jooksev keskmine omahind](running-average-cost-price.md).

## <a name="transactions-that-decrease-quantity"></a>Kanded, mis vähendavad kogust
Finance and Operations kasutab arvutatud keskmist jooksvat omahinda, kui sisestatakse kanne, mis vähendab kogust, sõltumata sellest, milline varude mudel on selle laovaruga seostatud. Kogust vähendav kanne ei tohi enne sisestamist teise kande juurde märgitud olla. Kui füüsiline vaba kaubavaru muutub negatiivseks, kasutab Finance and Operations kaubale lehel **Kaup** määratud laokulu. **Märkus.** Kui mitme asukoha funktsioon on lubatud, on see kulu asukohale lehel **Tellimuse vaikesätted** määratud varude kulu.

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



