---
title: Sugu andmebaasi enum laiendatavus
description: See artikkel annab ülevaate sugu aluse loetelu (enum) laiendatavusest.
author: twheeloc
ms.date: 05/23/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom:
- "51941"
- intro-internal
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61a80c16d24d8fda264340d79ed393db3f635908
ms.sourcegitcommit: 1717ff6af1879c6f3a8360936c42ecf55f86acd0
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/07/2022
ms.locfileid: "9749299"
---
# <a name="gender-base-enum-extensibility"></a>Sugu andmebaasi enum laiendatavus

Sooline **loetelu** (enum) on nüüd laiendatav. See artikkel kirjeldab muudatusi, mida peate koodi aluses tegema, kui plaanite sugu enum **laiendada**.

## <a name="gender-vs-hcmpersongender"></a>Sugu vs HcmPersonGender

Sugumisväärtustel on kaks enummist:

- **Sugu** (rakendusplatvorm)
- **HcmPersonGender** (PersonalManagement)

Sugumise **enum** on kasutusel kogu Microsoft Dynamics 365 Finantsis, **samas kui HcmPersonGender** on omane inimkapitali juhtimise (HCM) funktsioonile. Kui kasutate HCM-i funktsioone **ja** teete mis tahes muudatusi Sugu enum, **peaksite tegema samu muudatusi ka HcmPersonGenderis**. Näiteks kui lisate **Transgenderi** **sugu** enum loendisse, **lisage Transgender** **ka HcmPersonGender** enum’ile.

## <a name="hcmpersongendertranformutil-class"></a>HcmPersonGenderTranformUtil (klass)

Loodi uus **klass HcmPersonGenderTranformUtil**, et lubada tõlget kahe baas-enumeraümbrise vahel. Selles klassis on kaks meetodit: **convertGenderToHcmPersonGender** ja **convertHcmPersonGenderToGender**. Peaksite looma laiendi, kasutades **·** **käsuklassi** või sündmuseohjureid, ja laiendama mõlemat meetodit, et vastendada uusi väärtusi, mis on lisatud kas baasloendisse.

## <a name="payrollstatewagetaxprepdp-class"></a>PayrollStateWageTaxPrepDP (klass)

**PayrollStateWageTaxPrepDP** **on palga osariigi palgamaksu eelp** SQL Serveri aruandlusteenuste (SSRS) aruande andmepakkuja klass. USA jaoks on saadaval kolm väärtust:Plaanimine, Emane **ja** Määramata **.** **·** Meetodis **populatePayrollStateWageTaxPrepTmp** on lülituse väljavõte, **mida kasutatakse HcmPersonGender** enum väärtuse vastendamiseks ühega kolmest väljast: **IsMale**, **IsFemale** **või IsUnspecifiedGender**. Switch-lause vaikeväärtus on **IsUnspecifiedGender**. **Kui lisate HcmPersonGenderi** loendisse mis tahes väärtusi teisiti vastendamiseks, peate looma laiendi, **·** **kasutades käsuahela klassi populatePayrollStateWageTaxPrepTmp** meetodi kaudu, et väärtust vajaduse järgi muuta.

## <a name="smmoutlooksync_contact-class"></a>smmOutlookSync_Contact (klass)

Integreerimisklass **smmOutlookSync_Contact** väärtused Outlooki ja kontaktisikute **vahel** ja sealt **välja**. **Outlook** toetab kolme väärtust: **Failid**, **emased** **ja määramata**. Klassil on kaks meetodit, mis aitavad teil vastendada **sugusid** **OutlookGendersiga**. Vaikemeetod on **NonSpecific/UnSpecified**. Kui loote lisaväärtused sugu **enum**, peaksite looma laiendi, **kasutades** käsurea klassi mõlema meetodi ja kaardi vastavalt vajadusele.
