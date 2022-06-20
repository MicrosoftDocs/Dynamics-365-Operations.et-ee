---
title: ER-i funktsioon LISTDISTINCT
description: See artikkel annab teavet selle kohta, kuidas KASUTATAKSE FUNKTSIOONI LISTDISTINCT Electronic reporting (ER).
author: NickSelin
ms.date: 7/30/2020
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: d2f8e3a9d077493df3c3b7628608d31834f43f8a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876801"
---
# <a name="listdistinct-er-function"></a>ER-i funktsioon LISTDISTINCT

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Funktsioon `LISTDISTINCT` arvutab määratud avaldise valijana iga kirje jaoks, mis asub määratud loendis. See tagastab uue väärtuse *Kirjete loend*, mis sisaldab ühte kirjet iga kordumatu valija väärtuse kohta.

## <a name="syntax"></a>Süntaks

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a>Argumendid

`list`: *kirjete loend*

Andmetüübi *Kirjete loend* andmeallika kehtiv tee.

`selector`: *primitiivne andmetüüp*

Sobiv avaldis, mida kasutatakse valija väärtuse arvutamiseks määratud loendi iga kirje jaoks.

Selle parameetri puhul toetatakse järgmisi andmetüüpe.

- Kahendmuutuja
- Kuupäev
- DateTime
- GUID
- Täisarv
- Int64
- Tegelik
- String

## <a name="return-values"></a>Tagastusväärtused

*Kirjete loend*

Saadud kirjete loend.

## <a name="usage-notes"></a>Kasutamise märkused

Loodud loendi struktuur ühtib määratud loendi struktuuriga.

Samasugust valija väärtust võib arvutada määratud loendis mitme kirje jaoks. Sel juhul on loodud loendi asjaomase kirje väljade väärtused võrdsed määratud loendi esimese kirje väärtustega, mille jaoks valija väärtus arvutatakse.

Seda funktsiooni kasutatakse kõikide [elektroonilise aruandluse (ER)](general-electronic-reporting.md) andmeallikate puhul, mille tüüp on *Kirjete loend* ja mis on mälus olemas.

Andmeallikat **GROUPBY** saab kasutada ka nende kirjete loendi loomiseks, mille jaoks arvutatakse eristatavate väärtustega valija. Kuid jõudluse ja mälu tarbimise vaatenurgast on parem kasutada funktsiooni `LISTDISTINCT`, mitte andmeallikat **GROUBPY**, sest funktsioon käivitatakse mälus.

## <a name="example"></a>Näide

Järgmises näites on näha, kuidas saada loend kordumatutest kliendi kontonumbritest, millele on väljastatud kindla perioodi jooksul vähemalt üks müügi- või projektiarve.

1. Sisestage andmeallikas **SalesInvoice**, mille tüüp on `Record list` ning mis viitab rakendustabelile **CustInvoiceJour** ja filtreerib kindlate perioodide müügiarveid.

    Selle andmeallika väli `InvoiceAccount` tagastab arveldatud kliendi kontonumbri.

2. Sisestage andmeallikas **ProjectInvoice**, mille tüüp on `Record list` ning mis viitab rakendustabelile **ProjInvoiceJour** ja filtreerib kindlate perioodide projektiarveid.

    Selle andmeallika väli `InvoiceAccount` tagastab arveldatud kliendi kontonumbri.

3. Konfigureerige andmeallikas **AllInvoices**, mille tüüp on `Calculated field` ja mis sisaldab avaldist `LISTJOIN(SalesInvoice, ProjectInvoice)`.

    See andmeallikas tagastab müügi- ja projektiarvete ühendatud loendi.

4. Konfigureerige andmeallikas **InvoicedCustomer**, mille tüüp on `Record list` ja mis sisaldab avaldist `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.

    See andmeallikas tagastab uue loendi, mis sisaldab ühte kirjet iga kordumatu kliendi kohta, kellega on perioodi jooksul arveldatud. Selle loendi väli `InvoiceAccount` sisaldab kliendi kontonumbrit.

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]