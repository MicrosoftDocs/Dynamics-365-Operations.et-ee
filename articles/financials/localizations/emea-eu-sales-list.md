---
title: "EL-i käibearuandlus"
description: "Selles artiklis antakse teavet Euroopa Liidu (EL-i) käibearuande aruandluse kohta."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EUSalesList
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 12811
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e1eff86902170401e593019ea555d9c2a4c11c04
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="eu-sales-list-reporting"></a>EL-i käibearuandlus

[!INCLUDE [banner](../includes/banner.md)]

Selles artiklis antakse teavet Euroopa Liidu (EL-i) käibearuande aruandluse kohta.

<a name="eu-sales-list-reporting"></a>EL-i käibearuandlus
-----------------------

Tarnija, kes tarnib Euroopa Liidus (EL) loodud ettevõtetele EL-i siseseid kaupu või teenuseid, peab esitama EL-i siseste tarnete deklaratsiooni (EL-i käibearuanne või ESL). Üldjuhul tuleb esitada ESL maksuametile hiljemalt ESL-i kaetavale kalendriperioodile järgneva kuu viimasel päeval. Tarnija peab teatama ESL-i käibemaksu (KM) ID-numbri ja samuti kliendi kaupa järgmise teabe.

-   EL-i kliendi KM-i ID-number
-   Sellel perioodil EL-i klientidele tehtud EL-i siseste kaupade ja teenuste koguväärtus. Tarnija peab eraldama üldise kaubatarne ja triangulatsioonkaubandustarne. Triangulatsioonkaubanduse kanne hõlmab kauba otsetarnet tarnija tarnijalt kliendile, kui mõlemad osapooled on registreeritud muudes EL-i liikmesriikides.

ESL-i kasutades saavad iga EL-i liikmesriigi ametnikud kontrollida, kas iga EL-i sisese kande puhul on makstud käibemaksu. Loendite ja käibemaksutagastuste kombinatsioon võimaldab EL-i liikmesriikide teabevahetust kaupade liikumise kohta kogu EL-is.

## <a name="overview-of-the-eu-sales-list-reporting-process"></a>Ülevaade EL-i käibearuande protsessist
EL-i käibearuanne võimaldab teha järgmisi toiminguid.

-   Koguda teavet EL-i siseste kaubanduskannete kohta. EL-i sisene kaubanduskanne võib olla müügiarve, vabas vormis arve, projekti arve või hankija arve. Kanne tuvastatakse vastaspoole riigi/regiooni alusel. Eri tüüpi EL-i sisesed kaubakanded kogutakse EL-i käibearuande tabelisse, kus neid esitatakse tavavormis. ESL-i tabeli iga kirje esindab ühte kannet ja koosneb vastaspoole käibemaksu identifikaatorist ning tarnitud kaupade ja teenuste koguväärtusest.
-   (Valikuline) Eelvaadata **EL-i käibearuannet**. Saate eelvaadata ja kinnitada antud perioodi **EL-i käibearuande** Microsoft Exceli töövihiku vormis.
-   Luua **EL-i käibearuanne**. **EL-i käibearuanne** luuakse elektroonilise faili vormis konkreetses vormingus, mis on iga EL-i liikmesriigi puhul ainuomane. Üldiselt sisaldab **EL-i käibearuanne** põhiteavet aruandluse osapoole kohta ning kaupade ja teenuste väärtuste kohta. Teave on rühmitatud riigi ja vastaspoole KM-i identifikaatori järgi.
-   Sulgeda EL-i käibearuande aruandlusperioodi. Pärast **EL-i käibearuande** loomist ja ametiasutustele esitamist saate märkida ESL-i tabeli kirjete olekuks **Suletud**. Neid kandeid ei kaasata lisaaruannetesse.

