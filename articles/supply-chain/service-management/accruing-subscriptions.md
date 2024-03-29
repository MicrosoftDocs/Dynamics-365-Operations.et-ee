---
title: Lisandunud kordustellimused
description: teenustellimuste puhul kogute tulud käsitsi perioodidesse, mis järgnevad kuupäevale, millal kande eest arve esitasite.
author: sorenva
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ff184b24a264e37613b2302a3d92b74e870c5ac
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677334"
---
# <a name="accruing-subscriptions"></a>Lisandunud kordustellimused 

[!include [banner](../includes/banner.md)]


teenustellimuste puhul kogute tulud käsitsi perioodidesse, mis järgnevad kuupäevale, millal kande eest arve esitasite.

Lisandumisperioodid luuakse arve perioodi kohta, mille kordustellimuse tasule määrate, ning lisandumisperioodid põhinevad tellimuse perioodikoodil.

Saate viittulu koguda ja tühistada.

## <a name="reverse-accruals-of-credit-amounts"></a>Kreeditsummade viitvõlad

Kui krediteerite kordustellimuse tasu, mille eest on arve esitatud, siis saate tasu tühistamiseks kasutada kahte meetodit.

  - Saate ükshaaval tagasi pöörata kõik viittulukanded enne, kui loote kandele kreeditarve ettepaneku. See on käsitsimeetod. (käsitsi)

  - Saate viittulu tühistada kuupäeval, millal kreeditarve sisestatakse, või juurdekasvu esialgse sisestamise kuupäeval.

Lisateabe saamiseks vt teemat [Kordustellimuse parameetrid (vorm)](/dynamicsax-2012//subscription-parameters-form).

## <a name="setup-requirements"></a>Nõuete seadistamine

Tulu lisamiseks veenduge, et järgmised andmenõuded on täidetud.

## <a name="account-setup"></a>Konto seadistus

Kontod **Lõpetamata toodang – kordustellimus** ja **Viittulu – kordustellimus** tuleb seadistada moodulis **Projekt**.

Kui sisestate viittulu, siis debiteeritakse viittulu kontolt **Lõpetamata toodang – kordustellimus** ja kontot **Viittulu – kordustellimus** krediteeritakse viittulu summa võrra.

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a>Kontode seadistamine viittulu või kordustellimuse tulu jaoks

1.  Klõpsake valikuid **Projektihaldus ja -arvestus** \> **Seadistus** \> **Sisestamine** \> **Pearaamatu sisestamise seadistus**.

2.  Kontode seadistamiseks klõpsake vahekaarti **Tulukontod** ja valige seejärel **Lõpetamata toodang – kordustellimus** või **Viittulu – kordustellimus**.

## <a name="subscription-group-setup"></a>Kordustellimuste grupi seadistus

Tulu lisamiseks kordustellimuste jaoks peab märkeruut **Tulu lisamine** olema märgitud. Leiate selle kordustellimusega seotud grupi vormilt **Kordustellimuste grupid**. Klõpsake valikuid **Teenuste haldus** \> **Seadistus** \> **Teenuse kordustellimused** \> **Kordustellimuste grupid**.

## <a name="enable-revenue-accrual-on-a-subscription-group"></a>Tulude lisamise võimaldamine kordustellimuste grupi kohta

Klõpsake valikuid **Teenuste haldus** \> **Seadistus** \> **Teenuse kordustellimused** \> **Kordustellimuste grupid**.

## <a name="periods"></a>Perioodid

Seadistada tuleb arveldusperioodi kood. Kui te ei soovi lisada tulu sama ajavahemiku jooksul, mida kasutate arve esitamise puhul, siis tuleb seadistada ka lisandumisperiood.

Järgmine tabel annab ülevaate sellest, milliseid lisandumisperioode saate iga arveldusperioodi kohta seadistada.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Arveldusperiood</p></th>
<th><p>Laekumisperiood</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Aastad</strong></p></td>
<td><ul>
<li><p><strong>Aastad</strong></p></li>
<li><p><strong>Kvartal</strong></p></li>
<li><p><strong>Kuu</strong></p></li>
<li><p><strong>Päev</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Kvartal</strong></p></td>
<td><ul>
<li><p><strong>Kvartal</strong></p></li>
<li><p><strong>Kuu</strong></p></li>
<li><p><strong>Päev</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Kuu</strong></p></td>
<td><ul>
<li><p><strong>Kuu</strong></p></li>
<li><p><strong>Päev</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Nädal</strong></p></td>
<td><ul>
<li><p><strong>Päev</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Päev</strong></p></td>
<td><ul>
<li><p><strong>Päev</strong></p></li>
</ul></td>
</tr>
</tbody>
</table>

Arveldusperioodi seadistamine on üldise kordustellimuse grupi seadistamise kohustuslik osa. Saate otsustada, kas soovite seadistada ka lisandumisperioodi kordustellimuse grupi jaoks. Kui seadistate kordustellimuste grupile lisandumisperioodi, siis soovitatakse seda perioodi väljal **Perioodi kood**. See väli asub vormil **Kordustellimuse tulu lisamine** siis, kui lisate kordustellimuste tulu. Kuid laekumisperiood on kordustellimuste grupi puhul valikuline teave.


> [!NOTE]
> <P>Kasutage järgmist teed, et avada vorm <STRONG>Kordustellimuse tulu lisamine</STRONG>. Klõpsake valikuid <STRONG>Teenuste haldus</STRONG> &gt; <STRONG>Perioodiline</STRONG> &gt; <STRONG>Teenuse kordustellimused</STRONG> &gt; <STRONG>Kordustellimuse tulu lisamine</STRONG>.</P>


## <a name="transactions"></a>Kanded

Saate määrata pearaamatukannete arvu, mis luuakse viittulu sisestamisel. Kordustellimuste puhul saate määrata, kas pearaamatukanded tuleks luua tervikule või iga rea kohta.

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a>Laekumiskannete kohta kuvatavate detailide sisestamise tasandi määramine

1.  Klõpsake valikuid **Projektihaldus ja raamatupidamine** \> **Seadistus** \> **Projektihalduse ja raamatupidamise parameetrid**.

2.  Valige vahekaardi **Finants** väljal **Arve** suvand **Kokku** või **Rida**.


## <a name="see-also"></a>Vt ka

[Kordustellimuse tulu lisamine](accrue-subscription-revenue.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]