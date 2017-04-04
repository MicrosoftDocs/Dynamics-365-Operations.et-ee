---
title: Eemaldamisreeglid
description: "See teema pakub teavet kõrvaldamise reeglid ja aruandluse umbes elimineerimised erinevaid võimalusi."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: db4b05bc55d735513d7580ca5908a1e84eb760c6
ms.openlocfilehash: 152b63fdfc78b3c4e79b93340d18c5cf69257024
ms.lasthandoff: 03/31/2017


---

# <a name="elimination-rules"></a>Eemaldamisreeglid

See teema pakub teavet kõrvaldamise reeglid ja aruandluse umbes elimineerimised erinevaid võimalusi.

Eemaldamiskanded on nõutavad juhul, kui emaettevõttest juriidilisel isikul on ärisuhted ühe või mitme tütarettevõttest juriidilise isikuga ning ta kasutab konsolideeritud finantsaruandlust. Konsolideeritud finantsaruanded peavad sisaldama ainult konsolideeritud organisatsiooni ja teiste sellest organisatsioonist väljaspool asuvate üksuste vahelisi kandeid. Seega, juriidilised isikud, kes kuuluvad samasse organisatsiooni vaheliste tehingute eemaldada, või kõrvaldada pearaamatu, seetõttu ei kuvata finantsaruannete põhjal. Eemaldamistest saab teatada mitmesugusel moel.

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
Kõrvaldamise eeskirjad Dynamics 365 operatsioonide loomisel soovitame luua rahalise küljega konkreetselt kõrvaldamise eesmärgil. Enamik kliente nime Trading Partner või midagi sarnast. Kui te ei soovi kasutada rahalise küljega, siis kindlasti on IC-tehinguid ainult seotud keskne raamatupidamine. 

Setup elimineerimiste jaoks leitakse konsolideerimise moodul Setup valdkonnas. Kui olete sisestanud reegli kirjeldus, peate valima ettevõtte likvideerimise töölehe konteerib. See peaks olema ettevõte, mis on **kasutamine rahaliste kõrvaldamise protsessile** juriidilise isiku seadistuses valinud. 

Saate kuupäeva mis kõrvaldamiseks eeskirja jõustumist ja kuna see on aegunud, kui vaja. Peate määrama **aktiivne** et **Jah** kui see saadaval soovitusprotsessi kõrvaldamiseks. Valige töölehe nimi, mis on teatud tüüpi **kõrvaldamiseks**.

Pärast põhitõdesid, klõpsates saate määratleda tegelik eeskirjad **read**. On kaks võimalust elimineerimine, kõrvaldades muutus summa või kindlasummaline määratlemisel. 

Valige konto allikas. Kasutage tärni (\*) metamärgina. Nt 1\* valida kõik kontod, alustades 1 jaotamise andmete allikas. 

Pärast seda, kui valitud konto allikas on **moodustavad spetsifikatsioon** määrab sihtkoha firma, mida kasutatakse konto. Valige **allikas** kui soovite kasutada määratud sama peamine konto on **allikas** konto. Kui valite **kasutaja määratud**, siis määrake sihtkoht konto. 

Dimensiooni kirjeldus toimib samal viisil. Kui valite **allikas**, ta kasutab sama allikas ettevõtte sihtettevõttes. Kui valite **kasutaja määratud**, peate määrama sihtkoha ettevõttes dimensioonid, klõpsates selle **sihtkoha mõõtmed** menüükäsu. 

Valige allikas mõõtmed ja finantsdimensioonide ja kõrvaldamiseks allikana kasutatavad väärtused.

## <a name="process-elimination-transactions"></a>Eemaldamiskannete töötlemine
On kaks võimalust protsessi kõrvaldamiseks tehingute käigus Konsolideeri online või kõrvaldamise töölehe loomise ja likvideerimise soovitusprotsessi. Käesolevas punktis keskendutakse töölehe loomise ja käivitamise kõrvaldamise protsessile. 

Valige ettevõttelt kõrvaldamiseks ettevõtte määratletud, **kõrvaldamiseks töölehe** konsolideerimise moodul. Pärast valitud töölehe nime, klõpsake **read**. Ettepaneku käivitada valides ning **ettepanekud** menüü ja valige **kõrvaldamiseks ettepaneku**.

Valige ettevõte, mis on konsolideeritud andmete allikas ja valige reegel, mille soovite töödelda. Sisestage alguskuupäeva kõrvaldamiseks summad otsingu alustamiseks ja lõpetamiseks otsingu kuupäev kõrvaldamiseks summad kuupäeva. Selle **GL konteerimiskuupäeva** väli on kasutatav töölehe pearaamatusse sisestamise kuupäev. Pärast nupu **OK**, saate vaadata summad ja selle konteerida.


