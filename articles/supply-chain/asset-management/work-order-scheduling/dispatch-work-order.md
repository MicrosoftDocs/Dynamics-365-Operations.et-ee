---
title: Lähetage töökäsk
description: Selles teemas tutvustatakse, kuidas lähetada töökäsku varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetScheduledExecution
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d46beb04923d06aa8ccec05355731aa1b3f27c5b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426082"
---
# <a name="dispatch-work-order"></a>Lähetage töökäsk

[!include [banner](../../includes/banner.md)]

 

Saate ajastada ühe töökäsu või selle töid ühele töötajale funktsiooni **Lähetus** kaudu.

1. Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik Töökäsud** või **Aktiivsed töökäsud**.

2. Valige loendist töökäsk.

3. Klõpsake vahekaardil **Üldine** suvandit **Lähetus**.

4. Valige dialoogi **Plaani töökäsk** väljal **Töötaja** töötaja.

5. Välja **Ajasta töötunde** saate sisestada eeldatavad töötunnid, kui need erinevad eelarve tundidest.

6. Vajaduse korral saate väljal **Kavandatud algus** muuta alguskuupäeva ja kellaaega.

7. Kui kavandamisprotsess peaks jälgima teistele töödele juba kavandatud ressursside võimsuse piiranguid, veenduge et tumblernuppude **Vara**, **Tööriist** ja **Töötaja** väärtus on **Jah**. Kui soovite näha üksikasjalikumat teavet kavandamisprotsessi kohta, valige tumblernupu **Sõnaohter** väärtuseks **Jah**. See tähendab, et töökäsu arvutatud skooride üksikasjalikku teavet näidatakse Infologis.

8. Kalendris suletud päevade eiramiseks valige tumblernupu **Eira kava** väärtuseks **Jah** (kehtib vara, töötaja ja tööriistade osas). Valige tumblernupu **Eira käivitamisajakava** väärtuseks **Jah**, et eirata piiranguid, mis võivad olla valitud kavandamise töökäsus. 

    Käitamisajakava seadistamise teabe leiate jaotisest [Käitamisajakava](../setup-for-work-orders/scheduled-execution.md).

9. Klõpsake valikut **OK**. Töökäsu töötsükli olekut värskendatakse ise vastavalt **Kavandatud** töötsükli olekule, mis on määratud kohas **Varahaldus** > **Seadistus** > **Töökäsud** > **Töötsükli mudelid**.

Alloleval joonisel kuvatakse näidet lähetuse valikutest dialoogis **Töökäsu kavandamine**.

![Joonis 1](media/04-work-order-scheduling.png)

[!NOTE]
Töökäsu ajakava kustutamiseks valige töökäsk kohas **Kõik töökäsud** ja seejärel klõpsake vahekaardil **Üldine** valikut **Kustuta ajakava**. Ärge unustage ajakava kustutamisel värskendada käsitsi töökäsu töötsükli olekut.

