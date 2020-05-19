---
title: Puhkusetaotluse töövoo loomine
description: Looge puhkuse- ja puudumistaotluse töövoog, et hallata puhkusetaotlusi rakenduses Dynamics 365 Human Resources järjepidevalt.
author: andreabichsel
manager: AnnBe
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c2e994d11bbd45907a48c1f3955fa751a676a327
ms.sourcegitcommit: e69cfc74e9dbce64ae0e1ab7cd441e5ae6efd4c9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/08/2020
ms.locfileid: "3353684"
---
# <a name="create-a-leave-request-workflow"></a>Puhkusetaotluse töövoo loomine

Saate luua töövoo rakenduses Dynamics 365 Human Resources, et järjepidevalt hallata oma puhkuse- ja puudumistaotlusi. Töövoog **Puhkused ja puudumised** võimaldab teil teha järgmist.

- Ülesannete määratlemine
- Määramine, kes peab ülesanded lõpule viima
- Täpsustamine, kes saab taotlusi kinnitada või tagasi lükata

## <a name="create-a-leave-and-absence-request-workflow"></a>Puhkuse- ja puudumistaotluste töövoo loomine

1. Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.

2. Jaotises **Seadistus** valige suvand**Inimressursside töövood**.

3. Valige suvand **Uus** ja seejärel valige **Puhkuse- ja puudumistaotlus**. 

4. Kui kuvatakse teateaken **Kas avada see fail?**, valige käsk **Ava** ja logige oma ettevõtte mandaatidega sisse.

5. Kasutage töövoo redaktorit, et luua puhkusetaotluste jaoks töövoog. Lisateavet töövoogudega töötamise kohta vt teemast [Töövoogude loomise ülevaade](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Puhkuse- ja puudumistaotluste töövoo andmeelemendid

Te saate töövoos puhkuse- ja puudumistaotluste tingimuslike või automaatsete kinnituste loomiseks kasutada järgmisi andmeelemente.

- **Kommentaar**
- **Ettevõte**
- **Looja**
- **Loodud kuupäev ja kellaaeg**
- **Lõppkuupäev**
- **Puhkuse tüüp**
- **Muutja:**
- **Muutmise kuupäev ja kellaaeg**
- **Põhjuse kood**
- **Taotluse ID**
- **Alguskuupäev**
- **Olek** 
- **Edastuskuupäev**
- **Esitas**
- **Inimressursside edastatud**
- **Halduri edastatud**
- **Esitatud järgmise isiku nimel**
- **Töötaja**
- **Töötaja tüüp**

Need näited näitavad, kuidas saate luua erinevat tüüpi töövoo tingimusi, kasutades järgmisi andmeelemente:

- Kasutage tingimuslikus väljavõttes suvandit **Põhjusekood**, et suunata põhjusekoodiga **Operatsioon** haiguslehe taotlused inimressursside üksusele, suunates samas kõik muud põhjusekoodid haldurile. Tingimuslike väljavõtete kohta lisateabe saamiseks vt teemat [Tingimuslike otsuste konfigureerimine töövoos](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow). 

- Kasutage automaatses tegevuses suvandeid **Inimressursside edastatud** ja **Halduri edastatud**, et kinnitada automaatselt puhkusetaotlused, mida need rollid töötajate nimel esitavad. Automaatsete tegevuste kohta lisateabe saamiseks vt teemat [Kinnitusprotsesside konfigureerimine töövoos](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).

- Kasutage tingimuslikus väljavõttes või automaatses tegevuses suvandit **Puhkuse tüüp**, et kontrollida, kuidas töövoog suunab teatud puhkuse tüübiga taotlusi.

## <a name="see-also"></a>Vt ka

- [Puhkuste ja puudumiste ülevaade](hr-leave-and-absence-overview.md)
