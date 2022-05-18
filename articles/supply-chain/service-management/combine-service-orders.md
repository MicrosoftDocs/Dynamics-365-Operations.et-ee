---
title: Teenuse tellimuste ühendamine
description: Saate hooldustellimusi ühendada.
author: sorenva
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
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f89c60561746ac9f1c2e9d611089bfac69089081
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676771"
---
# <a name="combine-service-orders"></a>Teenuse tellimuste ühendamine   

[!include [banner](../includes/banner.md)]


Kui loote hooldustellimuse read automaatselt vormil **Hoolduslepped**, saate valida ühe järgmistest suvanditest, et määrata, kuidas neid grupeerida.

  - **Hooldusleppe alusel**

  - **Hooldustoimingu alusel**

  - **Töövõtja alusel**

  - **Teenuse objekti alusel**

## <a name="example"></a>Näide

Loote hooldusleppe alguskuupäevaga 31.03.2007. Määrate väljal **Hooldustellimuste ühendamine** valiku **Teenuse objekti alusel**. Seejärel saate luua järgmised teenuselepingu read:

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Lepperea number</p></th>
<th><p>Kande tüüp</p></th>
<th><p>Kirjeldus</p></th>
<th><p>Intervall</p></th>
<th><p>Teenuse objekt</p></th>
<th><p>Alguskuupäev</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p><strong>Tund</strong></p></td>
<td><p>SAL1</p></td>
<td><p>Iganädalane</p></td>
<td><p>X-1</p></td>
<td><p>1.04.2007</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p><strong>Tund</strong></p></td>
<td><p>SAL2</p></td>
<td><p>Üle nädala</p></td>
<td><p>X-2</p></td>
<td><p>1.04.2007</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p><strong>Tund</strong></p></td>
<td><p>SAL3</p></td>
<td><p>Iganädalane</p></td>
<td><p>X-2</p></td>
<td><p>1.04.2007</p></td>
</tr>
</tbody>
</table>


Te ei määra kellaaja aknaid ühelegi teenuseleppe reale. Seega ei liigu hooldustellimuse read arvutatud päevalt, millele nad langevad.

Järgmiseks loote hooldustellimuse read vormist **Hooldustellimuste loomine** alates 01.04.2007 kuni 30.04.2007.

Kokku luuakse 10 teenusetellimust. Kuna teie valitud kombineeritud säte oli **Teenuse objekti alusel**, on kõigil loodud hooldustellimustel üksnes hooldustellimuse read ühe konkreetse hooldusobjektiga. Hooldustellimuse read, mis luuakse hooldusleppest ja millel on sama hoolduskuupäev ja hooldusobjekt, kombineeritakse samale hooldustellimusele.


> [!NOTE]
> <P>Käesolevas näites pole kalendris, mis on määratud vormis <STRONG>Teenuste halduse parameetrid</STRONG>, suletud päevi.</P>



Hooldustellimuse ridade edasine grupeerimine hooldustellimustesse toimub hooldusleppe ridadel määratud kellaaja akna kohaselt.

## <a name="see-also"></a>Vt ka

[Hooldustellimuste loomine automaatselt](create-service-orders-automatically.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]