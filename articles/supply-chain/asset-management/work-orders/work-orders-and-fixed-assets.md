---
title: Töökäsud ja põhivarad
description: See artikkel selgitab varahalduses töötellimusi ja põhivarasid.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9a6b9cf8327f65371f8362a5729bb32746d900cd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885982"
---
# <a name="work-orders-and-fixed-assets"></a>Töökäsud ja põhivarad

[!include [banner](../../includes/banner.md)]


Varahalduses võivad varad olla seotud põhivaradega ja te saate luua nende varade jaoks töökäske. Selle funktsiooni kasutamisel saate täieliku ülevaate põhivaradest, seotud investeerimisprojektidest ja investeerimisprojektide kohta registreeritud kuludest moodulites **Projektihaldus ja -arvestus** ning **Põhivarad** rakenduses Microsoft Dynamics 365 for Finance and Operations.

>[!NOTE]
>Väli **Põhivara kood** seatakse töökäsu tööprojektis ainult juhul, kui töökäsu tööprojektis on projektitüübiks valitud **Investeering**.

Alltoodud joonis näitab mooduli **Projektihaldus ja -arvestus** investeerimisprojekti ja töökäsu tööprojekti vahelist seost.

![Joonis 1.](media/24-work-orders.png)

Järgmises toimingus kirjeldatakse varade, töökäskude, töökäskude tööprojektide ja põhivarade vahelist seost.

1. Loote vara, mille seostate mõne põhivaraga.

![Joonis 2.](media/25-work-orders.png)

2. Kui seadistate töökäsu tüüpe lehel **Töökäsu tüübid** (**Varahaldus** > **Seadistus** > **Töökäsud** > **Töökäsu tüübid**), loote investeeringute käitlemiseks töökäsu tüübi. Vt ka [Töökäskude tüübid](../setup-for-work-orders/work-order-types.md).

![Joonis 3.](media/26-work-orders.png)

3. Kui seadistate Töökäskude projektigrupid lehe **Töökäsu projekti seadistamine** vahekaardil **Projektigrupp** (**Varahaldus** > **Seadistus** > **Töökäsud** > **Projekti seadistus**), loote seose investeeringuteks kasutatava töökäsu tüübi ja projektigrupi, mis on investeeringuteks loodud mooduli **Projektihaldus ja -arvestus** lehel **Projektigrupid** (**Projektihaldus ja -arvestus** > **Seadistus** > **Sisestamine** > **Projektigrupid**).

![Joonis 4.](media/27-work-orders.png)

4. Kui loote töökäsu, mis on seotud põhivaraga, valite investeeringute käitlemiseks kasutatava töökäsu tüübi, näiteks **Investeering**.

5. Töökäsu loomisel kuvatakse seotud töökäsu tüüp lehel **Kõik töökäsud**.

![Joonis 5.](media/28-work-orders.png)

6. Kui töökäsk on loodud, siis luuakse töökäsuga seotud projekt mooduli **Projektihaldus ja -arvestus** lehel **Kõik projektid** (**Projektihaldus ja -arvestus** > **Projektid** > **Kõik projektid**). Projektiga seotud teabe vaatamiseks valige mooduli **Varahaldus** lehe **Kõik töökäsud** üksikasjade vaates kiirkaardi **Rea üksikasjad** vahekaardi **Üldine** väljal **Projekti ID** kuvatud link (**Varahaldus** > **Üldine** > **Töökäsud** > **Kõik töökäsud**).

![Joonis 6.](media/29-work-orders.png)

7. Põhivaraga seotud projektide ülevaate vaatamiseks valige **Põhivarad** > **Põhivarad** > **Põhivarad**, seejärel valige väljal **Põhivara kood** üksikasjade vaate avamiseks soovitud põhivara link. Laiendage lehe paremas servas paan **Seostuv teave** ja valige kiirkaart **Seotud projektid**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]