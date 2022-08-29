---
title: ER-i funktsioon Base64StringToContainer
description: See artikkel annab teavet selle kohta, kuidas base64StringToContainer elektroonilise aruandluse (ER) funktsiooni kasutatakse.
author: kfend
ms.date: 12/14/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 96dfffc3d899f1106c6c931efb08c941f5b3c1a6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291230"
---
# <a name="base64stringtocontainer-er-function"></a>ER-i funktsioon Base64StringToContainer

[!include [banner](../includes/banner.md)]

[Funktsioon](er-formula-language.md#Functions) `BASE64STRINGTOCONTAINER` teisendab tüübi *String* määratud sisendi tüübi *[Konteiner](er-functions-category-container.md)* andmeüksuseks.

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

![Näidis andmeallikad ER-i mudeli vastenduse koostaja lehel.](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a>Lisaressursid

[Konteineri funktsioonid](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
