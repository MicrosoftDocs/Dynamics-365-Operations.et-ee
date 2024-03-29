---
title: Teenindustase ja kirjeldus
description: See artikkel selgitab teenuse taset ja kirjeldust varahalduses.
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
ms.openlocfilehash: 753ad36b1d01d1ce0594f477cf863ca0e4a1ac75
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879188"
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