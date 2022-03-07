---
title: Kauba prognoosi arvutamine
description: Selles teemas tutvustatakse, kuidas arvutada kauba prognoosi varahalduses.
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5773149760ecb2a26f4916036fe36c9cc04f654039dee4eab9bfac86eb02e1fd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713026"
---
# <a name="calculate-item-forecast"></a>Kauba prognoosi arvutamine

[!include [banner](../../includes/banner.md)]

 

Nii nagu saate teha eelmises jaotises kirjeldatud täiskoormuse arvutusi, saate samuti teha kauba prognoosi arvutusi järgmiste näitajate põhjal:

- hooldusgraafiku read  
- töökäsud, mida pole veel plaanitud  
- plaanitud töökäsud

See on kasulik, kui soovite saada ülevaadet konkreetse perioodi oodatavast kauba tarbimisest (nii varuosad kui ka muu kaup, mis on vajalik töökäsu lõpetamiseks). Kauba prognoosi arvutuse saab teha kõigile varadele või valitud varadele. Samuti saate teha arvutuse hoolduskatkestuse toimingule (**Kõik hoolduskatkestuse toimingud** või **Aktiivsed hoolduskatkestuse toimingud**) või töökäsu kaustale (**Kõik töökäsu kaustad** või **Aktiivsed töökäsu kaustad**).

1. Klõpsake **Varahaldus** > **Päringud** > **Kauba prognoos** või **Varahaldus** > **Üldine** > **Töökäsu kaustad** > **Kõik töökäsu kaustad** / **Aktiivsed töökäsu kaustad** > valige loendist töökäsu kaust > nupp **Kauba prognoos** või **Varahaldus** > **Üldine** > **Hoolduskatkestuse toimingud** > **Kõik hoolduskatkestuse toimingud** / **Aktiivsed hoolduskatkestuse toimingud** > valige loendist hoolduskatkestuse toiming > nupp **Kauba prognoos**.

2. Dialoogiboksis **Arvuta kauba prognoos** valige arvutuse periood väljadel **Alguskuupäev/aeg** ja **Lõppkuupäev/aeg**.

3. Valige "Jah" tumblernupul **Kaasa hooldusgraafik**, kui soovite prognoosi arvutusse kaasata hooldusgraafiku read.

4. Valige "Jah" tumblernupul **Kaasa töökäsk**, kui soovite prognoosi arvutusse kaasata töökäsu tööd.

5. Saate kasutada välja **Tase**, et näidata kui üksikasjalikke töö asukohtade kauba prognoosi ridu te soovite. 

      Kui sisestate väljale näiteks arvu "1" ja teil on mitmetasandiline töö asukoha struktuur, kuvatakse ülemisel tasemel kõik töö asukoha hooldusgraafiku read ja töökäsud ning seetõttu võivad tunnid real olla lisatud ülespoole töö asukohtades, mis asuvad madalamal tasemel. 
  
      Kui sisestate väljale **Tase** arvu "0", näete üksikasjalikku tulemust, mis näitab kõiki hooldusgraafiku ridu ja kõiki töökäske kõigi töö asukoha tasemete kohta, millega nad on seotud.

6. Arvutuse alustamiseks klõpsake **OK**.

7. Gruppides **Rühmitusalus** klõpsake asjakohastele nuppudele, et näidata arvutuse soovitud üksikasja taset. Alloleval kuvatõmmisel on gruppide **Rühmitusalus** nupud esile tõstetud sinise värviga. Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.

8. Klõpsake nuppu **Kuva dimensioonid**, kui soovite näha kaubaga seotud toote, lao ja jälgimise dimensioone. Valige sobivad märkeruudud ja klõpsake nuppu **OK**.

![Joonis 1.](media/02-capacity-planning.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]