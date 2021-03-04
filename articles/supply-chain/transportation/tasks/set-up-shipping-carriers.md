---
title: Vedajate seadistamine
description: See teema näitab, kuidas seadistada tarne vedaja ja määratleda üksikasjad, nt teenus, saadetise režiim, transpordi maksevahend, transpordi piirangud ja tarnekulu.
author: ShylaThompson
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a71ea3983018b136d4fe3b22eadc0c332d2a698
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4426628"
---
# <a name="set-up-shipping-carriers"></a>Vedajate seadistamine

[!include [banner](../../includes/banner.md)]

See teema näitab, kuidas seadistada tarne vedaja ja määratleda üksikasjad, nt teenus, saadetise režiim, transpordi maksevahend, transpordi piirangud ja tarnekulu. Transpordi koordinaator saab seejärel määrata saadetise vedaja sissetulevale või väljaminevale koormale.


## <a name="create-a-new-shipping-carrier"></a>Uue kättetoimetaja loomine
1. Valige **Navigeerimispaneel > Moodulid > Transpordi haldus > Seadistus > Vedajad > Kättetoimetajad**.
2. Valige Toimingupaanil suvand **Uus**.
3. Sisestage väärtus väljale **Kättetoimetaja**.
4. Sisestage väärtus väljale **Nimi**.
5. Valige väljal **Režiim** ripploendist suvand.

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a>Kättetoimetaja üldise teabe sisestamine
1. Laiendage jaotist **Ülevaade**.
2. Märkige või tühjendage ruut **Aktiveeri saadetise vedaja**.
3. Valige väljal **Hankija konto** ripploendist suvand. Valige hankija konto, millele tarne vedaja määrata.  
4. Valige suvand väljal **Transpordi maksevahendi tüüp**. Valige transpordi maksevahendi lehe kasutamiseks **Juhend** või valige **EDI**, pakkumist värskendada elektroonilise andmevahetuse (EDI) abil.  
5. Märkige või tühjendage ruut **Aktiveeri vedaja hinnang** .

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a>Kättetoimetaja vajalike teenuste loomine
1. Laiendage jaotist **Teenused**.
2. Valige suvand **Uus**.
3. Sisestage väärtus väljale **Vedaja teenus**.
4. Sisestage väärtus väljale **Nimi**.
5. Valige väljal **Transpordimeetod** ripploendist suvand.

## <a name="set-up-the-address-for-the-carrier-optional"></a>Vedaja aadressi seadistamine (valikuline)
1. Lülitage ümber jaotis **Aadressid**.
2. Valige suvand **Uus**.
3. Sisestage väärtus väljale **Nimi või kirjeldus**.
4. Valige väljal **Riik/regioon** ripploendist suvand.
5. Valige väljal **Postiindeks** ripploendist suvand.
6. Sisestage väärtus väljale **Tänav**.
7. Valige nupp **OK**.

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a>Kättetoimetaja hinnanguprofiili seadistamine
1. Laiendage jaotist **Hinnanguprofiilid**.
2. Valige suvand **Uus**.
3. Sisestage väärtus väljale **Hinnanguprofiil**.
4. Sisestage väärtus väljale **Nimi**.
5. Valige väljal **Sait** ripploendist suvand.
6. Valige väljal **Ladu** ripploendist suvand.
7. Valige väljal **Määra mootor** ripploendist suvand. Valige Määra mootor, mis on kooskõlas vedaja lepinguga.  
8. Valige väljal **Määra juht** ripploendist suvand.
9. Valige väljal **Transiidiaja mootor** ripploendist suvand.
10. Valige käsk **Salvesta**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]