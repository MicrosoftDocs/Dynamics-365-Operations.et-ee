---
title: Maksuteenusele ei õnnestunud juurde pääseda
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
ms.openlocfilehash: f4682b83405071b4ad7647958122ab2b4e082133
ms.sourcegitcommit: 2977e92a76211875421e608555311c363cfbdc25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/16/2022
ms.locfileid: "8612312"
---
# <a name="failed-to-access-tax-service"></a>Maksuteenusele ei õnnestunud juurde pääseda

[!include [banner](../includes/banner.md)]


See teema kirjeldab, kuidas parandada maksu arvutamise teenuse tõrget "Maksuteenusele juurdepääs nurjus".

## <a name="symptoms"></a>Sümptomid

Microsoft Dynamics 365 Finances minge maksu **seadistamise** \> **maksu** \> **konfiguratsiooni maksuteenuse** \> **parameetritesse.** **Lubate vahekaardil** Üldine suvandi Luba **maksu arvutamine**. Kui proovite seejärel valida väärtust väljal Funktsiooni **häälestusnimi**, ilmneb tõrge. Tõrketeade: "Maksuteenusele ei pääsenud juurde."

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
