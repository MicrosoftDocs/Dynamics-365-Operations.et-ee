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
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026454"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a>Lehe Kauba hind vahekaardil Aktiivsed hinnad ei ole alguskuupäeva

KB number: 4613548

## <a name="symptoms"></a>Sümptomid

Ei ole **Alguskuupäev** väärtust **Kauba hind** vahekaardil **Ühiku hind** lehel.

## <a name="resolution"></a>Eraldusvõime

Ootele määratud hinna **alguskuupäeva** väärtust (kehtiv kuupäev) ei kanta üle aktiivsesse hinda.

Kauba kulukirje esmakordsel sisestamisel on sellel olek *Ootel* ja plaanitav jõustumiskuupäev. Kauba kulukirje aktiveerimisel määratakse olekuks *Aktiivne* ja jõustumiskuupäevaks määratakse aktiveerimiskuupäev. Seetõttu on aktiivse hinna aktiveerimiskuupäev alati tegelik aktiveerimise kuupäev.

Lisateavet leiate teemast [Kulude versioonide ülevaade](../../cost-management/costing-versions.md).
