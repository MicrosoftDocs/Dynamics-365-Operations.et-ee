---
title: Mobiilsete seadmete seadistamine laotöö jaoks
description: Teemas kirjeldatakse, kuidas konfigureerida menüü üksusi, mida laotöötajad kasutavad töö tegemiseks mobiilses seadmes.
author: MarkusFogelberg
manager: tfehr
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFSysDirSort, WHSWorkUserDisplaySettings
audience: Application User
ms.reviewer: kamaybac
ms.custom: 29941
ms.assetid: 6dff6313-dc6e-4f06-9c0c-dab24eefe4da
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f710403baef02173c39016406a19c82f604cc99d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996375"
---
# <a name="set-up-mobile-devices-for-warehouse-work"></a>Mobiilsete seadmete seadistamine laotöö jaoks

[!include [banner](../includes/banner.md)]

Teemas kirjeldatakse, kuidas konfigureerida menüü üksusi, mida laotöötajad kasutavad töö tegemiseks mobiilses seadmes.

> [!NOTE]
> See teema kehtib laohalduse funktsioonidele. See ei kehti funktsioonidele moodulis Varude haldus. Lao mobiilse seadme menüüdes kuvatavaid menüüelemente konfigureeritakse lehel **Mobiilse seadme menüüelemendid**. Kuna menüüelemente saab panna erinevatesse menüüdesse, on menüüstruktuure lihtne konfigureerida, nii et kindlatele kasutajatele kuvatakse ainult teatud tüüpi töid. Saate menüüelemente konfigureerida järgmiste ülesannete täitmiseks.

- Päringu töötlemine või tegevuse teostamine, nagu sildi printimine, identifitseerimisnumbrite loomine, tootmistellimuse käivitamine või kiiresti teabe vaatamine mõnes asukohas olevate kaupade kohta.
- Looge töö, mis tehakse läbi teise protsessi. Näiteks võib ostutellimuse jaoks kaupa vastuvõtmine luua teisele töötajale paigutamistöö.
- Mõne muu protsessiga (olemasoleva tööga) loodud töö tegemine, nt paigutamistöö, mis loodi ostutellimuse jaoks kauba vastuvõtmisel.

Tegevuse või päringu jaoks menüüelemendi loomiseks valige välja **Režiim** sätteks **Kaudne**. Seejärel muutub kättesaadavaks loend **Tegevuskoodide suvandid** nii et saate valida selle päringu või tegevuse tüübi, mille jaoks on menüüelement mõeldud. Laotöö jaoks menüüelemendi loomiseks valige välja **Režiim** sätteks **Töö**. Seejärel muutub kättesaadavaks loend **Töö loomise protsess**. Olemasoleva laotöö töötlemise jaoks menüüelemendi loomiseks valige välja **Režiim** sätteks **Töö** ja seejärel suvandi **Kasuta olemasolevat tööd** sätteks **Jah**. 

> [!NOTE]
> Täiendavad väljad võivad menüüelementide jaoks olla saadaval, sõltuvalt menüüelemendi jaoks valitud režiimist ja sellest, kas menüüelementi kasutatakse olemasoleva töö tegemiseks. Teavet lisaväljade valikute kohta vaadake selles teemas allpool olevast teemast „Menüüelementide lisavalikud”.

## <a name="configure-menu-items-for-activities-and-inquiries"></a>Menüüelemendi konfigureerimine tegevuste ja päringute jaoks
Kui menüüelemendi välja **Režiim** sätteks on valitud **Kaudne**, saate luua menüüelemendi tegema üldist tegevust või päringut, mis ei loo tööd. Niisugused tegevused on näiteks litsentsiplaadi siltide uuesti printimine ja päringute esitamine asukoha kaupade kohta. Järgmises tabelis on toodud saadaolevad suvandid.

