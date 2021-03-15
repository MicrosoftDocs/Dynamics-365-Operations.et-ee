---
title: ER-i funktsioon Base64StringToContainer
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni Base64StringToContainer.
author: NickSelin
manager: kfend
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 0e92ae41a3e0f03cb14d4791ab768f096f2a0523
ms.sourcegitcommit: e8a46e127d70986539c138b27a641bff6f6874d0
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/15/2020
ms.locfileid: "4739071"
---
# <a name="base64stringtocontainer-er-function"></a>ER-i funktsioon Base64StringToContainer

[!include [banner](../includes/banner.md)]

[Funktsioon](er-formula-language.md#functions) `BASE64STRINGTOCONTAINER` teisendab tüübi *String* määratud sisendi tüübi *[Konteiner](er-functions-category-container.md)* andmeüksuseks.

## <a name="syntax"></a>Süntaks

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a>Argumendid

`input`: *string*

Tüübi *String* andmeallika kehtiv tee.

## <a name="return-values"></a>Tagastusväärtused

*Konteiner*

Tulemuseks saadav kahendväärtus on binaarses suure objekti (BLOB) vormingus.

## <a name="usage-notes"></a>Kasutamise märkused

Kui sisendstring ei esita õiget binaarsest tekstiks kodeerimisskeemi Base64 gruppi, tehakse erand „Parameeter on kehtetu”.

## <a name="example"></a>Näide

Määratlege oma mudelivastenduses järgmised andmeallikad.

- Andmeallika **DocuTypeGroupEnum** juur tüübil *Dynamics 365 for Operations / loetellu*, mis viitab rakenduse loetelule **DocuTypeGroup**
- Andmeallika **Klient** juur tüübil *Dynamics 365 for Operations / tabelikirjed*, mis viitab rakenduse tabelile **CustTable**
- Andmeallikas **\#Meedium** tüübil *Arvutatud väli*, mis on konfigureeritud järgnevalt.

    - See on lisatud andmeallikale **Klient** alamandmeallikana.
    - See sisaldab avaldist `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.

- Andmeallikas **\#MediaAsBase64String** tüübil *Arvutatud väli*, mis on konfigureeritud järgnevalt.

    - See on lisatud andmeallikale **Klient.'\#Meedium'** alamandmeallikana.
    - See sisaldab avaldist `Customer.'#Media'.'getFileContentAsBase64String()'`.

- Andmeallikas **\#BlobFomBase64** tüübil *Arvutatud väli*, mis on konfigureeritud järgnevalt.

    - See on lisatud andmeallikale **Klient.'\#Meedium'** alamandmeallikana.
    - See sisaldab avaldist `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.

Selles näites kodeerib andmeallikas **\#MediaAsBase64String** praeguse meediumi manuse binaarse sisu tekstina, mis tähistab binaarsest tekstiks kodeerimisskeemi Base64 gruppi. Andmeallikas **\#BlobFomBase64** dekodeerib Base64 stringi ja tagastab binaarse väärtuse BLOB-vormingus.

![Näidis andmeallikad ER-i mudeli vastenduse koostaja lehel](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a>Lisaressursid

[Konteineri funktsioonid](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]