---
title: Pearaamatu seadistuses kontole tasumisele postitamine pole sisse lülitatud
description: Probleem ilmneb siis, kui ostutellimust arveldatakse olukorras, kus suvandi "Sisesta pearaamatu kulude kontole" väärtuseks on seatud Jah vahekaardil "Arve", mis asub lehel "Ostureskontro parameetrid"
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 592444958dad4624fdc9098dc58df0a2e49e63de
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476140"
---
# <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>Pearaamatu seadistuses kontole tasumisele postitamine pole sisse lülitatud

## <a name="symptoms"></a>Sümptomid

Probleem ilmneb siis, kui ostutellimust arveldatakse olukorras, kus suvandi **Sisesta pearaamatu kulude kontole** väärtuseks on seatud *Jah* vahekaardil **Arve**, mis asub lehel **Ostureskontro parameetrid**.

## <a name="reproduce-the-issue"></a>Probleemi taastekitamine

Järgmine protsess näitab üht viisi probleemi taastekitamiseks.

1. Avage **Ostureskontro \> Seadistus \> Ostureskontro parameetrid**.
1. Seadke vahekaardil **Arve** suvandi **Sisesta pearaamatu kulude kontole** väärtuseks *Jah*.
1. Avage **Varude haldus \> Seadistus \> Sisestus \> Sisestus**.
1. Tehke kindlaks, et te olete vahekaardil **Ostutellimus** kõik toote ostukulu read kustutanud.
1. Avage jaotis **Ostureskontro \> Ostutellimused \> Kõik ostutellimused**.
1. Looge ostutellimus. Valige väljal **Hankija konto** suvand *1001 Acme Office Supplies*.
1. Lisage järgmiste sätetega ostutellimuse rida.

    - **Kauba kood:** *D0011 Laser Projector*
    - **Koht:** *1*
    - **Ladu:** *11*
    - **Kogus:** *4*

1. Valige toimingupaanil vahekaardi **Ostmine** grupis **Tegevus** suvand **Kinnita**.
1. Tehke toimingupaani vahekaardil **Vastuvõtmine** grupis **Loo** valik **Toote sissetulek**.
1. Sisestage dialoogiboksis **Toote sissetuleku sisestamine** väljale **Toote sissetulek** suvaline number ja seejärel valige **OK**.
1. Valige toimingupaani vahekaardil **Arve** grupis **Loo** suvand **Arve**.
1. Sisestage väljale **Number** arve numbrina suvaline arv.
1. Värskendage vastavusseviimise olekut ja sisestage.
1. Pange tähele, et te saate nüüd ostutellimuse põhjal arvet luues järgmise tõrke: „Toote ostukulu kandetüübi kontonumbrit pole olemas”.

## <a name="resolution"></a>Lahendus

See sõltub arvete ja arvegruppide parameetrite seadistusest. Lisateavet leiate ajaveebipostitusest [Raamatupidamine ostukulu ja varude muudatuste puhul](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).
