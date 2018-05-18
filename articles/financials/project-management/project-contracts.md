---
title: Projektilepingud
description: "See teema kirjeldab projektilepinguid ja toob näiteid lepingutest, mida saate erinevatele projektitüüpidele ja rahastamise allikatele luua, ning näitab, kuidas hallata rakenduses Microsoft Dynamics 365 for Finance and Operations lepinguid ja arveprojekti kliente."
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: e46393b9ac8797bf12cca12099d177980b75ba38
ms.contentlocale: et-ee
ms.lasthandoff: 03/26/2018

---

# <a name="project-contracts"></a>Projektilepingud

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab projektilepinguid ja toob näiteid lepingutest, mida saate erinevatele projektitüüpidele ja rahastamise allikatele luua, ning näitab, kuidas hallata rakenduses Microsoft Dynamics 365 for Finance and Operations lepinguid ja arveprojekti kliente.

Projektilepingu jaoks loodav projekti tüüp määratleb meetodi, mida kasutatakse projekti klientidele arvete esitamiseks. Projekti lepingut ja seotud projekti saab muuta, kuid projekti tüüpi ei saa muuta. 

Projektilepingu abil saate koostada samal ajal vähemalt ühe projekti arved. Projektileping aitab tagada ka ühtse arveldusprotseduuri kasutamise projektistruktuuri iga alamprojekti puhul. 

Iga projekt, mille kohta arve koostatakse, peab olema seotud projektilepinguga. Projektilepingu sätted kehtivad kõigile projektidele ja alamprojektidele, mis on selle projektilepinguga seotud. 

Projektilepingus saab määrata ühe või mitu rahastamisallikat. Seetõttu saate jagada arveldamise mitme rahastaja vahel, seadistada rahastamise limiidid, nii et rahastamisallikatele esitatakse arved ainult teatud summa ulatuses, ja konfigureerida kulutuste rahastamisreeglid.

## <a name="funding-for-project-contracts"></a>Projektilepingute rahastamine
Mõned projektilepingud määravad, et projektikulude rahastamise eest vastutavad ühiselt mitu osapoolt. Järgmisena on toodud mõned näited.

-   Suur mitme divisjoniga klient soovib jagada projekti rahastamise divisjonide kaupa.
-   Teie ettevõtte jagab suure projekti kulusid välise organisatsiooniga.
-   Teeprojekti rahastab ühiselt kaks valda.
-   Sillaprojekti rahastatakse riigi toetusest ja erakorporatsiooni vahenditest.

Finance and Operationsis saate jagada ühe kande või kogu projekti arveldused mitme kliendi, toetuse või organisatsiooni vahel. 

Projektides, millel on mitu rahastajat, nimetatakse kõiki osapooli, kes panustavad keerukasse rahastusprojekti, rahastamise allikateks. Pärast kliendi, organisatsiooni või toetuse määratlemist rahastamise allikana, saab selle määrata vähemalt ühele rahastamise reeglile. Rahastamise reeglid sisaldavad kriteeriume, mis määravad, kuidas kulud projekti erinevate rahastamise allikate vahel jagatakse. 

Kuna ladustatavaid kaupu (näiteks neid, mis on nimetatud ostutaotlustel ja ostutellimustel) ei saa jagada, ei saa kulusummat jaotamise ajal mitme rahastamise allika vahel jagada. Seega jääb rahastamise allika väärtuseks 0 (null), kuni sisestatakse lao väljaminek. Lao väljamineku sisestamisel jagatakse kulu summa projekti jaotusreeglite järgi.

Siin on mõned juhised, kuidas hõlbustada arvete jagamist mitme rahastamisallika vahel.

-   Määrake, et kõik projekti kohta sisestatud kanded kasutavad sama müügivaluutat, mida projektileping.
-   Seadistage rahastamise limiidid, nii et rahastamise allikale ei esitata suuremat arvet kui projektile määratud summa.
-   Saate konfigureerida rahastamise reegleid ja rahastamise limiite iga töötaja, kauba, kategooria, kategooriagrupi ja kande tüübi kohta (või kõigi kande tüüpide kohta).
-   Valige soovi korral algus- ja lõppkuupäevad, et määratleda iga rahastamise reegli kehtivusperiood.
-   Määrake protsent, mille eest iga rahastamise allikas vastutab.
-   Määrake milline rahastamise allikas vastutab rahastamise eraldamise arvutustest tekkinud ümarduserinevuste eest.
-   Saate seadistada reeglid, mis määravad, kuidas projektikulude eest välistele klientidele ja siseorganisatsioonidele arveid esitatakse.
-   Salvestage kanded ooteloleval rahastamise kontol, kuni saate täiendavat rahastamist või kuni otsustate kulud kanda ettevõttesiseselt.