## <a name="prerequisites"></a>Eeltingimused 
Järgmises tabelis kuvatakse eeltingimused, mis peavad olema asukohakorralduse loomiseks täidetud.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategooria</th>
<th>Eeltingimus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Seadistus:</strong> juriidiline isik</td>
<td>Juriidilise isiku peamine aadress peab olema ELi liikmesriigis. Valige juriidiline isik lehel <strong>Juriidilised isikud</strong> (klõpsake valikuid <strong>Organisatsiooni haldus</strong> &gt; <strong>Organisatsioonid</strong> &gt; <strong>Juriidilised isikud</strong>). Kiirkaardil <strong>Aadressid</strong> looge aadress, valige riik/regioon ja muud aadressi osad ning märkige aadressi olekuks <strong>Esmane</strong>. Kiirkaardi <strong>Maksu registreerimine</strong> väljal <strong>Maksu registreerimisnumber</strong> määrake oma ettevõtte maksu registreerimisnumber.</td>
</tr>
<tr class="even">
<td><strong>Seadistus:</strong> maksuvabastuse ID parameetrid</td>
<td>Seadistage maksuvabastuse ID parameetrid lehel <strong>Riigi/regiooni parameetrid</strong> (klõpsake valikuid <strong>Maks</strong> &gt; <strong>Seadistus</strong> &gt; <strong>Käibemaks</strong> &gt; <strong>Riigi/regiooni parameetrid</strong>). Looge igale riigile/regioonile, kus teil on vastaspooli, lehele kirje ja lisage järgmine teave.
<ul>
<li><strong>Riik/regioon</strong> – valige riik/regioon, mis seostatakse maksuvabastuse ID-ga.</li>
<li><strong>Käibemaks</strong> – sisestage valitud riigi/regiooni maksuvabastuse ID-number (s.o maksukohuslase koodi eesliide).</li>
<li><strong>Kontrolli maksukohuslase koodi</strong> – valige see märkeruut, et kinnitada valitud riigi/regiooni maksuvabastuse ID.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Seadistus: </strong>maksukohuslase koodid</td>
<td>Looge vastaspooltele maksukohuslase koodid lehel <strong>Maksukohuslase koodid</strong> (klõpsake valikuid <strong>Maks</strong> &gt; <strong>Seadistus</strong> &gt; <strong>Käibemaks</strong> &gt; <strong>Maksukohuslase koodid</strong>). Looge iga maksukohuslase koodi kohta lehel kirje ja lisage järgmine teave.
<ul>
<li><strong>Riik/regioon </strong>– valige vastaspoole maksu registreerimise riik/regioon.</li>
<li><strong>Maksukohuslase kood</strong> – sisestage vastaspoole maksukohuslase kood.</li>
<li><strong>Ettevõtte nimi</strong> – (valikuline) sisestage vastaspoole nimi.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Seadistus: </strong>vastaspoolte maksu registreerimine</td>
<td>Seadistage vastaspoolte maksu registreerimise teave kas lehel <strong>Kõik kliendid</strong> (klõpsake valikuid <strong>Müük ja turundus</strong> &gt; <strong>Kliendid</strong> &gt; <strong>Kõik kliendid</strong>, valige kliendi kirje ja klõpsake siis valikuid <strong>Suvandid</strong> &gt; <strong>Muuda vaadet</strong> &gt; <strong>Üksikasjade vaade</strong>) või lehte <strong>Hankijad</strong> (klõpsake valikuid <strong>Hanked</strong> &gt; <strong>Hankijad</strong> &gt; <strong>Hankijad</strong>, valige hankija kirje ja klõpsake siis valikuid <strong>Suvandid</strong> &gt; <strong>Muuda vaadet</strong> &gt; <strong>Üksikasjade vaade</strong>). Valige kiirkaardi <strong>Arve ja tarne</strong> väljal <strong>Maksukohuslase kood</strong> maksu registreerimise number.</td>
</tr>
<tr class="odd">
<td><strong>Seadistus: </strong>käibemaks</td>
<td>Seadistage <strong>EL-i käibearuandesse</strong> kaasatavad maksukoodid lehel <strong>Käibemaksukoodid</strong> (klõpsake valikuid <strong>Maks</strong> &gt; <strong>Kaudsed maksud</strong> &gt; <strong>Käibemaks</strong> &gt; <strong>Käibemaksukoodid</strong>). Tühjendage kiirkaardil <strong>Aruande seadistus</strong> iga aruandesse kaasatava käibemaksukoodi puhul märkeruut <strong>Välistatud</strong>. Seadistage kaupade käibemaksu parameetrid lehel <strong>Kauba käibemaksugrupid</strong> (klõpsake valikuid <strong>Maks</strong> &gt; <strong>Kaudsed maksud</strong> &gt; <strong>Käibemaks</strong> &gt; <strong>Kauba käibemaksugrupid</strong>). Valige iga kauba käibemaksugrupi puhul väärtus väljal <strong>Aruandluse tüüp</strong>. Valitud väärtus määrab ESL-i summaveeru, kuhu lisatakse rea summa.
<ul>
<li><strong>Tühi</strong> – rea summa lisatakse veergu <strong>Määramata väärtus</strong>.</li>
<li><strong>Kaup</strong> – rea summa lisatakse veergu <strong>Kauba väärtus</strong>.</li>
<li><strong>Teenus</strong> – rea summa lisatakse veergu <strong>Teenuse väärtus</strong>.</li>
<li><strong>Investeering</strong> – rea summa lisatakse veergu <strong>Investeeringu väärtus</strong>. See veerg on asjakohane ainult Belgias.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Seadistus:</strong> ESL-i aruandluse konfiguratsioonid</td>
<td>ESL-ile elektroonilise aruandluse konfiguratsioonide importimine või loomine Elektroonilise aruandluse konfiguratsioonide loomise ja hooldamise kohta vaadake teavet elektroonilise aruandluse dokumentatsioonist.</td>
</tr>
<tr class="odd">
<td><strong>Seadistus: </strong>üldised parameetrid</td>
<td>Seadistage ESL-i aruandluse parameetrid lehel <strong>Väliskaubanduse parameetrid</strong> (klõpsake valikuid <strong>Maks</strong> &gt; <strong>Seadistus</strong> &gt; <strong>Väliskaubandus</strong> &gt; <strong>Väliskaubanduse parameetrid</strong>). Määrake järgmised parameetrid.
<ul>
<li>Vahekaart <strong>EL-i käibearuanne</strong>.
<ul>
<li><strong>Skontoaruandlus</strong> – valige see märkeruut, kui skonto tuleb kande kaasamisel ESL-i väärtusele lisada.</li>
<li><strong>Ostude ülekandmine</strong> – valige see märkeruut, et kaasata ostud ESL-i.</li>
<li><strong>Failivormingu vastendus</strong> – valige kasutatav elektroonilise aruandluse vormingu juhuks, kui ESL-ile luuakse elektrooniline fail.</li>
<li><strong>Aruandevormingu vastendus</strong> – valige kasutatav elektroonilise aruandluse vorming juhuks, kui ESL-ile luuakse eelvaate aruanne.</li>
<li><strong>Ümardamisreegel</strong> – määrake ümardamiseks reaalne number. ESL-i summad ümardatakse selle numbri kordseteks.</li>
<li><strong>Ümardamismeetod</strong> – valige kasutatav ümardamismeetod juhuks, kui ümardatakse ESL-i summasid (<strong>Tavaline</strong>, <strong>Allapoole</strong> või<strong>Ümardamine</strong>).</li>
<li><strong>Kasuta miinimumväärtust</strong> – valige see märkeruut, kui soovite, et summad, mis on väiksemad kui number <strong>Ümardamisreegel</strong>, ümardataks numbriks <strong>Ümardamisreegel</strong>.</li>
<li><strong>Kümnendkohtade arv</strong> – määrake kümnendkohtade arv, mida näidatakse ESL-i summades (nii elektroonilistes failides kui ka <strong>ESL-i eelvaate</strong> aruandes).</li>
</ul></li>
<li>Vahekaart <strong>Riigi/regiooni parameetrid</strong>: tuvastage EL-i liikmesriigid. Looge iga EL-i liikmesriigi kohta lehel kirje ja lisage järgmine teave.
<ul>
<li><strong>Riik/regioon</strong> – valige riik/regioon.</li>
<li><strong>Riigi/regiooni tüüp</strong> – kui suvandi <strong>Riik/regioon</strong> väärtus on riik/regioon, kuhu teie ettevõte on registreeritud, tehke valik <strong>Kodumaine</strong>. Kui suvandi <strong>Riik/regioon</strong> väärtus ei ole EL-i liikmesriik, kuhu teie ettevõte registreeritud on, tehke valik <strong>EL</strong>. Kui suvandi <strong>Riik/regioon</strong> väärtus ei ole EL-i liikmesriik, tehke valik <strong>Kolmas riik/regioon</strong>.</li>
</ul></li>
<li>Vahekaart <strong>Numbriseeriad</strong>: valige real, kus suvandi <strong>Viide</strong> väärtus on <strong>EL-i käibearuanne</strong>, numbriseeria kood.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Seotud kanded</strong></td>
<td><ul>
<li>Registreerige müük kliendile muus EL-i liikmesriigis.</li>
<li>Registreerige vabas vormis arve kliendile muus EL-i liikmesriigis.</li>
<li>Registreerige projekti arve kliendile muus EL-i liikmesriigis.</li>
<li>Registreerige arve hankijalt muus EL-i liikmesriigis.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="working-with-the-esl"></a>ESL-iga töötamine
### <a name="collecting-information-about-intra-community-trade-transactions"></a>EL-i siseste kaubanduskannete kohta teabe kogumine

