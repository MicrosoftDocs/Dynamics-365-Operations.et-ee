---
title: Hooldusgraafik
description: Selles teemas selgitatakse hooldusgraafikut varahalduses.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectCalendarCreateWO, EntAssetObjectCalendarListPagePoolsOpen, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePreviewPart, EntAssetObjectCalendarEdit, EntAssetObjectCalendarAdjust, EntAssetObjectCalendarDiscard, EntAssetObjectCalendarInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 40df8e6cba824f90e13b46cc258c76bef993a3e2dd9c35566d8c6a622ce4eb09
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738315"
---
# <a name="maintenance-schedule"></a>Hooldusgraafik

[!include [banner](../../includes/banner.md)]

 

Hooldusgraafik sisaldab kõigi oodatud teostatavate ennetavate hoolduskavade, hooldusnõuete ja hoolduskordade loendit. Mõned graafiku read võivad olla teisendatud töökäskudeks.

Neli hooldusgraafiku vaadet on veidi erinevad, olenevalt sellest, milliseid hooldusgraafiku ridu soovite näha.

| Menüü-üksus                  | Sisu kirjeldus                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kogu hooldusgraafik       | Kuvatakse kõiki hooldusgraafiku ridu.     |
| Minu vara graafik        | Selles loendis kuvatakse kõiki hooldusgraafikute ridu, mis sisaldavad nendesse töö asukohtadesse paigaldatud varasid, millega te töötajana seotud olete (seadistatud jaotises [Hooldustöötajad ja töötajate rühmad](../setup-for-objects/workers-and-worker-groups.md)). |
| Hooldusgraafiku ridade avamine | Selles loendis kuvatakse hooldusgraafiku ridu, mille olek on "Loodud", mis tähendab, et need ei ole veel töökäsuks teisendatud ega hüljatud.                                            |
| Hooldusgraafiku kaustade avamine | Selles loendis näidatakse töökäskude kogumiga seotud hooldusgraafiku ridu.                                                                                                                  |

>[!NOTE]
>Kui hooldusgraafiku rida sisaldub mitmes töökäsu kogumis (vt [Töökäskude kogumid](../work-orders/work-order-pools.md)), kuvatakse ühte kirjet igas jaotise **Avatud hooldusgraafiku kogumid** kogumis. Seda tehakse töökäsu kogumite filtreerimisvalikute optimeerimiseks.

Hooldusgraafiku avamiseks toimige järgmiselt.

1. Klõpsake **Varahaldus** > **Üldine** > **Hooldusgraafik** > **Kõik hooldusgraafikud** või **Avatud hooldusgraafiku read** või **Avatud hooldusgraafiku kogumid**.

2. Hooldusgraafiku värskendamiseks klõpsake **Hoolduskava** või **Hoolduskorrad**. 

3. Võite redigeerida hooldusgraafiku rida valides selle ja klõpsates **Redigeeri**. Näiteks saate kerge vaevaga värskendada töö eest vastutava töötaja teenindustaset. Võite redigeerida ainult neid hooldusgraafiku ridu, mis ei ole veel töökäsuga ühendatud.

4. Võite kustutada hooldusgraafiku rea valides selle loendi lehelt ja klõpsates **Kustuta**.

5. Võite hüljata hooldusgraafiku rea valides selle loendi lehelt ja klõpsates **Hülga**. See funktsioon on kasulik näiteks siis, kui varal on 2 000 km hoolduskava ja 10 000 km hoolduskava. Siis võite soovida hüljata 2 000 km hoolduskavast loodud rea, kui see langeb kokku 10 000 km-ga, 20 000 km-ga, 30 000 km-ga jne. Kui hülgate hoolduskavaga seotud hooldusgraafiku rea, ei kuvata seda rida kunagi hoolduskava ajastamisel uuesti.

6. Võite valida mitu hooldusgraafiku rida jaotisest **Kõik hooldusgraafikud** ja klõpsata valikut **Töökäskude kogum**, kui soovite, et kõik valitud read sisalduksid töökäsu kogumis.

7. Võite valida mitu hooldusgraafiku rida jaotises **Kõik hooldusgraafikud** või **Avatud hooldusgraafiku read** või **Avatud hooldusgraafiku kogumid** ja klõpsata valikut **Reguleeri graafikut**, kui soovita teha samu muudatusi mitmele reale. Võite muuta valitud hooldusgraafiku ridadega seotud oodatud alguse- ja lõppkuupäevi, teenindustaset ja vastutavat hooldustöötajate rühma või vastutavat hooldustöötajat.

- Kui hooldusgraafiku rida on seotud töökäsuga, kuvatakse töökäsu IDd väljal **Töökäsk**.  
- Varale saate hoolduskavasid valida jaotise **Kõik varad** üksikasjade vaate > kiirkaardil **Vara hoolduskavad**. Hiljem, kui kustutate jaotise **Kõik varad** varaga seotud hoolduskava rea, kustutate automaatselt kõik hooldusgraafiku read olekuga "Loodud", mis on loodud selle hoolduskava põhjal. Vaadake ka jaotist [Vara loomine](../objects/create-an-object.md).

Alloleval joonisel on kujutatud jaotise **Kõik hooldusgraafikud** loendi lehte.

![Joonis 1.](media/16-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]