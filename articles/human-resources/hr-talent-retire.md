---
title: Rakenduste meelitamine Dynamics 365 Talent ja pardal olemine
description: See teema kirjeldab rakenduste - Attract ja Onboard pensionile jäämist Dynamics 365 Talent.
author: twheeloc
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: df33f35f66e356c3c2a99f0d81ebba1d0f34b5d9
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069400"
---
# <a name="dynamics-365-talent-attract-and-onboard-apps-retirement"></a>Dynamics 365 Talent: Attract ja pardarakenduste pensionile jäämine


2019. aasta detsembris teatasime 1. veebruari 2022. aasta pensionile jäämisest Dynamics 365 Talent - Attract ja Onboard rakendused, andes oma klientidele kaks aastat planeerida.

Lisateavet nende rakenduste pensionile jäämise kohta leiate järgmistest andmetest.
 - [Pensionile jäämine Dynamics 365 Talent – meelitamine ja Dynamics 365 Talent: Onboard rakendused](https://community.dynamics.com/365/humanresources/b/dynamics365forhumanresources/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)
 - [Edukama tööjõu loomine Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources)

Jätkame toetamist Dynamics 365 Human Resources, mis aitab meie klientidel saada tööjõu ülevaateid, mis on vajalikud andmepõhiste töötajate kogemuste loomiseks mitmes valdkonnas, näiteks:

- Hüvitus
- Kasu
- Puhkused ja puudumine
- Vastavus
- Payroll
- Jõudluse tagasiside
- Koolitused ja sertifitseerimine
- Iseteeninduse programmid

## <a name="dynamics-365-talent-apps-retirement-faq"></a>Dynamics 365 Talent rakendused pensionile KKK

### <a name="what-is-the-user-experience-for-both-dynamics-365-talent---attract-and-onboard-apps-starting-february-1-2022"></a>Milline on kasutajakogemus nii Dynamics 365 Talent - Attract kui ka Onboard rakenduste jaoks alates 1. veebruarist 2022?

Kasutajad ei saa rakendusi kasutada ja suunatakse pensionilehele.

### <a name="can-customers-continue-to-export-data-for-both-dynamics-365-talent---attract-and-onboard-apps-after-february-1-2022"></a>Kas kliendid saavad pärast 1. veebruari 2022 jätkata andmete eksportimist nii - Attracti kui ka Dynamics 365 Talent Pardal olevate rakenduste jaoks?
  
Ei, pensionile jäämisest teatati 2019. aasta detsembris ja vajalikud ekspordivõimalused anti kuni 1. veebruarini 2022. 

### <a name="will-the-customers-data-related-to-both-dynamics-365-talent---attract-and-onboard-apps-in-dataverse-be-deleted-after-february-1-2022"></a>Kas kliendi andmed, mis on seotud nii - Attract kui ka Dynamics 365 Talent Onboard rakendustega Dataverse, kustutatakse pärast 1. veebruari 2022?

Ei, üksused jäävad kliendi Dataverse keskkonda ka pärast pensionile jäämist, välja arvatud juhul, Microsoft Dataverse kui Human Capital Management Talenti lahendus kustutatakse või desinstallitakse.

### <a name="i-know-the-name-of-the-talent-environment-how-can-i-see-the-attract-and-onboard-data-in-dataverse"></a>Ma tean talentide keskkonna nime. Kuidas ma näen Attracti ja Pardal andmeid Dataverse?

1.  Power Apps logi sisse:https://make.powerapps.com
2.  Valige keskkond, kus soovite näha Attracti ja Onboardi andmeid.
3.  Avage **Dataverse > tabelid**. 
4.  Tippige otsingusse **"msdyn_"**. Kui näete tabelite loendit, mis algab tabelite "msdyn_" + tabelinimedega (näide: msdyn_candidate), siis olete leidnud keskkonna Attracti ja Onboardi andmetega.

[![Power Apps](./media/Powerapps.png)](./media/Powerapps.png)

### <a name="i-dont-know-the-name-of-the-talent-environment-how-can-i-find-the-environment-that-has-the-data-for-the-dynamics-365-talent-attract-and-dynamics-365-talent-onboard-applications"></a>Ma ei tea talentide keskkonna nime. Kuidas leida keskkond, kus on andmed rakenduste ja Dynamics 365 Talent: Attract rakenduste kohta Dynamics 365 Talent: Onboard?

1)  Power Platform logige sisse halduskeskusesse:https://admin.powerplatform.microsoft.com/
2)  Valige **Keskkonnad**.
3)  Valige konkreetne keskkond, mida hinnata.
4)  Valige **Ressursid Dynamics 365 rakenduste** >.
5)  Kui näete **HCM Talenti** lahendust installitud, peaks selles keskkonnas olema Attracti ja Pardal olevad andmed. 

[![Power Platform](./media/HCMTalent.png)](./media/HCMTalent.png)

> [!NOTE] 
> **HCM Talent** lahendust kasutatakse Dynamics 365 Human Resources ka.
