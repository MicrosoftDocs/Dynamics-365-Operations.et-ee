---
title: Eraldiste töötlemine
description: Selles artiklis antakse teavet eraldamiste kohta, nende töötlemise võimaluste kohta Microsoft Dynamics 365 for Finance and Operationsis ja nende kasutamise kohta eelarve planeerimisel. Eraldamisi kasutatakse summade jaotamiseks mitme pearaamatukonto kombinatsiooni lõikes. Need aitavad tagada seda, et raamatupidamises esitatakse kulud või tulud õigele objektile.
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
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9a1946875460e9dfafb481b288a6d6a10ba8931d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846795"
---
# <a name="process-allocations"></a>Eraldiste töötlemine

[!include [banner](../includes/banner.md)]

Selles artiklis antakse teavet eraldamiste kohta, nende töötlemise võimaluste kohta Microsoft Dynamics 365 for Finance and Operationsis ja nende kasutamise kohta eelarve planeerimisel. Eraldamisi kasutatakse summade jaotamiseks mitme pearaamatukonto kombinatsiooni lõikes. Need aitavad tagada seda, et raamatupidamises esitatakse kulud või tulud õigele objektile.

Microsoft Dynamics 365 for Finance and Operations annab selle protsessi toetamiseks järgmised võimalused.

-   Kandesummade käsitsi eraldamine, kasutades arvestuse jaotustes tükeldamise toimingut või rakendades dokumendile finantsdimensiooni vaikemalle. Lisateavet kuluarvestuse kohta vt jaotisest [Arvestuse jaotused.](../accounts-payable/accounting-distributions.md)
-   Saate eraldada automaatselt kandesummasid eraldi põhikontol määratletud eraldustingimuste põhjal. Eraldamise konto kanded luuakse iga töölehe jaoks protsendi ja siht-pearaamatukonto põhjal, alati kui raamatupidamiskirje vastab lähte-pearaamatukontona määratletud kriteeriumidele.
-   Saate eraldada automaatselt pearaamatu saldosid või fikseeritud summasid pearaamatu eraldamisreeglite põhjal. Pearaamatu eraldamisreegleid töödeldakse perioodiliselt, kasutades eraldamise töölehti. 

###  <a name="allocations-in-budget-planning"></a>Eelarve plaanimise eraldamised

Pearaamatu eraldamisreegleid saab kasutada eelarveplaanide puhul. Eelarve plaanimisel pearaamatu eraldamisreeglite kasutamise korral toimivad eraldamisreeglid samal moel kui pearaamatus, kuid lähteandmed ja sihtandmed tulevad eelarveplaanist. Eelarveplaanides kasutatavad pearaamatu eraldamisreeglid saate valida käsitsi. Teise võimalusena saate kasutada eraldamisgraafikut, mida käitatakse osana töövooprotsessist.

> [!NOTE]
> Eelarve plaanimiseks ei saa kasutada kontsernisiseseid pearaamatu eraldamisreegleid.





