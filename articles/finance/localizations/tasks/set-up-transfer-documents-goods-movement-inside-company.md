---
title: Ettevõttesisese kaupade liikumise ülekandedokumentide häälestus
description: See protseduur näitab, kuidas määrata üleviimisdokumente kaupade liikumisel ettevõtte sees.
author: v-oloski
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 80805bf30b4be753d7543ed4c6de30401d36e981
ms.sourcegitcommit: 2fba4f2ef7e513357366fc640befe0d2f7bc31f5
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/05/2021
ms.locfileid: "7601446"
---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a>Ettevõttesisese kaupade liikumise ülekandedokumentide häälestus

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
