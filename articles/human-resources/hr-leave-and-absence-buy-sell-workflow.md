---
title: Puhkuse ostu- ja- müügitaotluste töövoo loomine
description: Looge puhkuse ostu- ja müügitaotluste töövoog, et hallata puhkuse ostu- ja müügitaotlusi rakenduses Dynamics 365 Human Resources järjepidevalt.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d490e0c36ea0e854c5d7afc5b3bf75f6b65e542c
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712586"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a>Puhkuse ostu- ja- müügitaotluste töövoo loomine

Saate luua töövoo rakenduses Dynamics 365 Human Resources, et järjepidevalt hallata oma puhkuse ostu- ja müügitaotlusi. Töövoog **Puhkuse ostmine ja müümine** võimaldab teil teha järgmist.

- Ülesannete määratlemine
- Määramine, kes peab ülesanded lõpule viima
- Täpsustamine, kes saab taotlusi kinnitada või tagasi lükata

## <a name="create-a-buy-and-sell-leave-request-workflow"></a>Puhkuse ostu- ja- müügitaotluste töövoo loomine

1. Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.

2. Jaotises **Seadistus** valige suvand**Inimressursside töövood**.

3. Valige suvand **Uus** ja seejärel valige **Puhkuse ostu- ja müügitaotlus**. 

4. Kui kuvatakse teateaken **Kas avada see fail?**, valige käsk **Ava** ja logige oma ettevõtte mandaatidega sisse.

5. Kasutage töövoo redaktorit, et luua puhkusetaotluste jaoks töövoog. Lisateavet töövoogudega töötamise kohta vt teemast [Töövoogude loomise ülevaade](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)

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

- Kasutage automaatses tegevuses suvandeid **Inimressursside edastatud** ja **Halduri edastatud**, et kinnitada automaatselt puhkuse ostu- ja müügitaotlused, mida need rollid töötajate nimel esitavad. Automaatsete tegevuste kohta lisateabe saamiseks vt teemat [Kinnitusprotsesside konfigureerimine töövoos](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).

- Kasutage tingimuslikus väljavõttes või automaatses tegevuses suvandit **Puhkuse tüüp**, et kontrollida, kuidas töövoog suunab teatud puhkuse tüübiga taotlusi.

## <a name="see-also"></a>Vt ka

[Puhkuste ja puudumiste ülevaade](hr-leave-and-absence-overview.md)<br>
[Puhkuse ostu ja müügi poliitikate haldamine](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)

