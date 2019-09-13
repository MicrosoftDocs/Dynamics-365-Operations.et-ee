---
title: Tõrkeotsingu juhend andmete integreerimiseks
description: See teema annab teavet Microsoft Dynamics 365 for Finance and Operations ja Common Data Service’i vahelise andmete integratsiooni tõrkeotsingu kohta.
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
ms.openlocfilehash: 5e71729dafd2ad85a01b055363d1c7056b5558b2
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873101"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Tõrkeotsingu juhend andmete integreerimiseks

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a>Lubage Common Data Service’i lisandmooduli jälituslogid ja kontrollige topeltkirjutamise lisandmooduli vea andmeid

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Kui kogete topeltkirjutamise sünkroniseerimisel probleemi või viga, järgige jälituslogi vigade kontrollimiseks neid etappe.

1. Enne vigade kontrollimist peate lubama lisandmooduli jälituslogid. Juhised leiate [õpetuse: lisandmooduli kirjutamine ja registreerimine](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) jaotisest „Jälituslogide vaatamine“.

    Nüüd võite vigu kontrollida.

2. Logige sisse rakendusse Microsoft Dynamics 365 for Sales.
3. Valige nupp **Sätted** (hammasratas) ja seejärel suvand **Täpsemad sätted**.
4. Menüüs **Sätted** valige **Kohandamine\> lisandmooduli jälituslogi**.
5. Vigade üksikasjade nägemiseks valige tüübi nimeks **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.

## <a name="inspect-dual-write-synchronization-errors-in-finance-and-operations"></a>Kontrollige Finance and Operationsi topeltkirjutamise sünkroonimise vigu

Järgige neid juhiseid, et kontrollida testimise ajal vigu.

1. Microsoft Dynamics Lifecycle Services’i (LCS) sisselogimine.
2. Avage LCS projekt, mille topeltkirjutamist testida.
3. Valige **Pilve majutatud keskkonnad**.
4. Looge kaugtöölaua ühendus Dynamics 365 for Finance and Operationsi virtuaalarvutiga (VM), kasutage selleks LCS-is näidatavat kohalikku kontot.
5. Avage sündmusevaatur. 
6. Minge **Rakenduste ja teenuste logid \> Microsoft \> Dynamics \> AX-DualWriteSync \> Toiming**. Näidatakse tõrkeid ja üksikasju.

## <a name="unlink-one-common-data-service-environment-from-finance-and-operations-and-link-another-environment"></a>Linkige lahti üks Common Data Service’i keskkond rakendusest Finance and Operations ja linkige teine keskkond

Linkide värskendamiseks tehke järgmist.

1. Minge Finance and Operationsi keskkonda.
2. Avage andmehaldus.
3. Valige **CDS rakenduste jaoks link**.
4. Valige kõik töötavad vastendused ja seejärel valige **Peata**
5. Valige kõik töötavad vastendused ja seejärel valige nuppu **Kustuta**.

    > [!NOTE]
    > Suvand **Kustuta** pole saadaval, kui mall **CustomerV3-Account** on valitud. Vajadusel tühjendage selle malli valik. **CustomerV3-Account** on vanem ettevalmistatud mall ja töötab raha väljavaate lahendusega. Kuna see on välja antud ülemaailmselt, näidatakse seda kõigi mallide puhul.

6. Valige nupp **Tühista keskkonna link**.
7. Toimingu kinnitamiseks valige **Jah**.
8. Uue keskkonna linkimiseks järgige [installimise juhendis](https://aka.ms/dualwrite-docs) olevaid juhiseid.
