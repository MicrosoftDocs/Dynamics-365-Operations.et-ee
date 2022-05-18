---
title: Eemaldamisreeglid
description: See teema annab teavet eemaldamisreeglite ja eemaldamistest teatamise erinevate võimaluste kohta.
author: aprilolson
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: twheeloc
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e062e7541871d77803cbed475d715621b19537f1
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722629"
---
# <a name="elimination-rules"></a>Eemaldamisreeglid

[!include [banner](../includes/banner.md)]

See teema annab teavet eemaldamisreeglite ja eemaldamistest teatamise erinevate võimaluste kohta.

Eemaldamiskanded on nõutavad juhul, kui emaettevõttest juriidilisel isikul on ärisuhted ühe või mitme tütarettevõttest juriidilise isikuga ning ta kasutab konsolideeritud finantsaruandlust. Konsolideeritud finantsaruanded peavad sisaldama ainult konsolideeritud organisatsiooni ja teiste sellest organisatsioonist väljaspool asuvate üksuste vahelisi kandeid. Seetõttu tuleb samasse organisatsiooni kuuluvate juriidiliste isikute vahelised kanded pearaamatust eemaldada, nii et neid finantsaruannetes ei kuvata. Eemaldamistest saab teatada mitmesugusel moel.

-   Eemaldamisreeglit saab luua ja töödelda konsolideerimis- või eemaldamisettevõttes.
-   Finantsaruandlust saab kasutada eemaldamiskontode ja dimensioonide kuvamiseks konkreetses reas või veerus.
-   Eemaldamiste jälgimiseks võib käsitsi kandekirjete sisestamiseks kasutada eraldi juriidilist isikut.

Selles teemas käsitletakse eemaldamisreegleid, mida töödeldakse eemaldamis- või konsolideerimisettevõttes. Saate seadistada eemaldamisreeglid, et luua eemaldamiskanded juriidilises isikus, mis on määratud sihtettevõttest juriidilise isikuna eemaldamiste jaoks. Seda sihtettevõttest juriidilist isikut nimetatakse eemaldamise juriidiliseks isikuks. Eemaldamistöölehti saab luua konsolideerimisprotsessis või eemaldamistöölehe soovituse abil. Enne eemaldamisreeglite seadistamist tuleb tutvuda järgmiste terminitega.

-   **Lähteettevõttest juriidiline isik** – juriidiline isik, kus sisestatakse eemaldatavad summad.
-   **Sihtettevõttest juriidiline isik** – juriidiline isik, kus sisestatakse eemaldamisreeglid.
-   **Eemaldamisettevõttest juriidiline isik** – juriidiline isik, mis on määratud eemaldamiste sihtettevõttest juriidiliseks isikuks.
-   **Konsolideeritud juriidiline isik** – juriidiline isik, mis on loodud finantstulemustest juriidiliste isikute grupile aruandmiseks. Juriidiliste isikute finantsandmed konsolideeritakse sellesse juriidilisse isikusse ja seejärel luuakse kombineeritud andmete põhjal finantsaruanne.

