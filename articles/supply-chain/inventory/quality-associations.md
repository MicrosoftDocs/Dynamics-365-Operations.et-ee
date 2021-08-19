---
title: Kvaliteediseosed
description: See teema kirjeldab, kuidas saate kasutada Microsoft Dynamics 365 Supply Chain Management kvaliteediseoseid, et luua automaatselt teie müügi-, ostu- ja tootmisprotsessidega seotud kvaliteettellimusi.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b0705af8f8c40db82e412f294f45f704b7a628c1ced679cef25ce77d49642feb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724840"
---
# <a name="quality-associations"></a>Kvaliteediseosed

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas saate kasutada Microsoft Dynamics 365 Supply Chain Management kvaliteediseoseid, et luua automaatselt teie müügi-, ostu- ja tootmisprotsessidega seotud kvaliteettellimusi.

Kvaliteediseos määratleb koostatava kvaliteettellimuse puhul kogu järgmise teabe.

- Kande sündmus
- Kaupade puhul tehtavate katsete kogum
- Vastuvõetav kvaliteeditase (AQL)
- Valimi plaan

Kvaliteediseos tuleb automaatset kvaliteettellimuse genereerimist nõudvas äriprotsessis määrata iga variatsiooni puhul. Näiteks saab kvaliteettellimuse koostada ostutellimuste, vahelaotellimuste, müügitellimuste ja tootmistellimuste äriprotsessides.

## <a name="working-with-quality-associations"></a>Kvaliteediseostega töötamine

Kvaliteediseost kasutav äriprotsess võib olla seotud mitmesuguste lähtedokumentidega, nt ostutellimuste, müügitellimuste või tootmistellimustega.

Iga kvaliteediseose kirje määrab ka katsete kogumi, AQL-i ning valikukava, mida rakendatakse loodud kvaliteettellimustele. Peate iga äriprotsessi variatsiooni jaoks määratlema kvaliteediseose kirje. Näiteks saate seadistada kvaliteediseose, mis koostab kvaliteettellimuse, kui ostutellimuse toote sissetulekut värskendatakse. Sõltuvalt täitmisplaani seadistusest saab käivitamisprotsessi ise blokeerida, kui on avatud kvaliteettellimus. Teise võimalusena saab blokeerida järgnevad protsessid, näiteks ostutellimuse arveldamine.

> [!NOTE]
> Kui on avatud kvaliteettellimusi, blokeeritakse varude koguste väljastamine automaatselt. Olenevalt valiku **Täielik blokeerimine** seadistusest lehel **Kaubaproovid** on kogus kas kvaliteettellimusel olev kogus või lähtedokumendi real olev kogus. Lisateavet vt [Kvaliteedijuhtimise kauba valim](quality-item-sampling.md).

Konkreetse äriprotsessi jaoks määratleb kvaliteediseos kirje sündmuse ja tingimused, mille jaoks kvaliteettellimus genereeritakse. Tingimused võivad olla asukoha või juriidilise isiku põhised. Purustavaid katseid hõlmavat kvaliteettellimust saab luua ainult siis, kui sündmusel on olemas vaba laovaru.

Kvaliteediseostega tööks minge **Varude haldus \> Seadistus \> Kvaliteedikontroll \> Kvaliteediseosed**. Järgmistes näidetes on näha, kuidas kvaliteediseose kirjet määratakse iga äriprotsessi variatsiooni puhul. Iga näite puhul võetakse järgmises tabelis kokku sündmused ja tingimused, mis on kvaliteediseose kirjega määratletud.

<table>
<thead>
<tr>
<th>Viite tüüp</th>
<th>Sündmuse tüüp</th>
<th>Käivitamine</th>
<th>Sündmuse blokeerimine</th>
<th>Dokumendi viide</th>
</tr>
</thead>
<tbody>
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
<td>None</td>
<td rowspan="3">Konkreetne ID, Grupp või Kõik ja Ressursipõhine, Grupp või Kõik</td>
</tr>
<tr>
<td>Teata lõpetamisest</td>
</tr>
<tr>
<td>Pärast</td>
<td>None</td>
</tr>
<tr>
<td rowspan="3">Kaastoote tootmine</td>
<td>Registreerimine</td>
<td>Pole kohaldatav</td>
<td rowspan="3">None</td>
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

> [!NOTE]
> Funktsioon *Kvaliteedijuhtimine laoprotsesside jaoks* lisab võimalusi kvaliteettellimuse töötlemiseks tootmise puhul, mille **Sündmuse tüüp** on seatud väärtusele *Teata lõpetamisest* ja **Käivitamine** väärtusele *Pärast*, ning ostude puhul, mille **Sündmuse tüüp** on seatud väärtusele *Registreerimine*. Lisateabe saamiseks vt [Kvaliteedijuhtimine laoprotsesside jaoks](quality-management-for-warehouses-processes.md).

