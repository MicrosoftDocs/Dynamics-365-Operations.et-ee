---
title: Kulu ja kuupäeva juhtelementi
description: Selles teemas tutvustatakse kulu ja kuupäeva juhtelementi varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2bcd1584f6a858f7589387fbfe96267b7c16176a
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918391"
---
# <a name="cost-and-date-control"></a>Kulu ja kuupäeva juhtelementi

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Varahalduses saate kulusid arvutada, et saada ülevaade tegelikest kuludest võrreldes varade, töö asukohtade ja töökäskude eelarvekuludega. Tegelikud kulud põhinevad sisestatud kannetel. Samuti saate teha kuupäeva arvutuse, kui soovite võrrelda plaanitud algus- ja lõppkuupäevasid töökäskude tegelike algus- ja lõppkuupäevadega.

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a>Kulu juhtelement varade, töö asukohtade ja töökäskude jaoks

Varade, funktsionaalsete asukohtade ja töökäskude kohta tehtud arvutused on peaaegu samasugused. Ainuke erinevus on, et varade ja funktsionaalsete asukohtade puhul saate arvutusse kaasata ka alavarasid ja alaasukohti. Kuupäev on kande kuupäev, mil registreering salvestati.

1. Klõpsake **Varahaldus** > **Päringud** > **Varad** > **Vara kulu juhtelement** või **Töö asukoha kulu juhtelement** või **Varahaldus** > **Päringud** > **Töökäsud** > **Töökäsu kulu juhtelement**.

2. Dialoogiboksis **Vara kulu juhtelement** / **Töö asukoha kulu juhtelement** / **Töökäsu kulu juhtelement** valige arvutatav periood.

3. Kui on nõutud, valige arvutusse kaasatav finatsdimensioonikogum.

4. Kui te ei soovi nulli kuluga tulemusi näidata, valige "Jah" lülitusnupul **Jäta null vahele**.

5. Saate kasutada välja **Tase**, et näidata, kui üksikasjalikult soovite, et kulujuhtimise read oleksid seotud töö asukohtadega. Kui sisestate väljale näiteks arvu "1" ja teil on mitmetasandiline töö asukoha hierarhia, kuvatakse ülemisel tasemel kõik töö asukoha kulu juhtelemendi read ning seetõttu võivad tunnid real olla lisatud ülespoole töö asukohtades, mis asuvad madalamal tasemel. Kui sisestate väljale **Tase** arvu "0", näete üksikasjalikku tulemust, mis näitab kõiki kulu juhtelemendi ridu kõigi töö asukoha tasemete kohta, millega nad on seotud.

6. Valige "Jah" tumblernupul **Kuva avatud kooskõlastatud kulu**, kui soovite seda tulpa arvutusse kaasata.

7. Märkige Jah nupul **Kaasa alavarad**, et näidata alavaradega seotud kulusid eraldi ridadena.

8. Kui soovite otsingut piirata, saate valida kindlad varad / funktsionaalsed asukohad / töökäsud **Lisamiskirjed** kiirkaardi valikus.

9. Arvutuse alustamiseks klõpsake **OK**.

Alloleval joonisel kuvatakse näidet dialoogiboksist **Vara kulu juhtelement**.

![Joonis 1](media/01-controlling-and-reporting.png)

10. Toimingupaani rühmades **Rühmitusalus** lehel **Vara kulu juhtelement** klõpsake asjakohastele nuppudele, et näidata arvutuse soovitud üksikasja taset. Valitud toimingupaani nupud on esile tõstetud. Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.

Alloleval joonisel kuvatakse näidet arvutuse tulemustest dialoogiboksis **Vara kulu juhtelement**.

![Joonis 2](media/02-controlling-and-reporting.png)

Teine viis kulu juhtelemendi loomiseks on teha mitmikvalik varadele suvandis **Kõik varad** või **Aktiivsed varad**. Seejärel klõpsake nupule **Kulu juhtelement** vahekaardil **Üldine**. Dialoogiboksis **Vara kulu juhtelement** valitud varad sisestatakse automaatselt väljale **Vara** vahekaardil **Kaasatavad kirjed**. Klõpsake **OK** ja kuvatakse kulu arvutus valitud varade kohta. Sama protseduuri saab teha funktsionaalsete asukohtade puhul väljades **Kõik funktsionaalsed asukohad** või **Aktiivsed funktsionaalsed asukohad** ja ktöökäskude puhul väljades **Kõik töökäsud** või **Aktiivsed töökäsud**.

>[!NOTE]
>**Algne eelarve** väli näitab eelarve kulusid töökäskude prognoosist. Väljal **Kooskõlastatud kulu** kuvatakse kulude kogusumma, mille juriidiline isik on võtnud kohustuseks maksta. Väljal **Avatud kooskõlastatud kulu** kuvatakse kohustused maksta kaupade, tundide ja teenuste eest, mille olete tellinud või saanud, kuid mille eest pole veel maksnud. Kui kõik tarbimise registreeringud on sisestatud, kaasatakse seotud kulud väljal **Tegelik kulu**.

## <a name="work-order-date-control"></a>Töökäsu kuupäevajuhtimine

Kasutage seda lehte, kui soovite saata ülevaate oodatavatest algus- ja lõppkuupäevadest võrreldes töökäskude tegelike algus- ja lõppkuupäevadega.

1. Klõpsake **Varahaldus** > **Päringud** > **Töökäsud** > **Töökäsu kuupäeva juhtelement**.

2. Klõpsake valikut **Arvuta**.

3. Valige töö asukoht väljal **Töö asukoht**.

4. Sisestage periood, mille kohta soovite arvutust teha väljadel **Kuupäevast** ja **Kuupäevani**. Kaasatakse kõik eeldatava alguskuupäevaga töökäsud perioodi ulatuses.

5. Klõpsake valikut **OK**.

6. Toimingupaani rühmades **Rühmitusalus** klõpsake asjakohastele nuppudele, et näidata arvutuse soovitud üksikasja taset. Valitud toimingupaani nupud on esile tõstetud. Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.

Alloleval joonisel kuvatakse näidet arvutuse tulemustest dialoogiboksis **Töökäsu kuupäeva juhtelement**.

![Joonis 3](media/03-controlling-and-reporting.png)

- Väljal **Keskm. alguse hilinemine** kuvatakse erinevus töökäsu plaanitud alguskuupäeva ja tegeliku alguskuupäeva vahel. Näiteks kui tegelik alguskuupäev oli kaks päeva enne plaanitud alguskuupäeva, kuvatakse sellel väljal "-2".  
- Väljal **Keskm. alguse hilinemine** kuvatakse erinevus töökäsu plaanitud lõppkuupäeva ja tegeliku lõppkuupäeva vahel. Näiteks kui tegelik lõppkuupäev oli kolm päeva pärast plaanitud lõppkuupäeva, kuvatakse sellel väljal "3".  
- Väljal **Esinemiskorrad** kuvatakse kõrvalekallete arv seoses töökäsu plaanitud ja tegelike alguskuupäevadega ning plaanitud ja tegelike lõppkuupäevadega.

