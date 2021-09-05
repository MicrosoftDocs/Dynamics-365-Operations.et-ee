---
title: Integreeritud koondplaneerimise ja planeerimise optimeerimise vahelised erinevused
description: Selles teemas loetletakse funktsioonid, mida plaanimise optimeerimine veel ei toeta ja mida pole loetletud planeerimise optimeerimise sobivuse analüüsi lehel.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a102f1d77362f650c060ce5d0aee5b62d2102532
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344950"
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
| Numbrijada plaanitud tellimustele | Numbrijadasid plaanitud tellimustele ei toetata. Plaanitud tellimuste numbrid luuakse teeninduse poolel. |
| Plaani kopeerimine, plaani kustutamine ja plaani versiooni puhastamine | <p>Järgmised üksused on navigeerimispaani jaotises **Koondplaneerimine \> Koondplaneerimine \> Plaanide haldamine** keelatud.</p><ul><li>Plaani koopia</li><li>Kustuta plaan</li><li>Plaani versiooni puhastamine</li></ul> |
| Tagastustellimused | Tagastustellimusi ei arvestata. |
| Planeerimisega seotud funktsioonid | Üksikasju vt teemast [Planeerimine lõpmatu võimsusega](infinite-capacity-planning.md#limitations). |
| Transpordikalendrid | Väärtust lehe **Tarneviisid** veerus **Transpordikalender** eiratakse. |

## <a name="additional-resources"></a>Lisaressursid

- [Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md)
- [Parameetrid, mida planeerimise optimeerimine ei kasuta](not-used-parameters.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
