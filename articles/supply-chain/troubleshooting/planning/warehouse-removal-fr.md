---
title: Prognoosiridadelt ei saa laojõudluse prognoosi mõõdet eemaldada
description: Prognoosiridadelt ei saa laojõudluse prognoosi mõõdet eemaldada.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026442"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a>Prognoosiridadelt ei saa laojõudluse prognoosi mõõdet eemaldada

KB number: 4614408

## <a name="symptoms"></a>Sümptomid

See probleem ilmneb, kui **Varude** dimensioon ei ole määratud vahekaardi **Prognoosi dimensioonid** **Nõudluse prognoosimise parameetri** lehel. Sellest hoolimata kuvatakse **Lao** veerg **Nõudluse prognoosi** lehel (**Koondplaneerimise \> Prognoosimine \> Käsitsi prognoosi üksus \> Nõudluse prognoosi read**).

## <a name="resolution"></a>Eraldusvõime

Sätted **Prognoosi dimensioonid** vahekaardil **Nõudluse prognoosimise parameetri** lehel ei mõjuta **Nõudluse prognoosi** lehte. Need kontrollivad alusprognoosi, mis luuakse ja näidatakse korrigeeritud nõudluse prognoosis. Kuid need ei kontrolli siiski "reaal"-nõudluse prognoosi jaoks nõutavaid dimensioone. Muutes kirjeid, mis on kuvatud **Korrigeeritud nõudluse prognoosi** lehel, saate need teisendada prognoosimudeli "reaal"-prognoosi kirjeteks. Seejärel saab seda mudelit kasutada koondplaneerimisel.

**Nõudluse prognoosi** lehel, "reaalse" prognoosi dimensioonid, mis kuvatakse nõudluse prognoosiridadel, on varude dimensioonide osa. (Selline käitumine sarnaneb müügitellimuse ridade käitumisega.) Kui teie süsteem ei ole seadistatud kasutama **Ladu** kohustusliku varude dimensioonina, saate lehte veeru peitmiseks kohandada.
