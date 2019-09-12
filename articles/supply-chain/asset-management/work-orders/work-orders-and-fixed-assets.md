---
title: Töökäsud ja põhivarad
description: Selles teemas selgitatakse töökäske ja põhivarasid varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f03b7fa073c4e5338b7b5681ba7b8c9fe00a657b
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875603"
---
# <a name="work-orders-and-fixed-assets"></a>Töökäsud ja põhivarad


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Varahalduses võivad varad olla seotud põhivaradega ja te saate luua nende varade jaoks töökäske. Selle funktsiooni kasutamisel saate täieliku ülevaate põhivaradest, seotud investeerimisprojektidest ja investeerimisprojektide kohta registreeritud kuludest moodulis **Projekti haldus-ja raamatupidamine** ning moodulis **Põhivarad** rakenduses Dynamics 365 for Finance and Operations.

>[!NOTE]
>Väli **Põhivara number** täidetakse ainult töökäsu tööprojektis, kui projektitüübiks on töökäsu projektis valitud "Investeering".

![Joonis 1](media/24-work-orders.png)

Järgmises toimingus kirjeldatakse varade, töökäskude, töökäskude tööprojektide ja põhivarade vahelist seost.

1. Loote vara, mis on seotud põhivaraga, nagu näidatud alloleval joonisel.

![Joonis 2](media/25-work-orders.png)

2. Kui seadistate töötellimuse tüüpe (**Varahaldus** > **Seadistus** > **Töökäsud** > **Töökäskude tüübid**), loote investeeringute käsitlemiseks töökäsu tüübi. Vt ka [Töökäskude tüübid](../setup-for-work-orders/work-order-types.md).

![Joonis 3](media/26-work-orders.png)

3. Kui seadistate Töökäskude projektigrupid (**Varahaldus** > **Seadistus** > **Töökäsud** > **Projekti seadistus** > **Projektigrupp** link), loote seose investeeringuteks kasutatava töökäsu tüübi ja projektigrupi, mis on loodud investeeringuteks moodulis **Projektihaldus ja raamatupidamine**, vahel (**Projektihaldus ja raamatupidamine** > **Seadistus** > **Postitamine** > **Projektigrupid**).

![Joonis 4](media/27-work-orders.png)

4. Kui loote töökäsu, mis on seotud põhivara objektiga, valite investeeringute käsitlemiseks kasutatava töökäsu tüübi (nt "Investeering").

5. Töökäsu loomisel kuvatakse seotud töökäsu tüüp kaardil **Kõik töökäsud**.

![Joonis 5](media/28-work-orders.png)

6. Kui töökäsk on loodud, luuakse töökäsuga seotud projekt kaardil **Projektihaldus ja raamatupidamine** > **Kõik projektid**. Projektiga seotud teavet saate vaadata, kui klõpsate töökäsu lingil **Projekti ID** ( **Varahaldus**, avage töökäsk üksikasjade vaates > **Rea üksikasjad** FastTab > vahekaart **Üldine** > väli **Projekti ID**).

![Joonis 6](media/29-work-orders.png)

7. Vahekaardil **Põhivarad** saate vaadata põhivaraga seotud projektide ülevaadet (**Põhivarad** > **Põhivarad** > **Põhivarad** > klõpsake väljal **Põhivara number** põhivaral > vaadake sisu paneelil **Seotud teave** > jaotises **Seotud projektid**).

