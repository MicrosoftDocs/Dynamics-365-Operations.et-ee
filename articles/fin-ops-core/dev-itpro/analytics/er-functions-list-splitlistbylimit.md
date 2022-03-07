---
title: ER-i funktsioon SPLITLISTBYLIMIT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni SPLITLISTBYLIMIT.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 52351c131480119ce9fb98a75307ebf6026cb12b9977e8b4236d3a24ef6a140e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744430"
---
# <a name="splitlistbylimit-er-function"></a>ER-i funktsioon SPLITLISTBYLIMIT

[!include [banner](../includes/banner.md)]

Funktsioon `SPLITLISTBYLIMIT` jaotab määratud loendi alamloendite (partiide) uueks loendiks. Iga partii kirjete arv arvutatakse dünaamiliselt. Funktsioon tagastab tulemuse uue *kirjete loendi* väärtusena, mis koosneb partiidest.

## <a name="syntax"></a>Süntaks

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a>Argumendid

`list`: *kirjete loend*

Andmetüübi *Kirjete loend* andmeallika kehtiv tee.

`limit value`: *täisarv* või *tegelik*

Piirangu maksimaalne väärtus, mida kasutatakse algse loendi partiideks tükeldamiseks.

`limit source`: *väli*

Tüübi *Täisarv* või *Tegelik* välja kehtiv tee määratud loendis. Selle välja väärtus määratleb sammu, millal kogusummat suurendatakse.

## <a name="return-values"></a>Tagastusväärtused

*Kirjete loend*

Saadud kirjete loend.

## <a name="usage-notes"></a>Kasutamise märkused

Tagastatav partiide loend sisaldab järgmisi elemente.

- **Väärtus**: *loend*

    Kirjete loend, mis kuuluvad praegusesse partiisse.

- **BatchNumber**: *täisarv*

    Praeguse partii number tagastatud loendis.

Piirangut ei rakendata algse loendi üksikule üksusele, kui piirallikas ületab määratud piirangut.

## <a name="example"></a>Näide

Järgmine joonis näitab elektroonilise aruandluse (ER) vormingut.

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

Järgmisel joonisel on näidatud vormingu puhul kasutatud andmeallikad.

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

Järgmisel joonisel on näidatud vormingu käitamise tulemus. Sel juhul on väljund tarbekaupade lame loend.

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

Järgmistes näidetes on sama vormingut kohandatud nii, et see esitab tarbekaupade loendi partiidena, kui üksik partii peab sisaldama tarbekaupu ja kogukaal ei tohi ületada piirangut 9.

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

Järgmisel joonisel on näidatud kohandatud vormingu käitamise tulemus.

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> Piirangut ei rakendata algse loendi viimasele üksusele, kuna selle piirangu allika (**mass**) väärtus (**11**) ületab määratletud piirangut (**9**). Aruande loomisel alamloendite ignoreerimiseks kasutage vastavalt vajadusele kas funktsiooni `WHERE` või vastava vormingu elemendi avaldist **Lubatud**.

## <a name="additional-resources"></a>Lisaressursid

[Loendi funktsioonid](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]