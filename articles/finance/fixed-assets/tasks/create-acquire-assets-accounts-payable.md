---
title: Varade loomine ja soetamine ostureskontrost
description: See ülesande juhend annab ülevaate põhivara loomise ja soetamise kohta ostuprotsessiga.
author: saraschi2
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb7c92fcab622109b01590d4acadce0d707d3d2d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227084"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Varade loomine ja soetamine ostureskontrost

[!include [banner](../../includes/banner.md)]

See ülesande juhend annab ülevaate põhivara loomise ja soetamise kohta ostuprotsessiga.  See kasutab raamatupidamis- ja ostureskontroametnikke ja demoettevõtet USMF.


## <a name="set-fixed-assets-parameters"></a>Põhivara parameetrite määramine
1. Paanil **Navigeerimispaan** avage **Moodulid > Põhivarad > Seadistus > Põhivara parameetrid**.
2. Laiendage kiirkaart **Ostutellimused**.
3. Märkige märkeruut **Luba vara soetamine ostmiselt**.
4. Märkige märkeruut **Loo vara toote sissetuleku või arve sisestamise ajal**.

## <a name="create-a-new-vendor-invoice"></a>Uue hankija arve koostamine
1. Paanil **Navigeerimispaan** avage **Moodulid > Ostureskontro > Tööruumid > Hankija arved**.
2. Klõpsake **Uus hankija arve**.
3. Väljal **Arve konto** klõpsake rippmenüü nuppu, et avada otsing.
4. Klõpsake loendis valitud real olevat linki.
5. Sisestage väärtus väljale **Arv**.
6. Väljale **Sisestuskuupäev** sisestage kuupäev.
7. Klõpsake käsku **Lisa rida**.
8. Väljal **Kaubakood** klõpsake ripploendi nuppu, et avada otsing. Põhivara soetamisel saab kasutada mitteladustatavaid kaupu või hankekategooriaid.  
9. Klõpsake loendis valitud real olevat linki.
10. Sisestage arv väljale **Kogus**. Üks arve rida loob ainult ühe põhivara, olenemata kogusest. Arve koguse välja väärtus kantakse üle põhivara kogusele.  
11. Sisestage arv väljale **Ühiku hind**.
12. Laiendage kiirkaarti **Rea üksikasjad**.
13. Klõpsake vahekaarti **Põhivarad**.
14. Märkige märkeruut **Loo uus põhivara**.
15. Väljal **Põhivara grupp** klõpsake rippmenüü nuppu, et avada otsing.
16. Valige loendist uue põhivara loomiseks kasutatav põhivara grupp.
17. Klõpsake loendis valitud real olevat linki.
18. Klõpsake käsku **Sisesta**. Põhivara luuakse ja soetatakse arve sisestamisel.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]