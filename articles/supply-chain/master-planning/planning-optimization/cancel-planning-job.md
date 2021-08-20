---
title: Plaanimistöö tühistamine
description: See teema selgitab, kuidas tühistada aktiivne plaanimistöö, mis kasutab funktsiooni Plaanimise optimeerimine.
author: ChristianRytt
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 85dffae7e5484d34d0cfa4bf44649fcdd69fc36804802ad9f02c122adf5d9785
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771454"
---
# <a name="cancel-a-planning-job"></a>Plaanimistöö tühistamine

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Managementis saab tühistada aktiivse plaanimistöö, mis kasutab funktsiooni Plaanimise optimeerimine. Kui valite dialoogiboksis käsu **Tühista**, kui plaanimise optimeerimise töö käivitatakse otse kasutajaliidesest (mitte taustal), ei tühista see plaanimise optimeerimise tööd. Isegi kui kuvatakse hoiatusteade (nt „Toiming tühistatud”), tuleb teil siiski kasutada järgmisi samme, et tühistada plaanimise optimeerimisega plaanimistöö.


Aktiivse plaanimistöö tühistamiseks toimige järgmiselt. 

> [!NOTE]
> Tühistada saab ainult aktiivseid töid.

1. Avage **Koondplaneerimine \> Seadistus \> Plaanid**.
2. Valige planeerimise jaoks sobiv plaan.
3. Valige **Ajalugu**.
4. Valige tühistamiseks plaanimistöö.
5. Valige **Tühista**.

Tööolek on **Tühistamine**, kuni Plaanimise optimeerimise teenus kinnitab, et töö on tühistatud. Olek muudetakse seejärel väärtusele **Tühistatud**.

> [!NOTE]
> Olekumuudatuste nägemiseks peate värskendama lehte, valides nupu **Värskenda**.

## <a name="additional-resources"></a>Lisaressursid

[Planeerimise optimeerimise ülevaade](planning-optimization-overview.md)

[Planeerimise optimeerimisega alustamine](get-started.md)

[Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md)

[Plaani ajaloo ja plaanimise logide vaatamine](plan-history-logs.md)

[Plaanile filtrite rakendamine](plan-filters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]