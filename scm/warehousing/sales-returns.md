---
title: "Müügitagastused"
description: "See teema pakub teavet protsessi tagastuskorraldused. See sisaldab teavet kliendi tulu ja nende mõju maksavad ja vaba varude kogused."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 269384
ms.assetid: 98a4b517-e606-4036-b55f-1ab248898bdf
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3d02a15387231160f5b8a237aa11008b91ef1223
ms.openlocfilehash: b265a20a271230de5dba6df93900a24aad642885
ms.lasthandoff: 03/31/2017


---

# <a name="sales-returns"></a>Müügitagastused

See teema pakub teavet protsessi tagastuskorraldused. See sisaldab teavet kliendi tulu ja nende mõju maksavad ja vaba varude kogused.

Hotelli naasta üksuste erinevatel põhjustel. Näiteks kauba võib olla vigane või see ei vasta kliendi ootustele. Tagasipöördumise protsess algab, kui klient annab kauba tagastamise taotluse. Pärast kliendi taotluse kättesaamise tagastuskorralduse luuakse Microsoft Dynamics 365 toiminguteks.

## <a name="return-order-process"></a>Tagastuskorralduse protsessi
Järgmine joonis annab ülevaate tagastuskorralduse protsessi.  

[![salesreturns01](./media/salesreturns01.jpg)](./media/salesreturns01.jpg)  

On kahte tüüpi tagastuskorralduse protsess: füüsiline tagasi ja ainult krediidi.

-   **Tegelik tagastamine** – tagasisaatmisotsust lubab toodete tegelik tagastamine.
-   **Krediidi ainult** – tagasisaatmisotsust lubab kliendikrediidi kuid ei nõua füüsiliselt tagastamist tooted.

### <a name="physical-return-order-process"></a>Füüsilise tagastuskorralduse protsessi

1.  **Tagastuskorralduse loomine** Ametlikult dokumendi defektne või soovimatu toodete tagastamise kliendi luba. Tagasisaatmisotsust ei nõua, et ettevõte aktsepteeri tagastatud toodete või käsitata kliendi. Kui tagastamise vastu, saate lubada uue elemendi enne defektne kaup tagasi saata.
2.  **Saabuvad lattu kontrollimiseks.** Täielik esmase kontrolli ja tagastuskorralduse dokumendi valideerimine. Tagastuskorralduse toetab ka karantiini tagastatud kaubad täiendavad ja kvaliteedikontrolli.
3.  **Kindlaks likvideerimise.** Ülevaatuse protsessi lõpule ja otsustada, mida teha tagastatud toodetega. Selle sammu raames otsustada, kas näidatakse krediidi klient, tagasilükkamist toote tagastamise või toote tagastamise vastu, toote jäägid, ja saatke kliendile asendustoote.
4.  **Luua saatelehega.** Luua saatelehe ja likvideerimise otsuse, sammus 3 tehtud endale. Logistiliste protsesside lõpetamine.
5.  **Loo arve.** Sulgege tagastuskorraldus.

### <a name="credit-only-process"></a>Ainult kohtutäiturite krediidi

1.  **Tagastuskorralduse loomine** Ametlikult dokumendi loa saada krediiti ilma tagasi defektne või soovimatu tooted kliendile. Selle **laenu ainult** likvideerimise kood lubab otsuse krediidiasutustele kliendi tegelik tagastamine ilma.
2.  **Loo arve.** Loo kreeditarve ja sulgege tagastuskorraldus.

## <a name="return-material-authorization"></a>Tagasi olulise lubade
Saatja materjal loa (RMA) töötlemine põhineb müügitellimuse funktsionaalsust. Mis RMA on registreeritud tagastuskorralduse, mis on loodud Müügitellimus ja võib olla seotud, nimetatakse ka asendamine teise müügitellimuse. Mõlemad müügitellimuste link pärit RMA kood.

