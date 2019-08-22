---
title: Tõrkeotsingu juhend andmete integreerimiseks
description: See teema pakub tõrkeotsingu teavet andmete integreerimise kohta rakenduste Microsoft Dynamics 365 for Finance and Operations ja Common Data Service vahel.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797271"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Tõrkeotsingu juhend andmete integreerimiseks

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a>Lülitage sisse lisandmoodulite jälgimine rakenduses Common Data Service ja kontrollige topeltkirjutamise lisandmooduli vea üksikasju.

Kui teil esineb probleem või tõrge topeltkirjutamise sünkroonimisega, saate kontrollida vigu jälituslogis.

1. Enne kui saate vigu kontrollida, peate lubama lisandmooduli jälgimise, kasutades juhiseid teemas [Lisandmooduli registreerimine](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) lisandmooduli jälgimise lubamiseks. Nüüd saate tõrkeid kontrollida.
2. Dynamics 365 for Sales-sse sisselogimine
3. Klõpsake ikoonil Sätted (käik) ja valige **Täpsemad sätted**.
4. Menüüs **Sätted** valige **Kohandamine > Lisandmooduli jälituslogi**.
5. Klõpsake tüübi nimetus **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**, et kuvada tõrke üksikasjad.

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a>Topeltkirjutamise sünkroonimise tõrgete kontrollimine rakenduses Finance and Operations

Tõrgete kontrollimiseks testimisel toimige järgmiselt.

+ Logige sisse teenusesse Lifecycle Services (LCS).
+ Avage LCS-i projekt, mille valisite topeltkirjutamise testimiseks.
+ Avage Pilve majutatud keskkonnad.
+ Kaugtöölaud Finance and Operations VM, kasutades kohalikku kontot, mis kuvatakse LCS-is.
+ Aruandevaaturi avamine 
+ Liikuge **Rakenduste ja teenuste logid > Microsoft > Dynamics > AX-DualWriteSync > Toiming**. Kuvatakse tõrked ja üksikasjad.

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a>Kuidas linkida ja lahti linkida teise Common Data Service’i keskkond rekandusest Finance and Operations.

Saate värskendada linke, järgides neid samme.

+ Liikuge Finance and Operationsi keskkonda.
+ Avage andmehaldus.
+ Klõpsake **Lingi CDS rakenduste jaoks**.
+ Valige kõik töötavad vastendused ja klõpsake nuppu **Peata**. 
+ Valige kõik töötavad vastendused ja klõpsake nuppu **Kustuta**.

    > [!NOTE]
    > Suvandit **Kustuta** ei kuvata, kui mall **CustomerV3-Account** on valitud. Vajaduse korral tühistage see valik. **CustomerV3-Account** on vanem ettevalmistatud mall ja töötab raha väljavaate lahendusega. Kuna see on välja antud ülemaailmselt, kuvatakse see kõigi mallide puhul.

+ Klõpsake nuppu **Tühista keskkonna link**.
+ Kinnitamiseks klõpsake **Jah**.
+ Uue keskkonna linkimiseks järgige [installimise juhendis](https://aka.ms/dualwrite-docs) olevaid juhiseid.

