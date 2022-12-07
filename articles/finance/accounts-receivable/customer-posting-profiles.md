---
title: Kliendi sisestusreeglid
description: See artikkel kirjeldab kliendi sisestusprofiile, mis kontrollivad kliendikannete sisestamist pearaamatusse.
author: JodiChristiansen
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04cf5b8656bccde974fb1adfdf830080e2f52436
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799568"
---
# <a name="customer-posting-profiles"></a>Kliendi sisestusreeglid

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab kliendi sisestusprofiile, mis kontrollivad kliendikannete sisestamist pearaamatusse.

## <a name="customer-posting-profiles"></a>Kliendi sisestusreeglid

Kliendi sisestusreeglid lasevad teil määrata pearaamatukontosid ja dokumendisätteid kõigile klientidele, kliendigrupile või ühele kliendile. Neid sätteid kasutatakse müügitellimuste arvete, vabas vormis arvete, projektiarvete, maksetöölehtede, märgukirjade ja viivisearvete loomisel. 

Vaike-sisestusreeglid määratletakse müügireskontro **parameetrite** lehe **vahekaardil Pearaamat ja** Käibemaks. See kaasatakse seejärel automaatselt uute dokumentide päisesse. Saate seda seal muuta, kui on vaja erinevaid sisestusprofiile. 

Organisatsioonid, mis aktsepteerivad klientide ettemakseid, konfigureerivad sageli ettemaksete jaoks teist sisestusreeglit ja lingivad selle parameetrites ettemaksude vaike sisestusreeglina. Lisateavet vt kliendi [ettemaksetest](customer-prepayments.md).

Saate seostada sisestamisdefinitsioonid kande sisestamistüüpidega lehel **Kande sisestamisdefinitsioonid**. Sisestusreeglite asemel kasutatakse sisestusdefinitsioone kliendikannete pearaamatusse sisestamise tegemiseks. Lisateavet vaadake teemast [Sisestamisdefinitsioonid](../general-ledger/posting-definitions.md).

## <a name="creating-a-posting-profile"></a>Sisestusreeglite loomine
Määrake kannete sisestamisel kasutatavad pearaamatukontod, mis kasutavad valitud sisestusreegleid. Valige konto kood ja kui võimalik, siis ka konto või grupi number valitud sisestusreegli jaoks. Sisestusprotsessis leitakse iga kande jaoks sobiv sisestusreegel, otsides kõige sobivamat kontokoodi, kontonumbri või grupi ja numbri kombinatsiooni järgmise prioriteediga.

| Välja Konto kood väärtus | Välja Konto/grupi number väärtus                | Otsingu prioriteet |
|--------------------------|-------------------------------------------------|-----------------|
| Tabel                    | Spetsiaalne kliendi konto                       | 1               |
| Grupp                    | Kliendigrupp, mis on kliendile määratud | 2               |
| Kõik                      | Tühi                                           | 3               |

Kui soovite, et kõigil kliendikannetel oleks sama sisestusr reeglid, seadistage ainult üks sisestusr reeglid, **kus** väljale Konto **kood sisestatakse** kõik. Määrake sisestusreeglite seadistamiseks järgmised väärtused.

<table>
<thead>
<tr>
<th>Väli</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Sisestusreeglid</strong></td>
<td>Tippige sisestusreegli kood. Näiteks saate luua kaks sisestusreeglit, et saada üks kliendi saldode konto riigi valuutas ja teine kliendi saldode konto välisvaluutas. Ühe konto nimeks võite panna Riiklik ja teise konto nimeks Välismaine.</td>
</tr>
<tr>
<td><strong>Kirjeldus</strong></td>
<td>Sisestage sisestusreeglite kirjeldus. Seda kasutatakse üksnes sisestusreeglite paremaks tuvastamiseks nende vaatamisel selle lehel.</td>
</tr>
<tr>
<td><strong>Konto kood</strong></td>
<td>Määrake, kas sisestusreegleid rakendatakse üksikule kliendile, kliendigrupile või kõikidele klientidele.
<ul>
<li><b>Tabel</b> – sisestusreeglid rakenduvad ühele kliendile. Valige kliendikonto väljal <b>Konto/grupi number</b> .</li>
<li><b>Grupp</b> – sisestusreeglid rakenduvad kliendigrupile. Valige kliendigrupp väljal <b>Konto/grupi</b> number.</li>
<li><b>Kõik</b> – sisestusreeglid rakenduvad kõigile klientidele. Jätke väli <b>Konto/grupi number</b> tühjaks.</li>
</ul>
</td>
</tr>
<tr>
<td><strong>Konto/grupi number</strong></td>
<td> <b>Kui</b> väljal Konto kood on <b>valitud</b> väärtus Tabel, saate valida sisestusreeglitega seotud kliendi kontonumbri. Kui <b>grupp</b> on valitud, valige kliendigrupp. Kui on valitud väärtus <b>Kõik</b>, jätke see väli tühjaks.</td>
</tr>
<tr>
<td><strong>Summakonto</strong></td>
<td>Valige põhikonto, mida kasutatakse sisestusreeglitega seotud klientide Müügireskontro kaubanduskontona. See konto on kliendi saldo sisestamistüübi <b></b> konto.</td>
</tr>
<tr>
<td><strong>Maksete likviidsuskonto</strong></td>
<td>Valige likviidsuse <strong>pearaamatukonto</strong> , mida kasutatakse likviidsuse eelarves. See väli kuvatakse ainult siis, kui likviidsuse prognoos on lubatud.</td>
</tr>
<tr>
<td><strong>Käibemaksu ettemaksed</strong></td>
<td><p>Valige ettemaksuna saadud maksete käibemaksu jaoks kasutatav konto.</p>
<p><strong>Märkus.</strong>  Kasutage lehte <b>Müügireskontro parameetrid</b> , et määrata sisestusreeglid, mida kasutatakse, kui makse on märgitud ettemaksuks.</p>
</td>
</tr>
<tr>
<td><strong>Allahindluse konto kohustused</strong></td>
<td>Valige allahindluse passiva pearaamatukonto.</td>
</tr>
<tr>
<td><strong>Märgukirja seeria</strong></td>
<td>Valige märgukirjaseeria identifikaator, mida kasutatakse klientide puhul, kellele on määratud sisestusreeglid.</td>
</tr>
<tr>
<td><strong>Viivise kood</strong></td>
<td>Valige intressi kood, mida kasutatakse intressi arvutamiseks klientide puhul, kellele on määratud sisestusreeglid.</td>
</tr>
</tbody>
</table>

