---
title: Mis on uut või mida on muudetud rakenduse Dynamics 365 for Operations versioonis 1611 (november 2016)
description: Selles teemas kirjeldatakse Dynamics 365 for Operationsi versiooni 1611 uusi või muutunud funktsioone.
author: sericks007
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 221294
ms.assetid: 357931ed-f843-4bf5-bc85-0da3de0619ec
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0b3ede085533fee1bb779ed9da899f509a77fc0c
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693427"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-operations-version-1611-november-2016"></a>Mis on uut või mida on muudetud rakenduse Dynamics 365 for Operations versioonis 1611 (november 2016)

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse Dynamics 365 for Operationsi versiooni 1611 uusi või muutunud funktsioone.

## <a name="cost-accounting"></a>Kuluarvestus

<table>
<thead>
<tr>
<th>Mida saate teha</th>
<th>Miks on see oluline</th>
</tr>
</thead>
<tbody>
<tr>
<td>Määratlege kuluelemendi dimensioonid ja importige kuluelemendi dimensiooni numbrid.</td>
<td>Kuluelemente kasutatakse kuluarvestuses, et kategoriseerida kulusid ja dokumenteerida kulude voogu. Esmased kuluelemendid imporditakse kas Microsoft Dynamics 365 for Operationsi andmekonnektori abil, et tuua põhikontod otse Operationsist, või üldise andmekonnektori abil, kus saate põhikontod Microsoft Exceli kaudu mis tahes muud tüüpi lähtesüsteemist. Pärast põhikontode importimist kuluarvestusse kasutatakse neid kuluelemendi dimensiooniliikmetena. Teisesed kuluelemendid on kasutaja määratletud ja neid kasutatakse eraldamistes, et dokumenteerida kulude voolu.</td>
</tr>
<tr>
<td>Vastendage kuluelemendi dimensioonid.</td>
<td>Kui teie juriidiliste isikute põhikontosid ei saa jagada seadusjärgsete raamatupidamisnõuete tõttu, saate need vastendada pärast nende importimist kuluarvestusse, et saada kogu organisatsioonist terviklik vaade.</td>
</tr>
<tr>
<td>Määratlege kuluobjekti dimensioonid ja importige kuluobjekti dimensiooni liikmed.</td>
<td>Kuluobjektid on mis tahes tüüpi objektid, millele kulud on määratud. Tüüpilised kuluobjektid hõlmavad tooteid, projekte, ressursse, osakondi, kulukeskuseid ja geograafilisi regioone. Saate kasutada Microsoft Dynamics 365 for Operationsi andmekonnektorit, et tuua Operationsist finantsdimensioone ja väärtuseid, või kasutada üldist andmekonnektorit, kus saate tuua dimensioonid ja väärtused Exceli kaudu mis tahes muud tüüpi lähtesüsteemist. Näiteks kui kasutate objekti dimensioonina kulukeskuse finantsdimensiooni, siis on kõik imporditavad kulukeskused selle kuluobjekti dimensiooniliikmed.</td>
</tr>
<tr>
<td>Määratlege või importige statistilised dimensioonid.</td>
<td>Statistilise dimensiooni liikmeid mõõdetakse mitterahalistes ühikutes, nagu masinatunnid, töötajate arv ja nelinurk. Neid kasutatakse väljavõtetes või eraldiste ja jaotuste alusena.</td>
</tr>
<tr>
<td>Looge statistiliste mõõtude pakkuja mallid.</td>
<td>Statistilise mõõtude pakkuja malli kasutatakse rakenduse Dynamics 365 for Operations andmete teisendamiseks statistilisteks mõõtudeks. Mall seostatakse seejärel antud statistilise dimensiooni liikmega. Malle eelfiltreeritakse nii, et nad näitavad ainult tabeleid, mis on seostatud finantsdimensioonidega.</td>
</tr>
<tr>
<td>Looge kuluarvestuse pearaamatud.</td>
<td>Kuluarvestuse pearaamat on sõltumatu pearaamat, mis kasutab enda kalendrit ja valuutat. See mängib olulist rolli kõikide kulukannete töötlemisel. Näiteks klassifitseerib kuluarvestuse pearaamat kulud enda kuluelementide põhjal ja koondab kulud enda objekti dimensioonide põhjal. Saate luua nii palju kuluarvestuse pearaamatuid kui vaja, et teha halduse aruandlust erinevatest perspektiividest.</td>
</tr>
<tr>
<td>Looge kulujuhtseadmed.</td>
<td>Kulujuhtseadmed moodustavad kulustruktuuri ja määratlevad kulude voolu kuluarvestuse pearaamatus. Need tuleb seostada kuluobjekti dimensioonidega, et tähistada kuluobjekti dimensioone pearaamatus.</td>
</tr>
<tr>
<td>Töödelge pearaamatu kirjeid.</td>
<td>Tegeliku jõudluse mõõtmiseks peavad teil olema andmed. Andmed imporditakse, kasutades konnektoreid, mille määratlete kuluarvestuse pearaamatu jaoks. Pearaamatu kirjete töötlemisel imporditakse andmed järk-järgult.</td>
</tr>
<tr>
<td>Töötlege eelarve kirjeid.</td>
<td>Eelarvestatud jõudluse mõõtmiseks peavad teil olema andmed. Andmed imporditakse, kasutades konnektoreid, mille määratlete kuluarvestuse pearaamatu jaoks. Eelarve kirjete töötlemisel imporditakse andmed järk-järgult.</td>
</tr>
<tr>
<td>Looge ja rakendage kulukäitumise poliitikad.</td>
<td>Kasutage kulukäitumise poliitikat, et klassifitseerida kulud kui fikseeritud, muutuvad või poolmuutuvad. Poliitika on reeglipõhine ja kuupäeva-efektiivne. Vaikimisi märgitakse kõik kulud klassifitseerimata kuludeks, kuni rakendate kulukäitumise poliitika ja arvutate reegli mõjud. Pärast arvutamist kulud klassifitseeritakse.</td>
</tr>
<tr>
<td>Jälgige kulusid.</td>
<td>Aitamaks teil mõista kulupoliitikate mõju, võimaldab kuluarvestus teil jälgida kulusid lähteväärtusteni ja rakendatud reegliteni, kust need pärinevad. See funktsioon pakub täieliku jälgitavuse selle kohta, millal kulud tekkisid, mis tüüpi kulud tekkisid ja milliseid kulukäitumise reegleid rakendati.</td>
</tr>
<tr>
<td>Määratlege dimensioonihierarhiad.</td>
<td>Saate luua dimensioonihierarhiad kategoriseerimise või klassifitseerimise otstarbel. Näiteks saate määratleda kategooriahierarhia, mis põhineb kuluelemendi dimensioonil ja selle liikmetel. Teise võimalusena saate määratleda klassifitseerimishierarhia, mis põhineb kuluobjekti dimensioonil ja selle liikmetel. Aruandluse struktuure kasutatakse järgmistes olukordades:
<ul>
<li>Te määratlete eraldised, kulumäärad ja kulukomplekti reeglid.</li>
<li>Vaadake väljavõtteid, kasutades tööruumi.</li>
<li>Määratlege juurdepääs, et vaadata koondatud andmeid.</li>
<li>Vaadake andmeid Excelis.</li>
</ul></td>
</tr>
<tr>
<td>Looge väljavõtted, mida saab vaadata tööruumis.</td>
<td>Kasutage tööruumi, et saada kiirülevaade tegelikest ja eelarvestatud kuludest ja ka kõrvalkalletest. Saate filtreerida andmeid perioodi või kulutaseme alusel. Tööruum on mõeldud juhtidele, kes vastutavad kulude kontrolli eest. See järgib juurdepääsureegleid, mis on dimensioonihierarhiate jaoks määratletud.</td>
</tr>
<tr>
<td>Looge aruandeid Excelit kasutades.
<blockquote>[!NOTE] Peate käivitama Microsoft Excel 2016.</blockquote>
</td>
<td>Saate eksportida kuluarvestuse andmed andmeüksuste kaudu otse Excelisse ja kasutada aruannete loomiseks Microsoft PivotTable'it.</td>
</tr>
</tbody>
</table>

## <a name="expense-management"></a>Kulude haldus

| Mida saate teha | Miks on see oluline |
|-----------------|-----------------------|
| Määrake ümber lõpetatud töötaja krediitkaardi kanded. | Mõnikord, kui töötaja lõpetatakse, keelatakse tema Active Directory' kataloogiteenuste (AD DS) konto selliste aktiivste krediitkaardi kannete importimisel, mis tuleb kuludesse kanda. Varasemalt ei saanud te määrata delegaati kulukirje jaoks või manustada krediitkaardi kandeid kuluaruandele. Nüüd saate kasutada lehte **Krediitkaardikanded**, et määrata töötaja ümber mis tahes krediitkaardi kandele, kus seostatud töötaja on lõpetatud. Pärast krediitkaardi kande ümbermääramist saab kande kuluaruande jaoks valida ja tasuda regulaarse kuluaruande korvamise protsessi kaudu. |
| Muutke krediitkaardi kuluteavet ootelolevatele ja varasematele töötajatele. | Saate muuta kuluhalduse krediitkaardi teavet ootelolevatele ja varasematele töötajatele. Varasemalt võisite muuta krediitkaardi kuluteavet ainult siis, kui töötaja on aktiivne töötaja. |
| Kopeerige kuluaruanne. | Nüüd saate kopeerida olemasoleva kulu uue kulu loomisel samas kuluaruandes. Saate kopeerida kuluaruande ja kõik seotud mittekrediitkaardi kulud uude kuluaruandesse. Peate ikka määratletud kulupoliitikate ja -kategooriate põhjal tegema mis tahes vajalikud loetelud ja manustama vajalikud kviitungid. Saate lisada krediitkaardi kanded kuluaruandele, valides vastavusseviimata kulude lisamise. |
| Redigeerige kulusid hulgi. | Mõned krediitkaardi kanded ei pruugi olla vastendatud kulukategooriale või need võivad importimisel olla valesti vastendatud. Sellisel juhul peavad töötajad seostatud kulukategooriate käsitsi muutma. Vastavusseviimata kulude haldamisel saate nüüd valitud kulude puhul kulukategooriat hulgiredigeerimida. Lisaks, kui haldate spetsiifilise kuluaruande jaok valitud kulusid, saate projekti ja lisateavet hulgiredigeerida. |
| Muutke krediitkaardi kannete jaoks vahetuskurssi. | Tegelik vahetuskurss, mida krediitkaardi kande puhul kasutatakse, võib erineda süsteemis seadistatud vahetuskursist. Varasemalt ei saanud töötajad muuta vahetuskurssi mis tahes kuluhaldusesse imporditud krediitkaardi kandele. Nüüd saate seada parameetri lehel **Kulutuste haldamise parameetrid**, et võimaldada vahetuskursi muutmist krediitkaardi kannetele. |
| Seadistage kulude jaoks korruptsioonivastane atesteerimine. | Mõnedel organisatsiooni töötajatel võib olla äritegevusi riigiametnikega ja mõnesid kulusid, mis tekivad osana nendest äritegevustest, võidakse näha altkäemaksuna. Kuluhalduses saate nüüd seadistada korruptsioonivastase atesteerimise, mida näidatakse valitud kulukategooriate puhul, nagu eined ja kingitused. Töötajad peavad valima, kas kulud, mis seadistatakse korruptsioonivastase atesteerimise jaoks, vastavad kriteeriumitele, mis määratletakse teie organisatsiooni poliitikatega. |
| Ennetage kulude käsitsi sisestamist teatud kulukategooriate puhul. | Kulukategooria saab seadistada tähistama krediitkaardi kannet, mille jaoks kategooriat ei saa muuta. Näide on tasu krediitkaardi hilise makse jaoks. Nüüd saate seadistada kulukategooria, mis võimaldab kulusid luua ainult impordi kaudu. See funktsioon takistab töötajatel kategooria jaoks käsitsi kulu luua. See ei luba ka kategooria muutmist kannetele, mis on imporditud ja mis kasutavad seda kategooriat. |
| Manustage kviitung mitmele kulule. | Kviitung, mis laetakse üles kuluhaldusesse, võib olla seotud mitme kuluga. Varem tuli mitme kuluga seotud kviitung iga kulu jaoks ühe korra üles laadida. Nüüd saate manustada kviitungi kulule, mis on juba üles laetud ja manustatud samal kuluaruandel teisele kulule. Lisaks kui laadite kviitungi üles kuluaruande päisesse, saate valida ühe või mitu rida, millele kviitung manustada. |
| Looge tulevase kuupäevaga kulud. | Kuluaruande kopeerimisel võib kulu kandel olla tulevane kuupäev. Varasemad väljalasked ei võimalda tulevase kuupäevaga kulusid. Nüüd saate luua ja salvestada kulusid, millel on tulevane kuupäev. Siiski ei saa te edastada tulevase kuupäevage kulu. |
| Konfigureerige kulu maksud osariigi/maakonna jaoks. | Mõnedes riikides/regioonides võivad erinevates osariikides/maakondades tekkinud kuludele kehtida erinevad müügimaksu määrad. Nüüd saate seadistada kulu maksu konfiguratsioonid osariigi/maakonna tasemel, mitte lihtsalt riigi/regiooni tasemel. Kui jätate välja **Osariik/provints** lehel **Maksu konfiguratsioon** tühjaks, rakendub määratud riigi/regiooni puhul müügimaksu grupp kõikidele osariikidele/provintsidele määratud riigi/regiooni puhul. |
| Seadistage kulu krediitkaardi tüübid. | Varasemalt ei olnud ühtki lehte, kus võisite luua krediitkaardi tüüpe, nagu Visa, MasterCard või AMEX, mida saaks kasutada kuluhaldusega. Nüüd saate luua krediitkaardi tüüpe, mida kasutada kuluhaldusega. Leht asub lehel **Seadistus** jaotises **Arvutused ja koodid**. |
| Määratlege kuluaruannete jaoks mitmetasandiline kinnitamise töövoog. | Uus töövoog kuluaruannete jaoks toetab mitmetasandilist kinnitamise protsessi. Töötajad sisestavad ajutised kinnitajad ja lõplikud kinnitajad kuluaruande loomisel. Töövoog suunab kuluaruande seejärel esmalt ajutistele kinnitajatele. Pärast kuluaruande sellisel tasemel kinnitamist suunab töövoog selle lõplikuks kinnitamiseks lõplikele kinnitajatele. |
| Looge ja hallake kulusid, mis ei ole manustatud kuluaruandele. | Kasutaja saab nüüd kulusid luua ja neid hallata (näiteks manustades või täpsustades kviitungeid või määrates külalisi) ilma esmalt kuluaruannet loomata. Uuele kuluaruandele saab valida ja lisada ühe või mitu kulu, et need saaks edastada kinnitamiseks. Valikus **Kulude haldus** &gt; **Minu kulud** &gt; **Kulud** on kulude haldamiseks saadaval uus leht. |

