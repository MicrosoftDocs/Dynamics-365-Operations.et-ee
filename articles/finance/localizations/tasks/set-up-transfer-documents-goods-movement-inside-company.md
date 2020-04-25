---
title: Ettevõttesisese kaupade liikumise ülekandedokumentide seadistamine
description: See protseduur näitab, kuidas koostada üleviimisdokumente kaupade liikumisel ettevõtte sees.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e85bd359ce1053629ad4217cf623e57b2976463a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143478"
---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a>Ettevõttesisese kaupade liikumise ülekandedokumentide seadistamine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas koostada üleviimisdokumente kaupade liikumisel ettevõtte sees. See protseduur on saadaval ainult juriidilistele isikutele, kelle esmane aadress on Leedus. Selle protseduuri loomisel kasutati demoettevõtte DEMF, mille esmaseks aadressiks on Leedu, andmeid. Enne seda protseduuri tuleb teha protseduur „Kaupade liikumise ülekandedokumendi seadistamine ettevõtte sees”. See protseduur on mõeldud laoraamatupidajatele. See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.


## <a name="create-a-transfer-order"></a>Üleviimistellimuse loomine
1. Avage Varude haldamine > Sissetulevad tellimused > Üleviimistellimus.
2. Klõpsake valikut Uus.
3. Sisestage või valige väärtus väljal Laost.
4. Sisestage või valige väärtus väljal Lattu.
5. Klõpsake vahekaarti Lisa.
6. Märkige loendis valitud rida.
7. Sisestage või valige väärtus väljal Kaubakood.

## <a name="enter-transportation-details-for-the-transfer-order"></a>Üleviimistellimuse transpordi üksikasjade sisestamine
1. Klõpsake nuppu Salvesta.
2. Klõpsake tegumiribal valikut Läheta.
3. Klõpsake valikut Transpordi üksikasjad.
4. Tehke väljal Prindi transpordi üksikasjad valik Jah.
5. Valige või sisestage väärtus väljal Kauba väljastaja.
6. Tippige väärtus väljale Pakk.
7. Tippige väärtus väljale Koorma riskitase.
8. Valige või sisestage väärtus väljal Vedaja.
9. Valige või sisestage väärtus väljal Mudel.
10. Tippige väärtus väljale Registreerimisnumber.
11. Tippige väärtus väljale Treileri registreerimisnumber.
12. Valige või sisestage väärtus väljal Juht.
13. Tippige väärtus väljale Juhi nimi.
14. Klõpsake nuppu Salvesta.
15. Sulgege leht.

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a>Sisestamata üleviimistellimuse saatelehe kuvamine
1. Klõpsake suvandit Saateleht.
2. Klõpsake nuppu OK.
3. Sulgege leht.

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a>Sisestatud üleviimistellimuse saatelehe kuvamine
1. Klõpsake tegumiribal valikut Üleviimistellimus.
2. Klõpsake tegumiribal valikut Läheta.
3. Klõpsake valikut Lähetuse üleviimistellimus.
4. Klõpsake vahekaarti Üldine.
5. Tehke valik väljal Uuenda.
6. Klõpsake vahekaarti Ülevaade.
7. Sisestage väärtus väljale Saateleht.
8. Klõpsake nuppu OK.
9. Klõpsake tegumiribal valikut Läheta.
10. Klõpsake suvandit Saateleht.
11. Klõpsake nuppu OK.

