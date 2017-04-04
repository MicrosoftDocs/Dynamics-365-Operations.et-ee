---
title: "Väikesed summad Ida-Euroopa"
description: "See teema pakub teavet väikesed summad funktsiooni, mille abil kasutajad Eesti, Leedu, Tšehhi, Ungari, Läti, Poola ja Venemaa kajastavad sularaha süsteemis."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RCashBalance, RCashCountStatementForm, RCashPosting, RCashRemainLimit, RCashReportJour_PL, RCashTable, RCashTableBalance, RCashTableCredLimit, RCashTableLastRevaluation, RCashTableTransactions, RCashTrans
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268504
ms.assetid: ff2ea7b0-8de2-48c5-8f9f-5d95d9924925
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: e843abff91f74ff8c2c577f499fa829821fc56ee
ms.lasthandoff: 03/31/2017


---

# <a name="petty-cash-for-eastern-europe"></a>Väikesed summad Ida-Euroopa

See teema pakub teavet väikesed summad funktsiooni, mille abil kasutajad Eesti, Leedu, Tšehhi, Ungari, Läti, Poola ja Venemaa kajastavad sularaha süsteemis.

Väikesed summad funktsiooni abil saate automatiseerida sissetulekute ja kulutuste raha, esmane dokumentide loomise ja vastavate aruannete printimine. Väikesed summad funktsioon lubab teil sooritada järgmisi toiminguid:

-   Konto ja rahaliste varade kulutamist.
-   Looge tüüpiline raha: raha korvamisorderite, Kassa Väljaminekuorderid ja raha saatelehtede registreerimise tööleht.
-   Maksimaalselt raha ravimitele, lubatud toimingud klientide, hankijate ja nii edasi.
-   Kajastama erinevate valuutade SULARAHAOPERATSIOONID süsteemi.
-   Teisendada anda raamatupidamise aruandluse vaikevaluuta, mis koguses sularaha.
-   Luua on **Kassa** aruande ja on kassapidaja aruanne.

## <a name="prerequisites"></a>Eeltingimused
Väikesed summad funktsiooni kasutamiseks peate täitma järgmised eeltingimused:

-   Sularahakontode seadistamine
-   Saate seadistada sisestusreeglite raha.
-   Saate seadistada raha dokumendi nummerdamisel kasutatavad Numbriseeriad.
-   Saate seadistada vaikeväärtusi raha ja pangakontod parameetrid.
-   Raha nimed seadistada üldiselt pearaamatu.

### <a name="set-up-cash-accounts"></a>Raha kontode

Raha seadistamiseks avage **raha ja pangakontod juhtimise**&gt;**panga**&gt;**raha kontode**, ja sisestage järgmine teave.

| Väli                 | Kirjeldus                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------|
| Sularaha                  | Sisestada tähise, mis tuvastab sularahaarve (raha).                                                                    |
| Nimi                  | Sisestage kirjeldus sularahaarve.                                                                             |
| Valuuta              | Valige sularahatehingu valuutakoodi.                                                              |
| Numbriseeria grupp | Kui dokumendid peab erinevad järjekorranumber s.t. raha järjekorranumber on parameetrites sisestada tähise. |
| Veel valuutasid       | Märkige see ruut, et valuutade, erinevate raamatupidamise valuuta sisestatakse.                     |
| Negatiivne kassa         | Märkige see ruut, et negatiivne raha erinevates valuutades.                                               |

