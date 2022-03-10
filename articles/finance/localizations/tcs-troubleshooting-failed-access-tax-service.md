---
title: Maksuteenusele <a0/& juurdepääs nurjus.
description: See teema kirjeldab, kuidas sooritada maksuarvutuse teenuse tõrke tõrkeotsingut.
author: hangwan
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 02/16/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 48a75cd0c1d91c3b3d9c3fb2e6cab93a76756532
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/05/2022
ms.locfileid: "8389123"
---
# <a name="failed-to-access-tax-service"></a>Maksuteenusele <a0/& juurdepääs nurjus.

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

See teema kirjeldab, kuidas parandada maksu arvutamise teenuse tõrget "Maksuteenusele juurdepääs nurjus".

## <a name="symptoms"></a>Sümptomid

Microsoftis Dynamics 365 Finance minge maksu seadistamise **maksu** \> **konfiguratsiooni** \> **maksu** \> **teenuse parameetritesse.** **Lubate vahekaardil** Üldine suvandi Luba **maksu arvutamine**. Kui proovite seejärel valida väärtust väljal Funktsiooni **häälestusnimi**, ilmneb tõrge. Tõrketeade: "Maksuteenusele ei pääsenud juurde."

## <a name="cause"></a>Põhjus

See tõrge ilmneb, kuna finantsid ei pääse maksuarvutuse teenusele juurde.

## <a name="resolution"></a>Lahendus 

1. Microsoft Dynamics Lifecycle Services’i (LCS) sisselogimine.
2. **Leidke keskkonnalehe** vahekaardil Keskkonna **lisandmoodulid maksuarvutuse** kaup **ja** vaadake selle olek üle. Olek peab olema Installimine **või** Installitud **·**. Kui maksuarvutusteenuse lisandmoodulit pole installitud, kuvatakse tõrketeade.

## <a name="mitigation"></a>Vähendamine

1. Valige LCS-i **lehel Finantsid** Power **Platformi integreerimise** jaotises **suvand Installi uus lisandmoodul**.
2. Kerige lehe allserva ja valige **installimiseks** maksuarvutuse lisandmoodul.
3. Naage tagasi oma finantskeskkonda ja proovige pääseda juurde maksuarvutuse teenusele.

> [!NOTE]
> Enne maksuarvutusteenuse installimist vaadake üle maksu arvutamise [teenuse eeltingimused](global-get-started-with-tax-calculation-service.md#prerequisites).
> 
> Kui te ei saa lisandmoodulit installida, kuna **Power Platformi** integreerimisjaos ei ole saadaval, vaadake [lisandmooduli ülevaadet](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Kui pärast lisandmooduli installimist ilmneb tõrge, võtke ühendust oma süsteemiadministraatoriga.