## <a name="financial-management"></a>Finantshaldus

<table>
<thead>
<tr>
<th>Mida saate teha</th>
<th>Miks on see oluline</th>
</tr>
</thead>
<tbody>
<tr>
<td>Jälgige põhivara hindamist, kasutades üksiku „raamatu” kontseptsiooni.</td>
<td>Varasemalt kasutati põhivara väärtuste jälgimiseks kaht eraldi hindamise tüüpi: väärtusmudelid ja kulumiraamatud. Praeguses versioonis on need kaks kontseptsiooni liidetud üheks hindamise kontseptsiooniks, mida nimetatakse raamatuteks. Raamatutel on kõik nii väärtusmudelite kui ka kulumiraamatute funktsioonid. Näiteks saate pearaamatusse sisestamise välja lülitada. Raamatuid, mis sisestatakse pearaamatusse, kasutatakse tavaliselt ettevõtte finantsaruandluses. Raamatuid, mida ei sisestata pearaamatusse, kasutatakse tavaliselt maksuaruandluse jaoks.</td>
</tr>
<tr>
<td>Tehke pearaamatu rahandusaasta sulgemine mitmele juriidilisele isikule.</td>
<td>Rahandusaasta sulgemise protsessi kiirendamiseks saate nüüd jagatud rahandusaasta sulgemise lehelt käivitada rahandusaasta sulgemise mitmele juriidilisele isikule. Juriidiliste isikute grupid saab määratleda koos sätetega, mis tuleks säilitada ühelt aastalt teisele. Rahandusaasta sulgemise protsessile on tehtud ka teised kasutatavuse täiustused.</td>
</tr>
<tr>
<td>Kasutage pearaamatu välisvaluuta ümberarvutamise täiustuste eeliseid.</td>
<td>Pearaamatu protsessile on välisvaluuta ümberarvutamise jaoks tehtud järgmised täiustused.
<ul>
<li>Vahetuskursi tüüp on lisatud põhikontole. Seda vahetuskursi tüüpi kasutatakse nüüd, et määrata valuuta ümberarvutamise käigus vahetuskurss. Kui ühtki vahetuskursi tüüpi ei määratleta, jätkub protsess, et kasutada pearaamatus määratletud vahetuskursi tüüpi.</li>
<li>Nüüd on lihtsam valida põhikontode ja valuutade vahemik, mille jaoks ümberarvutamise protsess käivitada.</li>
<li>Ümberarvutamise saab käivitada mitmele juriidilisele isikule.</li>
<li>Süsteem säilitab nüüd iga tehtud ümberarvutamise protsessi ajaloo, nagu see teeb seda ka müügireskontro ja ostureskontro ümberarvutamise protsesside jaoks.</li>
<li>Protsessi käivitamisel saate nüüd ümberarvutamise tulemusi eelvaadata. Eelvaade näitab tulemusi kõikidele juriidilistele isikutele, kelle jaoks protsess käivitati. Seejärel saate eelvaatest sisestada kõik juriidilised isikud või nende alamkogumi. Seejärel saate eksportida eelvaates olevad tulemused Excelisse.</li>
</ul></td>
</tr>
<tr>
<td>Saate täiendavate sisestamiskihtide jaoks kuvada kanded.</td>
<td>Loendilehel <strong>Proovibilanss</strong> ja aruandes <strong>Dimensiooniaruanne</strong> saate nüüd valida täiendavad sisestamiskihid, mis on lisatud pearaamatusse. Täiendavate sisestamiskihtide valimisel kaasatakse nende sisestamiskihtide korrigeerimised loendilehe või aruande saldodele.</td>
</tr>
<tr>
<td>Manustage õpetusdokumentatsioon finantsperioodi sulgemismallile.</td>
<td>Varasemalt võisite manustada dokumentatsiooni pärast ülesande lõpuleviimist. Näiteks võisite manustada loodud aruande. Nüüd saate mallile manustada ka õpetusdokumendi. See õpetusdokument kopeeritakse seejärel igale ülesandele finantsperioodi graafikus, et ülesande omanik saaks vaadata juhiseid selle kohta, kuidas ülesanne lõpule viia.</td>
</tr>
<tr>
<td>Määratlege kontsernisisese raamatupidamise seadistus ühiskasutusega lehelt.</td>
<td><strong>Kontsernisisese raamatupidamise seadistuse leht</strong> on nüüd ühiskasutuses, et organisatsioon saaks määratleda kõik juriidiliste isikute paarid, mis saavad teineteisega tehinguid teha. Lisaks saate nüüd sisestada kande pärinevasse juriidilisse isikusse, kuid mitte sihtkoha juriidilisse isikusse. Kui kumbki juriidiline isik saab käivitada kontsernisisese kande, tuleb määratleda vastastikune paar. Seetõttu seadistatakse sihtkoha juriidiline isik samuti pärineva juriidilise isikuna.</td>
</tr>
<tr>
<td>Edastage eelarveplaanide jaoks põhjendusdokumendid.</td>
<td>Nüüd saate mis tahes soovitud eelarvesummade jaoks luua täiendava dokumentatsiooni. Kasutajad saavad täita malli üksikasjad ja manustada malli eelarveplaanile, et seda saaks kasutada kinnitusprotsessi käigus.</td>
</tr>
<tr>
<td>Lubage eelarve registrikannete jaoks täpsemad reeglid.</td>
<td>Kui pearaamatus konfigureeritakse täpsemad reeglid, saab neid reegleid eelarveregistris kasutada uute kirjete ja ülekannete jaoks.</td>
</tr>
<tr>
<td>Kasutage ettemaksu arveldamise tegevuse suurendatud nähtavust.</td>
<td>Uus loendileht <strong>Avatud ettemaksed</strong> annab hetktõmmise ettemaksu arveldamise tegevuse olekust. Leht annab AP osakonnale teavet ostutellimuste kohta, millel on ülejäänud ettemaksu väärtused, mis tuleb arveldada, arveldatud väärtused, mis tuleb tasuda, ja makstud arveväärtused, mis tuleb rakendada standardsetele arvetele. Lisaks aitavad täiustused, mis tehakse standardsetele arvetele makstud ettemaksu arvete automaatsele rakendamisele, arve ametnikel andmete sisestust tõhusamalt teha.</td>
</tr>
<tr>
<td>Kasutage tööruumi <strong>Hankija koostöö arveldamine</strong>.</td>
<td>Uus tööruum <strong>Arve koostamine</strong> alas <strong>Hankija koostöö</strong> võimaldab välistel hankijatel turvaliselt nende arveteabele juurde pääseda. Näiteks saavad hankijad näha, kas arve on makstud ja edasta enda arve. See muudatus soodustab tõhusamat ja õigeaegset kommunikatsiooni väliste hankijatega. See on arveldamise ametnikel vähem katkestusi.</td>
</tr>
<tr>
<td>Vahetage juriidilisi isikuid arve sisestamise käigus.</td>
<td>Täiustused võimaldavad arveldamise ametnikel, kes peavad arveid esitama mitmele juriidilise isikule, kiiresti muuta juriidilist isikut arveldamise lehtedelt. See funktsioon säästab arveldamise ametnike aega, kuna nad ei pea enam praegusest juriidilisest isikust välja logima ja teisele juriidilise isikule sisse logima. Nii leht <strong>Globaalne arve tööleht</strong> kui ka leht <strong>Hankijaarved</strong> võimaldavad kasutajatel andmesisestuse käigus juriidilist isikut muuta.</td>
</tr>
<tr>
<td>Tugi elektroonilistele failidele USA Maksuameti (IRS) 1099 kombineeritud föderaalse/osariigi registreerimise programmi jaoks</td>
<td>Kui konfiguratsioonivõti <strong>US</strong> aktiveeritakse, pakub 1099 elektroonilise esitamise protsess täiendava funktsionaalsuse, mis vastab kombineeritud föderaalse/osariigi esitamise programmi IRS-i regulatsioonidele. IRS lõi selle programmi, et see saaks saadetud teavet elektrooniliselt osalevatele osariikidele edasi saata.</td>
</tr>
<tr>
<td>Lahendamise täiustused</td>
<td>Täiustused aitavad makseametnikel lahendusi tõhusamalt teha, kuna ametnikud saavad lubada mitme sisestamata makse sama arve suhtes tasakaalustamist.</td>
</tr>
<tr>
<td>Kontsernisisene vaade</td>
<td>Tsentraliseeritud makseametnikud saavad nüüd vaadata tähtaja ületanud arveid ettevõtete vahel. Tööruumid <strong>Hankijamaksed</strong> ja <strong>Kliendimaksed</strong> pakuvad nüüd paremat nähtavust tähtaja ületanud arvetele ja paremat kontrolli nende üle, andes viisi, kuidas vaadata ja filtreerida ettevõtete vahel, mis on osa tsentraliseeritud organisatsioonilisest hierarhiast.</td>
</tr>
<tr>
<td>Kasutage tööruumi <strong>Pangahaldus</strong>.</td>
<td>Uus tööruum <strong>Pangahaldus</strong> aitab jälgida teie juriidiliste isikute pangakontosid ja saldosid. Praegused ja ootelolevad saldod on kohe kõikide kontode jaoks kättesaadavad ja te saate puurida tagasi saldodest üksikasjalikesse tehingukannetesse. Samuti saate näha iga pangakonto ajaloolise saldo andmeid või kokkuvõtet kõikidest ettevõtte pangakontodest, nii lühiajalistes kui ka pikaajalistes vaadetes. Saate parema ülevaate pangakonto vastavusseviimisest, kuna viimase vastavusseviimise kuupäev teatatakse iga pangakonto kohta ja on ka indikaator pooleliolevate vastavusseviimiste kohta.</td>
</tr>
<tr>
<td>Importige elektroonilisi pangaväljavõtteid kõikidele juriidilistele isikutele ühes etapis.</td>
<td>Nüüd saate importida elektroonilisi väljavõtteid kõikidele juriidilistele isikutele ühes etapis. Pangaväljavõtte failid saavad sisaldada väljavõtteid paljudelt pangakontodelt ja juriidilistest isikutelt ja zip-failid saavad sisaldada mitmeid pangaväljavõtte faile. Üksiku impordiprotsessi kasutamisega saate käivitada vastavusseviimise kõikidele aruandes sisalduvatele pangakontodele kõikidel juriidilistel isikutel. See funktsioon aitab säästa aega, kuna te ei pea vahetama ettevõtete ja mitme väljavõtte importide vahel. Saate automaatselt käivitada vastendamise reeglid kõikide igas ettevõttes imporditud väljavõtete suhtes.</td>
</tr>
<tr>
<td>Hindamise jälgimine</td>
<td>Üksikul põhivaral võib olla mitu hindamist erinevatele raamatupidamise standarditele ja saab valikuliselt sisestada seostatud kandeid pearaamatusse. Varasemalt jälgiti neid hindamisi, kasutades väärtusmudeleid või kulumiraamatuid. Nüüd saate jälgida neid hindamisi, mida nimetatakse nüüd raamatuteks, kasutades töölehtede, päringute ja aruannete ühist komplekti. Ühtlustatud kogemus lihtsustab juurutamist ja vähendab liideste arvu, mida perioodiline protsess nõuab.</td>
</tr>
<tr>
<td>Kasutage kontsernisiseste kulumikäituste täiustuste eeliseid.</td>
<td>Nüüd saate ühelt lehelt käivitada kulumikäituse kõikide juriidiliste isikute varadele. Samuti saate automaatselt sisestada töölehti pärast nende loomist. Saate saata töölehtede loomise ja sisestamise pakktöötlusesse, et kulum käitaks taustal. Need täiustused vähendavad ebatõhusust, kuna te ei pea käivitama individuaalseid kulumi käituseid iga ettevõtte jaoks eraldi. Täiustus võimaldab ka teie põhivarade paremini tsentraliseertud haldust.</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>Inimkapitali juhtimine

