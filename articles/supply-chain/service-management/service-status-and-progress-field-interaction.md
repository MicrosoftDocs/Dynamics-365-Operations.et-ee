---
title: "Hoolduse olek ja edenemise välja vastasmõju"
description: "Vormi Hooldustellimused väli Edenemine päises näitab kogu teenustellimuse olekut ja Olek näitab hooldustellimuse üksikute ridade olekut."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 51ef39266e8de00488954918568d00a297a9b50a
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

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

  



