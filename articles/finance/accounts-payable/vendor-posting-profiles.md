---
title: Hankija sisestusreeglid
description: Hankija sisestusreeglid kontrollivad hankijakannete sisestamist pearaamatusse.
author: abruer
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 022e7d979ca7572bb824bc5248fec8c0b3c283d0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248155"
---
# <a name="vendor-posting-profiles"></a>Hankija sisestusreeglid

[!include [banner](../includes/banner.md)]

Hankija sisestusreeglid kontrollivad hankijakannete sisestamist pearaamatusse.

<a name="vendor-posting-profiles"></a>Hankija sisestusreeglid
-----------------------

Hankija sisestusreeglid võimaldavad määrata pearaamatukontosid ja dokumendisätteid kõigile hankijatele, hankijagrupile või üksikule hankijale. Neid sätteid kasutatakse ostutellimuste, hankija arvete ja sularahamaksete loomisel. Mõne kande puhul saate valida sisestusreegli, mis erineb ja on olulisem sellel lehel kannete jaoks seadistatud sisestusreeglitest. Vaike-sisestusreeglid määratletakse kiirkaardil **Pearaamat ja käibemaks** lehel **Ostureskontro parameetrid**. Vaike-sisestusreeglid lisatakse siis automaatselt uute dokumentide päisesse, kus saate need vajaduse korral teistsuguste sisestusreeglite vastu vahetada.

Saate seostada sisestamisdefinitsioonid kande sisestamistüüpidega lehel **Kande sisestamisdefinitsioonid**. Sisestamisdefinitsioonid juhivad hankija kannete sisestamist sisestusreeglite asemel pearaamatusse.

## <a name="creating-a-posting-profile"></a>Sisestusreeglite loomine
### <a name="setup"></a>**Häälestus**

Määrake kannete sisestamisel kasutatavad pearaamatukontod, mis kasutavad valitud sisestusreegleid. Valige konto kood ja kui võimalik, siis ka konto või grupi number valitud sisestusreegli jaoks. Sisestusprotsessis leitakse iga kande jaoks sobiv sisestusreegel, otsides kõige sobivamat kontokoodi, kontonumbri või grupi ja numbri kombinatsiooni järgmise prioriteediga.

| Välja **Konto kood** väärtus | Välja **Konto/grupi number** väärtus        | Otsingu prioriteet |
|------------------------------|---------------------------------------------|-----------------|
| **Tabel**                    | Konkreetse hankija konto                     | 1               |
| **Grupeeri**                    | Hankijale määratud hankijagrupp | 2               |
| **Kõik**                      | Tühi                                       | 3               |