<table>
<thead>
<tr>
<th>Mida saate teha</th>
<th>Miks on see oluline</th>
</tr>
</thead>
<tbody>
<tr>
<td>Looge jõudluse tööleht.</td>
<td>Enne ülevaate lõpuleviimist kogute sageli teavet tegevuste ja sündmuste kohta, mis aitasid ülevaatusperioodi jooksul kaasa teie edule töötajana. Saate lisada oma jõudluse töölehele kirje nende tegevuste ja sündmuste dokumenteerimiseks. Samuti saate ühendada need tegevused ja sündmused eesmärgi või jõudluse ülevaatega, et pakkuda ülevaatajale rohkem teavet.</td>
</tr>
<tr>
<td>Looge üksikasjalikumad eesmärgid.</td>
<td>Teil on rohkem kontrolli teie seatud eesmärkide sisu üle. Saab luua eesmärkide jaoks mõõtmiseid, siduda jõudluse töölehe kirjeid mõõtmistega ning manustada ja vaadata dokumente. Saate talletada eesmärke mallidena ja taaskasutada neid kiirseadistuse jaoks.</td>
</tr>
<tr>
<td>Looge üksikasjalikumad jõudluse ülevaated.</td>
<td>Jõudluse ülevaated, mis on ametlikult tuntud kui arutelud, on nüüd piisavalt paindlikud, et toetada nii pidevat tagasisidet kui ka ametlikke ülevaateid. Saate tõmmata aktiivseid eesmärke ja sisestada nende kohta kommentaare ning lisada jaotiseid pädevuste ülevaatamiseks. Antud on täiendavad jaotised, kus saate lisada ja vaadatada ülevaatega seotud mõõtmiseid, jõudluse töölehe sisestusi, manuseid ja nõusolekuid.</td>
</tr>
<tr>
<td>Seostage täiendavad positsioonihierarhiad töövoogudega.</td>
<td>Saate seostada töövoo positsioonihierarhiaga. Samuti saate modifitseerida töövooetappe, et optimeerida kinnitamisprotsessi nii, et see sobituks teie ärivajadustega. Seetõttu saate määratleda tõhus heakskiidu struktuuri, mis sobib erinevate aruandesuhted, mida organisatsioon kasutab.</td>
</tr>
<tr>
<td>Töövoo tugi isikukoodide (PIN-id) sisestamiseks töötaja iseteenindusse.</td>
<td>Töövoo võimsust inimressurside (HR) jaoks on laiendatud ja see hõlmab nüüd tuge PIN-idele. Töötajad saab lisada ja redigeerida oma PIN-i, et tõhusust täiustada. Siiski saavad inimressursside töötajad seda teavet täpsuse ja täielikkuse osas üle vaadata enne, kui nad lisavad selle töötaja kirjele.</td>
</tr>
<tr>
<td>Looge eesmärgimalle ja kasutage neid uute eesmärkide lisamiseks.</td>
<td>Saate luua eesmärgimalle eesmärkidele, mis on paljudel ettevõtte töötajatel ühiskasutuses. Töötajad saavad lisada mallist nende enda eesmärke, juhid saavad lisada mallist nende meeskonna jaoks eesmärke ja inimressursside meeskonna liikmed saavad lisada ettevõtte töötajate jaoks eesmärke.</td>
</tr>
<tr>
<td>Looge eesmärgigrupid ja kasutage neid uute eesmärkide lisamiseks.</td>
<td>Saate lisada grupile eesmärgimalle ja kasutada gruppi, et luua töötaja, meeskonna, positsiooni, osakonna või ettevõtte jaoks üks või rohkem eesmärke.</td>
</tr>
<tr>
<td>Rohkem kontrolli ülevaatamisprotsessi üle.</td>
<td>Saate kasutada ülevaatamisprotsessi juhtimiseks töövoogu. Saate luua ülevaatemalle ja kasutada neid ülevaadete loomiseks. Samuti saate ülevaatele lisada hinnanguid.</td>
</tr>
<tr>
<td>Kasutage ülevaateperioode, et määratleda ülevaate jaoks ajaraamistik.</td>
<td>Saate määratleda jõudluse ülevaate jaoks ajaperioodi ning ülevaate algus- ja lõppkuupäevad sisestatakse automaatselt. Siiski saate muuta neid vaikekuupäevi vastavalt vajadusele.</td>
</tr>
<tr>
<td>Inimressursside viiele uuele Power BI sisupaketile juurdepääsemine</td>
<td>Uued sisupaketid võimaldavad inimressursside organisatsioonidel ja inimressurside juhtidel analüüsida järgmist.
<p>Tööjõu mõõdikud</p>
<ul>
<li>Demograafilised jaotused vanuse, soo ja perekonnaseisu järgi</li>
<li>Kulutamismäärade võrdlemine aastate lõikes ja loendi nägemine põhjustest, mille töötajad on andnud organisatsioonist lahkumiseks</li>
<li>Avatud ametkohtade loendi vaatamine, aga ka avatud ja suletud ametikohtade võrdlus</li>
</ul>
<p>Hüvitused ja soodustused</p>
<ul>
<li>Tunnipõhiste ja põhipalgaga töötajate vaatamine</li>
<li>Saadaolevatesse soodustustesse registreeritud töötajate arvu vaatamine</li>
<li>Töötajate vaatamine töösuhte tüübi alusel:</li>
</ul>
<p>Värbamine</p>
<ul>
<li>Kandidaatide analüüsimine kandidaatide arvu, nende päritolu ja ametikohtade põhjal, kuhu nad kandideerivad eesmärgil</li>
</ul>
<p>Organisatsiooni koolitus</p>
<ul>
<li>Kursusele registreerimine asukoha järgi</li>
<li>Kursusel kohalviimine staatuse järgi</li>
<li>Töötajate loend, kes on registreeritud kursusele</li>
</ul>
<p>Töötaja pädevused ja areng</p>
<ul>
<li>Töötajate oskuste loend</li>
<li>Oskusetüüpide jaotus meeskonnaliikme alusel</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="localizations"></a>Lokaliseerimised

