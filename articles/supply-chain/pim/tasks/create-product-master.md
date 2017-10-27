--- 
title: Tooteetaloni loomine
description: "Tooteetaloni loomine eelmääratletud variantide puhul."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4e8d438da1524850c115f5c38865fac2f19f3ff5
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-product-master"></a>Tooteetaloni loomine

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tooteetaloni loomine eelmääratletud variantide puhul. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. See protseduur on mõeldud toote koostajale.


## <a name="create-a-new-product-master"></a>Uue tooteetaloni loomine
1. Avage Tooteteabe haldus > Tooted > Tooteetalonid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Toote number.
    * Number peab olema kordumatu. Numbrijada saab seadistada välja Tootenumber puhul. Sellisel juhul ei pea kasutaja väärtust sisestama.  
4. Sisestage väärtus väljale Toote nimi.
    * Sisestage kirjeldav toote nimi. Väärtus on vaikimisi otsingunimi, kuid kasutaja saab seda muuta.  
5. Klõpsake väljal Tootedimensiooni grupp otsingu avamiseks ripploendi nuppu.
    * Tootedimensiooni grupp määrab, millist 4 tootedimensiooni saab kasutada tootevariantide loomiseks. Selles näites kasutatakse gruppi värvi ja suurusega.  
6. Otsige loendist ja valige soovitud kirje.
7. Klõpsake loendis valitud real olevat linki.
    * Vaikimisi konfiguratsioonitehnoloogiaks on Eelmääratletud variant. Seda kasutatakse selle näite puhul.  
8. Klõpsake nuppu OK.

## <a name="select-product-dimension-groups"></a>Tootedimensiooni gruppide valimine
1. Klõpsake väljal Värvigrupp otsingu avamiseks ripploendi nuppu.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
4. Klõpsake väljal Suuruse grupp otsingu avamiseks ripploendi nuppu.
5. Otsige loendist ja valige soovitud kirje.
6. Klõpsake loendis valitud real olevat linki.

## <a name="add-dimension-groups"></a>Dimensioonigruppide lisamine
1. Klõpsake toimingupaanil suvandit Toode.
2. Klõpsake rippdialoogi avamiseks suvandit Dimensioonigrupid.
3. Klõpsake väljal Laoala dimensiooni grupp otsingu avamiseks ripploendi nuppu.
    * Laoala dimensioonid aitavad reguleerida kaupade ladustamist ja laost väljastamist. Näiteks saab laoala dimensioon hõlmata tegevuskohta ja ladu.  
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake loendis valitud real olevat linki.
6. Klõpsake väljal Jälgimisdimensiooni grupp otsingu avamiseks ripploendi nuppu.
    * Jälgimisdimensioonigrupp määratleb, milliseid jälgimisdimensioone saate tootele lisada. Näiteks kasutatakse laokaupade jälgimiseks partiinumbrit ja seerianumbrit.  
7. Otsige loendist ja valige soovitud kirje.
8. Klõpsake loendis valitud real olevat linki.
9. Klõpsake nuppu OK.
10. Klõpsake nuppu Salvesta.
11. Sulgege leht.