| Suvand | Kirjeldus |
|---|---|
| Puudub | See vaikeväärtus ei luba tegevust või päringut. |
| Teave | Vaadake süsteemi kohta teavet, nt versiooninumbrit, lao ID-d ja praegu sisse logitud töötajat. |
| Vaheta ladu | Muutke ladu, kuhu töötaja on sisse logitud. |
| Asukoha päring | Vaadake teavet asukoha kõikide kaupade ja koguste kohta. |
| Numbrimärgi päring | Vaadake litsentsiplaadil olevate kaupade kogust ja litsentsiplaadi asukohta. |
| Käivita tootmistellimus | Alustage tootmistellimust. |
| Tootmise praak | Sisestage praagi kogus, mis loodi tootmisel iga koosluserea kohta. |
| Tootmise viimane kaubaalus | Näidake, et viimane kaubaalus on toodetud tootmistellimuse jaoks ja tootmistellimuse olek tuleb värskendada sättele **Lõpetatuna kinnitatud**. Tootmise käigus tarbimata jäänud toormaterjalide olek muudetakse olekust **Komplekteeritud** tagasi olekusse **Tellimusel** ja kaubad saab varudesse tagastada. |
| Kauba päring | Skannige kaup, et määrata, kus laos see on. Päring annab vastuseks skannitud kauba kõik asukohad ja kogused. |
| Prindi silt uuesti | Printige litsentsiplaadi silt uuesti. |
| Litsentsiplaadi koostamine | Looge emalitsentsiplaat, ühendades mitu sama asukoha litsentsiplaati. See valik on kasulik, kui liigutate mitut litsentsiplaati samal ajal. Kui emalitsentsiplaat on liigutatud, peate igalt litsentsiplaadilt kaupade valimiseks litsentsiplaadi struktuuri lahti võtma. <p></p>**Näpunäide.** Emalitsentsiplaadi liigutamiseks peate kasutama mobiilset seadet, mis on konfigureeritud looma tööd liikumiste jaoks. |
| Litsentsiplaadi vahe | Võtke lahti litsentsiplaadi struktuur, et saaksite valida struktuuris olnud litsentsiplaatidelt kaupu. |
| Juhi sisseregistreerimine | Kui kasutate funktsiooni Transpordihaldus, registreerige autojuhi saabumine, skannides väljamineva koormuse ID, kohtumise ID või saadetise ID. Selle valiku puhul peab koorem olema määratud kohtumisele ja koorma olek olema **Laaditud**. |
| Juhi väljaregistreerimine | Registreerige, et autojuht on kohtumise lõpule viinud. |
| Numbriseeria vahemälu tühjendamine | Kustutage numbriseeria vahemälust numbriseeria. Seda tegevust teeb tavaliselt süsteemiadministraator vahemälu probleemide lahendamiseks, kui kasutatakse mobiilseid seadmeid. |
| Partii likvideerimise muutmine | Lubage töötajal määrata kaubale ja partiile partii likvideerimiskood. See valik värskendab partii jaoks määratud likvideerimiskoodi. |
| Kuva avatud tööloend | Saate kuvada konkreetsele kasutajale saadaolevate tööde loendi. Seejärel saab kasutaja valida tegemiseks töö ja ta suunatakse sellele. Seda loendit tuleb vaadata tahvelseadmetel, mille ekraani suurus on vähemalt 7 tolli. Selle suvandi valimisel muutuvad kättesaadavaks menüüelemendid **Päringu redigeerimine** ja **Väljaloend**. Lehel **Päringu redigeerimine** saate seadistada loendis kuvatava töö kriteeriumid. Lehel **Väljaloend** saate valida tööde loendis kuvatavad väljad. Näiteks saate vähendada kuvatavate väljade arvu, et kasutaja saaks sobiva tööüksuse kiiremini valida. Kiirkaardi **Üldine** väljal **Kirjeid leheküljel** saate valida ka igal leheküljel kuvatavate töökirjete arvu. Kui suvand **Luba kasutajatel filtreerida töid kande tüübi järgi** on märgitud, lisandub tööde loendisse juhtelement **Filtreeri töö**, mis võimaldab kasutajal kande tüübi järgi filtreerida. Tööde loendis näeb kasutaja ainult neid töid, millele tal on juurdepääsuluba. Peate tagama, et kasutajatel oleks luba ühele või mitmele kasutajale suunatud menüüelemendile, mis toetavad kindlaid tööklassitüüpe, millele neil peab juurdepääs olema. Load kinnitatakse, kui kasutaja üritab loendis olevat tööd teha.|
| Litsentsiplaatidelt üleviimistellimuse loomine | Laseb laotöötajatel luua ja töödelda üleviimistellimusi otse laorakenduses. Esiteks peavad laotöötajad valima sihtlao ja seejärel saavad nad skannida rakenduse abil ühe või mitu litsentsiplaati. Kui laotöötaja valib suvandi **Lõpeta tellimus**, loob pakett-töö litsentsiplaatide jaoks registreeritud vaba kaubavaru alusel vajaliku üleviimistellimuse ja tellimuse read. Lisateavet leiate teemast [Üleviimistellimuste loomine laorakenduses](create-transfer-order-from-warehouse-app.md)


## <a name="configure-menu-items-to-create-work-for-another-worker-or-process"></a>Menüüelementide konfigureerimine teisele töötajale või protsessile töö loomiseks
Saate seadistada menüüelemendi, mis loob töö teisele töötajale pärast seda, kui algne tegevus mobiilses seadmes tehtud. Näiteks kui üks töötaja kasutab mobiilset seadet kauba vastuvõtmiseks, luuakse teisele töötajale paigutamistöö. Tööd loova menüüelemendi loomiseks valige lehel **Mobiilse seadme menüüelemendid** väljal **Režiim** suvand **Töö**. Järgmises tabelis on välja **Töö loomise protsess** valikud korraldatud töötellimuse tüübi järgi.


