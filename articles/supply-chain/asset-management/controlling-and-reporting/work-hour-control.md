---
title: Töötundide kontroll
description: Selles teemas selgitatakse töötundide kontrolli varahalduses.
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
ms.openlocfilehash: 1a59b4bbf1a4612cea1ba3bd536ba4b018fc621f
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652329"
---
# <a name="work-hour-control"></a>Töötundide kontroll

[!include [banner](../../includes/banner.md)]

 

Varahalduses saate arvutada tunde, et saada ülevaade tegelikest tundidest, võrreldes eelarve tundidega varade, funktsionaalsete asukohtade või töötellimuste puhul. Tegelikud tunnid põhinevad sisestatud kannetel.

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a>Töötunni juhtelement varade, funktsionaalsete asukohtade ja töötellimuste jaoks

Varade, funktsionaalsete asukohtade ja töökäskude kohta tehtud arvutused on peaaegu samasugused. Ainuke erinevus on, et varade ja funktsionaalsete asukohtade puhul saate arvutusse kaasata ka alavarasid ja alaasukohti. Kuupäev on kande kuupäev, mil registreering salvestati.

1. Klõpsake **Varahaldus** > **Päringud** > **Varad** > **Varatunni kontroll** või **Funktsionaalse asukoha tunnikontroll** või **Varahaldus** > **Päringud** > **Töökäsud** > **Töökäsu tunnikontroll**.

2. **Vara tunnikontroll** dialoogiaknas.

3. Valige dialoogiaknas **Vara tunnikontroll** / **Funktsionaalse asukoha tunnikontroll** / **Töökäsu tunnikontroll** periood, mis arvutatakse väljadel **Alates** ja **Kuni**.

4. Vajadusel kaasake arvutusse **Finantsdimensiooni komplekt**.

5. Kui te ei soovi nulli tunniga tulemusi näidata, valige "Jah" lülitusnupul **Jäta null vahele**.

6. Saate kasutada välja **Tase**, et näidata, kui üksikasjalikult soovite, et tunnikontrolli read oleksid seotud töö asukohtadega. 

    Näiteks kui sisestate väljale numbri "1" ja teil on mitmetasandiline töö asukoha hierarhia, kuvatakse ülemisel tasemel kõik tunnikontrolli read töö asukoha kohta ja seetõttu võib rea tunnid kokku liita töö asukohtadest, mis asuvad madalamal tasemel. 
    
    Kui sisestate numbri "0" väljale **Tase**, näete üksikasjalikku tulemust, kus kuvatakse kõik tunnikontrolli read kõigil töö asukoha tasemetel, millega need on seotud.

7. Märkige Jah nupul **Kaasa alavarad**, et näidata alavaradega seotud kulusid eraldi ridadena.

8. Kui soovite otsingut piirata, saate valida kindlad varad / funktsionaalsed asukohad / töökäsud **Lisamiskirjed** kiirkaardi valikus.

9. Arvutuse alustamiseks klõpsake **OK**.

10. Klõpsale lehe **Varatunni kontroll** jaotise **Grupeerimisalus** nuppe, et näidata arvutuse nõutavat üksikasjalikku taset. Valitud nupud **Rühmitusalus** on esile tõstetud. Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.

## <a name="example"></a>Näide

Alltoodud kuvatõmmisel on näidatud lehe **Varatunni kontroll** näidisarvutus.

- Väli **Algne eelarve** väli näitab eelarve tunde töökäskude prognoosist. 
- Väljal **Tegelikud tunnid** kuvatakse töökäskudesse sisestatud tunnid. 
- Väli **Kooskõlastatud tunnid** näitab kogutunde, millele teie ettevõte on pühendunud seoses töökäskudega.

![Varatunni kontrolli näidisarvutus](media/04-controlling-and-reporting.png)

Teine moodus tundide arvutamiseks on valida kas **Kõik varad** või **Aktiivsed varad**. Seejärel klõpsake nuppu **Tunnikontroll** kiirkaardil **Üldine**. Valitud varad sisestatakse automaatselt välja **Varad** kiirkaardil **Kaasatavad kirjed**. Klõpsake **OK** dialoogiaknas **Varatunni kontroll** ja valitud varade arvutus kuvatakse. Sama protseduuri saab teha funktsionaalsete asukohtade puhul väljades **Kõik funktsionaalsed asukohad** või **Aktiivsed funktsionaalsed asukohad** ja ktöökäskude puhul väljades **Kõik töökäsud** või **Aktiivsed töökäsud**.


