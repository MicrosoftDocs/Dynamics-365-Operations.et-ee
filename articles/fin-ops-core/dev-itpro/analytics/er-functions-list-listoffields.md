---
title: ER-i funktsioon LISTOFFIELDS
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni LISTOFFIELDS.
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
ms.openlocfilehash: 0d51b59c437bd216c6d229546136bb604239fa92
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041994"
---
# <a name="LISTOFFIELDS">ER-i funktsioon LISTOFFIELDS</a>

[!include [banner](../includes/banner.md)]

Funktsioon `LISTOFFIELDS` tagastab *kirjete loendi* väärtuse, mis luuakse tüübi *Loetelu* või *Konteiner (kirje)* määratud argumendi struktuuri põhjal.

## <a name="syntax-1"></a>Süntaks 1

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a>Süntaks 2

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a>Argumendid

`path`: andmeallika viide

Ühe järgmistest andmetüüpidest andmeallika kehtiv viitetee.

- Mudeli loetelu
- Vormingu loetelu
- Rakenduse loetelu
- Konteiner (kirje)

`language`: *string*

Keele koodi tähistav tekst.

## <a name="return-values"></a>Tagastusväärtused

*Kirjete loend*

Saadud kirjete loend.

## <a name="usage-notes"></a>Kasutamise märkused

Loodud loend koosneb järgmiste väljadega kirjetest:

- **Nimi** (andmetüüp *String*)
- **Silt** (andmetüüp *String*)
- **Kirjeldus** (andmetüüp *String*)
- **IsTranslated** (andmetüüp *kahendmuutuja*)

Kui argument `path` viitab tüübi *Konteiner (kirje)* andmeallikale, lisatakse loodavasse loendisse iga viidatud konteineri kirje välja jaoks uus kirje. Iga loodud kirje puhul tagastab väli **Nimi** välja nime viidatud konteineri kirje jaoks, mille jaoks praegune kirje loodi.

Kui argument `path` viitab ühele tüübi *Loetelu* andmeallikale, lisatakse loodavasse loendisse iga viidatud loendi loetelu väärtuse jaoks uus kirje. Iga loodud kirje kohta tagastab väli **Nimi** viidatud loendi väärtuse, mille jaoks praegune kirje koostati, väli **Kirjeldus** tagastab selle loendi kirjelduse ja väli **Silt** tagastab selle loendi sildi.

Kui käitusajal kasutataks süntaksit 1, peavad väljad **Silt** ja **Kirjeldus** tagastama väärtused, mis põhinevad töötava elektroonilise aruandluse (ER) keelesätetel.

- Kui taotletud keele sildid ja kirjeldused on saadaval, tagastavad väljad **Silt** ja **Kirjeldus** väärtused, mis põhinevad sellel keelel, ja väli **IsTranslated** tagastab väärtuse **True**.
- Kui taotletud keele sildid ja kirjeldused ei ole saadaval, tagastavad väljad **Silt** ja **Kirjeldus** väärtused, mis põhinevad vaikekeelel **EN-US**, ja väli **IsTranslated** tagastab väärtuse **False**.

Kui käitusajal kasutataks süntaksit 2, peavad väljad **Silt** ja **Kirjeldus** tagastama väärtused, mis põhinevad keelel, mis on määratletud kutsutud funktsiooni teise argumendina.

- Kui taotletud keele sildid ja kirjeldused on saadaval, tagastavad väljad **Silt** ja **Kirjeldus** väärtused, mis põhinevad sellel keelel, ja väli **IsTranslated** tagastab väärtuse **True**.
- Kui taotletud keele sildid ja kirjeldused ei ole saadaval, tagastavad väljad **Silt** ja **Kirjeldus** väärtused, mis põhinevad keelel **EN-US**, ja väli **IsTranslated** tagastab väärtuse **False**.

## <a name="example-1"></a>Näide 1

Järgmises näites on ER-i andmemudelis kasutusele võetud loetelu.

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

Järgmises näites on toodud järgmised üksikasjad:

- mudeli loetelu on aruandesse sisestatud andmeallikana;
- ER-i avaldis kasutab mudeli loetelu funktsiooni `LISTOFFIELDS` parameetrina;
- tüübi *Kirjete loend* andmeallikas on sisestatud aruandesse loodud ER-i avaldise abil.

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

Järgmises näites kirjeldatakse ER-i vormingu elemente, mis on seotud funktsiooniga `LISTOFFIELDS` loodud tüübi *Kirjete loend* andmeallikaga.

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

Järgmisel joonisel on näidatud koostatud vormingu käitamise tulemus.

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> Siltide ja kirjelduste tõlgitud tekst sisestatakse ER-i vormingu väljundis vormingu peaelementide **FAIL** ja **KAUST** jaoks konfigureeritud keelesätete kohaselt.

## <a name="example-2"></a>Näide 2

Kasutate andmeallika tüüpi *Arvutatud väli* andmeallikate **enumType\_de** ja **enumTypede\_deCH** konfigureerimiseks andmemudeli loetelu **enumType** jaoks:

- **enumType\_de** = `LISTOFFIELDS (enumType, "de")`
- **enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`

Sel juhul saate järgmist avaldist kasutada Šveitsi saksa keele loeteluväärtuse sildi saamiseks, kui see tõlge on olemas. Kui šveitsi-saksa tõlge ei ole saadaval, on silt saksa keeles.

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)