<table>
<tbody>
<tr>
<th>Töötellimuse tüüp</th>
<th>Suvand</th>
<th>Kirjeldus</th>
</tr>
<tr>
<td rowspan="8">Ostutellimus</td>
<td>Vastuvõttev ostutellimuse rida</td>
<td>Registreerige kauba koguse vastuvõtmine, kasutades ostutellimuse numbrit ja ostutellimuse rea numbrit, ning looge teisele töötajale paigutamistöö.</td>
</tr>
<tr>
<td>Vastuvõttev ostutellimuse rida ja kõrvaleseadmine</td>
<td>Registreerige kauba koguse laekumine, kasutades ostutellimuse numbrit ja ostutellimuse rea numbrit, ning pange kaup kõrvale. Sama töötaja teeb mõlemat.</td>
</tr>
<tr>
<td>Vastuvõttev ostutellimuse üksus</td>
<td>Registreerige kauba koguse vastuvõtmine ostutellimuse puhul, registreerides ostutellimuse numbri ja ostutellimuse rea numbri, ning looge teisele töötajale paigutustöö.</td>
</tr>
<tr>
<td>Vastuvõttev ostutellimuse üksus ja kõrvaleseadmine</td>
<td>Registreerige ostutellimuse kauba koguse laekumine, registreerides ostutellimuse numbri ja kaubakoodi, ning pange kaup kõrvale. Sama töötaja teeb mõlemat.</td>
</tr>
<tr>
<td>Vastuvõttev litsentsiplaat</td>
<td>Saate võtta vastu sissetuleva saadetise eelteatise (ASN), kasutades litsentsiplaadi ID-d.</td>
</tr>
<tr>
<td>Litsentsiplaadi vastuvõtt ja kõrvaleseadmine</td>
<td>Saate võtta vastu ja kõrvale panna sissetuleva saadetise eelteatise (ASN), kasutades litsentsiplaadi ID-d.</td>
</tr>
<tr>
<td>Vastuvõetav koormas olev kaup</td>
<td>Registreerige koorma koguse sissetulek, kasutades koorma ID-d, ja looge teisele töötajale paigutustöö. Kaubakood ja tootedimensioonid vastavad ostutellimuse ridadele.</td>
</tr>
<tr>
<td>Vastuvõetav ja kõrvaleseatav koormas olev kaup</td>
<td>Registreerige koorma koguse laekumine, kasutades koorma ID-d, ja pange kaup kõrvale. Kaubakood ja tootedimensioonid vastavad ostutellimuse ridadele. Sama töötaja teeb mõlemat.</td>
</tr>
<tr>
<td rowspan="2">Tagastustellimus</td>
<td>Tagastustellimuse vastuvõtt</td>
<td>Registreerige kauba koguse sissetulek, registreerides tagastuskoodi, ja looge teisele töötajale paigutustöö.</td>
</tr>
<tr>
<td>Tagastustellimuse vastuvõtt ja kõrvaleseadmine</td>
<td>Registreerige kauba koguse laekumine, registreerides tagastatud kauba kood, ja pange kaup kõrvale. Sama töötaja teeb mõlemat.</td>
</tr>
<tr>
<td rowspan="6">Edastustellimus</td>
<td>Edastustellimuse kauba vastuvõtmine</td>
<td>Registreerige kauba koguse sissetulek ja looge teisele töötajale paigutustöö.

<strong>Märkus.</strong> Kasutage seda suvandit ainult juhul, kui kaubad lähetati laost, mis pole laohaldusprotsesside puhul lubatud.</td>
</tr>
<tr>
<td>Vastuvõttev edastustellimuse üksus ja kõrvaleseadmine</td>
<td>Registreerige kauba koguse laekumine ja pange kaup kõrvale. Sama töötaja teeb mõlemat.

