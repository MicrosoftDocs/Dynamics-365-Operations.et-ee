---
title: Konfiguratsiooni pakkujate loomine ja nende märkimine aktiivseks
description: Selles teemas selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua konfiguratsiooni pakkuja elektroonilise aruandluse (ER) puhul rakenduses Dynamics 365 for Finance and Operations.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d6df2068f99a42764fc13f282a7c38099109e06
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887083"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Konfiguratsiooni pakkujate loomine ja nende märkimine aktiivseks

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles teemas selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua konfiguratsiooni pakkuja elektroonilise aruandluse (ER) puhul rakenduses Dynamics 365 for Finance and Operations. Iga elektroonilise aruandluse konfiguratsioon viitab pakkujale kui konfiguratsiooni autorile. Selles näites loote konfiguratsiooni pakkuja näidisettevõttele Litware, Inc. Neid etappe teha mis tahes ettevõttes, kuna ER-konfiguratsiooni pakkujate on kõigil ettevõtetel ühised.

## <a name="create-a-provider"></a>Pakkuja loomine
1. Avage ülemises vasakpoolses nurgas **Navigeerimispaan** ja valige **Organisatsiooni administreerimine**.
2. Avage **Tööruumid > Elektrooniline aruandlus**.
3. Avage **Seotud lingid > Konfiguratsiooni pakkujad**.
4. Valige suvand **Uus**.
    - Pakkuja kirjel on kordumatu nimi ja URL. Vaadake selle lehe sisu üle ja jätke see protseduur vahele, kui kirje Litware, Inc.-i (https://www.litware.com) kohta on juba olemas.  
5. Trükkige nime väljale `Litware, Inc.`.
6. Sisestage internetiaadressi väljale väärtus `https://www.litware.com`.
7. Valige käsk **Salvesta**.
8. Sulgege leht.

## <a name="select-as-an-active-provider"></a>Valimine aktiivse pakkujana
1. Valige pakkuja Litware, Inc.
2. Valige **Määra aktiivseks**.

![Elektroonilise aruandluse tööruumi leht](../media/GER-Task-ActiveProvider-1.png)
