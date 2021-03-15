---
title: Negatiivsete vabade kogustega plaanimine
description: Selles teemas selgitatakse, kuidas plaanimise optimeerimise kasutamisel käsitsetakse negatiivset kaubavaru.
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
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 72ed2ba42c6233461743492fe6776f376195ada6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983462"
---
# <a name="planning-with-negative-on-hand-quantities"></a>Negatiivsete vabade kogustega plaanimine

[!include [banner](../../includes/banner.md)]

Kui süsteem näitab negatiivset kaubavaru kogust, käsitleb planeerimise mootor kogust kui 0 (null), et aidata vältida ületarnet. See funktsioon töötab järgmiselt.

1. Planeerimise optimeerimise funktsioon koondab vabad kogused laovarude dimensioonide madalaimal tasemel. (Näiteks kui *asukoht* ei ole laevarude dimensioon, koondab plaanimise optimeerimine vabad kogused *lao* tasemel.)
1. Kui laovarude dimensioonide kaubavaru kogus on negatiivne, eeldab süsteem, et vaba kogus on tegelikult 0 (null).

> [!IMPORTANT]
> Planeerimise süsteem võib olla ainult nii täpne kui sisendandmed. Kui sisendandmed on ebatäpsed, näitavad negatiivsed varude kirjed, et Microsoft Dynamics 365 Supply Chain Managementi varude teave on reaalse maailmaga sünkroonist väljas. Seetõttu on planeerimise tulemus vigane. Täpse planeerimise tulemuse saamiseks tuleb minimeerida kirjete arv, mis näitavad negatiivset vaba kogust.

## <a name="example-1"></a>Näide 1

Ladu 13 on konfigureeritud järgmisel viisil.

- **Katvuse kood:** min/max
- **Miinimum:** 15 tükki (tk)
- **Maksimum:** 25 tk

Laovarude dimensioonide madalaim tase on *ladu* ja järgmised vabad kogused salvestatakse *asukoha* tasemel.

- **Tegevuskoht 1, ladu 13, asukoht 1:** 20 tk
- **Tegevuskoht 1, ladu 13, asukoht 2:** &minus;8 tk

Seega on lao 13 kaubavaru kogus 12 tk (= 20 tk &minus; 8 tk).

Sellisel juhul kasutab planeerimise mootor kaubavaru kogust 12 tk lao 13 jaoks.

Tulemuseks on plaanitud tellimus 13 tk (= 25 tk &minus;12 tk), et täita ladu 13 koguselt 12 tk kogusele 25 tk.

## <a name="example-2"></a>Näide 2

Ladu 13 on konfigureeritud järgmisel viisil.

- **Katvuse kood:** min/max
- **Miinimum:** 15 tk
- **Maksimum:** 25 tk

Laovarude dimensioonide madalaim tase on *ladu* ja järgmised vabad kogused salvestatakse *asukoha* tasemel.

- **Tegevuskoht 1, ladu 13, asukoht 1:** 4 tk
- **Tegevuskoht 1, ladu 13, asukoht 2:** &minus;8 tk

Seega on lao 13 kaubavaru kogus &minus;4 tk (= 4 tk &minus; 8 tk). Teisisõnu on see vähem kui 0 (null).

Sellisel juhul eeldab planeerimise mootor, et lao 13 vaba kogus on 0 tk, mitte &minus;4 tk.

Tulemuseks on plaanitud tellimus 25 tk (= 25 tk &minus; 0 tk), et täita ladu 13 koguselt 0 tk kogusele 25 tk.

## <a name="related-resources"></a>Seotud ressursid

[Planeerimise optimeerimise ülevaade](planning-optimization-overview.md)

[Planeerimise optimeerimisega alustamine](get-started.md)

[Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md)

[Plaani ajaloo ja plaanimise logide vaatamine](plan-history-logs.md)

[Planeerimistöö tühistamine](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]