<strong>Märkus.</strong> Kasutage seda suvandit ainult juhul, kui kaubad lähetati laost, mis pole laohaldusprotsesside puhul lubatud.</td>
</tr>
<tr>
<td>Edastustellimuse rea vastuvõtmine</td>
<td>Registreerige kauba koguse sissetulek ja looge teisele töötajale paigutustöö.</td>
</tr>
<tr>
<td>Vastuvõetava ja kõrvaleseatava tellimuserea ülekanne</td>
<td>Registreerige kauba koguse laekumine ja pange kaup kõrvale. Sama töötaja teeb mõlemat.</td>
</tr>
<tr>
<td>Vastuvõttev litsentsiplaat</td>
<td>Saate võtta vastu sissetuleva saadetise eelteatise (ASN), kasutades litsentsiplaadi ID-d.</td>
</tr>
<tr>
<td>Litsentsiplaadi vastuvõtt ja kõrvaleseadmine</td>
<td>Saate võtta vastu ja kõrvale panna sissetuleva saadetise eelteatise (ASN), kasutades litsentsiplaadi ID-d.</td>
</tr>
<tr>
<td rowspan="4">Tootmine</td>
<td>Teata lõpetamisest</td>
<td>Registreerige lõpetatud kauba kogus, mille tootmine on lõpetatud, ja looge teisele töötajale paigutustöö. Kogus võib olla terve tootmiseks plaanitud kogus või osa sellest.</td>
</tr>
<tr>
<td>Teata lõpetamisest ja sea kõrvale</td>
<td>Registreerige lõpetatud kauba kogus, mille tootmine on lõpetatud, ja pange kaup kõrvale. Kogus võib olla terve tootmiseks plaanitud kogus või osa sellest. Sama töötaja teeb mõlemat.</td>
</tr>
<tr>
<td>Kanban</td>
<td>Näidake, et kanban on lõpule viidud, ja looge teisele töötajale paigutustöö.</td>
</tr>
<tr>
<td>Kanbani kõrvalepanek</td>
<td>Näidake, et kanban on lõpule viidud, ja pange kaubad kõrvale. Sama töötaja teeb mõlemat.</td>
</tr>
<tr>
<td rowspan="5">Varud</td>
<td>Liikumine</td>
<td>Registreerige, et kaubad on viidud ühest asukohast teise. Töötaja määrab asukohad, kust kuhu kaubad viiakse.</td>
</tr>
<tr>
<td>Vaheladu</td>
<td>Muutke litsentsiplaadi või asukoha vaba kaubavaru olekut, et kahjustatud või puuduv laokaup poleks kättesaadav.</td>
</tr>
<tr>
<td>Teisaldus malli alusel</td>
<td>Teisaldage kaubad poolautomaatselt ühest asukohast teise. Töötaja valib asukoha, kust kaupu teisaldada, ja süsteem kasutab asukohakorraldust, et määrata, kuhu need teisaldada.</td>
</tr>
<tr>
<td>Edastus laos</td>
<td>Registreerige, et kaubad on üle kantud ühest laost teise. Selleks peab töötajal olema lubatud teha tööd mõlemas laos.

<strong>Märkus.</strong> See menüüelement nõuab lao vaikeüleviimistöölehte, kus välja <strong>Sissekanne</strong> suvandiks on valitud <strong>Sisestamine</strong>.</td>
</tr>
<tr>
<td>Litsentsiplaadi laadimine</td>
<td>Kasutage seda võimalust, kui seadistate ladu esimest korda. Skannige lao kõigi asukohtade kõik litsentsiplaadid. Asukohad peavad olema litsentsiplaatidega juhitavad. Seda suvandit e&#39;i saa kasutada, kui suvand <strong>Seerianumber</strong> või <strong>Partii number</strong> on varude reserveerimishierarhias suvandist <strong>Asukoht</strong> kõrgemal.</td>
</tr>
<tr>
<td rowspan="3">Tsükliline inventuur</td>
<td>Saabumise korrigeerimine</td>
<td>Suurendage varudes olevate kaupade kogust. Määrake asukoht, litsentsiplaat, kaup, kogus, mõõtühik ja olek.</td>
</tr>
<tr>
<td>Väljastuse korrigeerimine</td>
<td>Vähendage varudes olevate kaupade kogust. Määrake asukoht, litsentsiplaat, kaup, kogus, mõõtühik ja varude olek.</td>
</tr>
<tr>
<td>Punkttsükliline inventuur</td>
<td>Alustage asukoha loendist. Töötaja peab loendama asukoha kõiki kaupu. Kui loendamise tulemus on oodatud kogusest väiksem, arvestatakse puuduv kogus kahjumiks.</td>
</tr>
</tbody>
</table>

## <a name="configure-menu-items-to-process-existing-work"></a>Menüüelementide konfigureerimine olemasoleva töö töötlemiseks
Peale laotöö loomise jaoks menüüelementide seadistamise saate seadistada menüüelemente juba loodud töö töötlemiseks. Määrake välja **Režiim** sätteks **Töö** ja valige suvand **Kasuta olemasolevat tööd**. Seejärel muutuvad vahekaardil **Üldine** kättesaadavaks lisavalikud. Saate juhtida juurdepääsu menüüelementidele, määrates kiirkaardil **Tööklass** ühe või enam tööklasse. Tööklassid määratlevad töö, mida menüüelement saab töödelda. Tööklassi saab kasutada ka kindlatele kasutajarollidele juurdepääsu andmiseks või erinevat tüüpi operatsioonide eraldi töötlemiseks. Järgmises tabelis on kirjeldatud saadaolevaid suvandeid. Selle suvandi saab valida lehel **Mobiilse seadme menüü-üksused** väljal **Juhtija**. 

<table>




