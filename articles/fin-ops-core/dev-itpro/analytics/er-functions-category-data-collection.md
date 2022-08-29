---
title: ER-i funktsioonide loend andmete kogumise kategoorias
description: See artikkel annab teavet andmete kogumise funktsioonide kohta, mida toetab elektrooniline aruandlus (ER).
author: kfend
ms.date: 12/04/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: e01bed49646ffe344004f9eb51e9013e1b4c5430
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286145"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a>ER-i funktsioonide loend andmete kogumise kategoorias

[!include [banner](../includes/banner.md)]

Elektroonilise aruandluse (ER) andmete kogumise funktsioone kasutatakse, et loendada ja liita käitatav ER-vorming, mis põhineb juba **teksti** või **XML-i** vormingus loodud väljundi andmetel. Seda varianti kasutatakse käitatud ER-vormingu jõudluse parandamiseks, loodud dokumentides jooksvate kogusummade väärtuste sisestamiseks ja muuks otstarbeks. See artikkel annab nende funktsioonide kokkuvõtte.

## <a name="list-of-supported-functions"></a>Toetatud funktsioonide loend

| Funktsioon | Kirjeldus |
|----------|-------------|
| [CollectedList](er-functions-datacollection-collectedlist.md) | See funktsioon tagastab *kirjete loendi* väärtuse, mis sisaldab nende väärtuste loendit, mis on tagastatud vorminguelementide atribuudi **Kogutud andmete võtme väärtus** poolt ja kogutud, kui vorminguelemente kasutati väljamineva dokumendi loomisel vormingu käitamise ajal, ja mis vastab määratud tingimustele. Iga tingimus koosneb võtmevahemikust ja võtmeväärtusest. |
| [CountIF](er-functions-datacollection-countif.md) | See funktsioon tagastab *täisarvu* väärtuse, mis tähistab vorminguelementide arvu, mis koguti, kui vorminguelemente kasutati väljamineva dokumendi loomiseks vormingu käitamise ajal, ja mis vastab määratud tingimusele. See tingimus koosneb võtmevahemikust ja võtmeväärtusest. |
| [CountIFs](er-functions-datacollection-countifs.md) | See funktsioon tagastab *täisarvu* väärtuse, mis tähistab vorminguelementide arvu, mis koguti, kui vorminguelemente kasutati väljamineva dokumendi loomiseks vormingu käitamise ajal, ja mis vastab määratud tingimustele. Iga tingimus koosneb võtmevahemikust ja võtmeväärtusest. |
| [FormatElementName](er-functions-datacollection-formatelementname.md) | See funktsioon tagastab *stringi* väärtuse, mis tähistab praeguse ER-vormingu elemendi nime. |
| [SumIF](er-functions-datacollection-sumif.md) | See funktsioon tagastab *tegeliku* väärtuse, mis tähistab vorminguelementide sidumiste tagastatud väärtuste summat ja mis koguti, kui vorminguelemente kasutati väljamineva dokumendi loomiseks vormingu käitamise ajal, ja mis vastab määratud tingimusele. See tingimus koosneb võtmevahemikust ja võtmeväärtusest. |
| [SumIFs](er-functions-datacollection-sumifs.md) | See funktsioon tagastab *tegeliku* väärtuse, mis tähistab vorminguelementide sidumiste tagastatud väärtuste summat ja mis koguti, kui vorminguelemente kasutati väljamineva dokumendi loomiseks vormingu käitamise ajal, ja mis vastab määratud tingimustele. Iga tingimus koosneb võtmevahemikust ja võtmeväärtusest. |

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)

[Valemikoostaja elektroonilises aruandluses](general-electronic-reporting-formula-designer.md)

[Elektroonilise aruandluse valemi keel](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
