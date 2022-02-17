---
title: Funktsioon GETLABELTEXT ER
description: See teema annab teavet selle kohta, kuidas funktsiooni GETLABELTEXT elektroonilist aruandlust (ER) kasutatakse.
author: NickSelin
ms.date: 01/04/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 911567a94b80c2b762a37e83d37fc500132edb18
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075743"
---
# <a name="getlabeltext-er-function"></a>Funktsioon GETLABELTEXT ER

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Funktsioon `GETLABELTEXT` otsib kindlat silti, et tagastada *[stringi](er-formula-supported-data-types-primitive.md#string)* väärtus, mis tähistab määratud sildi tõlget määratud keeles.

## <a name="syntax"></a>Süntaks

```vb
GETLABELTEXT (label id, language)
```

## <a name="arguments"></a>Argumendid

### <a name="label-id"></a>Sildi ID

`label id`: *Stringi* või *sildi ID*

Ühe järgmiste silditüüpide kehtiv ID:

- [Elektroonilise aruandluse (ER)](general-electronic-reporting.md) silt
- Microsofti Dynamics 365 Finance silt

#### <a name="usage-notes"></a>Kasutamise märkused

Seda argumenti saab määratleda ainult konstandina, kasutades ühte järgmistest toetatud mustritest.

- ER-i siltide puhul:

    - `@"GER_LABEL:<LABEL ID>"`
    - `"GER_LABEL:<LABEL ID>"`

- Finantssiltide puhul:

    - `@"<LABEL ID>"`
    - `"<LABEL ID>"`

> [!NOTE]
> Kujundusajal kuvatakse **[valemikujundaja](er-advanced-formula-editor.md)** lehel valideerimisvea teade, kui esitatud sildi ID abil silti ei leita.

### <a name="language"></a>Keel

`language`: *string*

String, mis tähistab keelekoodi.

#### <a name="usage-notes"></a>Kasutamise märkused

Seda argumenti saab määratleda kas tekstikonstandina või andmeallika välja teena, mis tagastab *stringiväärtuse*.

> [!NOTE]
> Kujundusajal kuvatakse valideerimistõrke teade, kui esitatud `language` argumendi abil ei leita ühtegi keelekoodi, kui see on määratletud tekstikonstandina.
>
> Käitusajal tagastatakse süsteemikeele tõlge `EN-US` määratud sildile, kui esitatud `language` argumendi abil pole keelekoodi leitud.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="example-1-system-label"></a><a name=example-1></a> Näide 1: süsteemi silt

Väljendid `GETLABELTEXT (@"SYS70894", "en-us")` ja `GETLABELTEXT ("SYS70894", "en-us")` tagastage rakenduse sildi ingliskeelne tõlge "Pole midagi printida" `@SYS70894`.

## <a name="example-2-er-label"></a><a name=example-2></a> Näide 2: ER-silt

Te hakkate redigeerima ISO20022 kreeditülekande (DE) konfiguratsioonist tuletatud ER-i [konfiguratsiooni](general-electronic-reporting.md#Configuration)[, sisestage](er-quick-start2-customize-report.md#DeriveProvidedFormat) välja arvutatud **uue andmeallika ja konfigureerige selle andmeallika avaldis**.*[...](er-calculated-field-ds-performance.md)*`GETLABELTEXT(@"GER_LABEL:VendorName", "de")` Sellisel juhul tagastab andmeallikas käitusajal saksakeelse tõlke "Kreditorenname" ER-märgise jaoks`@GER_LABEL:VendorName`, mis oli algselt konfigureeritud ISO20022 krediidiülekande (DE) **ER-i põhikonfiguratsioonis**.

## <a name="additional-resources"></a>Lisaressursid

[Tekstifunktsioonid](er-functions-category-text.md)

[Mitmekeelsete aruannete kujundamine elektroonilises aruandluses](er-design-multilingual-reports.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
