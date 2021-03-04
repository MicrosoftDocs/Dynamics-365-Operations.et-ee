---
title: Kulu ja kuupäeva juhtelementi
description: Selles teemas tutvustatakse kulu ja kuupäeva juhtelementi varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetBICostControlWorkspace, EntAssetWorkOrderDateControl, EntAssetWorkOrderForecastCostInfoPart, EntAssetMaintenanceCostTrans, EntAssetWorkOrderDateControlCalcDialog, EntAssetCostControl, EntAssetCostObjectCalendar, EntAssetWorkOrderCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 18373ff16b63ea61a3a4bc38ee7fa0b5e33154b5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426156"
---
# <a name="cost-and-date-control"></a>Kulu ja kuupäeva juhtelementi

[!include [banner](../../includes/banner.md)]

 

Varahalduses saate kulusid arvutada, et saada ülevaade tegelikest kuludest võrreldes varade, töö asukohtade ja töökäskude eelarvekuludega. Tegelikud kulud põhinevad sisestatud kannetel. 

Samuti saate teha kuupäeva arvutuse, kui soovite võrrelda plaanitud algus- ja lõppkuupäevasid töökäskude tegelike algus- ja lõppkuupäevadega.

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a>Kulu juhtelement varade, töö asukohtade ja töökäskude jaoks

Varade, funktsionaalsete asukohtade ja töökäskude kohta tehtud arvutused on peaaegu samasugused. Ainuke erinevus on, et varade ja töö asukohtade puhul saate arvutusse kaasata ka alamvarasid ja alamasukohti. Kuupäev on kande kuupäev, mil registreering salvestati.

1. Klõpsake **Varahaldus** > **Päringud** > **Varad** > **Vara kulu juhtelement** või **Töö asukoha kulu juhtelement** või **Varahaldus** > **Päringud** > **Töökäsud** > **Töökäsu kulu juhtelement**.

2. Dialoogiboksis **Vara kulu juhtelement** / **Töö asukoha kulu juhtelement** / **Töökäsu kulu juhtelement** valige arvutatav ajavahemik.

3. Kui on nõutud, valige arvutusse kaasatav finatsdimensioonikogum.

4. Kui te ei soovi nulli kuluga tulemusi näidata, valige "Jah" lülitusnupul **Jäta null vahele**.

5. Saate kasutada välja **Tase**, et näidata, kui üksikasjalikult soovite, et kulujuhtimise read oleksid seotud töö asukohtadega. 

    Kui sisestate väljale näiteks arvu "1" ja teil on mitmetasandiline töö asukoha hierarhia, kuvatakse ülemisel tasemel kõik töö asukoha kulu juhtelemendi read ning seetõttu võivad tunnid real olla lisatud ülespoole töö asukohtades, mis asuvad madalamal tasemel. 
    
    Kui sisestate väljale **Tase** arvu "0", näete üksikasjalikku tulemust, mis näitab kõiki kulu juhtelemendi ridu kõigi töö asukoha tasemete kohta, millega nad on seotud.

6. Valige "Jah" tumblernupul **Kuva avatud kooskõlastatud kulu**, kui soovite seda tulpa arvutusse kaasata.

7. Märkige Jah nupul **Kaasa alavarad**, et näidata alavaradega seotud kulusid eraldi ridadena.

8. Kui soovite otsingut piirata, saate valida kindlad varad / funktsionaalsed asukohad / töökäsud **Lisamiskirjed** kiirkaardi valikus.

9. Arvutuse alustamiseks klõpsake **OK**.

    Alloleval joonisel kuvatakse näidet dialoogiboksist **Vara kulu juhtelement**.

    ![Dialoogiboks Vara kulu juhtimine](media/01-controlling-and-reporting.png)

10. Klõpsale lehe **Vara kulu juhtimine** jaotise **Grupeerimisalus** nuppe, et näidata arvutuse nõutavat üksikasjalikku taset. Valitud nupud **Rühmitusalus** on esile tõstetud. Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.

