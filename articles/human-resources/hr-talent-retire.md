---
title: Pensionile jäämine Dynamics 365 Talent – väljaminekud – väljamineku- ja pardarakendused
description: See teema kirjeldab rakenduste -Rakenduste Dynamics 365 Talent JaRakendusterakenduste töölt kõrvaldamine.
author: twheeloc
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: e17b92621f05ad8483a7c578bfaece58a530df2d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691998"
---
# <a name="dynamics-365-talent-attract-and-onboard-apps-retirement"></a>Dynamics 365 Talent: Attract ja rakenduste pensionile jäämine


2019. a. detsembris soovitame välja 1. veebruari 2022 Dynamics 365 Talent pensionile jäämise – Ärirakendus ja Plaanimisel olevad rakendused, andes klientidele plaanimiseks kaks aastat.

Lisateavet nende rakenduste pensionilemineku kohta vt:
 - [Vananemine Dynamics 365 Talent –rakendus ja rakendused Dynamics 365 Talent: Onboard](https://community.dynamics.com/365/humanresources/b/dynamics365forhumanresources/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)
 - [Edukama tööjõu ülesehitamine koos Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources)

Jätkame toetamist Dynamics 365 Human Resources, mis aitab meie klientidel saada tööjõuülevaateid, mis on vajalikud andmepõhiste töötajakogemuste kogumiseks mitmetes valdkondades, nagu näiteks:

- Hüvitus
- Kasu
- Puhkused ja puudumine
- Vastavus
- Palgaarvestus
- Jõudluse tagasiside
- Koolitused ja sertifitseerimine
- Iseteeninduse programmid

## <a name="dynamics-365-talent-apps-retirement-faq"></a>Dynamics 365 Talent rakenduste pensionile jäämise KKK

### <a name="what-is-the-user-experience-for-both-dynamics-365-talent---attract-and-onboard-apps-starting-february-1-2022"></a>Milline on kasutajakogemus rakendustes Dynamics 365 Talent Omakaad ja Jaerakendus alates 1. veebruarist 2022?

Kasutajad ei saa avaldusi kasutada ja nad suunatakse pensionile.

### <a name="can-customers-continue-to-export-data-for-both-dynamics-365-talent---attract-and-onboard-apps-after-february-1-2022"></a>Kas kliendid jätkavad andmete Dynamics 365 Talent eksportimist niiRakenduste kui kaboardrakenduste jaoks pärast 1. veebruari 2022?
  
Ei, 2019. a. detsembris 2019 teatati välja pensionile jäämine ja nõutavad ekspordivõimalused olid antud kuni 1. veebruarini 2022. 

### <a name="will-the-customers-data-related-to-both-dynamics-365-talent---attract-and-onboard-apps-in-dataverse-be-deleted-after-february-1-2022"></a>Kas kliendi andmed on seotud Dynamics 365 Talent niiRakendustega kui Dataverse kaboard rakendustega – kustutatakse pärast 1. veebruari 2022?

Ei, üksused Dataverse jäävad kliendi keskkonda isegi pärast Microsoft Dataverse pensionile jäämist, v.a juhul, kui inimkapitali halduse Anne'i lahendus on kustutatud või desinstallitud.

### <a name="i-know-the-name-of-the-talent-environment-how-can-i-see-the-attract-and-onboard-data-in-dataverse"></a>Ma ei tea Anne'i keskkonna nime. Kuidas saab kliente ja kliente näha Dataverse?

1.  Sisselogimine Power Apps: https://make.powerapps.com
2.  Valige keskkond, milles soovite vaadata Lisama ja Lisa andmeid.
3.  Avage > **Dataverse tabelid**. 
4.  Tippige otsingusse **sõna msdyn_ "msdyn_"**. Kui te näete tabelite loendit, alustades "msdyn_" + tabelinimedega (nt: msdyn_candidate), siis olete leidnud keskkonna Andmetega Rõhk ja Sisseostja.

[![Power Apps](./media/Powerapps.png)](./media/Powerapps.png)

### <a name="i-dont-know-the-name-of-the-talent-environment-how-can-i-find-the-environment-that-has-the-data-for-the-dynamics-365-talent-attract-and-dynamics-365-talent-onboard-applications"></a>Ma ei tea Anne'i keskkonna nime. Kuidas leida keskkonda, kus on nende ja rakenduste Dynamics 365 Talent: Attract andmed Dynamics 365 Talent: Onboard?

1)  Logige halduskeskusesse Power Platform sisse: https://admin.powerplatform.microsoft.com/
2)  Valige **Keskkonnad**.
3)  Valige hinnamiseks konkreetne keskkond.
4)  Valige **Ressursid > Dynamics 365 rakenduste jaoks**.
5)  Kui näete, et **HCM Anne'i** lahendus on installitud, peaks selles keskkonnas olema Ajastamise jaTahvlile talletatud andmed. 

[![Power Platform](./media/HCMTalent.png)](./media/HCMTalent.png)

> [!NOTE] 
> Seda **HCM Anne'i** lahendust kasutatakse ka selles.Dynamics 365 Human Resources