<table>
<thead>
<tr>
<th>Mida saate teha</th>
<th>Miks on see oluline</th>
</tr>
</thead>
<tbody>
<tr>
<td>Lokalisatsioonid on saadaval 18 lisariigile:
<ul>
<li>Austria</li>
<li>Belgia</li>
<li>Brasiilia</li>
<li>Hiina</li>
<li>Tšehhi Vabariik</li>
<li>Eesti</li>
<li>Soome</li>
<li>Ungari</li>
<li>Itaalia</li>
<li>Läti</li>
<li>Leedu</li>
<li>Norra</li>
<li>Poola</li>
<li>Saudi Araabia</li>
<li>Hispaania</li>
<li>Rootsi</li>
<li>Šveits</li>
<li>Tai</li>
</ul>
<p>Järgmised riigid nõuavad ka jaemüügi lokaliseerimist. Jaemüügi lokaliseerimist pole nende riikide jaoks lõpule viidud ja on plaanitud ainult H1 CY2017-le.</p>
<ul>
<li>Brasiilia</li>
<li>Tšehhi Vabariik</li>
<li>Eesti</li>
<li>Ungari</li>
<li>Läti</li>
<li>Leedu</li>
<li>Malaisia</li>
<li>Poola</li>
<li>Rootsi</li>
</ul>
</td>
<td>Dynamics 365 for Operations on saadaval veel 18 riigis. Osana meie pingutusest muuta lokaliseerimist lihtsamaks ja paremini konfigureeritavamaks on regulatiivsed elektroonilised aruandluse funktsioonid teisendatud elektroonilise aruandluse (ER) konfiguratsioonideks ning mõned teenuse Microsoft SQL Server Reporting Services (SSRS) regulatiivaruanded on teisendatud elektroonilise aruandluse konfiguratsioonideks, mis kasutavad Exceli malle. Neid teisendatud funktsioone on spetsiaalselt mainitud hiljem selles tabelis.</td>
</tr>
<tr>
<td>Jaapan – põhivarade grupeerimine vormi 26 ja sellele lisatud tabelite printimisel.</td>
<td>Vorm 26 tuleb edastada igasse linna, kus ettevõtte tegutseb. Vähendamaks teie vaeva vormi 26 printimisel saab põhivara automaatselt asukoha järgi grupeerida ja sortida.</td>
</tr>
<tr>
<td>Jaapan – kiirendatud ja täiendava kulumi summade vaatamine profiilis.</td>
<td>Profiil saab pakkuda kiirendatud ja täiendava kulumi summade täpset eelarvestust.</td>
</tr>
<tr>
<td>Jaapan – kinnipeetava maksu progressiivne arvutamine.</td>
<td>Jaapani valitsus nõuab, et arvutaksite kinnipeetavat maksu progressiivselt maksesumma põhjal.</td>
</tr>
<tr>
<td>Jaapan – sihtnumbri faili importimine spetsiifiliselt suurte ettevõtte ehitiste puhul.</td>
<td>Sihtnumbri faili, mille asutus annab konkreetsetele suure ettevõtte ehitistele, saab importida süsteemi. Aadressi saab seejärel tuletada sihtnumbritest.</td>
</tr>
<tr>
<td>Jaapan – põhivarade jaoks jõudeperioodi konfigureerimine.</td>
<td>Jõudeoleku periood võimaldab kasutajal peatada põhivara kulumit täpsustatud perioodi jooksul. Seda funktsiooni nõuab määrus.</td>
</tr>
<tr>
<td>Euroopa – käibemaksu (KM) registreerimisnumbri konfigureerimine osapoole aadressile, kasutades registreerimise ID raamistikku.</td>
<td>Saate konfigureerida KM-i registreerimisnumbri osapoole aadressile, kasutades registreerimise ID raamistikku ja uut <strong>KM-i ID</strong> registreerimiskategooria KM ID-d.</td>
</tr>
<tr>
<td>Soome – tolli kliendikoodi konfigureerimine osapoole aadressi jaoks, kasutades registreerimise ID raamistiku.</td>
<td>Saate konfigureerida tolli kliendikood osapoole aadressile, kasutades registreerimise ID raamistikku ja uut registreerimiskategooriat <strong>Tollikliendi ID</strong>.</td>
</tr>
<tr>
<td>Prantsusmaa – kliendiarvete printimine Prantsusmaale omases paigutuses.</td>
<td>Kliendiarve väljatrükki kohandatakse nii, et see vastaks Prantsusmaa nõuetele.</td>
</tr>
<tr>
<td>Prantsusmaa – dokumentide kronoloogilise nummerdamise jõustamine rahandusperioodi alusel.</td>
<td>Prantsusmaa nõuete täitmiseks kliendiarvete nummerdamisel saate seadistada kliendiarvete numbriseeriad rahandusperioodi alusel.</td>
</tr>
<tr>
<td>Austria lokalisatsioon – elektroonilise aruandluse konfiguratsioonid</td>
<td>
<ul>
<li>EL-i käibearuande XML-i vorming Austria puhul</li>
<li>Intrastati vorming Austria puhul</li>
<li>ISO20022 kreeditiülekande maksevorming Austria puhul</li>
<li>ISO20022 otsedeebeti maksevorming Austria puhul</li>
<li>Austria EDIFACT-PAYMUL-vorming</li>
<li>Käibemaksudeklaratsioon Austria puhul</li>
</ul>
</td>
</tr>
<tr>
<td>Belgia lokalisatsioon – elektroonilise aruandluse konfiguratsioonid</td>
<td>
<ul>
<li>BLWI vorming Belgia puhul</li>
<li>EL-i käibearuande XML-i vorming Belgia puhul</li>
<li>Põhivarade aruanne Belgia puhul</li>
<li>Intervati vorming Belgia puhul</li>
<li>Intrastati vorming Belgia puhul</li>
<li>Arve käibe aruanne Belgia puhul</li>
<li>Pearaamatu kande ekspordivorming Belgia puhul</li>
<li>SWIFT hankija makse vorming Belgia puhul</li>
<li>CODA pangaväljavõtte impordivorming Belgia puhul</li>
<li>ISO20022 kreeditiülekande maksevorming Belgia puhul</li>
<li>ISO20022 otsedeebeti maksevorming Belgia puhul</li>
</ul>
</td>
</tr>
<tr>
<td>Brasiilia lokalisatsioon – elektroonilise aruandluse konfiguratsioonid</td>
<td>
<ul>
<li>GIA SP Brasiilia puhul</li>
<li>GIA-ST Brasiilia puhul</li>
</ul>
</td>
</tr>
<tr>
<td>Tšehhi Vabariigi lokaliseerimine – elektroonilise aruandluse konfiguratsioonid</td>
<td>
<ul>
<li>EL-i käibearuande XML-vorming Tšehhi Vabariigi puhul</li>
<li>Intrastat-vorming Tšehhi Vabariigi puhul</li>
<li>Käibemaksudeklaratsioon Tšehhi Vabariigi puhul</li>
</ul>
</td>
</tr>
<tr>
<td>Hiina lokalisatsioon – elektroonilise aruandluse konfiguratsioonid</td>
<td>
<ul>
<li>Kliendi ajalise jaotuse aruande vorming Hiina puhul</li>
<li>Kliendi tähtajasumma analüüsiaruande vorming Hiina puhul</li>
<li>Hankija ajalise jaotuse aruande vorming Hiina puhul</li>
<li>Hankija tähtajasumma analüüsiaruande vorming Hiina puhul</li>
<li>Saadaoleva makse ajalise jaotuse analüüsi vorming Hiina puhul</li>
<li>Kliendi saldo aruande vorming Hiina puhul</li>
<li>Pearaamatukonto saldo aruande vorming Hiina puhul</li>
<li>Hankija saldo aruande vorming Hiina puhul</li>
<li>GBT fail Hiina puhul</li>
<li>Kuldse maksusüsteemi ekspordifaili vorming</li>
<li>Tootmise tarbimise hälbe aruande vorming Hiina puhul</li>
</ul>
</td>
</tr>
<tr>
<td>Eesti lokalisatsioon – elektroonilise aruandluse konfiguratsioonid</td>
<td>
<ul>
<li>EL-i käibearuande XML-vorming Eesti puhul</li>
<li>Intrastati vorming Eesti puhul</li>
<li>Varude ümberklassifitseerimise väljavõte Eesti puhul</li>
<li>ISO20022 kreeditiülekande maksevorming Eesti puhul</li>
<li>Kliendi hankija saldoteatise aruanne Eesti puhul</li>
<li>Käibemaksudeklaratsioon Eesti puhul</li>
</ul>
</td>
</tr>
<tr>
<td>Soome lokalisatsioon – elektroonilise aruandluse konfiguratsioonid</td>
<td>
<ul>
<li>EL-i käibearuande TXT-vorming Soome puhul</li>
<li>Intrastati vorming Soome puhul</li>
<li>ISO20022 kreeditiülekande maksevorming Soome puhul</li>
</ul>
</td>
</tr>
<tr>
<td>Ungari lokalisatsioon – elektroonilise aruandluse konfiguratsioonid</td>
<td>
<ul>
<li>EL-i käibaruande XML-vorming Eesti puhul</li>
<li>Intrastati vorming Ungari puhul</li>
<li>Intrastati lihtsustatud vorming Ungari puhul</li>
<li>Arveloendi ekspordivorming Ungari puhul</li>
<li>Käibemaksu deklaratsioon Ungari puhul</li>
<li>Käibemaksu deklaratsiooni üksikasjalik loetelu Ungari puhul</li>
<li>Inventuuriväljavõte Ungari puhul</li>
<li>MultiCashi maksevorming Ungari puhul</li>
</ul>
</td>
</tr>
<tr>
<td>Itaalia lokalisatsioon – elektroonilise aruandluse konfiguratsioonid</td>
<td>
<ul>
<li>Intrastati vorming Itaalia puhul</li>
<li>Projektiarve vorming Itaalia puhul</li>
<li>Müügiarve vorming Itaalia puhul</li>
<li>ISO20022 kreeditiülekande maksevorming Itaalia puhul</li>
<li>ISO20022 otsedeebeti maksevorming Itaalia puhul</li>
<li>RIBA kogumise rahaülekande vorming Itaalia puhul</li>
<li>Kodumaine maksukannete aruanne Itaalia puhul</li>
<li>Musta loendi aruanne Itaalia puhul</li>
<li>Modello770 aruanne Itaalia puhul</li>
<li>Iga-aastane maksusuhtluse aruanne Itaalia puhul</li>
</ul>
</td>
</tr>
<tr>
<td>Läti lokalisatsioon – elektroonilise aruandluse konfiguratsioonid</td>
<td>
<ul>
<li>Kassaorderite kasutuse aruanne (LV)</li>
<li>EL-i käibearuande XML-vorming Läti puhul</li>
<li>EL-i käibearuande paranduste XML-vorming Läti puhul</li>
<li>Intrastati (A) vorming Läti puhul</li>
<li>Intrastati (B) vorming Läti puhul</li>
<li>Varude inventuuri loend Läti puhul</li>
<li>Varude inventuuri väljavõte Läti puhul</li>
<li>Varude liikumine Läti puhul</li>
<li>Sisemise ülekande tarneteade Läti puhul</li>
<li>Varude ümberklassifitseerimise dokument Läti puhul</li>
<li>ISO20022 kreeditiülekande maksevorming Läti puhul</li>
<li>Käibemaksudeklaratsioon Läti puhul</li>
</ul>
</td>
</tr>
<tr>
<td>Leedu lokalisatsioon – elektroonilise aruandluse konfiguratsioonid</td>
<td>
<ul>
<li>EL-i käibaruande XML-vorming Leedu puhul</li>
<li>Intrastati vorming Leedu puhul</li>
<li>Inventuuriväljavõte Leedu puhul</li>
<li>ISO20022 kreeditiülekande maksevorming Leedu puhul</li>
<li>Kliendi-hankija sisemise vastavusseviimise aruanne Leedu puhul</li>
<li>Käibemaksudeklaratsioon Leedu puhul</li>
</ul>
</td>
</tr>
<tr>
<td>Norra lokalisatsioon – elektroonilise aruandluse konfiguratsioonid</td>
<td>
<ul>
<li>Märgukirja vorming Norra puhul</li>
<li>AutoGiro maksuvorming Norra puhul</li>
<li>AvtaleGiro kliendi maksevorming Norra puhul</li>
<li>eFaktura kliendi maksevorming Norra puhul</li>
<li>ISO20022 kreeditiülekande maksevorming Norra puhul</li>
<li>NETS maksevorming Norra puhul</li>
</ul>
</td>
</tr>
<tr>
<td>Poola lokalisatsioon – elektroonilise aruandluse konfiguratsioonid</td>
<td>
<ul>
<li>Intrastati vorming Poola puhul</li>
<li>Laodokumendid Poola puhul</li>
<li>Varude ümberklassifitseerimise dokument Poola puhul</li>
<li>MultiCashi maksevorming Poola puhul</li>
<li>MultiCashi välismaksevorming Poola puhul</li>
<li>Kliendi-hankija saldo kinnitusaruanne Poola puhul</li>
</ul>
</td>
</tr>
<tr>
<td>Saudi-Araabia lokalisatsioon – elektroonilise aruandluse konfiguratsioonid</td>
<td>Bank LC mitmesuguste kulude eraldamise vorming Saudi-Araabia puhul</td>
</tr>
<tr>
<td>Hispaania lokalisatsioon – elektroonilise aruandluse konfiguratsioonid</td>
<td>
<ul>
<li>EL-i käibearuande TXT-vorming Hispaania puhul</li>
<li>Intrastati vorming Hispaania puhul</li>
<li>Projektiarve vorming Hispaania puhul</li>
<li>Müügiarve vorming Hispaania puhul</li>
<li>ISO20022 kreeditiülekande maksevorming Hispaania puhul</li>
<li>ISO20022 otsedeebeti maksevorming Hispaania puhul</li>
<li>Hispaania KM-i registreerimise raamatu vorming</li>
<li>Hispaania KM registreerimisraamatu kokkuvõtte vorming</li>
<li>Deklaratsiooni 347 eksport ASCII-sse Hispaania puhul</li>
<li>Deklaratsiooni 347 aruanne Hispaania puhul</li>
</ul>
</td>
</tr>
<tr>
<td>Rootsi lokalisatsioon – elektroonilise aruandluse konfiguratsioonid</td>
<td>
<ul>
<li>Intrastati vorming Rootsi puhul</li>
<li>Bankgirot Autogiro kliendimakse vorming Rootsi puhul</li>
<li>Bankgiroti hankijamaksete vorming Rootsi puhul</li>
<li>SWIFT hankijamakse vorming Rootsi puhul</li>
<li>SIE ekspordivorming Rootsi</li>
<li>ISO20022 kreeditiülekande maksevorming Rootsi puhul</li>
</ul>
</td>
</tr>
<tr>
<td>Šveitsi lokalisatsioon – elektroonilise aruandluse konfiguratsioonid</td>
<td>
<ul>
<li>DebitDirecti maksevorming Šveitsi puhul</li>
<li>LSV otsedeebeti maksevorming Šveitsi puhul</li>
<li>ISO20022 kreeditiülekande maksevorming Šveitsi puhul</li>
<li>ISO20022 otsedeebeti maksevorming Šveitsi puhul</li>
<li>ESR-i pangaväljavõtte impordivorming Šveitsi puhul</li>
</ul>
</td>
</tr>
<tr>
<td>Saksamaa – hankijamaksete eksportimine DTAZV-vormingus</td>
<td>Saksamaa nõuab DTAZV-vormingut välisriigi vorminguspetsifikatsiooniga, mis kujutab krediidiülekande (hankijamakse) teadet vastavalt spetsifikatsioonile välismaksete puhul Saksamaalt välisriigi pangas asuvale kontole või kodumaisesse panka välisvaluutas.</td>
</tr>
</tbody>
</table>

### <a name="electronic-reporting"></a>Elektrooniline aruandlus

