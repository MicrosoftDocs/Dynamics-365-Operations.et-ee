---
title: Mis on uut või mida on muudetud rakenduse Dynamics AX versioonis 7.0.1 (mai 2016)
description: Selles artiklis kirjeldatakse rakenduse Microsoft Dynamics AX versiooni 7.0.1 uusi või muutunud funktsioone. See versioon ilmus mais 2016 ja selle number on 7.0.1265.23014.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 4524eb14ff06561ad186cf63654e6a716632a3f4
ms.sourcegitcommit: 4d6ec2b1a9674712e1efb8c46b919d554f21a2b3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2019
ms.locfileid: "2627609"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a>Mis on uut või mida on muudetud rakenduse Dynamics AX versioonis 7.0.1 (mai 2016)

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse rakenduse Microsoft Dynamics AX versiooni 7.0.1 uusi või muutunud funktsioone. See versioon ilmus mais 2016 ja selle number on 7.0.1265.23014.

## <a name="electronic-reporting-er"></a>Elektrooniline aruandlus (ER)

| Mida saate teha? | Miks on see oluline? |
|------------------|------------------------|
| Saate konfigureerida käitusaja dialoogiboksi elektroonilise aruandluse (ER) aruannete kujundamiseks, et kasutajad saaksid soovitud finantsdimensioone valida. | Käitusajal saab kasutaja ER-aruande käitamise dialoogiboksis valida mitu finantsdimensiooni. Valitud finantsdimensioonide üksikasjad kuvatakse koostatava elektroonilises dokumendis. |
| Saate konfigureerida ER-aruande koostamise ajal juurdepääsu mitmele finantsdimensioonile ühe vastenduse abil soovitud andmeallikaga. | Sama elektroonilise aruandluse aruande konfiguratsiooni saab kasutada, et luua elektroonilisi dokumente, mis esitavad kandeandmeid koos finantsdimensioonide üksikasjadega, hoolimata nende finantsdimensioonide arvust, mida valib kasutaja või mis on konfigureeritud praeguse juriidilise isiku või eksemplari jaoks. |
| Saate konfigureerida ER-i aruannet andmete sisestamiseks OPENXML-i töölehe vormingus loodud elektroonilise dokumendi dünaamiliselt loodud veergudesse. | ER-aruanne saab sisestada andmeid OPENXML-töölehele, mis luuakse veergude horisontaalse paljundamise teel. Seetõttu saab sama ER-aruande konfiguratsiooni uuesti kasutada, et koostada elektroonilisi dokumente, millel on erinev arv dünaamiliselt loodud veerge. |
| Saate konfigureerida elektroonilise aruandluse sihtkohti, nii et vormingu väljundtulemus on suunatud konkreetsele sihtkohale: fail, meil või arhiiv (Microsoft SharePointi kaust või Microsoft Azure’i salvestusruum). | Varem, kui käivitasite ER-konfiguratsiooni, kuvati teateväli, mis nõudis kasutaja tegevust faili salvestamiseks või avamiseks. Nüüd saate eelkonfigureerida sihtkoha igale vormingu konfiguratsioonile ja igale väljundi komponendile (kaust või fail) eraldi. Kasutajad, kellel on sobilikud juurdepääsuõigused, võivad sihtkoha sätteid ka käitusajal muuta. |

## <a name="pos--microsoft-dynamics-ax-retail"></a>Kassa – Microsoft Dynamics AX Retail

| Mida saate teha? | Miks on see oluline? |
|------------------|------------------------|
| Kasutage Google Chrome’i brauserit. | Jaemüüjad saavad nüüd käivitada pilvekassa Chrome’i brauserist ja kasutada kõiki funktsioone, mis on saadaval pilvekassa Microsoft Edge’i ja Internet Exploreri versioonis. |

## <a name="financial-reporting"></a>Finantsaruandlus

