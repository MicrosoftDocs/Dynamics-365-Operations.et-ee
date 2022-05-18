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
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26bf5a83a6d25e99996ec4219c5fbbeed806e22d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693720"
---
# <a name="create-loan-items"></a>Loo laenuartikleid


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Laenuartiklid on kirjed, mis aitavad teil jälgida füüsilisi kaupu, näiteks telefone või arvuteid, mida teie ettevõte töötajatele laenab. Iga füüsiline kaup peab laenuartiklile vastama. Iga laenuartikli kirjel tuleb kirjeldada, mida laenatakse, kes on laenu eest vastutav ja mitmeks päevaks võib artiklit laenata. Saate luua mitu laenuartiklit, nagu võtmed, pääsukaardid või vormirõivad, samal ajal. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="create-loan-types"></a>Laenutüüpide loomine
1. Minge tüübile **InimressursidWorkersLoan** > **·** > **itemsLoan** > **·**.
2. Klõpsake valikut **Uus**.
3. **Tippige väärtus väljale** Laenu tüüp.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Sisestage päevade arv, mille võrra võib seda tüüpi laenuartiklite tagastamine tähtaja ületada. 
6. Klõpsake nuppu **Salvesta**.
7. Sulgege leht.
8. Värskendage lehte.

## <a name="create-loan-items"></a>Laenuartiklite loomine
1. Minge kaupade **kausta InimressursidWorkersLoan** > **·** > **itemsLoan** > **·**.
2. Klõpsake nuppu **Loo laenuüksused**.
3. **Sisestage number** väljale Kogus.
4. Sisestage väärtus väljale **Kirjeldus**.
5. **Otsingu avamiseks** klõpsake väljal Laenu tüüp ripploendit.
6. Otsige loendist ja valige soovitud kirje.
7. Klõpsake loendis valitud real olevat linki.
8. Sisestage päevade arv, mille jooksul artikkel võib olla välja laenatud.
    * Lehe Laenatud seadmed välja Plaanitud tagastus vaikeväärtus arvutatakse, liites tänasele kuupäevale selle numbri.  
9. **Otsingu avamiseks** klõpsake väljal Vastutav isik ripploendit.
10. Klõpsake **Vali**.
11. Sisestage **number** väljale Algväärtus.
12. Sisestage number väljale **Intervall**.
13. **Tippige väärtus** väljale Vorming.
    * Näiteks kui laenukauba algusnumber on 10, sisestage vormingu väljale kaks **numbrisümbolit**.  
14. Klõpsake valikut **OK**.
15. Värskendage lehte.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