Seadistada saldo kontrolli eeskirjad valige sularahakonto sularahaarve ja siis Updatehagi paani kohta selle **raha konto** vahekaardil, on **saldolimiiti** nuppu **saldolimiiti**. Sisestage järgmine teave.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Väli</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valuuta tüüp</td>
<td>Valige valuuta:
<ul>
<li><strong>Raamatupidamise valuuta</strong> – põhi firma valuutatähist.</li>
<li><strong>Näidatud valuuta</strong> – valuuta kood, mis erineb tava ettevõtte valuuta tähis.</li>
</ul></td>
</tr>
<tr class="even">
<td>Valuuta</td>
<td>Kui valisite <strong>näidatud valuuta</strong> ja selle <strong>valuutatüüp</strong> number, valuuta tähis. See väli pole saadaval, kui valitud <strong>raamatupidamise valuuta</strong> ja selle <strong>valuutatüüp</strong> välja.</td>
</tr>
<tr class="odd">
<td>Saldolimiidi tüüp</td>
<td>Tehke saadaolevad väärtused:
<ul>
<li><strong>Maksimaalne</strong> – sularaha saldot ei tohi ületada selle <strong>saldolimiiti</strong> summa raha arvel (ülemist).</li>
<li><strong>Vähemalt</strong> – sularaha saldot ei tohi minna alla selle <strong>saldolimiiti</strong> summa raha arvel (all seotud).</li>
</ul></td>
</tr>
<tr class="even">
<td>Kontrolli saldolimiiti</td>
<td>Valige, mis tekib ajal raha dokumentide protsessis kui ka <strong>saldolimiiti</strong> sularahaarve ületamise määrast:
<ul>
<li><strong>Nõus</strong> – piir ei tohi ületada.</li>
<li><strong>Hoiatus</strong> -piiri saab ületada, kuid kasutaja saab hoiatuse. Kassadokument heaks või heaks.</li>
<li><strong>Viga</strong> – piirmäära ei ületata. Kasutaja saab veateate ja kassadokument ei ole heaks või heaks.</li>
</ul>
Kassa korvamis protsessis kohta lisateabe saamiseks vaadake selle &quot;raha tehingu kinnitamine ja sisestamise&quot; käesoleva teema jaotises.</td>
</tr>
<tr class="odd">
<td>Saldolimiit</td>
<td>Sisestage selle konto saldo piir. Summa peaks olema määratud valuutas.</td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-posting-profiles"></a>Saate seadistada sisestusreeglite raha

Raha sisestusreeglite määratleda konteeringud pearaamatusse. Seadistatud sisestusreeglid raha, minge **raha****ja panga juhtimise**&gt;**Setup**&gt;**raha sisestusreegleid**, ja valida või luua. Sisestage järgmine teave.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Väli</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kehtib</td>
<td>Saate valida, kas sisestusreegleid rakendatakse konkreetse sularahakonto või kõik raha ja pangakontod:
<ul>
<li><strong>Tabelis</strong> – kui konteeringu profiili Real raha arvel, et kasutatakse Kassa kannete sisestamisel.</li>
<li><strong>Kõik</strong> – ei postitad profiili jaoks on rida sularahaarve.</li>
</ul></td>
</tr>
<tr class="even">
<td>Sularaha</td>
<td>Kui valisite <strong>tabeli</strong> ja selle <strong>puhul kehtib</strong> valdkonnas, täpsustada sularahaarve. See väli on tühi, kui valisite <strong>kõik</strong> ja selle <strong>puhul kehtib</strong> välja.</td>
</tr>
<tr class="odd">
<td>Pearaamatukonto</td>
<td>Sisestage pearaamatukonto kasutada konto raha konto number.</td>
</tr>
</tbody>
</table>

### <a name="set-up-number-sequences-for-cash-documents"></a>Kassa dokumentide numbriseeriate seadistamine

Seadistama raha dokumentide jaoks, minge **raha ja pangakontod juhtimise**&gt;**Setup**&gt;**raha ja pangakontod parameetrid**. Kohta ning **jada Number** vahekaardil, saate määrata Numbriseeria koodid jaoks ning **raha korvamisorderite**, **raha Väljaminekuorderid**, **parandus sularahakviitungi**, ja **valuutakursi korrigeerimisel** dokumendid, ja **raha aruande number**.

### <a name="set-up-default-values-for-cash-and-bank-management-parameters"></a>Saate seadistada vaikeväärtusi raha ja pangakontod parameetrid