-   **Tagastuskorralduse** -registreerimiseks on tagastatud kauba tagasi tellimus, mis on müügitellimuse, mis on määratud tüüp, **tagasi järjekorras.** RMA teabe mis tahes muudatused uuendatakse automaatselt müügitellimuse. Kuni tagasisaatmisotsust olek on **avatud**, see kuvatakse müügitellimuste loend. Kasutate tagastatud kauba saabumist ja tagastatud kaupade tarne ning lubada krediidi vaid likvideerimise meetmeid (vt lõik **likvideerimise koodid ja likvideerimise meetmete**). Kõik järgnenud protsessides ülimat müügitellimuse.
-   **Asendamise korra** – kui asendamine tellimus tuleb saata kliendile on tagastatud kauba võib sisaldada teise seotud müügitellimus. Käsitsi loomiseks asendamine selleks, et toetada kohe lähetamiseks RMA. Teise võimalusena asendamise korra loomist automaatselt pärast saabumist, kontroll ja vastuvõtmine on lõpetatud on likvideerimise kood, mis näitab asendamine RMA müügirea kauba kohta. Asendamine tellimusel on samu funktsioone, mis on seotud müügitellimusega. Näiteks saate selle konfigureerida kohandatud toode asenduskaup, luua tootmistellimuse tagastatud kauba remont, Otsetarne ostutellimuse saatmiseks tarnija asendamine või toetada muul otstarbel.

## <a name="create-a-return-order"></a>Tagastustellimuse loomine
Tagastuskorralduse protsess algab, kui klient võtab ühendust organisatsiooni defektne või soovimatu toote ja/või mis tuleb kanda. Pärast oma organisatsiooni aktsepteerib tagasi, tagasi tagastuskorralduse poolt dokumenteeritud. Edasi-tagasi lahendit sisemine tagastatud toote keskpunktiks. Järgmine joonis kujutab tagastuskorralduse loomine.  

[![Tagastuskorralduse loomine](./media/salesreturn02.png)](./media/salesreturn02.png)

### <a name="create-a-return-order-header"></a>Tagastuskorralduse päise loomine

Tagastuskorralduse loomisel tuleb lisada teave järgmises tabelis.

| Väli              | Kirjeldus                                              | Kommentaarid                                                                                                                                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kliendi konto   | Viide tabeli Kliendid                       | Peate sisestama kliendi konto.                                                                                                                                                                                                                                                                                                  |
| Tarneaadress   | Tagastatava kauba aadress                 | Vaikimisi kasutatakse organisatsiooni aadressi. Kindla lao märkimisel päise muudetakse tarneaadress lao aadressile. Võite muuta see aadress on **tagasi tellimuse üksikasjad** lehel.                                                                                                  |
| Saidi/ladu     | Saidi või saab Tagastatav kaup lattu | Tarneaadressi saidi või lao määratakse tagasisaatmisotsust tarneaadressi.                                                                                                                                                                                                                                 |
| Tagastuse number         | ID, mis määratakse tagasisaatmisotsust              | RMA kood kasutatakse kogu tagastuskorralduse asendusliikme klahvile. RMA-kood, mis määratakse põhineb tagastatud kauba kohta seadistatud numbriseeria on **Müügireskontro parameetrid** lehel.                                                                                                                              |
| Lõpptähtaeg           | Viimane kuupäev, millal kaup tagastada               | Vaikeväärtus arvutatakse praegune kuupäev ja kehtivusaeg. Näiteks kui deklaratsioon kehtib ainult 90 päeva jooksul alates kuupäevast, millal tagasisaatmisotsust luuakse, 1. mail loodi tagasisaatmisotsuse, välja väärtus on **30-juuli**. Kehtivusaeg on sisse ning **Müügireskontro parameetrid** lehel. |
| Tagastuspõhjuse kood | Kliendi tagastamise põhjus          | Põhjuse tähis on valitud siia põhjus koodide loetelu. Sellel väljal saate värskendada igal ajal.                                                                                                                                                                                                                                    |

### <a name="create-return-order-lines"></a>Tagastuskorralduse ridade loomine

Pärast tagasi päise, te saate loomiseks kasutada ühte järgmistest meetoditest:

-   Käsitsi sisestada üksuse andmed, kogus ja muud teavet iga edasi-tagasi käsitsi.
-   Tagasi liini abil luua ka **leida müügitellimuse** funktsiooni. Soovitame kasutada seda funktsiooni tagastuskorralduse loomisel. Selle **leida müügitellimuse** funktsiooni kehtestatakse viite tagasi liini arveldatud müügitellimuse rea ja toob rida andmeid, nt kauba kood, kogus, hind, allahindlus ja omahindade müügirealt. Viide aitab tagada, et kui toode tagastatakse ettevõttele, see on väärtustatud üksuse juures see, et ostetud. Viide ka kinnitab, et tagasi kogus, mis ületab kogust, mida müüdi arvel ei ole luua ostutellimused.

