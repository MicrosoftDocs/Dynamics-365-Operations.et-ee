---
title: Vastutavad hooldustöötajad
description: Selles teemas selgitatakse, kuidas sätestada vastutavaid hooldustöötajaid varahalduses.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
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
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 432a235668bbd969f497003a98b7f66390e5308f
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790484"
---
# <a name="responsible-maintenance-workers"></a>Vastutavad hooldustöötajad

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Vastutavad hooldustöötajad võivad olla seotud vara tüüpide, varade, funktsionaalsete asukohtade, hooldustöö tüübi kategooriate, hooldustöö tüüpide, hooldustöö tüüpide variantide ja kaubandusega. Neid saab kasutada töökäskudel ja hooldustaotlustel, et näidata eelistust hooldustöötajate osas, kes peaksid olema töökäsu eest vastutavad. (Kuid need hooldustöötajad ei ole tingimata samad töötajad, kellele on ette nähtud töökäsk täita.) Selle funktsiooni kasutamine on valikuline. Näiteks saab seda kasutada, et valida vastutavad töötajad või töötajate rühmad spetsiifiliste töö tüüpide või tööalade jaoks.

Töökösu elutsükli või hooldustaotluse elutsükli jooksul saab vastutavaid hooldustöötajaid muuta või värskendada. Muutus või värskendus võib olla seotud näiteks hooldustaotluse elutsükli oleku või töökäsu elutsükli oleku muutusega.

Häälestust lehel **Vastutavad hooldustöötajad** *ei* kasutata töökäsu planeerimise ajal.

> [!NOTE]
> Varahalduses saate samuti sätestada *eelistatud* hooldustöötajaid, kes võivad olla eraldatud töökäskudele töökäsu planeerimise ajal.

Enne kui saate sätestada vastutavaid hooldustöötajaid, peate sätestama töötajad ja töötajate rühmad, mis peaksid valikuks saadava olema. Lisateavet töötajate ja töötajate rühmade sätestamiseks vt teemast [Hooldustöötajad ja töötajate rühmad](../setup-for-objects/workers-and-worker-groups.md).

## <a name="set-up-responsible-maintenance-workers"></a>Vastutavate hooldustöötajate sätestamine

1. Valige **Varahaldus**\>**Häälestus**\>**Töötajad**\>**Vastutavad hooldustöötajad**.
2. Valige **Uus**, et luua uus kirje.
3. Esmalt looge vaikimisi vastutava hooldustöötaja või vastutava töötajate rühma häälestus, kus sätestate üksnes välja **Vastutav töötajate rühm** ja/või välja **Vastutav töötaja**. Ülejäänud väljad jätke tühjaks. Seda vaikimisi häälestust kasutatakse töökäsu planeerimisel, kui teine spetsiifilisem kombinatsioon ei vasta töökäsu sisule.

    > [!NOTE]
    > Kui vastutav hooldustöötaja või vastutavate hooldustöötajate rühm on hooldustaotluse loomise käigus valikuks saadaval lehel **Kõik hooldustaotlused**, vaatab varahaldus läbi kõik vastutavad hooldustöötaja kirjed, et leida võimalik vaste. Varahaldus kontrollib alati kõige spetsiifilisemat kombinatsiooni esimesena. Teisisõnu kontrollib varahaldus esmalt vastet väljale **Kaubandus**. Kui vastet ei leita, otsib see vastet väljale **Hooldustöö tüübi variant**. Kui vastet ei leita, otsib see vastet väljale **Hooldustöö tüüp** jne. Nagu näete lehe kujundusest, tähendab selline käitumine, et kõige spetsiifilisema kombinatsiooni leidmiseks otsib varahaldus kirjeid vaste leidmiseks paremalt vasakule (esmalt **Kaubandus**, seejärel **Hooldustöö tüübi variant**, seejäel **Hooldustöö tüüp**, seejärel **Hooldustöö tüübi kategooria**, seejärel **Funktsionaalne asukoht**, seejärel **Vara** ja viimaks **Vara tüüp**). Kui vastet ei leita, kasutatakse vaikimisi kirjet, mille valikutes pole kasutatud ühtegi neist väljast.

Järgnev illustratsioon näitab lehe **Vastutavad hooldustöötajad** näidet.

![Joonis 1](media/08-setup-for-requests.png)