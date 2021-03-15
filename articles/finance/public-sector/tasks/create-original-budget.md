---
title: Algse eelarve loomine ja seejärel esialgse eelarve kirjete tagasivõtmine avalikus sektoris
description: See teema kirjeldab, kuidas luua ja tühistada algset eelarvekirjet, kasutades eelarvemudelit ja dimensiooniväärtusi, mis hõlmavad esialgseid eelarvesummasid.
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
ms.search.region: Global
ms.search.industry: Service industries
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 134e2ca851d72965198026107817c66a808ac705
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987950"
---
# <a name="create-an-original-budget-and-then-reverse-preliminary-budget-entries-in-the-public-sector"></a>Algse eelarve loomine ja seejärel esialgse eelarve kirjete tagasivõtmine avalikus sektoris

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]