---
title: ER-i funktsioon NUMSEQVALUE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni NUMSEQVALUE.
author: NickSelin
ms.date: 12/17/2019
ms.topic: article
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
ms.openlocfilehash: c3351360d0c1afca9f828ba4fc935096ddfd67f2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743999"
---
# <a name="numseqvalue-er-function"></a>ER-i funktsioon NUMSEQVALUE

[!include [banner](../includes/banner.md)]

Funktsioon `NUMSEQVALUE` tagastab *stringi* väärtuse, mis tähistab numbriseeria uue loodud väärtuse, põhinedes määratletud numbriseerial, ulatusel ja ulatuse ID-l. Ulatuse ID on võrdne ettevõtte koodiga, mille varustab elektroonilise aruandluse (ER) vormingu käitamise kontekst.

## <a name="syntax-1"></a>Süntaks 1

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a>Süntaks 2

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a>Süntaks 3

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a>Argumendid

`number sequence code`: *string*

Teksti väärtus, mis tähistab numbriseeria koodi, milles on nõutav uus väärtus.

`number sequence record ID`: *Int64*

Väärtus *Int64*, mis tähistab kirje kirde ID-d tabelis NumberSequenceTable, mis sisaldab numbriseeria definitsiooni, milles on nõutav uus väärtus.

`scope type`: *loetelu väärtus*

Loetelu **ERExpressionNumberSequenceScopeType** loetelu väärtus, mis määratleb numbriseeria ulatuse, milles on nõutav uus väärtus. Saadaolevad ulatuse tüübid on **Ühiskasutuses**, **Juriidiline isiku** ja **Ettevõte**.

`scope ID`: *string*

*Stringi* väärtus, mis tuvastab määratud ulatuse tüübi põhjal ulatuse.

## <a name="return-values"></a>Tagastusväärtused

*String*

Tulemiks saadud teksti väärtus.

## <a name="usage-notes"></a>Kasutamise märkused

Määratlege ülatuse tüübi **Ühiskasutuses** jaoks tühi string ulatuse ID-ks.

Määratlege ulatuse tüüpide **Ettevõtte** ja **Juriidiline isik** jaoks ettevõtte kood ulatuse ID-ks. Kui määratlete nendele ulatuse tüüpidele ulatuse ID-ks tühja stringi, kasutatakse praegust ettevõtte koodi.

Kui kasutatakse süntaksit 1, taotletakse ulatuse tüübile **Ettevõte** numbriseeriat ja ettevõtte kood tuleb kontekstist, kus ER-vormingut käitatakse.

## <a name="example-1"></a>Näide 1

Oma ER-vormingus määratlete tüübi *Kasutaja sisendparameeter* andmeallika **AskNumSeq**. See andmeallikas viitab laiendatud andmetüübile (EDT) **Kirjeldus**. Järgmisena määratlete tüübi *Arvutatud väli* andmeallika **NumSeq**. See andmeallikas sisaldab avaldist `NUMSEQVALUE (AskNumSeq)`. Kui kutsutakse andmeallikat **NumSeq**, tagastab see numbriseeria uue loodud väärtuse, mis määrati käitusajal, sisestades selle koodi dialoogiboksi. Numbriseeriat taotletakse ulatuse tüübile **Ettevõte**. Ettevõtte koodi varustab ER-vormingu käitamise kontekst.

## <a name="example-2"></a>Näide 2

Teie mudelivastenduses on määratletud järgmised andmeallikad.

- Tüübi *Tabel* andmeallikas **LedgerParms**. See andmeallikas viitab tabelile LedgerParameters.
- Tüübi *Arvutatud väli* andmeallikas **NumSeq**. See andmeallikas sisaldab avaldist `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.

Kui kutsutakse **NumSeq** andmeallikat, tagastatakse numbriseeria uus loodud väärtus, mis on konfigureeritud pearaamatu parameetrites selle ettevõtte jaoks, mis varustab ER-vormingu käitamise konteksti. See numbriseeria tuvastab kordumatult töölehed ja toimingud partiinumbrina, mis seob kanded omavahel.

## <a name="example-3"></a>Näide 3

Teie mudelivastenduses on määratletud järgmised andmeallikad.

- Teenuse Microsoft Dynamics 365 Finance *loetelu* tüübi andmeallikas **enumScope**. See andmeallikas viitab laiendatud loetelule **ERExpressionNumberSequenceScopeType**.
- Tüübi *Arvutatud väli* andmeallikas **NumSeq**. See andmeallikas sisaldab avaldist `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.

Kui kutsutakse **NumSeq** andmeallikat, tagastatakse numbriseeria **Gene\_1** uus loodud väärtus, mis on konfigureeritud selle ettevõtte jaoks, mis varustab ER-vormingu käitamise konteksti.

## <a name="additional-resources"></a>Lisaressursid

[Muud (ettevõtte domeenipõhised) funktsioonid](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]