Saate seadistada vaikeväärtusi raha ja pangakontod väikesed summad funktsiooni parameetrid, minge **raha ja pangakontod juhtimise**&gt;**Setup**&gt;**raha ja panga parameetrid**. Kohta ning **raha** sakk, sisestage järgmine teave.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Väli</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Sularaha</td>
<td>Valige vaikekonto raha töölehtedel.</td>
</tr>
<tr class="even">
<td>Kassaseisu sisestamine</td>
<td>Sisestage vaikimisi raha sisestusreeglid, mida kasutatakse, kui määratakse muu sisestusreegel.</td>
</tr>
<tr class="odd">
<td>Kontrolli kasutatud kannet</td>
<td>Valige, mis toimub kui Duplikaatnumbrid ajal sisse raha dokumendi number:
<ul>
<li>Lükka duplikaat tagasi</li>
<li>Tagasi lükata koopiad majandusaasta jooksul</li>
<li>Luba duplikaate</li>
<li>Hoiata duplikaatide korral</li>
</ul></td>
</tr>
<tr class="even">
<td>Kontrolli toimingute limiiti</td>
<td>Saate määrata, mis toimub kui ületatakse piirmäära koostöölepinguid counteragents:
<ul>
<li><strong>Nõus</strong> – piir ei tohi ületada.</li>
<li><strong>Hoiatus</strong> -piiri saab ületada, kuid kasutaja saab hoiatuse. Toiming sisestatakse.</li>
<li><strong>Viga</strong> – piirmäära ei ületata. Kasutaja saab veateate ja operatsiooni ei ole postitatud.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Kontrollimeetod</td>
<td>Kontrollimeetod, mida kasutatakse tegevuste kontrolli ületada limiite valimine
<ul>
<li><strong>Operatsiooni</strong> – valideerimine on tehtud kande kohta</li>
<li><strong>Lepingu</strong> – valideerimine toimub ühe tehingu, mis on määratud vastaspoolega leping.</li>
</ul></td>
</tr>
<tr class="even">
<td>Toimingute limiit</td>
<td>Sisestage maksimaalne lubatud koostöölepinguid counteragents sularahas.</td>
</tr>
<tr class="odd">
<td>Sisestus varasemal kuupäeval</td>
<td>Märkige see ruut, et sularahatehingutes enne viimase raha kanne konteeritakse.</td>
</tr>
<tr class="even">
<td>Dimensioonid</td>
<td>Sisestage mõõtmed on <strong>osakonna kood</strong>, <strong>analüüsi kood</strong>, ja <strong>eesmärgi koodi</strong> väljad. Kassa dokumentide trükkimise vorm kajastab seda teavet.</td>
</tr>
<tr class="odd">
<td>Kasuta kinnitatud olekut</td>
<td>Märkige see ruut, kui kasutada täiendavaid olek, <strong>kinnitatud</strong>, raha dokumentide kinnitamise käigus. (Lisateabe saamiseks vt selle &quot;raha tehingu kinnitamine ja sisestamise&quot; osa.)</td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-journal-names-in-general-ledger"></a>Raha nimed seadistada üldiselt pearaamatu

Sularaha tehingute sisestamiseks töölehe loomiseks minge **PR**&gt;**seadistus on**&gt;**nimesid**, ja luua uue kirje. Aastal ning **tüüp** valdkonnas, määrata **raha**. Kui vaja, saate määratleda muud töölehe vaikeparameetrid.

