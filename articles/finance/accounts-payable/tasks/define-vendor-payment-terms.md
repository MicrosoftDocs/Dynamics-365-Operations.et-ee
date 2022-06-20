---
title: Hankija maksetingimuste määratlemine
description: See artikkel selgitab, kuidas hankija arvetele maksetingimusi seadistada.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a676856ed43bf1b78684eac0682e0fdef9c84083
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906467"
---
# <a name="define-vendor-payment-terms"></a>Hankija maksetingimuste määratlemine

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas hankija arvetele maksetingimusi seadistada. See ülesanne kasutab demoettevõtte USMF andmeid.

1. Avage **Navigeerimispaan > Moodulid > Ostureskontro > Makse häälestus > Maksetingimused**.
2. Valige suvand **Uus**. Maksetingimuste **lehte** kasutatakse tähtaja arvutamise määratlemiseks. Seda ei kasutata määratlemaks, kuidas skonto kuupäeva arvutatakse.  
3. Sisestage väärtus väljale **Maksetingimused**.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Sisestage number väljale **Päevad**. Siin sisestatud numbrit kasutatakse maksemeetodis määratud tähtaja või perioodi **lõppu lisamiseks**. Näiteks kui valite **Neto**, lisatakse number tähtajale. **Praeguse kuu** valimisel lisatakse tähtaja arvutamiseks number praeguse kuu viimasele päevale.  
6. Valige käsk **Salvesta**.
7. Sulgege leht.
8. Avage **Ostureskontro > Makse seadistus > Skontod**.
9. Valige suvand **Uus**.
10. Sisestage ID väljale **Skonto**.
11. Sisestage väärtus väljale **Kirjeldus**.
12. Kui hankija pakub mitmetasandilist allahindlust, valige järgmine skonto pärast praeguse aegumist.
13. Sulgege leht.
14. Sisestage number väljale **Päevad**. Väljale Päevad **sisestatud kogust kasutatakse** **skonto kuupäeva arvutamiseks,** võttes aluseks väljal Neto/Praegune valitud **variandi**. **Neto** valimisel lisatakse skonto kuupäeva määramiseks kogus arve kuupäevale. **Praeguse kuu** valimisel lisatakse skonto kuupäeva määramiseks kogus arve kuupäevale.  
15. Sisestage skonto protsent väljale **Allahindlus**. 
16. Sisestage põhikonto, kuhu skonto sisestatakse kliendiarvete puhul, seejärel sisestage põhikonto, kuhu skonto sisestatakse hankija arvete puhul. Kui suvand **Allahindluse vastaskontod** on seatud valikule **Kasuta hankija allahindluse jaoks põhikontot**, siis kasutatakse põhikontot. Kui suvand on seatud valikule **Kontod arve real**, sisestatakse skonto arve ridadel vara/kulu kontodele.  
17. Valige käsk **Salvesta**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
