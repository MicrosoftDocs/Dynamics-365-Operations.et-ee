---
title: ER-i funktsioon LIST
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni LIST
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 6848fe535a6a588eaf06f96e93f28db9ef304940
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917277"
---
# <a name="LIST">ER-i funktsioon LIST</a>

[!include [banner](../includes/banner.md)]

Funktsioon `LIST` tagastab *kirjete loendi* väärtuse, mis koosneb määratud argumentidest loodud uuest kirjete loendist.

## <a name="syntax"></a>Süntaks

```
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