| Mida saate teha | Miks on see oluline |
|-----------------|-----------------------|
| Konfigureerige elektroonilise aruandluse aruandeid, et sisestada andmeid erinevates vormingutes dokumendihalduse mälust loodud elektroonilistesse sõnumitesse. | Elektroonilise aruandluse aruandeid saab sisestada elektroonilistesse teadetesse, mis luuakse dokumendihalduse mälust. Seetõttu saab äridokumendi manuseid lisada elektroonilistele sõnumitele, mis luuakse selle dokumendi jaoks vastavalt juriidilistel nõuetele. Praegu saab need manused MIME-vormingus lisada loodud XML-teatesse. Teise võimalusena saab manused Base64-vormingus lisada loodud binaarsesse teatesse. |
| Saate konfigureerida elektroonilise aruandluse aruandeid, et luua Excelis, Microsoft Wordis või PDF-vormingus elektroonilisi dokumente. | Üks konfiguratsioon lubab elektroonilise aruandluse aruanded, et luua elektroonilisi dokumente kolmes erinevas vormingus: OpenXML-i tööleht (Excel), Word ja XML-vormide andmevorming (XFDF) (PDF). Kasutajad saavad valida vormingu, lisades vormingu malli elektroonilisele aruandlusele Exceli, Wordi või PDF-i dokumendina. |
| Konfigureerige elektroonilise aruandluse aruandeid, et kontrollida lehepiire ja sisestada andmed selliste elektrooniliste dokumentide lehe päisetesse ja jalustesse, mis luuakse OpenXML-i töölehe vormingus. | Elektroonilise aruandluse aruanded saavad sisestada äriandmeid lehepäistesse ja -jalustesse ning samuti kontrollida, kus lehepiir tekib. Seetõttu saavad aruanded toetada loodud elektrooniliste dokumentide lehtede staatilisi ülemisi ja alumisi jaotiseid. Need saavad toetada ka nende dokumentide spetsiifilist saalimist, et need vastaks juriidilistele nõuetele. |
| Konfigureerige elektroonilise aruandluse aruannete sihtkohta, et väljund saadetaks meilina ning et äriandmeid ja elektroonilise aruandluse loogikat (avaldised) saaks kasutada käitusajal kasutatava meiliaadressi määramiseks. | Varasemalt, kui konfigureerisite elektroonilise aruandluse sihtkohta, sai väljundi adressaadi meiliaadressit määratleda käitusajal. Nüüd saate konfigueerida avaldist elektroonilise aruandluse vormingus. Selle avaldise saab seejärel valida sihtkohas meiliaadressi allikana iga vormingu konfiguratsiooni ja iga väljundi komponendi (kaust või fail) jaoks eraldi. Seetõttu, kui elektrooniline aruanne töötab, saab iga loodava faili erinevale adressaadile saata ja meiliaadressi saab määratleda elektroonilise aruandluse loogika- ja äriandmete põhjal. |
| Saate konfigureerida elektroonilise aruandluse aruannete sihtkohta nii, et väljund saadetaks Microsoft SharePointi kausta olemasoleva faili uue nimega faili või uue versioonina ja äriandmeid saaks kasutada Microsoft Power BI raamistikus andmekogumi või aruandena. | Elektroonilise aruandluse aruannete konfigureerimisel saate nüüd hõlpsalt (ilma kodeerimiseta) valmistada ette nõutavad äriandmed, et Power BI raamistik saaks neid kasutada. Kui käivitate need elektroonilise aruandluse aruanded, saate pakkuda Power BI raamistikku sobivate äriandmete ja/või Exceli aruannetega, mis on juba saadaval. Kui ajastate aruande käitused korduvas režiimis, saate luua äriandmete ajastatud lükke rakendusest Dynamics 365 for Operations Power BI-sse, et toetada Power BI põhiste aruannete värskendamisgraafikut. |
| Konfigureerige elektroonilise aruandluse aruandeid, et kasutada osa elektroonilisest dokumendist, mis on juba loodud andmeallikana selle ülejäänud dokumendi loomiseks. | Saate konfigureerida elektroonilise aruandluse aruandeid väljundi tekstivormingus loomiseks, et teha dokumendi rea loendamine. Seda teavet saab seejärel kasutada teistes dokumendi osades, et luua read, mis hõlmavad kokkuvõtlikke üksikasju. Kokkuvõtlikut teavet (kogusummad ja numbrid) saab arvutada ja printida loodavatesse elektroonilistesse dokumentidesse ilma, et oleks vaja andmete täiendavaid teisendusi. Seetõttu täiustab see funktsioon aruande käivitamise jõudlust ja aitab hoida konfigureeritud elektroonilise aruandluse vormingu tulevast hooldust lihtsamana. |
| Konfigureerige elektroonilise aruandluse aruandeid, et määrata tekstivormingus loodavate elektrooniliste dokumentide failinime laiend. | Saate konfigureerida elektroonilise aruandluse aruanded, et luua väljund tekstivormingus nii, et seda saaks salvestada kindla laiendiga failina. Lisaks vaikimisi txt-laiendile saate vormingu spetsifikatsiooni järgi konfigureerida laiendid, nagu .csv ja .prn. |
| Looge uued elektroonilise aruandluse aruanded, mis põhinevad kindlal elektroonilise aruandluse mudeli versioonil. | Varasemalt, kui lõite uue elektroonilise aruandluse vormingu, sai vormingu andmeallika asukohana kasutada ainult valitud elektroonilise aruandluse mudeli kõige värskemat versiooni. Nüüd saate valida valitud elektroonilise aruandluse mudeli mis tahes saadaoleva versiooni. See funktsioon võimaldab teil säilitada käesoleva aasta elektroonilise aruandluse aruanded ja kujundada paralleelselt järgmise aasta jaoks uus elektroonilise aruandluse mudeli versioon. |
| Otsige andmeallikaid ja vorminguid/mudeleid teksti või valitud artefakti alusel ühe klõpsuga. Lahendage proaktiivselt aluse muutmise konfliktid ja lahendage konfliktid konfiguratsioonide vahel. Konfigureerige elektroonilise aruandluse aruanded, et luua mitu valideerimisteadet vigadele, mida avastatakse, kuni aruande käivitamine lõpetatakse. | Mitmed kasutajakogemuse (UX) täiustused elektroonilise aruandluse raamistikus aitavad kasutajatel elektroonilise aruandlusega tõhusamalt ja hõlpsamalt töötada. |
| **Elektroonilise aruandluse** tööruumi kuvamine Power BI aruannetel. | Kasutajad saavad konfigureerida **elektroonilise aruandluse** lehe nii, et see hõlmaks uusi menüü-üksuseid ja reaalajas paane, et käitada Power BI põhiseid aruandeid. |

## <a name="payroll"></a>Palk

<table>
<thead>
<tr>
<th>Mida saate teha</th>
<th>Miks on see oluline</th>
</tr>
</thead>
<tbody>
<tr>
<td>Konfigureerige maksekirjed ja töödelge palgaarvestust, kasutades funktsiooni, mis on samaväärne mooduliga <strong>Palk</strong> rakenduses Microsoft Dynamics AX 2012 R3.</td>
<td>Nüüd saate konfigureerida ja töödelda USA palgaarvestust, kasutades funktsioonikogumit, mis on võrdne funktsioonikogumiga AX 2012 R3-s.
<ul>
<li>Saate konfigureerida tasutsüklid ja tasuperioodid, töötsüklid ja tööperioodid, tulukoodid ja tulukoodi grupid, ajakavad, puhkusetüübid ja soodustuse kogumisplaanid.</li>
<li>Samuti saate seadistada nii eeliste kui ka maksude jaoks kohustuslikud mahaarvamised ja salvestada ametikohtade ja töötajate palgaarvestuse teabe aruandlus- ja analüüsiotstarbel.</li>
<li>Saate seadistada ja hallata mahaarvamisi sissenõudmiste ja maksulõivude ning mis tahes seostatud haldustasude kohta.</li>
</ul>
</td>
</tr>
<tr>
<td>Jälgige ja töödelge makseperioodi protsessi, kasutades uut tööruumi <strong>Palgaarvestuse haldamine</strong>.</td>
<td>Nüüd saate hõlpsalt jälgida palgaarvestuse töötlemist. Lühidalt saavad palgaarvestuse administraatorid näha tulu- ja palgaväljavõtteid, mis nõuavad nende tähelepanu nii, et palgatöötlus on täielik ja täpne. Tööruum <strong>Palgaarvestuse haldamine </strong>võimaldab kasutajatel jälgida ja käitada täielikud protsessid ühest tööjaamast.</td>
</tr>
<tr>
<td>Looge palgatšekkide jaoks positiivsete maksefailid.</td>
<td>On uus laiendus sularaha- ja pangahalduse positiivsele palgafunktsioonile palgamaksete puhul. Eraldi menüü-üksused on lisatud kogu tuumprotsessi jooksul, et lubada palgaarvestusele omast isoleeritud konfiguratsiooni. Funktsionaalsus on identne positiivse makse tuumfunktsiooniga, mis väljastati Microsoft Dynamics AX-i rakenduse versioonis 7.0.1 (mai 2016). Selle laienduse tõttu on palgaarvestuse andmed ülejäänud positiivsetest makseülekannetest täiesti isoleeritud. See isolatsioon aitab tagada, et ainult palgaarvestuse kasutajatel on juurdepääs ja saavad vaadata andmeid, mis on seotud palgaarvestusega.</td>
</tr>
<tr>
<td>Tuluväljavõtte ridade importimine välisest allikast, kasutades uut tuluväljavõtte rea andmete üksust.</td>
<td>Oluline uus andmeüksust võimaldab integratsiooni välise aja ja tulude arvutamise süsteemiga. Andmeüksus impordib tulude väljavõtte read ja teeb kogu sama vaikeloogika, mille kasutaja sisestas otse tuluväljavõttesse. Pärast importimist seostatakse read automaatselt asjakohase tulude väljavõtte dokumendiga. Kui asjakohast tulude väljavõtte dokumenti pole olemas, luuakse dokument automaatselt.</td>
</tr>
</tbody>
</table>

## <a name="planning-and-scheduling"></a>Plaanimine

| Mida saate teha | Miks on see oluline |
|-----------------|-----------------------|
| Määrake müügile ja ostudele tellimuse vaikesätted mis tahes tooteetalonis oleva aktiivse tootedimensiooni põhjal. Seetõttu saate määratleda tellimuse vaikesätted varude arvestusühiku (SKU) või osalise SKU jaoks. | Saate määrata tellimuse vaikesätted, mis rakenduvad tootedimensioonile või tootedimensioonide kombinatsioonile.<p>**Näide**</p><p>Müüte toodet, mille nimi on Polo t-särk. See toode on saadaval kahes värvitoonis: roheline ja sinine. Samuti on see saadaval kahes suuruses: väike ja keskmine. Värv ja suurus on Polo t-särgi aktiivsed tootedimensioonid. Saate blokeerida kõikide roheliste Polo t-särkide ostud olenemata nende suurusest.</p> |

## <a name="product-master-data"></a>Toote koondandmed

<table>
<thead>
<tr>
<th>Mida saate teha</th>
<th>Miks on see oluline</th>
</tr>
</thead>
<tbody>
<tr>
<td>Seadistage kõiki tellimuse vaikesätteid ja tegevuskoha spetsiifilisi tellimuse sätteid samaaegselt ühelt lehelt.</td>
<td>See funktsioon annab kauba sätetest parema ülevaate.</td>
</tr>
<tr>
<td>Looge tootevariandi numbrite jaoks nomenklatuur.</td>
<td>Saate oma tootevariandi numbritesse kaasata elemendid, nagu tootedimensioonid, atribuudid ja märgid. Müügitellimuse või ostutellimuse loomisel saate kiiresti leida konkreetse tootevariandi.</td>
</tr>
<tr>
<td>Otsige tooteid ja tootevariante müügi- ja ostustsenaariumidest.</td>
<td>Müügi- või osturea loomisel otsimisel saate otsida tooteid, kasutades tootedimensioone ja mis tahes tootenumbreid, välja arvatud kaubanduses kasutatavad globaalsed ID-koodid (GTIN) ja vöötkoodid. See otsing on täistekstiline otsing, mis asendab olemasoleva müügi ja ostu otsinguloendis kasutatava otsingu „Algab järgmisega”. See funktsioon võimaldab teil leida toodete grupid, millel on sarnased omadused, või ühe toote, millel on ainulaadsed omadused. Selle funktsiooni sisselülitamiseks valige parameeter <strong>Tooteotsingu lubamine</strong> lehel <strong>Otsinguparameetrid</strong>.</td>
</tr>
<tr>
<td>Määrake tootevariant otse müügi- või ostukande loomisel. Teise võimalusena saate valida dimensioonikombinatsioonide loendist.</td>
<td>See funktsioon on tootlikkuse täiustus.
<p><strong>Näide</strong></p>
<p>Müüte toodet, mille nimi on Polo t-särk. See toode on saadaval kahes värvitoonis: roheline ja sinine. Samuti on see saadaval kahes suuruses: väike ja keskmine. Värv ja suurus on Polo t-särgi aktiivsed tootedimensioonid. Kui sisestate Polo T-särgi müügirea, millel on värv Roheline ja suurus Väike, ei pea te sisestama andmeid väljadele <strong>Kaubakood</strong>, <strong>Värv</strong> ja <strong>Suurus</strong>. Saate luua rea, järgides üht järgmistest etappidest.</p>
<ul>
<li>Väljale <strong>Kaubakood</strong> sisestage tootevariandi number, värvi väärtus või suurus. Otsingus leidke kindel variant, mida soovite müüa, ja looge müügirida.</li>
<li>Väljale <strong>Kaubakood</strong> sisestage kaubakood. Minge mis tahes tootedimensiooni väljale. Otsingus <strong>Tootedimensioon</strong> näete kõiki väljastatud dimensioonikombinatsioone, mis rakenduvad Polo T-särgile. Ühes etapis saate valida tootevariandi, mida soovite müüa.</li>
</ul>
</td>
</tr>
<tr>
<td>Määrake, kas tootenumbrid ilmuvad kandelehel.</td>
<td>Kandelehed, nagu müügi- ja ostutellimused, näitavad ainult välju <strong>Kaubakood</strong> ja <strong>Toote nimi</strong>. Välja <strong>Tootenumber</strong> nägemiseks valige parameeter <strong>Tootenumbrite kuvamine vormidel</strong> jaotises <strong>Tooteteabe halduse parameetrid</strong>.</td>
</tr>
</tbody>
</table>

## <a name="project-management-and-accounting"></a>Projektihaldus ja -arvestus

