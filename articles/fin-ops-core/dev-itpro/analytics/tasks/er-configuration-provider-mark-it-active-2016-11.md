---
title: Konfiguratsiooni pakkujate loomine ja nende märkimine aktiivseks
description: See artikkel selgitab, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollile määratud kasutaja saab luua konfiguratsioonipakkuja.
author: kfend
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
ms.openlocfilehash: db5226720a4e0c0f167921a972429c0a5ecdd2e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267809"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a>Konfiguratsiooni pakkujate loomine ja nende märkimine aktiivseks

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollile määratud kasutaja saab luua konfiguratsioonipakkuja elektroonilise aruandluse jaoks (ER). Iga elektroonilise aruandluse konfiguratsioon viitab pakkujale kui konfiguratsiooni autorile. Selles näites loote konfiguratsiooni pakkuja näidisettevõttele Litware, Inc. Neid etappe teha mis tahes ettevõttes, kuna ER-konfiguratsiooni pakkujate on kõigil ettevõtetel ühised.

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

![Elektroonilise aruandluse tööruumi leht.](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