## <a name="daily-cash-operations-via-a-slip-journal"></a>Igapäevane raha toimingute saatelehe tööleht
Saatelehe töölehe kaudu raha dokumendi loomiseks minge **raha ja pangakontod juhtimise**&gt;**sularaha tehingud**&gt;**saatelehe tööleht**, ja looge uus. Kohta ning tegevus paanil klõpsake **read**. Lisada uus rida ja sisestage järgmine teave.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Väli</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kuupäev</td>
<td>Sisestage kande kuupäev.</td>
</tr>
<tr class="even">
<td>Konto</td>
<td>Valige konto raha. Vaikimisi Kassa kontot määratud parameetrites raha haldamise.</td>
</tr>
<tr class="odd">
<td>Kirjeldus</td>
<td>Saate sisestada kande selgitav tekst.</td>
</tr>
<tr class="even">
<td>Deebet kreedit</td>
<td>Sisestage dokumendi rahasumma ühte neist väljadest:
<ul>
<li><strong>Deebet</strong> – selle välja abil saate registreerida sularaha kviitungid ja Kassa korvamisorderi.</li>
<li><strong>Krediidi</strong> – selle välja abil saate registreerida raha kulutuste ja kassa väljaminekuorderi.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vastaskonto tüüp vastaskonto</td>
<td>Saate valida vastaskonto tüübi ja vastaskonto kontonumbri.</td>
</tr>
<tr class="even">
<td>Valuuta</td>
<td>Valige kande valuuta tähist.</td>
</tr>
<tr class="odd">
<td>Kanne</td>
<td>See väli täidetakse automaatselt, vastavalt seadistus.</td>
</tr>
<tr class="even">
<td>Tellimuse kood</td>
<td>Kui ühtegi muud numbriseeriat seadistatakse sularahaarve, see väli täidetakse automaatselt, vastavalt parameetrites määratud numbriseeria. Sellele väljale saate sisestada käsitsi tellimuse numbrit, kui vaja. Et inconsistence raha dokumendi nummerdust, rakendatakse järgmisi kontrolli: raha dokumendi, mis on varem tegevuse arv ei tohi ületada arvu raha dokumendi, mis on hiljem operatsiooni. Kui te ei vaja seda juhtelementi, valige selle <strong>sisestus varasemal kuupäeval</strong> raha ja pangakontod dokumendihalduse Parameetrid ruut.</td>
</tr>
<tr class="odd">
<td>Kinnitamise olek</td>
<td>Esimene olek on <strong>pole</strong>. Kande oleku kohta lisateavet selle &quot;raha tehingu kinnitamine ja sisestamise&quot; lõik.</td>
</tr>
<tr class="even">
<td>Dokumendi tüüp </td>
<td>Sellel välja selle <strong>raha tellimuse</strong> kaart sisestatakse automaatselt, kassadokument sisestatud koguse põhjal:
<ul>
<li><strong>Sularaha korvamisorderi</strong> – seda väärtust kasutatakse, kui sisestasite vastav summa on <strong>deebet</strong> välja raha arvel.</li>
<li><strong>Väljaminekuorderi sularaha</strong> – seda väärtust kasutatakse, kui sisestasite vastav summa on <strong>krediidi</strong> tarbeks raha välja</li>
<li><strong>PARANDUS</strong> – sisestatud negatiivne summa on <strong>deebet</strong> välja või <strong>krediidi</strong> välja raha arvel.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Käibemaksugrupp</td>
<td>Saate määrata käibemaksugrupi maksude toimimise arvutamiseks.</td>
</tr>
<tr class="even">
<td>Kauba käibemaksugrupp</td>
<td>Määrake kauba käibemaksu Grupi tegevuse maksude arvutamiseks.</td>
</tr>
<tr class="odd">
<td>Põhjus</td>
<td>Kohta ning <strong>tellimuse raha</strong> sakk, sisestage tekst, mis kirjeldab kande suhtes. See tekst trükitakse kassa väljaminekuorder aruandluse vormi.</td>
</tr>
<tr class="even">
<td>Dokumendi kuupäev</td>
<td>Sisestage kirjeldus, number ja kuupäev on kande (nt ettemakse aruanded, arve või tellimuse) põhjus esmase dokumendi.</td>
</tr>
<tr class="odd">
<td>Esindaja tüüp</td>
<td>Sellel väljal saavad olla järgmised väärtused:
<ul>
<li><strong>Töötaja</strong> – teenuse <strong>esindaja</strong> otsing sisaldab töötajate nimekirja, kui selle <strong>vastaskonto</strong> on välja <strong>pearaamatu</strong> või <strong>panga</strong>, või loetelu ning vastaspoole kontaktisikud, kui on <strong>vastaskonto</strong> on välja <strong>kliendi</strong> või <strong>hankija</strong>. Seadistatud esindajad, minge <strong>põhilised</strong>&gt;<strong>Setup</strong>&gt;<strong>kontaktid</strong>&gt;<strong>kontaktisik</strong>.</li>
<li><strong>Muud</strong> – teenuse <strong>esindaja</strong> otsing sisaldab teiste klientide loetelu. Vastuvõtjad, kes ei ilmu seadistamiseks on <strong>hotelli</strong> või <strong>müüjad</strong> tabelis, minge <strong>PR</strong>&gt;<strong>vastuvõtjad</strong>. Selline on saadaval ainult Lätis. (Ka <strong>CSELatvia</strong> peaks olema lubatud.)</li>
<li><strong>Hankija</strong> – teenuse <strong>esindaja</strong> otsing sisaldab tarnijate loend. Hankijate seadistamiseks avage <strong>arved</strong>&gt;<strong>müüjad</strong>.</li>
<li><strong>Kliendi</strong> – teenuse <strong>esindaja</strong> otsing sisaldab klientide loetelu. Hotelli seadistamiseks avage <strong>laekumata arved</strong>&gt;<strong>hotelli</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Esindaja</td>
<td>Esinduslik määratud tüüpi on <strong>esindaja tüüp</strong> välja.</td>
</tr>
<tr class="odd">
<td>Inimese nimi</td>
<td>See väli täidetakse automaatselt, vastavalt selle <strong>vastaskonto</strong> ja <strong>esindaja</strong> väljad. Raha saatelehtede trükkimine vorm kajastab seda teavet.</td>
</tr>
<tr class="even">
<td>ID-kaart</td>
<td>See väli täidetakse automaatselt, kontaktisiku (esindaja) isikutunnistuse andmete alusel. Kui on <strong>vastaskonto tüüp</strong> on välja <strong>Avansisaajate</strong>, ja <strong>vastaskonto</strong> väärtuseks on töötaja numbri, raha laekumine või kulu saab teha alates või töötajale. Sel juhul on <strong>ID-kaardi</strong> väli täidetakse automaatselt, kasutades andmeid: isikutunnistuse ning <strong>töötaja</strong> tabeli (<strong>personali raamatupidamise</strong>&gt;<strong>töötajate tabelis</strong>).</td>
</tr>
<tr class="odd">
<td>Eesmärk</td>
<td>Aastal ning <strong>eesmärki</strong> tabel, määratleda ühe või mitme sihtkoha koodid tehingu summa. Valige sihtkoha kood on <strong>eesmärk</strong> ja sisestage selgitust selle <strong>tekst</strong> välja. Linnas on <strong>summa</strong> Sisestage summa kande valuutas. Selle <strong>%</strong> välja näitab, protsentuaalne suhe sihtkoha summa kogu tehingute hulgast.</td>
</tr>
<tr class="even">
<td>Jääk</td>
<td>Ülejäänud summa arvutatakse. Pange tähele, et kogu tehingu summa tuleb määrata sihtkoha koodid.</td>
</tr>
<tr class="odd">
<td>Ametiisikud</td>
<td>Kohta ning <strong>ametnike</strong> vahekaardil, määrake eest vastutavate isikute nimed ja pealkirjad: direktor, juhtiv raamatupidaja ja kassapidaja. Selle <strong>seisukoht</strong> väärtused määratakse ametnike seadistus on <strong>üldise</strong> ja <strong>pearaamatu</strong> saki on <strong>ametnike</strong> lehe (<strong>põhilised</strong>&gt;<strong>Setup</strong>&gt;<strong>kontaktid</strong>&gt;<strong>ametnike</strong>).</td>
</tr>
<tr class="even">
<td>Ettemaks</td>
<td>Märkige see ruut, kui kanne on Ettemaks.</td>
</tr>
<tr class="odd">
<td>Sisestusreeglid</td>
<td>Sisestage sisestusreegliga sularahaarve. Vaikimisi kasutatakse selle raha ja panga Parameetrid määratud sisestusreeglid.</td>
</tr>
<tr class="even">
<td>Vastaskontoga sisestamise reeglid</td>
<td>Saate sisestada valitud vastaskontoks sisestusreeglid.</td>
</tr>
<tr class="odd">
<td>Kogusumma</td>
<td>Aastal ning <strong>kogusumma</strong> jaotises lehekülje allosas on <strong>Reimb</strong> väljal kuvatakse kogusumma, mis on arvutatud kõik raha tagasimaksmise libiseb, mis on kantud töölehele, ja <strong>Disb</strong> väljal kuvatakse kogusumma kõik Kassa Väljaminekuorderid.</td>
</tr>
</tbody>
</table>