**Märkus:** edasi-tagasi read, mis on müügitellimuse viite käideldakse kui parandused või tühistamised, müük. Lisateavet leiate jaotisest "Post pearaamatusse", selle teema.

### <a name="charges"></a>Tasud

Lõivude ja tasude lisamist tagastuskorralduse kaudu ühte või mitut järgmistest meetoditest:

-   Te saate käsitsi lisada tasud tagastuskorralduse päises, tagastuskorralduse Real või mõlemad.
-   Tagastuskorralduse päises saab tasud automaatselt lisada tagastamise põhjuse tähis funktsioonina.
-   Tasusid saab automaatselt lisada tagastuskorralduse Real, põhineb likvideerimise koodi rea.

Maksud lisatakse automaatselt pärast tagastamise põhjuse tähis või likvideerimise tähis määratakse rea. Kui põhjusetähis hiljem muuta, olemasolevaid voodeid kanne ei eemaldata, kuid on uus kanne võidakse lisada, vastavalt uue põhjuse tähis. Eest, et tagasi ridade lisamisel kulud, mis arvutatakse protsendina rea või tellimuse väärtus muutuda negatiivseks, kui rea või tellimuse rida on negatiivne, kui protsent on negatiivne arv. Eest, mis on negatiivne väärtus esindab kliendile krediiti.

### <a name="return-reason-codes"></a>Tagastuspõhjuste koodid

Rakendades põhjusetähiste tulu, aitab teil teha edasi-tagasi mustrite hõlpsam analüüsida. Põhjusetähiste teavet, miks klient soovib kaubad tagasi. Mõned organisatsioonid on palju põhjusetähised. Need organisatsiooni rühmitada põhjusetähiste ka põhjus grupid saada parema ja akumuleeritud aruandluseks.

### <a name="disposition-codes-and-disposition-actions"></a>Likvideerimise koodid ja likvideerimise meetmed

Oluline samm edasi-tagasi, et protsess on tagastuskorralduse Real likvideerimise koodi määramist saabumist registreerimiseks. Likvideerimise tähis määratleb järgmised andmed:

-   **Rahaline mõju** -klient kantakse tagastatud kaupade ja kõik maksud lisatakse tagastuskorralduse Real?
-   **Tagastatud kauba võõrandamine** – kaup on uuesti lisada varude, see tuleb tühistada või tuleks see tagastada kliendile?
-   **Tagastatud kauba logistika** – uue elemendi väljastatakse kliendile?

Lisaks määratakse kindlaks, kuidas kõrvaldatakse tagastamisele, põhjustada likvideerimise koodid tagasi liini kohaldatavad tasud. Neid saab rühmitada tagastab statistiliseks analüüsiks. Likvideerimise koodid on määratletud tagastuskorraldused setup osana. Siiski iga likvideerimise kood peab viitama üks sisseehitatud likvideerimise meetmeid. Järgmises tabelis on loetletud, sisseehitatud likvideerimise ning neid oma tegevuses. **Tähtis:** üksus peaks ei tagastata juhul, kui klient ikka kantakse, määrata on **krediidi ainult** likvideerimise koodi tagasi liini.

