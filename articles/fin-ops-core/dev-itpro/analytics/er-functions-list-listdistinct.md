---
title: ER-i funktsioon LISTDISTINCT
description: See artikkel annab teavet selle kohta, kuidas KASUTATAKSE FUNKTSIOONI LISTDISTINCT Electronic reporting (ER).
author: kfend
ms.date: 07/30/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: cd773f3455af1be1e952cb3852a648436670ce0f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285271"
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
