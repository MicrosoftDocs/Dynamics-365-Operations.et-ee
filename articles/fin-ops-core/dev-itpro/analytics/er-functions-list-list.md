---
title: ER-i funktsioon LIST
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni LIST
author: NickSelin
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50cb8858301c030df07ad4af9fe2a9513f41fead
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750408"
---
# <a name="list-er-function"></a>ER-i funktsioon LIST

[!include [banner](../includes/banner.md)]

Funktsioon `LIST` tagastab *kirjete loendi* väärtuse, mis koosneb määratud argumentidest loodud uuest kirjete loendist.

## <a name="syntax"></a>Süntaks

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a>Argumendid

`record 1`: *konteiner (kirje)*

Viide andmetüübi *Kirje* andmeallikale. See argument on kohustuslik.

`record N`: *konteiner (kirje)*

Viide andmetüübi *Kirje* andmeallikale. Need täiendavad argumendid on valikulised.

## <a name="return-values"></a>Tagastusväärtused

*Kirjete loend*

Saadud kirjete loend.

## <a name="usage-notes"></a>Kasutamise märkused

Loodud loendi struktuur sisaldab ainult neid välju, mis on esitatud argumentides mainitud iga kirje struktuuris.

## <a name="example"></a>Näide

Sisestate tüübi *Konteiner* andmeallika **Kirje 1**. See andmeallikas sisaldab tüübi *Arvutatud välja* järgmisi pesastatud välju:

- **Kood:** see väli sisaldab avaldist, mis tagastab tüübi *String* väärtuse.
- **Kogus:** see väli sisaldab avaldist, mis tagastab tüübi *Tegelik* väärtuse.

Seejärel sisestate tüübi *Konteiner* andmeallika **Kirje 2**. See andmeallikas sisaldab tüübi *Arvutatud välja* järgmisi pesastatud välju:

- **Kogus:** see väli sisaldab avaldist, mis tagastab tüübi *Tegelik* väärtuse.
- **IsValid:** see väli sisaldab avaldist, mis tagastab tüübi *Kahendmuutuja* väärtuse.

Sel juhul tagastab avaldis `LIST('Record 1', 'Record 2')` uue loendi, mis sisaldab kaht kirjet. Selle loendi struktuur koosneb ühest tüübi *Tegelik* väljast **Summa**, kuna see väli on ainuke väli, mis on esitatud kutsutud funktsiooni igas argumendis.

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]