<table>
<thead>
<tr class="header">
<th>Likvideerimiskood</th>
<th>Finantsmõju</th>
<th>Mõju logistikale</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ainult kreedit</td>
<td><ul>
<li>Klient krediteeritakse müügihind miinus tasusid ja makse.</li>
<li>Kahjum lammutamise kaup sisestatakse pearaamatusse.</li>
</ul></td>
<td>Üksust ei tuleks tagasi. Likvideerimise meetmeid kasutatakse järgmistel juhtudel:
<ul>
<li>On piisavalt usaldust teiste isikute hulgas.</li>
<li>Defektse kauba tagastamise kulud on ülemäära kallis.</li>
<li>Üksused ei tohi varudesse tagasi. Muude tingimuste tõttu tegelik tagastamine ei ole nõutav.</li>
</ul></td>
</tr>
<tr class="even">
<td>Krediit</td>
<td><ul>
<li>Klient krediteeritakse müügihind miinus tasusid ja makse.</li>
<li>Varude maksumuse võrra tagastatud kauba maksumusest.</li>
</ul></td>
<td>Üksus tagastatakse ja lisata varude.</td>
</tr>
<tr class="odd">
<td>Asenda ja kanna kreeditisse</td>
<td><ul>
<li>Klient krediteeritakse müügihind miinus tasusid ja makse.</li>
<li>Varude maksumuse võrra tagastatud kauba maksumusest.</li>
<li>Ettenähtud eraldi Müügitellimus luuakse ja käideldakse eraldi.</li>
</ul></td>
<td>Üksus tagastatakse ja lisata varude.</td>
</tr>
<tr class="even">
<td>Asenda ja kanna praaki</td>
<td><ul>
<li>Krediteeritakse kliendi müügihind, vähem tasusid ja makse.</li>
<li>Kahjum lammutamise kaup sisestatakse pearaamatusse.</li>
<li>Ettenähtud eraldi Müügitellimus luuakse ja käideldakse eraldi.</li>
</ul></td>
<td>Kauba on tagastatud ja maha kanda.</td>
</tr>
<tr class="odd">
<td>Tagasta kliendile</td>
<td>Ükski, välja arvatud lõivud ja maksud.</td>
<td>Kaup tagastatakse, kuid saadetakse tagasi kliendile pärast kontrolli. Selle likvideerimise meetmete kasutamiseks, kui kaup on kahjustatud tahtlikult või garantii on tühistatud.</td>
</tr>
<tr class="even">
<td>Praak</td>
<td><ul>
<li>Klient krediteeritakse müügihind miinus tasusid ja makse.</li>
<li>Kahjum lammutamise kaup sisestatakse pearaamatusse.</li>
</ul></td>
<td>Kaup tagastatakse või maha kanda.</td>
</tr>
</tbody>
</table>

## <a name="arrival-at-the-warehouse-for-inspection"></a>Saabumist lattu kontrollimiseks
Enne füüsiliselt vastuvõtmist tagastatud kaupade nimekirja saatelehe sisestamisega, läbivad kaupade saabumise registreerimise ja valikuline kontroll. Järgmine näide annab ülevaate saabumise protsessi. Järgnevates jaotistes kirjeldatakse iga samm, mis on näidatud joonisel.  

[![Saabumist protsess](./media/salesreturn03.png)](./media/salesreturn03.png)  

Protsess on mitu muudatust, mis ei ole hõlmatud selle teema. Siin on mõned sellised muudatused:

-   Ärge kasutage selle **saabumist ülevaade** luua saabuva töölehtede loendi. Selle asemel käsitsi luua saabuva tööleht. Tagasi tellimusi **Müügitellimus** võrdlusena.
-   Kui kasutate laohaldust, luua kaubaaluste transpordi. Tagasi liini on olek **saabunud** kaubaaluste transpordi ajal.
-   Registreerida otse tagastuskorralduse Real tagastatud kauba saabumist abil on **registreerimise** funktsiooni.

Ajal saabumist, tagastab on integreeritud üldmenetluse lattu saabumisel. Samuti toetab saabumise protsessi loomine vahelaoorderid tagastatud kaubad, mis peavad läbima eraldi kontrolli.

### <a name="identify-products-in-the-arrival-overview-list"></a>Toodete saabumist ülevaade nimekirja

Selle **saabumist ülevaade** lehel loetletakse kavandatud sissetuleva saabunud. **Märkus:** saabunud tagastuskorralduselt töödeldakse eraldi saabumist tehingute muid. Pärast seda, kui olete kindlaks sissetuleva paketi kohta on **saabumist ülevaade** (nt kasutades tagastatud kauba saatedokumendi), Updatehagi paani suvandil **alustada saabumist** luua ja käivitada saabumise töölehe, mis vastab saabumist.

### <a name="edit-the-arrival-journal"></a>Redigeeri saabuva tööleht

Seadmisega ning **karantiini juhtimine** võimalus **Jah**, looge vahelao order tagasi liini. Kui rida on saadetud karantiini kontrollimiseks, ei saa määrata likvideerimise tähise. **Märkus:** kui on **karantiini juhtimine** võimalus **Jah** ja kauba laomudeligrupi, on **karantiini juhtimine** ostuoptsiooni on **tööleheridade** lehele märgitakse saabumise töölehe rea ja subtiitrite. Kui rida saadetakse karantiini, määrake sobiv vahelattu. Kui saabumist rida saadetakse kontrollimiseks, lattu saabumise kantseleisse määrata tähise likvideerimise otse žurnaalireale saabumist ja saabumise töölehe seejärel sisestada. Kui likvideerimise samasse ei määrata vöötkoode järgmistest tagasi liini või rea täiskogus ei ole saanud, tuleb jagada rea. Kui jagate saabumist žurnaalirida, jagate ka tagasi liini (**SalesLine**) ja luua uue partii ID. Võite jagada rea saabumist rea vähendamise abil. Töölehe sisestamisel luuakse uus edasi-tagasi rida olek on **eeldatav** allesjäänud koguse. Saate tükeldada rea klõpsates **funktsioonid**&gt;**Split**.

