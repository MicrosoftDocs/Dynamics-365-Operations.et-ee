---
title: Mõõtühiku teisendus tootevariandi kohta
description: See teema kirjeldab, kuidas seadistada tootevariantide mõõtühikute teisendusi. See sisaldab seadistuse näidet.
author: johanhoffmann
manager: tfehr
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 71d35d47a703f0931ba3b4ab5df21c7199c7ea5b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426546"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a>Mõõtühiku teisendus tootevariandi kohta

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas seadistada erinevaid tootevariantide mõõtühikute teisendusi.

Selle asemel, et luua mitut haldamist vajavat individuaalset toodet, saate kasutada tootevariante ühe toote variatsioonide loomiseks. Näiteks võib tootevariant olla antud suuruse ja värviga t-särk.

Varasemalt sai ühiku teisendusi seadistada ainult tooteetalonil. Seetõttu olid kõigil tootevariantisel samad ühikuteisenduse reeglid. Kui aga funktsioon *Tootevariantide mõõtühiku teisendused* on sisse lülitatud, kui müüte t-särke kastides ja ühte kasti pakendatavate t-särkide kogus sõltub t-särgi suurusest, saate nüüd seadistada ühikuteisendusi erinevate särgisuuruste ja pakendamiseks kasutatavate kastide vahel.

## <a name="turn-on-the-feature-in-your-system"></a>Funktsiooni sisselülitamine teie süsteemis

Kui seda funktsiooni veel ei kuvata teie süsteemis, avage [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja lülitage sisse funktsioon *Tootevariantide mõõtühiku teisendused*.

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a>Seadistage toode ühiku teisaldamiseks varjandi kohta

Tootevariante saab luua ainult toodetele, mis on tooteetalonid. Lisateavet vt jaotisest [Tooteetaloni loomine](tasks/create-product-master.md). Funktsioon *Tootevariantide mõõtühiku teisendused* ei ole saadaval toodete puhul, millel on seadistatud tegeliku kaalu protsessid.

Tooteetaloni konfigureerimiseks, et toetada ühikuteisendust ühe variandi kohta, toimige järgmiselt.

1. Avage **Tooteteabe haldus \> Tooted \> Tooteetalonid**.
1. Looge või avage tooteetalon, et avada selle leht **Toote üksikasjad**.
1. Määrake suvandi **Luba mõõtühiku teisendused** Väärtuseks *Jah*.
1. Tehke Toimingupaani vahekaardil **Toode** grupis **Häälesta** valik **Ühiku teisendused**.
1. Avaneb leht **Ühiku teisendused**. Valige üks järgmistest vahekaartidest.

    - **Klassisisesed teisendused** – valige see vahekaart, et teisendada samasse ühiku klassi kuuluvaid ühikuid.
    - **Klassivahelised teisendused** – valige see vahekaart, et teisendada erinevatesse ühiku klassidesse kuuluvaid ühikuid.

1. Uue ühiku teisenduse lisamiseks valige **Uus**.
1. Määrake väljale **Loo teisendus:** üks järgmistest väärtustest.

    - **Toode** – selle väärtuse valimisel saate seadistada ühiku teisenduse tooteetaloni jaoks. Seda ühiku teisendust kasutatakse varuvariandina kõigi tootevariantide puhul, millele pole ühiku teisendust määratletud.
    - **Tootevariant** – selle väärtuse valimisel saate seadistada ühiku teisenduse kindla tootevariandi jaoks. Variandi valimiseks kasutage välja **Tootevariant**.

    ![![Uue ühiku teisenduse lisamine](media/uom-new-conversion.png "Uue ühiku teisenduse lisamine")](media/uom-new-conversion.png "Adding a new unit conversion")

1. Ühiku teisenduse seadistamiseks kasutage teisi saadaolevaid välju.
1. Uue ühiku teisenduse salvestamiseks valige **OK**.

> [!TIP]
> Toote või tootevariandi lehe **Ühiku teisendused** saate avada mis tahes järgmistelt lehtedelt.
> 
> - Toote üksikasjad
> - Väljastatud toodete üksikasjad
> - Väljastatud tootevariandid

## <a name="example-scenario"></a>Näidisstsenaarium

Selles stsenaariumis müüb ettevõte t-särke suuruses S, M, L ja XL. T-särk määratletakse tootena ja erinevad suurused määratletakse selle toote variantidena. Särke pakendatakse kastidesse. Suuruste S, M ja L, saab ühte kasti pakendada viis särki. Kuid suuruse XL puhul on ühes kastis ruumi ainult nelja särgi jaoks.

Ettevõte soovib jälgida t-särkide erinevaid variante ühiku *Tükid* järgi, aga müüb t-särke ühikus *Kastid*. Suuruste S, M ja L puhul on lao- ja müügiüksuse vaheliseks teisenduseks 1 kast = 5 tükki. Suuruse XL puhul on teisenduseks 1 kast = 4 tükki.

1. Avage toote **T-särk** lehel **Väljastatut toote üksikasjad** leht **Ühiku teisendused**.
1. Seadistage lehel **Ühiku teisendused** väljastatud tootevariandi **XL** jaoks järgmine ühiku teisendus.

    | Field                 | Sätted                 |
    |-----------------------|-------------------------|
    | Loo teisendus: | Tootevariant         |
    | Tootevariant       | T-särk : : XL : : |
    | Lähteühik             | Kastid                   |
    | Tegur                | 4                       |
    | Ühikuks               | Osad                  |

1. Kuna väljastatud toodete variantidel **S**, **M** ja **L** on ühikute *Kast* ja *Tükid* vahel sama ühiku teisendus, saate nende tootevariantide ühiku teisendused määratleda tooteetalonis.

    | Field                 | Sätted |
    |-----------------------|---------|
    | Loo teisendus: | Toode |
    | Toode               | T-särk |
    | Lähteühik             | Kastid   |
    | Tegur                | 5       |
    | Ühikuks               | Osad  |

## <a name="using-excel-to-update-the-unit-conversions"></a>Exceli kasutamine ühikuteisenduste värskendamiseks

Kui tootel on palju erinevate ühiku teisendustega tootevariante, oleks hea eksportida ühiku teisendused Microsoft Exceli töövihikusse, värskendada need ja seejärel avaldada Dynamics 365 Supply Chain Managementis uuesti.

Ühiku teisenduste eksportimiseks Excelisse Toimingupaani lehe **Ühiku teisendused** kaudu, valige **Ava Microsoft Office'is**.

## <a name="additional-resources"></a>Lisaressursid

[Mõõtühiku haldamine](tasks/manage-unit-measure.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]