| Mida saate teha | Miks on see oluline |
|-----------------|-----------------------|
| Kasutage hilist valikut, kui sisestate arvesoovitused partiis. | Projekti raamatupidajad saavad seadistada pakett-töö automaatselt valima sisestamiseks arvesoovitusi, kui need soovitused vastavad kriteeriumidele, mis on määratud pakett-töös. See funktsioon täiustab arve sisestamise automatiseerimist, sest pakett-tööd saab käitada pidevalt ja valib soovitused sisestamiseks automaatselt. |
| Saate luua analüüsi Power BI töölaual. | Projekti ja ressursiga seotud andmete äriteabe (BI) sisu saab Power BI töölaual hõlpsalt luua. |
| Kasutage ostutellimuse ettemakseid ja kaasake need õigesti projekti hindamisprotsessi. | Projekti ostutellimuste puhul tuleb ettemaksed töödelda enne, kui mingi makse saab hankijatele väljastada. Need ettemaksuarved kuvatakse nüüd projekti hindamise/tuvastamise protsessis tüübiga **Fikseeritud hind** projektide puhul |
| Saate kulu- ja tuluhinnangutele ning kaubanõuetele juurde pääseda ja neid hallata otse tööjaotuse struktuuri (WBS) ülesande kaudu. | Saate hallata konkreetse WBS-i ülesande hinnangulisi kulusid ja tulusid ning kaubanõudeid selle ülesande üksikasjade dialoogiboksis WBS-i plaanimise vaates. |
| Valige tasutöölehtedel rahastamise allikas. | Kui projekti leping sisaldab mitut rahastamise allikat, saate tasude sisestamisel valida ühe kindla rahastamise allika. Kui te ei vali konkreetset rahastamise allikat, kasutatakse lepingus määratud rahastamisreegleid tasu eraldamiseks. |
| Avage projekti väljavõtted Excelis. | Uued andmeüksused pearaamatu ja eelarve värskenduste jaoks võimaldavad avada projekti väljavõtte andmeid Excelis ja luua analüüsi, kasutades Exceli funktsionaalsust. |
| Ainult ainult üht konfiguratsioonivõtit, et lubada projektihalduse ja raamatupidamise (PMA) funktsioonid. | Projektiga seotud konfiguratsioonivõtmed on asendatud ühe projekti konfiguratsioonivõtmega, mis lülitab sisse PMA funktsioonid. |

## <a name="retail-and-commerce"></a>Jaemüük ja kaubandus

### <a name="advanced-warehouse-management-in-a-retail-store"></a>Täpsem laohaldus kaupluses

Jaemüüjad saavad oma kauplustes kasutada täpsemat laohalduse (WHS) lahendust ja teha praegusele kassale (POS) selle toetamiseks vajalikud värskendused. Pihuseadme lahenduse protsessid peavad kaupluses töötama nii, nagu need toimivad mis tahes laos. Kõiki praeguseid kaupluse lao protsess ja mis tahes kassa protsesse, mis loovad või värskendavad laokandeid, värskendatakse nii, et need kasutavad WHS-i loaga ladude jaoks spetsiifilisi nõudeid.

| Mida saate teha | Miks on see oluline |
|-----------------|-----------------------|
| Kasutage kassat, et otsida WHS-loaga kauplustes saadaolevaid varusid. | Varude otsimisel peaks protsess toimima samamoodi nagu enne. Otsing peaks näitama saadaolevaid koguseid laotasemel ja ei tohiks arvestada asukohta, varude olekut või litsentsiplaadi dimensioone. |
| Kasutage kassat, et WHS-loaga kauplustes toote sissetulekut üleviimistellimuse jaoks töödelda. | WHS-loaga kaupluse ja kaupade kassas saate üleviimistellimusi vastu võtta. Kasutaja peaks suutma valida vastuvõtmise asukohad ja peaks saama sisestada litsentsiplaadi ID-d, et vastuvõtmise read automaatselt täita. |
| Kasutage kassat, et WHS-loaga kaupluses toote sissetulekut ostutellimuse jaoks töödelda. | WHS-loaga kaupluse ja kaupade kassas saate ostutellimusi vastu võtta. Kasutaja peaks suutma valida vastuvõtmise asukohad ja peaks saama sisestada litsentsiplaadi ID-d, et vastuvõtmise read automaatselt täita. |
| Kasutage kassat, et töödelda toodete saadetist WHS-loaga kauplusest. | WHS-loaga kaupluse ja kaupade kassas saate üleviimisi registreerida. Kasutaja peaks saama valida asukohad, kust lähetada, varude olekut peaks automaatselt luua ja litsentsiplaate peaks ignoreerima. |

### <a name="enable-seamless-omni-channel-commerce"></a>Sujuva ühiskanali kaubanduse lubamine

Sujuv ühiskanali kaubandus viitab haldusele ja tellimuse töötlemisele füüsilistes kauplustes, võrgupoe fassaadides, kõnekeskustes ja mobiilse kaubanduse kogemustes. Selle väljalaske puhul on selles alas tehtud järgmised investeerimised.

- Täiustused avaldamisele e-kaubanduse fassaadide puhul
- Uus tarbijale suunatud mobiilirakendus, mis võimaldab toote tuvastamist, kontode haldamist ja võrgupõhist ostlemist.

| Mida saate teha | Miks on see oluline |
|-----------------|-----------------------|
| Tarbija: tarbijale suunatud rakenduse praegune väljalase lubab järgmised funktsioonid – tooteotsing, kategooria sirvimine, lisamine kärule ja külalise väljaregistreerimine. Jaemüüjad saavad rakendada ka nende ettevõtte kaubamärgi rakendusele ja seejärel pakendada selle Androidi ja iOS-i rakendusepoodidele. | Jaemüüjad saate lihtsalt luua tarbijale suunatud rakendust, mis võimaldab nende klientidel sirvida, otsida tooteid ja lähetada tooteid külalisena nende mobiiliseadmetest. |
| Kliendi soovinimekirjad c-kaubanduse võrgupoe fassaadides | Sõltumatud tarkvarahankijad (ISV-d) saavad kasutada soovinimekirja juhtelementi, et võimaldada kasutajatel luua ja hallata nende veebipoe fassaadis mitut nimekirja ning vaadata/kasutada neid nimekirju kassas. |
| Asünkroonne kliendi loomine e-kaubanduse võrgupoe fassaadides | Sõltumatud tarkvaratarnijad saavad nüüd luua kliendikontod isegi siis, kui Commerce Data Exchange: Real-time Service pole kättesaadav. |
| Avaldage kanali tooted jaemüügiserverist muu osapoole kaupluse fassaadidele. | Jaemüügiserver toetab nüüd teenusest teenusesse autentimist. Sõltumatud tarkvaratarnijad saavad kasutada kanali toote avaldamise eeliseid jaemüügiserverist muu osapoole kaupluse fassaadidele. |

### <a name="extensibility"></a>Laiendatavus

- Kaubanduse käitusaja projektid on nüüd jaemüügi SDK-st pitseeritud.
- Lihtsam juurutamine ja hooldamine komponentiseeritud Microsofti komponendipakettide ja sõltumatu tarkvaratarnija pakettide kaudu kassa, jaemüügiserveri, andmebaaside, makse- ja riistvarajaamade puhul.

| Mida saate teha | Miks on see oluline |
|-----------------|-----------------------|
| CRT/Jaemüügiserver: Jaemüüjad või ISV-d saavad laiendada CRT pikenduskonksude kaudu. Koodisiseseid muudatusi ei toetata enam. | Pideva integratsiooni ja pideva juurutamise lubamiseks tuleb koodisiseseid muudatusi täielikult vältida. Samuti selleks, et toetada lihtsat kiirparanduse teostamist ilma koodi liitmise ja CRT komponentide juurutamiseta. |

### <a name="personalized-product-recommendations"></a>Isikupärastatud tootesoovitused

| Mida saate teha | Miks on see oluline |
|-----------------|-----------------------|
| Vaadake isikupärastatud tootesoovitusi mitmes kassa puutepunktis, et määrata, milline klient võib huvitatud olla, kui arvestada nende ostuajalugu, nende sooviloendis olevaid esemeid ja esemeid, mida teised kliendid on ostnud Internetist ja traditsioonilistest kauplustest. | Suurte kataloogidega jaemüüjate puhul aitavad isikupärastatud soovitused kliendil toodet tuvastada ja kaupluse kaastöötajaid intelligentse kliendisuhete loomisega volitada. Kliendihuvidele ja ostuharjumustele suunatud toodete väljapanekuga saavad tootesoovitused aidata jaemüüjatel müüki suurendada ja kliendilojaalsust parandada. Rakenduses Retail toimivad jaemüügi tootesoovitused kognitiivsete teenuste ja Microsoft Azure’i masinõppe abil. |

### <a name="pos-task-recorder"></a>Kassa ülesande salvestaja

| Mida saate teha | Miks on see oluline |
|-----------------|-----------------------|
| Jaemüüjad saavad kasutada kassa tegevuse salvestajat, et toota koolitusmaterjale, äriprotsesside modelleerija (BPM) diagramme ja luua spikrisisu täiustamaks tootlikkust ja tegemaks paremat rakenduste analüüsi ja kujundust. | Pideva integratsiooni ja pideva juurutamise lubamiseks tuleb sisemuudatusi täielikult vältida. Samuti selleks, et toetada lihtsat kiirparanduse teostamist ilma koodi liitmise ja CRT komponentide juurutamiseta. |
| Reaalajas spikker kassas. | Kassapidaja/juhataja saab hankida kassast äriprotsesside kohta reaalajas abi ilma konteksti muutmata. |

### <a name="store-system-providing-a-seamless-on-premises-store-experience"></a>Kaupluse süsteemi: annab sujuva asutusesisese kaupluse kogemuse

Kaupluse süsteem on juurutamisvalik jaemüüjatele, mis aitab juhtida kaupluse toimingute kogumit, kas asutusesiseses kaupluses, Microsofti avalikus pilves või kliendi enda privaatpilves. Selle versiooni puhul on skoop ainult kauplusesisene. Aeglase ja ebausaldusväärse võrguühenduvusega keskkondade paremaks toetamiseks peame pakkuma jaemüüjatele võimaluse juurutada kanali and Nad saavad seejärel jätkata nende äri tuumstsenaariumide käitamist isegi siis, kui peakontoriga (HQ) puudub ühenduvus. Erinevate andmepuntkide põhjal, mis hõlmas tehnilise töörühma arutelusid, kliendi uuringutulemusi ja konkurendi analüüsi, oleme tuvastanud järgmise lahenduse ulatuse kui ideaalse sobivuse meie sihtklientidega.

- Kaupluse süsteemi jaoks on saadaval iseteeninduse pakett.
- Vaikeinstall on ühe kastiga juurutamine, kuid kohandatud juurutamine on lubatud.
- Lubage lihtne juurutamine/iseteenindus.
- Jaemüügiserver ja kaupluse andmebaas on kaupluses koos Async Clienti teenusega.
- Jaemüügiserver suhtleb kaupluses otse rakendusobjekti serveriga (AOS) kauplusesüsteemi HQ-s.
- Toetage terminalivahelisi stsenaariumeid, kus puudub HQ ühenduvus.
- Retail Modern POS ja pilvekassa suhtlevad kaupluses alati jaemüügiserveriga.
- Toetage Retail Modern POS-i ja pilvekassat, kus puudub HQ ühenduvus.
- Toetage Retail Modern POS-i spetsiifilist võrguühenduseta andmebaasi (isoleeritud igale Retail Modern POS eksemplarile), kus puudub HQ ühenduvus.
- Autentimise põhineb kauplusesüsteemi puhul ainult teenuselt teenusele.
- Reaalajas teenuse kõnesid ei toetata, kui puudub Interneti-ühendus.
- Retail Modern POS-i otsest andmebaasiühendust kanali andmebaasiga ei toetata.
- Lubage telemeetria/jälgimine.

