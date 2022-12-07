---
title: Intrastati ülevaade
description: Selles artiklis antakse teavet Euroopa Liidu (EL-i) riikide/regioonide vahelise kauba- ja mõnel juhul teenuste vahetuse Intrastati aruandluse kohta.
author: mrolecki
ms.date: 11/30/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: Intrastat
audience: Application User
ms.reviewer: kfend
ms.custom:
- "28581"
- intro-internal
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 762de8a098c61bc0d717c038d6ca0ff6d649bff3
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815707"
---
# <a name="intrastat-overview"></a>Intrastati ülevaade

[!include [banner](../includes/banner.md)]

Selles artiklis antakse teavet Euroopa Liidu (EL-i) riikide/regioonide vahelise kauba- ja mõnel juhul teenuste vahetuse Intrastati aruandluse kohta. See artikkel annab ka aruandeprotsessi ülevaate ja kirjeldab nõutavaid sätteid ja eeltingimusi.

Intrastat on Euroopa Liidu (EL-i) riikide/regioonide vahelise kaubavahetuse teabe kogumise ja statistika koostamise süsteem. Intrastat-aruandlus on nõutav, kui toote ületab teise ELi riigi/regiooni piiri. Mitmes riigis/regioonis kehtib Intrastat-aruandlus ka teenustele. Intrastat-aruandluses võidakse koguda kohustuslikke ja valikulisi elemente. Järgmised elemendid on kohustuslikud: teabe esitamise eest vastutava osapoole käibemaksukohustuslase number, viiteperiood, voog (saabumine või lähetamine), kaheksakohaline kaubakood, partneri liikmesriik (saatmise liikmesriik saabumise puhul ja lähetuste puhul sihtliikmesriik), kauba väärtus, kaubakogus (netomass ja täiendav ühik) ning kande iseloom. Riigid/regioonid võivad koguda mitmesugustel tingimustel ka valikulisi elemente. Mõned valikulised elemendid on päritoluriik/-regioon, tarnetingimused, transpordiliik, üksikasjalikum kaubakood kui CN8, lähetuste puhul lähtepiirkond ja saabumiste puhul sihtpiirkond, statistiline protseduur, statistiline väärtus, kauba kirjeldus ja laadimise/mahalaadimise sadam/lennujaam.

## <a name="overview-of-the-intrastat-reporting-process"></a>Intrastat-aruandluse protsessi ülevaade
Järgmised jaotised kirjeldavad üldist teabevoogu, mida Intrastat-aruandluses kasutatakse.

### <a name="enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a>Sisestage kanne, mis ületab teise ELi riigi/regiooni piiri

Kliendiarve, vabas vormis arve, ostuarve, projektiarve, kliendi saateleht, hankija toote sissetulek või üleviimistellimus edastatakse Intrastati töölehele ainult juhul, kui sihtkoha (lähetuste puhul) või lähtekoha (saabumiste puhul) riigi/regiooni sihtkoha tüüp on **EU**. Seda funktsiooni laiendati Microsoft Dynamics 365 for Operationsile (1611) ja see võimaldab teil määrata laadimisaadressid ELi-siseste kannete jaoks. Kui laadimisaadress erineb hankija ettevõtte aadressist (või kliendi ettevõtte aadressist tagastustellimuse puhul), kasutab Intrastati aruandlus seda teavet. Kui loote müügitellimuse, vabas vormis arve, ostutellimuse, hankijaarve, projektiarve või üleviimistellimuse, on mõnel väliskaubandusega seotud väljal dokumendi päises või real vaikeväärtused. Kandekoodi vaikeväärtus võetakse lehe **Väliskaubanduse parameetrid** vastavalt väljalt. Kaubakoodi, päritoluriigi/-regiooni ja päritolumaakonna/-provintsi vaikeväärtused võetakse kaubalt. Vaikeväärtusi saab muuta ja lisada saab ka muud väliskaubandusega seotud teavet: statistikaprotseduuri, transporti ja sadamat.

### <a name="use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a>Intrastati töölehe abil saate luua ELi riikide/regioonide vahelise kaubavahetuse teavet.

