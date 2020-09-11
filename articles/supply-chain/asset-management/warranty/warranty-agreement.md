---
title: Garantiilepingud
description: Selles teemas selgitatakse garantiilepinguid varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f049165fd12dfae672293e0c30ddb186ad3ed12c
ms.sourcegitcommit: 18c5ef10e311f3dd2dbf45c6439ae6beff921af8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/24/2020
ms.locfileid: "3719234"
---
# <a name="warranty-agreements"></a>Garantiilepingud

[!include [banner](../../includes/banner.md)]

 


Varahalduses saate seadistada garantii tingimused, mida saab siduda vara või varatüübiga. Garantiitingimused luuakse kindla perioodi kohta. Garantii saab seadistada nii, et see võimaldaks täielikku katvust või osalist katvust, ning saate seadistada tundide, kulude ja kaupadega seotud tingimused.

Esimene samm on luua hankija garantiilepingud, mis teil on oma varustuse jaoks. Seejärel lisage varade või varatüüpide garantiilepingud. Hankija garantiilepinguid kasutatakse ainult informatiivsel eesmärgil. Kui hankija garantii on seadistatud varale, saate vaadata vara garantii laovarude perioodi.

## <a name="create-a-warranty-agreement"></a>Garantiilepingu loomine

Garantiileping võib sisaldada mitut lepingurida, mis katavad tööaja, kulude ja kaupade garantii.

1. Valige **Varahaldus** \> **Seadistus** \> **Varad** \> **Garantii**.
2. Valige **Uus**, et luua uus toode.
3. Sisestage garantii ID väljale **Garantii**. 
4. Väljale **Nimi** sisestage kirjeldus.

    Kiirkaardil **Üksikasjad** kuvatakse väljal **Varad** aktiivsete varade arv, mis kasutavad garantiilepingut.

5. Järgige kiirkaardil **Garantiiread** neid toiminguid garantiilepingusse kaasatavate ridade lisamiseks.

    1. Valige suvand **Lisa rida**, et lisada garantiile uus tingimus. Väljale **Rida** sisestatakse automaatselt seerianumber.
    2. Valige garantiiperioodi tüüp väljal **Periood**.
    3. Sisestage number väljale **Intervall**. See väli määratleb perioodide arvu, millele garantii peaks kehtima.
    4. Sisestage väljale **Protsent** garantii rea laovarude protsent. Protsent näitab, kui palju teie ettevõte katab.

![Garantiileht](media/01-warranty.png)