Päevikukannete Updatehagi paani, klõpsake nuppu **Valideeri**.

## <a name="daily-cash-operations-via-a-general-journal"></a>Peažurnaali kaudu raha igapäevatöös
Raha kandega peažurnaali loomiseks minge **PR**&gt;**päevikukannete**&gt;**Peažurnaalide**, ja looge uus. Kohta ning tegevus paanil klõpsake **read**. Lisada uus rida ja sisestage järgmine teave.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Väli</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kuupäev</td>
<td>Sisestage kande kuupäev.</td>
</tr>
<tr class="even">
<td>Konto tüüp</td>
<td>Valige <strong>väikesed summad</strong>.</td>
</tr>
<tr class="odd">
<td>Konto</td>
<td>Valige Kassa konto number.</td>
</tr>
<tr class="even">
<td>Kande tekst</td>
<td>Saate sisestada kande selgitav tekst.</td>
</tr>
<tr class="odd">
<td>Deebet kreedit</td>
<td>Sisestage dokumendi rahasumma ühte neist väljadest:
<ul>
<li><strong>Deebet</strong> – selle välja abil saate registreerida sularaha kviitungid ja Kassa korvamisorderi.</li>
<li><strong>Krediidi</strong> – selle välja abil saate registreerida raha kulutuste ja kassa väljaminekuorderi.</li>
</ul></td>
</tr>
<tr class="even">
<td>Vastaskonto tüüp vastaskonto</td>
<td>Saate valida vastaskonto tüübi ja vastaskonto kontonumbri.</td>
</tr>
<tr class="odd">
<td>Valuuta</td>
<td>Valige kande valuuta tähist.</td>
</tr>
</tbody>
</table>