| Mida saate teha | Miks on see oluline |
|-----------------|-----------------------|
| Jaemüüja laadib kauplusesüsteemi iseteeninduse installifaili alla kanali andmebaasi lehelt Dynamics AX HQ-sse ja laadib alla konfiguratsioonifaili. | Jaemüüja saab iseteeninduse paketi sujuvalt alla laadida. |
| Jaemüüja installib kauplusesüsteemi, kasutades iseteeninduse installerit. | Jaemüüja saab installida kauplusesüsteemi, kasutades iseteeninduse paketti. |
| IT-juht konfigureerib rakenduses Dynamics 365 for Operations kauplusesüsteemi (kanali andmebaas, kanali profiil, kauplus ja juurutatav pakett). | IT-juht saab konfigureerida kauplusesüsteemi hõlpsalt ja efektiivselt. |
| Jaemüüja kasutab Retail Modern POS-i asutusesiseses kaupluses ja saab ühenduvuse korral teha reaalajas toiminguid, nagu kinkekaartide väljastamine. | Jaemüüja saab ühenduse olemasolu korral teha kauplusesüsteemist reaalajas toiminguid. |
| Jaemüüja saab sünkroonida andmeid asutusesisesest kauplusesüsteemist HQ-sse alati, kui on ühendus. | Jaemüüja saab ühenduse olemasolu korral sünkroonida kauplusesüsteemi ja sellest välja. |
| Jaemüüjal võib olla turvaline kommunikatsioon asutusesisese kauplusesüsteemi ja HQ vahel. | Jaemüüja saab ühenduse olemasolu korral kommunikeerida turvaliselt kauplusesüsteemist. |
| IT-juht ja Microsoft Operations saavad jälgida ja aru anda asutusesiseses kauplusesüsteemis (diagnostika ja aruandluse muudatused). | IT-juht ja Microsoft Operations saavad jälgida kauplusesüsteemi turvaliselt ja teha tõhusalt tõrkeotsingut. |

### <a name="universal-windows-platform-app-for-retail-modern-pos"></a>Universaalne Windowsi platvormi rakendus Retail Modern POS-ile

Praegu on Retail Modern POS saadaval ainult Windows 8.1 rakendusena laua- ja tahvelarvutitele ning pilvekassana laua- ja tahvelarvuti brauseritele. Selles väljalaskes teisendatakse tänapäevane jaemüügikassa rakenduseks Universal Windows Platform (UWP). See muudatus võimaldab Retail Modern POS-i käitada mis tahes Windows 10 seadmes (laua- või tahvelarvuti või telefon) ja Continuumi toega seadmete puhul isegi vaateid vahetada.

| Mida saate teha | Miks on see oluline |
|-----------------|-----------------------|
| Lubage olulised kassa funktsioonid väikese vormi teguriga seadmete jaoks. | Retail POS-i funktsioonid on saadaval telefonidele ja teistele väikese vormi teguriga seadmetele, mis kasutavad operatsioonisüsteemi Windows 10. |

## <a name="supply-chain-management"></a>Hankeahela haldamine

### <a name="consignment-inventory"></a>Veose varud

| Mida saate teha | Miks on see oluline |
|-----------------|-----------------------|
| Hankijana saate salvestada kliendi laos toormaterjali. Kliendina saate tegeliku ostu edasi lükata, kuni toormaterjalid on tootmiseks vajalikud. | Toormaterjalide varude hoidmine võib hõlmata tõsiseid kulusid. Veose varude kasutamisega saab hankija hoida toormaterjale kliendi laos. Klient saab seejärel tegeliku ostu edasi lükata, kuni toormaterjalid on tootmiseks vajalikud. Toormaterjalid tellitakse ja võetakse vastu, kasutades veose täiendamise tellimust. See täiendamise tellimus salvestab füüsilised kanded, kuid ei mõjuta pearaamatut. Kliendile ja hankijale kuuluvate laokaupade vahel eristamiseks saate kasutada omaniku varude dimensiooni. Varude omanikuvahetust käsitleb töölehe töötlemine, mis käsitleb toormaterjalide omandiõiguse üleviimist hankijale kuuluvatelt varudelt kliendile kuuluvate varudeni. See protsess käivitab ostutellimuse ja toote sissetuleku loomise.<blockquote>[!NOTE] See funktsioon on piiratud tootmiseks mõeldud toormaterjalide sissetuleva veosega. See pole integreeritud laohalduse (WHS) ja transpordihaldusega (TMS).</blockquote> |
| Hankijana saate teavet kliendile üleviidavate veose varude summa kohta. | Kliendile arve esitamiseks nõuab hankija teavet veose varudest ostetud toormaterjalide kohta ja ostukuupäeva. Hankija saab ka jälgida vaba kaubavaru kliendi tegevuskohas, kasutades hankija koostööliidest. |
| Liigutage hankijale kuuluvaid varusid, kasutades üleviimistöölehte. | Hankijale kuuluvate varude füüsilise asukoha jälgimiseks peate salvestama asukoha süsteemis. Üleviimistöölehe kasutamisel saate kirjendada varude füüsilise liikumise, näiteks liikumise lao ühest asukohast teise asukohta selles laos. |
| Reguleerige hankijale kuuluvaid varusid, kasutades inventuuritöölehte. | On oluline hoida süsteemi vaba kaubavaru sünkroonis tegelike füüsiliste varudega. Hankijale kuuluvaid varusid saab reguleerida sisse ja välja, kasutades inventuuriprotsesse, nagu koguse reguleerimine ja inventuuritöölehe protsessid. |
| Lugege lisateavet rakenduses Dynamics 365 for Operations saadetise seadistamise kohta | Veoseprotsesside toe kohta lisateabe saamiseks vaadake teemasid [Saadetis](../../../supply-chain/inventory/consignment.md), [Veose seadistamine](../../../supply-chain/inventory/set-up-consignment.md), [Veose täiendustellimuse loomine (ülesande juhend)](../../../supply-chain/inventory/tasks/create-consignment-replenishment-order.md) ja [Kaubavaru omandiõiguse muutmine tootmise nõudluse põhjal (ülesande juhend)](../../../supply-chain/inventory/tasks/change-ownership-consignment.md). |

### <a name="vendor-collaboration-previously-known-as-the-vendor-portal"></a>Hankija koostöö (varasema nimega hankijaportaal)

| Mida saate teha | Miks on see oluline |
|-----------------|-----------------------|
| Lubage hankijatel vastata igale ostutellimuse reale ja soovitada muudatusi. | Mõnel juhul soovivad hankijad aktsepteerida mõnesid ostutellimuse ridu, kuid lükata teisi tagasi. Hankijad saavad nüüd ostutellimuse ridu individuaalselt hallata. Iga rida saab tagasi lükata, aktsepteerida või aktsepteerida muudatustega. Näiteks saavad hankijad muuta tarnekuupäeva, tükeldada tarnet ja kogust või soovitada alternatiivset kaupa. |
| Lubage hankijate hallata kontaktisiku teavet. | Hankijad saavad säilitada nende ettevõtte kontaktisiku teabe. See teave sisaldab nimesid, meiliaadresse ja telefoninumbreid. Juurdepääs sellele funktsioonile antakse integreeritud turberolli kaudu. |
| Andke ühiskasutusse dokumente, mis on seotud hankijatega tehtud ostutellimustega. | Kui peate andma dokumendi hankijaga ühiskasutusse, nt dokument nõuete kohta, on mugav linkida dokument asjakohase ostutellimusega. Hankija saab seejärel anda märkuseid ja manuseid kliendiga ühiskasutusse, linkides dokumendi tema vastusega ostutellimusele. Dokumendihaldus on aluseks olev tugiraamistik ja ainult märkuseid ja manuseid, mis on klassifitseeritud kui „väline”, saab hankijatega ühiskasutusse anda. |
| Valmistage ette uusi hankija kasutajaid. | Kui hankijad kasutavad koostööliidest, siis on neil tõrgeteta võimalus nõuda uusi kasutajakontosid, kui uued kontaktid nõuavad juurdepääsu hankija koostööle. Hankeprofessionaalid saavad esitada nõude kontaktisiku kasutajakontole hankija organisatsioonis. Hankija kontaktisik, kes on juba hankija koostöö kasutaja, saab samuti esitada seda tüüpi taotlust. See taotlus loob lõpuks rakenduses Dynamics 365 for Operations uue kasutaja, kellel on hankijakohased turberollid. See hõlbustab ka taotluse esitamist Microsoft Azure B2B portaalile kasutajale uue Azure Active Directory (Azure AD) kasutajakonto andmise kohta. Hankijad saavad ka nõuda, et konkreetsed hankija-kasutajakontod inaktiveeritaks või et turberolle modifitseeritaks. |
| Lugege lisateavet hankija koostöö toe kohta rakenduses Dynamics 365 for Operations. | Hankija koostöö kohta lisateabe saamiseks vaadake [Hankija koostöö väliste hankijatega](../../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md), [Hankija koostöö klientidega](../../../supply-chain/procurement/vendor-collaboration-work-customers-dynamics-365-operations.md), [Hankija koostöö kasutajate haldamine](../../../supply-chain/procurement/manage-vendor-collaboration-users.md), [Hankija koostöö seadistamine ja haldamine](../../../supply-chain/procurement/set-up-maintain-vendor-collaboration.md) ja [Hankija koostöö arve tööruum](../../../finance/accounts-payable/vendor-portal-invoicing-workspace.md). |

### <a name="intercompany-order-processing"></a>Kontsernisisene tellimuse töötlemine

<table>
<thead>
<tr>
<th>Mida saate teha</th>
<th>Miks on see oluline</th>
</tr>
</thead>
<tbody>
<tr>
<td>Määratlege otse müügitellimuse ridadel, kust tuleks nõudlus hankida ja kuidas seda tuleks hankida.
<p><strong>Näide</strong></p>
<p>Looge müügitellimuse rida ja määrake tarnetüübiks otsetarne. Esmane hankija lisatakse müügitellimuse reale hankimispunktina.</p>
</td>
<td>Tellimuse võtmise voogu on märkimisväärselt täiustatud. Nüüd saate määratleda otse müügitellimuse ridadel, kust tuleks nõudlus hankida ja kuidas seda tuleks hankida. Te ei pea enam ootama, kuni kõik read on lisatud müügitellimusele. Uued valikud müügitellimuse ridadel võimaldavad hankija määramisel määrata tarnetüübi. Hankija müügitellimuse ridadega seostamisel luuakse hankijalt tarnimise jaoks tellimuseahelad.
<ul>
<li>Hankija võib olla kontsernisisene hankija, kes kasutab sisemist ostutellimust ja müügitellimust või see võib olla väline hankija, kes kasutab välise ostutellimust.</li>
<li>Tarnetüüp võib olla <strong>Otsetarne</strong> või <strong>Ladu</strong>. Tarnetüüp <strong>Ladu</strong> näitab, et hankija peaks tarnima kohalikesse varudesse enne, kui lähetab kliendile.</li>
</ul>
</td>
</tr>
<tr>
<td>Looge tellimuse lubaduse otse müügitellimuse ridadelt.
<p><strong>Näide</strong></p>
<p>Looge müügitellimuse rida, mis hangitakse kontsernisiseselt hankijalt. Lahkuge realt. Tarnekuupäevad arvutatakse hankeettevõttes kättesaadavuse järgi.</p>
</td>
<td>Sellise müügitellimuse loomisel, mis kasutab uut hanketeavet, arvutatakse tarnekuupäevad juhtelemendi <strong>Tarnekuupäev</strong> järgi. Näiteks kontsernisisese hankija valimisel arvutatakse hankeettevõtte kättesaadavus. Sellisel juhul luuakse tellimuse ahelad koos müügitellimuse ridadega. See funktsioon aitab tagada, et tarnekuupäevad muutuvad hankeettevõttes nähtavaks, et lubamiseks saadaval (ATP) profiilid saaksid käsitleda plaanitud nõudmisi otse müügitellimuste loomise ajal.</td>
</tr>
<tr>
<td>Vaadake toote kättesaadavus üle kõikides hankeasukohtades ja valige parim hankevõimalus.</td>
<td>Leht <strong>Tarne alternatiivid</strong> on ümber kujundatud ja pakub nüüd väärtuslikku teavet kõikide heaks kiidetud sisemiste ja väliste hankijate kohta. See teave hõlmab hankevalikuid hankija hankimise jaoks. Tarneviisi valimisel arvutab süsteem teostatavad tarnekuupäevad. Saate sujuvalt valida kliendi jaoks parima valiku ja rakendada selle valiku igale müügitellimuse reale.</td>
</tr>
</tbody>
</table>

### <a name="warehouse-enhancements-for-high-volume-distribution-centers"></a>Laotäiustused suuremahuliste jaotuskeskuste jaoks

