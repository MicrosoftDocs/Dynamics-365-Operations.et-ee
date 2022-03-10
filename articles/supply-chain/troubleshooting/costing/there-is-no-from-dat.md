---
title: Lehe Kauba hind vahekaardil Aktiivsed hinnad ei ole alguskuupäeva
description: Lehe Kauba hind vahekaardil Aktiivsed hinnad ei ole alguskuupäeva.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: dc0071bc508fc1b2fcfa5071f0756434641b7e6f872308ed4febb0cb34d37840
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730126"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a>Lehe Kauba hind vahekaardil Aktiivsed hinnad ei ole alguskuupäeva

KB number: 4613548

## <a name="symptoms"></a>Sümptomid

Ei ole **Alguskuupäev** väärtust **Kauba hind** vahekaardil **Ühiku hind** lehel.

## <a name="resolution"></a>Eraldusvõime

Ootele määratud hinna **alguskuupäeva** väärtust (kehtiv kuupäev) ei kanta üle aktiivsesse hinda.

Kauba kulukirje esmakordsel sisestamisel on sellel olek *Ootel* ja plaanitav jõustumiskuupäev. Kauba kulukirje aktiveerimisel määratakse olekuks *Aktiivne* ja jõustumiskuupäevaks määratakse aktiveerimiskuupäev. Seetõttu on aktiivse hinna aktiveerimiskuupäev alati tegelik aktiveerimise kuupäev.

Lisateavet leiate teemast [Kulude versioonide ülevaade](../../cost-management/costing-versions.md).