Järgmises tabelis on veel teavet kvaliteettellimuste loomise kohta konkreetset tüüpi protsessidele.

<div class="tableSection">
<table>
<thead>
<tr>
<th>Protsessi tüüp</th>
<th>Millal saab kvaliteettellimusi automaatselt luua</th>
<th>Millal saab kvaliteettellimusi luua, kui on vajalik purustav katsetamine</th>
<th>Tingimuse teave</th>
<th>Käsitsi loomise teave</th>
</tr>
</thead>
<tbody>
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
<td>Destruktiivseid katseid nõudvaid kvaliteettellimusi ei saa luua. Eeldatakse, et garantiitellimuse funktsionaalsus käsitleb hävinenud materjali käsitlemist.</td>
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
<td>Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või hankijat või nende tingimuste kombinatsiooni.</td>
<td>Käsitsi loodud tootmistellimusele viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</td>
</tr>
<tr>
<td>Tootmistellimus, millel on protsessitoiming</td>
<td>Enne või pärast toimingu aruande lõpetamist</td>
<td>Pärast viimase toimingu tootmise lõpetamisest teatamist</td>
<td>Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või toimingute ressurssi või nende tingimuste kombinatsiooni.</td>
<td>Käsitsi loodud protsessitoimingule viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</td>
</tr>
<tr>
<td>Varud</td>
<td>Kvaliteettellimust ei saa automaatselt koostada varude töölehe kandele või ülekandetellimuse tehingutele.</td>
<td></td>
<td></td>
<td>Kvaliteettellimus tuleb kauba laokogusele käsitsi koostada. Nõutav on füüsiline vaba laovaru.</td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a>Kvaliteettellimuste automaatse genereerimise näited

### <a name="purchasing"></a>Ostmine

Kui määrate ostmisel välja **Sündmuse tüüp** väärtuseks *Toote sissetulek* ja välja **Käivitamine** väärtuseks *Pärast* lehel **Kvaliteediseosed**, saate järgmised tulemused:

- Kui valiku **Värskendatud koguse kohta** väärtuseks on seatud *Jah*, luuakse iga sissetuleku kohta kvaliteettellimus ostutellimuse suhtes, võttes aluseks sissetulnud koguse ja kauba valimi sätted. Iga kord, kui ostutellimuse vastu on saadud kogus, luuakse äsja vastuvõetud koguse põhjal uued kvaliteettellimused.
- Kui valiku **Värskendatud koguse kohta** väärtuseks on seatud *Ei*, luuakse sissetulnud koguse põhjal esimese sissetuleku kohta kvaliteettellimus ostutellimuse suhtes. Lisaks luuakse üks või mitu kvaliteettellimust järelejäänud koguse põhjal, sõltuvalt jälgimisdimensioonidest. Kvaliteettellimusi ei looda järgnevate sissetulekute kohta ostutellimuse suhtes.

### <a name="production"></a>Tootmine

Kui määrate tootmisel välja **Sündmuse tüüp** väärtuseks *Lõpetamise kinnitamine* ja välja **Käivitamine** väärtuseks *Pärast* lehel **Kvaliteediseosed**, saate järgmised tulemused:

- Kui valiku **Värskendatud koguse kohta** väärtuseks on seatud *Jah*, luuakse kvaliteettellimus iga lõpetatud koguse ja kauba valimi sätete alusel. Iga kord, kui kogus märgitakse tootmistellimuse suhtes lõpetatuks, luuakse äsja lõpetatud koguse põhjal uued kvaliteettellimused. See loomisloogika on kooskõlas ostuga.
- Kui valiku **Värskendatud koguse kohta** väärtuseks on seatud *Ei*, luuakse lõpetatud koguse põhjal kvaliteettellimus esimesel korral, kui kogus kinnitatakse lõpetatuks. Lisaks luuakse üks või mitu kvaliteettellimust järelejäänud koguse põhjal, sõltuvalt kauba valimi jälgimisdimensioonidest. Hilisemate lõpetatud koguste kohta ei looda kvaliteettellimusi.

