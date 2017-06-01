---
title: "Eraldiste töötlemine"
description: "Selles artiklis antakse teavet eraldamiste kohta, nende töötlemise võimaluste kohta Microsoft Dynamics 365 for Operationsis ja nende kasutamise kohta eelarve planeerimisel. Eraldamisi kasutatakse summade jaotamiseks mitme pearaamatukonto kombinatsiooni lõikes. Need aitavad tagada seda, et raamatupidamises esitatakse kulud või tulud õigele objektile."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1cfaeab1562716aa4c91806b228f17625e25dfff
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="process-allocations"></a>Eraldiste töötlemine

[!include[banner](../includes/banner.md)]


Selles artiklis antakse teavet eraldamiste kohta, nende töötlemise võimaluste kohta Microsoft Dynamics 365 for Operationsis ja nende kasutamise kohta eelarve planeerimisel. Eraldamisi kasutatakse summade jaotamiseks mitme pearaamatukonto kombinatsiooni lõikes. Need aitavad tagada seda, et raamatupidamises esitatakse kulud või tulud õigele objektile.

Microsoft Dynamics 365 for Operations annab selle protsessi toetamiseks järgmised võimalused.

-   Kandesummade käsitsi eraldamine, kasutades arvestuse jaotustes tükeldamise toimingut või rakendades dokumendile finantsdimensiooni vaikemalle. Lisateavet kuluarvestuse kohta vt jaotisest [Arvestuse jaotused.](../accounts-payable/accounting-distributions.md)
-   Saate eraldada automaatselt kandesummasid eraldi põhikontol määratletud eraldustingimuste põhjal. Eraldamise konto kanded luuakse iga töölehe jaoks protsendi ja siht-pearaamatukonto põhjal, alati kui raamatupidamiskirje vastab lähte-pearaamatukontona määratletud kriteeriumidele.
-   Saate eraldada automaatselt pearaamatu saldosid või fikseeritud summasid pearaamatu eraldamisreeglite põhjal. Pearaamatu eraldamisreegleid töödeldakse perioodiliselt, kasutades eraldamise töölehti. 

###  <a name="allocations-in-budget-planning"></a>Eelarve plaanimise eraldamised

Pearaamatu eraldamisreegleid saab kasutada eelarveplaanide puhul. Eelarve plaanimisel pearaamatu eraldamisreeglite kasutamise korral toimivad eraldamisreeglid samal moel kui pearaamatus, kuid lähteandmed ja sihtandmed tulevad eelarveplaanist. Eelarveplaanides kasutatavad pearaamatu eraldamisreeglid saate valida käsitsi. Teise võimalusena saate kasutada eraldamisgraafikut, mida käitatakse osana töövooprotsessist.

> [!NOTE]
> Eelarve plaanimiseks ei saa kasutada kontsernisiseseid pearaamatu eraldamisreegleid.






