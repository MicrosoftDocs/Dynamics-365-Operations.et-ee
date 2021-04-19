---
title: Hoolduse atribuudi tüübid
description: Selles teemas selgitatakse, kuidas luua varahalduses atribuudi tüüpe.
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
ms.openlocfilehash: 283cff931ce665ae09152c8f3d3c976b7c8b66ff
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808516"
---
# <a name="maintenance-attribute-types"></a>Hoolduse atribuudi tüübid

[!include [banner](../../includes/banner.md)]

 

Selles teemas selgitatakse, kuidas luua varahalduses atribuudi tüüpe. Atribuute kasutatakse erinevate elementide omaduste kirjeldamiseks. Saate seadistada atribuudid järgmistele elementidele.

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