Kui soovite, et kõigil hankija kannetel oleksid samad sisestusreeglid, seadistage ainult üks sisestusreegel, valides väljal **Konto kood** väärtuse **Kõik**. Määrake sisestusreeglite seadistamiseks järgmised väärtused.

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
<td>Tippige sisestusreegli kood. Näiteks saate luua kaks sisestusreeglit, et saada üks hankijasaldode konto riigi valuutas ja teine hankijasaldode konto välisvaluutas. Ühe konto nimeks võite panna Riiklik ja teise konto nimeks Välismaine.</td>
</tr>
<tr class="even">
<td><strong>Kirjeldus</strong></td>
<td>Sisestage sisestusreeglite kirjeldus.</td>
</tr>
<tr class="odd">
<td><strong>Konto kood</strong></td>
<td>Määrake, kas sisestusreeglit rakendatakse kindlale hankijale, hankijagrupile või kõikidele hankijatele.
<ul>
<li><strong>Tabel</strong> – sisestusreeglid rakenduvad ühele hankijale. Valige hankija konto väljal <strong>Konto/grupi number</strong>.</li>
<li><strong>Grupp</strong> – sisestusreeglid rakenduvad hankijagrupile. Valige hankijagrupp väljal <strong>Konto/grupi number</strong>.</li>
<li><strong>Kõik</strong> – sisestusreeglid rakenduvad kõigile hankijatele. Jätke väli <strong>Konto/grupi number</strong> tühjaks.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Konto/grupi number</strong></td>
<td>Kui väljal <strong>Konto kood</strong> on valitud väärtus <strong>Tabel</strong>, valige sisestusreegliga seotud hankija konto number. Kui on valitud väärtus <strong>Grupp</strong>, valige hankijagrupp. Kui on valitud väärtus <strong>Kõik</strong>, jätke see väli tühjaks.</td>
</tr>
<tr class="odd">
<td><strong>Summakonto</strong></td>
<td>Valige selle pearaamatukonto number, mida kasutatakse antud sisestusreeglitega seotud hankijate puhul summakontona. Märgitakse parameeter <strong>Ära luba käsitsi sisestamist</strong>. Kui eemaldate seejärel selle konto sisestusreeglitest, kinnitage seadistus <strong>Ära luba käsitsi sisestamist</strong> lehel <strong>Põhikontod</strong>. 
<p><strong>Märkus</strong>Kui lehel <strong>Pearaamatu parameetrid</strong> on valitud nupp <strong>Kasuta sisestamisdefinitsioone</strong>, kasutatakse hankija arvete puhul summakonto asemel kande sisestamisdefinitsiooni.</p>
</td>
</tr>
<tr class="even">
<td><strong>Tasakaalusta konto</strong></td>
<td>Valige likviidsuse planeerimisel kasutatud pearaamatu likviidsuskonto. See väli on saadaval ainult siis, kui on lubatud likviidsuse planeerimine.</td>
</tr>
<tr class="odd">
<td><strong>Käibemaksu ettemaksed</strong></td>
<td>Valige ettemaksuna saadud maksete käibemaksu jaoks kasutatav konto.
<p><strong>Märkus.</strong>Sisestusreegel, mida kasutatakse, kui ettemakseks märgitud makse on valitud lehel <strong>Ostureskontro parameetrid</strong> ala <strong>Pearaamat ja käibemaks</strong> väljal <strong>Sisestusreeglid</strong> <strong>Ettemaksu töölehekandega</strong>.</p>
</td>
</tr>
<tr class="even">
<td><strong>Saabumine</strong></td>
<td>Valige pearaamatukonto, kuhu sisestatakse teave kinnitamata hankija arvete kohta. Teave sisestatakse arveregistri töölehele. Näiteks kasutaja sisestab kõige põhilisema teabe hankija arvete kohta, nii nagu need on vastu võetud arveregistrisse. Arveregistri sisestamisel sisestatakse kanded sellele väljale ja väljale <strong>Vastaskonto</strong> sisestatud kontole. Kui arved kinnitatakse, kantakse võlg saabumiskontolt üle hankija summakontole.</td>
</tr>
<tr class="odd">
<td><strong>Vastaskonto</strong></td>
<td>Valige pearaamatukonto, mida kasutatakse arveregistri kaudu uuendatavate kinnitamata hankijaarvete vastaskontona. Vastaskonto toimib saabumiskontodele sisestatud kannete vastaskontona. Konto sisaldab seetõttu veel kinnitamata hankija oste.</td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a>**Tabelipiirangud**

Valitud sisestusreeglitega kanded määravad, kas kanded tasakaalustatakse automaatselt, kas arvutatakse intress ja väljastatakse märgukirjad. Saate valida ka konto, mida kasutatakse, kui valitud sisestusreeglitega kanded on suletud.

Määrake sisestusreeglite seadistamiseks järgmised väärtused.

| Väli          | Kirjeldus                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tasakaalustus** | Tehke see valik nende sisestusreeglitega kannete automaatse tasakaalustamise lubamiseks. Kui see valik eemaldada, tuleb kanded käsitsi tasakaalustada, kasutades lehte **Avatud kannete tasakaalustamine**. |
| **Tühista**     | Tehke see valik, kui soovite, et saaksite nende sisestusreeglitega kandeid tühistada.                                                                                                               |
| **Sulge**      | Valige sisestusreeglid, millele üle minna, kui nende sisestusreeglitega kanded suletakse. Kanne loetakse suletuks, kui see on täielikult tasakaalustatud.                                       |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]