Statistilistel eesmärkidel luuakse ELi riikide/regioonide vahelise kaubavahetuse teave iga kuu. Kandeid saab edastada vabas vormis arvelt, kliendiarvelt, kliendi saatelehelt, hankija arvelt, hankija saatelehelt, projekti arvelt või üleviimistellimuselt, lehel **Väliskaubanduse parameetrid** seadistatud edastuskriteeriumide alusel. Kandeid saab sisestada ka käsitsi. Saate edastatud kandeid Intrastati töölehel käsitsi muuta, kui muutmine on vajalik. Konkreetsete tingimuste alusel, mis on seadistatud lehel **Intrastati tihendamine**, saate tihendada Intrastati töölehe kandeid. Mõnes riigis/regioonis on teil lubatud kohaldada väikest kande läve. Seejärel saate edastada aruandesse kandeid, mis jäävad määratud kaubakoodi all sellest lävest allapoole. Saate muuta kaubakoodi vastavatel Intrastati töölehe ridadel, tuginedes sättele **Alampiir** lehel **Väliskaubanduse parameetrid**. Saate neid kandeid sätte **Intrastati tihendamine** alusel ka tihendada. Saate kinnitada Intrastati töölehel olevate kannete terviklikkuse sätte **Kontrolli seadistust** põhjal lehel **Väliskaubanduse parameetrid**. Vastavatel väljadel olevate andmete terviklikkust saab kontrollida: riik/regioon, maakond või provints, kaal, kaubakood, kande kood, täiendav ühik, sadam, lähtekoht, tarnetingimus, transpordiliik ja maksuvabastuse number. Kanded, mida ei ole lõpule viidud, märgitakse kehtetuks.

### <a name="use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a>Intrastati töölehe abil saate koostada ELi riikide/regioonide vahelise kaubavahetuse aruande.

Statistilistel eesmärkidel koostatakse ELi riikide/regioonide vahelise kaubavahetuse aruanne iga kuu. Saate Intrastat-aruande välja printida, tuginedes lehe **Aruande vormingu vastendamine** sätetele lehel **Väliskaubanduse parameetrid**. Saate luua ka elektroonilise faili, tuginedes lehe **Failivormingu vastendamine** sätetele lehel **Väliskaubanduse parameetrid**. Lisateavet Intrastati aruandluse, sh nõutavate eeltingimuste kohta vaadake Intrastati aruandluse tegevuse salvestistest.

  - EL-i Intrastati deklaratsiooni loomine.
  - Kannete ülekandmine Intrastati.
  - Laadimisaadressi määramine ühendusesisesele kandele.

## <a name="prerequisites"></a>Eeltingimused
Järgmises tabelis on loetletud Intrastati aruandluse eeltingimused.

