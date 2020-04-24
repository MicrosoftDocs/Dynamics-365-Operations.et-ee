---
title: ER-i funktsioon REPLACE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni REPLACE.
author: NickSelin
manager: kfend
ms.date: 04/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 83d5095620a938f1ac4b8428fff9209fda7a7831
ms.sourcegitcommit: fb8ad8e2b142441a6530b364f3258bbcc0c724d2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201062"
---
# <a name=""></a><a name="REPLACE">ER-i funktsioon REPLACE</a>

[!include [banner](../includes/banner.md)]

Funktsioon `REPLACE` tagastab määratud tekstistringi *stringi* väärtusena pärast seda, kui kõik või osa sellest on asendatud teise stringiga.

## <a name="syntax"></a>Süntaks

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a>Argumendid

`text`: *string*

Tüübi *String* andmeallika kehtiv tee.

`pattern`: *string*

Kui argumendi `regular expression flag` tulem on **FALSE**, sisaldab see argument teksti, mis tuleb asendada.

Kui argumendi `regular expression flag` tulem on **TÕENE**, sisaldab see argument tavalist avaldist, mis määratleb nii otsingumustri kui ka asendusteksti.

`replacement`: *string*

Kui argumendi `regular expression flag` tulem on **FALSE**, sisaldab see argument asendamiseks kasutatavat teksti.

Kui argumendi `regular expression flag` tulem on **TRUE**, siis seda argumenti ei kasutata.

`regular expression flag`: *kahendmuutuja*

*Kahendmuutuja* väärtus, mis näitab, kas asendamiseks kasutatakse tavalist avaldist.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Kui argumendi `regular expression flag` tulem on **TRUE**, tagastab see funktsioon määratud stringi pärast selle muutmist, rakendades tavalise avaldise, mis on argumendiga `pattern` määratud. Tavalist avaldist kasutatakse asendatavate tähemärkide otsimiseks.

Kui argument `regular expression flag` on **VÄÄR**, tagastab see funktsioon määratud stringi pärast seda, kui argumendis `pattern` määratletud tähemärgid on asendatud argumendi `replacement` tähemärkidega. 

## <a name="example-1"></a>Näide 1

`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` rakendab regulaaravaldist, mis eemaldab kõik mittearvulised sümbolid, ja see tagastab väärtuse **„19234564971”**. 

## <a name="example-2"></a>Näide 2

`REPLACE ("abcdef", "cd", "GH", false)` asendab mustri **„cd”** stringiga **„GH”** ja tagastab väärtuse **„abGHef”**.

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)
