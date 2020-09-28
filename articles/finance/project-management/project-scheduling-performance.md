---
title: Projekti ressursi plaanimise tulemused
description: Selles teemas antakse teavet selle kohta, kuidas parandada suure hulga projektide ressursi planeerimise tulemusi.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760529"
---
# <a name="project-resource-scheduling-performance"></a>Projekti ressursi plaanimise tulemused

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Ressursi planeerimise tulemustega seotud probleemid võivad ilmneda siis, kui projektide arv jõuab tuhandeteni. Ressursi planeerimise tulemuste parandamiseks on saadaval funktsioon, mis võimaldab kasutajatel ressursi kättesaadavuse vormi käivitamiseks kuluvat aega vähendada. See eemaldab ressursi tulemuste kokkuvõtete sünkroonimisprotsessi ja kasutab ressursiotsingu kiirendamiseks tabelit **ResProjectResource**. Pange tähele, et tabelit **ResRollup** enam ei kasutata.

> [!IMPORTANT]
> Kui ressursi tulemuste kokkuvõtete sünkroonimisprotsessist või tabelist **ResProjectResource** on sõltuvus, ärge seda funktsiooni kasutage.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Ressursi ajastamise toimivuse täiustamise lubamine
Ressursi ajastamise toimivuse täiustamise lubamiseks tehke järgmist.

1. Avage **Funktsioonihaldus** > **Kõik** ja otsige funktsioonide loendist üles suvand **Luba projekti ressursi ajastamise toimivuse täiustamise funktsioon**.
2. Valige **Luba kohe**.

> [!NOTE]
> Kui te ei leia funktsiooni loendist, tehke loendi värskendamiseks valik **Otsi värskendusi**.

3. Värskendage oma brauserit ja seejärel avage **Projektihaldus ja -arvestus** > **Perioodilised** > **Projekti ressursid** > **Sünkrooni ressursi kalendrite võimsust kõigis ettevõtetes**.
4. Eelmiste andmete eemaldamiseks seadke suvandi **Eemalda olemasolevad võimsuse kirjed** väärtuseks **Jah**. Kui soovite luua inkrementandmeid, seadke selle väärtuseks **Ei**.
5. Valige väljal **Perioodi kood** periood, mille jooksul tuleks andmed genereerida. Kui valite perioodi koodi, ei pea te algus- ja lõppkuupäeva määratlema.
6. Kui jätate välja **Perioodi kood** tühjaks, valige teabe loomiseks kindlad algus- ja lõppkuupäevad.
7. Valige nupp **OK**.

 > [!NOTE]
 > See jaotab üldandmed tabelisse **ResCalendarCapacity** kõigis teie keskkonna ettevõtetes, seega tuleb pakett-tööd käitada ainult ühes juriidilises isikus. Selle pakett-töö andmeid on vaja ressursi tulemuste arvutamiseks seostuva kalendri kaudu.

8. Avage **Projektihaldus ja -arvestus** > **Perioodilised** > **Projekti ressursid** > **Asusta projekti ressursid kõigis ettevõtetes** ja seejärel valige **OK**. See on üldandmete täiendamise skript tabelites **ResProjectResource**, **ResCalendarDateTimeRange** ja **ResEffectiveDateTimeRange**. Uuendatakse ka välja **PSAPRojSchedRole.RootActivity** väärtusi. Kui seda ei käitata, kuvatakse ressursi ajastamise toimingute käivitamisel hoiatus.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Ressursi ajastamise toimivuse täiustamise väljalülitamine

1. Avage **Funktsioonihaldus** > **Kõik** ja otsige üles suvand **Luba projekti ressursi ajastamise toimivuse täiustamise funktsioon**.
2. Valige funktsioon ja seejärel valige nupp **Keela**.
3. Värskendage oma brauserit.
4. Valige **Projektihaldus ja raamatupidamine** > **Perioodiline** > **Võimsuse sünkroonimine** > **Ressursside võimsuse kokkuvõtete sünkroonimine**.
5. Varasemate andmete eemaldamiseks seadke lehel **Tulemuste kokkuvõtete sünkroonimine** suvandi **Eemalda olemasolevad võimsuse kirjed** väärtuseks **Jah**. Kui soovite luua inkrementandmeid, seadke selle väärtuseks **Ei**.
6. Valige väljal **Perioodi kood** periood, mille jooksul tuleks andmed genereerida. Kui valite perioodi koodi, ei pea te algus- ja lõppkuupäeva määratlema.
7. Kui jätate välja **Perioodi kood** tühjaks, valige teabe loomiseks kindlad algus- ja lõppkuupäevad.
8. Valige nupp **OK**.

> [!NOTE]
> See jaotab üldandmed tabelisse **ResRollup** kõigis teie keskkonna ettevõtetes, seega tuleb pakett-tööd käitada ainult ühes juriidilises isikus. See pakett-töö on vajalik kõigi vaadete **Ressursi kättesaadavus** korral. Kui seda pakett-tööd ei käitata, luuakse **ResRollupi** andmed käigu pealt, mis võib aega võtta.