### <a name="process-the-quarantine-order"></a>Protsessi vahelaoorderi

Kui tagastatud tooted saadetakse kontrolli vahelaos, mis tahes täiendava töötlemise lõpetamist vahelao order. Üks vahelaoorder on loodud ridadele saabumist, mis saadetakse karantiini. Likvideerimise kood näitab kontrolli protsessi tulemus. Võite jagada vahelao order, nagu saate tükeldada töölehe saabumist. Kui jagate vahelaoorderi, põhjustada vastava split tagasi liini. Likvideerimise koodi sisestamisel, täielik vahelaoorderi abil üks selle **End** funktsiooni või **lõpetatuna** funktsiooni. Kui valite **lõpetatuna**, luuakse uus saabumine määratud laos. Võite planeeringut töödelda see saabumine abil on **saabumist ülevaade** lehel. Kui vahelaoorder on koostanud saabumist, ei saa muuta likvideerimise kood, mis määratakse kontrolli käigus. Kui täidad vahelaoorderi abil on **End** funktsioon, partii on automaatselt registreeritud. Mõnikord, kaup võidakse saata tagasi karantiinist laevandus ja saavad osakond. Näiteks võib karantiini inspektor ei tea kuhu salvestada kaup laos. Sel juhul vastab sisestamisel tuleb ajakohastada õigesti registreerida ja tegutseda likvideerimise koodi, mis on määratud karantiini tõttu. Vastuvõtuteatise võib saata kliendile tagasi liini registreerimisel. Selle **edasi-tagasi kinnituse** aruande sarnaneb tagastuskorralduse dokumendi. Selle **edasi-tagasi kinnituse** ei ole töölehele sisestatud või muul viisil süsteemis registreeritud, ja see ei ole vajalik samm tagastuskorralduse protsessi.

## <a name="replace-a-product"></a>Asendada
On kaks meetodit haldamise toote asendamine.

-   **Up-front asendamine** – asendada enne, kui Tagastatav kaup on saadud kliendilt.
-   **Likvideerimise koodi asendamine** – automaatselt asendamine uue tellimuserea loomiseks.

### <a name="up-front-replacement"></a>Esimene asendus

Up-front asendamine tarnitavate asendatava kauba kliendile enne kauba tagasi. See meetod on kasulik, kui näiteks kaup on masina osa, mida ei saa eemaldada, kui varuosa on olemas oma kohta või kui soovite teie klient on asendustoode kiiresti. Up-front asendamine tellimus on sõltumatu müügitellimuse. Päiseteavet käivitub kliendi ja line info on lähtestatud tagastuskorralduselt. Saate redigeerida, töödelda ja kustutada asendamine tagasisaatmisotsust sõltumatult. Asendamine tellimuse kustutamisel kuvatakse teade, et tellimuse loomise asendamise korra. Järgmisel joonisel on up-front asendamise protsessi.  

