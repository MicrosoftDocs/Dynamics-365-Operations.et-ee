---
title: Puhkusetaotluse töövoo loomine
description: Looge puhkuse- ja puudumistaotluse töövoog, et hallata puhkusetaotlusi rakenduses Dynamics 365 Human Resources järjepidevalt.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a4ce8d0a121e2fa24e3c221a30eb13debd6e44ea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855082"
---
# <a name="create-a-leave-request-workflow"></a>Puhkusetaotluse töövoo loomine

> [!Important]
> Selles artiklis märgitud funktsioonid on klientide jaoks praegu saadaval eraldiseisev Dynamics 365 Human Resources. Osa või kõik funktsioonid on saadaval osana Finance'i taristu tulevasest väljalaskest pärast Finance'i versiooni 10.0.26.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Saate luua töövoo rakenduses Dynamics 365 Human Resources, et järjepidevalt hallata oma puhkuse- ja puudumistaotlusi. Töövoog **Puhkused ja puudumised** võimaldab teil teha järgmist.

- Ülesannete määratlemine
- Määramine, kes peab ülesanded lõpule viima
- Täpsustamine, kes saab taotlusi kinnitada või tagasi lükata

## <a name="create-a-leave-and-absence-request-workflow"></a>Puhkuse- ja puudumistaotluste töövoo loomine

1. Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.

2. Jaotises **Seadistus** valige suvand **Inimressursside töövood**.

3. Valige suvand **Uus** ja seejärel valige **Puhkuse- ja puudumistaotlus**. 

4. Kui kuvatakse teateaken **Kas avada see fail?**, valige käsk **Ava** ja logige oma ettevõtte mandaatidega sisse.

5. Kasutage töövoo redaktorit, et luua puhkusetaotluste jaoks töövoog. Lisateavet töövoogudega töötamise kohta vt teemast [Töövoogude loomise ülevaade](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Puhkuse- ja puudumistaotluste töövoo andmeelemendid

Te saate töövoos puhkuse- ja puudumistaotluste tingimuslike või automaatsete kinnituste loomiseks kasutada järgmisi andmeelemente.

- **summa**
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

- Kasutage tingimuslikus väljavõttes suvandit **Põhjusekood**, et suunata põhjusekoodiga **Operatsioon** haiguslehe taotlused inimressursside üksusele, suunates samas kõik muud põhjusekoodid haldurile. Tingimuslike väljavõtete kohta lisateabe saamiseks vt teemat [Tingimuslike otsuste konfigureerimine töövoos](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md). 

- Kasutage automaatses tegevuses suvandeid **Inimressursside edastatud** ja **Halduri edastatud**, et kinnitada automaatselt puhkusetaotlused, mida need rollid töötajate nimel esitavad. Automaatsete tegevuste kohta lisateabe saamiseks vt teemat [Kinnitusprotsesside konfigureerimine töövoos](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).

- Kasutage tingimuslikus väljavõttes või automaatses tegevuses suvandit **Puhkuse tüüp**, et kontrollida, kuidas töövoog suunab teatud puhkuse tüübiga taotlusi.

## <a name="see-also"></a>Vt ka

- [Puhkuste ja puudumiste ülevaade](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
