---
title: Algse eelarve loomine ja seejärel esialgse eelarve kirjete tagasivõtmine avalikus sektoris
description: Kui luuakse algse eelarve kande ja mida kasutatakse eelarve mudel ja dimensiooni väärtused, mis sisaldavad esialgses eelarvesummad, esialgsete eelarvesummade saab tühistada.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTransaction, BudgetAccountStructureLookup, BudgetTransactionMultiPost
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4895a48622d5bbd80ea284be8fe0b8e59622e488
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845738"
---
# <a name="create-an-original-budget-and-then-reverse-preliminary-budget-entries-in-the-public-sector"></a>Algse eelarve loomine ja seejärel esialgse eelarve kirjete tagasivõtmine avalikus sektoris

[!include [task guide banner](../../includes/task-guide-banner.md)]

Kui luuakse algse eelarve kande ja mida kasutatakse eelarve mudel ja dimensiooni väärtused, mis sisaldavad esialgses eelarvesummad, esialgsete eelarvesummade saab tühistada. See protseduur loodi PSUS-ettevõtte demoandmetega avaliku sektori sektsioonis.

1. Tehke valik Eelarvestamine > Eelarveregistri kirjed.
2. Klõpsake valikut Uus.
3. Klõpsake väljal Budget model (Eelarve mudel) otsingu avamiseks ripploendi nuppu.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake väljal Budget code (Eelarve kood) otsingu avamiseks ripploendi nuppu.
6. Klõpsake loendis valikut Original budget (Algne eelarve).
7. Klõpsake nuppu Salvesta.
8. Klõpsake käsku Lisa rida.
9. Valikuline: kui soovite päises kuupäeva muuta, sisestage uus kuupäev. See kuupäev määrab rahdnusperioodi, millesse eelarve salvestatakse.
10. Klõpsake väljal Konto struktuur otsingu avamiseks ripploendi nuppu.
11. Otsige loendist ja valige soovitud kirje.
12. Täpsustage väljal Dimension values (Dimensiooni väärtused) soovitud väärtused.
13. Sisestage number väljale Summa.
14. Klõpsake väljal Valuuta otsingu avamiseks ripploendi nuppu.
15. Klõpsake loendis valitud real olevat linki.
16. Klõpsake nuppu Salvesta.
17. Klõpsake Update budget balances (Värskenda eelarve tasakaalud).
    * Valikuline: Saate valida suvandi Reverse preliminary budget (Tühista esialgne eelarve). Pange tähele, et saate tühistada kõik esialgsed eelarvekanded või ainult teie poolt täpsustatud eelarvekoodiga esialgsed eelarvekanded.  
    * Lisavalikute tegemiseks klõpsake lehe ülaosas ikooni Unlock (Vabasta lukust).  
18. Klõpsake käsku Uuenda.

