---
title: Seadista ja loo elektroonilise aruandluse abil positiivsed maksefailid
description: See teema kirjeldab, kuidas seadistada positiivset makset elektroonilise aruandluse abil.
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 43dd1a9cba1fe8df5cff26fe76af7e2957a0d6a4
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544540"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Seadistage elektroonilise aruandluse abil positiivsed maksefailid

Positiivse makse seadistamine pangale edastatava elektroonilise tšekkide loendi loomiseks. Tšeki esitamisel pangale võrdleb pank seda tšekkide loendiga. Kui tšekk vastab loendis olevale tšekile, maksab pank selle välja. Kui tšekk ei vasta ühelegi loendis olevale tšekile, võtab pank selle ülevaatamiseks enda kätte.

## <a name="set-up-the-electronic-reporting-configuration"></a>Elektroonilise aruandluse konfiguratsiooni seadistamine

1. Minge tööruumide **elektroonilise aruandluse \> juurde**.
2. Microsofti konfiguratsioonipakkuja paanil **valige** hoidlad **·**.
3. Valige **Globaalne** ja seejärel valige **Ava**.
4. Kui tuleb luua ühendus hoidlaga, valige dialoogiaknast sinine link.
5. Leidke ja valige konfiguratsiooniloendist Positiivne **maksemudel Positiivne \> maksevorming**.
6. Valige kiirkaardil **Versioonid** uusim versioon ja seejärel käsk **Impordi**.

## <a name="set-up-a-positive-pay-format"></a>Positiivse maksevormingu seadistamine

1. Avage sularaha- **ja pangahalduse seadistuse positiivse \> makse \> vormingud**.
2. Valige suvand **Uus**.
3. Seadistage **maksevorming** ja kirjelduse **väljad**.
4. Märkige ruut **Üldine elektrooniline ekspordivorming**.
5. Seadke konfiguratsioonivälja **Ekspordivorming** väärtuseks Positiivne **maksevorming**.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Määrake pangakontole positiivne maksevorming.

1. Minge sularaha **- ja pangahalduse pankade \> pangakontodele \>**.
2. Avage pangakonto.
3. Seadke kiirkaardil **Üldine** positiivse makse **vormingu väli** varem loodud vormingusse.
4. Seadke välja **Positiivse makse alguskuupäev** praegusele kuupäevale.

## <a name="generate-a-positive-pay-file"></a>Loo positiivne maksefail

1. Avage sularaha **- ja pangahalduse \> pangakontod \>**.
2. Avage pangakonto, mille jaoks on seadistatud positiivne makse.
3. Valige halda **maksete positiivse \> makse positiivse \> makse faili**.
4. Seadke välja **katkestamise** kuupäev. Kaasatakse enne seda kuupäeva loodud tšekid.

Tulemuseks saadav XML-fail laaditakse alla.
