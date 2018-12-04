---
title: "Kvaliteedijuhtimise ülevaade"
description: "Selles teemas kirjeldatakse, kuidas kasutada Microsoft Dynamics 365 for Finance and Operationsis kvaliteedijuhtimist, et täiustada tarneahela toote kvaliteeti."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 79b3127f726a08cc24c20145b5ad9969157a899c
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="quality-management-overview"></a>Kvaliteedijuhtimise ülevaade

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas kasutada Microsoft Dynamics 365 for Finance and Operationsis kvaliteedijuhtimist, et täiustada tarneahela toote kvaliteeti.

Kvaliteedijuhtimise abil saate hallata ümberpööramise aegu, kui käsitsete mittevastavaid tooteid, olenemata nende päritolukohast. Kuna diagnostikatüübid on seotud parandustest teatamisega, saab Microsoft Dynamics 365 for Finance and Operations plaanida ülesandeid probleemide kõrvaldamiseks ja nende kordumise vältimiseks.

Lisaks mittevastavuste haldamiseks mõeldud funktsioonidele hõlmab kvaliteedijuhtimine funktsioone probleemide jälgimiseks probleemi tüübi alusel (isegi sisemiste probleemide puhul) ja lühiajaliste või pikaajaliste lahenduste tuvastamiseks. Tulemuslikkuse võtmenäitajate (KPI) statistika annab ülevaate varasematest mittevastavuse probleemidest ja nende kõrvaldamiseks kasutatud lahendustest. Saate kasutada varasemaid andmeid eelmiste kvaliteedimeetmete tulemuslikkuse ülevaatamiseks ja sobivate tulevikus kasutatavate meetmete määramiseks.

Kvaliteediseose seadistamisel saab Finance and Operations koostada kvaliteettellimusi mitmesugustele äriprotsessidele, sündmustele ja tingimustele. Kvaliteediseos võib hõlmata konkreetset kaupa, konkreetset kaubagruppi või kõiki kaupu.

## <a name="examples-of-the-use-of-quality-management"></a>Kvaliteedijuhtimise kasutamise näited
Kvaliteedijuhtimine on paindlik ja seda saab rakendada mitmesugusel moel, et järgida konkreetsete tarneahela toimingute tasemete nõudeid. Järgmised näited illustreerivad nende funktsioonide võimalikke kasutusviise.

-   Saate kvaliteedikontrolli protsessi automaatselt käivitada, tuginedes eelnevalt määratletud kriteeriumidele (konkreetse hankija ostutellimuse registreerimisel laos).
-   Kontrollimise ajal varude blokeerimine, et vältida heakskiitmata varude kasutamist (ostutellimuse koguste täielik blokeerimine).
-   Saate kasutada kauba valimit kvaliteediseose osana jooksvate füüsiliste varude hulga määratlemiseks, mida kontrollida tuleb. Valimi aluseks võib olla fikseeritud kogus või protsent.
-   Looge kvaliteettellimused osaliste tarnete jaoks. Kvaliteettellimuse loomiseks, mis põhineb tellimusega füüsiliselt saadud kogusel, peate märkima ruudu **Värskendatud koguse kohta** vormil **Kauba valim**.
-   Saate luua katsetüüpe, mis sisaldavad katse minimaalset, maksimaalset ja sihtväärtust ning teha kvalitatiivset vs kvantitatiivset kontrolli, millel on eelnevalt määratud valideerimistulemused.
-   Määrake sobiv kvaliteeditase (AQL) kvaliteedimeetme hälvete kontrollimiseks.
-   Saate määrata ressursid, mida kontrollimistoiming nõuab, nt katsepiirkond ja katseinstrumendid.

## <a name="working-with-quality-associations"></a>Kvaliteediseostega töötamine
Kvaliteediseost kasutav äriprotsess võib olla seotud mitmesuguste lähtedokumentidega, nt ostutellimuste, müügitellimuste või tootmistellimustega.

Iga kvaliteediseose kirje määrab ka katsete kogumi, AQL-i ning valikukava, mida rakendatakse loodud kvaliteettellimustele. Peate iga äriprotsessi variatsiooni jaoks määratlema kvaliteediseose kirje. Näiteks saate seadistada kvaliteediseose, mis koostab kvaliteettellimuse, kui ostutellimuse toote sissetulekut värskendatakse. Olenevalt käivitamisplaani seadistusest saab käivitusprotsessi enese blokeerida, kui on olemas avatud kvaliteettellimus, või saab blokeerida järgmised protsessid, nt ostutellimuse eest arve esitamise.

