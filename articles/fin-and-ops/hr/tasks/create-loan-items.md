---
title: Loo laenuartikleid
description: Laenuartiklid on kirjed, mis aitavad teil jälgida füüsilisi kaupu, näiteks telefone või arvuteid, mida teie ettevõte töötajatele laenab.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75b2f17eb41ead7422276f72429eb6ede2ef4759
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/19/2019
ms.locfileid: "856227"
---
# <a name="create-loan-items"></a>Loo laenuartikleid

[!include [task guide banner](../../includes/task-guide-banner.md)]

Laenuartiklid on kirjed, mis aitavad teil jälgida füüsilisi kaupu, näiteks telefone või arvuteid, mida teie ettevõte töötajatele laenab. Iga füüsiline kaup peab laenuartiklile vastama. Iga laenuartikli kirjel tuleb kirjeldada, mida laenatakse, kes on laenu eest vastutav ja mitmeks päevaks võib artiklit laenata. Saate luua mitu laenuartiklit, nagu võtmed, pääsukaardid või vormirõivad, samal ajal. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="create-loan-types"></a>Laenutüüpide loomine
1. Avage Inimressursid > Töötajad > Laenuartiklid > Laenutüübid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Laenu tüüp.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Sisestage päevade arv, mille võrra võib seda tüüpi laenuartiklite tagastamine tähtaja ületada. 
6. Klõpsake nuppu Salvesta.
7. Sulgege leht.
8. Värskendage lehte.

## <a name="create-loan-items"></a>Laenuartiklite loomine
1. Avage Inimressursid > Töötajad > Laenuartiklid > Laenuartiklid.
2. Klõpsake suvandit Loo laenuartikleid.
3. Väljale Kogus väljale Protsessi kogus.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Klõpsake väljal Laenu tüüp otsingu avamiseks ripploendi nuppu.
6. Otsige loendist ja valige soovitud kirje.
7. Klõpsake loendis valitud real olevat linki.
8. Sisestage päevade arv, mille jooksul artikkel võib olla välja laenatud.
    * Lehe Laenatud seadmed välja Plaanitud tagastus vaikeväärtus arvutatakse, liites tänasele kuupäevale selle numbri.  
9. Klõpsake väljal Vastutav isik otsingu avamiseks ripploendi nuppu.
10. Klõpsake Vali.
11. Sisestage number väljale Algväärtus.
12. Sisestage number väljale Intervall.
13. Sisestage väärtus väljale Vorming.
    * Näiteks kui laenuartikli algusnumber on 10, sisestage väljale Vorming kaks numbri sümbolit.  
14. Klõpsake nuppu OK.
15. Värskendage lehte.

