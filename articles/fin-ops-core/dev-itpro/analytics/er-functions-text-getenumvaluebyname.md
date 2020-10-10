---
title: ER-i funktsioon GETENUMVALUEBYNAME
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni GETENUMVALUEBYNAME.
author: NickSelin
manager: kfend
ms.date: 09/23/2020
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
ms.openlocfilehash: 722ea8ea233d617b0584e21e98073428f16c0801
ms.sourcegitcommit: ad5b7676fc1213316e478afcffbfaee7d813f3bb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/24/2020
ms.locfileid: "3885223"
---
# <a name="getenumvaluebyname-er-function"></a>ER-i funktsioon GETENUMVALUEBYNAME

[!include [banner](../includes/banner.md)]

Funktsioon `GETENUMVALUEBYNAME` otsib määratud *loetelu* andmeallikast konkreetset loetelu väärtust, kasutades loendi nime, mis on määratud *stringi* väärtuseks. Kui *loetelu* väärtus leitakse, tagastab funktsioon selle. Vastasel korral tagastab funktsioon loendamise väärtuse **null**.

## <a name="syntax"></a>Süntaks

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>Argumendid

`enumeration data source path`: *loetelu*

Ühe järgmistest loenditüüpidest andmeallika kehtiv tee.

- Elektroonilise aruandluse (ER) mudeli loetelu
- ER-vormingu loetelu
- Microsoft Dynamics 365 Finance’i loetelu

`enumeration value text`: *string*

Stringi väärtus, mis tähistab ühe loetelu väärtuse nime.

## <a name="return-values"></a>Tagastusväärtused

Nullitav *loetelu*

Tulemiks saadud loetelu väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Ühtegi erandit ei esitata, kui väärtust *Loetelu* ei leita, kasutades loetelu väärtuse nime, mis on määratud *stringi* väärtuseks.

## <a name="example-1"></a>Näide 1

Järgmises näites on andmemudelis kasutusele võetud loetelu **ReportDirection**. Pange tähele, et loetelu väärtuste puhul on määratletud sildid.

![Andmemudeli loetelu jaoks saadaolevad väärtused](./media/ER-data-model-enumeration-values.PNG)

Järgmises näites on toodud järgmised üksikasjad:

- Andmeallikas **$Direction** konfigureeritakse ER-i aruandes. See andmeallikas konfigureeritakse mudeli **ReportDirection** loetelu põhjal.
- Avaldis `$IsArrivals` on mõeldud kasutama mudeli loetelul põhinevat andmeallikat **$Direction** selle funktsiooni parameetrina.
- Võrdluse avaldise väärtus on **TRUE**.

![Andmemudeli loetelu näide](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a>Näide 2

Funktsioonid `GETENUMVALUEBYNAME` ja [`LISTOFFIELDS`](er-functions-list-listoffields.md) võimaldavad teil tuua toetatud loetelude väärtuseid ja silte tekstiväärtustena. (Toetatud loetelud on rakenduse loetelud, andmemudeli loetelud ja vormingu loetelud.)

Järgmises näites on mudelivastenduses kasutusele võetud andmeallikas **TransType**. See andmeallikas viitab rakenduse loetelule **LedgerTransType**.

![Mudelivastenduse andmeallikas, mis viitab rakenduse loetelule](./media/er-functions-text-getenumvaluebyname-example2-1.png)

Järgmises näites on näha andmeallikas **TransTypeList**, mis on konfigureeritud mudelivastenduses. See andmeallikas konfigureeritakse rakenduse loetelu **TransType** põhjal. Funktsiooni `LISTOFFIELDS` kasutatakse selleks, et tagastada kõik loetelu väärtused välju sisaldavate kirjete loendina. Sel viisil on iga loetelu väärtuse üksikasjad nähtaval.

> [!NOTE]
> Väli **EnumValue** konfigureeritakse andmeallika **TransTypeList** jaoks avaldise `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` abil. See väli tagastab loetelu väärtuse iga selles loendis oleva kirje jaoks.

![Mudelivastenduse andmeallikas, mis tagastab valitud loetelu kõik loetelu väärtused kirjete loendina](./media/er-functions-text-getenumvaluebyname-example2-2.png)

Järgmises näites on näha andmeallikas **VendTrans**, mis on konfigureeritud mudelivastenduses. See andmeallikas tagastab rakenduse tabelist **VendTrans** pärit hankija kandekirjed. Iga kande pearaamatu tüüp määratletakse välja **TransType** väärtuse põhjal.

> [!NOTE]
> Väli **TransTypeTitle** konfigureeritakse andmeallika **VendTrans** jaoks avaldise `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` abil. See väli tagastab praeguse kande loetelu väärtuse sildi tekstina, kui see loetelu väärtus on saadaval. Muidu tagastatakse tühja stringi väärtus.
>
> Väli **TransTypeTitle** on seotud väljaga **LedgerType**, mis kuulub andmemudelisse, mis võimaldab seda teavet kasutada igas ER-i vormingus, mis kasutab seda andmemudelit andmeallikana.

![Mudelivastenduse andmeallikas, mis tagastab hankija kanded](./media/er-functions-text-getenumvaluebyname-example2-3.png)

Järgmisel joonisel on näha, kuidas saate kasutada [andmeallika silurit](er-debug-data-sources.md) konfigureeritud mudelivastenduse testimiseks.

![Andmeallika siluri kasutamine konfigureeritud mudelivastenduse testimiseks](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

Andmeallika väli **LedgerType** muudab kandetüüpide sildid ootuspäraselt nähtavaks.

Kui kavatsete kasutada seda meetodit suure hulga kandeandmete jaoks, peate võtma arvesse käitamise jõudlust. Lisateavet leiate teemast [Elektroonilise aruandluse vormingute täitmise jälitamine jõudlusprobleemide tõrkeotsinguks](trace-execution-er-troubleshoot-perf.md).

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)

[Elektroonilise aruandluse vormingute täitmise jälitamine jõudlusprobleemide tõrkeotsinguks](trace-execution-er-troubleshoot-perf.md)

[ER-i funktsioon LISTOFFIELDS](er-functions-list-listoffields.md)

[ER-i funktsioon FIRSTORNULL](er-functions-list-firstornull.md)

[ER-i funktsioon WHERE](er-functions-list-where.md)
