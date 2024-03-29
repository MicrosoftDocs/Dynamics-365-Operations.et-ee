---
title: Saate konfigureerida toote, mida soovite tasuta müüa
description: See artikkel kirjeldab, kuidas konfigureerida toodet nii, et seda saab osta tasuta sisse Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 88370085de047a5e0be773dde218770cfa242d14
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280360"
---
# <a name="configure-a-product-to-be-purchased-for-free"></a>Saate konfigureerida toote, mida soovite tasuta müüa

[!include [banner](includes/banner.md)]


See artikkel kirjeldab, kuidas konfigureerida toodet nii, et seda saab osta tasuta sisse Microsoft Dynamics 365 Commerce.

## <a name="configure-the-product"></a>Toote konfigureerimine

Toote müümiseks tasuta Dynamics 365 Commerce peate selle hinna väärtuseks määrama 0 (null). Lisaks peate konfigureerima toote **nullhinna kehtiva** sätte.

Commerce Headquarters`is **nullhinna kehtiva** sätte konfigureerimiseks järgige neid samme.

1. Tehke valik **Jaemüük ja kaubandus \> Tooted ja kategooriad \> Väljastatud tooted kategooria järgi**.
1. Minge tootele, mida soovite tasuta müüa. 
1. Tootelehe **Ettevõte** jaotises määrake suvandi **Nullhind kehtib** väärtusele **Jah**.

Järgmine illustratsioon näitab toodet, kus suvandi **Nullhind kehtib** väärtuseks on seatud **Jah**.

![Näide toote kohta, kus suvandile nullhind on väärtuseks seatud jah.](./media/Zero-price.png)

## <a name="configure-the-online-stores-functionality-profile"></a>Konfigureerige e-poe funktsiooniprofiil

Enne kui vaba kandeid saab töödelda, peate konfigureerima sätte **Luba väljaregistreerimine ilma makseta** sätte jaoks funktsiooniprofiili nii, et tasutavad kanded ei ole lubatud. Lisateavet funktsiooniprofiilide loomise kohta vt teemast [Võrgufunktsioonide profiili loomine](online-functionality-profile.md).

Commerce Headquarters`is **Luba väljaregistreerimine ilma makseta** sätte konfigureerimiseks järgige neid samme.

1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus**.
1. Häälestage oma kaupluse funktsiooniprofiili lehel **väljaregistreerimise** jaotises suvand **Luba väljaregistreerimine ilma makseteta** suvandile **Jah**.

Järgmine näide näitab näidet võrgupoe profiili kohta, kus valik **Luba väljaregistreerimine ilma makseta** on seatud väärtusele **Jah**.

![Näide selgitab näidet võrgupoe profiili kohta, kus valik luba väljaregistreerimine ilma makseta on seatud väärtusele jah.](./media/Zero-price-profile.png)

## <a name="additional-resources"></a>Lisaressursid

[Jaemüügihinna haldamine](price-management.md)

[Funktsiooniprofiili loomine võrgus](online-functionality-profile.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
