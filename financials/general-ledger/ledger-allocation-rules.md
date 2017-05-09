---
title: Pearaamatu eraldamisreeglid
description: Selles artiklis antakse teavet pearaamatu eraldamisreeglite kohta. See kirjeldab nende eraldamisreeglite mitmesuguseid komponente ja eraldamismeetodeid, mida nende puhul kasutada saab.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bd2ba11ff4f10d3369babf10fc70659ae8a717fa
ms.lasthandoff: 03/31/2017


---

# <a name="ledger-allocation-rules"></a>Pearaamatu eraldamisreeglid

[!include[banner](../includes/banner.md)]


Selles artiklis antakse teavet pearaamatu eraldamisreeglite kohta. See kirjeldab nende eraldamisreeglite mitmesuguseid komponente ja eraldamismeetodeid, mida nende puhul kasutada saab.

Pearaamatu eraldamisreegleid kasutatakse eraldamistöölehtede ja kontokannete automaatseks arvutamiseks ja loomiseks pearaamatu saldode või fikseeritud summade eraldamise eesmärgil. Eraldamismeetodid võivad olla muutuvad või fikseeritud. Pearaamatu eraldamisreeglite jaoks saab kasutada järgmisi eraldamismeetodeid.

-   **Alus** – seda muutujameetodit kasutatakse, kui eraldamine sõltub tegelikust pearaamatu saldost, võttes aluseks filtreerimiskriteeriumid. Näiteks saab eraldada reklaamikulusid iga osakonna müügitulemuste põhjal osakondade kogu müügitulu suhtes.
-   **Fikseeritud protsent** ja **fikseeritud mass** – nende meetodite puhul määratletakse reegli jaoks otse eraldamisprotsent või -mass. Näiteks saab reklaamikulusid eraldada nii, et osakond A saab 70 protsenti ja osakond B 30 protsenti reklaamikulust.
-   **Võrdne** – see meetod jaotab summa võrdselt iga määratud sihtkoha vahel. Näiteks kui osakonna A ja osakonna B jaoks on sihtkohad määratletud, saab reklaamikulusid eraldada nii, et nii osakond A kui ka osakond B saavad 50 protsenti reklaamikuludest.

Kui eraldamisreegli puhul on eraldamismeetodiks Alus, peate määratlema ka eraldi pearaamatu eraldamise põhised reeglid. Eraldamistaotluse töötlemise protsess võimaldab kasutajatel töödelda pearaamatu eraldamisreeglit ja saadud eraldustöölehe kandeid eelvaadata, enne kui need arvutatud eraldused kas sisestavad või kustutavad.

## <a name="components-of-ledger-allocation-rules"></a>Pearaamatu eraldamisreeglite komponendid
Igal eraldamisreeglil on neli komponenti: üldine, allikas, sihtkoht ja vastaskonto. Kui eraldamismeetodiks on Alus, on nõutav täiendav komponent, pearaamatu eraldamispõhised reeglid. Iga komponent annab olulise osa eraldamiste töötlemiseks vajalikust teabest.

-   **Üldine** – selles komponendis määrab kasutaja valikud, nagu eraldamismeetod, kontsernisisesed reeglisätted ja see, kas reegel on aktiivne või mitte.
-   **Allikas** – selles komponendis määrab kasutaja eraldamise lähteandmed. Eraldamine võib toimuda pearaamatu saldode (**Andmeallikas** = **peaaamat**) või fikseeritud summade (**Andmeallikas** = **fikseeritud väärtus**) põhjal. Kui suvandi **Andmeallikas** sätteks on valitud **Pearaamat**, tuleb pearaamatu eraldamisreegli jaoks määratleda allika filtreerimiskriteeriumid (nt reklaamikulude jaoks).
-   **Sihtkoht** – see komponent määratleb, kuidas tuleks eraldamisarvutuse tulemus jaotada ja arvestada. Näiteks saab olla iga osakonna kohta üks sihtkoharida.
-   **Vastaskonto** – see komponent määratleb, kuidas tuleks põhikontod ja dimensioonid sihkohakandeid tasakaalustavate vastaskonto kannete kohta määrata. Allikal põhinevate kontode ja dimensioonide asemel kasutatakse tavaliselt kasutaja määratletud suvandeid. Kui suvandi **Andmeallikas** sätteks on valitud **Fikseeritud väärtus**, ei saa suvandit **Allikas** kasutada.
-   **Pearaamatu eraldamispõhised reeglid** – need reeglid määratlevad oma allika filtreerimiskriteerumite alusel, milliseid pearaamatu saldosid tuleks eraldamiseks kasutada (nt eelarve osakonna kohta). Iga eralduspõhist reeglit saab kasutada mitme eraldusreegliga.