| Mida saate teha? | Miks on see oluline? |
|------------------|------------------------|
| Saate koostada uuesti finantsaruandluse andmevaka. | Dynamics AX-i andmebaaside liigutamiseks keskkondade vahel või keskkonnale muude invasiivsete muudatuste tegemiseks tuleb finantsaruandluse andmebaasid uuesti luua. Nüüd on olemas Windows PowerShelli skript, mis loob andmebaasi teie eest. |
| Te ei saa enam valida kehtetuid aruandekoosturi valikuid. | Mitu aruandekoosturi valikut, mida kasutati turul olevate Management Reporteri versioonides, ei kehti selle Dynamics AX-i versiooni puhul. Need suvandid olid seotud finantsaruande kujunduse, väljundi ja linkimisega. Need suvandid on kasutajatõrgete vältimiseks finantsaruande kujundajast eemaldatud. |

## <a name="financial-management"></a>Finantshaldus

| Mida saate teha? | Miks on see oluline? |
|------------------|------------------------|
| Saate luua ostureskontro maksete jaoks positiivseid maksefaile. | Positiivseid maksefaile saab luua tšekipettuste vältimiseks. |

## <a name="warehouse-and-production"></a>Ladu ja tootmine

<table>
<thead>
<tr>
<th>Mida saate teha?</th>
<th>Miks on see oluline?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Määratlege lao tööpoliitika, mis juhib töö loomist toodete kogumile konkreetsetes asukohtades.</td>
<td>Laoprotsessid ei hõlma alati tööd. Uut lao tööpoliitikat kasutades saate vältida töö loomist toormaterjali komplekteerimise puhul ja lõpetatud kaupade ladustamist toodete kogumi puhul kindlates asukohtades.</td>
</tr>
<tr>
<td>Määrake, et tootmise väljundi asukoht pole litsentsiplaadiga juhitud.</td>
<td>Saate nüüd määrata, et toote väljundi asukoht pole litsentsiplaadiga juhitud. Näiteks on see funktsioon kasulik, kui ülesvoolu tootmistellimus registreerib kaupade valmisoleku otse asukohas, mis toimib allavoolu tootmistellimuse tootmise sisendkohana.</td>
</tr>
<tr>
<td>Saate toetada kooslusi, mis sisaldavad kaupu, millel on sama kauba erinevad tootedimensioonid.</td>
<td>Kui kasutate tootmises ühte või mitut tootedimensiooni, võib teil olla olukordi, kus soovite toota kauba sama kauba teistsuguse variandi põhjal. Lisateavet leiate <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">sellest ajaveebist</a>.</td>
</tr>
<tr>
<td>Ümmarguse struktuuriga tootmistellimused nende koosluste esimesel tasemel jäetakse materjali ressursiplaanimise koosluse tasandi arvutusest välja.</td>
<td>Pole võimalik määrata õigeid koosluse tasemeid tootevariantidele selliste tootmistellimuste puhul, mis põhjustavad koosluse hierarhias ringviiteid.</td>
</tr>
<tr>
<td>Saate arvutada eraldi koosluse tasemeid materjali ressursiplaanimise ja kuluarvutuse jaoks.
<ul>
<li>Materjali ressursiplaanimiseks arvutatakse koosluse tasemed uues tabelis <strong>ReqItemLevel</strong>. Lõpetatud tootmistellimusi ei arvestata arvutuses.</li>
<li>Tootmiskulu arvutamiseks arvutatakse koosluse tasemed tabelis <strong>InventTable</strong>. Lõpetatud tootmistellimusi arvestatakse arvutuses.</li>
</ul>
</td>
<td>
<ul>
<li>Materjali ressursiplaanimise käivitamisel (nt koondplaanimise plaani koostamisel ja jaotamisel) tuleb arvutada ümber ainult materjali ressursiplaanimiseks kasutatud koosluse tasemed. Teisisõnu: tootmise kuluarvutuse jaoks kasutatud koosluse tasemeid pole vaja arvutada.</li>
<li>Kui kasutatakse kuluarvutuse toiminguid (nt lao sulgemist), tuleb arvutada ümber ainult tootmise kuluarvutuse jaoks kasutatud koosluse tasemed.</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Lisaressursid

[Mis on uus või muudetud?](whats-new-changed.md)

[Uued või värskendatud ülesande juhised (mai 2016)](new-updated-task-guides-available-may-2016.md)
