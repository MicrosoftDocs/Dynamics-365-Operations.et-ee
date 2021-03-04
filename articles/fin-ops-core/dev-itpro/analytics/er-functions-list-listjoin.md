---
title: ER-i funktsioon LISTJOIN
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni LISTJOIN.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28f03e5e6af0f252a994f2e54b57a5ef654f4e67
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682239"
---
# <a name="listjoin-er-function"></a>ER-i funktsioon LISTJOIN

[!include [banner](../includes/banner.md)]

`LISTJOIN` funktsioon tagastab *kirjete loendi* väärtuse, mis tähistab määratud argumentidest loodud uut ühendatud kirjete loendit.

## <a name="syntax"></a>Süntaks

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a>Argumendid

`list 1`: *kirjete loend*

Viide andmetüübi *Kirjete loend* andmeallikale. See argument on kohustuslik.

`list N`: *kirjete loend*

Viide andmetüübi *Kirjete loend* andmeallikale. Need täiendavad argumendid on valikulised.

## <a name="return-values"></a>Tagastusväärtused

*Kirjete loend*

Saadud kirjete loend.

## <a name="usage-notes"></a>Kasutamise märkused

Loodud loendi struktuur sisaldab ainult neid välju, mis on esitatud argumentides mainitud iga kirjete loendi struktuuris.

## <a name="example"></a>Näide

Sisestate tüübi `Container` andmeallika **Kirje 1**. See andmeallikas sisaldab tüübi `Calculated field` järgmisi pesastatud välju:

- **Kood**: see väli sisaldab avaldist, mis tagastab tüübi `String` väärtuse.
- **Summa**: see väli sisaldab avaldist, mis tagastab tüübi `Real` väärtuse.

Seejärel sisestate tüübi `Container` andmeallika **Kirje 2**. See andmeallikas sisaldab tüübi `Calculated field` järgmisi pesastatud välju:

- **Summa**: see väli sisaldab avaldist, mis tagastab tüübi `Real` väärtuse.
- **IsValid**: see väli sisaldab avaldist, mis tagastab tüübi `Boolean` väärtuse.

![ER-i mudelivastenduse koostaja leht](./media/er-functions-list-listjoin-image1.gif)

Sel juhul tagastab avaldis `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` uue loendi, mis sisaldab kaht kirjet.

![ER-i mudelivastenduse koostaja leht kahe kirjega](./media/er-functions-list-listjoin-image2.gif)

Selle loendi struktuur koosneb ühest tüübi `Real` väljast **Summa**, kuna see väli on ainuke väli, mis on esitatud kutsutud funktsiooni igas argumendis.

![ER-i mudelivastenduse koostaja lehe summaväli](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)

[Käivitatud ER-vormingu andmeallikate silumine andmevoo ja teisenduse analüüsimiseks](er-debug-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]