|  Eeltingimus  |  Kirjeldus  |
|-------------------------|-------------------------|
| Aadressi häälestamine | Saate seadistada riikide/regioonide ISO (Rahvusvahelise Standardiorganisatsiooni) koodid. |
| Juriidiline isik | Saate seadistada impordi/ekspordi maksuvabastuse numbrid, impordi/ekspordi filiaali koodi laiendi ja juriidilisele isikule määratud Intrastati koodi. |
| Toote kategooriahierarhia (müügihierarhia, hankehierarhia) | Saate määrata Intrastati kaubakoodid kategooriasõlmedele vahekaardil **Kaubakoodid** lehel **Kategooriahierarhia**. Kui määrate kaubakoodi peamisele kategooriasõlmele, kehtib see kood kõigile kategooria alamsõlmedele. Valitud kaubakoodid on saadaval vaates **Valitud** kui valite väljastatud toote üksikasjades ja müügitellimuse, ostutellimuse ja üleviimistellimuse ridadel kaubakoodi. |
| Väljastatud toote üksikasjad | Saate seadistada järgmised väljastatud toodete väliskaubanduse andmed.<ul><li>**Kaubakood** – valige määratud tootekategooriatest toodud valitud kaupade loendist või Intrastati kaubakoodide tervikloendist.</li><li>**Statistiliste tasude protsent**</li><li>**Päritoluriik/-regioon** – saate valida vaikeriigi/-regiooni, kust kaup täielikult hangiti või kus see toodeti.</li><li>**Lähte-/sihtmaakond/-provints** – valige sihtmaakonna/-provintsi vaikeväärtus saabumiste puhul ja lähtemaakond/-provints lähetuste puhul.</li><li>**Netokaal (kg)**</li><li>**Jäta**  välja– luba sellel parameetril selle tootega kandeid Intrastati üle mitte kanda</li></ul> |
| Kliendid | Saate seadistada kliendi tarneaadressi ELi riigis/regioonis. |
| Hankijad | Saate seadistada hankija aadressi ELi riigis/regioonis. |
| Mitmesugused tasud | Saate seadistada lisakulude koodi arve summale, statistilisele summale või mõlemale lisamiseks. Aktiveerige lehel **Tasukoodid** vahekaardil **Väliskaubandus** valik **Intrastati arve väärtus**, et kaasata tasusumma arve väärtusse, ja aktiveerige valik **Intrastati statistiline väärtus** tasusumma kaasamiseks statistilisse väärtusse.</br>Lisateabe saamiseks vaadake üle [kandekoodide ja lisakulude](#transaction-codes-and-miscellaneous-charges) näide. |
| Elektrooniline aruandlus | Saate seadistada elektroonilise aruandluse konfiguratsioonid Intrastati andmete eksportimiseks elektroonilisse faili, mis on vastavate asutuste nõutavas vormingus, ja Intrastati andmete eelvaate kuvamiseks kasutajasõbralikus, loetavas vormingus (nt Microsoft Excelis). |
| Ladustamine | Saate seostada hankijakontosid laokoodidega maksukohustuslase koodi lisamiseks üleviimistellimuse üleviimisel.</br>Lisateabe saamiseks vaadake üle üleviimistellimuse [näide](#transfer-order).|

## <a name="setup"></a>Häälestus
Järgmised jaotised kirjeldavad sätteid, mida on Intrastat-aruandluse jaoks vaja.

### <a name="set-up-all-required-intrastat-related-lists"></a>Kõigi vajalike Intrastatiga seotud loendite seadistamine

|   Loend   |   Lisateave   |
|-------------------------|-------------------------|
| Kaubaartiklite koodid | Saate seadistada kategooriahierarhia tüübiga **Kaubakood** ja sisestada kõik kaubakoodid kombineeritud nomenklatuuriloendi alusel. Iga kauba kohta saate seadistada järgmise teabe.<ul><li>Kauba nimi ja kaubakood</li><li>Hüüdnimi ja/või tõlgitud nimi</li><li>Lisaühikute (täiendavate ühikute) aruandluse sätted vahekaardil **Väliskaubandus**. Lisaühiku saab valida ühikute loendist. Samuti saate määrata, kas kaupade kaal tuleb lisaks valitud lisaühikule aruandesse lisada.</li></ul>Lisateabe saamiseks vaadake üle lisaühikute [näide](#additional-units).|
| Kandekoodid | Saate seadistada kande iseloomu teie riigi/regiooni nõuete kohaselt. Iga seadistatava kandekoodi puhul peate seadistama reeglid üleviimistellimuste ja müügi-/ostutellimuste arvesummade ja statistiliste summade arvutamiseks.<ul><li>Üleviimistellimuste puhul saate seadistada arvesummade ja statistiliste summade arvutamiseks ühe järgmistest reeglitest.<ul><li>**Tühi** – summa on 0 (null).</li><li>**Finantsomahind** – summa on võrdne finantsomahinnaga.</li><li>**Kogumaksumus** – summa on võrdne kande kogumaksumusega.</li><li>**Käsitsi** – summa on võrdne üleviimistellimuse käsitsi määratud summaga.</li></ul></li><li>Müügi- ja ostutellimuste puhul saate seadistada arvesummade ja statistiliste summade arvutamiseks ühe järgmistest reeglitest.<ul><li>**Tühi** – summa on 0 (null).</li><li>**Arve summa** – summa on võrdne kauba eest esitatud arvel oleva summaga.</li><li>**Baassumma** – summa on võrdne enne allahindluse rakendamist arvel oleva summaga.</li></ul></ul>Lisateabe saamiseks vaadake üle [kandekoodide ja lisakulude](#transaction-codes-and-miscellaneous-charges) näide. |
| Transpordimeetodid | Saate seadistada transpordiliigi teie riigi/regiooni nõuete kohaselt. Saate määrata iga tarneviisi jaoks vahekaardil **Väliskaubandus** vaike-transpordiliigi. |
| Sadamad | Saate seadistada laadimise/mahalaadimise sadama/lennujaama, kui teie riigis/regioonis neid andmeid kogutakse. |
| Statistikaprotseduurid | Saate seadistada statistilise protseduuri, kui seda teavet teie riigis/regioonis kogutakse. |



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

## <a name="example"></a>Näide

### <a name="transaction-codes-and-miscellaneous-charges"></a><a name= "transaction-codes-and-miscellaneous-charges"></a> Kandekoodid ja lisakulud

See artikkel katab stsenaariumi, kus Saksamaa ettevõte peab ostma kaupu Itaalia ettevõttest. Ostu sooritamiseks peab Saksa ettevõte seadistama uued kandekoodid ning konfigureerima nende kandekoodide arvesumma ja statistilise summa arvutusreeglid. Lisaks tuleb ettevõtte arve loomisel määrata lisakulud ja nende protsendid. Neid väärtusi arvestatakse statistilise väärtuse arvutamisel.

See stsenaarium kasutab **DEMF-i juriidilist** isikut.

#### <a name="preliminary-setup"></a>Esialgne seadistamine

1. Minge organisatsiooni **haldusorganisatsiooni juriidiliste** > **isikutesse** > **ja** valige **DEMF**.
2. Aadresside **kiirkaardil** veenduge, et riigi **/regiooni välja väärtuseks** on **seatud DEU(Saksamaa).**
3. Minge **ostureskontro** > **hankijatele** > **kõigile hankijatele**.
4. Valige ruudustikus DE-001 **·**.
5. Valige kiirkaardil **Aadress** käsk **Redigeeri**.
6. Dialoogiakna **Aadressi redigeerimine** väljal **Riik/regioon** valige **ITA**.
7. Valige dialoogiboksi sulgemiseks suvand **OK**.

#### <a name="set-up-transaction-codes"></a>Saate häälestada kandekoode.

1. Avage **Maks** > **Seadistus** > **Väliskaubandus** > **Kandekoodid**.
2. Valige ruudustikus **11**. Seejärel valige tegevuspaanil **kustutamisloend**.
3. Valige toimingupaanil nupp **Uus**.
4. Kiirkaardil Kandekoodid väljale **Kande** kood **sisestage** **11** . **·**
5. Väljale Nimi **sisestage** otseost **/-müük**.
6.  **Valige jaotise Müük ja** ostud väljal **Arve summa** väärtus Arve **summa**.
7. Valige väljal **Statistiline** summa väärtus **Arve summa**.
8. Valige toimingupaanil nupp **Salvesta**.

#### <a name="set-up-miscellaneous-charges"></a>Lisakulude seadistus

1. Minge ostureskontro kulude seadistuse **kulude koodi** > **.** > **·**
2. Ruudustikus valige **Veos**.
3. Valige Toimingupaanil nupp **Redigeeri**.
4. Seadke väliskaubanduse kiirkaardil Intrastati arve väärtuse **ja**  **Intrastati statistiliste väärtuste valikud** olekusse **Jah** . **·**

#### <a name="set-up-foreign-trade-parameters"></a>Väliskaubanduse parameetrite häälestamine

1. Avage **Maks** > **Seadistus** > **Väliskaubandus** > **Väliskaubanduse parameetrid**.
2. Valige vahekaardil **Intrastat** kiirkaardil **Üldine** väljal **Kande** **kood** väärtus **11**.
3. Veenduge, **et kaubakoodi** hierarhia kiirkaardil on kategooriahierarhia **väljal** seatud **Intrastat.**

#### <a name="create-a-purchase-order"></a>Ostutellimuse loomine

1. Avage **Ostureskontro** > **Ostutellimused** > **Kõik ostutellimused**.
2. Valige toimingupaanil nupp **Uus**.
3. Valige dialoogiboksi **Müügitellimuse loomine** väljal **Hankija konto** suvand **DE-001**.
4. Valige nupp **OK**.
5. Veenduge, **Päis** **Välis** **Kaubanduse** kiirkaardil **Kande kood** väljal oleks seatud väärtusele **11**.
6. Valige **Read** vahekaardil **Müügi tellimuse ridade** väljal **Kaubakoodi** väärtuseks **D0003**. Sisestage väljale **Kogus** väärtus **10**.
7. Väliskaubanduse **jaotise** rea üksikasjade **kiirkaardi** vahekaardil Väliskaubandus veenduge, **·**  **et** kande koodi väli on automaatselt seatud.
8.  **Valige ostutellimuse ridade** kiirkaardi menüü **Finantsid jaotises** Tasud **suvand** Säilita **tasud**.
9. Valige väljal **Tasukood** suvand **VEOS**.
10. Väljale Kulude **väärtus** sisestage **30**.
11. Valige toimingupaanil nupp **Salvesta**. Seejärel sulgege leht.
12. Valige toimingupaanil vahekaardi **Ostmine** grupis **Tegevused** suvand **Kinnita**.
13. Valige toimingupaani vahekaardil **Arve** grupis **Loo** suvand **Arve**.
14. Valige tegumiribal suvand **Vaike vorm**. Valige **Tellitud kogus** väljal **Ridade vaikekogus**. Seejärel valige **OK**.
15. Sisestage **hankija arve päise** kiirkaardi jaotise **Arve ID** jaotisse **Number** väljale väärtus **00100**.
16.  **Valige jaotise Arve** kuupäevad **väljal**  **Arve kuupäev 11/24/2021**  (24. november 2021).
17. Valige arve postitamiseks toimingupaanilt **Postita**.

### <a name="transfer-the-vendor-invoice-to-the-intrastat-journal"></a>Hankija arve ülekandmine Intrastati töölehele

1. Avage **Maks** > **Deklaratsioonid** > **Väliskaubandus** > **Intrastat**.
2. Valige tegevuste paanil käsk **Insener**.
3. Dialoogiboksis **Intrastat (ülekanne)** seadke **hankija arve** valikuks **Jah**.
4. Tehingute ülekandmiseks valige **OK** ja vaadake Intrastati päevikut.

   ![Rida, mis tähistab ostutellimust koos lisakuludega Intrastati lehel](media/intrastat_overview_1.png)

5. Vaadake üle **Üldine** ostutellimuse vahekaart. Pange tähele **,**  **·**  **et arve väärtuse**  **·**  **väljal** kuvatakse arve summa ja arve kulude summa väljade summa ning väljal Statistiline väärtus kuvatakse statistika summa ja statistika **kulude summa väljade** summa.

   ![Ostutellimuse üksikasjad koos lisakuludega Intrastati lehe vahekaardil Üldine](media/intrastat_overview_2.png)

### <a name="transfer-order"></a>Üleviimistellimus

Selles näites peab Saksamaa ettevõte teisaldama kaks kaubaühikut Saksamaa laost Itaalia lattu. Välja Statistiline väärtus raamatupidamise jaoks tuleb selle toote jaoks määrata ka tasud **määraga** 20 protsenti. Selles näites kasutatakse **DEMF-i juriidilist** isikut.

#### <a name="preliminary-setup"></a>Esialgne seadistamine

1. Minge organisatsiooni **haldusorganisatsiooni juriidiliste** > **isikutesse** > **ja** valige **DEMF**.
2. Aadresside **kiirkaardil** veenduge, et riigi **/regiooni välja väärtuseks** on **seatud DEU(Saksamaa).**
3. Avage **Maks** > **Seadistus** > **Väliskaubandus** > **Väliskaubanduse parameetrid**.
4. Veenduge, **et kaubakoodi** hierarhia kiirkaardil on kategooriahierarhia **väljal** seatud **Intrastat.**
5. Minge **ostureskontro** > **hankijatele** > **kõigile hankijatele**.
6. Valige ruudustikus DE-001 **·**.
7. Valige kiirkaardil **Aadress** käsk **Redigeeri**.
8. Dialoogiakna **Aadressi redigeerimine** väljal **Riik/regioon** valige **ITA**.
9. Valige dialoogiboksi sulgemiseks suvand **OK**.

#### <a name="set-up-transaction-codes"></a>Saate häälestada kandekoode.

1. Avage **Maks** > **Seadistus** > **Väliskaubandus** > **Kandekoodid**.
2. Valige ruudustikus **11**. Seejärel valige tegevuspaanil **kustutamisloend**.
3. Valige toimingupaanil nupp **Uus**.
4. Kiirkaardil Kandekoodid väljale **Kande** kood **sisestage** **11** . **·**
5. Väljale Nimi **sisestage** otseost **/-müük**.
6. Valige jaotise Üleviimistellimus väljal Arve summa **suvand Kogukulu**  **.**  **·**
7. Väljal Statistiline **summa** valige suvand **Kogukulu**.
8. Valige toimingupaanil nupp **Salvesta**.
9. Avage **Maks** > **Seadistus** > **Väliskaubandus** > **Väliskaubanduse parameetrid**.
10.  **Valige Intrastati** vahekaardi Kiirkaart **Üldine** väljal **Üleviimistellimus väärtus**  **11**.

#### <a name="set-up-charges-for-an-item"></a>Kauba kulude seadistamine

1. Avage **Tooteteabe haldus** > **Tooted** > **Väljastatud tooted**.
2. Valige ruudustikus **D0001**.
3. Sisestage **Intrastati** jaotise Väliskaubanduse **kiirkaardi** väljale Kulude **protsent**  **väärtus 20**.

#### <a name="change-the-site-address"></a>Muutke saidi aadressi

1. Avage jaotis **Warehouse management** > **Seadistus** > **Ladu** > **Saidid**.
2. Valige ruudustikus **1**.
3. Kiirkaardil **Aadressid** valige **Redigeeri**.
4. Dialoogiakna **Aadressi redigeerimine** väljal **Riik/regioon** valige **DEU**.
5. Valige nupp **OK**.
6. Valige ruudustikus **2**.
7. Kiirkaardil **Aadressid** valige **Redigeeri**.
8. Dialoogiakna **Aadressi redigeerimine** väljal **Riik/regioon** valige **ITA**.
9. Valige nupp **OK**.
10. Avage **Laohaldus** > **Seadistus** > **Ladu** > **Laod**.
11. Valige ruudustikus **21**.
12.  **Valige kiirkaardi** Üldine jaotise **Viide** väljal **Hankija konto väärtus**  **DE-001**.

#### <a name="create-a-transfer-order"></a>Üleviimistellimuse loomine

1. Minge varude **halduse väljaminevate** > **tellimuste üleviimistellimusele** > **·**.
2. Valige toimingupaanil nupp **Uus**.
3.  **Valige vahekaardi** Read kiirkaardi **Üleviimistellimuse** päis **jaotise**  **Ülevaade väljal Laost**  **väärtus 11.** Valige väljal **Lattu** väärtus **21**.
4. Valige kiirkaardi **Üleviimistellimuse** **read vahekaardil** Read suvand **Lisa**.
5. Valige väljal **Kaubakood** väärtus **D0001**. Seejärel sisestage **väljale Üleviimiskogus**  **2**.
6. Väliskaubanduse **jaotise** rea üksikasjade **kiirkaardi** vahekaardil Väliskaubandus veenduge, **·**  **et** kande koodi väli on automaatselt seatud.
7. Märkige tegevuspaani vahekaardil **Läheta** jaotises Operatsioonid **ruut** Lähetuse **üleviimistellimus**.
8. Valige dialoogiboksi Saadetis vahekaardi **Ülevaade** väljal Uuendamine **suvand** **Kõik** . **·**
9. Valige **OK** tellimuse lähetamiseks.
10. Valige tegevuspaani vahekaardil **Võta** vastu grupis **Operatsioonid** suvand **Võta vastu**.
11.  **Valige dialoogiboksi** Vastuvõtu vahekaart **Ülevaade** väljal Uuendamine **suvand** **Kõik**.
12. Valige **OK** tellimuse lähetamiseks.

#### <a name="transfer-the-transfer-order-to-the-intrastat-journal"></a>Üleviimistellimuse ülekandmine Intrastati töölehele

1. Avage **Maks** > **Deklaratsioonid** > **Väliskaubandus** > **Intrastat**.
2. Valige tegevuste paanil käsk **Insener**.
3. Määrake dialoogiboksis **Intrastat (ülekanne**) **valiku Üleviimistellimus väärtuseks**  **Jah** ja kõigi muude valikute väärtuseks **Ei**.
4. Tehingute ülekandmiseks valige **OK** ja vaadake Intrastati päevikut.

   ![Rida, mis tähistab üleviimistellimust Intrastati lehel](media/intrastat_overview_3.png)

5.  Vaadake üle **üleviimistellimuse** vahekaart Üldine.

    Pange tähele, et arve väärtuse **ja statistilise** väärtuse **jaotiste** väljad seatakse automaatselt. Väljade Arve summa ja **Statistiline** summa **väärtused põhinevad kandekoodide** lehel olevatel sätetel **.**  Välja Kulude **protsent väärtus**  **20** on lehel Väljastatud toode seatud **väärtus**. Välja Statistilised kulud **väärtus** on kulude kvantitatiivne avaldis (sest välja 107,24 väärtus on 20 protsenti 536,18). Välja Statistiline väärtus **väärtus on väljade Statistiline summa** ja Statistika kulude **summa** väärtuste **summa** .

  ![Üleviimistellimuse üksikasjad intrastati lehe vahekaardil Üldine](media/intrastat_overview_4.png)

### <a name="additional-units"></a>Lisaühikud

Selles näites peab Saksamaa ettevõte ostma 10 kaubaühikut Itaalia ettevõttest. Lisaks artiklikoodidele tuleb nendele kaupadele määrata lisaühikud. Näide näitab, kuidas luua uusi mõõtühikuid, määrata Intrastati kaubakoodile lisaühikuid, sisestada lisaühikutega kandeid ja vaadata üle Intrastat-tööleht, kus on seadistatud lisaühikute väli.

#### <a name="preliminary-setup"></a>Esialgne seadistamine

1. Minge organisatsiooni **haldusorganisatsiooni juriidiliste** > **isikutesse** > **ja** valige **DEMF**.
2. Aadresside **kiirkaardil** veenduge, et riigi **/regiooni välja väärtuseks** on **seatud DEU(Saksamaa).**
3. Avage **Maks** > **Seadistus** > **Väliskaubandus** > **Väliskaubanduse parameetrid**.
4. Valige vahekaardil **Intrastat** kiirkaardil **Üldine** väljal **Kande** **kood** väärtus **11**.
5. Veenduge, **et kaubakoodi** hierarhia kiirkaardil on kategooriahierarhia **väljal** seatud **Intrastat.**
6. Minge **ostureskontro** > **hankijatele** > **kõigile hankijatele**.
7. Valige ruudustikus DE-001 **·**.
8. Valige kiirkaardil **Aadress** käsk **Redigeeri**.
9. Dialoogiakna **Aadressi redigeerimine** väljal **Riik/regioon** valige **ITA**.
10. Valige dialoogiboksi sulgemiseks suvand **OK**.

#### <a name="create-a-unit-of-measure"></a>Mõõtühiku loomine

1. Minge organisatsiooni **halduse seadistusühikutesse** > **·** > **·** > **·**.
2. Valige toimingupaanil nupp **Uus**.
3.  **Sisestage** väljale Ühik mõõtühiku nimi. Selle näite puhul sisestage **GRM**.
4. Valige jaotise **Klassifikatsioon väljal**  **Ühiku klass atribuut,**  **mida ühik näitab.**  Selle näite puhul valige **Mass**.
5.  **Väljal Ühikutesüsteem** valige mõõtmissüsteem, kuhu ühik kuulub. Näiteks valige meetermõõdu **ühikud**.

#### <a name="set-up-unit-conversions"></a>Ühikuteisenduste häälestamine

1. Minge organisatsiooni **halduse häälestusühikute** > **·** > **·** > **ühikuteisenduste loendisse.**
2. Valige vahekaardil **Klassidevahelised teisendused** suvand **Uus**.
3. Valige dialoogiakna **Ühiku** teisendus väljal **Toode väärtus**  **F00007**.
4. Valige väljal **Ühikust** väärtus **ea**.
5.  **Väljal Ühikuni** valige **GRM**.
6. Kontrollige, kas teisendusmäär **on 1 = 1**.
7. Valige nupp **OK**.
8. Avage **Tooteteabe haldus** > **Tooted** > **Väljastatud tooted**.
9. Valige ruudustikus **F00007**.
10. Valige kiirkaardi **Varud jaotise**  **Ühik** väljal **Ühik suvand** GRM **.**
11. Valige toimingupaanil nupp **Salvesta**.

#### <a name="set-up-product-information"></a>Seadistage tooteteave

1. Avage **Tooteteabe haldus** > **Tooted** > **Väljastatud tooted**.
2. Valige ruudustikus **F00007**.
3. Valige kiirkaardi **Väliskaubandus** jaotise **Intrastat** väljal **Kaup** valige **920 20 34**.
4. Valige toimingupaanil nupp **Salvesta**.

#### <a name="assign-the-additional-unit-to-an-intrastate-commodity-code"></a>Lisaühiku määramine Intrastati kaubaartikli koodile

1. Minge jaotisse **Tooteteabe haldus** > **Seadistus** > **Kategooriad ja atribuudid** > **Kategooria hierarhiad**.
2. Valige loendist **Intrastat**.
3. Ruudustikus **valigekõlar**.
4. Valige väliskaubanduse kiirkaardi väljal **Lisaühikud**  **suvand GRM** . **·**
5. Valige toimingupaanil nupp **Salvesta**.

   Lisateavet vt mõõtühikute [haldamine](../../supply-chain/pim/tasks/manage-unit-measure.md).

#### <a name="create-a-purchase-order"></a>Ostutellimuse loomine

1. Avage **Ostureskontro** > **Ostutellimused** > **Kõik ostutellimused**.
2. Valige toimingupaanil nupp **Uus**.
3. Valige dialoogiboksi **Müügitellimuse loomine** väljal **Hankija konto** suvand **DE-001**.
4. Valige nupp **OK**.
5. Veenduge, **Päis** **Välis** **Kaubanduse** kiirkaardil **Kande kood** väljal oleks seatud väärtusele **11**.
6. Valige **Read** vahekaardil **Müügi tellimuse ridade** väljal **Kaubakoodi** väärtuseks **F00007**. Sisestage väljale **Kogus** väärtus **10**.
7. Väliskaubanduse **jaotise** rea **üksikasjade** kiirkaardi vahekaardil Väliskaubandus veenduge, **·**  **·**  **et kande kood ja kauba väljad** seatakse automaatselt.
8. Valige toimingupaanil vahekaardi **Ostmine** grupis **Tegevused** suvand **Kinnita**.
9. Valige toimingupaani vahekaardil **Arve** grupis **Loo** suvand **Arve**.
10. Valige tegumiribal suvand **Vaike vorm**. Valige **Tellitud kogus** väljal **Ridade vaikekogus**. Seejärel valige **OK**.
11. Sisestage **hankija arve** päise kiirkaardi jaotise **Arve** ID väljale **Number**  **väärtus VE-0010**.
12.  **Valige arve kuupäevade**  **·**  **väljal Arve kuupäev 10/5/2021**  (5. oktoober 2021).
13. Valige arve postitamiseks toimingupaanilt **Postita**.

#### <a name="transfer-the-vendor-invoice-to-the-intrastat-journal"></a>Hankija arve ülekandmine Intrastati töölehele

1. Avage **Maks** > **Deklaratsioonid** > **Väliskaubandus** > **Intrastat**.
2. Valige tegevuste paanil käsk **Insener**.
3. Dialoogiboksis **Intrastat (ülekanne)** seadke **hankija arve** valikuks **Jah**.
4. Tehingute ülekandmiseks valige **OK** ja vaadake Intrastati päevikut.

   ![Rida, mis tähistab ostutellimust Intrastati lehel](media/intrastat_overview_5.png)

5. Vaadake üle **Üldine** ostutellimuse vahekaart. Pange tähele, **et jaotises Ühik** seadistatakse **automaatselt** lisaühikute kogus **ja** lisaühiku väljad.

   ![Ostutellimuse üksikasjad intrastati lehe vahekaardil Üldine](media/intrastat_overview_6.png)
   
## <a name="list-of-countryregion-specific-articles"></a>Riigi-/regiooni kindlate artiklite loend
Järgmises tabelis loetletakse saadaolevad riigi-/regiooniomased Intrastati artiklid.

| Riik          | Link      |
|------------------|-----------|
| Austria          |[Austria Intrastat](emea-aut-intrastat.md)| 
| Belgia          |[Belgia Intrastat](emea-bel-intrastat.md)|
| Tšehhi Vabariik   |[Tšehhi Intrastat](emea-cze-intrastat.md)|
| Taani          |[Taani Intrastat](emea-dnk-intrastat.md)|
| Eesti          |[Eesti Intrastat](emea-est-intrastat.md)|
| Soome          |[Soome Intrastat](emea-fin-intrastat.md)|
| Prantsusmaa           |[Prantsuse Intrastat](emea-fra-intrastat.md)|
| Saksamaa          |[Saksa Intrastat](emea-deu-intrastat.md)|
| Ungari          |[Ungari Intrastat](emea-hun-intrastat.md)|
| Itaalia            |[Itaalia Intrastat](emea-ita-intrastat.md)|
| Läti           |[Läti Intrastat](emea-lva-intrastat.md)|
| Leedu        |[Leedu Intrastat](emea-ltu-intrastat.md)|
| Holland      |[Hollandi Intrastat](emea-nl-intrastat.md)|
| Poola           |[Poola Intrastat](emea-pol-intrastat.md)|
| Hispaania            |[Hispaania Intrastat](emea-esp-intrastat.md)|
| Rootsi           |[Rootsi Intrastat](emea-swe-intrastat.md)|


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
