---
title: Teenindustase ja kirjeldus
description: Selles teemas selgitatakse teenindustaset ja kirjeldust varahalduses.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectServiceLevel, EntAssetWorkOrderStandardDescription, EntAssetWorkOrderServiceLevel, EntAssetServiceLevelLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 32e6dd6ba7291e8ea1cb78eeed2d8e2fcec0f6dd3cbd039336be0169730101ba
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758684"
---
# <a name="service-level-and-description"></a>Teenindustase ja kirjeldus

[!include [banner](../../includes/banner.md)]

 

Kui loote töökäsu, võite soovida määratleda selle teenindustasemeid ja lisada sellele üldise kirjelduse. Töökäsu teenindustasemeid saate luua lehel **Töökäsu teenindustasemed** ja kirjeldusi lehel **Töökäsu kirjeldus**.

## <a name="create-a-service-level"></a>Teenindustaseme loomine

1. Valige **Varahaldus** \> **Seadistus** \> **Töökäsud** \> **Teenindustase**.
2. Valige suvand **Uus**.
3. Sisestage väljale **Teenindustase** teenindustase (näiteks arv).
4. Väljale **Nimi** sisestage nimi.

    Kiirkaardil **Töökäsud** saate määratleda oodatavat alguse ja lõpukuupäeva ning kellaaega. Selle kiirkaardi väljad määratlevad ajaperioodi, mille kestel töökäsud tuleks alustada ja lõpetada. Neid kasutatakse käsitsi loodud töökäskude korral ja hooldusnõuetel põhinevate töökäskude korral. 

5. Sisestage väljale **Alguspäev** päevade arv, et määrata periood, mille jooksul töökäsku peaks alustama. Päevade arvu arvutatakse alates töökäsu loomise kuupäevast. Näiteks, kui töökäsk peaks algama siis, kui see loodi, sisestage **0**. Kui töökäsk peaks algama ühe nädala jooksul pärast selle loomist, sisestage **7**.
6. Töökäsu alguskuupäeva seadistamiseks seadistage lisaks alguskuupäevale suvand **Määra algusaeg** olekusse **Jah**. Siis sisestage algusaeg väljale **Algusaeg**. Kui seadistasite suvandi olekusse **Ei**, kasutatakse praegust kellaaega.
7. Sisestage väljale **Lõpp-päev** päevade arv, et määrata periood, mille jooksul töökäsku peaks lõpetama. Päevade arvu arvutatakse alates töökäsu alguskuupäevast. Näiteks, kui töökäsk peaks lõppema ühe nädala jooksul alates alguskuupäevast, sisestage **7**.
8. Töökäsu lõppkellaaja seadistamiseks seadistage lisaks lõpp-päevale suvand **Määra lõppkellaaeg** olekusse **Jah**. Siis sisestage lõppkellaaeg väljale **Lõppkellaaeg**. Kui seadistasite suvandi olekusse **Ei**, kasutatakse praegust kellaaega.
9. Valige käsk **Salvesta**.

![Töökäskude teenusetaseme leht.](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a>Kirjelduse loomine

1. Valige **Varahaldus** \> **Seadistus** \> **Töökäsud** \> **Kirjeldus**.
2. Valige suvand **Uus**.
3. Sisestage kirjeldus väljale **Kirjeldus**.
4. Valige käsk **Salvesta**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]