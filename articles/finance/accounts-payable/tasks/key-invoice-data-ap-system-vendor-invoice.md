---
title: AP arve põhiandmed, kasutades hankija arvet
description: Selle tegevusejuhise abil saate ostutellimuse põhjal luua hankija arve ja vaadata ostutellimuse, sissetuleku ja arve (kolmesuunaline vastavusseviimine) vastavusseviimise tulemusi.
author: abruer
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f80c88b7fb3542f624d233f670cd7cd6ccd48b94
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442203"
---
# <a name="key-invoice-data-in-ap-using-a-vendor-invoice"></a>AP arve põhiandmed, kasutades hankija arvet

[!include [banner](../../includes/banner.md)]

Selle tegevusejuhise abil saate ostutellimuse põhjal luua hankija arve ja vaadata ostutellimuse, sissetuleku ja arve (kolmesuunaline vastavusseviimine) vastavusseviimise tulemusi.


## <a name="create-a-purchase-order"></a>Ostutellimuse loomine
1. Avage navigeerimispaanil **Moodulid > Arved > Ostutellimused > Kõik ostutellimused**.
2. Klõpsake valikut **Uus**.
3. Klõpsake väljal **Hankija konto** otsingu avamiseks ripploendi nuppu.
4. Leidke valitav hankija. Kerige näiteks alla suvandini US-104.
5. Valige hankija US-104.
6. Klõpsake valikut **OK**.
7. Klõpsake väljal **Kaubakood otsingu** avamiseks ripploendi nuppu.
8. Valige laokaup. Valige näiteks kauba number 1000.
9. Laiendage kiirkaarti **Rea üksikasjad**.
10. Klõpsake vahekaarti **Seadistamine**. Teil on võimalik alistada vastavusseviimise poliitika ja kasutada vastavusseviimise puudumist, kahesuunalist vastavusseviimist või kolmesuunalist vastavusseviimist.  
11. Klõpsake toimingupaanil valikut **Ost**.
12. Klõpsake käsku **Kinnita**.

## <a name="receive-the-products"></a>Toodete vastuvõtmine
1. Klõpsake toimingupaanil valikut **Vastuvõtt**.
2. Klõpsake valikut **Toote sissetulek**.
3. Sisestage väljale **Toote sissetulek** tootesissetuleku number. Sisestage näiteks PR123.
4. Klõpsake tootesissetuleku sisestamiseks nuppu **OK**.
5. Sulgege leht.

## <a name="create-a-vendor-invoice"></a>Hankijaarve koostamine
1. Minge navigeerimispaanil jaotisse **Moodulid > Maksmisele kuuluvad kontod > Ostutellimused> Saadud, kuid arveta ostutellimused**.
2. Valige loodud ostutellimus.
3. Klõpsake toimingupaanil valikut **Arve**.
4. Klõpsake **Arve**.
5. Sisestage väljale **Number** arve number.
6. Sisestage väljale **Arve kirjeldus** soovitud väärtus.
7. Sisestage kuupäev väljale **Arve kuupäev**.
8. Sisestage 1200 väljale **Ühiku hind**.
9. Klõpsake käsku **Lisa rida**.
10. Klõpsake väljal **Kaubakood otsingu** avamiseks ripploendi nuppu.
11. Leidke loendist installimistasu kaubakood. Näiteks S0001
12. Valige installimistasu kaubakood. Võtke arvesse, et vastavusseviimist pole pärast muudatuste tegemist toimunud.  
13. **Klõpsake suvandit Värskenda vastendamise olek.**
14. Klõpsake toimingupaanil valikut **Vaata üle**.
15. Klõpsake valikut **Vastanduvad üksikasjad**. Uus teenuste rida ei pea olema vastavusse viidud, nii et olekuks jääb Täitmata.  
16. Valige saadud laokauba toote sissetulek. Tootesissetuleku rida on vastavusse viidud, kuid kogus või hind ei sobi, nii et see nurjub.  
17. Sisestage arv väljale **Ühiku hind**. Nüüd, kui ühiku hind on vastavuses, värskendatakse olekut, ja uueks oleks seatakse Arvestatud. Kui teie poliitika lubab lahknevusi või kui vastavusseviimine on ainult hoiatus, saate arve siiski sisestada.  
18. Sulgege leht.
19. Klõpsake käsku **Sisesta**.
20. Sulgege vorm. Võtke arvesse, et ostutellimus pole loendis enam „vastu võetud“, vaid „arveldamata“.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]