---
title: Vara tootjad ja mudelid
description: See artikkel selgitab, kuidas seadistada vara tootjaid ja seotud mudeleid Varahalduses.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetProductLookup, EntAssetModelLookup, EntAssetProduct
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 95d0998bbacef7a4350d0fd0a58259ec35759d28
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868039"
---
# <a name="asset-manufacturers-and-models"></a>Vara tootjad ja mudelid

[!include [banner](../../includes/banner.md)]

 

See artikkel selgitab, kuidas seadistada vara tootjaid ja seotud mudeleid Varahalduses. Mudelid võivad olla seotud varade tüüpidega.

## <a name="set-up-product-model-relations"></a>Tooteseoste häälestamine

1. Valige **Varahaldus**\>**Häälestus**\>**Varad**\>**Tootja ja mudel**.
2. Valige uue toote loomiseks **Uus**.
3. Väljale **Tootja** sisestage vara tootja nimi.
4. Väljale **Kirjeldus** sisestage kirjeldus.
5. Kiirkaardil **Mudelid** valige **Lisa** varamudeli loomiseks, mis peaks olema seotud vara tootjaga.
6. Väljale **Mudel** sisestage vara mudeli nimi.
7. Väljale **Kirjeldus** sisestage kirjeldus.
8. Väljal **Vara tüüp** valige vara tüüp, millega tootja mudel peaks seotud olema.

    > [!NOTE]
    > Samuti saate seadistada vara tüüpide, tootjate ja mudelite vahelisi seoseid otsingus **Vara tüübid**. Lisateavet leiate teemast [Vara tüübid](../setup-for-objects/object-types.md).

    Kiirkaardil **Üksikasjad** kuvatakse väljal **Mudelid** valitud vara tootja jaoks seadistatud vara mudelite arv. Väljal **Varad** kuvatakse valitud tootja kasutavate varade arv.
    
    Väljal **varad** kuvatakse valitud tootja kasutavate objektid arv.

> [!NOTE]
> Vara tüübil ei saa olla vara tootja mudeli seoste kogumeid, see võib olla seotud ühe vara tootja mudeliga või mitme vara tootja mudeliga. Kui vara tüüp on seotud vähemalt ühe tootja mudeliga, saab nende varahalduse lehtedel valida ainult neid kombinatsioone, mis on sätestatud otsingus **Tootja mudel**, kus saab sätestada vara tüübi, tootja ja mudeli kombinatsiooni. Need leheküljed hõlmavad suvandeid **Kõik varad**, **Vara teenindustasemed**, **Töö tüübi vaikesätted** ja **Hoolduse eelarveread**. Kui mõned vara tüübid ei ole seotud ühegi tootja mudeliga, kuvatakse lehtedel ainult need vara tüübid ja tootja mudelid, millel puudub seos vara tüüpidega.

## <a name="select-a-manufacturer-and-model-on-an-object"></a>Valige objektil tootja ja mudel

1. Valige **Varahaldus**\>**Ühised**\>**Varad**\>**Kõik varad**.
2. Veerus **Vara** valige vara link. Kuvatakse leht **Üksikasjad**.
3. Valige suvand **Redigeeri**.
4. Kiirkaardil **Üldine** valige väärtused väljadel **Tootja** ja **Mudel**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]