[![Up-front vahetuse](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn04.png)  

Tagastuskorralduse sisaldub viide asendamise järjekorra. Kui tellimuse up-front asendamine luuakse tagastuskorralduse enne defektiga kauba tagastamise kohta, ei saa valida likvideerimise koodid asendamine pärast defektse kauba tagasi.

### <a name="replacement-by-disposition-code"></a>Likvideerimise koodi asendamine

Kui lähetate kliendile uue elemendi ja kasutate selle **asendus ja -jäägid** või **asendamine ning krediidi** likvideerimise meetmed tagastuskorraldus, kasutage protsessi on näidatud järgmisel joonisel.  

[![Asendamise protsessile kui paigutus-koodi](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn05.png)  

Asendatava kauba teieni sõltumatut müügitellimuse asendamine müügitellimuse abil. Müügitellimus luuakse tagasisaatmisotsust saatelehe loomisel. Tellimuse päise kasutab klienditeabe, millele viidatakse tagastuskorralduse päises. Rea teavet kogutakse teavet, mis on kantud ka **asenduskaup** lehel. Selle **asenduskaup** leht peab olema täidetud ridade on likvideerimise meetmeid, mis algavad sõnaga "asendamine." Siiski kogus ega asendatava kauba andmed on valideeritud või piiratud. Selline käitumine võimaldab juhtudeks, kui klient soovib sama, kuid erineva konfiguratsiooni või suuruse ja juhul kui kliendid tahab täiesti teise kauba. Vaikimisi, sisestatakse identne kaup on **asenduskaup** lehel. Siiski saate valida teise kauba, tingimusel, et funktsioon on loodud. **Märkus:** saate redigeerida ja kustutada asendamine müügitellimuse ei.

## <a name="generate-a-packing-slip"></a>Luua saatelehe
Enne tagastatud kaupu saab varudesse vastu, peate värskendama saatelehe tellimuse, et kaubad kuuluvad. Nii nagu arve uuendustoimingut on ajakohastatud tehingust, saatelehe värskenduse protsess on lao kirje füüsilise sisestamisega. Tähendab, see protsess võtab varude muutused. Tegemist on kasumit, rakendatakse selle pakendamisel samme, mis on määratud likvideerimise uuendamisel. Saatelehe loomisel ilmneda järgmised sündmused:

-   Ladu, standardne protsessi teostamiseks kasutatud füüsilise sissetuleku. Pearaamatu sisestusi luuakse, kui varude mudel rühma (**füüsilise lao sisestamine**) ja Accounts receivable parameters (**Sisesta saateleht pearaamatusse**) õigesti seatud.
-   Kaubad, mis on märgistatud likvideerimise meetmeid, mis sisaldab sõna "jääk" ja varude vähenemise sisestatakse pearaamatusse.
-   Üksused, mis on märgistatud selle **tagastab kliendile** likvideerimise tegevuse vastu ja tellijale. Need üksused on varude ei mõjuta.
-   Müügitellimus luuakse asendaja. Selle müügitellimuse põhineb teabel ning **asenduskaup** lehel.

Saate luua ainult read, edasi-tagasi olek on saatelehe **tähitud**, ja ainult terve koguse kohta tagasi liini puhul. Kui mitu rida tagastuskorraldus on selle **tähitud** staatus, saate luua osa ridu saatelehe kustutades read: selle **Sisesta saateleht** lehel. Osaliste deklaratsioonide on määratletud tagastuskorralduse read ei tagastuskorralduse saadetiste osas. Seetõttu, kui kuvatakse üks tagastuskorralduse Real näidatud täiskoguse, kuid te saate midagi ülejäänud tagastuskorralduse read, tarne pole osaline tarne. Kui tagastuskorralduse Real ette 10 ühikut kaupa tagastada, kuid kuvatakse ainult neli ühikut, on tarne osaline tarne. Kui mitte eeldatav tagastatud kaubad on kohale jõudnud, saate saadetise tootmisest ja Tagastatud kaup jõuab puhata oodake. Teise võimalusena saate registreerida ja sisestada osalise kogus. Saatelehtede sisestamisel protsessi raames võimalik seostada need read saatelehe viite number: kliendi veodokumendid. See ühendus on valikuline ja seda saab kasutada üksnes viitamiseks. See ei loo selgituseks värskendusi. Üldiselt jäta pakendamise protsessi libiseda ja minna otse arve. Sellisel juhul täidetakse juhiseid, mida te sooviksite on teostatud pakkimis-slip põlvkonna jooksul arveldamist.

## <a name="generate-an-invoice"></a>Loo arve
Kuigi on **tagastuskorraldusel** leht sisaldab teavet ja meetmeid, mis on vajalikud hakkama eri logistiline aspektides tagastuskorraldus, kasutage selle **Müügitellimus** lehe arveldusprotsessi lõpuleviimiseks. Teie organisatsioon saab siis arve edasi-tagasi ja müügitellimused samal ajal ja sama isik suudaks arveldusprotsessi, vastavalt vajadusele. Tagastustellimus kuvamiseks on **Müügitellimus** lehel, klõpsake linki avada seotud müügitellimuse müügitellimuse number. Leiate ka tagasisaatmisotsust kohta on **kõik Sales orders** lehel. Tagasi on müügitellimused, mis on tellimuse tüüpi **tagasi tellimuse**.

### <a name="credit-correction"></a>Kreediti parandus

Osana arveldusprotsessi kontrollida lisakulusid on õiged. Põhjustada pearaamatu sisestusi saada parandused (Storno), võite kasutada ka **krediidi korrigeerimine** ostuoptsiooni on **muud** vahekaardil on **arve sisestamist** lehekülg arve/kreeditarve konteerimisel. **Märkus:** vaikimisi on **krediidi korrigeerimine** valik on aktiveeritud, kui on **kreeditarve parandus** ostuoptsiooni ka **Müügireskontro parameetrid** leht on kasutatav. Siiski soovitame, et te Postita naaseb koos Storno.

## <a name="create-intercompany-return-orders"></a>Luua IC tagastuskorraldused
Tagastuskorraldused lõpule viia oma organisatsioonis kahe ettevõtte vahel. Toetatakse järgmistel juhtudel:

-   Lihtne kontsernisisese tagastab vahel kaks äriühingut, kes osalevad kontsernisisese seoses
-   Kontserniahela, mis on loodud kliendi tagastuskorralduse loomisel müügiettevõtte
-   Kontserniahela, mis on kehtestatud hankija tagastuskorralduse loomise ostmine firma
-   Otsetarne saadetise tagastab väliskliendi ja kaks äriühingut, kes osalevad kontsernisisese seoses

### <a name="setup"></a>Häälestus

Järgmisel joonisel miinimumseadistuse on vajalik kahe ettevõtte kontsernisisese seoses osalema ja Kontserni kaubavahetuse ära.  

[![Minimum setup](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn06.png)  

Järgmist stsenaariumi CompBuy on ostvale ettevõttele ja CompSell on müügiettevõte. Müüa ettevõte toome kauba ostvale ettevõttele või Otsetarne saadetise juhul otse lõpptarbijale. Aastal CompBuy, hankija IC\_CompSell määratletakse kontsernisiseste lõpp-punktiga seostatud ettevõtte CompSell. Samal ajal, CompSell, kliendi IC\_CompBuy määratletakse kontsernisiseste lõpp-punktiga seostatud ettevõtte CompBuy. Asjakohaseid meetmeid poliitika üksikasjad ja väärtuste vastendused määratlemist mõlemas ettevõttes. Otsetarne saadetise stsenaariumi puhul luuakse IC tagastuskorraldus, mis on ka kontsernisisene müügitellimus, müügiettevõte. RMA numbri IC tagastuskorralduse saab kätte alates CompSell RMA numbriseeria või seda saab kopeerida määratud algne tagastuskorralduse CompBuy RMA kood. RMA numbri seaded on **PurchaseRequisition** tegevuse poliitika CompBuy kindlaks need toimingud. Kui RMA kood on sünkroonitud, Planeerige number kokkupõrked riski vähendamiseks, kui kaks äriühingut kasutama sama numbriseeriat.

### <a name="simple-intercompany-returns"></a>Lihtne kontserni kasumit

Sel juhul kaasab kaks ühes organisatsioonis, nagu näidatud järgmisel joonisel.  

[![Lihtne kontsernisisese tulu](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn07.png)  

Tellimuse ahelat suudetakse tagastuskorralduse hankija loomisel ostvale ettevõttele või kliendi tagastuskorralduse luuakse müügiettevõte. Dynamics 365 toiminguteks kehtestatud nõuetele teises ettevõttes ning on kindel, et päise ja rea teavet hankija tagasi tellimuse kajastab kliendi seaded tagasi järjekorras. Tagastuskorralduse, mis asub saab kaasamiseks või viide (**leida müügitellimuse**) – olemasoleva kliendi arve. Saatelehtede ja arvete mõlemas saab töödelda eraldi. Näiteks ei ole saatelehe hankija tagastuskorralduse loomiseks enne luua kliendi tagastuskorralduse saatelehe.

### <a name="direct-delivery-shipment-returns-among-three-parties"></a>Otsetarne saadetise tagastab kolme osapoole vahel

Selle stsenaariumi suudetakse kui eelmise müügist ning **otsetarneks** tüüp on täidetud ja kui arve vastu kliendi olemas mis suhtleb kliendiga. Järgmises näites ettevõte CompBuy on varem müüdud ja arveldatud tooted kliendile Extern. Tooted lähetati kliendile kontsernisisese tellimuse ahelat kaudu otse firma CompSell.  

[![Otsetarne saadetise tagastab kolme osapoole vahel](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn08.png)  

Kui klient Extern soovib tagastada tooted, tagastuskorralduse (RMA02) on loodud kliendi ettevõtte CompBuy. Kontserniahela kindlakstegemiseks märgitakse tagasisaatmisotsust otsese pakkumise eest. Kui kasutate ning **leida müügitellimuse** valida kliendi arve saamiseks funktsiooni seatakse kontsernisisese tellimuse ahelat, mis koosneb järgmistest dokumentidest:

-   **Algne tagastuskorralduse:** RMA02 (firma CompBuy)
-   **Ostutellimus:** PO02 (firma CompBuy)
-   **Kontserni tagastuskorralduse:** RMA\_00032 (firma CompSell)

Otsetarne kontserniahela on loodud, füüsilist käitlemist ja andmete töötlemine peab toimuma raames IC tagastuskorraldus, RMA\_00032 ettevõtte CompSell. Tooteid ei saa vastu võtta ettevõtte CompBuy. Likvideerimise kood on määratud IC tagastuskorralduse, sünkroonitakse see algne tagastuskorralduse, et algne nõuetekohase arveldamiseks.

## <a name="post-to-the-ledger"></a>Pearaamatusse
Tagastuskorralduse arveldamisel luuakse pearaamatu sisestused on mõjutatud mõned olulised sätted ja parameetrid:

-   **Tagastamise omahind** – sest varude mudelid, välja arvatud **standardkulu**, et **tagastamise omahind** mδδrab kauba omahind on vastu tagasi võetud varude või maha kanda. Varude õige väärtuse arvutamiseks on oluline teie määratud selle **tagastamise omahind** parameeter õigesti. Kasutamisel on **leida müügitellimuse** funktsiooni tagastuskorralduse Real, mis on kliendi arve viite loomiseks on **tagastamise omahind** väärtus on võrdne müüdud kauba omahinda. Muul juhul omahind väärtus pärineb kauba seadistusest või saab käsitsi sisestada.
-   **Krediidi korrigeerimine/Storno** – teenuse **krediidi korrigeerimine** parameeter on **arve sisestamist** leht määrab, kas sisestuste registreeritud positiivsed (DR/CR) kanded või parandatakse, negatiivsed kanded.

Järgnevad näited tagastamise omahind on esindatud ka **arve omahind**.

### <a name="example-1-the-return-order-doesnt-reference-a-customer-invoice"></a>Näide 1: Tagasisaatmisotsust ei viidata kliendi arve

Tagasisaatmisotsust ei viidata kliendi arve. Tagastatud kauba krediteeritakse. Selle **krediidi korrigeerimine** parameeter ei ole valitud, tagastuskorralduse, arve või kreeditarve, loomisel.  

[![Tagastuskorralduse ei viidata kliendi invoic](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn09.png)  

**Märkus:** kapten müügihinna kasutatakse vaikimisi ka **tagastamise omahind** parameeter. Vaike hind erineb omahind lao väljamineku ajal. Seega järeldus on, et 3 kahju on tekkinud. Lisaks tagasisaatmisotsust ei sisalda kliendile antud müügitellimuse allahindluse. Seetõttu tekib liiga kõrge laenu.

### <a name="example-2-credit-correction-is-selected-for-the-return-order"></a>Näide 2: Kreeditiparandust valitakse tagastuskorraldus

Näide 2 on sama kui näide 1, kuid **krediidi korrigeerimine** parameetri valimise tagastuskorralduse arve loomisel.  

[![Kus valitakse kreeditiparandust tagastuskorraldus](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn10.png)  

**Märkus:** negatiivne parandusena sisestatakse pearaamatu sisestusi.

### <a name="example-3-the-return-order-line-is-created-by-using-the-find-sales-order-function"></a>Näide 3: Tagastuskorralduse Real on loodud müügitellimuse funktsiooni Otsi abil

Selle näite puhul luuakse tagastuskorralduse Real on **leida müügitellimuse** funktsiooni. Selle **krediidi korrigeerimine** parameeter ei ole valitud arve loomisel.  

[![Tagasi loomiseks kasutatakse otsingu müügitellimuse rea](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)](https://msdynamics.blob.core.windows.net/media/2017/02/SalesReturn11.png)  

**Märkus:****Soodus** ja **tagastamise omahind** on õiged. Seetõttu tekib täpne pöördumise kliendi arve.


