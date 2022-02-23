---
title: Rea kauba töövoogude konfigureerimine
description: Selles teemas selgitatakse, kuidas konfigureerida rea kauba töövoo elementi.
author: ChrisGarty
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c19693151399fc02ea9562757af7fc24124c9b6c
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798825"
---
# <a name="configure-line-item-workflows"></a>Rea kauba töövoogude konfigureerimine

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas konfigureerida rea kauba töövoo elementi.

Töövooredaktoris rea kauba töövoo elemendi konfigureerimiseks paremklõpsake elementi ja seejärel klõpsake valikut **Atribuudid**, et avada leht **Atribuudid**. Seejärel kasutage rea kauba töövoo elemendi atribuutide konfigureerimiseks järgmisi protseduure.

## <a name="name-the-line-item-workflow-element"></a>Rea kauba töövoo elemendile nime andmine

Tehke rea kauba töövoo elemendile nime sisestamiseks järgmist.

1. Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2. Sisestage väljale **Nimi** rea kauba töövoo elemendi jaoks kordumatu nimi.

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a>Määrake, kas sama töövoogu kasutatakse kõigi rea kaupade töötlemiseks.

Järgige neid etappe, et määrata, kas sama töövoogu kasutatakse dokumendi kõigi rea kaupade töötlemiseks.

1. Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2. Kui sama töövoog peab töötlema dokumendi kõiki rea kaupu, klõpsake valikut **Kutsu üksik töövoog kõigile rea kaupadele**. Seejärel valige töövoog, millega rea kaupu töödelda.
3. Kui teatud töövoog peaks töötlema rea kaupu, mis vastavad määratud tingimustele, klõpsake valikut **Kutsu töövoog igale rea kaubale**. Järgige neid etappe tingimustekogumi määratlemiseks.

    1. Klõpsake vahekaarti **Lisa**.
    2. Valige tabelist tingimus.
    3. Sisestage vahekaardil **Tingimuse nimi** määratletava tingimustekogumi nimi.
    4. Tingimuse sisestamiseks klõpsake valikut **Lisa tingimus**.
    5. Sisestage täiendavad vajalikud tingimused.
    6. Kontrollimaks, kas sisestatud tingimustekogum on õigesti konfigureeritud, klõpsake käsku **Katseta**. Lehel **Töövoo tingimuse katsetamine** alas **Kontrolli tingimust** valige kirje ja seejärel klõpsake käsku **Katseta**. Süsteem hindab kirjet otsustamaks, kas see vastab teie määratud tingimustele. Klõpsake **OK** või valikut **Tühista**, et naasta lehele **Atribuudid**.

    Vahekaardil **Töövoog** valige töövoog, mida kasutada teie määratletud tingimustekogumile vastavate rea kaupade töötlemiseks.