## <a name="example"></a>Näide

Alloleval kuvatõmmisel kuvatakse näidet arvutuse tulemustest dialoogiboksis **Vara kulu juhtimine**.

- **Algne eelarve** väli näitab eelarve kulusid töökäskude prognoosist. 
- Väljal **Kooskõlastatud kulu** kuvatakse kulude kogusumma, mille juriidiline isik on võtnud kohustuseks maksta. 
- Väljal **Avatud kooskõlastatud kulu** kuvatakse kohustused maksta kaupade, tundide ja teenuste eest, mille olete tellinud või saanud, kuid mille eest pole veel maksnud. 
- Kui kõik tarbimise registreeringud on sisestatud, kuvatakse seotud kulud väljal **Tegelik kulu**.

![Arvutustulemuste näide lehel vara kulu juhtimine](media/02-controlling-and-reporting.png)

Teine viis kulu juhtelemendi loomiseks on teha mitmikvalik varadele suvandis **Kõik varad** või **Aktiivsed varad**. Seejärel klõpsake nupule **Kulu juhtelement** vahekaardil **Üldine**. Dialoogiboksis **Vara kulu juhtelement** valitud varad sisestatakse automaatselt väljale **Vara** vahekaardil **Kaasatavad kirjed**. Klõpsake **OK** ja kuvatakse kulu arvutus valitud varade kohta. Sama protseduuri saab teha funktsionaalsete asukohtade puhul väljades **Kõik funktsionaalsed asukohad** või **Aktiivsed funktsionaalsed asukohad** ja ktöökäskude puhul väljades **Kõik töökäsud** või **Aktiivsed töökäsud**.


## <a name="work-order-date-control"></a>Töökäsu kuupäevajuhtimine

Kasutage seda lehte, kui soovite saata ülevaate oodatavatest algus- ja lõppkuupäevadest võrreldes töökäskude tegelike algus- ja lõppkuupäevadega.

1. Klõpsake **Varahaldus** > **Päringud** > **Töökäsud** > **Töökäsu kuupäeva juhtelement**.

2. Klõpsake valikut **Arvuta**.

3. Valige töö asukoht väljal **Töö asukoht**.

4. Sisestage vahemik, mille kohta soovite arvutust teha väljadel **Kuupäevast** ja **Kuupäevani**. Kaasatakse kõik eeldatava alguskuupäevaga töökäsud vahemiku piires.

5. Klõpsake valikut **OK**.

6. Valige nupud **Rühmitusalus**, et vaadata arvutuse soovitud üksikasja taset. Valitud nupud **Rühmitusalus** on esile tõstetud. Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.

## <a name="example"></a>Näide

Alloleval kuvatõmmisel kuvatakse näide arvutustulemuste kohta dialoogiboksis **Töökäsu kuupäeva juhtimine**.

- Väljal **Keskm. alguse hilinemine** kuvatakse erinevus töökäsu plaanitud alguskuupäeva ja tegeliku alguskuupäeva vahel. Näiteks kui tegelik alguskuupäev oli kaks päeva enne plaanitud alguskuupäeva, kuvatakse sellel väljal "-2".  
- Väljal **Keskm. alguse hilinemine** kuvatakse erinevus töökäsu plaanitud lõppkuupäeva ja tegeliku lõppkuupäeva vahel. Näiteks kui tegelik lõppkuupäev oli kolm päeva pärast plaanitud lõppkuupäeva, kuvatakse sellel väljal "3".  
- Väljal **Esinemiskorrad** kuvatakse kõrvalekallete arv seoses töökäsu plaanitud ja tegelike alguskuupäevadega ning plaanitud ja tegelike lõppkuupäevadega.

![Arvutustulemuste näide lehel Töökäsu kuupäeva juhtimine](media/03-controlling-and-reporting.png)




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]