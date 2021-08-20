---
title: Hoolduse olek ja edenemise välja vastasmõju
description: Vormi Hooldustellimused väli Edenemine päises näitab kogu teenustellimuse olekut ja Olek näitab hooldustellimuse üksikute ridade olekut.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 210ff82a904e9657d9808a0994c70683e9126622d279aae94e946be0c4f484c1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756048"
---
# <a name="service-status-and-progress-field-interaction"></a>Hoolduse olek ja edenemise välja vastasmõju 

[!include [banner](../includes/banner.md)]


Vormi **Hooldustellimused** väli **Edenemine** hooldustellimuse päises näitab kogu teenustellimuse olekut ja **Olek** näitab hooldustellimuse üksikute ridade olekut.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Edenemine</p></th>
<th><p>1. rea olek</p></th>
<th><p>2. rea olek</p></th>
<th><p>3. rea olek</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Pooleli</strong></p></td>
<td><p><strong>Loodud</strong></p></td>
<td><p><strong>Loodud</strong></p></td>
<td><p><strong>Loodud</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Pooleli</strong></p></td>
<td><p><strong>Tühistatud</strong></p></td>
<td><p><strong>Loodud</strong></p></td>
<td><p><strong>Loodud</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Pooleli</strong></p></td>
<td><p><strong>Loodud</strong></p></td>
<td><p><strong>Tühistatud</strong></p></td>
<td><p><strong>Sisestatud</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Tühistatud</strong></p></td>
<td><p><strong>Tühistatud</strong></p></td>
<td><p><strong>Tühistatud</strong></p></td>
<td><p><strong>Tühistatud</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Sisestatud</strong></p></td>
<td><p><strong>Sisestatud</strong></p></td>
<td><p><strong>Sisestatud</strong></p></td>
<td><p><strong>Sisestatud</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Sisestatud</strong></p></td>
<td><p><strong>Sisestatud</strong></p></td>
<td><p><strong>Tühistatud</strong></p></td>
<td><p><strong>Tühistatud</strong></p></td>
</tr>
</tbody>
</table>


Teenustellimuse edenemine toimub siis, kui kõikidel ridadel on olek **Loodud**; edenemine toimub ka siis, kui mõnel real on olek **Tühistatud** või **Sisestatud**.

Kui teenustellimuse kõik read on märgitud kui **Sisestatud**, on edenemisel olek **Sisestatud**. Kui mõned read on **Sisestatud** ja mõned on **Tühistatud**, on edenemine ikkagi **Sisestatud**.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]