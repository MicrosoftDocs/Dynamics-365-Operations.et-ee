---
title: Kliendi sisestusreeglid
description: Kliendi sisestusreeglid kontrollivad kliendikannete sisestamist pearaamatusse.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: roschlom
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 07acb7ef5565fa4a63607f6828e46c1fcf8110cc
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193614"
---
# <a name="customer-posting-profiles"></a>Kliendi sisestusreeglid

[!include [banner](../includes/banner.md)]

Kliendi sisestusreeglid kontrollivad kliendikannete sisestamist pearaamatusse.

## <a name="customer-posting-profiles"></a>Kliendi sisestusreeglid

Kliendi sisestusreeglid võimaldavad määrata pearaamatukontosid ja dokumendisätteid kõigile klientidele, kliendigrupile või üksikule kliendile. Neid sätteid kasutatakse müügitellimuste, vabas vormis arvete, sularahamaksete, märgukirjade ja viivisearvete loomisel. Mõne kande puhul saate valida sisestusreegli, mis erineb ja on olulisem sellel lehel kannete jaoks seadistatud sisestusreeglitest. 

Vaike-sisestusreeglid määratletakse kiirkaardil Pearaamat ja käibemaks lehel Müügireskontro parameetrid. Vaike-sisestusreeglid lisatakse siis automaatselt uute dokumentide päisesse, kus saate vahetada need vajaduse korral teistsuguste sisestusreeglite vastu.

Saate seostada sisestamisdefinitsioonid kande sisestamistüüpidega lehel Kande sisestamisdefinitsioonid. Sisestamisdefinitsioonid juhivad kliendikannete sisestamist sisestusreeglite asemel pearaamatusse.

## <a name="creating-a-posting-profile"></a>Sisestusreeglite loomine
Määrake kannete sisestamisel kasutatavad pearaamatukontod, mis kasutavad valitud sisestusreegleid. Valige konto kood ja kui võimalik, siis ka konto või grupi number valitud sisestusreegli jaoks. Sisestusprotsessis leitakse iga kande jaoks sobiv sisestusreegel, otsides kõige sobivamat kontokoodi, kontonumbri või grupi ja numbri kombinatsiooni järgmise prioriteediga.

| Välja **Konto kood** väärtus | Välja **Konto/grupi number** väärtus            | Otsingu prioriteet |
|------------------------------|-------------------------------------------------|-----------------|
| **Tabel**                    | Spetsiaalne kliendi konto                       | 1               |
| **Grupp**                    | Kliendigrupp, mis on kliendile määratud | 2               |
| **Kõik**                      | Tühi                                           | 3               |

Kui soovite, et kõigil kliendi kannetel oleksid samad sisestusreeglid, seadistage ainult üks sisestusreegel, valides väljal Konto kood väärtuse Kõik. Määrake sisestusreeglite seadistamiseks järgmised väärtused.

<table>
<thead>
<tr class="header">
<th>Väli</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Sisestusreeglid</strong></td>
<td>Tippige sisestusreegli kood. Näiteks saate luua kaks sisestusreeglit, et saada üks kliendi saldode konto riigi valuutas ja teine kliendi saldode konto välisvaluutas. Ühe konto nimeks võite panna Riiklik ja teise konto nimeks Välismaine.</td>
</tr>
<tr class="even">
<td><strong>Kirjeldus</strong></td>
<td>Sisestage sisestusreeglite kirjeldus. Seda kasutatakse üksnes sisestusreeglite paremaks tuvastamiseks nende vaatamisel selle lehel.</td>
</tr>
<tr class="odd">
<td><strong>Konto kood</strong></td>
<td>Määrake, kas sisestusreegleid rakendatakse üksikule kliendile, kliendigrupile või kõikidele klientidele.
<ul>
<li><strong>Tabel</strong> – sisestusreeglid rakenduvad ühele kliendile. Valige kliendikonto väljal Konto/grupi number.</li>
<li><strong>Grupp</strong> – sisestusreeglid rakenduvad kliendigrupile. Valige kliendigrupp väljal Konto/grupi number.</li>
<li><strong>Kõik</strong> – sisestusreeglid rakenduvad kõigile klientidele. Jätke väli Konto/grupi number tühjaks.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Konto/grupi number</strong></td>
<td>Kui väljal Konto kood on valitud väärtus Tabel, valige sisestusreegliga seotud kliendi konto number. Valiku Grupp korral valige kliendigrupp. Kui on valitud väärtus Kõik, jätke see väli tühjaks.</td>
</tr>
<tr class="odd">
<td><strong>Summakonto</strong></td>
<td>Valige selle pearaamatukonto number, mida kasutatakse antud sisestusreeglitega seotud klientide puhul kliendi summakontona.</td>
</tr>
<tr class="even">
<td><strong>Tasakaalusta konto</strong></td>
<td>Valige likviidsuse planeerimisel kasutatud pearaamatu likviidsuskonto. See väli kuvatakse ainult juhul, kui likviidsuse planeerimine on lubatud.</td>
</tr>
<tr class="odd">
<td><strong>Käibemaksu ettemaksed</strong></td>
<td>Valige ettemaksuna saadud maksete käibemaksu jaoks kasutatav konto.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Paberraha" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Märkus</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lehe Müügireskontro parameetrid abil saate määrata sisestusreeglid, mida kasutada, kui makse on märgitud ettemakseks.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Allahindluse konto kohustused</strong></td>
<td>Valige allahindluse passiva pearaamatukonto.</td>
</tr>
<tr class="odd">
<td><strong>Märgukirja seeria</strong></td>
<td>Valige märgukirjaseeria identifikaator, mida kasutatakse klientide puhul, kellele on määratud sisestusreeglid.</td>
</tr>
<tr class="even">
<td><strong>Viivise kood</strong></td>
<td>Valige intressi kood, mida kasutatakse intressi arvutamiseks klientide puhul, kellele on määratud sisestusreeglid.</td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a>**Tabelipiirangud**

Valitud sisestusreeglitega kanded määravad, kas kanded tasakaalustatakse automaatselt, kas arvutatakse intress ja väljastatakse märgukirjad. Saate valida ka konto, mida kasutatakse, kui valitud sisestusreeglitega kanded on suletud.

Määrake sisestusreeglite seadistamiseks järgmised väärtused.

| Väli                 | Kirjeldus                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tasakaalustus**        | Tehke see valik nende sisestusreeglitega kannete automaatse tasakaalustamise lubamiseks. Kui see valik eemaldada, tuleb kanded käsitsi tasakaalustada, kasutades lehte Avatud kannete tasakaalustamine või Kliendimaksete sisestamine. |
| **Huvi**          | Tehke see valik, kui neid sisestusreegleid kasutavate kliendikontode puhul tuleks arvestada intressi. Kui see valik on eemaldatud, siis nende klientide puhul intressi ei arvutata.                                           |
| **Märgukiri** | Tehke see valik, kui neid sisestusreegleid kasutavate kliendikontode puhul tuleks koostada märgukirjad. Kui see valik on eemaldatud, siis nende klientide puhul märgukirju ei koostata.                                                 |
| **Sulge**             | Valige sisestusreeglid, millele üle minna, kui nende sisestusreeglitega kanded suletakse. Kanne loetakse suletuks, kui see on täielikult tasakaalustatud.                                                                           |



Lisateabe saamiseks vt [Kliendimaksete ülevaade](../cash-bank-management/tasks/customer-payment-overview.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]