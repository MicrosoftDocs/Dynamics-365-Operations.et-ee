---
title: FUNKTSIOON GETLABELTEXT ER
description: See artikkel annab teavet selle kohta, kuidas getLABELTEXT elektroonilise aruandluse (ER) funktsiooni kasutatakse.
author: kfend
ms.date: 03/18/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: AX 10.0.25
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: dad87548518b77f2def1cf2383a21607f45170e1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285935"
---
# <a name="getlabeltext-er-function"></a>FUNKTSIOON GETLABELTEXT ER

[!include [banner](../includes/banner.md)]

Funktsioon `GETLABELTEXT` otsib konkreetset silti, et tagastada *[stringi](er-formula-supported-data-types-primitive.md#string)* väärtus, mis tähistab määratud sildi tõlget määratud keeles.

## <a name="syntax"></a>Süntaks

```vb
GETLABELTEXT (label id, language)
```

## <a name="arguments"></a>Argumendid

### <a name="label-id"></a>Sildi ID

`label id`: *stringi* või *sildi ID*

Ühe järgmise silditüübi kehtiv ID:

- [Elektroonilise aruandluse (ER)](general-electronic-reporting.md) silt
- Microsoft Dynamics 365 finantside silt

#### <a name="usage-notes"></a>Kasutamise märkused

Seda argumenti saab määratleda ainult konstandina, kasutades üht järgmistest toetatud mustritest:

- ER-siltidele:

    - `@"GER_LABEL:<LABEL ID>"`
    - `"GER_LABEL:<LABEL ID>"`

- Finantssiltide jaoks:

    - `@"<LABEL ID>"`
    - `"<LABEL ID>"`

> [!NOTE]
> Kui silti ei leita **[...](er-advanced-formula-editor.md)** antud sildi ID abil, kuvatakse konstruktsiooni ajal valemikujundaja lehel valideerimise tõrketeade.

### <a name="language"></a>Keel

`language`: *string*

Keelekoodi tähistav string.

#### <a name="usage-notes"></a>Kasutamise märkused

Seda argumenti saab määratleda kas tekstikonstandina või andmeallika välja teena, mis tagastab *stringiväärtuse*.

> [!NOTE]
> Konstruktsiooni ajal kuvatakse valideerimise tõrketeade `language`, kui keelekoodi ei leita esitatud argumenti kasutades, kui see on määratletud tekstikonstandina.
>
> Käitusajal tagastatakse süsteemikeele `EN-US` tõlge määratud sildile, kui antud argumenti kasutades pole keelekoodi `language` leitud.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="example-1-system-label"></a><a name=example-1></a> Näide 1: süsteemi silt

Avaldised `GETLABELTEXT (@"SYS70894", "en-us")` ja `GETLABELTEXT ("SYS70894", "en-us")` tagastage avalduse sildi jaoks inglise tõlge "Pole midagi `@SYS70894` printida".

## <a name="example-2-er-label"></a><a name=example-2></a> Näide 2: ER-silt

Alustate ISO20022 krediidiülekande (DE) konfiguratsioonist tuletatud ER-konfiguratsiooni [...](general-electronic-reporting.md#Configuration)[...](er-quick-start2-customize-report.md#DeriveProvidedFormat)**redigeerimist,** *[...](er-calculated-field-ds-performance.md)* sisestate väljatüübi Arvutatud uue andmeallika ja konfigureerite selle andmeallika avaldise.`GETLABELTEXT(@"GER_LABEL:VendorName", "de")` Sel juhul tagastab andmeallikas `@GER_LABEL:VendorName` käitusajal saksa tõlke "Kreditorenname" **ER-sildi jaoks, mis algselt konfigureeriti iso20022 baaskrediidiülekande (DE)** ER-i konfiguratsioonis.

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)

[Mitmekeelsete aruannete kujundamine elektroonilises aruandluses](er-design-multilingual-reports.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
