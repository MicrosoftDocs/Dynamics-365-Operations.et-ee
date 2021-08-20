---
title: Lähetage töökäsk
description: Selles teemas tutvustatakse, kuidas lähetada töökäsku varahalduses.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetScheduledExecution
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 87f67f4db143fabbfae926e30e7e5d97ac6af0f6fa5469218e4ab3605aa44dcb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778720"
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

![Joonis 1.](media/04-work-order-scheduling.png)

[!NOTE]
Töökäsu ajakava kustutamiseks valige töökäsk kohas **Kõik töökäsud** ja seejärel klõpsake vahekaardil **Üldine** valikut **Kustuta ajakava**. Ärge unustage ajakava kustutamisel värskendada käsitsi töökäsu töötsükli olekut.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]