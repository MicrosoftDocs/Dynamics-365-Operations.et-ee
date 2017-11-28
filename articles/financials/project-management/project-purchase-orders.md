---
title: Projekti ostutellimused
description: "See artikkel kirjeldab erinevaid meetodeid, mille abil saate luua projekti ostutellimusi. Kasutatav meetod sõltub ostutellimuse eesmärgist ja sellest, millal ostetud kaupu tarbitakse ja nende eest projektile kulud arvestatakse."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0cf1effee6fd9e08b85d30f90c5e83aa77bc22cc
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="purchase-orders-for-a-project"></a>Projekti ostutellimused

[!include[banner](../includes/banner.md)]


See artikkel kirjeldab erinevaid meetodeid, mille abil saate luua projekti ostutellimusi. Kasutatav meetod sõltub ostutellimuse eesmärgist ja sellest, millal ostetud kaupu tarbitakse ja nende eest projektile kulud arvestatakse.

Microsoft Dynamics 365 for Finance and Operations, Enterprise editionis saate kasutada projekti ostutellimuste loomiseks mitut meetodit. Kasutatav meetod sõltub ostutellimuse eesmärgist, sellest, millal ostetud kaupu tarbitakse ja millal ostetud kaupade eest projektile kulud arvestatakse.

### <a name="methods-for-creating-a-purchase-order"></a>Ostutellimuse loomise meetodid

Saate projekti haldamise ja raamatupidamise ostutellimuse loomiseks kasutada üht järgmistest meetoditest. Ostutellimuse eesmärk määratleb, millal ostutellimust tarbitakse, ning seega ka selle, millal kaubad projekti kuludesse kantakse.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Meetod</th>
<th>Eesmärk</th>
<th>Kaupade tarbimine</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ostutellimuse loomine otse projektist.</td>
<td>Kasutage seda meetodit välishankijalt kaupade ostmiseks projektis tarbimiseks. Ostutellimust saab luua kahel viisil.
<ul>
<li>Otse projekti kaudu. Sel juhul on projekt juba ostutellimuse jaoks määratletud.</li>
<li>Liikudes projekti ostutellimusele. Valida tuleb nii hankija kui projekt, mille jaoks ostutellimus luuakse.</li>
</ul></td>
<td>Kaubad tarbitakse kui hankijaarve on uuendatud.</td>
</tr>
<tr class="even">
<td>Ostutellimuse loomine müügitellimuse põhjal</td>
<td>Kasutage seda meetodit kaupade ostmiseks projekti müügitellimuse loomisel.</td>
<td>Kaubad tarbitakse siis, kui kliendile esitatakse müügitellimuse arve.</td>
</tr>
<tr class="odd">
<td>Ostutellimuse loomine kaubavajaduse põhjal</td>
<td>Kasutage seda meetodit kaupade ostmiseks projekti kaubavajaduse loomisel.</td>
<td>Kaubad tarbitakse kui kaubavajaduse saateleht on uuendatud.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Hankijaarve või saatelehe uuendamisel palutakse teil uuendada ka kaubavajaduse saateleht.

Lisateabe saamiseks vt [Kaubavajaduse ostutellimuse kaupade vastuvõtt](tasks/receive-items-purchase-order-item-requirement.md).


