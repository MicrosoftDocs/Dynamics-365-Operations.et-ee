---
title: Intrastati ülevaade
description: Selles teemas antakse teavet Euroopa Liidu riikide/regioonide vahelise kauba- ja mõnel juhul teenuste vahetuse intrastati aruandluse kohta. Antakse ülevaade aruandlusprotsessist ning kirjeldatakse nõutavaid sätteid ja eeltingimusi.
author: EvgenyPopovMBS
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Intrastat
audience: Application User
ms.reviewer: kfend
ms.custom:
- "28581"
- intro-internal
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 49433b2eba225c3c45a01b0c28045873b20cf2ba7357fbebc6b5a1814d533bb3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774233"
---
# <a name="intrastat-overview"></a>Intrastati ülevaade

[!include [banner](../includes/banner.md)]

Selles teemas antakse teavet Euroopa Liidu riikide/regioonide vahelise kauba- ja mõnel juhul teenuste vahetuse intrastati aruandluse kohta. Antakse ülevaade aruandlusprotsessist ning kirjeldatakse nõutavaid sätteid ja eeltingimusi.

Intrastat on Euroopa Liidu (EL-i) riikide/regioonide vahelise kaubavahetuse teabe kogumise ja statistika koostamise süsteem. Intrastat-aruandlus on nõutav, kui toote ületab teise ELi riigi/regiooni piiri. Mitmes riigis/regioonis kehtib Intrastat-aruandlus ka teenustele. Intrastat-aruandluses võidakse koguda kohustuslikke ja valikulisi elemente. Järgmised elemendid on kohustuslikud: teabe esitamise eest vastutava osapoole käibemaksukohustuslase number, viiteperiood, voog (saabumine või lähetamine), kaheksakohaline kaubakood, partneri liikmesriik (saatmise liikmesriik saabumise puhul ja lähetuste puhul sihtliikmesriik), kauba väärtus, kaubakogus (netomass ja täiendav ühik) ning kande iseloom. Riigid/regioonid võivad koguda mitmesugustel tingimustel ka valikulisi elemente. Mõned valikulised elemendid on päritoluriik/-regioon, tarnetingimused, transpordiliik, üksikasjalikum kaubakood kui CN8, lähetuste puhul lähtepiirkond ja saabumiste puhul sihtpiirkond, statistiline protseduur, statistiline väärtus, kauba kirjeldus ja laadimise/mahalaadimise sadam/lennujaam.

## <a name="overview-of-the-intrastat-reporting-process"></a>Intrastat-aruandluse protsessi ülevaade
Järgmised jaotised kirjeldavad üldist teabevoogu, mida Intrastat-aruandluses kasutatakse.

### <a name="1-enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a>1. Sisestage kanne, mis ületab teise ELi riigi/regiooni piiri

Kliendiarve, vabas vormis arve, ostuarve, projektiarve, kliendi saateleht, hankija toote sissetulek või üleviimistellimus edastatakse Intrastati töölehele ainult juhul, kui sihtkoha (lähetuste puhul) või lähtekoha (saabumiste puhul) riigi/regiooni sihtkoha tüüp on **EU**. Seda funktsiooni laiendati Microsoft Dynamics 365 for Operationsile (1611) ja see võimaldab teil määrata laadimisaadressid ELi-siseste kannete jaoks. Kui laadimisaadress erineb hankija ettevõtte aadressist (või kliendi ettevõtte aadressist tagastustellimuse puhul), kasutab Intrastati aruandlus seda teavet. Kui loote müügitellimuse, vabas vormis arve, ostutellimuse, hankijaarve, projektiarve või üleviimistellimuse, on mõnel väliskaubandusega seotud väljal dokumendi päises või real vaikeväärtused. Kandekoodi vaikeväärtus võetakse lehe **Väliskaubanduse parameetrid** vastavalt väljalt. Kaubakoodi, päritoluriigi/-regiooni ja päritolumaakonna/-provintsi vaikeväärtused võetakse kaubalt. Vaikeväärtusi saab muuta ja lisada saab ka muud väliskaubandusega seotud teavet: statistikaprotseduuri, transporti ja sadamat.

### <a name="2-use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a>2. Looge Intrastati töölehe abil ELi riikide/regioonide vahelise kaubavahetuse teave.