Järgmist tüüpi kandeid saab nimetada EL-i sisesteks kaubanduskanneteks.

-   Müügiarved
-   Vabas vormis arved
-   Projektiarved
-   Hankijaarved

Kannet peetakse EL-i siseseks kaubanduskandeks, kui kande tarneaadress on EL-i liikmesriigis. Selliste riikide/regioonidep kohta peab olema kirje lehe **Väliskaubanduse parameetrid**  vahekaardil **Riigi/regiooni parameetrid** ja suvandi **Riigi/regiooni tüüp** väärtus peab olema **EL**. EL-i sisesed kaubanduskanded on väljal **Loendi kood** märgitud. Seda välja kasutades saate eraldada ka üldised EL-i sisesed kaubanduskanded triangulatsioonkaubanduse kannetest. Saate koguda teavet EL-i siseste kaubanduskannete kohta lehel **EL-i käibearuanne** (klõpsake valikuid **Maks** &gt; **Deklaratsioonid** &gt; **Väliskaubandus** &gt; **EL-i käibearuanne**), kasutades funktsiooni **Ülekanne**. Selle funktsiooni abil saate kaasata kanded, millel on mitmeid erinevaid aruandluse tüüpe (s.o kaubad või teenused) vastavalt kauba käibemaksugruppidele, mis on kanderidadel määratud. Samuti saate rakendada muid filtreid, et määratleda kaasatavaid kandeid. Funktsioon **Ülekanne** loob lehel **EL-i käibearuanne** kirje igale kaasatud EL-i sisesele kaubanduskandele ja määrab vastaspoole kontonumbri, riigi/regiooni, maksukohuslase koodi, arve numbri ja kuupäeva ning ridade kogusumma aruandluse tüübi kohta. See kopeerib kandest ka väärtuse **Loendi kood**. Saate käsitsi muuta kande loendi koodi lehel **EL-i käibearuanne**. Funktsioon **Ülekanne** loob kirjed, kui väärtus **Aruandluse olek** on olekus **Kaasatud**. Saate kinnitada teabe, mida kogutakse lehel **EL-i käibearuanne**, kasutades funktsiooni **Kinnitamine**.

