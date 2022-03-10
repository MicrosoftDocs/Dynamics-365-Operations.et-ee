---
title: Maksuarvestuse parameetrites on tühi maksufunktsiooni loend.
description: See teema kirjeldab probleemi tõrkeotsingut, kui maksu funktsioonide loend maksu arvutamise parameetrite lehel on tühi.
author: wangchen
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 5b87499042c9c4bfe76e182b170adf4f1cfeac4b
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/05/2022
ms.locfileid: "8389126"
---
# <a name="empty-tax-feature-list-in-tax-calculation-parameters"></a>Maksuarvestuse parameetrites on tühi maksufunktsiooni loend.

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="symptom"></a>Sümptom

Olete avaldanud funktsiooni Regulatiivses konfiguratsiooniteenuses (RCS), et seda Saaks Microsoftis kasutada Dynamics 365 Finance. Kui avate finantsid, **·** \> **·** \> **·** \> **minge maksu seadistamise maksu konfiguratsiooni maksuarvutuse parameetritesse ja proovige valida väärtust väljal Funktsiooni häälestuse** **nimi**, on väärtuste loend tühi.

## <a name="reason"></a>Põhjus

See probleem ilmneb tavaliselt seetõttu, et teie finantskeskkond ja RCS-keskkond pole sama rentniku all.

### <a name="rcs-tenant"></a>RCS-i rentnik

Järgige neid samme, et leida oma RCS-i rentniku ID.

1. Kopeerib täieliku RCS-i URL-i. Näiteks URL võib olla `https://rcs-rts-sf-ed22b5aeea8-int-westus2.configure.global.int.dynamics.com/namespaces/817ff7a0-0d77-4aba-9360-3c9749e2c5de/?cmp=dat&mi=RCSFeatureDomainsWorkspace`.
2. Avage inPrivate-brauseri aken, kleepige RCS-i URL aadressiribale ja valige seejärel sisestusklahv (**Enter**). Teid suunatakse sisselogimislehele, kus on võimalik leida RCS-i rentniku ID. Kui näiteks sisselogimislehe URL on, on `https://login.microsoftonline.com/d335a570-a05b-4bc5-8eb3-c42c65f9560d` rentniku ID teave, mis kuvatakse pärast `https://login.microsoftonline.com/` või **d335a570-a05b-4bc5-8eb3-c42c65f9560d**.

### <a name="finance-environment-tenant-id"></a>Finantskeskkonna rentniku ID

Oma finantskeskkonna rentniku ID leidmiseks järgige samu samme, mida järgisite RCS-i rentniku leidmiseks. Kopeerige ja kleepige finantskeskkonna täielik URL täieliku RCS-i URL-i asemel.

## <a name="resolution"></a>Lahendus

Kui rentnike ID-de kaks erinevust, tuleb teil ette selles teemas kirjeldatud probleemi. Kui need on samad, tekib probleeme, mis pole seotud. Sel juhul on soovitatav võtta ühendust Microsofti toega.

### <a name="solution-1"></a>Lahendus 1

Logige oma RCS-keskkond sisse samale rentnikule, mis teie finantskeskkond on sisse loginud. Seejärel looge ja avaldage maksufunktsioon.

### <a name="solution-2"></a>2. lahendus

Jagage maksufunktsiooni finants rentnikuga RCS-s.

1. Minge RCS-i globaliseerimisfunktsiooni **maksuarvutusse** \> **·**.
2. Valige jagamiseks funktsioon ja seejärel valige vahekaardil **Organisatsioonid suvand Jaga** **.**
3. **Sisestage nimi väljale** Organisatsiooni domeeni nimi. Näiteks sisestage **contoso.onmicrosoft.com**.
4. Valige **Anna ühiskasutusse**.

![Jagage välise organisatsiooni ripploendiga.](media/ShareTaxFeature.png)
