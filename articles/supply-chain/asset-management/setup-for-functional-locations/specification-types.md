---
title: Hoolduse atribuudi tüübid
description: See artikkel selgitab, kuidas varahalduses atribuuditüüpe luua.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationTypeCopy, EntAssetAttributeType, EntAssetAttributeTypeValue, EntAssetFunctionalLocationType
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a0aca3ccf24505c064ad59f0adafb771056ba95
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887656"
---
# <a name="maintenance-attribute-types"></a>Hoolduse atribuudi tüübid

[!include [banner](../../includes/banner.md)]

 

See artikkel selgitab, kuidas varahalduses atribuuditüüpe luua. Atribuute kasutatakse erinevate elementide omaduste kirjeldamiseks. Saate seadistada atribuudid järgmistele elementidele.

- [Töö asukoha tüübid](../setup-for-functional-locations/functional-location-types.md)
- [Töö asukohtade loomine](../functional-locations/create-functional-locations.md)
- [Vara tüübid](../setup-for-objects/object-types.md)
- Varad

Seadistatavad atribuudid erinevad vastavalt elemendile. Näiteks saate funktsionaalsele asukohale seadistada atribuudid konfiguratsiooni ja asukoha füüsilise suuruse jaoks. Vara tüübi ja vara korral saate seadistada atribuudid mootorimahule, energiatarbele ja maksimaalsele koormusele erinevatel tingimustel.

## <a name="create-attribute-types"></a>Atribuudi tüüpide loomine

Saate luua oma atribuudi tüüpe. Lisaks saate edastada tootedimensioone rakendusest lehele **Atribuudi tüübid**.

1. Valige **Varahaldus**\>**Häälestus**\>**Atribuudi tüübid**.
2. Esimesel korral kui atribuudi tüüpe seadistate, valige **Tootedimensioonide loomine**, et edastada automaatselt standardsed tootedimensioonid.
3. Valige uue atribuudi tüübi loomiseks **Uus**.
4. Väljale **Atribuudi tüüp** sisestage atribuudi tüübi nimi.
5. Väljale **Kirjeldus** sisestage kirjeldus.
6. Väljale **Ühik** valige vastavalt vajadusele vastav atribuudi ühik.
7. Valige väljal **Andmetüüp** ühiku andmetüüp.
8. Kui valisite andmetüübiks **String**, toimige atribuudi tüübi väärtuste loomiseks järgmiselt.

    1. Valige atribuudi tüüp ja seejärel valige **Väärtused**.
    2. Valige väljal **Atribuudi väärtused** suvand **Uus**.
    3. Valige väljal **Atribuudi tüüp** atribuudi tüüp (dimensioon).
    4. Sisestage väljale **Väärtus** seotud väärtus.
    5. Väljale **Kirjeldus** sisestage kirjeldus.
    6. Salvesta kirje.
    7. Naaske lehele **Atribuudi tüübid**.

9. Salvesta kirje.

    Väli **Funktsionaalsed asukoha tüübid** näitab funktsionaalsete asukohtade arvu, mis atribuudi tüüpi kasutavad. Väli **Vara tüübid** näitab seda kasutavate vara tüüpide arvu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]