<thead>
<tr class="header">
<th>Suvand</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Puudub</td>
<td>See vaikeväärtus e&#39;i töötle tööd.</td>
</tr>
<tr class="even">
<td>Süsteemi suunatud</td>
<td>Supply Chain Management juhib töötajale määratud töö tüüpi ja järjekorda. Selle suvandi valimisel saate valida toimingupaanil suvandi <strong>Süsteemi juhitud töö</strong>, et avada leht <strong>Süsteemi juhitud sortimisjärjestus</strong>, kus saate seadistada töö sortimiskriteeriumid. Sortimiskriteeriumid määravad järjestuse, milles töötaja teeb tööd. Saate lisada nii palju kriteeriume kui vaja.</td>
</tr>
<tr class="odd">
<td>Kasutaja suunatud</td>
<td>Töötaja valib tehtava töö ja järjekorra, milles seda teha.</td>
</tr>
<tr class="even">
<td>Kasutajate rühmitus</td>
<td>Töötaja rühmitab töö käsitsi. See suvand on kasulik näiteks siis, kui töötaja saab valida asukohast korraga mitu kaupa. Kui töötaja on nõutud kaupade komplekteerimise lõpetanud, saab ta kaubad kõrvale paigutada.</td>
</tr>
<tr class="odd">
<td>Süsteemi rühmitamine</td>
<td>Supply Chain Management rühmitab töötaja jaoks töö määratud välja järgi. Näiteks rühmitatakse tööd, kui töötaja skannib saadetise ID, koorma ID või mis tahes väärtuse, millega saab tööüksusi seostada. Selle valiku valimisel on kohustuslikud järgmised väljad.
<ul>
<li><strong>Süsteemi rühmitusväli</strong> – valige väli, mida töötaja skannib töö rühmitamiseks.</li>
<li><strong>Süsteemi rühmitussilt</strong> – sisestage tekst töötaja juhendamiseks, mida on töö rühmitamiseks vaja skannida.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kinnitatud kasutaja suunatud</td>
<td>Töötaja valib tehtava töö, kui töö seostatakse suurema üksusega, nt koorma või saadetisega. Töötaja määrab kaupade komplekteerimise järjekorra. Selle valiku valimisel on kohustuslikud järgmised väljad.
<ul>
<li><strong>Kinnitatud kasutaja suunatud väli</strong> – valige väli, mida töötaja skannib töö rühmitamiseks.</li>
<li><strong>Kinnitatud kasutaja suunatud silt</strong> – sisestage tekst töötaja juhendamiseks, mida skannida, kui komplekteerimistöö on rühmitanud süsteem.</li>
</ul>
See suvand on kasulik näiteks siis, kui koorma jaoks kasutatakse mitut kaubaalust. Kui valite väljal <strong>Kinnitatud kasutaja suunatud</strong> suvandi <strong>LoadId</strong>, saab töötaja valida koormaga seostatud mis tahes kaubaaluse. Kui töötaja skannib kaupa, mis po&#39;le koormaga seostatud, kuvatakse tõrketeade.</td>
</tr>
<tr class="odd">
<td>Kogumi komplekteerimine</td>
<td>Töötaja rühmitab töö kogumitesse. Kogumid võimaldavad töötajatel valida ühest asukohast korraga mitu töötellimust.</td>
</tr>
<tr class="even">
<td>Tsüklilise inventuuri rühmitamine</td>
<td>Töötaja valib tsooni, töökausta või asukoha ja Supply Chain Management määrab töö valiku järgi. Kui valite selle valiku, võite klõpsata ka toimingupaanil suvandit <strong>Tsükliline inventuur</strong>, et määrata kuvatav lisateave ja samuti see, mitu korda peab töötaja erinevuse leidmisel inventuuri kordama.</td>
</tr>
 <tr class="odd">
<td>Transpordi laadimine</td>
<td>See funktsioon võimaldab mitmel laotöötajal laadida varusid samast või erinevatest koormatest samale veokile ja kasutada täielikult või osaliselt tarnitavaid koormaid.</td>
</tr>
</tbody>
</table>

## <a name="additional-menu-item-options"></a>Menüüelemendi lisavalikud
Lehel **Mobiilse seadme menüüelemendid** on saadaval täiendavad menüüelemendid. Suvandid erinevad olenevalt protsessist, mille jaoks menüüelemendi konfigureerite. 

Valikute selgitused leiate järgmisest tabelist.

<table>




