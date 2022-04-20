---
title: Täpsema panga vastavusseviimise importimise häälestus elektroonilise aruandluse abil
description: See teema kirjeldab, kuidas kasutada elektroonilist aruandlust, et seadistada täiustatud panga vastavusseviimise impordiprotsess BAI2-väljavõtete jaoks.
author: panolte
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 39f1d8ba561ab0e36346f1dfb4f70df318c92a37
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544549"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Täpsema panga vastavusseviimise importimise häälestus elektroonilise aruandluse abil

[!include [banner](../includes/banner.md)]

Täpsem panga vastavusseviimise funktsioon võimaldab teil importida elektroonilisi pangaväljavõtteid ja viia need automaatselt vastavusse pangakannetega Microsoft Dynamics 365 finantsis. See teema kirjeldab, kuidas seadistada bai2 pangaväljavõtte impordi funktsioone.

## <a name="set-up-the-electronic-reporting-configuration"></a>Elektroonilise aruandluse konfiguratsiooni seadistamine

1. Minge tööruumide **elektroonilise aruandluse \> juurde**.
2. Microsofti konfiguratsioonipakkuja paanil **valige** hoidlad **·**.
3. Valige **Globaalne** ja seejärel valige **Ava**.
4. Kui tuleb luua ühendus hoidlaga, valige dialoogiaknast sinine link.
5. Konfiguratsiooniloendist otsige pangaväljavõtte **mudeli bai2 \> pangaväljavõtte mudelit**.
6. **Valige BAI2-vorming**.
7. Valige kiirkaardil **Versioonid** uusim versioon ja seejärel käsk **Impordi**.

## <a name="set-up-the-bank-statement-format"></a>Pangaväljavõtte vormingu häälestamine

1. Minge kassa- **ja pangahalduse häälestuse täpsema \>\> panga vastavusseviimise häälestuse pangaväljavõtte \> vormingule**.
2. Valige suvand **Uus**.
3. Seadke väljavõtte **vorming ja** nimeväljad **·**.
4. Märkige ruut **Üldine elektrooniline impordivorming**.
5. Seadke impordivormingu **konfiguratsiooni** väli **BAI2-vormingule**.

## <a name="set-up-the-bank-account"></a>Pangakonto seadistamine

1. Minge jaotisse **Sularaha- ja pangahaldus \> Pangakontod \> Pangakontod**.
2. Avage pangakonto.
3. Seadke vastavusseviimise **kiirkaardil** panga vastavusseviimise **täpsemaks suvandiks** **Jah**.
4. Seadke väljavõtte **vormingu väli** varem loodud **BAI2-vormingule**.

## <a name="import-the-bank-statement"></a>Pangaväljavõtte importimine

1. Avage sularaha- **ja pangahalduse pangaväljavõtte \> vastavusseviimise pangaväljavõtted \>**.
2. Valige pangaväljavõtete **lehe** ülaosas suvand **Impordi väljavõte**.
3. **Seadke väljavõttes** pangakontole väli Pangakonto.
4. Seadke väljavõtte **vormingu väli** varem loodud **BAI2-vormingule**.
5. Valige **sirvimine** ja valige **BAI-fail**.
6. Valige nupp **Laadi üles**.
7. Valitud **faili importimiseks valige OK**.