Järgmises tabelis on kirjeldatud kannete tüüpe, mis võivad olla eemaldatavad.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kande tüüp</th>
<th>Näide</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Müügitellimus kanne ja arve (tsentraliseeritud töötlemine)</td>
<td>Müüte toote kliendile oma organisatsiooni teise juriidilise isiku nimel.</td>
</tr>
<tr class="even">
<td>Müügitellimuse kanne (kontsernisisene) ja arve</td>
<td>Müüte tooteid oma organisatsiooni juriidiliste isikute vahel.</td>
</tr>
<tr class="odd">
<td>Ostutellimused (tsentraliseeritud töötlemine)</td>
<td>Ostate varusid, tarneid, teenuseid, põhivarasid ja muid tooteid hankijalt oma organisatsiooni teise juriidilise isiku nimel.</td>
</tr>
<tr class="even">
<td>Laohaldus (kontsernisisene)</td>
<td><ul>
<li>Kannate oma organisatsiooni ühe juriidilise isiku varud üle teise juriidilise isiku põhivaradesse.</li>
<li>Kannate oma organisatsiooni ühe juriidilise isiku varud üle teise juriidilise isiku varudesse.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Teel olevate varude jälgimine</td>
<td>Kannate kaupu üle samas juriidilises isikus, kuid erinevates geograafilistes paikades asuvate ladude vahel.</td>
</tr>
<tr class="even">
<td>Ostureskontro tsentraliseeritud arvetöötlus</td>
<td>Kirjendate arve oma organisatsiooni teise juriidilise isiku nimel.</td>
</tr>
<tr class="odd">
<td>Ostureskontro tsentraliseeritud maksetöötlus</td>
<td>Tasute arve oma organisatsiooni teise juriidilise isiku nimel.</td>
</tr>
<tr class="even">
<td>Kassahaldus ja kassa (tsentraliseeritud töötlemine)</td>
<td><ul>
<li>Saate töödelda maksumakseid, maksu tagasimakseid, viivisetasusid, laene, ettemakse, makstud dividende ja ettemakstud autoritasusid või komisjonitasusid.</li>
<li>Tasute kulu oma organisatsiooni teise juriidilise isiku nimel. Arve on sisestatud sihtettevõttest juriidilise isiku raamatutesse ja te peate tegema ettevõtetevahelise tasakaalustuse. Näiteks tasub üks juriidiline isik teise juriidilise isiku töötaja kuluaruande. Sellisel juhul on töötaja kuluaruandes kulud, mis on seotud teise juriidilise isikuga.</li>
<li>Kannate sularaha oma organisatsiooni ühest juriidilisest isikust teise.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Müügireskontro (tsentraliseeritud töötlemine)</td>
<td>Võtate sularaha vastu teise juriidilise isiku kliendiarve jaoks ja deponeerite tšeki selle juriidilise isiku pangakontole.</td>
</tr>
<tr class="even">
<td>Palk (tsentraliseeritud töötlemine, kontsernisisene)</td>
<td><ul>
<li>Maksate teise juriidilise isiku palgad. Näiteks võib juriidiline isik maksta oma töötajale palka, kuid arvestab maha tasu töö eest, mille töötaja tegi selle palgaarvestusperioodi jooksul teisele juriidilisele isikule. Või kui töötaja töötas pool aega juriidilisele isikule A ja pool aega juriidilisele isikule B ning soodustused katavad kogu tasu. Neil juhtudel sisaldab töötaja palk tasu mõlemalt juriidiliselt isikult. Sisestatakse mitte ainult töötasud, vaid ka maksud, soodustused, mahaarvamised ja viitvõlad töötasudele.</li>
<li>Kannate töö üle ühest osakonnast või üksusest teise.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Põhivarad (kontsernisisene)</td>
<td>Kannate põhivarad üle teise juriidilise isiku põhivaradesse või varudesse.</td>
</tr>
<tr class="even">
<td>Eraldamised (kontsernisisene)</td>
<td>Töötlete ettevõtte eraldusi. Eraldused on tegevused kõigi eraldatud kontodega, olenemata moodulist, kust see pärit on.</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Näide
Teie juriidiline isik (A) müüb vidinad teisele teie ettevõtte juriidilisele isikule (B). Järgmises näites kirjeldatakse, kuidas kahe juriidilise isiku vahelised kannete eemaldamine võib vajalikuks osutuda.

-   Juriidiline ettevõte A müüb 10,00 eurot maksva vidina juriidilisele isikule B hinnaga 10,00 eurot.
-   Juriidiline isik A müüb 10,00 eurot maksva vidina juriidilisele isikule B hinnaga 10,00 eurot pluss 2,00 eurot tegelikku postikulu.
-   Juriidiline isik A müüb 10,00 eurot maksva vidina juriidilisele isikule B hinnaga 15,00 eurot ja saab selle müügi pealt brutotulu.
-   Juriidiline isik A müüb 10.00 eurot maksva vidina juriidilisele isikule B hinnaga 15.00 eurot ja saab selle müügi pealt poole brutotulust. Juriidiline isik B saab teise poole brutotulust. Seetõttu on tulu jagatud. Jagatud tulu pakub soodustust välisest organisatsioonist tellimise asemel oma organisatsiooni teisest ettevõttest tellimise korral.

