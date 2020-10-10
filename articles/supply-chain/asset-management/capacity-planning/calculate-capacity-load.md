---
title: Täiskoormuse arvutamine
description: Selles teemas tutvustatakse, kuidas arvutada täiskoormust varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCapacityLoad, EntAssetWorkOrderCapacityLoadCalculate, EntAssetWorkOrderCapacityLoad
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5015955338a4cbc2b51585d6297756f20dccee8b
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888734"
---
# <a name="calculate-capacity-load"></a>Arvuta täiskoormus

[!include [banner](../../includes/banner.md)]


Varahalduses saate arvutada täiskoormust järgmiste näitajate kohta:

- hooldusgraafiku read  
- töökäsud, mida pole veel plaanitud  
- plaanitud töökäsud

See on kasulik, kui soovite saada ülevaate konkreetse perioodi oodatavast täiskoormusest. Täiskoormuse arvutuse saab teha kõigile varadele või valitud varadele. Samuti saate teha arvutuse hoolduskatkestuse toimingute või töökäsu kaustade kohta.

1. Klõpsake **Varahaldus** > **Päringud** > **Täiskoormus** või **Varahaldus** > **Üldine** > **Töökäsu kaustad** > **Kõik töökäsu kaustad** / **Aktiivsed töökäsu kaustad** > valige loendist töökäsu kaust > nupp **Täiskoormus** või **Varahaldus** > **Üldine** > **Hoolduskatkestuse toimingud** > **Kõik hoolduskatkestuse toimingud** / **Aktiivsed hoolduskatkestuse toimingud** > valige loendist hooldustoiming > nupp **Täiskoormus**.

2. Dialoogiboksis **Arvuta täiskoormus** valige arvutuse periood väljadel **Alguskuupäev/aeg** ja **Lõppkuupäev/aeg**.

3. Valige "Jah" tumblernupul **Kaasa hooldusgraafik**, kui soovite arvutusse kaasata hooldusgraafiku read.

4. Valige "Jah" tumblernupul **Kaasa töökäsk**, kui soovite arvutusse kaasata töökäsu tööd.

5. Saate kasutada välja **Tase**, et näidata kui üksikasjalikke töö asukohtade täiskoormuse ridu te soovite. 

    Kui sisestate väljale näiteks arvu "1" ja teil on mitmetasandiline töö asukoha struktuur, kuvatakse ülemisel tasemel kõik töö asukoha hooldusgraafiku read ja töökäsud ning seetõttu võivad tunnid real olla lisatud ülespoole töö asukohtades, mis asuvad madalamal tasemel. 
    
    Kui sisestate väljale **Tase** arvu "0", näete üksikasjalikku tulemust, mis näitab kõiki hooldusgraafiku ridu ja kõiki töökäske kõigi töö asukohtade tasemete kohta, millega nad on seotud.

6. Arvutuse alustamiseks klõpsake **OK**.

7. Gruppides **Rühmitusalus** klõpsake asjakohastele nuppudele, et näidata arvutuse soovitud üksikasja taset. Alloleval kuvatõmmisel on gruppide **Rühmitusalus** nupud esile tõstetud sinise värviga. Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.

    ![Joonis 1](media/01-capacity-planning.png)

>[!NOTE]
>Kui soovite keskenduda ainult planeeritud töökäskude võimsuse planeerimisele, vaadake teemat [Täiskoormuse arvutamine plaanitud töökäskude kohta](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).

