---
title: "Hankija maksete tööruum"
description: "See teema annab teavet hankija maksete tööruumi kohta. Hankija maksete tööruumis on näidatud teave, mis on seotud hankija maksete töötlemisega."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/09/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPaymentWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: cb5a674472936a52b624c548fd37079d57eb6cb7
ms.openlocfilehash: fa8ddf52d34c3662e120509156ab0b343bb4cc16
ms.contentlocale: et-ee
ms.lasthandoff: 12/14/2017

---

# <a name="vendor-payments-workspace"></a>Hankija maksete tööruum

[!INCLUDE [banner](../includes/banner.md)]

**Hankija maksete** tööruumis on näidatud teave, mis on seotud hankija maksete töötlemisega. See tööruum sisaldab vaadet **Minu töö** ja lehte **Analüüs**. Vaade **Minu töö** kuvab kokkuvõttepaanid, hankija kannete tabelid ja hankija seonduvad andmed. Leht **Analüüs** kasutab Microsoft Power BI võimalusi hankija maksetega seotud visuaalide kuvamiseks.

## <a name="my-work-view"></a>Minu töö vaade

### <a name="summary-tiles"></a>Kokkuvõttepaanid

Paanid jaotises **Kokkuvõte** annavad ülevaate teie makseteabe olekust. Näete maksetöölehti, mis pole veel sisestatud, arveid, mille tähtaeg on möödunud, kõiki hankijaid ja ootelolevaid hankijaid. Jaotises **Kokkuvõte** saate luua uue maksetsükli.

Teave jaotises **Kokkuvõte** on ettevõtte kohta, kuhu olete sisse loginud.

### <a name="vendor-transactions-grids"></a>Hankija kannete tabelid

Jaotis **Hankija kanded** sisaldab tabeleid, milles on näha möödunud tähtajaga arved ja tasakaalustamata maksed. Tabelis **Tähtaja ületanud arved** saate vaadata valitud arve tasakaalustusajalugu. Tabelis **Tasakaalustamata maksed** saate vaadata valitud arve tasakaalustusajalugu ja arvet tasakaalustada.

Tsentraliseeritud makseametnikud saavad kasutada filtrit, mis kuvatakse iga tabeli ülaosas, ettevõtte valimiseks. Seejärel filtreeritakse tabelit, nii et see näitab ainult neid ettevõtteid, mis on määratletud tsentraliseeritud makse organisatsiooni hierarhias, mille vaatamiseks tsentraliseeritud makseametnikul on õigused.

Vahekaardil **Otsi kandeid** jaotises **Hankija kanded** saate otsida hankija kannet.

### <a name="related-information"></a>Seostuv teave

Saate vaadata aruannet **Hankija aegumine** ja aruannet **Maksete kokkuvõte päevade lõikes**, kasutades linke tööruumi jaotises **Seostuv teave**.

## <a name="analytics-page"></a>Analüüsi leht

Lehel **Analüüs** on antud olulised mõõdikud, nt tähtaja ületanud hankija arved ja tulevase tähtajaga hankija arved. See leht sisaldab üheksat aruandelehte. Üks leht annab ülevaate ja ülejäänud kaheksal lehel on ostureskontro maksemõõdikute üksikasjad.

Järgmine tabel näitab igal aruandelehel olevaid visualiseeringuid.


|            Aruandeleht            |                                                                                                                                                                                Visualiseering                                                                                                                                                                                |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     Hankija maksete ülevaade      | <ul><li>Tähtaja ületanud arved</li><li>Tänase tähtajaga arved</li><li>Tehtud ja kaotatud allahindlused</li><li>Tulevase tähtajaga arved skonto kuupäeva järgi</li><li>Tulevase tähtajaga arved tähtaja järgi</li><li>Hiljem ja õigel ajal tasutud arved</li><li>Makse töövoo määramine</li><li>Hankija ja kliendi saldo</li><li>Ooteloleva maksega avatud arved</li></ul> |
|         Tähtaja ületanud arved         |                                                                                             <ul><li>Tähtaja ületanud arved</li><li>Tähtaja ületanud arvete üksikasjad</li><li>Avatud arveid kokku</li><li>Tähtaja ületanud arved hankijagrupi kohta</li><li>Tähtaja ületanud arved ettevõtte kohta</li></ul>                                                                                              |
|        Tänase tähtajaga arved         |                                                                                                         <ul><li>Tänase tähtajaga arved</li><li>Tänase tähtajaga arvete üksikasjad</li><li>Tänase tähtajaga arved ettevõtte kohta</li><li>Tänase tähtajaga arved hankijagrupi kohta</li></ul>                                                                                                          |
| Tehtud ja kaotatud allahindlused |                                                                             <ul><li>Tehtud ja kaotatud allahindlused</li><li>Tehtud ja kaotatud allahindluste üksikasjad</li><li>Tehtud ja kaotatud allahindlused ettevõtte kohta</li><li>Tehtud ja kaotatud allahindlused hankijagrupi kohta</li></ul>                                                                              |
|      Tulevase tähtajaga arved       |                                                 <ul><li>Tulevase tähtajaga arved</li><li>Tulevase tähtajaga arvete üksikasjad</li><li>Tulevase tähtajaga arved ettevõtte kohta</li><li>Tulevase tähtajaga arved hankijagrupi kohta</li><li>Tulevase tähtajaga arved skonto kuupäeva järgi</li><li>Tulevase tähtajaga arved tähtaja järgi</li></ul>                                                  |
|        Hiljem tasutud arved         |                                                         <ul><li>Pärast tähtaega tasutud arved</li><li>Pärast tähtaega tasutud arvete üksikasjad</li><li>Pärast tähtaega tasutud arved ettevõtte kohta</li><li>Pärast tähtaega tasutud arved hankijagrupi kohta</li><li>Hiljem tasutud arved võrreldes õigel ajal tasutud arvetega</li></ul>                                                          |
|         Makse töövoog          |                                                                                <ul><li>Hankija makse töövooeksemplarid</li><li>Hankija makse töövooeksemplarid kinnitaja kohta</li><li>Hankija makse töövooeksemplarid ettevõtte kohta</li><li>Keskmine töövoo päevade arv kinnitaja kohta</li></ul>                                                                                |
|    Hankija ja kliendi saldo     |                                                                                                                   <ul><li>Hankija ja kliendi saldo</li><li>Hankija ja kliendi saldo ettevõtte kohta</li><li>Hankija ja kliendi saldo üksikasjad</li></ul>                                                                                                                    |
|    Ooteloleva maksega arved     |                                                                                         <ul><li>Ooteloleva maksega arved</li><li>Ooteloleva maksega arvete üksikasjad</li><li>Ooteloleva maksega arved ettevõtte kohta</li><li>Ooteloleva maksega arved hankijagrupi kohta</li></ul>                                                                                          |


