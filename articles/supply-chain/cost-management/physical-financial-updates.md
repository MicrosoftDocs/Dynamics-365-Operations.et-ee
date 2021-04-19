---
title: Füüsilised ja finantsilised värskendamised
description: Käesolev teema annab ülevaate selle kohta, millised kande tüübid suurendavad või vähendavad laokoguseid.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88432b9a5e564f9e81892e0bb379f95ff40d6c9d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842149"
---
# <a name="physical-and-financial-updates"></a>Füüsilised ja finantsilised värskendamised

[!include [banner](../includes/banner.md)]

Käesolev teema annab ülevaate selle kohta, millised kande tüübid suurendavad või vähendavad laokoguseid. 

Laokandeid saab füüsiliselt värskendada ja finantsiliselt värskendada rakenduses Dynamics 365 Supply Chain Management. Mõnd tüüpi füüsilised ja finantsilised kanded suurendavad varude koguseid ja mõned teised tüübid vähendavad koguseid.

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
Kogust suurendavad kanded sisestatakse jooksva keskmise omahinnaga. Arvutatud jooksev keskmine omahind põhineb iga finantsiliselt jälgitava varude dimensiooni iga kande kulul. Lisateavet jooksva keskmise omahinna kohta vt jaotisest [Jooksev keskmine omahind](running-average-cost-price.md).

## <a name="transactions-that-decrease-quantity"></a>Kanded, mis vähendavad kogust
Arvutatud keskmist jooksvat omahinda kasutatakse siis, kui sisestatakse kanne, mis vähendab kogust, sõltumata sellest, milline varude mudel on selle laovaruga seostatud. Kogust vähendav kanne ei tohi enne sisestamist teise kande juurde märgitud olla. Kui füüsiline vaba kaubavaru muutub negatiivseks, kasutatakse kaubale lehel **Kaup** määratud laokulu. 

> [!NOTE]
> Kui mitme asukoha funktsioon on lubatud, on see kulu asukohale lehel **Tellimuse vaikesätted** määratud varude kulu.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]