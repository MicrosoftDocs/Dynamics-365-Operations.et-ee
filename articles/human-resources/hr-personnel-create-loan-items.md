---
title: Loo laenuartikleid
description: Laenuartiklid on kirjed, mis aitavad teil jälgida füüsilisi kaupu, näiteks telefone või arvuteid, mida teie ettevõte töötajatele laenab.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21127c46615015c30e06465b390f67b835e746cb
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068130"
---
# <a name="create-loan-items"></a>Loo laenuartikleid


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Laenuartiklid on kirjed, mis aitavad teil jälgida füüsilisi kaupu, näiteks telefone või arvuteid, mida teie ettevõte töötajatele laenab. Iga füüsiline kaup peab laenuartiklile vastama. Iga laenuartikli kirjel tuleb kirjeldada, mida laenatakse, kes on laenu eest vastutav ja mitmeks päevaks võib artiklit laenata. Saate luua mitu laenuartiklit, nagu võtmed, pääsukaardid või vormirõivad, samal ajal. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="create-loan-types"></a>Laenutüüpide loomine
1. Avage puhasja **human resourcesWorkersLoan** > **·** > **itemsLoan** > **types**.
2. Klõpsake valikut **Uus**.
3. Tippige väljale **Laenu liik** väärtus.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Sisestage päevade arv, mille võrra võib seda tüüpi laenuartiklite tagastamine tähtaja ületada. 
6. Klõpsake nuppu **Salvesta**.
7. Sulgege leht.
8. Värskendage lehte.

## <a name="create-loan-items"></a>Laenuartiklite loomine
1. Avage **puhasüksusedTöölisedLoan** > **·** > **itemsLoan** > **items**.
2. Klõpsake nuppu **Loo laenukaubad**.
3. Sisestage väljale **Kogus** number.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Otsingu avamiseks klõpsake väljal **Laenu tüüp** rippmenüü nuppu.
6. Otsige loendist ja valige soovitud kirje.
7. Klõpsake loendis valitud real olevat linki.
8. Sisestage päevade arv, mille jooksul artikkel võib olla välja laenatud.
    * Lehe Laenatud seadmed välja Plaanitud tagastus vaikeväärtus arvutatakse, liites tänasele kuupäevale selle numbri.  
9. **Otsingu avamiseks klõpsake väljal Vastutav** isik rippmenüüd.
10. Klõpsake **Vali**.
11. Sisestage väljale **Algväärtus** number.
12. Sisestage number väljale **Intervall**.
13. Tippige väljale **Vorming** väärtus.
    * Näiteks kui laenukauba algusnumber on 10, sisestage väljale **Vorming** kaks numbritähist.  
14. Klõpsake valikut **OK**.
15. Värskendage lehte.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
