---
title: Kulumisoovituse koostamine
description: See artikkel kirjeldab, kuidas kulumi pakktöötluse ettepanekud töötavad ja selgitab põhivara kulumisoovitust.
author: abruer
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1f39a1412c6f96fe0a8261602a88a6a3c3cd6b8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858492"
---
# <a name="create-a-depreciation-proposal"></a>Kulumisoovituse koostamine

[!include [banner](../../includes/banner.md)]

See artikkel kirjeldab, kuidas kulumi pakktöötluse ettepanekud töötavad ja selgitab põhivara kulumisoovitust. See ülesanne kasutab demoettevõtet USMF ja raamatupidaja rolli.


## <a name="create-a-depreciation-proposal"></a>Kulumisoovituse koostamine
1. Navigeerimispaanil minge töölehe sisestuste **> ja > Looge kulumisoovitus**.
2. Väljal **Töölehe nimi** valige suvand rippmenüüst.
3. Sisestage kuupäev väljale **Lõppkuupäev**.

    - Valige suvand **Summeeri kulum**, et summerida igakuised kulumid ühele töölehe reale.  
    - Näiteks, kui lõpukuupäeva väärtus on 31. märts 2015, siis luuakse järgmine kirjeldus: „Kulum alates 31. jaanuar 2015”. Soovitud töölehe ridade väljale **Kuupäev** sisestatakse 31. märts 2015.  
    - Kulumi soovitust saab filtreerida vara, vara grupi või muude kriteeriumide alusel, kasutades suvandit **Filter**.  
    - Kui kasutate vormi **Looge põhivara soetamise või kulumi pakkumisi** saate koostada kulumisoovitusi partiina. See on soovitatav suuremate soovituste puhul, mis kasutavad rohkem süsteemi ressursse. Kui valite partii suvandi, saate töö ajal endiselt muid ülesandeid teha. Kui soovitate kulumit sel moel, arvutatakse põhivarade väärtusmudelite kulum.  

4. Valige käsk **Loo tööleht**.

## <a name="review-depreciation-entries"></a>Kulumiraamatu kannete ülevaade
1. Avage navigeerimispaneelil **Moodulid > Põhivarad > Töölehe kanded > Põhivarade tööleht**.
2. Otsige loendist ja valige soovitud kirje.
3. Valige **Read**.
4. Valige **Sisesta**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