**Märkus.** avatud kvaliteettellimuste olemasolu korral blokeeritakse automaatselt varude koguste väljastamine. Olenevalt valiku **Täielik blokeerimine** seadistusest lehel **Kaubaproovid** on kogus kas kvaliteettellimusel olev kogus või lähtedokumendi real olev kogus.

Nimetatud äriprotsessi puhul määratleb kvaliteediseose kirje sündmuse ja tingimused, mille jaoks kvaliteettellimus on loodud. Tingimused võivad olla asukoha või juriidilise isiku põhised. Purustavaid katseid hõlmavat kvaliteettellimust saab luua ainult siis, kui sündmusel on olemas vaba laovaru.

Järgmistes näidetes on näha, kuidas kvaliteediseose kirjet määratakse iga äriprotsessi variatsioonide puhul. Iga näite puhul võetakse järgmises tabelis kokku sündmused ja tingimused, mis on kvaliteediseose kirjega määratletud.

<table>
<tbody>
<tr>
<th>Viite tüüp</th>
<th>Sündmuse tüüp</th>
<th>Käivitamine</th>
<th>Sündmuse blokeerimine</th>
<th>Dokumendi viide</th>
</tr>
<tr>
<td>Varud</td>
<td>Pole kohaldatav</td>
<td>Pole kohaldatav</td>
<td>Puudub</td>
<td>Kõik</td>
</tr>
<tr>
<td rowspan="7">Müük</td>
<td rowspan="4">Komplekteerimise protsess on plaanitud</td>
<td rowspan="4">Enne</td>
<td>Puudub</td>
<td rowspan="22">Ainult Konkreetne ID, Grupp või Kõik</td>
</tr>
<tr>
<td>Komplekteerimise protsess</td>
</tr>
<tr>
<td>Saateleht</td>
</tr>
<tr>
<td>Arve</td>
</tr>
<tr>
<td rowspan="3">Saateleht</td>
<td rowspan="3">Enne</td>
<td>Puudub</td>
</tr>
<tr>
<td>Saateleht</td>
</tr>
<tr>
<td>Arve</td>
</tr>
<tr>
<td rowspan="15">Ost</td>
<td rowspan="7">Sissetulekute loend</td>
<td rowspan="4">Enne</td>
<td>Puudub</td>
</tr>
<tr>
<td>Sissetulekute loend</td>
</tr>
<tr>
<td>Toote sissetulek</td>
</tr>
<tr>
<td>Arve</td>
</tr>
<tr>
<td rowspan="3">Pärast</td>
<td>Puudub</td>
</tr>
<tr>
<td>Toote sissetulek</td>
</tr>
<tr>
<td>Arve</td>
</tr>
<tr>
<td rowspan="3">Registreerimine</td>
<td rowspan="3">Pole kohaldatav</td>
<td>Puudub</td>
</tr>
<tr>
<td>Toote sissetulek</td>
</tr>
<tr>
<td>Arve</td>
</tr>
<tr>
<td rowspan="5">Toote sissetulek</td>
<td rowspan="3">Enne</td>
<td>Puudub</td>
</tr>
<tr>
<td>Toote sissetulek</td>
</tr>
<tr>
<td>Arve</td>
</tr>
<tr>
<td rowspan="2">Pärast</td>
<td>Puudub</td>
</tr>
<tr>
<td>Arve</td>
</tr>
<tr>
<td rowspan="8">Tootmine</td>
<td rowspan="3">Registreerimine</td>
<td rowspan="3">Pole kohaldatav</td>
<td>Puudub</td>
<td rowspan="12">Kõik</td>
</tr>
<tr>
<td>Teata lõpetamisest</td>
</tr>
<tr>
<td>Lõpp</td>
</tr>
<tr>
<td rowspan="5">Teata lõpetamisest</td>
<td rowspan="3">Enne</td>
<td>Puudub</td>
</tr>
<tr>
<td>Teata lõpetamisest</td>
</tr>
<tr>
<td>Lõpp</td>
</tr>
<tr>
<td rowspan="2">Pärast</td>
<td>Puudub</td>
</tr>
<tr>
<td>Lõpp</td>
</tr>
<tr>
<td rowspan="4">Vaheladu</td>
<td rowspan="3">Teata lõpetamisest</td>
<td rowspan="2">Enne</td>
<td>Teata lõpetamisest</td>
</tr>
<tr>
<td>Lõpp</td>
</tr>
<tr>
<td>Pärast</td>
<td>Lõpp</td>
</tr>
<tr>
<td>Lõpp</td>
<td>Enne</td>
<td>Lõpp</td>
</tr>
<tr>
<td rowspan="3">Protsessi operatsioon</td>
<td rowspan="3">Teata lõpetamisest</td>
<td rowspan="2">Enne</td>
<td>Puudub</td>
<td rowspan="3">Konkreetne ID, Grupp või Kõik ja Ressursipõhine, Grupp või Kõik</td>
</tr>
<tr>
<td>Teata lõpetamisest</td>
</tr>
<tr>
<td>Pärast</td>
<td>Puudub</td>
</tr>
<tr>
<td rowspan="3">Kaastoote tootmine</td>
<td>Registreerimine</td>
<td>Pole kohaldatav</td>
<td rowspan="3">Puudub</td>
<td rowspan="3">Kõik</td>
</tr>
<tr>
<td rowspan="2">Teata lõpetamisest</td>
<td>Enne</td>
</tr>
<tr>
<td>Pärast</td>
</tr>
</tbody>
</table>