Kohta ning **arve** jaotises saate määrata sisestusreeglid valitud konto ja vastaskonto. Kui registreeritud kanne on ettemaks, valige selle **ettemaks** ruut selle **makse** vahekaart. Aastal ning **esindaja** valdkonnas rühma, täitke väljad nagu sa Slip tööleheridade printimiseks on **raha** aruande. Päevikukannete Updatehagi paani, klõpsake nuppu **Valideeri**.

## <a name="cash-transaction-approval-and-posting"></a>Sularaha tehingu kinnitamine ja sisestamine
Sularahatehingu, saab kasutada alljärgnevat staatust: **ükski**, **kinnitatud**, **kinnitatud**, ja **hüljatud**. A **Kasuta kinnitatud olekut** parameeter on **heakskiidu** FastTab ja selle **raha** tab kell **raha haldamise**&gt;**Setup**&gt;**raha ja pangakontod parameetrid** saate aktiveerida kaks täiendavat olekut: **kinnitatud** ja **hüljatud**. Kinnitus on asjakohane, kui väljastatakse sularaha ja raha laekumine või kulud jagavad kaks töötajat: raamatupidaja ja kassapidaja. Selle **oleku lähtestamise** funktsioon muudab praegune olek. **Tunnustatud** saab **kinnitatud**, ja **kinnitatud** saab **pole**. Raha päevikukannete saab redigeerida ainult siis, kui olek on **pole**. Sularahatehingud saab lükata ainult siis, kui olek on **kinnitatud**. Dokumendid on kantud raha tagasi selle **raha dokumentide registreerimise tööleht** aruande, kuid nad ei ole kajastatud ning **Kassa** aruande. Tehingu kinnitamiseks valige vastava saatelehe töölehe rea, ja klõpsake **dokumendid heakskiitmise**&gt;**kinnitus**. Tellimuse number luuakse vastavalt määratud numbriseeria. Kannete olek muudetakse **kinnitatud**, ja te saate enam töölehe rea. Konto saldo jääb samaks. Raha dokumendi keeldumiseks klõpsake **dokumendid heakskiitmise**&gt;**tagasi**. See suvand on saadaval ainult dokumendid, mis on **kinnitatud** staatus. Tehingu kinnitamiseks valige vastava saatelehe töölehe rea, ja klõpsake **dokumendid heakskiitmise**&gt;**kinnitamine**. Selle **kinnitatud** olek näitab, et rahalised vahendid, mis on saadud või tühjaks saamas. Selle saldo muutmisel. Sularaha tehingu konteerimist. Tühistada on **kinnitatud** olek ja et oleku lähtestamise **puudub**, klõpsake **dokumendid heakskiitmise**&gt;**oleku lähtestamise**. Ainult kinnitatud kanded sisestatakse raha. Žurnaali konteerimiseks klõpsake nuppu **Post**&gt;**Post**.