<thead>
<tr class="header">
<th>Väli</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Luba töö tükeldamine</td>
<td>Selle suvandi valimisel saavad kasutajad panna töötellimuse kaupu rohkem kui ühele sihtlitsentsiplaadile. See suvand on kasulik näiteks siis, kui sihtlitsentsiplaat on täis ja töötaja peab lisama ülejäänud kaubad teisele litsentsiplaadile. Selleks et näidata, et litsentsiplaat on täis, saab töötaja valida suvandi <strong>Täis</strong> ja lõpetada komplekteerimistööde vastuvõtmine. Seejärel kuvatakse komplekteeritud kaupade panemiskoht ja juba tehtud komplekteerimistöö viiakse uude töötellimusse. Sihtlitsentsiplaadi järelejäänud komplekteerimistöö jääb algsesse töötellimusse.</td>
</tr>
<tr class="even">
<td>Ankurdamine</td>
<td>Valige see suvand, et töötajad saaksid määrata asukoha, mis tühistab soovitatud vahe- või laadimiskoha. Kõik ülejäänud paigutustööd suunatakse uude asukohta. See suvand on kasulik näiteks siis, kui töötaja tahab panna doki 1 vaheasukohas kaubad tellimusse 1, aga ei saa seda teha, sest eelmine koorem pole asukohast lahkunud. Selle asemel et oodata, kuni vaheasukoha dokk 1 vabaneb, on töötajal võimalik kasutada doki 2 vaheasukohta. Sellisel juhul tühistab töötaja soovitatud vaheasukoha. Töötellimuse ülejäänud kaupade paigutusasukoht värskendatakse doki 2 vaheasukohale. Selle suvandi valimisel peate määrama välja <strong>Ankurdaja</strong>.</td>
</tr>
<tr class="odd">
<td>Ankurdaja</td>
<td>Kui kasutat&#39;e ankurdamist, peate määrama, kas ankurdada saadetise või koorma järgi.</td>
</tr>
<tr class="even">
<td>Auditi malli ID</td>
<td>Valige töö auditi mall, mis katkestab selle menüüelemendi tööprotsessi, et saaks teha muud toimingut. Näiteks kui menüüelement käib sissetuleva töö kohta, võib auditi mall nõuda, et töötaja kontrolliks temperatuuri tarnekonteineris. Punkt, milles protsess katkestatakse, määratakse auditi mallil. See punkt võib olla näiteks töö alustamine või lõpule viimine või selle oleku muutmine.</td>
</tr>
<tr class="odd">
<td>Kogumiprofiili ID</td>
<td>Valige kogumi komplekteerimiseks kogumiprofiil. Kogumiprofiil sisaldab sätteid, näiteks seda, kas kogumid tuleks luua automaatselt, positsioonide nimesid ja tööüksuste arvu, mida saab neile määrata, millal lammutada kogumid eraldi üksusteks ja kas vajalik on kinnitamine. See väli on saadaval ainult siis, kui väljal <strong>Suunaja</strong> on valitud suvand <strong>Kogumi komplekteerimine</strong>.</td>
</tr>
<tr class="even">
<td>Loenda esimesena kauba täielik kogus</td>
<td>Selle suvandi valimisel on töötajal kohustus loendada loendamise ajal kõigepealt täielik kogus. Kui leitakse erinevus, peab töötaja sisestama lisaandmeid, näiteks identifitseerimisnumbri, partiinumbri ja seerianumbrid.</td>
</tr>
<tr class="odd">
<td>Loo liikumine</td>
<td>Valige see suvand, et töötaja saaks luua teisaldamiseks tööd, kuid ei peaks seda kohe tegema. See suvand on kasulik näiteks siis, kui tehtud on kvaliteedikontroll ja ülevaataja tahab kauba kvaliteedikontrolli alalt ära liigutada.</td>
</tr>
<tr class="even">
<td>Korralduse kood</td>
<td>Konkreetse asukohakorralduse kasutamiseks valige asukohakorraldusega seotud korralduse kood. See väli on saadaval töö loomisel, kui töö loomise protsessiks on <strong>Teisaldus malli alusel</strong>.</td>
</tr>
<tr class="odd">
<td>Keela tsüklilise inventuuri läved</td>
<td>Valige see suvand, et eirata tsüklilise inventuuri lävesid. Selle suvandi valimisel e&#39;i looda läveväärtuste ületamisel tsüklilise inventuuri tööd.</td>
</tr>
<tr class="even">
<td>Partii likvideerimiskoodi kuvamine</td>
<td>Selle suvandi valimisel kuvatakse partii likvideerimiskoodid. Näiteks saate kuvada partii likvideerimiskoodid, kui võtate vastu tagastatud partii. Seejärel saavad töötajad hinnata partii olekut või kvaliteeti ja valida sobiva koodi. Partii likvideerimiskoodi reeglid määravad, kas partii on saadaval teiste laoprotsesside jaoks. Kui te seda suvandit e&#39;i vali, kasutatakse üht järgmistest partii likvideerimiskoodidest.
<ul>
<li>Kui saate uue partiinumbri, kasutatakse kauba mudeligrupis määratud partii vaikelikvideerimiskoodi.</li>
<li>Kasutatakse partiile juba määratud partii likvideerimiskoodi.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Kuva likvideerimiskood</td>
<td>Valige see suvand likvideerimiskoodide kuvamiseks. Näiteks saate kuvada likvideerimiskoodid, kui võtate vastu tagastatud kaubad. Seejärel saavad töötajad hinnata kaupade olekut või kvaliteeti ja valida sobiva koodi. Likvideerimiskoodi reeglid määravad, kas kaup on saadaval teiste laoprotsesside jaoks.</td>
</tr>
<tr class="even">
<td>Kuva varude olek</td>
<td>Valige see suvand, et kuvada varudes olevate kaupade olek. See valik on saadaval kõikide menüüelementide jaoks, mis kasutavad olemasolevat tööd, v.a tsükliline inventuur.</td>
</tr>
<tr class="odd">
<td>Kuva komplekteerimiskuva kokkuvõte</td>
<td>Valige see suvand, et kuvada valitud töötellimuse komplekteerimistöö kokkuvõte. Kokkuvõte kuvatakse seni, kuni töödeldakse töötellimuse esimest töörida.</td>
</tr>
<tr class="even">
<td>Loo litsentsiplaat</td>
<td>Valige see suvand, et luua kordumatu identifitseerimisnumber, lähtudes numbriseeria valikust. Näiteks saate luua identifitseerimisnumbri ostutellimuste jaoks vastu võetud kaupadele.</td>
</tr>
<tr class="odd">
<td>Grupi kõrvalepanek</td>
<td>Valige see suvand paigutustöö rühmitamiseks. See suvand on saadaval, kui töö rühmitas töötaja või Supply Chain Management. Kui töötaja on lõpetanud kõik rühma komplekteerimistööd, luuakse paigutamistöö sama rühma jaoks.</td>
</tr>
<tr class="even">
<td>Varude korrigeerimistüübid</td>
<td>Valige varude korrigeerimistüüp, mis määrab varude inventuuritöölehe, mida kasutatakse korrigeerimise sisestamiseks, ja selle, kas reserveeringud eemaldatakse. See väli on saadaval vaid tööloomisprotsesside <strong>Saabumise korrigeerimine</strong> või <strong>Väljastuse korrigeerimine</strong> jaoks.</td>
</tr>
<tr class="odd">
<td>Partiinumbri alistamine</td>
<td>Selle suvandi valimisel saavad töötajad, kes esitavad tootmistellimuses lõpetatud koguse, sisestada partiinumbri, mis erineb tootmistellimusele määratud partiinumbrist.</td>
</tr>
<tr class="even">
<td>Sihtlitsentsiplaadi alistamine</td>
<td>Selle suvandi valimisel saavad töötajad määrata identifitseerimisnumbri, mis erineb soovitatud sihtlitsentsiplaadist. Valige see suvand, kui töötellimuse esimene komplekteerimine hõlmab litsentsiplaadil oleva kauba tervet kogust. See suvand on kasulik näiteks kaubaaluse uuesti kasutamisel.</td>
</tr>
<tr class="odd">
<td>Komplekteerimine ja pakkimine</td>
<td>Selle suvandi valimisel saavad töötajad ühendada müügitellimuse või koorma töö ühte tööüksusesse. Töötaja saab teha tööd ainult müügitellimuse või koorma jaoks. See suvand on kasulik näiteks siis, kui peate pärast müügitellimuse jaoks koorma, saadetise ja töö loomist suurendama müügitellimuse kogust. See valik on saadaval, kui menüüelement kasutab olemasolevat tööd ja töö suunab kasutaja või süsteem.</td>
</tr>
<tr class="even">
<td>Komplekteeri vanim partii</td>
<td>Näidake, kas töötaja peab kõigepealt komplekteerima asukoha vanima partii. Valikud on järgmised:
<ul>
<li><strong>Puudub</strong> – töötaja saab komplekteerida asukohas mis tahes töö. Töötaja ei saa mingit sõnumit.</li>
<li><strong>Hoiata</strong> – töötaja saab komplekteerida asukohas mis tahes partii, aga kui partii po&#39;le kõige vanem, kuvatakse hoiatusteade.</li>
<li><strong>Sunni</strong> – töötaja peab komplekteerima asukoha vanima partii. Töötaja saab tõrketeade, kui partii pol&#39;e vanim. <strong>Märkus.</strong> See suvand on asjakohane ainult siis, kui kaubale määratud reserveerimishierarhias on <strong>Partii number</strong> madalamal kui <strong>Asukoht</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Prindi silt</td>
<td>Valige see suvand, et töötajad saaksid printida litsentsiplaadi silte.</td>
</tr>
<tr class="even">
<td>Süsteemi rühmitusväli</td>
<td>Valige väli, mis määratleb, kuidas Supply Chain Management rühmitab töötajate jaoks komplekteerimistöö. Kui valite näiteks välja <strong>ShipmentId</strong>, skannib töötaja komplekteerimistöö rühmitamiseks saadetise ID. Seejärel määratakse kogu saadetisega seotud töö töötajale. Selleks peate looma menüüelemendi, et kasutada süsteemi rühmitatud olemasolevat tööd. Peate ka sisestama teksti väljale <strong>Süsteemi rühmitussilt</strong> töötaja juhendamiseks, mida on töö rühmitamiseks vaja skannida.</td>
</tr>
<tr class="odd">
<td>Süsteemi rühmitussilt</td>
<td>Sisestage tekst töötaja juhendamiseks, mida skannida, kui Supply Chain Management rühmitab komplekteerimistöö. Kui kasutat&#39;e näiteks komplekteerimistöö rühmitamiseks saadetise järgi välja <strong>ShipmentId</strong>, võib vajalik olla väljale <strong>Saadetise ID</strong> sisestamine. Selleks peate looma menüüelemendi, et kasutada süsteemi rühmitatud olemasolevat tööd. Peale selle peate valima väljal <strong>Süsteemi rühmitamine</strong> rühmitamise aluseks oleva välja.</td>
</tr>
<tr class="even">
<td>Kasuta vaikeandmeid</td>
<td>Selle suvandi valimisel lubatakse toimingupaanil nupp <strong>Vaikeandmed</strong>, kust saate valida väljad nende andmete kuvamiseks, mida töötajal enamasti igapäevases töös vaja läheb. See suvand on kasulik näiteks siis, kui töötaja komplekteerib kaupu sageli samast asukohast. Asukoha vaikimisi kuvamiseks valige väli <strong>Asukohast</strong>.</td>
</tr>
<tr class="odd">
<td>Kinnitatud kasutaja suunatud väli</td>
<td>Valige väli, mida töötaja skannib töö rühmitamiseks. Kui näiteks valite välja <strong>LoadId</strong>, saab töötaja valida mis tahes töö, mis on seotud valitud koormaga. Peate ka sisestama teksti väljale <strong>Kinnitatud kasutaja suunatud silt</strong> töötaja juhendamiseks, mida on töö rühmitamiseks vaja skannida.</td>
</tr>
<tr class="even">
<td>Kinnitatud kasutaja suunatud silt</td>
<td>Sisestage tekst töötaja juhendamiseks, mida skannida, kui komplekteerimistöö rühmitab kinnitatud kasutaja suunatud välja. Kui kasutate näiteks komplekteerimistöö rühmitamiseks koorma järgi välja <strong>LoadId</strong>, võib vajalik olla <strong>Koorma ID</strong> sisestamine välja.</td>
</tr>
<tr class="odd">
<td>Töömalli kood</td>
<td>Valige töömall, mis loob protsessi jaoks töö. Näiteks kui võtate ostutellimuse jaoks kauba vastu, luuakse töömalli alusel paigutamistöö. Kui te töömalli ei vali, määrab Supply Chain Management malli päringukriteeriumide alusel. Töömallide kohta lisateavet leiate teemast <a href="control-warehouse-location-directives.md">Laotöö juhtimine töömallide ja asukohakorraldustega</a>.</td>
<tr class="even">
<td>Töörea loendi kuvamine</td>
<td>Valige suvand, kuidas töötajad saavad vaadata ja suhelda praegu valitud komplekteerimistöö ridadega. Lisateavet selle suvandi kohta leiate teemast <a href="pick-line-overview.md">Mobiilse seadme menüüelemendi seadistamine komplekteerimisrea ülevaate kuvamiseks</a>.</td>
</tr>
</tbody>
</table>

