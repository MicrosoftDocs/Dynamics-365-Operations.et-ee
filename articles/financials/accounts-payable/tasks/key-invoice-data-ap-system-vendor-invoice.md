---
title: Arve põhiandmed AP-süsteemis, kasutades hankija arvet
description: Selle tegevusejuhise abil saate ostutellimuse põhjal luua hankija arve ja vaadata ostutellimuse, sissetuleku ja arve (kolmesuunaline vastavusseviimine) vastavusseviimise tulemusi.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1d2e31a5de7cefd20996c18bf4771296a587997
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569628"
---
# <a name="key-invoice-data-in-ap-system-using-vendor-invoice"></a>Arve põhiandmed AP-süsteemis, kasutades hankija arvet

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selle tegevusejuhise abil saate ostutellimuse põhjal luua hankija arve ja vaadata ostutellimuse, sissetuleku ja arve (kolmesuunaline vastavusseviimine) vastavusseviimise tulemusi.


## <a name="create-a-purchase-order"></a>Ostutellimuse loomine
1. Avage Ostureskontro > Ostutellimused > Kõik ostutellimused.
2. Klõpsake valikut Uus.
3. Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.
4. Leidke valitav hankija. Kerige näiteks alla suvandini US-104.
5. Valige hankija US-104.
6. Klõpsake nuppu OK.
7. Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.
8. Valige laokaup. Valige näiteks kauba number 1000.
9. Laiendage või ahendage jaotist Rea üksikasjad.
10. Klõpsake vahekaarti Seadistus.
    * Teil on võimalik alistada vastavusseviimise poliitika ja kasutada vastavusseviimise puudumist, kahesuunalist vastavusseviimist või kolmesuunalist vastavusseviimist.  
11. Laiendage või ahendage jaotist Rea üksikasjad.
12. Klõpsake toimingupaanil valikut Ost.
13. Klõpsake käsku Kinnita.

## <a name="receive-the-products"></a>Toodete vastuvõtmine
1. Klõpsake toimingupaanil valikut Vastuvõtt.
2. Klõpsake valikut Toote sissetulek.
3. Sisestage väljale Toote sissetulek tootesissetuleku number. Sisestage näiteks PR123.
4. Klõpsake tootesissetuleku sisestamiseks nuppu OK.
5. Sulgege leht.

## <a name="create-a-vendor-invoice"></a>Hankijaarve koostamine
1. Avage Ostureskontro > Ostutellimused > Saadud, kuid arveldamata ostutellimused.
2. Valige loodud ostutellimus.
3. Klõpsake toimingupaanil valikut Arve.
4. Klõpsake valikut Arve.
5. Sisestage väljale Number arve number.
6. Sisestage väljale Arve kirjeldus soovitud väärtus.
7. Sisestage kuupäev väljale Arve kuupäev.
8. Sisestage 1200 väljale Ühiku hind.
9. Klõpsake käsku Lisa rida.
10. Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.
11. Leidke loendist installimistasu kaubakood. Näiteks S0001
12. Valige installimistasu kaubakood.
    * Võtke arvesse, et vastavusseviimist pole pärast muudatuste tegemist toimunud.  
13. Klõpsake valikut Värskenda vastandamise olek.
14. Klõpsake toimingupaanil valikut Vaata üle.
15. Klõpsake valikut Vastanduvad üksikasjad.
    * Uus teenuste rida ei pea olema vastavusse viidud, nii et olekuks jääb Täitmata.  
16. Valige saadud laokauba toote sissetulek.
    * Tootesissetuleku rida on vastavusse viidud, kuid kogus või hind ei sobi, nii et see nurjub.  
17. Sisestage arv väljale Ühiku hind.
    * Nüüd, kui ühiku hind on vastavuses, värskendatakse olekut, ja uueks oleks seatakse Arvestatud. Kui teie poliitika lubab lahknevusi või kui vastavusseviimine on ainult hoiatus, saate arve siiski sisestada.  
18. Sulgege leht.
19. Klõpsake valikut Sisesta.
20. Sulgege vorm.
    * Võtke arvesse, et ostutellimus pole loendis enam „vastu võetud“, vaid „arveldamata“.  