Määramiseks, millist maksugruppi kandega seostada, otsitakse projektist maksugrupi määrangut. Kui ühtegi maksugrupi määrangut projekti tasandil pole, otsitakse projektilepingust.

### <a name="example-multiple-funding-sources-simple"></a>Näide: mitu rahastamise allikat (lihtne)

Järgmises tabelis pakutakse stsenaariume rahastamise mitmele rahastamise allikale eraldamise haldamiseks. Need stsenaariumid põhinevad järgmistel eeldustel.

-   Prioriteedisätteid arvestatakse vahendite eraldamises enne teiste rahastamise reegli kriteeriumide rakendamist.
-   Rahastamise reegli kehtivusperioodi määratlemiseks pole kuupäevavahemikku määratud.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Stsenaarium</strong></td>
<td><strong>Rahastamise allikas </strong></td>
<td><strong>Eraldise % </strong></td>
<td><strong>Eraldise prioriteet </strong></td>
</tr>
<tr class="even">
<td>Soovite määrata kulusid ühele rahastamise allikale, kuni selle vahendid on otsas, eraldada kulusid teisele rahastamise allikale, kuni selle vahendid on otsas ja eraldada lõpuks ülejäänud kulud kolmandale rahastamise allikale.</td>
<td><ul>
<li>Rahastamise　allikas　1</li>
<li>Rahastamise　allikas　2</li>
<li>Rahastamise　allikas　3</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>1</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Soovite eraldada 75 protsenti kuludest ühele rahastamise allikale ja 25 protsenti teisele rahastamise allikale. Kui kumbki neist rahastamise allikatest ammendub, soovite maksta ülejäänud kulud kolmandast rahastamise allikast.</td>
<td><ul>
<li>Rahastamise　allikas　1</li>
<li>Rahastamise　allikas　2</li>
<li>Rahastamise　allikas　3</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>1</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Soovite eraldada 75 protsenti kuludest ühele rahastamise allikale ja 25 protsenti teisele rahastamise allikale. Kui kumbki neist rahastamise allikatest ammendub, soovite jagada ülejäänud kulud kolmanda ja neljanda rahastamise allika vahel.</td>
<td><ul>
<li>Rahastamise　allikas　1</li>
<li>Rahastamise　allikas　2</li>
<li>Rahastamise　allikas　3</li>
<li>Rahastamise　allikas　4</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>0,5</li>
<li>0,5</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Soovite eraldada esimesed 25 protsenti kuludest ühele rahastamise allikale ja ülejäänu teisele rahastamise allikale.</td>
<td><ul>
<li>Rahastamise　allikas　1</li>
<li>Rahastamise　allikas　2</li>
</ul></td>
<td><ul>
<li>25%</li>
<li>1</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Näide: mitu rahastamise allikat (keerukas)

Teil on kolm rahastamise allikat, mida soovite kasutada järgmises järjekorras.

1.  Kasutate rahastamise allikat 2 ja rahastamisallikat 3 võrdselt, kuni rahastamise allikas 2 on ammendatud.
2.  Jätkate rahastamise allika 3 kasutamist, kuni see on ammendatud.
3.  Kasutate rahastamise allikat 1 pärast rahastamise allika 3 ammendamist.

Selle eesmärgi saavutamiseks tuleb teha järgmist.

-   Seadistage rahastamise limiidid rahastamise allikale 2 ja rahastamise allikale 3 nende vastavate summade ulatuses.
-   Looge järgmised rahastamise reeglid.
    -   Reegel 1 (prioriteet 1): eraldate 50 protsenti kannetest rahastamise allikale 2 ja 50 protsenti rahastamise allikale 3.
    -   Reegel 2 (prioriteet 2): eraldate 100 protsenti kannetest rahastamise allikale 3.
    -   Reegel 3 (prioriteet 3): eraldate 100 protsenti kannetest rahastamise allikale 1.

See seadistus toimib, sest kandeid on reeglite ja piirangute suhtes kontrollitud, et määrata, kas neid rakendatakse kande puhul. Kui kandele ei rakendata konkreetseid reegleid või piiranguid, kehtib kõigi kannete reegel. Kõigi kannete reegel sobib kõigi kannetega. 