## <a name="require-workers-to-confirm-the-product-location-or-quantity-when-they-pick-items"></a>Nõue, et töötajad kinnitaksid kaupade komplekteerimisel toote, asukoha või koguse
Saate seadistada töökinnitused, mis nõuavad, et töötaja kasutaks laos tööd tehes asukoha või koguse registreerimiseks mobiilset seadet. Töökinnitused aitavad tagada, et töötaja on õiges asukohas või tegeleb õige kaubakogusega. Peale selle saate lubada, et Supply Chain Management kinnitab töötaja registreeringu automaatselt. Kui lubate automaatse kinnitamise, ei saa te nõuda asukoha või koguse kinnitamist. Töökinnitused sisaldavad ka tooteid ja tootevariante. Peale selle saate kinnitusi vöötkoodi skannides registreerida. Toodete ja tootevariantide kinnitamiseks peate sisestama toote või tootevariandi ID. See võib olla toote ID, tooteotsingu ID, väline ID, GTIN või vöötkood. Kui olete ID sisestanud või vöötkoodi skanninud, kuvatakse mobiilses seadmes tootevariandi dimensioonid. 

Järgmises tabelis kirjeldatakse erinevaid töötüüpe, millega saate töökinnitusi kasutada.

| Suvand | Kirjeldus |
|------------------------|----------------------------------------------------------------------------|
| Komplekteeri | Kinnitusnõue kaupade komplekteerimisel. |
| Pane | Kinnitusnõue kaupade asukohta paigutamisel. |
| Inventuur | Nõuda kinnitust tsükli inventuuris. |
| Korrigeerimised | Kinnitusnõue varude koguste korrigeerimisel. |
| Kohandatud | Nõuda kinnitust kohandatud töö korral. |
| Vaheladu | Kinnitusnõue kaupade teisaldamisel vahelattu. |
| Litsentsiplaadi koostamine | Kinnitusnõue kaupade konsolideerimisel litsentsiplaadi koostamiseks. |
| Prindi | Kinnitusnõue litsentsiplaadi siltide printimisel. |
| Oleku muutus | Kinnitusnõue varude oleku muutmisel. |

> [!NOTE]
> Saate toote kinnitamist taotleda üksnes komplekteerimise ja ladustamise tüüpi tööde korral.

<a name="additional-resources"></a>Lisaressursid
--------

[Mobiilse seadme menüüelemendi seadistamine ostutellimuse lõpetamiseks](tasks/set-up-mobile-device-menu.md)

[Mobiilse seadme menüükäsu seadistamine saabunud kaupade registreerimiseks](tasks/set-up-mobile-device-menu-item-register-received-items.md)

[Varude olekud](../inventory/inventory-statuses.md)


