---
title: Tooteetaloni loomine
description: Tooteetaloni loomine eelmääratletud variantide puhul.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 70008e903763fff35c6cff12c42396fe5fcabbee
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832078"
---
# <a name="create-a-product-master"></a>Tooteetaloni loomine

[!include [banner](../../includes/banner.md)]

Tooteetaloni loomine eelmääratletud variantide puhul. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. See protseduur on mõeldud toote koostajale.


## <a name="create-a-new-product-master"></a>Uue tooteetaloni loomine
1. Avage **Navigeerimispaan > Moodulid > Tooteteabe haldus > Tooted > Tootetalongid**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Toote number**. Number peab olema kordumatu. Numbrijada saab seadistada välja **Tootenumber** puhul. Sellisel juhul ei pea kasutaja väärtust sisestama.
4. Sisestage väärtus väljale **Toote nimi**. Sisestage kirjeldav toote nimi. Väärtus on vaikimisi otsingunimi, kuid kasutaja saab seda muuta.
5. Klõpsake väljal **Tootedimensiooni grupp** otsingu avamiseks ripploendi nuppu. Tootedimensiooni grupp määrab, millist 4 tootedimensiooni saab kasutada tootevariantide loomiseks. Selles näites kasutatakse gruppi värvi ja suurusega.
6. Otsige loendist ja valige soovitud kirje.
7. Klõpsake loendis valitud real olevat linki. Vaikimisi **Konfiguratsioonitehnoloogiaks** on „Eelmääratletud variant”. Seda kasutatakse selle näite puhul.
8. Klõpsake valikut **OK**.

## <a name="select-product-dimension-groups"></a>Tootedimensiooni gruppide valimine
1. Klõpsake väljal **Värvigrupp** otsingu avamiseks ripploendi nuppu.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
4. Klõpsake väljal **Suuruse grupp** otsingu avamiseks ripploendi nuppu.
5. Otsige loendist ja valige soovitud kirje.
6. Klõpsake loendis valitud real olevat linki.

## <a name="add-dimension-groups"></a>Dimensioonigruppide lisamine
1. Klõpsake **toimingupaanil** suvandit **Toode**.
2. Klõpsake rippdialoogi avamiseks suvandit **Dimensioonigrupid**.
3. Klõpsake väljal **Laoala dimensiooni grupp** otsingu avamiseks ripploendi nuppu. Laoala dimensioonid aitavad reguleerida kaupade ladustamist ja laost väljastamist. Näiteks saab laoala dimensioon hõlmata tegevuskohta ja ladu.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake loendis valitud real olevat linki.
6. Klõpsake väljal **Jälgimisdimensiooni grupp** otsingu avamiseks ripploendi nuppu. Jälgimisdimensioonigrupp määratleb, milliseid jälgimisdimensioone saate tootele lisada. Näiteks kasutatakse laokaupade jälgimiseks partiinumbrit ja seerianumbrit.
7. Otsige loendist ja valige soovitud kirje.
8. Klõpsake loendis valitud real olevat linki.
9. Klõpsake valikut **OK**.
10. Klõpsake valikut **Salvesta**.
11. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]