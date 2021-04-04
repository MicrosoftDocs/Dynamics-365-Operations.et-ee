---
title: ER-i funktsioon LISTDISTINCT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni LISTDISTINCT.
author: NickSelin
manager: kfend
ms.date: 7/30/2020
ms.topic: article
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
ms.openlocfilehash: f20565d73cea8d0cc1361bd03cda86a79a97955e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563820"
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