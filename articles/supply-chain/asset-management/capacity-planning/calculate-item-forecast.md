---
title: Kauba prognoosi arvutamine
description: See artikkel selgitab, kuidas arvutada kauba prognoosi varahalduses.
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
ms.openlocfilehash: 25e9b00533fb183b27c1bbe616cf6f414b44b5e7
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016097"
---
# <a name="calculate-item-forecast"></a>Kauba prognoosi arvutamine

[!include [banner](../../includes/banner.md)]

 

Nii nagu saate teha eelmises jaotises kirjeldatud täiskoormuse arvutusi, saate samuti teha kauba prognoosi arvutusi järgmiste näitajate põhjal:

- hooldusgraafiku read  
- töökäsud, mida pole veel plaanitud  
- plaanitud töökäsud

See on kasulik, kui soovite saada ülevaadet konkreetse perioodi oodatavast kauba tarbimisest (nii varuosad kui ka muu kaup, mis on vajalik töökäsu lõpetamiseks). Kauba prognoosi arvutuse saab teha kõigile varadele või valitud varadele. Samuti saate teha arvutuse hoolduskatkestuse toimingule (**Kõik hoolduskatkestuse toimingud** või **Aktiivsed hoolduskatkestuse toimingud**) või töökäsu kaustale (**Kõik töökäsu kaustad** või **Aktiivsed töökäsu kaustad**).

1. Klõpsake varahalduse päringute kaubaprognoosi **või** > **·** > **·** **varahalduse töötellimuste kaustu kõik töötellimuste kaustad > valige töötellimuse kaustu loendist > Kaubaeelarve** > **·** > **·** / **või** Varahalduse hoolduse downtime-tegevused Kõik hoolduse downtime-tegevused **aktiivse hoolduse downtime-tegevused** **> valige loendilt > Kaubaeelarve** > **·** > **tegevus.** / **·** **·**

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