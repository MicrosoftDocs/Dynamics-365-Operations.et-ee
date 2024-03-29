---
title: Arve töötlemine
description: See artikkel annab teavet arve töötlemise kohta Ida-Euroopa jaoks.
author: EvgenyPopovMBS
ms.date: 02/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters, VendParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia, Italy
ms.author: epopov
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: edb50ddebeca18653a318596e9c291a3f3df6d9c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848444"
---
# <a name="invoice-processing"></a>Arve töötlemine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab lühidalt mõningaid riigispetsiifilisi stsenaariume, nt EL-sisest lisaväärtusmaksu (VAT) ja viitmaksu. Mõne Euroopa riigi seadusenõuded mõjutavad arveldusprotsessi. See artikkel annab ka teavet selle kohta, kuidas kliendi- ja hankijaarveid nende riikide jaoks töödeldakse. 
<table>
<thead>
<tr>
<th>Stsenaarium</th>
<th>Riigid</th>
<th>Funktsioonimuudatuste kirjeldus</th>
</tr>
</thead>
<tbody>
<tr>
<td> Müügireskontro ja ostureskontro kuupäevad käibemaksu jaoks</td>
<td>Tšehhi Vabariik, Poola</td>
<td>
<p>Euroopa Liidu (EL) riikidest kaupade ostmisel on kohustuslik iseseisev KM arvestamine:</p>
<ul>
<li>arvestatud KM tuleb maksta sellel KM-perioodil, millal arve väljastati (dokumendi kuupäev).</li>
<li>Sisendkäibemaksu ei saa enne dokumendi kättesaamist (KM registreerimise kuupäeva) maha arvestada.</li>
</ul>
<p>Selle stsenaariumi toetamiseks peaksid olema konfigureeritud järgmised sätted.</p>
<ul>
<li>Aktiveerige lehel <strong>Ostureskontro parameetrid</strong> valik <strong>EL-i sisene KM</strong> ja <strong>Dokumendi kuupäev EL-i sisese käibemaksu puhul</strong>.</li>
<li>Seadistage kuni kaks käibemaksukoodi: üks, millel on positiivne käibemaksuprotsent ja teine, millel on negatiivne käibemaksuprotsent.</li>
<li>Seadistage käibemaksugrupp, mis sisaldab nii positiivset kui ka negatiivset käibemaksukoodi. Negatiivse käibemaksukoodi puhul määrake parameetri <strong>EL-i sisene KM</strong> väärtuseks <strong>Jah</strong>.</li>
</ul>
<p>Pärast edukat seadistust on ostudel kaks sisestatud käibemaksukannet:</p>
<ul>
<li>positiivne kanne, mille suund on <strong>saadaolev käibemaks</strong> ja millel on arve sisestuslehe kuupäevaga võrdne käibemaksu registreerimiskuupäev;</li>
<li>negatiivne kanne, mille suund on <strong>maksmisele kuuluv käibemaks</strong> ja mille käibemaksu registreerimiskuupäev on võrdne dokumendi kuupäevaga.</li>
</ul>
</td>
</tr>
<tr>
<td>Müügidokumendi kuupäeva muutmine.</td>
<td>Kõik Ida-Euroopa riigid</td>
<td><p>Saate muuta välja <strong>Dokumendi kuupäev</strong> projekti arvel. See kuupäev kuvatakse prinditud arvel.</p>
<p>Lehtedel <strong>Arve sisestamine</strong> ja <strong>Vabas vormis arve</strong> on ka väli <strong>Dokumendi kuupäev</strong>. Pärast arve sisestamist kuvatakse dokumendi kuupäev arve päises.</p>
</td>
</tr>
<tr>
<td>Dokumendi kuupäev vahetuskursside jaoks</td>
<td>Poola, Ungari, Tšehhi Vabariik, Itaalia</td>
<td>
<p>Seaduses on äritehingute jaoks kehtivate vahetuskursside valimiseks erinevad reeglid. Lehtede <strong>Müügireskontro parameetrid</strong> ja <strong>Ostureskontro parameetrid</strong> väljal <strong>Vahetuskursi kuupäev</strong> saab valida kuupäeva, mida tuleks kasutada ostu- ja müügidokumentidel arvestusvaluuta arvutuste jaoks. Andmete sisestamisel toob süsteem selle parameetri põhjal kande vahetuskursi.</p>
<blockquote>[!NOTE]<br>Itaalia puhul rakendub see funktsioon ainult ostureskontro moodulis. Ostureskontro parameetrites saab kasutaja valida <strong>Sisestamise kuupäeva</strong> või <strong>Dokumendi kuupäeva</strong> väljal <strong>Vahetuskursi kuupäev</strong>.   </blockquote>
<blockquote><br>Kui määrate välja <strong>Vahetuskursi kuupäev</strong> väärtuseks <strong>Dokumendi kuupäev (ainult EL-i kaubanduse puhul)</strong>, kasutab süsteem käibemaksugruppi. Käibemaksugrupi puhul on vahekaardil <strong>Üldine</strong> parameeter <strong>EL-i kaubandus</strong>. Kui käibemaksugrupil on valiku <strong>EL-i kaubandus</strong> väärtuseks määratud <strong>Jah</strong> ja kui see käibemaksugrupp on dokumendi päises olemas, toob süsteem vahetuskursi dokumendi kuupäeva põhjal. Kui selle käibemaksugrupi puhul on valiku <strong>EL-i kaubandus</strong> väärtuseks määratud <strong>Ei</strong>, toob süsteem vahetuskursi dokumendi sisestuskuupäeva põhjal.</blockquote>
  <blockquote><br>Poola jaoks on müügireskontro <strong></strong> moodulis saadaval selle <strong>parameetri</strong> täiendav automaatse kuupäeva määramise väärtus. Kui see ruut on märgitud, valib süsteem arve sisestuskuupäevast, müügikuupäevast ja maksekuupäevast automaatselt varaseima kuupäeva.</blockquote>
