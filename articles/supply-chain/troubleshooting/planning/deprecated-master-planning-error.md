---
title: Sisseehitatud üldplaneerimise mootori käivitamisel kuvatakse tõrge
description: Aegunud sisseehitatud üldplaneeringu mootori käivitamisel kuvatakse tõrketeade.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7c0c674818a21d3ad422661fc427b0b9c4aad52b8d44d08791d2d703be528fe3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751717"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a>Sisseehitatud üldplaneerimise mootori käivitamisel kuvatakse tõrge

Tõrkekood: ReqCalcScheduleItemTablePlanningOptimizationFitError

## <a name="symptoms"></a>Sümptomid

Kui käivitate üldplaneeringu kasutades vananenud sisseehitatud üldplaneeringu mootorit, kuvatakse järgmine tõrketeade:

> See tõrketeade kuvatakse, sest sisseehitatud koondplaneerimise mootorit kasutati selleks, et optimeerida stsenaariumeid, mida toetab planeerimise optimeerimine. Peaksite kohe planeerimise optimeerimisele üle minema, sest praegune sisseehitatud koondplaneerimine on iganenud. Arvestage, et see koondplaneerimise käivitamine viidi siiski edukalt lõpule. Juhul, kui üleminek sõltub suuresti ootel funktsioonidest, saate taotleda sisseehitatud koondplaneerimise mootori jätkuva kasutuse erandit. Alustamiseks täitke järgmine küsimustik ja vajaduse korral paluge erandit planeerimise optimeerimisele üleminekul. [Optimeerimise migreerimise plaanimine ja erandi küsimustik](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a>Põhjus

Kui käivitate planeerimise ja ei kasuta tootmise juhtimise funktsioone, peaksite kaaluma migreerimist plaanimise optimeerimisele. Integreeritud koondplaneerimise mootor on aegunud. Seetõttu peate selle kasutamise soovimisel paluma Microsoftilt teile erand teha.

## <a name="resolution"></a>Lahendus

Lisateavet plaanimise optimeerimisele migreerimise kohta või erandi rakendamiseks, nii et saate kasutada selle asemel aegunud integreeritud plaanimismootorit, vaadake jaotisest [Plaanimise optimeerimisele migreerimine koondplaneerimiseks](/dynamics365/supply-chain/master-planning/new-master-planning-engine).