Statistilistel eesmärkidel luuakse ELi riikide/regioonide vahelise kaubavahetuse teave iga kuu. Kandeid saab edastada vabas vormis arvelt, kliendiarvelt, kliendi saatelehelt, hankija arvelt, hankija saatelehelt, projekti arvelt või üleviimistellimuselt, lehel **Väliskaubanduse parameetrid** seadistatud edastuskriteeriumide alusel. Kandeid saab sisestada ka käsitsi. Saate edastatud kandeid Intrastati töölehel käsitsi muuta, kui muutmine on vajalik. Konkreetsete tingimuste alusel, mis on seadistatud lehel **Intrastati tihendamine**, saate tihendada Intrastati töölehe kandeid. Mõnes riigis/regioonis on teil lubatud kohaldada väikest kande läve. Seejärel saate edastada aruandesse kandeid, mis jäävad määratud kaubakoodi all sellest lävest allapoole. Saate muuta kaubakoodi vastavatel Intrastati töölehe ridadel, tuginedes sättele **Alampiir** lehel **Väliskaubanduse parameetrid**. Saate neid kandeid sätte **Intrastati tihendamine** alusel ka tihendada. Saate kinnitada Intrastati töölehel olevate kannete terviklikkuse sätte **Kontrolli seadistust** põhjal lehel **Väliskaubanduse parameetrid**. Vastavatel väljadel olevate andmete terviklikkust saab kontrollida: riik/regioon, maakond või provints, kaal, kaubakood, kande kood, täiendav ühik, sadam, lähtekoht, tarnetingimus, transpordiliik ja maksuvabastuse number. Kanded, mida ei ole lõpule viidud, märgitakse kehtetuks.

### <a name="3-use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a>3. Koostage Intrastati töölehe abil ELi riikide/regioonide vahelise kaubavahetuse aruanne.

Statistilistel eesmärkidel koostatakse ELi riikide/regioonide vahelise kaubavahetuse aruanne iga kuu. Saate Intrastat-aruande välja printida, tuginedes lehe **Aruande vormingu vastendamine** sätetele lehel **Väliskaubanduse parameetrid**. Saate luua ka elektroonilise faili, tuginedes lehe **Failivormingu vastendamine** sätetele lehel **Väliskaubanduse parameetrid**. Lisateavet Intrastati aruandluse, sh nõutavate eeltingimuste kohta vaadake Intrastati aruandluse tegevuse salvestistest.

-   EL-i Intrastati deklaratsiooni loomine.
-   Kannete ülekandmine Intrastati.
-   Laadimisaadressi määramine ühendusesisesele kandele.

## <a name="prerequisites"></a>Eeltingimused
Järgmises tabelis on loetletud Intrastati aruandluse eeltingimused.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Eeltingimus</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Aadressi häälestamine</td>
<td>Saate seadistada riikide/regioonide ISO (Rahvusvahelise Standardiorganisatsiooni) koodid.</td>
</tr>
<tr class="even">
<td>Juriidiline isik</td>
<td>Saate seadistada impordi/ekspordi maksuvabastuse numbrid, impordi/ekspordi filiaali koodi laiendi ja juriidilisele isikule määratud Intrastati koodi.</td>
</tr>
<tr class="odd">
<td>Toote kategooriahierarhia (müügihierarhia, hankehierarhia)</td>
<td>Saate määrata Intrastati kaubakoodid kategooriasõlmedele vahekaardil <strong>Kaubakoodid</strong> lehel <strong>Kategooriahierarhia</strong>. Kui määrate kaubakoodi peamisele kategooriasõlmele, kehtib see kood kõigile kategooria alamsõlmedele. Valitud kaubakoodid on saadaval vaates <strong>Valitud</strong> kui valite väljastatud toote üksikasjades ja müügitellimuse, ostutellimuse ja üleviimistellimuse ridadel kaubakoodi.</td>
</tr>
<tr class="even">
<td>Väljastatud toote üksikasjad</td>
<td>Saate seadistada järgmised väljastatud toodete väliskaubanduse andmed.
<ul>
<li><strong>Kaubakood</strong> – valige määratud tootekategooriatest toodud valitud kaupade loendist või Intrastati kaubakoodide tervikloendist.</li>
<li><strong>Statistiliste tasude protsent</strong></li>
<li><strong>Päritoluriik/-regioon</strong> – saate valida vaikeriigi/-regiooni, kust kaup täielikult hangiti või kus see toodeti.</li>
<li><strong>Lähte-/sihtmaakond/-provints</strong> – valige sihtmaakonna/-provintsi vaikeväärtus saabumiste puhul ja lähtemaakond/-provints lähetuste puhul.</li>
<li><strong>Netokaal (kg)</strong></li>
<li><strong>Välista</strong> - selle parameetri lubamiseks ei tohi selle tootega kandeid intrastati üle kanda</li>
</ul></td>
</tr>
<tr class="odd">
<td>Kliendid</td>
<td>Saate seadistada kliendi tarneaadressi ELi riigis/regioonis.</td>
</tr>
<tr class="even">
<td>Hankijad</td>
<td>Saate seadistada hankija aadressi ELi riigis/regioonis.</td>
</tr>
<tr class="odd">
<td>Mitmesugused tasud</td>
<td>Saate seadistada lisakulude koodi arve summale, statistilisele summale või mõlemale lisamiseks. Aktiveerige lehel <strong>Tasukoodid</strong> vahekaardil <strong>Väliskaubandus</strong> valik <strong>Intrastati arve väärtus</strong>, et kaasata tasusumma arve väärtusse, ja aktiveerige valik <strong>Intrastati statistiline väärtus</strong> tasusumma kaasamiseks statistilisse väärtusse.</td>
</tr>
<tr class="even">
<td>Elektrooniline aruandlus</td>
<td>Saate seadistada elektroonilise aruandluse konfiguratsioonid Intrastati andmete eksportimiseks elektroonilisse faili, mis on vastavate asutuste nõutavas vormingus, ja Intrastati andmete eelvaate kuvamiseks kasutajasõbralikus, loetavas vormingus (nt Microsoft Excelis).</td>
</tr>
<tr class="even">
<td>Ladustamine</td>
<td>Saate seostada hankijakontosid laokoodidega maksukohustuslase koodi lisamiseks üleviimistellimuse üleviimisel.</td>
</tr>
</tbody>
</table>

