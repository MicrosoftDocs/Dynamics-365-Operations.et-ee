---
title: Konsolideerimise impordivorming
description: Selles teemas esitatakse üksikasjalikku teavet impordivormingu kohta, mida kasutatakse mitmelt juriidiliselt isikult finantsandmete konsolideerimisel.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 5bea69d72ac93d29ae67dd6d762e1376d9a282f0
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735779"
---
# <a name="import-format-for-consolidation"></a>Konsolideerimise impordivorming

[!include [banner](../includes/banner.md)]

Selles teemas esitatakse üksikasjalikku teavet impordivormingu kohta, mida kasutatakse mitmelt juriidiliselt isikult finantsandmete konsolideerimisel. Impordivorming tuleb salvestada tekstifailina (.txt).

## <a name="import-format"></a>Impordivorming

Järgmises tabelis on toodud impordivorming, mida peate kasutama impordi ajal konsolideerimise käigus.

| Kirjete tabel | Vorming | Märkmed |
|--------------|---------|-------|
| 1            | 170150, Goodwill, 4 | <ul><li>Kirjete tabel</li><li>Allika põhikonto ID</li><li>Põhikonto rida</li><li>Põhikonto tüüp</li></ul> |
| 2            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>Põhikonto ID</li><li>Kande kuupäev</li><li>Finantsperioodi tüüp (**0** = avamine, **1** = kasutamine ja **2** = sulgemine)</li><li>Kande valuuta</li><li>Deebet või kreedit (**0** = deebet ja **1** = kreedit)</li><li>Sisestamiskiht</li><li>Kandesummad</li><li>Kogus</li><li>Kohalik RecID (kande mitmetähenduslik, kordumatu int64 väärtus)</li></ul> |
| 3            | USMF0000009, 2017/01/01, FY2017, 1, 2017,01,01, 602200, USD, 6053.6.0 | <ul><li>Kirje number (eelarve päise kande number)</li><li>Eelarve päise vaikekuupäev</li><li>Eelarve mudeli ID</li><li>Eelarve tüüp (**1 - algne eelarve**, **2** - ülekanne, **3** - revisjon, **4** - pandiõigused, **5** eelpanddiõigused, **6** - ülekangtav eelarve, **7** – projekt, **8** põhivarad, **9** - nõudluse prognoos, **10** - tarneprognoos, **11** - ülekantavad eelarved, **12** - esialgne eelarve.)</li><li>Rea kuupäev</li><li>Rea põhikonto ID</li><li>Rea valuutakood</li><li>Rea summa kande valuutas</li><li>Rea eelarvetüübi loetelu täisarvuline väärtus (kulu või tulu)</li></ul> |
| 4            | DEMF | RecordCompany on juriidilisest isikust allikas. |
| 5            | 110130, 2015/01/01, 1, USD, 0,0,80699.39,0,1 | <ul><li>Põhikonto ID</li><li>Kande kuupäev</li><li>Eelarveprioodi tüüp (0 avamine, 1 kasutamine ja 2 sulgemine)</li><li>Kande valuuta</li><li>Deebet või kreedit (0 deebeti jaoks ja 1 kreediti jaoks)</li><li>Sisestamiskiht</li><li>Kandesumma</li><li>Kogus</li><li>Kohalik recid (kande mitmetähenduslik, kordumatu int64 väärtus)</li></ul>  |
| 6            | BusinessUnit, 1 osakond, 2 | Finantsdimensiooni atribuudid, mis on määratletud segmendi järjestuses.<p>Saate kasutada lehte **Eksport**, et kontrollida atribuutide määratlemist.</p> |
| 7            | 002,1,658 | <ul><li>Finantsdimensiooni väärtus</li><li>Finantsdimensioon kui indeks, mis on esitatud väljal RecordDimensions</li><li>Mitmetähenduslik, kordumatu kirje ID, mis on seotud kordumatu kirje ID-ga väljal RecordTrans või RecordTrans2</li></ul> |
| 8            | 002,1,1 | <ul><li>Dimensiooniväärtused, mis on seotud kandega väljal RecordBudget</li><li>Finantsdimensioon kui indeks, mis on esitatud väljal RecordDimensions</li><li>Mitmetähenduslik reakirje ID, mis on vastavuses faili kanderidade järjestusega</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
