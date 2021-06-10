---
title: Soodustuskõlblikkuse reeglite ja poliitikate määratlemine
description: Selles artiklis näidatakse, kuidas luua soodustuse kõlblikkuse reegleid ja poliitikaid ning seejärel soodustustele reegleid määrata.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 046b045fbdda125c5a2259783c0347f687453528
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053149"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Soodustuskõlblikkuse reeglite ja poliitikate määratlemine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas näidatakse, kuidas luua soodustuse kõlblikkuse reegleid ja poliitikaid ning seejärel soodustustele reegleid määrata.  

## <a name="create-benefit-eligibility-policy-rule-type"></a>Soodustuskõlblikkuse poliitika reegli tüübi loomine

1. Avage **Inimressursid > Soodustused > Kõlblikkus > Soodustuskõlblikkuse poliitika reeglitüübid**.
2. Valige suvand **Uus**.
3. Sisestage väljale **Reegli nimi** väärtus.
4. Sisestage väärtus väljal **Kirjeldus**.
5. Valige väljal **Päringu nimi** ripploendi nupp otsingu avamiseks.
6. Valige loendis link valitud reas.
7. Valige käsk **Salvesta**.
8. Sulgege leht.

## <a name="benefit-eligibility-policy"></a>Sooduskõlblikkuse poliitika

1. Avage **Inimressursid > Soodustused > Kõlblikkus > Soodustuskõlblikkuse poliitikad**.
2. Valige olemasolev soodustuse poliitika.
3. Valige loendis link valitud reas.
4. Laiendage jaotisi **Poliitika organisatsioonid**. Saate lisada või eemaldada mis tahes organisatsioone, mida soovite poliitikasse kaasata.
5. Laiendage või ahendage jaotist **Poliitika reeglid**.
6. Leidke loendist varem loodud poliitika reegel.
7. Valige **Poliitika reegli loomine**.
8. Sisestage väljale **Jõustumiskuupäev** kuupäev, alates millest soovite muuta poliitika jõustuvaks.
    * Jõustumis- ja lõppkuupäevade seadistamine võimaldab teil poliitika reegleid edaspidi muuta ja et teil pole vaja poliitika juurde naasta, kui soovite, et need muudatused jõustuksid.  
9. Vajadusel lisage väljale **Lisa tingimus** kui-tingimus.
    * Näiteks kui soovisite reeglit rakendada ainult müügijuhtidele, saite luua Kui tingimuse, mis ütleb järgmist: kui ametikoha kirjeldus võrdub müügijuhi omaga. Saate reeglisse lisada mitu kui-tingimust koos.  
10. Valige nupp **OK**.
11. Sulgege leht.

## <a name="assign-rule-to-benefit"></a>Reegli määramine soodustusele

1. Avage **Personaliarvestus > Soodustused > Soodustused**.
2. Otsige loendist ja valige soovitud kirje.
3. Valige loendis link valitud reas.
4. Laiendage või ahendage jaotist **Sobivuse reeglid**.
5. Valige suvand **Redigeeri**.
6. Valige väljal **Sobivus** väärtus reegel.
7. Valige väljal **Reegli tüüp** varem loodud reegel.
9. Valige loendis link valitud reas.
10. Valige käsk **Salvesta**.
11. Sulgege vorm.



[!INCLUDE[footer-include](../includes/footer-banner.md)]