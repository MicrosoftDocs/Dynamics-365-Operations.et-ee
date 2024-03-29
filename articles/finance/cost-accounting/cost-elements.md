---
title: Kuluelemendi dimensioonid
description: Ühe kuluarvestuse tuumsambana kasutatakse kuluelemendi dimensioone, et kategoriseerida ja jälgida, kuhu kulud voolavad.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: twheeloc
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 86d2e431e630afd37ebd1fa3b8f7f553c77bb822
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735166"
---
# <a name="cost-element-dimensions"></a>Kuluelemendi dimensioonid

[!include [banner](../includes/banner.md)]

Ühe kuluarvestuse tuumsambana kasutatakse kuluelemendi dimensioone, et kategoriseerida ja jälgida, kuhu kulud voolavad. 

Kuluelement vastab kulu asjakohasele kaubale kontoplaanis. Põhimõtteliselt võib see olla mis tahes tüüpi element ettevõtte madalaimal tasandil, kuhu kulud saavad voolata. Kuluelemendid kontseptsioonina ulatuvad pearaamatukontost kõigi kulu asjakohaste ressurssideni. Praegu toetab kuluarvestus pearaamatukontosid.

## <a name="two-types-of-cost-elements"></a>Kahte tüüpi kuluelemendid
On kahte tüüpi kuluelemente: esmased kuluelemendid ja teisesed kuluelemendid. Järgmine tabel kirjeldab erinevust nende kahe tüübi vahel.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Esmased kuluelemendid</strong></td>
<td><strong>Sekundaarsed kuluelemendid</strong></td>
</tr>
<tr class="even">
<td>Esmased kuluelemendid tähistavad kulude voogu finantsaruandlusest kuluarvestusse. Kuluelemendi struktuur vastab pearaamatus kasumi ja kahjumi kontostruktuurile, kus kuluelement võib vastata põhikontole. Mitte kõiki põhikontosid ei pea ilmtingimata ärinõuetest sõltuvalt tähistama kuluelementidena. Näiteid esmastest kuluelementidest.
<ul>
<li>Müüdud kaupade kulud</li>
<li>Kaudsed materjalikulud</li>
<li>Personalikulud</li>
<li>Energiakulud</li>
</ul></td>
<td>Teisesed kuluelemendid tähistavad kulude sisevoolu, kuna neid kulusid luuakse ja kasutatakse ainult kuluarvestuses. Neid kasutatakse tagamaks, et kulude allikat saab jälgida. Neid kuluelemente kasutatakse kulude eraldamises ja üldkulude arvutustes. Näiteid teisestest kuluelementidest.
<ul>
<li>Tootmiskulud</li>
<li>Tootmine, materjal ja turustamise üldkulud</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a>Kuluelemendi dimensioonid ja kuluelemendi dimensiooni liikmed
Kuluelemente nimetatakse *kuluelemendi dimensioonideks* . Individuaalseid dimensiooniväärtuseid nimetatakse *kuluelemendi dimensiooni liikmeteks*. Näiteks on teil USA kontoplaani struktuur (COA), mis on teie seadusliku aruandluse alus. Seda COA-d kasutatakse kuluelemendi dimensioonina. Kontosid, mis on esmased kuluelemendid, tähistatakse kuluarvestuses kuluelemendi dimensiooniliikmetena. Järgmine kuvatõmmis näitab näidet põhikontodest kuluelemendi dimensioonina, kus selle tegelikud põhikontod on kuluelemendi dimensiooni liikmed. 

[![Kuvatõmmis põhikontodest kui kuluelemendi dimensioonist.](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)

## <a name="import-cost-element-dimension-members-through-data-connectors"></a>Kuluelemendi dimensiooni liikmete importimine andmekonnektorite kaudu
Kuluelemendi dimensiooni liikmete seadistamise lihtsustamiseks kuluarvestuses saate kasutada andmekonnektoreid, mis on eelnevalt ehitatud või teie järgi kohandatud, et tuua esmased kuluelemendid ühest või mitmest lähtesüsteemist.

## <a name="implementation-considerations"></a>Juurutamise kaalutlused
Kuna kuluelemendid tähistavad kulu üksikasjade madalaimat tasanit, peaksite tagama, et kõik juhtimisaruandluse tegemiseks vajalikud kuluelemendi on kuluelemendi struktuuri juurutamisel kaasatud. See võib olla väljakutse, et leida kulujuhtimise jaoks kuluelementide sobiv number. Tuhandete kuluelementide omamine võib muuta iga kuluelemendi juhtimise keeruliseks. Alternatiivina saate kuluelemente grupeerida ja hallata kulu juhtimist koondtasemel.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