## <a name="setup"></a>Seadistamine
Järgmised jaotised kirjeldavad sätteid, mida on Intrastat-aruandluse jaoks vaja.

### <a name="set-up-all-required-intrastat-related-lists"></a>Kõigi vajalike Intrastatiga seotud loendite seadistamine

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Loend</th>
<th>Lisateave</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kaubaartiklite koodid</td>
<td>Saate seadistada kategooriahierarhia tüübiga <strong>Kaubakood</strong> ja sisestada kõik kaubakoodid kombineeritud nomenklatuuriloendi alusel. Iga kauba kohta saate seadistada järgmise teabe.
<ul>
<li>Kauba nimi ja kaubakood</li>
<li>Hüüdnimi ja/või tõlgitud nimi</li>
<li>Lisaühikute (täiendavate ühikute) aruandluse sätted vahekaardil <strong>Väliskaubandus</strong>. Lisaühiku saab valida ühikute loendist. Samuti saate määrata, kas kaupade kaal tuleb lisaks valitud lisaühikule aruandesse lisada.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kandekoodid</td>
<td>Saate seadistada kande iseloomu oma riigi/regiooni nõuete kohaselt. Iga seadistatava kandekoodi puhul peate seadistama reeglid üleviimistellimuste ja müügi-/ostutellimuste arvesummade ja statistiliste summade arvutamiseks.
<ul>
<li>Üleviimistellimuste puhul saate seadistada arvesummade ja statistiliste summade arvutamiseks ühe järgmistest reeglitest.
<ul>
<li><strong>Tühi</strong> – summa on 0 (null).</li>
<li><strong>Finantsomahind</strong> – summa on võrdne finantsomahinnaga.</li>
<li><strong>Kogumaksumus</strong> – summa on võrdne kande kogumaksumusega.</li>
<li><strong>Käsitsi</strong> – summa on võrdne üleviimistellimuse käsitsi määratud summaga.</li>
</ul></li>
<li>Müügi- ja ostutellimuste puhul saate seadistada arvesummade ja statistiliste summade arvutamiseks ühe järgmistest reeglitest.
<ul>
<li><strong>Tühi</strong> – summa on 0 (null).</li>
<li><strong>Arve summa</strong> – summa on võrdne kauba eest esitatud arvel oleva summaga.</li>
<li><strong>Baassumma</strong> – summa on võrdne enne allahindluse rakendamist arvel oleva summaga.</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>Transpordimeetodid</td>
<td>Saate seadistada transpordiliigi oma riigi/regiooni nõuete kohaselt. Saate määrata iga tarneviisi jaoks vahekaardil <strong>Väliskaubandus</strong> vaike-transpordiliigi.</td>
</tr>
<tr class="even">
<td>Sadamad</td>
<td>Saate seadistada laadimise/mahalaadimise sadama/lennujaama, kui teie riigis/regioonis neid andmeid kogutakse.</td>
</tr>
<tr class="odd">
<td>Statistikaprotseduurid</td>
<td>Saate seadistada statistilise protseduuri, kui seda teavet teie riigis/regioonis kogutakse.</td>
</tr>
</tbody>
</table>

