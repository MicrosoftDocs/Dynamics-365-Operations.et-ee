---
title: "Hilisema kuupäevaga dateeritud tšekid"
description: "Selles artiklis kirjeldatakse postdated kontrolli Microsoft Dynamics 365 operatsioonide toetamine. Hilisema kuupäevaga dateeritud tšekid on tšekid, mis väljastatakse tulevasel kuupäeval maksete tegemise ja vastuvõtmise eesmärgil. Seetõttu ei saa tšekki enne määratud kuupäeva sularahaks vahetada."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 7349771b7f9a1ad4cd5b239f1d10bd3229d2d0df
ms.lasthandoff: 03/31/2017


---

# <a name="postdated-checks"></a>Hilisema kuupäevaga dateeritud tšekid

Selles artiklis kirjeldatakse postdated kontrolli Microsoft Dynamics 365 operatsioonide toetamine. Hilisema kuupäevaga dateeritud tšekid on tšekid, mis väljastatakse tulevasel kuupäeval maksete tegemise ja vastuvõtmise eesmärgil. Seetõttu ei saa tšekki enne määratud kuupäeva sularahaks vahetada.

Microsoft Dynamics 365 toiminguteks toetab täielikult tsükli postdated kontroll Müügireskontro ja Ostureskontro, nagu on näidatud järgmises tabelis.
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
<td>Registreerige hankijale väljastatava hilisema kuupäevaga tšeki üksikasjad. Makse konteerimisel hankija vastutuse on tunnustatud, kuid pangakonto ei ole veel laenu. Selle asemel kasutatakse selleks kliiringukontot.</td>
</tr>
<tr class="odd">
<td>Kliendi hilisema kuupäevaga tšeki registreerimine ja postitamine</td>
<td>Regitreerige kliendilt saadud hilisema kuupäevaga tšeki üksikasjad. Makse sisestamisel Müügireskontro kliendile on krediiti, kuid pangakonto ei ole veel debiteerida. Selle asemel kasutatakse selleks kliiringukontot.</td>
</tr>
<tr class="even">
<td>Registreerida ja sisestada kliendi või hankija asendamine postdated sisse</td>
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
<td>Saate konteeritud postdated sisse sellistes olukordades:-kontrolli tagastatakse panga poolt.
-Kontrolli rakendatakse vale arve.
-Sularahamakse tehakse kontrolli.
</td>
</tr>
<tr class="even">
<td>Postdated sisse maksete peatamist</td>
<td>Saate peatada hankijale väljastatud hilisema kuupäevaga dateeritud tšeki põhjustel, nagu ebapiisavad vahendid, muudatused hankijaga sõlmitud lepingu tingimustes, hankija tarnitud defektsed kaubad või kaupade tagastamine hankijale. Võimalik maksete peatamist kontrollidele, mis ei ole tühi.</td>
</tr>
</tbody>
</table>