Kui leitakse reegel, mis kandele sobib, rakendatakse esmalt selles reeglis eraldatud protsenti, kuid alles pärast seda, kui vastavusi on kontrollitud kõigi seadistatud limiitide suhtes. Kui limiit on täis ja rahastamise allika vahendid on otsas, ignoreeritakse rahastamise limiidiga seotud rahastamise reeglit ja programm kontrollib järgmist reeglit, mida rakendatakse. 

Mõnel juhul saab reegli alusel eraldada ainult osa kandest. See võib juhtuda limiidi täitumise tõttu kande eraldamisel. Sellisel juhul eraldatakse selle reegli alusel igale rahastamise allikale ainult teatud summa, näiteks 50 protsenti. Selline on olukord reeglis 1, mida selles osas eelnevalt kirjeldati. Jäägid eraldatakse jada järgmise reegli järgi. 

Järgmises tabelis käsitletakse seda stsenaariumi täpsemalt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Fookus </strong></td>
<td><strong>Üksikasjad</strong></td>
</tr>
<tr class="even">
<td>Rahastamisreeglid</td>
<td><ul>
<li>Reegel 1 (prioriteet 1) – kõik kanded. Eraldage rahastamise allikale 2 50% ja rahastamise allikale 3 50%.</li>
<li>Reegel 2 (prioriteet 2) – kõik kanded. Eraldage rahastamise allikale 3 100%.</li>
<li>Reegel 3 (prioriteet 2) – kõik kanded. Eraldage rahastamise allikale 1 100%.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Rahastamise limiidid</td>
<td><ul>
<li>Rahastamise allika 1 limiit = 10 000.00</li>
<li>Rahastamise allika 2 limiit = 500.00</li>
<li>Rahastamise allika 3 limiit = 750.00</li>
</ul></td>
</tr>
<tr class="even">
<td>Kanne 1</td>
<td><strong>Kande summa:</strong> 100.00<strong>Rahastamine:</strong> Kande eest tasutakse ainult reegli 1 alusel, kuna kanne on pärast reegli 1 rakendamist täielikult makstud. Kanne rahastatakse võrdselt rahastamise allikast 2 ja rahastamise allikast 3.
<ul>
<li>Rahastamise allikas 2: 50.00</li>
<li>Rahastamise allikas 3: 50.00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Kanne 2</td>
<td><strong>Kande summa:</strong> 5000.00<strong>Rahastamine:</strong> Kande eest makstakse kõigi kolme reegli alusel. <strong>Reegel 1</strong>
<ul>
<li>Rahastamise allikas 2: 450.00</li>
<li>Rahastamise allikas 3: 450.00</li>
</ul>
<strong>Reegel 2</strong>
<ul>
<li>Rahastamise allikas 3: 250.00 (= 750.00 – 50.00 – 450.00)</li>
</ul>
<strong>Reegel 3</strong>
<ul>
<li>Rahastamise allikas 1: 3850.00 (= 5000.00 – 450.00 – 450.00 – 250.00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Igale rahastamisallikale jaotatav vahendite koondsumma</td>
<td><ul>
<li>Rahastamise allikas 1: 3850.00</li>
<li>Rahastamise allikas 2: 500.00</li>
<li>Rahastamise allikas 3: 750.00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Arveldusreeglid
Kliendiga projektilepingu läbirääkimisi pidades saate määratleda, kuidas ja millal kliendile projekti raames tehtava töö eest arve esitate. Pärast projektilepingu ja projekti seadistamist saate seadistada projekti arveldusreeglid. Arveldusreeglid põhinevad projektilepingus määratud projekti tingimustel. Arveldusreeglid, mida saate luua, sõltuvad projektilepingu tingimustest ja projekti tüübist (nt aeg ja materjal või fikseeritud hind), mille arveldusreegliga seostate. Saate luua projekti lepingu jaoks rohkem kui ühe arveldusreegli. Saate määrata arveldusreegli mitmele sama projektilepinguga seotud sarnaste maksetingimustega projektile. 

Saate seadistada järgmist tüüpi arveldusreegleid.

-   **Tarneühik** – kliendile esitatakse arve, kui tarneühik on lõpetatud. Tarneühikud määratletakse lepingus.
-   **Edenemine** – kliendile esitatakse arve määratud projekti osa lõpetamisel. Saate seadistada arveldusreegli lõpetatud töö protsendi automaatseks arvutamiseks või saate arvutada lõpetatud töö protsendi ja kliendi arvele lisatava summa käsitsi.
-   **Vahe-eesmärk** – kliendile esitatakse arve projekti vahe-eesmärgi kogu summa ulatuses, kui projekti vahe-eesmärk on saavutatud.
-   **Tasu**– kliendi arvele lisatakse tasu teenuste eest ja juhtimistasu, mis on tavaliselt protsent teenuste hinnast.
-   **Aeg ja materjal**– kliendile esitatakse arve projektis kasutatava aja- ja materjalikulu ulatuses.

Kõigi arveldusreeglite tüüpide puhul saate määrata kinnipeetava protsendimäära, mis arvestatakse kliendi arvetelt maha, kuni protsent jõuab kokkulepitud etappi. Maksest kinnipeetav protsendimäär on määratud projektilepingus. Summa arvutatakse ja lahutatakse kliendiarve ridade koguväärtusest. 

Arveldusreeglite **Aeg ja materjal** ning **Edenemine** puhul saate määrata arveldatavad kategooriad. Arveldatavad kategooriad näitavad kandeid, mis tuleb kliendiarvetele lisada. 

Kui olete valmis kliendile arvet esitama, arvestatakse arveldusreeglite alusel projekti arve summa ja koostatakse projekti arvesoovitus. 

Järgmistes jaotistes on näited projekti arveldusreeglite seadistamise ja haldamise kohta.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Näide: tarnitud ühikutel põhineva arveldusreegli loomine

Teie organisatsioon sõlmib lepingu kokku viie koolituskursuse korraldamises kliendi töötajatele hinnaga 10 000 ühe koolituskursuse kohta. Esitate pärast iga koolituskursust kliendile arve. 

Lepingu arveldusreeglite seadistamisel kasutate järgmisi väärtusi.

-   Tarneühik on üks koolituskursus.
-   Ühiku hind on 10 000 koolituskursuse kohta.
-   Ühikute arv on viis koolituskursust.

Kui olete ühe koolituskursuse lõpetanud, koostate esimese ühiku kohta arve summas 10 000 ja saadate arve kliendile.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Näide: projekti teatud (käsitsi arvutatud) osa valmimisel põhineva arveldusreegli loomine

Teie organisatsioon, tarkvarakonsultatsioone pakkuv firma, sõlmib kliendiga lepingu kliendi arendatava toote osa arendamiseks. Teie organisatsioon nõustub edastama programmi kuue kuu jooksul. Klient nõustub maksma teie organisatsioonile töö eest kokku 100 000. Loote arveldusreegli kliendile arve esitamiseks projekti raames tehtud töö protsendi eest, vastavalt lepingu sätetele.

-   Esimese kuu lõpus saate kliendiga kokku, et määrata tehtud töö protsent. Projekti ülevaatamisel leiate ühiselt, et projektist on valmis 15%.
-   Koostate arve summale 15 000 (15 protsenti summast 100 000) ja saadate selle kliendile.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Näide: projekti teatud (automaatselt arvutatud) osa valmimisel põhineva arveldusreegli loomine

Teie organisatsioon, tarkvaraarendusettevõte, nõustub töötama kliendile välja palgaarvestuse paketi tasu eest 30 000. Klient nõustub maksma teie organisatsioonile valmis töö protsendi alusel. Hindate projekti maksumuseks 20 000. Projektilepingus on ära toodud töökategooriad, mida arveldusprotsessis kasutatakse. Saate seadistada arveldusreeglid, mis arvutavad automaatselt arvesummad iga kategooria lõpuleviidud töö protsendi jaoks. Seadistate iga kategooria eelarve.

-   **Arendus** – kulu 15 000 ja tulu 20 000
-   **Paigaldus** – kulu 5000 ja tulu 10 000

Esmakordsel kliendiarve koostamisel arvutatakse arve summa automaatselt järgmiste andmete põhjal.

-   Ühe kuu pärast esitab projektiga seotud töötaja projekti ajatabeli. Töötaja tundide maksumus on 5000 arenduse ja 1000 installimise eest. Arendustööst on valminud 33 protsenti (5000 tegelik kulu / 15 000 eelarvekulu) ja installimistööst on valminud 20 protsenti (1000 tegelik kulu / 5000 eelarvekulu).
-   Arve summa 8667 arvutatakse automaatselt (33 protsenti summast 20 000 + 20 protsenti summast 10 000).
-   Koostate arve summale 8667 ja saadate selle kliendile.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Näide: kokkulepitud vahe-eesmärkidel põhineva arveldusreegli loomine

Teie organisatsioon, juhtimiskonsultatsioonide firma, nõustub viima läbi turu-uuringu tarbekauba kohta, mida klient müüa kavatseb. Klient nõustub kasutama teie teenuseid kolme kuu jooksul, alates märtsist, ja nõustub tasuma teie organisatsioonile 50 000. Projektil on kolm vahetähtaega.

-   Vahe-eesmärk 1: tarbijaandmete kogumine – 31. märts
-   Vahe-eesmärk 2: tarbijaandmete analüüsimine – 30. aprill
-   Vahe-eesmärk 3: toote elujõulisuse soovituse esitamine – 31. mai

Klient nõustub maksma teie organisatsioonile 10 000 esimese vahe-eesmärgi, 20 000 teise vahe-eesmärgi ja 20 000 kolmanda vahe-eesmärgi eest. 

Projektilepingu seadistamisel lepite kokku, et esitate kliendile arveid saavutatud vahe-eesmärkide alusel. Arveldusreegli seadistus koosneb järgmistest etappidest.

-   Projekti vahe-eesmärkide määratlemine.
-   Määratlege summa, mille eest kliendile iga vahe-eesmärgi täitmise puhul arve esitatakse.

Esimese vahe-eesmärgi saavutamisel 31. märtsil märgite vahe-eesmärgi saavutatuks, koostate arve summas 10 000 ja saadate selle kliendile. Vahe-eesmärgi kohta ei saa esitada arvet enne, kui olete vahe-eesmärgi saavutatuks märkinud.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Näide: arveldusreegli loomine teenuste ja juhtimistasu põhjal

Teie organisatsioon, juhtimiskonsultatsioonide firma, nõustub viima läbi turu-uuringu, et hinnata kliendi (jaemüügiettevõtte) arendatava toote elujõulisust. Lepingu tingimustes on kirjas, et teenuseid osutavad teie kolm parimat juhtimiskonsultanti, kes viivad uuringu läbi aja- ja materjalikulu alusel. Klient nõustub maksma tunni kohta 100 pluss 10 protsenti juhtimistasu projekti raames arvestatud konsulteerimistundide eest. 

Projektilepingu seadistamisel saate luua arveldusreegli 10 protsendi juhtimistasu lisamiseks projekti raames arvestatud konsulteerimistundidele. 

Kliendi arvele lisatakse 10 protsendi suurune juhtimistasu pluss konsulteerimistundide hind. Näiteks kui kolm konsultanti töötas projektiga kokku 200 tundi, koostatakse arve summas 22 000, kasutades järgmist arvutust.

-   200 tundi tunnitasuga 100 = 20 000
-   10 protsenti juhtimistasu = 2000
-   Arve kogusumma = 22 000

Kui tasud on kliendi puhul maksustatavad ja valite projektilepingus käibemaksugrupi, sisestatakse käibemaksugrupp automaatselt tasude arveldusreeglisse.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Näide: arveldusreegli loomine aja ja materjali väärtuse kohta

Teie organisatsioon, tarkvarakonsultatsioonide firma, nõustub andma viis tehnilist konsultanti, kes töötavad kliendi tarkvara arendusprojektiga järgmise kuue kuu jooksul. Klient nõustub maksma 150 iga nõustamistunni eest pluss kontoritarvete maksumuse. Teie organisatsiooni saadab kliendile iga kuu lõpus arve. 

Projektilepingu seadistamisel lepite kokku, et esitate kliendile arveid igakuiselt projekti aja- ja materjalikulu eest. Saate luua arveldusreegli, mis sisaldab järgmist teavet.

-   Lepingu kestus on kuus kuud.
-   Konsultatsiooniaja hind tunni kohta on 150.
-   Kontoritarvete eest küsitakse tasu tegeliku kulu alusel ja projekti kulu kokku ei tohi olla üle 10 000.
-   Koostate projekti vältel kliendile iga kalendrikuu lõpus arve.

Esimese kuu jooksul registreerivad konsultandid projektile kokku 800 tundi. Projekti kontoritarvete kulu on 2000. Seega koostate kuu lõpus arve summas 122 000, mis sisaldab 800 tundi hinnaga 150 tunni kohta pluss 2000 kontoritarvete eest.