### <a name="set-up-rules-for-compressing-intrastat-transactions"></a>Intrastati kannete tihendamise reeglite seadistamine

Lehel **Intrastati tihendamine** saate valida tihendamiseks kasutatavad väljad. Kõik kanded, millel on Intrastati töölehel valitud väljadel sama väärtuste kombinatsioon, tihendatakse üheks kandeks, kui kasutate Intrastati töölehel tihendamise funktsiooni.

### <a name="set-up-foreign-trade-parameters"></a>Väliskaubanduse parameetrite häälestamine

Kasutage lehte **Väliskaubanduse parameetrid** parameetrite seadistamiseks järgmises tabelis.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Vahekaart</th>
<th>Parameetrid</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Üldine</td>
<td><ul>
<li><strong>Üldine</strong> – määrake järgmised andmed.
<ul>
<li>Müügi- ja ostutellimuste, kreeditarvete ja üleviimistellimuste kandekoodide vaikeväärtus. Kreeditarvetele seadistatud kandekoodi kasutatakse ka füüsiliste kaupade tagastamise koodina ning seda kasutatakse füüsiliste tagastuste ja parandamise kreeditarvete hälbe puhul. Füüsiliste kaupade tagastused esitatakse Intrastati kannetes erineva suunaga. Tagastustellimust kirjendatakse kui lähetust ja lähetust kirjendatakse saabumisena.</li>
<li>Töötaja, kes vastutab Intrastati aruannete koostamise eest.</li>
</ul></li>
<li><strong>Alampiir</strong> – määrake lävest allapoole jäävate kannete muutmise sätted.
<ul>
<li>Läve summa ja kaal</li>
<li>Lävest allapoole jäävate kannete puhul kohaldatav kaubakood</li>
</ul></li>
<li><strong>Ülekanne</strong> – määrake kriteeriumid kannete ülekandmiseks Intrastati töölehele. Saate määrata, et kanded kantakse üle ainult siis, kui kaubad vastavad ühele või kõigile järgmistele kriteeriumidele.
<ul>
<li>Kaubad ei ole teenusüksused.</li>
<li>Kaupadel on kaubakood.</li>
<li>Kaupadel on kaal.</li>
<li>Kaupadel on lisaühikud.</li>
</ul></li>
<li><strong>Seadistuse kontrollimine</strong> – määrake reeglid Intrastati andmete terviklikkuse kontrollimiseks. Saate valida, milliseid andmeid kontrollitakse.</li>
<li><strong>Ümardamisreeglid</strong> – määrake järgmised sätted summade ja kaalude ümardamiseks Intrastati aruandes.
<ul>
<li>Ümardamisreegel (täpsus)</li>
<li>Ümardamismeetod: üles, alla või tavaline</li>
<li>Summade ja kaalude kümnendkohtade arv</li>
<li>Juhised alla 1 kilogrammi (kg) suuruste kaalude ümardamiseks: üles 1 kg-ni, tavaline või ilma ümardamiseta</li>
</ul></li>
<li><strong>Elektrooniline aruandlus</strong> – määrake elektroonilise aruandluse konfiguratsioonide viited, et saaksite luua elektroonilise faili ja aruande.</li>
<li><strong>Kaubakoodide hierarhia</strong> – määrake kategooriahierarhia <strong>Kaubakoodi</strong> tüübile, mis kajastab Intrastati kaubakoodi CN8.</li>
  <li> <strong>Vahetuskursi tüüp</strong> – soovi korral saate määrata aruande intrastati müügi- ja ostukannetes kasutatava vahetuskursi välisvaluutades, Seda kasutatakse juhul, kui kurss erineb kande sisestamisel rakendatud kursist.</li>  
</ul></td>
</tr>
<tr class="even">
<td>Agendi kontaktandmed</td>
<td>Määrake agendi nimi, aadress, maksukohustuslase kood, telefoninumber ja faksinumber.</td>
</tr>
<tr class="odd">
<td>Riigi/regiooni atribuudid</td>
<td>Määrake praeguse juriidilise isiku riigiks/regiooniks <strong>Kodumaine</strong>. Määrake praeguse juriidilise isikuga ELi kaubanduses osalevate ELi riikide/regioonide riigiks/koodiks <strong>EL</strong>. Iga riigi/regiooni puhul saate määrata ka riigi/regiooni koodi väliskaubanduse eesmärgil.</td>
</tr>
<tr class="even">
<td>Numbriseeria</td>
<td>Saate määrata Intrastati töölehe numbriseeria.</td>
</tr>
</tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
