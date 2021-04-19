---
title: Varude loendamine laos
description: Selles teemas kirjeldatakse protsessi, kuidas luua ja sisestada varude inventuuritöölehte, et loendada konkreetset kaupa asukohas laos.
author: MarkusFogelberg
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 24b8bc2daff2d7df6279c76f4d9a0e83244c7988
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834045"
---
# <a name="count-inventory-in-a-warehouse"></a>Varude loendamine laos

[!include [banner](../../includes/banner.md)]

Selles teemas kirjeldatakse protsessi, kuidas luua ja sisestada varude inventuuritöölehte, et loendada konkreetset kaupa asukohas laos. Seda protseduuri rakendatakse funktsiooni „üldine ladustamine” puhul laohalduse moodulis, mitte ladustamisfunktsiooni puhul moodulis Laohaldus. Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades. Kui kasutate oma andmeid, siis veenduge, et teil oleksid tooted ja asukohad seadistatud ja et oleksite loonud inventuuritöölehtedele varude töölehe nime. Inventuuri teeb harilikult laotöötaja.


## <a name="create-an-inventory-counting-journal"></a>Lao inventuuritöölehe loomine
1. **Avage Laohaldus > Töölehe sisestused > Kauba inventuur > Inventuur.**
2. Valige suvand **Uus**.
3. Valige väljal **Nimi** varude inventuuri töölehe nimi, mida soovite ripploendis kasutada. Mõned muud väljad täidetakse teie valitud lao inventuuritöölehe nime seadistuse põhjal.  
4. Klõpsake välja **Töötaja** otsingu avamiseks ripploendi nuppu.
5. **Valige** loendist töötaja, keda soovite kasutada.
6. Valige nupp **OK**.

## <a name="create-journal-lines"></a>Loo töölehe read
1. Valige suvand **Uus**.
2. Väljal **Eseme number** valige soovitud kirje ripploendist. Kui kasutate demoettevõtte USMF andmeid, valige **A0001**.  
3. Väljal **sait** valige soovitud kirje ripploendist. Kui kasutate demoettevõtte USMF andmeid, valige tegevuskoht **2**.
4. Väljal **Ladu** valige soovitud kirje ripploendist. Kui kasutate demoettevõtte USMF andmeid, valige ladu **24**.  
5. Väljal **Asukoht** valige soovitud kirje ripploendist. Kui kasutate demoettevõtte USMF andmeid, valige tegevuskoht **BULK-001**.  
6. Sisestage number väljale Loendatud. Kui sisestate loendatud arvu, mis erineb väljal **Laos** näidatud arvust, värskendatakse välja **Kogus**, näidates lahknevust.  
7. Valige käsk **Salvesta**.

## <a name="post-the-inventory-counting-journal"></a>Lao inventuuritöölehe sisestamine
1. Valige **Sisesta**. Kui sisestate lao inventuuritöölehe ja loendatud arv erineb väljal **Laos** olevast kogusest, sisestatakse lao sissetulek või väljaminek, kaubavaru taset ja väärtust muudetakse ja tekitatakse pearaamatukanded.
2. Valige nupp **OK**.

## <a name="view-inventory-transactions"></a>Varude kannete kuvamine
1. Valige **Laoseis**.
2. Valige **Kanded**. Siin saate vaadata kõiki seotud kandeid, mis teie laoinventuuri töölehe sisestamisel luuakse.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]