Järgmises tabelis on veel teavet kvaliteettellimuste loomise kohta konkreetset tüüpi protsessidele.
<div class="tableSection">

<table>
<tbody>
<tr>
<th>Protsessi tüüp</th>
<th>Millal saab kvaliteettellimusi automaatselt luua</th>
<th>Millal saab kvaliteettellimusi luua, kui on vajalik purustav katsetamine</th>
<th>Tingimuse teave</th>
<th>Käsitsi loomise teave</th>
</tr>
<tr>
<td>Ostutellimus</td>
<td>Enne või pärast sissetulekute loendi või vastuvõetava materjali toote sissetuleku sisestamist</td>
<td>Pärast vastuvõetava materjali toote sissetuleku sisestamist, kuna materjal peab olema kättesaadav purustavaks katsetamiseks</td>
<td>Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või hankijat või nende tingimuste kombinatsiooni.</td>
<td>Käsitsi loodud ostutellimusele viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</td>
</tr>
<tr>
<td>Vahelao order</td>
<td>Enne või pärast vahelao tellimuse lõpetatuna kinnitamist või lõpetamist</td>
<td>Purustavaid katseid nõudvaid kvaliteettellimusi ei saa koostada. Eeldatakse, et vahelao tellimuse funktsioon tegeleb rikutud materjali likvideerimisega.</td>
<td>Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või hankijat või nende tingimuste kombinatsiooni.</td>
<td>Käsitsi loodud vahelaoorderile viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</td>
</tr>
<tr>
<td>Müügitellimus</td>
<td>Enne plaanitud komplekteerimisprotsessi või saatelehe uuendamist lähetatavate kaupade puhul</td>
<td>Igas etapis</td>
<td>Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või klienti või nende tingimuste kombinatsiooni.</td>
<td>Käsitsi loodud müügitellimusele viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</td>
</tr>
<tr>
<td>Tootmistellimus</td>
<td>Enne või pärast tootmistellimuse lõpetatud kogusest teatamist</td>
<td>Pärast tootmistellimuse lõpetatud kogusest teatamist</td>
<td>Kvaliteettellimuse vajadus võib kajastada konkreetset laoala või kaupa või nende tingimuste kombinatsiooni.</td>
<td>Käsitsi loodud tootmistellimusele viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</td>
</tr>
<tr>
<td>Tootmistellimus, millel on protsessitoiming</td>
<td>Enne või pärast toimingu aruande lõpetamist</td>
<td>Pärast viimase toimingu tootmise lõpetamisest teatamist</td>
<td>Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või operatsiooniressurssi või nende tingimuste kombinatsiooni.</td>
<td>Käsitsi loodud protsessitoimingule viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</td>
</tr>
<tr>
<td>Varud</td>
<td>Kvaliteettellimust ei saa automaatselt koostada varude töölehe kandele või üleviimistellimuse kandele.</td>
<td></td>
<td></td>
<td>Kvaliteettellimus tuleb kauba laokogusele käsitsi koostada. Nõutav on füüsiline vaba laovaru.</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a>Kvaliteedijuhtimise lehed
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Lehekülg</th>
<th>Kirjeldus</th>
<th>Näide</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kvaliteediseosed</td>
<td>Vt selle artikli varasemaid jaotisi.</td>
<td>Kvaliteediseos määratleb koostatava kvaliteettellimuse puhul kogu järgmise teabe.
<ul>
<li>Kande sündmus</li>
<li>Kaupade puhul tehtavate katsete kogum</li>
<li>AQL</li>
<li>Valimi plaan</li>
</ul>
Kvaliteediseos tuleb automaatset kvaliteettellimuse genereerimist nõudvas äriprotsessis määrata iga variatsiooni puhul. Näiteks saab kvaliteettellimuse koostada ostutellimuste, vahelaotellimuste, müügitellimuste ja tootmistellimuste äriprotsessides.</td>
</tr>
<tr class="even">
<td>Katsed</td>
<td>Määrake ja vaadake selle lehe abil üksikuid katseid, mis määratlevad, kas teie tooted vastavad kvaliteedispetsifikatsioonidele või mitte. Saate määrata katsegrupile vähemalt ühe eraldi katse. Sellisel juhul määrate ka testipõhised andmed, nt vastuvõetavad mõõtmisväärtused. Mõõtmisväärtusi kasutatakse kvantitatiivsete katsete puhul ja katsemuutujaid kasutatakse kvalitatiivsete katsete puhul.
<ul>
<li>Kvantitatiivse katse tüüp on <strong>täisarv</strong> või <strong>murd</strong> ja sellele on määratud ka mõõtühik. Kvaliteedispetsifikatsioone ja katsetulemusi väljendatakse numbritena.</li>
<li>Kvalitatiivse katse tüüp on <strong>valik</strong>. Kvalitatiivsed katsed nõuavad lisateavet mõõdetava katsemuutuja ja selle loetletud valikute kohta. Kvaliteedispetsifikatsioone ja katsetulemusi väljendatakse tulemuse järgi.</li>
</ul></td>
<td>Tootjaettevõte sooritab kaks katset ostetud materjaliga: kvantitatiivse katse materjali kvaliteedi kohta ja kvalitatiivne katse pakendikahjustuse kohta. Ettevõte määrab lisateabe kvalitatiivse katse kohta, et määratleda katse muutuja (kahjustatud pakend) ja selle tulemused. Ettevõte kasutab lehte <strong>Katsegrupid</strong>, et määrata katsegrupile kaks katset ning määrata katsepõhine teave. Katsegrupp määratakse kvaliteeditellimusele, nii et ettevõte saab teavitada kahe katse katsetulemustest.</td>
</tr>
<tr class="odd">
<td>Katsegrupid</td>
<td>Kasutage antud lehte katsegruppide ja katsegrupile määratud eraldi katsete seadistamiseks, redigeerimiseks ning vaatamiseks. Ülemine paan kuvab katsegruppe ja alumine paan kuvab valitud katsegruppi määratud katseid. Saate määrata katsegrupile mitmed põhimõtted nagu valimiplaani, vastuvõetava kvaliteeditaseme (AQL) ja nõuded purustavale katsetamisele. Kui määrate katsegrupile eraldi katse, määratlete lisateabe, näiteks järjestuse, dokumendid ja kehtivuse kuupäevad. Kvantitatiivse katse puhul sisaldab teie määratletud teave ka vastuvõetavaid mõõtmisväärtusi. Kvalitatiivse katse puhul sisaldab teave katsemuutujat ja vaiketulemust. Kvaliteettellimusele määratud katsegrupp määratleb katsete vaikekogumi, mis tuleb määratud kaubaga sooritada. Kuid saate kvaliteettellimuse katseid lisada, kustutada või muuta. Iga katse tulemused kinnitatakse kvaliteettellimuses.</td>
<td>Tootmisettevõte määrab iga kvaliteetjuhise variandi puhul katsegrupi. Erinevad katsegrupid näitavad erinevusi valimiplaanides, katsehulkasid, mida peab koos läbi viima, vastuvõetavat kvaliteeditaset ja muid tegureid. Kvantitatiivsete katsete puhul on erinevused ka vastuvõetavates mõõteväärtustes. Kvaliteedipõhimõtteid järgides määrab ettevõte igale reeglile katsegrupi, et koostada automaatselt kvaliteettellimusi lehel <strong>Kvaliteediseosed</strong>, ja määrab katsegrupi ka käsitsi loodud kvaliteettellimustele.</td>
</tr>
<tr class="even">
<td>Üksuse kvaliteedigrupid</td>
<td>Kasutage seda lehte, et seadistada, redigeerida ja vaadata kaupu, mis on määratud kaubale määratud kvaliteedigrupile või kvaliteedigruppidele. Kvaliteedigrupp tähistab kaupade üldisi testimisnõudeid. Pärast katsenõuete määratlemist lehel <strong>Katsegrupid</strong> saate määratleda reeglid kvaliteettellimuste automaatseks koostamiseks. Protsessi hõlbustamiseks ei määratleta reegleid üksikutele kaupadele. Selle asemel määratletakse reeglid kvaliteedigrupile, kasutades lehte <strong>Kvaliteediseosed</strong>. Saate kasutada valitud kvaliteedigrupi puhul ka lehte <strong>Kauba kvaliteedigrupid</strong> sobivate kaupade määramiseks sellesse gruppi. Saate kasutada valitud kauba puhul ka lehte <strong>Kauba kvaliteedigrupid</strong> sobivate kvaliteedigruppide määramiseks sellele kaubale.</td>
<td>Tootmisettevõte ostab mitmesuguseid ühesuguste sissetulekukontrolli katsenõuetega toormaterjale. Ettevõte määrab kvaliteedigrupi ja määrab sellele grupile toormaterjaliga seotud kaubakoodid. Hiljem ostab ettevõte uut tüüpi toormaterjali, millel on samad katsenõuded. Selle asemel, et seadistada uuele materjalile uued katsenõuded, lisab ettevõte uue materjali kaubakoodi olemasolevasse kvaliteedigruppi. Sama tootmisettevõte toodab ka ühesuguste tootmisalaste katsenõuetega kaupu ja lähetab ühesuguste nõuetega kaubad lähetuseelsete katsete tegemiseks. Ettevõte määrab kaks täiendavat kvaliteedigruppi ja määrab seejärel igale grupile sobivad kaubakoodid.</td>
</tr>
<tr class="odd">
<td>Katse muutujad</td>
<td>Sellel lehel saate määratleda ja kuvada kvalitatiivse katsega seotud muutujaid. Iga muutuja puhul saab määratleda nummerdatud tulemused, mis kajastavad võimalikke valikuid. Saate määratleda katsed lehel <strong>Katsed</strong>. Kvalitatiivsete katsete puhul peate määrama katsetüübi <strong>Valik</strong>. Kasutage lehte <strong>Katsegrupid</strong> katse muutuja määramiseks individuaalsele katsele.</td>
<td>Küpsiseid valmistav tootmisettevõte kasutab valmistoote kontrollkatset. Sellel kontrollkatsel on mitu muutujat. Üks muutuja on maitse ja selle muutuja võimalikud väärtused on hea ja halb. Teine muutuja on värvus ja võimalikud tulemused on liiga tume, liiga hele ja õige.</td>
</tr>
<tr class="even">
<td>Katse muutuja väljundteated</td>
<td>Kasutage seda lehte kvalitatiivse katsega seotud muutuja võimalike katsetulemuste seadistamiseks, redigeerimiseks ja vaatamiseks. Iga tulemuse puhul tuleb määrata olek <strong>läbis</strong> või <strong>ei läbinud</strong>. Peate määrama muutuja ja tema väljundid iga kvalitatiivse katse jaoks, mis on määratud lehel <strong>Katsed</strong>. (Kvalitatiivsete katsete puhul on katse tüübiks määratud <strong>Valik</strong> lehel <strong>Katsed</strong>.) Kasutage lehte <strong>Katsegrupid</strong> katsemuutuja ja vaikeväärtuse määramiseks kindlale kvalitatiivsele katsele.</td>
<td>Küpsiseid valmistav tootmisettevõte kasutab valmistoote kontrollkatset. Sellel kontrollkatsel on mitu muutujat. Üks muutuja on maitse ja selle muutuja võimalikud väärtused on hea ja halb. Teine muutuja on värvus ja võimalikud tulemused on liiga tume, liiga hele ja õige. Igale tulemusele omistatakse väärtus <strong>läbis</strong> või <strong>ei läbinud</strong>. Iga muutuja kontrolltesti ajal registreerib katsetaja katse tulemuse, valides ühe väljundi väärtustest.</td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a>Lisaressursid
--------

[Kvaliteedijuhtimise protsessid](quality-management-processes.md)

[Mittevastavuse haldamise võimaldamine](enable-nonconformance-management.md)

