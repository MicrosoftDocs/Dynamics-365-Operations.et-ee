---
title: Hooldusprognoosid
description: Selles teemas tutvustatakse hooldusprognoose varahalduses.
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
ms.openlocfilehash: 1a416bbb79be3f25998d3c0da8d231d0df808685
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875612"
---
# <a name="maintenance-forecasts"></a>Hooldusprognoosid

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Kui loote töökäsu, loote töökäsu tööd koos asjakohaste varade ja hooldustööde tüüpidega. Kui valite hooldusprognoosi sisaldava hooldustöö tüübi, kopeeritakse prognoosid automaatselt töökäsku.

Saate töökäsule prognoosi ridu lisada või neid kustutada. Töökäsu töötsükli oleku, asjakohase projekti tüübi ja projekti tüübiga seotud etapi reeglite seadistus määrab selle, kas saate prognoosi ridu lisada või redigeerida. 

1. Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.

2. Valige loendist töökäsk ja klõpsake **Prognoos**. Jaotises **Töökäsu hooldusprognoos** kuvatakse töökäsu tööl valitud hooldustöö tüüpi prognoosi ridu.


## <a name="add-hours-forecast-to-a-work-order"></a>Tundide prognoosi lisamine töökäsule

1. Valige töökäsu töö, millele soovite prognoosi lisada.

2. Klõpsake uue rea loomiseks kiirkaardil **Tunnid** suvandit **Lisa**.

3. Valige kategooria väljal **Kategooria**.

4. Sisestage väljale **Tunnid** prognoositud tundide arv.

5. Valige real kasutatav kulu tüüp väljal **Rea atribuut**.


## <a name="add-items-forecast-to-a-work-order"></a>Üksuste prognoosi lisamine töökäsule

Üksuste lisamiseks töökäsu hooldusprognoosile on kolm võimalust: võite luua read üksustele (varuosadele), mis ei sisaldu varuosade loendis või vara koosluses, võite valida varuosi kinnitatud varuosade loendist ja võite valida üksuseid vara kooslusest.

1. Valige töökäsu töö, millele soovite prognoosi lisada.

2. Valige kiirkaart **Üksused**.

3. Klõpsake varuosade loendis või vara koosluses mittesisalduva varuosa jaoks uue rea loomiseks suvandil **Lisa**.

4. Valige kaup väljal **Kaubakood**.

5. Sisestage kogus väljale **Müügi kogus** ja valige koguse üksus väljal **Üksus**.

6. Sisestage omahind ja valuuta vastavatele väljadele ja valige **Rea atribuut**.

7. Kui soovite muuta üksuse ridadel kuvatavate mõõtude loendit, klõpsake **Varud** > **Kuva mõõdud**, valige mõõdud ja valige tumblernupul **Salvesta seadistus** suvand "Jah".

8. Kui soovite hooldusprognoosile lisada kinnitatud varuosa, klõpsake suvandit **Lisa varuosad**, valige varuosa, redigeerige vajadusel sellega setud andmeid ja klõpsake **OK**.

9. Kui soovite hooldusprognoosile lisada vara koosluse üksusi, klõpsake suvandit **Lisa koosluse üksusi**, valige üksus, redigeerige vajadusel sellega setud andmeid ja klõpsake **OK**.

10. Kui soovite saada ülevaadet, kus valitud rea üksust varahalduses seoses varade, vaikimisi hooldustöö tüüpide, varuosade ja töökäskudega kasutatakse, klõpsake suvandit **Üksus kus kasutatud**. 



## <a name="add-expense-forecast-to-a-work-order"></a>Kuluprognoosi lisamine töökäsule

1. Selles teemas kirjeldatakse töökäsule kuluprognoosi lisamist. Valige vormi vasakult poolelt töökäsu töö, millele soovite prognoosi lisada.

2. Valige kiirkaart **Kulu**.

3. Uue rea loomiseks klõpsake **Lisa**.

4. Valige kategooria väljal **Kategooria**.

5. Sisestage kogus väljale **Kogus**.

6. Sisestage omahind ja müügi valuuta ja müügihind vastavatele väljadele.

7. Valige real kasutatav kulu tüüp väljal **Rea atribuut**.

>[!NOTE]
>Kiirkaardil **Hooldusprognoosi kogusummad** võite näha valitud töökäsu töö ja töökäsu igale vahekaardile loodud ridade arvu ülevaadet. Samuti näete töökäsu töö ja töökäsu prognoositud töötundide summat.

![Joonis 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>Töökäsu prognooside automaatne värskendamine

Varahalduses saate mistahes tunnikulude, üksuse kulude ja teistes rakenduse Dynamics 365 for Finance and Operations moodulites värskendatud kuludega seotud töökäsu prognooside muudatusi automaatselt värskendada. Seda tehakse selleks, et kindlustada töökäsu prognoosides alati uusimate omahindade kasutamine. Sarnaseid värskendusi on võimalik teha ka [hooldustöö tüübi prognoosidele](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

1. Klõpsake **Varahaldus** > **Perioodiline** > **Prognoos** > **Värskenda töökäsu prognoosi**.

2. Rippdialoogis **Töökäsu prognoosi värskendamine** saate vajadusel lisada valikuid seoses konkreetsete töökäskude või töökäsu töödega. Nende valikute tegemiseks klõpsake **Filter**.

3. Vajadusel saate seadistada automaatse värskenduse pakett-tööna kiirkaardil **Taustal käitamine**.

4. Prognoosi värskendamise käivitamiseks klõpsake **OK**.


![Joonis 2](media/07-work-orders.png)