| Mida saate teha | Miks on see oluline |
|-----------------|-----------------------|
| Looge töö pärast kaupade pakkimist pakkejaamas. | See funktsioon on kasulik, kui pärast käsitsi pakketööd on täiendavad protsessid (nagu kaubaaluste loomine, kvaliteedikontoll, saadetiste konsolideerimine või muudatused laadimisõlmedele). Uus töö tüüp **Pakitud konteineri komplekteerimine** võimaldab teil modelleerida neid ülesandeid, kasutades eraldi tööridu. Nüüd saate modelleerida pakkejaamu, et luua pakkimisjärgne töö. Seda tööd saab kasutada pakitud varude liikumise korraldamiseks. |
| Grupeerige konterinereid pakkimisjaamas. | See funktsioon võimaldab mitut pakendit pakkimisjaamas üheks konteineriks või litsentsiplaadiks grupeerida. Näiteks saab e-kaubanduse/hulgimüügi operaatori grupeerida 100 eraldi pakitud paketti ühte konteinerisse (nagu kaubaalus või puur). Seda konteinerit saab seejärel teisaldada, ettevalmistada või laadida ühe töö juhise kaudu, mille töötaja loob, skannides üksiku vöötkoodi (litsentsiplaat) grupeeritud konteineri jaoks. See funktsioon minimeerib töökandeid paljude väiksemate pakitud konteinerite liigutamiseks. Lisateabe saamiseks vaadake teemat [Mobiilse seadme menüüelemendi loomine litsentsiplaadi konsolideerimiseks (tegevuse juhis)](../../../supply-chain/warehousing/tasks/create-mobile-device-license-plate-consolidation.md). |
| Looge pakitud konteinerite jaoks vabastuspoliitika. | Konteineri vabastamisega käivitatavat tööd saab luua automaatselt või manuaalselt. Kui see on automaatne, luuakse töö konteineri sulgemisel, kasutades asukoha direktiivi ja töömalli raamistikku. Kui vabastamine on manuaalne, saab pakkija otsustada, kas töö tuleb luua üksiku konteineri või konteinerite grupi jaoks. See funktsioon vähendab ohtu, et suletud konteinerid komplekteeritakse ja liigutatakse enne, kui need on valmis pakkimisjaama liigutamiseks. Samuti võimaldab ka mittesüsteemiga juhitavat grupeeritud vabastamist. |
| Lühi-komplekteerimise ümberjaotamine | Lühi-komplekteerimise protsesside jaoks on lisatud tugi, et aidata seostada, kes ei saa kaupu komplekteerida ja soovib täita tellimuse siis, kui nõutav kaup on saadaval teises asukohas. Saate kasutada automaatset ümberjaotamise protsessi, mis kasutab kaupade toomiseks samu asukohakorraldusi, kui need on teises asukohas olemas. Alternatiivselt, kui kasutatakse käsitsi ümberjaotamist, näitab mobiiliseade asukohtade loendit koos saadaoleva kogusega. Laotöötaja saab seejärel valida, millise asukoha varusid kasutada. Need kaks meetodit saab määrata individuaalselt või kombineerituna üksiku käsuna laotöötaja menüüs. Käsitsi ümberjaotamiste kasutamisel saab laotöötaja komplekteerida lühikeselt komplekteeritud kauba koguse mitmest asukohast. Lisateabe saamiseks vaadake teemat [Kauba lühikese valiku ümberjaotamise seadistamine (ülesande juhend)](../../../supply-chain/warehousing/tasks/set-up-short-picking-item-reallocation.md). |
| Liigutage varusid, millega on seostatud töö. | Nüüd saate liigutada varusid, millega on seostatud töö. See funktsioon võib olla kasulik näiteks siis, kui töötaja soovib tühjendada osa saabumisala ruumist ja liigutada registreeritud kaubaaluseid, mis ootavad teise sissetulekukohta kõrvalepanemist. Ala tühjendatakse ja see saab vastu võtta täiendavaid kaupade koormaid ja liigutatud varusid värskendatakse uue kõrvalepaneku teabega. Seda funktsiooni saab kasutada ka komplekteerimise asukohtades ruumi vabastamiseks, teisaldades varud, millega on seostatud tööd, ja vabastades ruumi täiendamiseks. Saate seda kasutada ka koormate liigutamiseks ühest vaheasukohast teise ilma kaotamata loodud laadimistööd. Sellisel viisil aitab see funktsioon optimeerida aega, mis on vajalik veokite laadimiseks nende saabumisel. Saate teisaldada varusid, mis on reserveeritud müügitellimuste jaoks, üle viia tellimuse probleeme, üle viia tellimuse sissetulekuid ja ostutellimusi. Liikumist takistatakse, kui see põhjustab ridade tükeldamist. Näiteks kui teil on töö rida kauba 100 tükile, ei saa te liigutada teise asukohta ainult 30 selle kauba tükki. |
| Ühendage litsentsiplaadid, millega seostatud tööd. | Saate ühendada litsentsiplaadid, millega seostatud väljaminevat tööd. Näiteks kui komplekteerimine on jagatud töö mitmeks osaks, saab see olla kasulik, et võimaldada litsentsiplaatide ühendamist pärast nende tarnimist vaheasukohta. Litsentsiplaate saab konsolideerida ainult siis, kui need on samas asukohas, on sama koorma liikmed ja neil on sama saadetise teave. |
| Külmutage komplekteerimistöö, mis on seostatud rea tasemel täiendamisega. | Nüüd saate külmutada töö päise taseme asemel rea tasemel, et töötajad saaks täita komplekteerimisridu, mis ei ole külmutatud nõudluse täiendamisega. Seetõttu saavad hulgimüüja, kellel on suured müügitellimused, või jaemüüja, kellel on suured müügitellimused või täiendamise üleviimistellimused, lubada komplekteerimistöö käivitamise kõikidel ridadel, mis ei allu täiendamise tööle. Komplekteerimis- ja täiendamistöö saab seejärel paraleelselt lõpule viia. Seda funktsiooni saab konfigureerida nii, et saate valida päise- või reatasemel külmutamise. Samuti saate kasutada mõlemat meetodit ja luua iga meetodi jaoks malli. Päise/rea konfiguratsioon seadistatakse töömallides, kuid saate seda muuta otse loodud tööl. |
| Tühistage töö, kasutades mobiilseadet. | Nüüd saate töö mobiiliseadme abil tühistada koos nõudluse täiendamisega või ilma selleta. Varasemalt pidite kasutama rikast klienti. Selle funktsiooni lubamiseks looge mobiiliseadme menüü-üksus, mille režiim on seatud valikule **Kaudne** ja tegevuskood seatud valikule **Tühista töö**. |

### <a name="warehouse-operation-enhancements"></a>Laotoimingu täiustused

| Mida saate teha | Miks on see oluline |
|-----------------|-----------------------|
| Modelleerige erinevad konteineri tüübid. | Võite laos kasutada erinevaid konteineri tüüpe, et optimeerida talletamist ja muudel põhjustel. Uuel konteineri tüübi üksusel on konteineri tüüpide füüsilised omadused. Nüüd saate seostada litsentsiplaadid konkreetse konteineri tüübiga ja kasutada asukoha ladustamispiiranguid. Näiteks saate kasutada seda funktsiooni kontrollimaks, mitu kaubaalust (või muud tüüpi konteinereid) lubate kindlas asukohas. Konteineritüübid on lisatud ka üksuse seeriagruppidele, et vastuvõtmisprotsessi jaoks konteineri vaiketüübid lisada. Konteineritüüpe saab kasutada sissetulevate ja väljaminevate asukohakorraldustega. Neid saab kasutada ka vaba kaubavaru vaates, et aidata teil määrata, kuidas paljud konteineri tüübid on praegu talletatud laoseisus. Lisateabe jaoks vaadake atjaveebipostitus [Konteineritüüpidega seotud litsentsiplaatide kasutamine laohalduse protsesside jaokss](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/06/20/use-of-license-plates-associated-with-a-container-type-to-drive-warehouse-management-processes/). Kuigi see ajaveebipostitus kirjeldab värskendust rakendusele Microsoft Dynamics AX 2012, on sama tugi lisatud nüüd rakendusele Dynamics 365 for Operations. |
| Pöörake saadetised ümber. | Laos peate saama käsitleda hilinenud muudatusi. Näiteks mõned kaubad võivad olla kahjustatud, nii et neid ei saa lähetada. Teise võimalusena võib klient võib teha hilinenud nõude tellimuse tühistamiseks või muutmiseks. Dynamics 365 for Operations võimaldab nüüd saadetise tagasi pöörata. Seetõttu saate saatelehe tühistada, et saaksite seda hiljem õigete kogustega värskendada. Sarnaselt saate sissetulevas voos tühistada toote sissetulekud nii, et saab luua värskendatud versiooni. |
| Kasutage kaubaaluseid, millel on sedatud kaubad. | Nüüd saate „segatud” kaubaaluse vastu võtta ja registreerida. Segatud kaubaalus sisaldab erinevaid kaupu, mis on koondatud ühele kaubaalusele ühe või mitme ostutellimuse või rea jaoks. Kõik registreerimised saab kokku võtta ühte sihtlitsentsiplaati. See protsess lubatakse lao mobiiliseadme kaudu. Näiteks kui segatud kaupade kaubaalused saabuvad lattu, tuvastab vastuvõtuametnik kaubaalusel olevad kaubad ja kogused enne, kui kaubaalus liigutatakse sihtotstarbelisse kõrvalepaneku asukohtadesse. Kõrvalepaneku asukohad tuvastatakse töömallide ja asukohakorraldustega. Kui kõrvalepaneku asukohad jaotatakse mitmele kaubale, millel on fikseeritud asukohad, siis loob see funktsioon nii palju asetamise tööridu kui on erinevaid kaupu segatud kaubaalusel. See funktsioon muudab vastuvõetud segatud kaubaaluste registreerimise ja kõrvalepanemise kiiremaks ja paindlikumaks. Lisateabe saamiseks vaadake ajaveebipostitust [Mitmesuguste lähtedokumendi ridadega aluse vastuvõtmine ja registreerimine, kasutades 1 litsentsiplaati](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/13/receive-and-register-a-pallet-with-mixed-source-document-lines-using-1-license-plate-purchase-order-matching/) ja teavet segatud kaubaaluse toe kohta [meie hiljutise kumulatiivse värskenduse teatest](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/06/30/whats-new-in-cu11-for-wms-and-tms/). Kuigi see ajaveebipostitus kirjeldab värskendust rakendusele AX 2012, on sama tugi lisatud nüüd rakendusele Dynamics 365 for Operations. |

### <a name="minor-feature-enhancements-in-supply-chain-management"></a>Väikesed funktsioonitäiustused tarneahela halduses

<table>
<thead>
<tr>
<th>Mida saate teha</th>
<th>Miks on see oluline</th>
</tr>
</thead>
<tbody>
<tr>
<td>Kasutage andmete importimiseks ja eksportimiseks uusi andmeüksuseid.</td>
<td>Saate importida ja eksportida andmeid, kasutades neid andmeüksuseid:
<ul>
<li>Veoarve</li>
<li>Laoseisu koondamine lao ja varude oleku järgi</li>
<li>Varude kulud</li>
<li>Pakkumine</li>
</ul>
</td>
</tr>
<tr>
<td>Kasutage täiustatud Gantti juhtelementi interaktiivsete plaanimise stsenaariumide arendamiseks.</td>
<td>Täiustatud Gantti juhtelement võimaldab teil arendada uusi interaktiivseid plaanimise stsenaariume ja tarnida täiustatud API-sid, mida saab kasutada tegevuste ilme kohandamiseks. Siin on mõned uued API-d:
<ul>
<li>Tegevuste vertikaalne pukseerimine</li>
<li>Tegevuste lisamine/eemaldamine</li>
<li>Reserveeritud peroodide eelvaatamine kokkuvõtteribal</li>
<li>Tegevuse piiride värvi ja laadi muutmine</li>
<li>Teksti värvi, laadi ja tausta muutmine ruudustikus</li>
</ul>
</td>
</tr>
<tr>
<td>Käsitlege materjalide ja ressursside plaanimist paremini.</td>
<td>Materjalide ja ressursside plaanimisele on tehtud mõned täiustused.
<ul>
<li>Väljamineku ohutusvaru käsitletakse nüüd siis, kui kaup on laos.</li>
<li>Kirjutage tarnekuupäev üle plaanitud tellimuste kinnitamisel.</li>
<li>Prioritiseerige tellimuste täitmist puhvervaru üle.</li>
<li>Vältige plaanitud tellimuste plaanimist minevikus.</li>
</ul>
</td>
</tr>
<tr>
<td>Saate aru anda tootmise tegelikust tarbimisest ja vaadata varude olekut.</td>
<td>Saate vaadata tootmise tegelikku tarbimist. Täiendavalt võimaldab uus valikule <strong>Liikumine</strong> menüü-üksuses <strong>Töö loomine</strong> lisatud märkeruut<strong>Kuva varude olek</strong> vaadata teil varude olekut.</td>
</tr>
<tr>
<td>Arvutage mahuline kaal, kui teie kättetoimetaja määrad põhinevad mahulisel kaalul.</td>
<td>On lisatud uus mahulisel kaalul põhinev TMS-i määra mootor, et saaksite arvutada mahulist kaalu.</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Lisaressursid

[Mis on uut või muudetud Finance and Operationsi avalehel](whats-new-changed.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]