## <a name="print-a-cash-order"></a>Prindi kassa järjekorras
Sularaha tellimuse printimiseks valige Slip žurnaalirealt ja Updatehagi paani, klõpsake **printida**&gt;**Kassaorderi aruanne**. Kassa korvamisorderi või Kassa väljaminekuorderi, sõltuvalt sellest, kas summa on kantud trükkimise vorm loob süsteem selle **deebet** välja ning või **krediidi** välja valitud rea:

-   Kui on vastav summa on **deebet** välja: raha korvamisorderi
-   Kui on vastav summa on **krediidi** välja: raha väljaminekuorderi

Saatelehe töölehe read, mis on **kinnitatud**, **kinnitatud**, või **hüljatud** olek saate printida. Saate printida Kassa järjekorras dokumentide **raha ja pangakontod juhtimise**&gt;**Inquires ja aruanded**&gt;**sularaha tellimuse**.

## <a name="periodic-tasks"></a>Perioodilised ülesanded
Järgmisi ülesandeid saab täita kell **raha ja pangakontod juhtimise**&gt;**perioodilisi toiminguid**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Perioodiline ülesanne</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kontrolli saldolimiiti</td>
<td>Kontrollige valitud Kassa konto saldo määratud kuupäeval ja teate tulemuste kuvamine. Saldo arvutamisel võib arvestada ainult kinnitatud kanded. Märgitud on <strong>palgaarvestuse</strong> ei peeta.</td>
</tr>
<tr class="even">
<td>Kassasaldo ümberarvutamine</td>
<td>Kasutage selle tööülesande pearaamatusaldod Sularahakontode puhul sobivad kassajäägi.</td>
</tr>
<tr class="odd">
<td>Sularaha (ainult Poola) aruande loomine</td>
<td>Loomine on <strong>raha</strong> aruande. Selle <strong>raha</strong> aruande number luuakse numbriseeria jaoks seadistatud vastavalt <strong>aruande number</strong>. Dialoogis kasti ülesande, mis on <strong>seni</strong>, määrata viimase kuupäeva, mis raha tehingud tuleks arvestada selle <strong>raha</strong> aruande. Kasutamine ning <strong>Filter</strong> funktsiooni ning <strong>kaasamiseks</strong> vahekaarti, et määrata täiendavad kriteeriumid, et piirata sularaha tehingute valikul. Need kriteeriumid võivad sisaldada raha numbrite ja valuutatähiste. Aastal ning <strong>loomiseks</strong> number, kasutaja, kes vastutab aruande loomine. Kuvamiseks on <strong>raha</strong> aruande, mis on loodud kasutamiseks on <strong>sularaha aruannete</strong> nupuga selle <strong>raha kontode</strong> lehekülg.</td>
</tr>
<tr class="even">
<td>Raha - Exchange korrigeerimine FIFO ja LIFO (ainult Poola) puhul</td>
<td>Arvutada valuutakursi korrigeerimise Poola standardite kohta. Kasutamine ning <strong>Filter</strong> funktsiooni ning <strong>kaasamiseks</strong> vahekaarti, et määrata raha konto käivitada ülesanne. Valige selle <strong>ümberarvutamine</strong> ruut Valuutakursi erinevuse korrigeerimise täielik ümberarvutus kõigi avatud perioodide teha. Siin on valuutakursi korrigeerimise arvutamine kui esmalt FIFO, esimene ja Viimane, esimene LIFO meetodid on kasutatud:
<ul>
<li><strong>FIFO meetod</strong> – kulude kanne, mis on varasema kande kuupäev (väiksem järjekorranumber) elama sissetulekukanne, mis on varasema kande kuupäev (väiksem järjekorranumber) otsib süsteem.</li>
<li><strong>LIFO meetod</strong> – otsib süsteem kulude kanne, mis on tehingu hiljem (suurema järjekorranumber) elama sissetulekukanne, mis on tehingu hiljem (suurema tellimuse number).</li>
</ul>
Tasakaalustatud summa kajastub on <strong>tasakaalustatud valuuta</strong> kohta välja selle <strong>raha tehingu</strong> lehel. Kui valuutakursi korrigeerimise vahe, summa kajastub selle <strong>vahetuskursi korrigeerimise summa</strong> välja ja tehingu on <strong>valuutakursi erinevusi</strong> dokumendi tüüp on loodud ning <strong>sularaha tehingu</strong> tabel. Kasumi/kahjumi kannete pearaamatukontodele määratakse selle <strong>valuuta</strong> tabelis (<strong>valuutakursi finantskasum</strong> ja <strong>valuutakursi finantskahjum</strong>).</td>
</tr>
<tr class="odd">
<td>Välisvaluuta ümberarvutamine – kassa</td>
<td>Selle ülesande abil on piisav saldo vaikevaluutas soetamisel kui toimingud on sisestatud välisvaluutas. Kasutamine ning <strong>Filter</strong> funktsiooni ning <strong>kaasamiseks</strong> vahekaarti, et määrata raha konto käivitada ülesanne. Ülesande dialoogiboksi kasutada selle <strong>olevast</strong> ja <strong>et valuuta</strong> välja, et määrata kande valuuta. Süsteem võrdleb summa valuutas, mis muudeti vahetuskursi abil valitud kuupäeval summa vaikevaluutas. (Välja arvatud eelmise valuutakursi korrigeerimise) kahe summa vahe on arvutatud valuutakursi korrigeerimine. Selleks loob heakskiidetud sularahatehinguid ning selle <strong>valuutakursi korrigeerimisel</strong> tüüp. Pearaamatusse koostatakse pearaamatu kontoga raha ja määratud pearaamatukonto <strong>realiseerimata kasum</strong> või <strong>realiseerimata kahjum</strong> ja selle <strong>valuuta</strong> tabel.</td>
</tr>
</tbody>
</table>

## <a name="inquiries-and-reports"></a>Päringud ja aruanded
| Päring või aruanne                             | Kirjeldus                                                                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sularahatehingud Vaata                        | Saatelehe töölehe rea, kasutada selle **päringute** nuppu Updatehagi paani saate pearaamatukandeid, sularahasaldo ja muud teavet.                                                                                  |
| Sularahakanne                              | Mine **raha ja pangakontod juhtimise**&gt;**päringute ja aruannete**&gt;**sularaha tehingud** raha kannete kuvamiseks. Kasutamine ning **Filter** funktsioon määrata täiendavad kriteeriumid, et piirata sularaha tehingute valikul. |
| (Eesti, Venemaa) puhul registreerimise tööleht | Raporti **raha ja pangakontod juhtimise**&gt;**päringute ja aruannete**&gt;**registreerimise tööleht** peegeldab Kassa ja kassa Väljaminekuorderid, mis on välja antud.                                   |
| Kassaraamatu (puhul Läti, Leedu, Venemaa)     | Raporti **raha ja pangakontod juhtimise**&gt;**päringute ja aruannete**&gt;**raha Broneeri aruanne** kajastab tegelikku raha fondi liikumiste (tulusid ja kulusid).                                                            |




