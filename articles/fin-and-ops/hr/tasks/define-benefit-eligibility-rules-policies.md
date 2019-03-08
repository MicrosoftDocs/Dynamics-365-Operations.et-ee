---
title: Soodustuskõlblikkuse reeglite ja poliitikate määratlemine
description: See registreerimine näitab, kuidas luua soodustuse kõlblikkuse reegleid ja poliitikaid ning seejärel soodustustele reegleid määrata.
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d346c3277e8f19020d6aa96cf6961c4c52ac28fb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "341668"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Soodustuskõlblikkuse reeglite ja poliitikate määratlemine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See registreerimine näitab, kuidas luua soodustuse kõlblikkuse reegleid ja poliitikaid ning seejärel soodustustele reegleid määrata.  

Selle kirje loomisel kasutati demoettevõtte USMF-i andmeid.


## <a name="create-benefit-eligibility-policy-rule-type"></a>Soodustuskõlblikkuse poliitika reegli tüübi loomine
1. Avage Inimressursid > Soodustused > Kõlblikkus > Soodustuskõlblikkuse poliitika reeglitüübid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Reegli nimi.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Klõpsake väljal Päringu nimi otsingu avamiseks ripploendi nuppu.
6. Klõpsake loendis valitud real olevat linki.
7. Klõpsake nuppu Salvesta.
8. Sulgege leht.

## <a name="benefit-eligibility-policy"></a>Sooduskõlblikkuse poliitika
1. Avage Inimressursid > Soodustused > Kõlblikkus > Soodustuskõlblikkuse poliitikad.
2. Valige olemasolev soodustuse poliitika.
3. Klõpsake loendis valitud real olevat linki.
4. Laiendage jaotisi Poliitika organisatsioonid.  Siin saate lisada või eemaldada mis tahes organisatsioone, mida soovite poliitikasse kaasata.
5. Laiendage või ahendage jaotist Poliitika reeglid.
6. Leidke loendist varem loodud poliitika reegel.
7. Klõpsake valikut Loo poliitika reegel.
8. Sisestage väljale Jõustumiskuupäev kuupäev, alates millest soovite muuta poliitika jõustuvaks.
    * Jõustumis- ja lõppkuupäevade seadistamine võimaldab teil poliitika reegleid edaspidi muuta ja kõrvaldab vajaduse poliitika juurde naasta, kui soovite, et need muudatused jõustuksid.  
9. 
    * Näiteks kui soovisite reeglit rakendada ainult müügijuhtidele, saite luua Kui tingimuse, mis ütleb järgmist: kui ametikoha kirjeldus võrdub müügijuhi omaga.  Saate operaatoritega And või Or kaasata reeglisse mitu Kui tingimust.  
10. Klõpsake nuppu OK.
11. Sulgege leht.
12. Sulgege leht.

## <a name="assign-rule-to-benefit"></a>Reegli määramine soodustusele
1. Avage Personaliarvestus > Soodustused > Soodustused.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
4. Laiendage või ahendage jaotist Sobivuse reeglid.
5. Klõpsake nuppu Redigeeri.
6. Valige väljal Sobivus reegel loendi alusel.
7. Klõpsake väljal Reegli tüüp otsingu avamiseks ripploendi nuppu.
8. Leidke ja valige loendist varem loodud reegel.
9. Klõpsake loendis valitud real olevat linki.
10. Klõpsake nuppu Salvesta.
11. Sulgege vorm.

