---
title: "Veose täiendustellimuse loomine"
description: "See protseduur näitab, kuidas koostada veose täiendustellimust, kus saate jälgida hankija eeldatavat tarnet oma veose varudesse."
author: mkirknel
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f7f8005ec9e723c94d53e6ab81f04ee388c83faa
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-consignment-replenishment-order"></a>Veose täiendustellimuse loomine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas koostada veose täiendustellimust, kus saate jälgida hankija eeldatavat tarnet oma veose varudesse. Samuti näitab see, kuidas registreerida toodete sissetulekut, et veose varud oleksid registreeritud hankijale kuuluva vaba kaubavaruna. Selle protseduuri viib tavaliselt läbi hankespetsialist. Saate seda juhendit kasutada demoettevõtte USMF andmetega. See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.




## <a name="create-a-consignment-replenishment-order"></a>Veose täiendustellimuse loomine
1. Avage Hanked > Saadetis > Saadetise täiendustellimused.
2. Klõpsake valikut Uus.
3. Valige väljalt Hankija konto hankija US-104.
    * Peate valima hankija, kes on registreeritud omanikuna lehel Varude omanikud.  
4. Klõpsake nuppu OK.
5. Klõpsake käsku Lisa rida.
6. Tippige väärtus M9211CI väljale Kaubakood.
    * Peate valima kauba, mis on seadistatud veose kaubavaruna.  
7. Sisestage arv väljale Kogus.
8. Sisestage kuupäev väljale Nõutav tarnekuupäev.
    * MRP moodul kasutab nõutud ja kinnitatud kuupäevi kaupade eeldatava saabumise jaoks.  
9. Sisestage kuupäev väljale Kinnitatud tarnekuupäev.
10. Laiendage jaotis Rea üksikasjad.
11. Klõpsake vahekaarti Varude dimensioonid.
12. Omaniku näitamiseks väljal Laodimensioonide omanik värskendage lehte.
    * Hankija US-104 on nüüd omanikuna registreeritud.  

## <a name="check-the-inventory-transaction-status"></a>Kontrollige kande kuupäeva olekut
1. Klõpsake Ladu.
2. Klõpsake suvandit Kanded.
3. Märkige loendis valitud rida.
    * Pange tähele, et välja Sissetulek olekuks on määratud Tellitud.  
4. Sulgege leht.

## <a name="receive-items"></a>Võta kaubad vastu
1. Klõpsake valikut Toote sissetulek.
2. Tippige väärtus väljale Väline toote sissetulek.
3. Sisestage väljale Kogus seal kuvatud numbrist väiksem number.
4. Klõpsake nuppu OK.

## <a name="check-the-on-hand-inventory"></a>Kontrollige vaba kaubavaru
1. Klõpsake Ladu.
2. Klõpsake valikut Laoseis.
3. Klõpsake valikut Ülevaade.
    * Kaubad, mis on saadud hankijale kuuluva veose kaubavaruna, on vaba varuna saadaval. Ülejäänud kogus veose täiendustellimusel on näidatud väljal Tellitud kokku.  
4. Sulgege leht.
5. Klõpsake valikut Sule.

