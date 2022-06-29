---
title: Täiskoormuse arvutamine
description: See artikkel selgitab, kuidas arvutada varahalduses võimsuse koormust.
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCapacityLoad, EntAssetWorkOrderCapacityLoadCalculate, EntAssetWorkOrderCapacityLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 95d1e38db8e4658a57f36139836264b87d525e61
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016126"
---
# <a name="calculate-capacity-load"></a>Arvuta täiskoormus

[!include [banner](../../includes/banner.md)]


Varahalduses saate arvutada täiskoormust järgmiste näitajate kohta:

- hooldusgraafiku read  
- töökäsud, mida pole veel plaanitud  
- plaanitud töökäsud

See on kasulik, kui soovite saada ülevaate konkreetse perioodi oodatavast täiskoormusest. Täiskoormuse arvutuse saab teha kõigile varadele või valitud varadele. Samuti saate teha arvutuse hoolduskatkestuse toimingute või töökäsu kaustade kohta.

1. Klõpsake varahalduse päringute võimsuse koormust **või** > **·** > **·** **varahalduse töötellimuste kaustu Kõik töötellimuste kaustad aktiivsete töötellimuste kaustad > valige loendist töötellimuse kogum nupust >** > **·** > **Võimsuse laadimine või** / **Varahalduse** hoolduse downtime-tegevused **Kõik hoolduse** **mahatunnitöö tegevused > valige loendist > Võimsuse koormuse** > **·** > **nupp.** / **·** **·**

2. Dialoogiboksis **Arvuta täiskoormus** valige arvutuse periood väljadel **Alguskuupäev/aeg** ja **Lõppkuupäev/aeg**.

3. Valige "Jah" tumblernupul **Kaasa hooldusgraafik**, kui soovite arvutusse kaasata hooldusgraafiku read.

4. Valige "Jah" tumblernupul **Kaasa töökäsk**, kui soovite arvutusse kaasata töökäsu tööd.

5. Saate kasutada välja **Tase**, et näidata kui üksikasjalikke töö asukohtade täiskoormuse ridu te soovite. 

    Kui sisestate väljale näiteks arvu "1" ja teil on mitmetasandiline töö asukoha struktuur, kuvatakse ülemisel tasemel kõik töö asukoha hooldusgraafiku read ja töökäsud ning seetõttu võivad tunnid real olla lisatud ülespoole töö asukohtades, mis asuvad madalamal tasemel. 
    
    Kui sisestate väljale **Tase** arvu "0", näete üksikasjalikku tulemust, mis näitab kõiki hooldusgraafiku ridu ja kõiki töökäske kõigi töö asukohtade tasemete kohta, millega nad on seotud.

6. Arvutuse alustamiseks klõpsake **OK**.

7. Gruppides **Rühmitusalus** klõpsake asjakohastele nuppudele, et näidata arvutuse soovitud üksikasja taset. Alloleval kuvatõmmisel on gruppide **Rühmitusalus** nupud esile tõstetud sinise värviga. Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.

    ![Joonis 1.](media/01-capacity-planning.png)

>[!NOTE]
>Kui soovite keskenduda ainult planeeritud töökäskude võimsuse planeerimisele, vaadake teemat [Täiskoormuse arvutamine plaanitud töökäskude kohta](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]