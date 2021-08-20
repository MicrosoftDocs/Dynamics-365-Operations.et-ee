---
title: Kulumisoovituse koostamine
description: Teemas kirjeldatakse, kuidas töötavad kulumi pakettsoovitused, ja selgitatakse, kuidas soovitada põhivarade kulumit.
author: abruer
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a6cf285e8764af8c6525fb3f9cbec7306917e57e832777588e8c2c1d4aeed818
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719242"
---
# <a name="create-a-depreciation-proposal"></a>Kulumisoovituse koostamine

[!include [banner](../../includes/banner.md)]

Teemas kirjeldatakse, kuidas töötavad kulumi pakettsoovitused, ja selgitatakse, kuidas soovitada põhivarade kulumit. See ülesanne kasutab demoettevõtet USMF ja raamatupidaja rolli.


## <a name="create-a-depreciation-proposal"></a>Kulumisoovituse koostamine
1. Navigeerimispaanil avage **Moodulid > Põhivarad > Töölehe kanded > Loo kulumisoovitus**.
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