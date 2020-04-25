---
title: Vastutavad hooldustöötajad
description: Selles teemas selgitatakse, kuidas sätestada vastutavaid hooldustöötajaid varahalduses.
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b5f83474e56c996a40bdbdf7d3a7c8d495429c6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208934"
---
# <a name="responsible-maintenance-workers"></a>Vastutavad hooldustöötajad

[!include [banner](../../includes/banner.md)]

 

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

![Vastutavate hooldustöötajate leht](media/08-setup-for-requests.png)