Kõik need kanded loovad kontsernisisesed kanded, mis sisestatakse algus- ja lõpptähtaja kontodele. Peale selle võivad need kanded hõlmata hinnalisandiga ja hinnavähendusega summasid, kui kontsernisisene müügisumma ja müüdud kaupade maksumus ei ole võrdsed.

## <a name="set-up-elimination-rules"></a>Eemaldamisreeglite seadistamine
Eemaldamisreeglite seadistamisel soovitame luua spetsiaalselt eemaldamiseks mõeldud finantsdimensiooni. Enamik kliente annab sellele nimeks Kaubanduspartner või muud sarnast. Kui te ei soovi finantsdimensiooni kasutada, siis peavad teil kindlasti olema ainult ettevõtete vahelisteks kanneteks mõeldud põhikontod. 

Eemaldamised saate seadistada mooduli Konsolideerimised alal Seadistus. Kui olete reegli kohta kirjelduse sisestanud, peate valima ettevõtte, millesse eemaldamisreegel sisestab. See peab olema ettevõte, mille puhul on juriidilise isiku seadistuses valitud suvand **Kasuta finantsiliseks eemaldamisprotsessiks**. 

Saate määrata eemaldamisreegli jõustumiskuupäeva ja vajadusel ka aegumiskuupäeva. Kui soovite, et see oleks eemaldamispakkumise protsessis saadaval, valige suvandi **Aktiivne** sätteks **Jah**. Valige selle töölehe nimi, mille tüüp on **Eemaldamine**.

Kui olete põhiparameetrid määratlenud, saate määratleda ka tegelikud töötlusreeglid, klõpsates valikut **Read**. Eemaldamiseks on kaks võimalust: netomuutuse summa eemaldamine või fikseeritud summa määratlemine. 

Valige lähtekonto. Saate kasutada metamärgina tärni (\*). Näiteks väärtuse 1\* korral valitakse eralduse andmeallikana kõik kontod, mis algavad numbriga 1. 

Kui olete lähtekontod valinud, määrab valik **Konto täpsustus** kasutatava konto sihtettevõttes. Valige suvand **Allikas**, kui soovite kasutada sama põhikontot, mis on määratletud jaotises **Lähtekonto**. Kui valite suvandi **Kasutaja määratletud**, peate määrama sihtkonto. 

Dimensiooni täpsustus toimib samal moel. Kui valite suvandi **Allikas**, kasutab see sihtettevõttes lähteettevõttega samu dimensioone. Kui valite suvandi **Kasutaja määratletud**, peate määrama sihtettevõtes dimensioonid, klõpsates menüüelementi **Sihtdimensioonid**. 

Valige lähtedimensioonid ja finantsdimensioonid ning väärtused, mida kasutatakse eemaldamisallikana.

## <a name="process-elimination-transactions"></a>Eemaldamiskannete töötlemine
Eemaldamiskannete töötlemiseks on kaks võimalust: ainult võrgu kaudu konsolideerimise ajal või luues eemaldamise tööraamatu ja käitades eemaldamispakkumise protsessi. See jaotis keskendub töölehe loomisele ja eemaldamisprotsessi käitamisele. 

Valige eemaldamisettevõttena määratletud ettevõttes moodulis Konsolideerimine suvand **Eemaldamisreegel**. Pärast töölehe nime valimist klõpsake valikut **Read**. Pakkumise saate käivitada, valides menüü **Pakkumised** ja seejärel suvandi **Eemaldamisperiood.**

Valige ettevõte, mis on konsolideeritud andmete allikas, ja seejärel valige reegel, mida soovite töödelda. Sisestage eemaldamissummade otsimiseks algus- ja lõppkuupäev. Välja **Pearaamatu sisestamise kuupäev** kasutatakse töölehe pearaamatusse sisestamiseks. Pärast nupu **OK** klõpsamist saate summad üle vaadata ja töölehe sisestada.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