<table>
<thead>
<tr>
<th>Kvaliteedi spetsifikatsioon</th>
<th>Värskendatud koguse kohta</th>
<th>Jälgimisdimensiooni kohta</th>
<th>Tulemus</th>
</tr>
</thead>
<tbody>
<tr>
<td>Protsent: 10%</td>
<td>Jah</td>
<td>
<p>Partii number: ei</p>
<p>Seerianumber: ei</p>
</td>
<td>
<p>Tellimuse kogus: 100</p>
<ol>
<li>Teata 30 lõpetatuks
<ul>
<li>Kvaliteettellimus 1 3 kohta (10% 30-st)</li>
</ul>
</li>
<li>Teata 70 lõpetatuks
<ul>
<li>Kvaliteettellimus 2 7 kohta (10% järelejäänud tellimuse kogusest, mis võrdub sel juhul 70-ga)</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Fikseeritud kogus: 1</td>
<td>Ei</td>
<td>
<p>Partii number: ei</p>
<p>Seerianumber: ei</p>
</td>
<td>Tellimuse kogus: 100
<ol>
<li>Teata 30 lõpetatuks
<ul>
<li>Kvaliteettellimus 1 1 kohta (esimese lõpetatuna kinnitatud koguse jaoks, millel on fikseeritud väärtus 1)</li>
<li>Kvaliteettellimus 2 1 kohta (järelejäänud koguse jaoks, millel on ikka fikseeritud väärtus 1)</li>
</ul>
</li>
<li>Teata 10 lõpetatuks
<ul>
<li>Ühtegi kvaliteettellimust ei looda.</li>
</ul>
</li>
<li>Teata 60 lõpetatuks
<ul>
<li>Ühtegi kvaliteettellimust ei looda.</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Fikseeritud kogus: 1</td>
<td>Jah</td>
<td>
<p>Partii number: jah</p>
<p>Seerianumber: jah</p>
</td>
<td>
<p>Tellimuse kogus: 10</p>
<ol>
<li>Lõpetatuna kinnitamine 3: 1 partiinumbri b1 puhul, seerianumber s1; 1 partiinumbri b2 puhul, seerianumber s2; ja 1 partiinumbri b3 puhul, seerianumber s3
<ul>
<li>Kvaliteettellimus 1 1 kohta partiist b1, seerianumber s1</li>
<li>Kvaliteettellimus 2 1 kohta partiist b2, seerianumber s2</li>
<li>Kvaliteettellimus 3 1 kohta partiist b3, seerianumber s3</li>
</ul>
</li>
<li>Teata lõpetatuna: 2: 1 partiinumbri b4 puhul, seerianumber s4; ja 1 partiinumbri b5 puhul, seerianumber s5
<ul>
<li>Kvaliteettellimus 4 1 kohta partiist b4, seerianumber s4</li>
<li>Kvaliteettellimus 5 1 kohta partiist b5, seerianumber s5</li>
</ul>
</li>
</ol>
<p><strong>Märkus.</strong> Partiid saab uuesti kasutada.</p>
</td>
</tr>
<tr>
<td>Fikseeritud kogus: 2</td>
<td>Ei</td>
<td>
<p>Partii number: jah</p>
<p>Seerianumber: jah</p>
</td>
<td>
<p>Tellimuse kogus: 10</p>
<ol>
<li>Lõpetatuna kinnitamine 3: 1 partiinumbri b1 puhul, seerianumber s1; 1 partiinumbri b2 puhul, seerianumber s2; 1 partiinumbri b3 puhul, seerianumber s3 ja 1 partiinumbri b4 puhul, seerianumber s4
<ul>
<li>Kvaliteettellimus 1 1 kohta partiist b1, seerianumber s1</li>
<li>Kvaliteettellimus 2 1 kohta partiist b2, seerianumber s2</li>
<li>Kvaliteettellimus 3 1 kohta partiist b3, seerianumber s3</li>
<li>Kvaliteettellimus 4 1 kohta partiist b4, seerianumber s4</li>
</ul>
<ul>
<li>Kvaliteettellimus 5 2 kohta,ilma viiteta partiile ja seerianumbrile</li>
</ul>
</li>
<li>Teata lõpetatuna 6: 1 partiinumbri b5 puhul, seerianumber s5; 1 partiinumbri b6 puhul, seerianumber s6; 1 partiinumbri b7 puhul, seerianumber s7; 1 partiinumbri b8 puhul, seerianumber s8; 1 partiinumbri b9 puhul, seerianumber s9; ja 1 partiinumbri b10 puhul, seerianumber s10
<ul>
<li>Ühtegi kvaliteettellimust ei looda.</li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Lisaressursid

- [Kvaliteedijuhtimise protsessid](quality-management-processes.md)
- [Kvaliteedi ja mittevastavuse haldamise lubamine](enable-quality-management.md)
- [Laoprotsesside kvaliteedijuhtimine](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
