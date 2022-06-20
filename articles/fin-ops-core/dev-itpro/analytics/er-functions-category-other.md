---
title: ER-i funktsioonide loend ettevõtte domeenipõhises kategoorias
description: See artikkel annab teavet äridomeenile omaste funktsioonide kohta, mida toetab elektrooniline aruandlus (ER).
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
ms.openlocfilehash: d9df826dcc0b672977d4d8af1feb985ab9a0ab7d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879945"
---
# <a name="list-of-er-functions-in-the-business-domainspecific-category"></a>ER-i funktsioonide loend ettevõtte domeenipõhises kategoorias

[!include [banner](../includes/banner.md)]

Elektroonilise aruandluse (ER) domeenispetsiifilisi Microsoft Dynamics funktsioone saab kasutada 365 Finantside rakendusse omaste arvutuste ja andmepääsu taotluste esitamiseks. See artikkel annab nende funktsioonide kokkuvõtte.

## <a name="list-of-supported-functions"></a>Toetatud funktsioonide loend

| Funktsioon| Kirjeldus |
|---------|-------------|
| [CH_Bank_Mod_10](er-functions-other-chbankmode10.md) | See funktsioon tagastab *stringi* väärtuse, mis tähistab kreeditori viidet MOD10 avaldisena, mis põhineb määratud arve numbri numbritel. |
| [CN_GBT_AdditionalDimensionID](er-functions-other-cngbtadditionaldimensionid.md) | See funktsioon tagastab *stringi* väärtuse, mis tähistab ühte finantsdimensiooni ID-d, mis on määratud stringist võetud. Määratud string esitab kõik dimensioonid komadega eraldatud ID-de loendina. |
| [ConvertCurrency](er-functions-other-convertcurrency.md) | See funktsioon tagastab *tegeliku* väärtuse, mis kajastab määratud rahasumma määratud lähtevaluutast määratud sihtvaluutaks konverteerimise tulemust, kasutades määratud kuupäeval määratud ettevõtte sätteid. |
| [CurCredRef](er-functions-other-curcredref.md) | See funktsioon tagastab *stringi* väärtuse, mis tähistab kreeditori viidet, mis põhineb määratud arve numbri numbritel. |
| [FA_Balance](er-functions-other-fabalance.md) | See funktsioon tagastab *konteineri (kirje)* väärtuse, mis koosneb põhivara saldo andmetest määratud põhivara kauba, väärtusmudeli koodi, aruandeaasta ja aruandluse kuupäeva kohta. |
| [FA_Sum](er-functions-other-fasum.md) | See funktsioon tagastab *konteineri (kirje)* väärtuse, mis koosneb põhivara summade andmetest määratud põhivara kauba, väärtusmudeli koodi ja kuupäevade perioodi kohta. |
| [GetCurrentCompany](er-functions-other-getcurrentcompany.md) | See funktsioon tagastab *stringi* väärtuse, mis tähistab juriidilise isiku (ettevõtte) koodi, kuhu kasutaja on praegu sisse loginud. |
| [ISOCredRef](er-functions-other-isocredref.md) | See funktsioon tagastab *stringi* väärtuse, mis tähistab Rahvusvahelise Standardiorganisatsiooni (ISO) kreeditori viidet määratud arve numbri arvude ja tähestikus olevate sümbolite alusel. |
| [IsValidCharacterISO7064](er-functions-other-isvalidchariso7064.md) | See funktsioon tagastab *kahendmuutuja* väärtuse **TRUE**, kui määratud string on kehtiv rahvusvaheline pangakonto number (IBAN). Muidu tagastab see *kahendväärtuse* **VÄÄR**. |
| [Mod_97](er-functions-other-mod97.md) | See funktsioon tagastab *stringi* väärtuse, mis tähistab kreeditori viidet MOD97 avaldisena, mis põhineb määratud arve numbri numbritel. |
| [NumSeqValue](er-functions-other-numseqvalue.md) | See funktsioon tagastab *stringi* väärtuse, mis tähistab numbriseeria uue loodud väärtuse, põhinedes määratletud numbriseerial, ulatusel ja ulatuse ID-l. Ulatuse ID on võrdne ettevõtte koodiga, mille varustab ER-vormingu käitamise kontekst. |
| [RoundAmount](er-functions-other-roundamount.md) | See funktsioon tagastab *tegeliku* väärtuse, mis tähistab määratud summa määratud kümnendkohtade arvule määratud ümardamisreegli kohaselt ümardamise tulemust. |
| [TableName2ID](er-functions-other-tablename2id.md) | See funktsioon tagastab määratud tabeli nime tabeli ID numbrilise esituse *täisarvulise* väärtusena. |

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)

[Valemikoostaja elektroonilises aruandluses](general-electronic-reporting-formula-designer.md)

[Elektroonilise aruandluse valemi keel](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]