## <a name="posting-examples"></a>Sisestamisnäited

Järgmine tabel näitab vaikimisi sisestamistüüpide näiteid koos näidis põhikontode ja kirjeldustega. Veerg **Deebet/Kreedit** näitab, kas kannet tavaliselt debiteeritakse või krediteeritakse või mõnel juhul saab sisestada kumbki neist. Kliiringukonto **veerg** näitab, et sisestamistüüp on kliiringukonto. See tähendab, et hilisema kande sisestamisel tühistatakse kontole sisestatud summa automaatselt. 

| Sisestamistüüp | Põhikonto näide | Põhikonto nime näide | Konto tüüp | Deebet/krediit | Kliiringukonto | Kirjeldus |
|--------------|----------------------|---------------------------|--------------|--------------|------------------|-------------|
| Kliendi saldo | 130100 | Müügireskontro kaubandus | Vara | Mõlemad | Nr | Määratlege konto summakonto **väljal**.|
| Pole | 110110 | Pangakonto | Vara | Mõlemad | Nr | Määrake maksete likviidsuskonto **väljal põhikonto** . Seda kontot ei kasutata sisestamiseks. Seda kasutatakse ainult likviidsuse prognoosimiseks. |
| Käibemaksu ettemaksed | 202900 | Käibemaksu puhastamine | Kohustus | Mõlemad | Jah | Valige ettemaksuna saadud maksete käibemaksu jaoks kasutatav konto. |
| Passiva allahindluse kontole | 250600 | Viittulu ja allahindlused | Kohustus | Mõlemad | Jah | Valige allahindluse passiva pearaamatukonto.|     

### <a name="table-restrictions"></a>Tabelipiirangud

Valitud sisestusreeglitega kanded määravad, kas kanded tasakaalustatakse automaatselt, kas arvutatakse intress ja väljastatakse märgukirjad. Saate valida ka konto, mida kasutatakse, kui valitud sisestusreeglitega kanded on suletud.

Määrake sisestusreeglite seadistamiseks järgmised väärtused.

| Väli                 | Kirjeldus                                           |
|-----------------------|-------------------------------------------------------|
| Tasakaalustus        | Tehke see valik nende sisestusreeglitega kannete automaatse tasakaalustamise lubamiseks. Kui see tumblerlüliti on tühjendatud, tuleb kanded käsitsi tasakaalustada, kasutades lehte Avatud **kannete** tasakaalustamine või **Kliendimaksete sisestamine** . |
| Viivis          | Tehke see valik, kui neid sisestusreegleid kasutavate kliendikontode puhul tuleks arvestada intressi. Kui see valik on eemaldatud, siis nende klientide puhul intressi ei arvutata.                                           |
| Märgukiri | Tehke see valik, kui neid sisestusreegleid kasutavate kliendikontode puhul tuleks koostada märgukirjad. Kui see valik on eemaldatud, siis nende klientide puhul märgukirju ei koostata.                                                 |
| Sulge             | Valige sisestusreeglid, millele üle minna, kui nende sisestusreeglitega kanded suletakse. Kanne loetakse suletuks, kui see on täielikult tasakaalustatud.             |



Lisateabe saamiseks vt [Kliendimaksete ülevaade](../cash-bank-management/tasks/customer-payment-overview.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