### <a name="generating-the-eu-sales-list-report"></a>EL-i käibearuande loomine

Saate luua aruande **EL-i käibearuanne**, kasutades funktsiooni **Aruandlus**lehel **EL-i käibearuanne**. Selle funktsiooniga saate valida aruandlusperioodi ja rakendada filtreid kaasatavate ESL-i kirjete määratlemiseks. Lisaks saate määrata muid parameetreid, mis on igas riigis/regioonis ainuomased. Saate luua ka eelvaate aruande, elektroonilise faili või mõlemad. Funktsioon **Aruandlus**kasutab aruande ja failivormingu sätteid, mis on määratud lehel **Väliskaubanduse parameetrid**. Üldiselt koosneb **EL-i käibearuanne** eraldi ridadest, mis loetlevad kaupade kogusummad vastaspoole riigi/regiooni, maksukohuslase koodi ja aruandluse tüübi (kaasatud on triangulatsioonkaubanduse kanded) kohta. Pärast konkreetse perioodi kohta **EL-i käibearuande** loomist saate märkida aruandesse kaasatud ESL-i kirjed, seadistades väärtuse **Aruandluse olek** olekuks **Esitatud**. Selle oleku seadistamiseks kasutage funktsiooni **Märgi esitatuks**lehel **EL-i käibearuanne**.

### <a name="closing-the-eu-sales-list-reporting-period"></a>EL-i käibearuande aruandlusperioodi sulgemine

Kui olete lõpetanud konkreetse perioodi aruandlusprotsessi (näiteks kui maksuametnikud on **EL-i käibearuande** kinnitanud), saate märkida ESL-i kirjed, mis on perioodil aruandesse kaasatud, seadistades väärtuse **Aruandluse olek** olekuks **Suletud**. Kasutage selle oleku määramiseks funktsiooni **Märgi suletuks**lehel **EL-i käibearuanne**. Kui ennistate perioodi lõpetamise, saate märkida ESL-i kirjed, seadistades suvandi **Aruandluse olek** väärtuseks **Kaasatud**. Need kirjed saab siis uuesti **EL-i käibearuandesse** lisada. Selle oleku seadistamiseks kasutage funktsiooni **Märgi** **kaasatuks**lehel **EL-i käibearuanne**.




