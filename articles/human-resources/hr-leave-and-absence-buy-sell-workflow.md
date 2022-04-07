---
title: Puhkuse ostu- ja- müügitaotluste töövoo loomine
description: Looge puhkuse ostu- ja müügitaotluste töövoog, et hallata puhkuse ostu- ja müügitaotlusi rakenduses Dynamics 365 Human Resources järjepidevalt.
author: twheeloc
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3f200fec48dc6bff2702b962c47cbd6951c5921c
ms.sourcegitcommit: 67c4ed957e43d4d60bb609d93921a0be9619e675
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8509412"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a>Puhkuse ostu- ja- müügitaotluste töövoo loomine


>[!Important]
>Selles teemas märgitud funktsioone saavad kliendid praegu kasutada eraldiseisvas teenuses Dynamics 365 Human Resources. Osa või kõik funktsioonid on saadaval osana Finance'i taristu tulevasest väljalaskest pärast Finance'i versiooni 10.0.26.


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Saate luua töövoo rakenduses Dynamics 365 Human Resources, et järjepidevalt hallata oma puhkuse ostu- ja müügitaotlusi. Töövoog **Puhkuse ostmine ja müümine** võimaldab teil teha järgmist.

- Ülesannete määratlemine
- Määramine, kes peab ülesanded lõpule viima
- Täpsustamine, kes saab taotlusi kinnitada või tagasi lükata

## <a name="create-a-buy-and-sell-leave-request-workflow"></a>Puhkuse ostu- ja- müügitaotluste töövoo loomine

1. Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.

2. Jaotises **Seadistus** valige suvand **Inimressursside töövood**.

3. Valige suvand **Uus** ja seejärel valige **Puhkuse ostu- ja müügitaotlus**. 

4. Kui kuvatakse teateaken **Kas avada see fail?**, valige käsk **Ava** ja logige oma ettevõtte mandaatidega sisse.

5. Kasutage töövoo redaktorit, et luua puhkusetaotluste jaoks töövoog. Lisateavet töövoogudega töötamise kohta vt teemast [Töövoogude loomise ülevaade](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Puhkuse- ja puudumistaotluste töövoo andmeelemendid

Te saate töövoos puhkuse ostu- ja müügitaotluste tingimuslike või automaatsete kinnituste loomiseks kasutada järgmisi andmeelemente.

- **summa**
- **Puhkuse ostmise ja müümise poliitika**
- **Ettevõte**
- **Looja:**
- **Loodud kuupäev ja kellaaeg**
- **Lõppkuupäev**
- **Puhkuse tüüp**
- **Muutja**
- **Muutmise kuupäev ja kellaaeg**
- **Taotluse ID**
- **Alguskuupäev**
- **Olek** 
- **Edastuskuupäev**
- **Esitas**
- **Inimressursside edastatud**
- **Halduri edastatud**
- **Esitatud järgmise isiku nimel**
- **Töötaja**

## <a name="workflow-examples"></a>Töövoo näited

Need näited näitavad, kuidas saate luua erinevat tüüpi töövoo tingimusi, kasutades järgmisi andmeelemente:

- Kasutage automaatses tegevuses suvandeid **Inimressursside edastatud** ja **Halduri edastatud**, et kinnitada automaatselt puhkuse ostu- ja müügitaotlused, mida need rollid töötajate nimel esitavad. Automaatsete tegevuste kohta lisateabe saamiseks vt teemat [Kinnitusprotsesside konfigureerimine töövoos](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).

- Kasutage tingimuslikus väljavõttes või automaatses tegevuses suvandit **Puhkuse tüüp**, et kontrollida, kuidas töövoog suunab teatud puhkuse tüübiga taotlusi.

## <a name="see-also"></a>Vt ka

[Puhkuste ja puudumiste ülevaade](hr-leave-and-absence-overview.md)<br>
[Puhkuse ostu ja müügi poliitikate haldamine](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)<br>
[Puhkuse ostmine ja müümine](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
