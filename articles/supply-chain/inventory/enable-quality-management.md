---
title: Kvaliteedi ja mittevastavuse haldamise lubamine
description: See teema annab ülevaate protsessist kvaliteedi ja mittevastavuse haldus funktsioonide seadistamiseks ja konfigureerimiseks Microsoftis Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d5da648e31d07d054246f5d308a6c6cdeb506c
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956250"
---
# <a name="enable-quality-and-nonconformance-management"></a>Kvaliteedi ja mittevastavuse haldamise lubamine

[!include [banner](../includes/banner.md)]

See teema annab ülevaate protsessist kvaliteedi ja mittevastavuse haldus funktsioonide seadistamiseks ja konfigureerimiseks Microsoftis Dynamics 365 Supply Chain Management.

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a>Kvaliteedi ja mittevastavuse haldamise lubamine

Järgige neid samme, et lubada kvaliteedijuhtimine oma süsteemis.

1. Avage **Varude haldus \> Seadistus \> Varude ja laohalduse parameetrid**.
1. Seadke vahekaardil **Kvaliteedijuhtimine** suvandi **Kasuta kvaliteedijuhtimist** väärtuseks *Jah*.
1. Sisestage väljale **Tunnimäär** tunnitasu kohalikus valuutas. Tunnimäära kasutatakse mittevastavusega seotud toimingute kulude arvutamiseks. Tunnimäär ja arvutatud kulud annavad viiteteavet mittevastavuse kohta. Need ei mõjuta teisi funktsioone.
1. Valige **Aruande seadistamine**.
1. Lisage erinevatele aruande tüüpidele uued read ja valige dokumenditüüp, mida igas aruandes kasutada.
1. Sulgege leht.
1. Sulgege leht.

## <a name="quality-management-configuration-process"></a>Kvaliteedijuhtimise konfigureerimisprotsess

Enne kui saate alustada kvaliteedijuhtimise funktsioonide kasutamist ja luua kvaliteettellimusi, peate konfigureerima süsteemi ja selle eeltingimusi. Siin on nimekiri sammudest, mis on vajalikud kvaliteedijuhtimise konfigureerimiseks.

1. [Kvaliteedi ja mittevastavuse haldamise lubamine](#enable-qm).
1. Valikuline: [Testvahendite konfigureerimine](quality-test-instruments.md).
1. [Testide konfigureerimine](quality-tests.md).
1. [Konfigureerige testi muutujad ja tulemused](quality-test-variables.md).
1. [Konfigureerige testgrupid](quality-test-groups.md).
1. Valikuline: [konfigureerige kvaliteedigrupid ja linkige toodetega](quality-groups.md).
1. Valikuline: [konfigureerige kvaliteediseosed](quality-associations.md).

Kui konfiguratsioon on lõpule viidud, saate alustada kvaliteettellimuste loomisest ja töötlemisest. Lisateavet kvaliteeditellimuste loomise ja kasutamise kohta leiate teemast [Kvaliteeditellimused](quality-orders.md).

## <a name="nonconformance-management-configuration-process"></a>Mittevastavuse halduse konfigureerimisprotsess

Enne kui saate alustada mittevastavuse halduse funktsioonide kasutamist ja luua mittevastavusi, peate konfigureerima süsteemi ja selle eeltingimusi. Siin on nimekiri sammudest, mis on vajalikud mittevastavuste halduse konfigureerimiseks.

1. [Kvaliteedi ja mittevastavuse haldamise lubamine](#enable-qm).
1. [Mittevastavuste kinnitamise eest vastutavad töötajate konfigureerimine](quality-responsible-workers.md).
1. [Konfigureerige probleemi tüübid](quality-problem-types.md).
1. [Saate konfigureerida vahelao tsoone](quality-quarantine-zones.md).
1. [Diagnostikatüüpide konfigureerimine](quality-diagnostic-types.md).
1. [Operatsioonide konfigureerimine](quality-operations.md).
1. Valikuline: [konfigureerige kvaliteeditasusid](quality-charges.md).

Kui konfiguratsioon on lõpule viidud, saate alustada mittevastavuste loomise ja töötlemisega. Lisateavet lehel mittevastavuste loomise ja nendega töötamise kohta leiate teemast [Mittevastavuste loomine ja töötlemine](tasks/create-process-non-conformance.md).

## <a name="additional-resources"></a>Lisaressursid

- [Kvaliteedijuhtimise ülevaade](quality-management-processes.md)
- [Kvaliteedi ja mittevastavuse haldamise lubamine](enable-quality-management.md)
- [Laoprotsesside kvaliteedijuhtimine](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