</td>
</tr>
<tr>
<td>Kaubavahetuse kuupäevad, käibemaksu registreerimise kuupäevad ja käibemaksu kuupäeva juhtimine</td>
<td>Poola, Ungari, Tšehhi Vabariik</td>
<td>
<p>Müügikuupäev ja dokumendi vastuvõtukuupäev on käibemaksuaruande jaoks kohustuslikud.</p>
<ul>
<li>Müügikuupäev on kande täitmise kuupäev müügireskontrol.</li>
<li>Dokumendi vastuvõtukuupäev on kuupäev, mis näitab käibemaksu mahaarvamise nõudmise õigusi ostureskontrol. Igal vastuvõetaval dokumendil on auditeerimiseks kuupäev.</li>
</ul>
<p>Ungari kuupäeva tähtaegade funktsioon, Tšehhi Vabariigi kuupäevade täitmise funktsioon ja Poola KM registreerimise kuupäeva funktsioon hõlmavad maksuteabe aruandluse nõuet, mis põhineb sisestuskuupäevast erineval kuupäeval.</p>
<p>Väli <strong>KM-registri kuupäev</strong> toetab seda nõuet ja kuvatakse rohkem kui 20 lehel. Nende lehtede hulka kuuluvad töölehed, müügitellimused, ostutellimused, vabas vormis arved, hankija arve töölehed ja projektiarved. Dokumentide värskendamisel või sisestamisel sisestatakse kõik maksud käibemaksuregistri asjakohase kuupäevaga ja kuupäev on lisatud lehtedele, nt kliendi ja hankija arve töölehtede lehtedele.</p>
<p>Konkreetselt Tšehhi Vabariigi puhul võib väli <strong>Käibemaksu registreerimiskuupäev</strong> sisestamise ajal tühi olla, kui KM-sisestus on edasi lükatud. Vastasel korral väli on kohustuslik ja tuleb täita.</p>
<p>Kuupäeva valideerimise parameetrid saab määrata lehel <strong>Käibemaksugrupid</strong>.</p>
<ul>
<li>Parameetreid <strong>KM-registri kuupäeva täitmine</strong> ja <strong>Müügikuupäeva täitmine</strong> kasutatakse täitmise vaikemeetodina sobivatel kuupäevadel. Saadaval on ka käsitsi sisestus ja mitu automaatset sisestusmeetodit.</li>
<li>Väljal <strong>Kohustuslik müügikuupäev</strong> on näidatud, kas müügikuupäev tuleb sisestada enne müügiarve sisestamist.</li>
</ul>
<p>Lehel <strong>Käibemaksuregistri kanded</strong> saate täita sisestatud maksukannete kohta käibemaksuregistri tühjad kuupäevad.</p>
</td>
</tr>
<tr>
<td>KM-registri kuupäevad, mis sisaldavad viitmaksu</td>
<td>Ungari</td>
<td>
<p>Ungari maksuseadused nõuavad, et arved koostatakse kas täitmise ajal või hiljemalt 15 päeva pärast täitmist.</p>
<p>Täitmise kuupäev on tellitud teenuste osutamise või tellitud kaupade kohaletoimetamise kuupäev. Dokumentide muutmisel või sisestamisel sisestatakse kõik maksud, kasutades vastavat käibemaksuregistri kuupäeva, ja kuupäev kuvatakse vastavatel lehtedel. Lisaks nõuavad eeskirjad, et pidevalt osutatavate teenuste (nt rentimine, liisimine, konsultatsioonid ja küte) KM vastaks järgmistele kriteeriumidele.</p>
<ul>
<li>KM tuleb sisestada spetsiaalsele pearaamatukontole arve kuupäeval.</li>
<li>KM tuleb kanda üle spetsiaalsetelt kontodelt saadaoleva või tasumisele kuuluva käibemaksu kontole ja see peab kajastuma ettenähtud kuupäeva KM-aruandes.</li>
</ul>
<p>Nende nõuete täitmiseks võite kanda pearaamatu sisestused laekuva viitmaksu kontole ja väljamineva viitmaksu kontole. Kuid kõigepealt peavad olema täidetud järgmised eeltingimused.</p>
<ul>
<li>Seadistage pearaamatu sisestamisgruppides maksmisele kuuluva viitkäibemaksu ja saadaoleva viitkäibemaksu pearaamatukontod.</li>
<li>Lubage kauba käibemaksugruppide parameeter <strong>Viitkäibemaks</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td> Kohustuslik käibemaksu kuupäev</td>
<td>Poola</td>
<td>
<p>Võite nõuda, et KM-registri kuupäev lisataks ostu- ja müügikande kirjetele. Seetõttu saab KM-registri kuupäeva hõivata enne kande sisestamist. Selle funktsiooni abil saate vältida mitme kande töötlemist perioodi lõpus.</p>
<p>Saate muuta välja <strong>KM-registri kuupäev</strong> kliendi või hankija kannete sisestamisel kohustuslikuks. Välja kohustuslikuks muutmiseks lubage seotud kliendi või hankija kontol valik <strong>KM kuupäev on nõutav</strong>.</p>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
