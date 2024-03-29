---
title: Hilisema kuupäevaga dateeritud tšekid
description: Selles artiklis antakse teavet hilisema kuupäevaga tšekkide toe kohta. Pärast kuupäevaga dateeritud tšekke väljastatakse maksete tegemiseks ja saamiseks tulevasel kuupäeval.
author: angelad116
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPostDatedChecks, CustPostDatedChecks
audience: Application User
ms.reviewer: kfend
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4d32ed9de66bc92e17c5515a4266f41aaeb9f2c1
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151357"
---
# <a name="postdated-checks"></a>Hilisema kuupäevaga dateeritud tšekid

[!include [banner](../includes/banner.md)]

Selles artiklis antakse teavet hilisema kuupäevaga tšekkide toe kohta. Hilisema kuupäevaga dateeritud tšekid on tšekid, mis väljastatakse tulevasel kuupäeval maksete tegemise ja vastuvõtmise eesmärgil. Seetõttu ei saa tšekki enne määratud kuupäeva sularahaks vahetada.

Dynamics 365 Finance toetab järelndekseeritud tšekkide täielikku haldustsüklit nii müügireskontros kui ka ostureskontros, nagu näha järgmises tabelis.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Stsenaarium</th>
<th>Üksikasjad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Hilisema kuupäevaga tšekkide seadistamine</td>
<td>Peate seadistama uue makseviisi ja määrama makserutiini väljastatud tšekkide, vastuvõetud tšekkide ja kinnipeetava maksu kliiringukontodele.</td>
</tr>
<tr class="even">
<td>Registreeri ja postita hankija hilisema kuupäevaga tšekk</td>
<td>Registreerige hankijale väljastatava hilisema kuupäevaga tšeki üksikasjad. Kui makse on sisestatud, siis tuvastatakse hankija kohustus, kuid pangakonto ei ole veel krediteeritud. Selle asemel kasutatakse selleks kliiringukontot. </td>
</tr>
<tr class="odd">
<td>Kliendi hilisema kuupäevaga tšeki registreerimine ja postitamine</td>
<td>Regitreerige kliendilt saadud hilisema kuupäevaga tšeki üksikasjad. Kui makse on sisestatud, siis on kliendi nõue krediteeritud, kuid pangakontot ei ole veel debiteeritud. Selle asemel kasutatakse selleks kliiringukontot.</td>
</tr>
<tr class="even">
<td>Registreerige ja postitage kliendi või hankija hilisema kuupäevaga asendustšekk.</td>
<td>
Kui teie algne tšekk hankijale või kliendilt on kadunud või kahjustatud, siis saate hankijale väljastada hilise kuupäevaga dateeritud asendustšeki. Tšeki üksikasjade registreerimisel lisage viide esialgsele tšekile ja näidake, et uus tšekk on originaali asendaja. Asendustšeki saate ka sisestada.</td>
</tr>
<tr class="odd">
<td>Kliendi hilisema kuupäevaga tšeki ülekandmine hankijale</td>
<td>Kui saate kliendilt hilisema kuupäevaga dateeritud tšeki, saate tšeki hankijale maksena üle kanda.</td>
</tr>
<tr class="even">
<td>Kliendi või hankija hilisema kuupäevaga tšeki tasakaalustamine</td>
<td>Tasakaalustage hilise kuupäevaga tšekk, mis sisestatakse kliendi või hankija vahekontole, kui tšekk lõpuks valmis on. Tšeki tasakaalustamisel pank lõpuks debiteerib või krediteerib varem kasutatud kliiringukonto.</td>
</tr>
<tr class="odd">
<td>Hankija hilisema kuupäevaga tšeki tühistamine</td>
<td>Sisestatud hilisema kuupäevaga tšeki saate tühistada järgmistes olukordades. - Pank tagastab tšeki.
- Tšekk on rakendatud valele arvele.
- Tšeki põhjal tehakse sularahamakse.
  </td>
  </tr>
  <tr class="even">
  <td>Hilisema kuupäevaga tšeki makse peatamine</td>
  <td>Saate peatada hankijale väljastatud hilisema kuupäevaga dateeritud tšeki põhjustel, nagu ebapiisavad vahendid, muudatused hankijaga sõlmitud lepingu tingimustes, hankija tarnitud defektsed kaubad või kaupade tagastamine hankijale. Makse saate peatada ainult tasaarvestamata tšekkide puhul.</td>
  </tr>
  </tbody>
  </table>



Lisateavet vt järgmistest teemadest:

[Hilisema kuupäevaga tšekkide seadistamine](tasks/set-up-postdated-checks.md)

[Kliendi hilisema kuupäevaga tšeki registreerimine ja sisestamine](tasks/register-post-postdated-check-customer.md)

[Kliendi hilisema kuupäevaga tšeki tasakaalustamine](tasks/settle-postdated-check-customer.md)

[Hankija hilisema kuupäevaga tšeki registreerimine ja sisestamine](tasks/register-post-postdated-check-vendor.md) 

[Hankija hilisema kuupäevaga tšeki tasakaalustamine](tasks/settle-postdated-check-vendor.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
