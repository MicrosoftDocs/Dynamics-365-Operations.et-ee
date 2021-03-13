---
title: Plaanimistöö tühistamine
description: See teema selgitab, kuidas tühistada aktiivne plaanimistöö, mis kasutab funktsiooni Plaanimise optimeerimine.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 7cee11e6d9e8bc2fe83f5369554ae9ff9ee2b741
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008212"
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
