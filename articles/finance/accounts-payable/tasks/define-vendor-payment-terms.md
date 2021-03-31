---
title: Hankija maksetingimuste määratlemine
description: Selles teemas selgitatakse, kuidas sätestada maksetingimusi tarnija arvete jaoks.
author: abruer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6a37272694609be14b566dae3c6cf561d4c6d2f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227228"
---
# <a name="define-vendor-payment-terms"></a>Hankija maksetingimuste määratlemine

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse, kuidas sätestada maksetingimusi tarnija arvete jaoks. See ülesanne kasutab demoettevõtte USMF andmeid.

1. Avage **Navigeerimispaan > Moodulid > Ostureskontro > Makse häälestus > Maksetingimused**.
2. Valige suvand **Uus**. Lehte Maksetingimused kasutatakse määratlemaks, kuidas tähtaega arvutatakse. Seda ei kasutata määratlemaks, kuidas skonto kuupäeva arvutatakse.  
3. Sisestage väärtus väljale **Maksetingimused**.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Sisestage number väljale **Päevad**. Siin sisestatud numbrit kasutatakse tähtajale või makseviisis määratletud perioodi lõppu lisamiseks. Näiteks kui valite **Neto**, lisatakse number tähtajale. **Praeguse kuu** valimisel lisatakse tähtaja arvutamiseks number praeguse kuu viimasele päevale.  
6. Valige käsk **Salvesta**.
7. Sulgege leht.
8. Avage **Ostureskontro > Makse seadistus > Skontod**.
9. Valige suvand **Uus**.
10. Sisestage ID väljale **Skonto**.
11. Sisestage väärtus väljale **Kirjeldus**.
12. Kui hankija pakub mitmetasandilist allahindlust, valige järgmine skonto pärast praeguse aegumist.
13. Sulgege leht.
14. Sisestage number väljale **Päevad**. Väljale **Päevad** sisestatud kogust kasutatakse skonto kuupäeva arvutamiseks selle põhjal, milline suvand väljal **Neto/praegune** valiti. **Neto** valimisel lisatakse skonto kuupäeva määramiseks kogus arve kuupäevale. **Praeguse kuu** valimisel lisatakse skonto kuupäeva määramiseks kogus arve kuupäevale.  
15. Sisestage skonto protsent väljale **Allahindlus**. 
16. Sisestage põhikonto, kuhu skonto sisestatakse kliendiarvete puhul, seejärel sisestage põhikonto, kuhu skonto sisestatakse hankija arvete puhul. Kui suvand **Allahindluse vastaskontod** on seatud valikule **Kasuta hankija allahindluse jaoks põhikontot**, siis kasutatakse põhikontot. Kui suvand on seatud valikule **Kontod arve real**, sisestatakse skonto arve ridadel vara/kulu kontodele.  
17. Valige käsk **Salvesta**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]