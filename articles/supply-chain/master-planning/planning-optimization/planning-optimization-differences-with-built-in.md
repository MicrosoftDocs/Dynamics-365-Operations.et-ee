---
title: Integreeritud koondplaneerimise ja planeerimise optimeerimise vahelised erinevused
description: Selles teemas loetletakse funktsioonid, mida plaanimise optimeerimine veel ei toeta ja mida pole loetletud planeerimise optimeerimise sobivuse analüüsi lehel.
author: ChristianRytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: e271ddd3331d7b5de78f00a02b60a0479879c172
ms.sourcegitcommit: f8b597b09157d934b62bd5fb9a4d05b8f82b5a0e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/26/2021
ms.locfileid: "7700001"
---
# <a name="differences-between-built-in-master-planning-and-planning-optimization"></a>Integreeritud koondplaneerimise ja planeerimise optimeerimise vahelised erinevused

[!include [banner](../../includes/banner.md)]

Plaanimise optimeerimise tulemused võivad erineda integreeritud koondplaneerimise mootori tulemustest. Erinevusi võivad põhjustada ootel funktsioonid. Selles teemas loetletakse funktsioonid, mida plaanimise optimeerimine veel ei toeta ja mida pole loetletud lehel **[Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md)**].

| Funktsioon | Plaanimise optimeerimise praegune käitumine |
|---|---|
| Tegeliku kaaluga tooted | Tegeliku kaaluga tooteid peetakse tavalisteks toodeteks.|
| Laiendatavad dimensioonid | Laiendatavad dimensioonid on plaanitud tellimustel tühjad, isegi kui märkeruut **Laovarude planeerimine dimensioonide kaupa** on lehel **Laoala dimensioonigrupid** või **Jälgimisdimensioonigrupid** valitud. |
| Filtreeritud tootmiste käitamised | Lisateavet vt jaotisest [Tootmise planeerimine - filtrid](production-planning.md#filters). |
| Eelarveplaanimine | Prognooside planeerimist ei toetata. Soovitame teil kasutada koondplaneerimist seal, kus koondplaanile on määratud prognoosimudel. |
| Numbrijada plaanitud tellimustele | Numbrijadasid plaanitud tellimustele ei toetata. Plaanitud tellimuste numbrid luuakse teeninduse poolel. Plaanitud tellimuse numbrit näidatakse tavaliselt 10 numbriga, kuid järjestus on tegelikult üles ehitatud 20 tähemärgile, 10 numbrid tähistavad planeerimiste arvu ja ülejäänud 10 numbrit plaanitud tellimuste arvu. |
| Plaani kopeerimine, plaani kustutamine ja plaani versiooni puhastamine | <p>Järgmised üksused on navigeerimispaani jaotises **Koondplaneerimine \> Koondplaneerimine \> Plaanide haldamine** keelatud.</p><ul><li>Plaani koopia</li><li>Kustuta plaan</li><li>Plaani versiooni puhastamine</li></ul> |
| Tagastustellimused | Tagastustellimusi ei arvestata. |
| Planeerimisega seotud funktsioonid | Üksikasju vt teemast [Planeerimine lõpmatu võimsusega](infinite-capacity-planning.md#limitations). |
| Puhvervaru täitmine | Planeerimise optimeerimine kasutab alati *Tänane kuupäev + hankeaeg* valikut **Täitke minimaalselt** välja **Toode katvus** lehe jaoks. See aitab vältida soovimatuid planeeritud tellimusi ja muid probleeme, sest kui turvavarude hankimise aega ei arvestata, lükkuvad väheste varude jaoks loodud kavandatud tellimused alati tähtaja tõttu edasi. |
| Ohutusvaru sidumine ja võrgunõuded | *Turvavarud* nõude tüüp ei kuulu komplekti ja seda ei kuvata lehel **Võrgu nõuded**. Turvavarud ei kujuta endast nõudlust ega ole seotud nõude kuupäevaga. Selle asemel seab see piirangu sellele, kui palju laoseisu peab alati olema. Planeeritud tellimuste arvutamisel üldplaneerimisel võetakse siiski arvesse välja väärtust **Minimum**. Soovitame teil vaadata lehe **Võrgu nõuded** veergu **Kogunenud kogus**, et näha, kas seda väärtust arvestati. |
| Transpordikalendrid | Väärtust lehe **Tarneviisid** veerus **Transpordikalender** eiratakse. |

## <a name="additional-resources"></a>Lisaressursid

- [Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md)
- [Parameetrid, mida planeerimise optimeerimine ei kasuta](not-used-parameters.md)
- [Kuupäeva ja kellaaja parameetrid, mida planeerimise optimeerimine ei kasuta](date-time-used.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
