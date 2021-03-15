---
title: Eraldiste töötlemine
description: Selles artiklis antakse teavet eraldamiste kohta, nende töötlemise võimaluste kohta Microsoft Dynamics 365 Financeis ja nende kasutamise kohta eelarve planeerimisel. Eraldamisi kasutatakse summade jaotamiseks mitme pearaamatukonto kombinatsiooni lõikes. Need aitavad tagada seda, et raamatupidamises esitatakse kulud või tulud õigele objektile.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a715fe2ae0cb32e523248ffb15bdde4b36bd01d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990210"
---
# <a name="process-allocations"></a>Eraldiste töötlemine

[!include [banner](../includes/banner.md)]

Selles artiklis antakse teavet eraldamiste kohta, nende töötlemise võimaluste kohta is ja nende kasutamise kohta eelarve planeerimisel. Eraldamisi kasutatakse summade jaotamiseks mitme pearaamatukonto kombinatsiooni lõikes. Need aitavad tagada seda, et raamatupidamises esitatakse kulud või tulud õigele objektile.

Seda protsessi toetavad järgmised võimalused:

-   Kandesummade käsitsi eraldamine, kasutades arvestuse jaotustes tükeldamise toimingut või rakendades dokumendile finantsdimensiooni vaikemalle. Lisateavet vt [Arvestuse jaotused](../accounts-payable/accounting-distributions.md).
-   Saate eraldada automaatselt kandesummasid eraldi põhikontol määratletud eraldustingimuste põhjal. Eraldamise konto kanded luuakse iga töölehe jaoks protsendi ja siht-pearaamatukonto põhjal, alati kui raamatupidamiskirje vastab lähte-pearaamatukontona määratletud kriteeriumidele. Lisateabe jaoks vt [Põhikonto eraldustingimused](../general-ledger/main-account-allocation-terms.md)
-   Saate eraldada automaatselt pearaamatu saldosid või fikseeritud summasid pearaamatu eraldamisreeglite põhjal. Pearaamatu eraldamisreegleid töödeldakse perioodiliselt, kasutades eraldamise töölehti. Lisateavet leiate jaotisest [Eraldusreeglid](../general-ledger/ledger-allocation-rules.md).

###  <a name="allocations-in-budget-planning"></a>Eelarve plaanimise eraldamised

Pearaamatu eraldamisreegleid saab kasutada eelarveplaanide puhul. Eelarve plaanimisel pearaamatu eraldamisreeglite kasutamise korral toimivad eraldamisreeglid samal moel kui pearaamatus, kuid lähteandmed ja sihtandmed tulevad eelarveplaanist. Eelarveplaanides kasutatavad pearaamatu eraldamisreeglid saate valida käsitsi. Teise võimalusena saate kasutada eraldamisgraafikut, mida käitatakse osana töövooprotsessist.

> [!NOTE]
> Eelarve plaanimiseks ei saa kasutada kontsernisiseseid pearaamatu eraldamisreegleid.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]