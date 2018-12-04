--- 
title: Varade loomine ja soetamine ostureskontrost
description: "See ülesande juhend annab ülevaate põhivara loomise ja soetamise kohta ostuprotsessiga."
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e6c36338cc67855c79ec97d88bb8b633417b85c7
ms.contentlocale: et-ee
ms.lasthandoff: 09/14/2018

---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Varade loomine ja soetamine ostureskontrost

[!include [task guide banner](../../includes/task-guide-banner.md)]

See ülesande juhend annab ülevaate põhivara loomise ja soetamise kohta ostuprotsessiga.  See kasutab raamatupidamis- ja ostureskontroametnikke ja demoettevõtet USMF.


## <a name="set-fixed-assets-parameters"></a>Põhivara parameetrite määramine
1. Avage Põhivarad > Seadistus > Põhivarade parameetrid.
2. Laiendage või ahendage jaotist Ostutellimused.
3. Märkige ruut Luba vara soetamine ostmiselt.
4. Märkige ruut Loo vara toote sissetuleku või arve sisestamise ajal.

## <a name="create-a-new-vendor-invoice"></a>Uue hankija arve koostamine
1. Avage Ostureskontro > Tööruumid > Hankija arved.
2. Klõpsake suvandit Uus hankija arve.
3. Klõpsake väljal Arve konto otsingu avamiseks ripploendi nuppu.
4. Klõpsake loendis valitud real olevat linki.
5. Sisestage väärtus väljale Arv.
6. Sisestage kuupäev väljale Sisestuskuupäev.
7. Klõpsake käsku Lisa rida.
8. Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.
    * Põhivara soetamisel saab kasutada mitteladustatavaid kaupu või hankekategooriaid.  
9. Klõpsake loendis valitud real olevat linki.
10. Sisestage arv väljale Kogus.
    * Üks arve rida loob ainult ühe põhivara, olenemata kogusest.  Arve koguse välja väärtus kantakse üle põhivara kogusele.  
11. Sisestage arv väljale Ühiku hind.
12. Laiendage või ahendage jaotist Rea üksikasjad.
13. Klõpsake vahekaarti Põhivara.
14. Märkige ruut Loo uus põhivara.
15. Klõpsake väljal Põhivara grupp otsingu avamiseks ripploendi nuppu.
16. Valige loendist uue põhivara loomiseks kasutatav põhivara grupp.
17. Klõpsake loendis valitud real olevat linki.
18. Klõpsake valikut Sisesta.
    * Põhivara luuakse ja soetatakse arve sisestamisel.  


