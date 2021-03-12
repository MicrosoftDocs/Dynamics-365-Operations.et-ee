---
title: Väikesed summad Ida-Euroopa ja Venemaa puhul
description: Selles teemas antakse teavet väikeste summade funktsiooni kohta, mis võimaldab Eestis, Leedus, Tšehhi Vabariigis, Ungaris, Lätis, Poolas ja Venemaal asuvatel kasutajatel kajastada süsteemis sularahatehinguid.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCashBalance, RCashCountStatementForm, RCashPosting, RCashRemainLimit, RCashReportJour_PL, RCashTable, RCashTableBalance, RCashTableCredLimit, RCashTableLastRevaluation, RCashTableTransactions, RCashTrans
audience: Application User
ms.reviewer: kfend
ms.custom: 268504
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: c22da535afeeb7e57c19ecc2c4f221be1e124da3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5002862"
---
# <a name="petty-cash-for-eastern-europe-and-russia"></a>Väikesed summad Ida-Euroopa ja Venemaa puhul

[!include [banner](../includes/banner.md)]

Selles teemas antakse teavet väikeste summade funktsiooni kohta, mis võimaldab Eestis, Leedus, Tšehhi Vabariigis, Ungaris, Lätis, Poolas ja Venemaal asuvatel kasutajatel kajastada süsteemis sularahatehinguid.

Väikeset summade funktsioon võimaldab automatiseerida sularahasissetulekute ja -kulude toiminguid, põhidokumentide loomist ja seotud aruannete printimist. Väikeste summade funktsioon võimaldab teha järgmist.

-   Arvestada saadaoleva sularaha sissetulekuid ja kulusid.
-   Luua tüüpilisi sularahavorme: sularaha korvamisorderid, sularaha väljaminekuorderid ja sularahaorderite registreerimiste tööleht.
-   Juhtida maksimaalset sularahasummat, mis on klientide, hankijatega jne tehtavate toimingute puhul lubatud.
-   Kajastada süsteemis sularahatoiminguid erinevates valuutades.
-   Teisendada sularahatoimingute välisvaluutas summasid vaikevaluutasse ja esitada raamatupidamise aruandeid.
-   Luua **kassaraamatu** ja kassapidaja aruandeid.

## <a name="prerequisites"></a>Eeltingimused
Väikeste summade funktsiooni kasutamiseks peate täitma järgmised eeltingimused.

-   Seadistama sularahakontod.
-   Seadistama sularahakonto sisestusreeglid.
-   Seadistama kassadokumentide numbriseeriad.
-   Seadistama sularaha- ja pangahalduse parameetrite vaikeväärtused.
-   Seadistama pearaamatus sularahatöölehtede nimed.

### <a name="set-up-cash-accounts"></a>Sularahakontode seadistamine

Sularahakonto seadistamiseks avage **Sularaha- ja pangahaldus** &gt; **Pangakontod** &gt; **Sularahakontod** ja sisestage järgmine teave.

| Väli                 | Kirjeldus                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------|
| Sularaha                  | Sisestage kood sularahakonto (kassa) tuvastamiseks.                                                                    |
| Nimi                  | Sisesta sularahakonto kirjeldus                                                                             |
| Valuuta              | Valige sularahatehingute vaikevaluutakood.                                                              |
| Numbriseeria grupp | Kui kassadokumentide numeratsioon peab erinema parameetrites määratud numeratsioonist, sisestage kood. |
| Veel valuutasid       | Märkige see ruut, et võimaldada arvestusvaluutast erinevate valuutade sisestamist.                     |
| Negatiivne kassa         | Märkige see ruut, et võimaldada mis tahes valuutas negatiivseid sularahasaldosid.                                               |

Sularahakonto puhul sularahasaldo juhtimise reeglite seadistamiseks valige sularahasaldo ja seejärel klõpsake toimingupaanil vahekaardi **Sularahakonto** rühmas **Saldolimiit** valikut **Saldolimiit**. Sisestage järgmine teave.

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
<td>Valige valuuta tüüp.
<ul>
<li><strong>Arvestusvaluuta</strong> – saate kasutada ettevõtte põhivaluutakoodi.</li>
<li><strong>Näidatud valuuta</strong> – saate kasutada ettevõtte põhivaluutakoodist erinevat valuutakoodi.</li>
</ul></td>
</tr>
<tr class="even">
<td>Valuuta</td>
<td>Kui tegite väljal <strong>Valuuta tüüp</strong> valiku <strong>Näidatud valuuta</strong>, valige valuutakood. See väli pole saadaval, kui tegite väljal <strong>Valuuta tüüp</strong> valiku <strong>Arvestusvaluuta</strong>.</td>
</tr>
<tr class="odd">
<td>Saldolimiidi tüüp</td>
<td>Valige üks saadaolevatest väärtustest.
<ul>
<li><strong>Maksimaalne</strong> – sularahasaldo ei tohi ületada sularahakonto summat <strong>Saldolimiit</strong> (ülapiir).</li>
<li><strong>Minimaalne</strong> – sularahasaldo ei tohi langeda alla sularahakonto summat <strong>Saldolimiit</strong> (alapiir).</li>
</ul></td>
</tr>
<tr class="even">
<td>Kontrolli saldolimiiti</td>
<td>Valige, mis juhtub kassadokumentide heakskiiduprotsessi ajal, kui sularahakonto puhul ületatakse summa <strong>Saldolimiit</strong>.
<ul>
<li><strong>Aktsepteeri</strong> – limiidi saab ületada.</li>
<li><strong>Hoiatus</strong> – limiidi saab ületada, kuid kasutaja saab hoiatusteate. Kassadokument kinnitatakse või kiidetakse heaks.</li>
<li><strong>Tõrge</strong> – limiiti ei saa ületada. Kasutaja saab tõrketeate ja kassadokumenti ei kinnitata või ei kiideta heaks.</li>
</ul>
Lisateavet kassadokumentide heakskiiduprotsessi kohta vt selle teema allpool olevast teemast &quot;Sularahakande kinnitamine ja sisestamine&quot;.</td>
</tr>
<tr class="odd">
<td>Saldolimiit</td>
<td>Sisestage sularahakonto saldolimiit. Summa tuleb sisestada teie määratud valuutas.</td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-posting-profiles"></a>Sularahakonto sisestusreeglite seadistamine

Sularahakonto sisestusreeglid määratlevad sisestused pearaamatusse. Sularahakonto sisestusreeglite seadistamiseks avage **Sularaha-** **ja pangahaldus** &gt; **Seadistus** &gt; **Sularahakonto sisestusreeglid** ning valige või looge sisestusreeglid. Sisestage järgmine teave.

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
<td>Valige, kas sisestusreegleid rakendatakse kindlale sularahakontole või kõigile sularahakontodele.
<ul>
<li><strong>Tabel</strong> – kui sularahakonto jaoks on sisestusreeglite rida olemas, kasutatakse seda rida sularahakannete sisestamiseks.</li>
<li><strong>Kõik</strong> – sularahakonto jaoks sisestusreeglite rida puudub.</li>
</ul></td>
</tr>
<tr class="even">
<td>Sularaha</td>
<td>Kui tegite väljal <strong>Kehtib</strong> valiku <strong>Tabel</strong>, määrake sularahakonto. See väli jääb tühjaks, kui tegite väljal <strong>Kehtib</strong> valiku <strong>Kõik</strong>.</td>
</tr>
<tr class="odd">
<td>Pearaamatukonto</td>
<td>Sisestage selle pearaamatukonto number, mida kasutatakse sularahakonto puhul kliendi koondkontona.</td>
</tr>
</tbody>
</table>

### <a name="set-up-number-sequences-for-cash-documents"></a>Kassadokumentide numbriseeriate seadistamine

Kassadokumentide numbriseeriate seadistamiseks avage **Sularaha- ja pangahaldus** &gt; **Seadistus** &gt; **Sularaha- ja pangahalduse parameetrid**. Vahekaardil **Numbriseeria** määrake numbriseeria koodid dokumentidele **Kassa korvamisorderid**, **Kassa väljaminekuorderid**, **Kassa paranduskanne** ja **Valuutakursi korrigeerimine** ning väljale **Sularahaaruande number**.

### <a name="set-up-default-values-for-cash-and-bank-management-parameters"></a>Sularaha- ja pangahalduse parameetrite vaikeväärtuste seadistamine.

Sularaha- ja pangahalduse parameetrite vaikeväärtuste seadistamiseks väikeste summade funktsiooni jaoks avage **Sularaha- ja pangahaldus** &gt; **Seadistus** &gt; **Sularaha- ja pangahalduse parameetrid**. Vahekaardil **Sularaha** sisestage järgmine teave.

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
<td>Valige töölehtedel kasutatav vaikesularahakonto.</td>
</tr>
<tr class="even">
<td>Kassaseisu sisestamine</td>
<td>Sisestage sularahakonto vaikesisestusreeglid, mida kasutatakse, kui muid sisestusreegleid pole määratud.</td>
</tr>
<tr class="odd">
<td>Kontrolli kasutatud kannet</td>
<td>Valige, mis juhtub, kui kassadokumendi numbri kontrollimisel leitakse topeltnumbrid.
<ul>
<li>Lükka duplikaat tagasi</li>
<li>Ära luba koopiaid samal rahandusaastal</li>
<li>Luba duplikaate</li>
<li>Hoiata duplikaatide korral</li>
</ul></td>
</tr>
<tr class="even">
<td>Kontrolli toimingute limiiti</td>
<td>Määrake, mis juhtub, kui vastaspooltega tehtavate toimingute piirmäär on ületatud.
<ul>
<li><strong>Aktsepteeri</strong> – limiidi saab ületada.</li>
<li><strong>Hoiatus</strong> – limiidi saab ületada, kuid kasutaja saab hoiatusteate. Toiming sisestatakse.</li>
<li><strong>Tõrge</strong> – limiiti ei saa ületada. Kasutaja saab tõrketeate ja toimingut ei sisestata.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Kontrollimeetod</td>
<td>Valige kontrollimismeetod, mida kasutatakse toimingute piirsummade ületamise juhtimiseks.
<ul>
<li><strong>Toiming</strong> – kontrollitakse iga kannet.</li>
<li><strong>Leping</strong> – kontrollitakse iga tehingut, millel on vastaspoolega määratud leping.</li>
</ul></td>
</tr>
<tr class="even">
<td>Toimingute limiit</td>
<td>Sisestage maksimaalne summa, mis on vastaspooltega tehtavate sularahatoimingute puhul lubatud.</td>
</tr>
<tr class="odd">
<td>Sisestus varasemal kuupäeval</td>
<td>Märkige see ruut, et lubada sularahakannete sisestamine enne viimast sularahakande kuupäeva.</td>
</tr>
<tr class="even">
<td>Dimensioonid</td>
<td>Sisestage dimensioonid väljadele <strong>Osakonna kood</strong>, <strong>Analüütiline kood</strong> ja <strong>Eesmärgi kood</strong>. See teave kajastub kassadokumentide prindivormil.</td>
</tr>
<tr class="odd">
<td>Kasuta kinnitatud olekut</td>
<td>Märkige see ruut, et kasutada kassadokumentide kinnitusprotsessi käigus lisaolekut <strong>Kinnitatud</strong>. (Lisateavet vt teemast &quot;Sularahakannete kinnitamine ja sisestamine&quot;.)</td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-journal-names-in-general-ledger"></a>Pearaamatus sularahatöölehtede nimede seadistamine

Sularahakannete sisestamiseks töölehe loomiseks avage **Pearaamat** &gt; **Töölehe seadistamine** &gt; **Töölehtede nimed** ja looge uus kirje. Valige väljal **Töölehe tüüp** suvand **Sularaha**. Määratlege muud vajalikud töölehe vaikeparameetrid.

## <a name="daily-cash-operations-via-a-slip-journal"></a>Igapäevased sularahatoimingud saatelehe töölehe kaudu
Kassadokumendi loomiseks saatelehe töölehe kaudu avage **Sularaha- ja pangahaldus** &gt; **Sularahakanded** &gt; **Saatelehe tööleht** ning looge uus tööleht. Klõpsake toimingupaanil valikut **Read**. Lisage uus rida ja sisestage järgmine teave.

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
<td>Valige sularahakonto. Vaikimisi määratakse sularahakonto sularaha- ja pangahalduse parameetrites.</td>
</tr>
<tr class="odd">
<td>Kirjeldus</td>
<td>Sisestage kande jaoks selgitav tekst.</td>
</tr>
<tr class="even">
<td>Deebet, kreedit</td>
<td>Sisestage kassadokumendi summa ühele järgmistest väljadest.
<ul>
<li><strong>Deebet</strong> – kasutage seda välja kassa sissetuleku- ja väljaminekuorderite registreerimiseks.</li>
<li><strong>Kreedit</strong> – kasutage seda välja kassa kulu- ja väljaminekuorderite registreerimiseks.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vastaskonto tüüp, vastaskonto</td>
<td>Valige vastaskonto tüüp ja vastaskonto number.</td>
</tr>
<tr class="even">
<td>Valuuta</td>
<td>Valige kande valuutakood.</td>
</tr>
<tr class="odd">
<td>Kanne</td>
<td>See väli täidetakse automaatselt töölehe seadistuse põhjal.</td>
</tr>
<tr class="even">
<td>Tellimuse kood</td>
<td>Kui sularahakonto jaoks pole muid numbriseeriaid seadistatud, täidetakse see väli automaatselt parameetrites määratud numbriseeria põhjal. Saate sellele väljale sisestada soovi korral tellimuse numbri käsitsi. Kassadokumentide numeratsiooni ebajärjekindluse vältimiseks rakendatakse järgmist reeglit: varasema toimingukuupäevaga kassadokumendi number ei saa olla suurem kui hilisema toimingukuupäevaga kassadokumendi number. Kui te ei soovi seda reeglit rakendada, märkige sularaha- ja pangahalduse parameetrites ruut <strong>Sisestamine varasemal kuupäeval</strong>.</td>
</tr>
<tr class="odd">
<td>Kinnitamise olek</td>
<td>Esimese kande olek on <strong>Pole</strong>. Teavet kande oleku määramise kohta vt teemast &quot;Sularahakannete kinnitamine ja sisestamine&quot;.</td>
</tr>
<tr class="even">
<td>Dokumendi tüüp </td>
<td>See väli vahekaardil <strong>Kassaorder</strong> täidetakse automaatselt kassadokumenti sisestatud summa põhjal.
<ul>
<li><strong>Kassa korvamisorder</strong> – seda väärtust kasutatakse, kui sisestasite summa sularahakonto väljale <strong>Deebet</strong>.</li>
<li><strong>Kassa väljaminekuorder</strong> – seda väärtust kasutatakse, kui sisestasite summa sularahakonto väljale <strong>Kreedit</strong>.</li>
<li><strong>Parandus</strong> – olete sisestanud sularahakonto väljale <strong>Deebet</strong> või <strong>Kreedit</strong> negatiivse summa.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Käibemaksugrupp</td>
<td>Määrake käibemaksugrupp toimingu maksude arvutamiseks.</td>
</tr>
<tr class="even">
<td>Kauba käibemaksugrupp</td>
<td>Määrake kauba käibemaksugrupp toimingu maksude arvutamiseks.</td>
</tr>
<tr class="odd">
<td>Põhjus</td>
<td>Sisestage vahekaardil <strong>Kassaorder</strong> kande teemat kirjeldav tekst. See tekst prinditakse kassaorderi aruandlusvormile.</td>
</tr>
<tr class="even">
<td>Dokumendi kuupäev</td>
<td>Sisestage kande põhjuseks oleva põhidokumendi (nt ettemaksuaruanded, arve või tellimus) kirjeldus, number ja kuupäev.</td>
</tr>
<tr class="odd">
<td>Esindaja tüüp</td>
<td>See väli võib sisaldada üht järgmistest väärtustest.
<ul>
<li><strong>Töötaja</strong> – otsing <strong>Esindaja</strong> sisaldab töötajate loendit, kui väljal <strong>Vastaskonto</strong> on valitud <strong>Pearaamat</strong> või <strong>Pank</strong>, või vastaspoole kontaktisikute loendit, kui väljal <strong>Vastaskonto</strong> on valitud <strong>Klient</strong> või <strong>Hankija</strong>. Esindajate seadistamiseks avage <strong>Põhiline</strong> &gt; <strong>Seadistus</strong> &gt; <strong>Kontaktid</strong> &gt; <strong>Kontaktisik</strong>.</li>
<li><strong>Muu</strong> – otsing <strong>Esindaja</strong> sisaldab muude klientide loendit. Saajate, keda tabelis <strong>Kliendid</strong> või <strong>Hankijad</strong> ei kuvata, seadistamiseks avage <strong>Pearaamat</strong> &gt; <strong>Saajad</strong>. See tüüp on saadaval ainult Läti puhul. (Konfiguratsioonivõti <strong>CSELatvia</strong> peab olema lubatud.)</li>
<li><strong>Hankija</strong> – otsing <strong>Esindaja</strong> sisaldab hankijate loendit. Hankijate seadistamiseks avage <strong>Ostureskontro</strong> &gt; <strong>Hankijad</strong>.</li>
<li><strong>Klient</strong> – otsing <strong>Esindaja</strong> sisaldab klientide loendit. Klientide seadistamiseks avage <strong>Müügireskontro</strong> &gt; <strong>Kliendid</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Esindaja</td>
<td>Valige esindaja, kelle tüübi määrasite väljal <strong>Esindaja tüüp</strong>.</td>
</tr>
<tr class="odd">
<td>Inimese nimi</td>
<td>See väli täidetakse automaatselt väljade <strong>Vastaskonto</strong> ja <strong>Esindaja</strong> põhjal. See teave kajastub kassaorderite prindivormil.</td>
</tr>
<tr class="even">
<td>ID-kaart</td>
<td>See väli täidetakse automaatselt kontaktisiku (esindaja) ID-kaardi andmete põhjal. Kui väljal <strong>Vastaskonto tüüp</strong> on valitud <strong>Avansisaaja</strong> ja väli <strong>Vastaskonto</strong> on määratud töövõtja koodile, saab kassaordereid või kulusid teha töövõtjalt või töövõtjale. Sellisel juhul täidetakse väli <strong>ID-kaart</strong> automaatselt, kasutades ID-kaardi andmeid tabelist <strong>Töövõtja</strong> (<strong>Personaliarvestus</strong> &gt; <strong>Töövõtjate tabel</strong>).</td>
</tr>
<tr class="odd">
<td>Eesmärk</td>
<td>Tabelis <strong>Eesmärk</strong> saate määratleda kande summa ühe või mitu sihtkoodi. Valige sihtkood väljal <strong>Eesmärk</strong> ja sisestage selgitus väljale <strong>Kande tekst</strong>. Sisestage väljale <strong>Summa</strong> summa kandevaluutas. Väljal <strong>Protsent</strong> kuvatakse sihtsumma ja kande kogusumma suhe protsentides.</td>
</tr>
<tr class="even">
<td>Jääk</td>
<td>Arvutatud järelejäänud summa. Pange tähele, et kande kogusumma tuleb määrata sihtkoodidele.</td>
</tr>
<tr class="odd">
<td>Ametiisikud</td>
<td>Vahekaardil <strong>Ametiisikud</strong> saate määrata vastutavate isikute (direktor, pearaamatupidaja ja kassiir) nimed ja ametinimetused. Välja <strong>Ametikoht</strong> väärtused määratletakse ametiisikute seadistusega lehe <strong>Ametiisikud</strong> vahekaartidel <strong>Üldine</strong> ja <strong>Pearaamat</strong> (<strong>Põhiline</strong> &gt; <strong>Seadistus</strong> &gt; <strong>Kontaktid</strong> &gt; <strong>Ametiisikud</strong>).</td>
</tr>
<tr class="even">
<td>Ettemaks</td>
<td>Märkige see ruut, kui kanne on ettemakse.</td>
</tr>
<tr class="odd">
<td>Sisestusreeglid</td>
<td>Saate sisestada sularahakonto sisestusreeglid. Vaikimisi kasutatakse sularaha- ja pangahalduse parameetrites määratud sisestusreegleid.</td>
</tr>
<tr class="even">
<td>Vastaskontoga sisestamise reeglid</td>
<td>Saate sisestada valitud vastaskonto sisestusreeglid.</td>
</tr>
<tr class="odd">
<td>Kogusumma</td>
<td>Lehe alaosas asuvas väljagrupis <strong>Kogusumma</strong> oleval väljal <strong>Korv.</strong> kuvatakse kogusumma, mis arvutatakse kõigi praegusele töölehele sisestatud kassa korvamisorderite kohta, ning väljal <strong>Väljam.</strong> kuvatakse kõigi kassa väljaminekuorderite kogusumma.</td>
</tr>
</tbody>
</table>

Töölehekannete vaatamiseks klõpsake toimingupaanil nuppu **Kinnita**.

## <a name="daily-cash-operations-via-a-general-journal"></a>Igapäevased sularahatoimingud päevaraamatu töölehe kaudu
Sularahakannete loomiseks pearaamatu töölehe kaudu avage **Pearaamat** &gt; **Töölehe sisestused** &gt; **Päevaraamatud** ja looge uus tööleht. Klõpsake toimingupaanil valikut **Read**. Lisage uus rida ja sisestage järgmine teave.

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
<td>Valige <strong>Väikesed summad</strong>.</td>
</tr>
<tr class="odd">
<td>Konto</td>
<td>Valige sularahakonto number.</td>
</tr>
<tr class="even">
<td>Kande tekst</td>
<td>Sisestage kande jaoks selgitav tekst.</td>
</tr>
<tr class="odd">
<td>Deebet, kreedit</td>
<td>Sisestage kassadokumendi summa ühele järgmistest väljadest.
<ul>
<li><strong>Deebet</strong> – kasutage seda välja kassa sissetuleku- ja väljaminekuorderite registreerimiseks.</li>
<li><strong>Kreedit</strong> – kasutage seda välja kassa kulu- ja väljaminekuorderite registreerimiseks.</li>
</ul></td>
</tr>
<tr class="even">
<td>Vastaskonto tüüp, vastaskonto</td>
<td>Valige vastaskonto tüüp ja vastaskonto number.</td>
</tr>
<tr class="odd">
<td>Valuuta</td>
<td>Valige kande valuutakood.</td>
</tr>
</tbody>
</table>

Vahekaardil **Arve** saate määrata valitud konto ja vastaskonto sisestusreeglid. Kui registreeritud kanne on ettemakse, märkige ruut **Ettemakse** vahekaardil **Makse**. Täitke väljagrupis **Esindaja** väljad, nagu saatelehe töölehtede puhul, et printida välja aruanne **Sularaha**. Töölehekannete vaatamiseks klõpsake toimingupaanil nuppu **Kinnita**.

## <a name="cash-transaction-approval-and-posting"></a>Sularahakande kinnitamine ja sisestamine
Sularahakannete puhul saab rakendada järgmisi olekuid: **Pole**, **Kinnitatud**, **Heaks kiidetud**, **Tagasi lükatud**. Parameeter **Kasuta kinnituse olekut** vahekaardi **Sularaha** kiirkaardil **Kinnitamine** (**Sularaha- ja pangahaldus** &gt; **Seadistus** &gt; **Sularaha- ja pangahalduse parameetrid**) võimaldab aktiveerida kaks lisaolekut: **Kinnitatud** ja **Tagasi lükatud**. Kinnitus on asjakohane, kui kassadokumendid on väljastatud ning kaks töövõtjat – raamatupidaja ja kassiir – kasutavad ühiselt kassaordereid või kulusid. Funktsioon **Lähtesta olek** muudab kande praegust olekut. Olek **Heaks kiidetud** muutub olekuks **Kinnitatud** ja olek **Kinnitatud** muutub olekuks **Pole**. Sularahatöölehe sisestusi saab redigeerida ainult siis, kui olek on **Pole**. Sularahakandeid saab tagasi lükata ainult siis, kui kande olek on **Kinnitatud**. Tagasi lüktatud kassadokumendid kaasatakse aruandesse **Kassadokumentide registreerimise tööleht**, kuid need ei kajastu aruandes **Kassaraamat**. Kande kinnitamiseks valige vastav saatelehe töölehe rida ja klõpsake valikuid **Dokumentide heakskiitmine** &gt; **Kinnita**. Luuakse tellimuse number, võttes aluseks määratud numbriseeria. Kande olekuks muutub **Kinnitatud** ja töölehe rida ei saa enam redigeerida. Sularahakonto saldo jääb muutumatuks. Kassadokumendi tagasilükkamiseks klõpsake valikuid **Dokumentide heakskiitmine** &gt; **Lükka tagasi**. See suvand on saadaval ainult dokumentide puhul, mille olek on **Kinnitatud**. Kande heakskiitmiseks valige vastav saatelehe töölehe rida ja klõpsake valikuid **Dokumentide heakskiitmine** &gt; **Kiida heaks**. Olek **Heaks kiidetud** näitab, et sularaha on vastu võetud või kulutatud. Kassasaldo on muutunud. Sularahakannet saab sisestada. Oleku **Heaks kiidetud** tühistamiseks ja ennistamiseks väärtusele **Pole** klõpsake valikuid **Dokumentide heakskiitmine** &gt; **Lähtesta olek**. Sisestada saab ainult heakskiidetud sularahakandeid. Töölehe sisestamiseks klõpsake valikuid **Sisesta** &gt; **Sisesta**.

## <a name="print-a-cash-order"></a>Kassaorderi printimine
Kassaorderi printimiseks valige saatelehe töölehe rida ja seejärel klõpsake toimingupaanil valikuid **Prindi** &gt; **Kassaorderi aruanne**. Süsteem loob prindivormi kas kassa korvamisorderi või kassa väljaminekuorderi kohta olenevalt sellest, kas summa on sisestatud valitud real väljale **Deebet** või **Kreedit**.

-   Kui summa on väljal **Deebet**: kassa korvamisorder
-   Kui summa on väljal **Kreedit**: kassa väljaminekuorder

Printida saab saatelehe töölehe ridu, mille olek on **Kinnitatud**, **Heaks kiidetud** või **Tagasi lükatud**. Samuti saate printida kassaorderi dokumente jaotises **Sularaha- ja pangahaldus** &gt; **Päringud ja aruanded** &gt; **Kassaorder**.

## <a name="periodic-tasks"></a>Perioodilised ülesanded
Jaotises **Sularaha- ja pangahaldus** &gt; **Perioodilised ülesanded** saab teha järgmist.

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
<td>Saate kontrollida valitud sularahakonto saldot määratud kuupäeval ja kuvada tulemuse teabesõnumis. Saldoarvutusse saab kaasata ainult heakskiidetud kandeid. Kandeid märkega <strong>Palgaarvestuseks</strong> arvesse ei võeta.</td>
</tr>
<tr class="even">
<td>Kassasaldo ümberarvutamine</td>
<td>Selle ülesandega saate kontrollida, kas sularahakontode pearaamatusaldod vastavad sularahasaldole.</td>
</tr>
<tr class="odd">
<td>Sularahaaruande loomine (ainult Poola puhul).</td>
<td>Looge aruanne <strong>Sularaha</strong>. Aruande <strong>Sularaha</strong> number luuakse suvandi <strong>Aruande number</strong> jaoks seadistatud numbriseeria põhjal. Määrake ülesande dialoogiboksis väljal <strong>Tähtaeg</strong> viimane kuupäev, mille sularahakandeid tuleb aruandes <strong>Sularaha</strong> arvesse võtta. Määrake vahekaardi <strong>Kaasatavad kirjed</strong> funktsiooniga <strong>Filtreeri</strong> lisakriteeriumid sularahakannete valiku piiramiseks. Need kriteeriumid võivad sisaldada sularahakontode numbreid ja valuutakoode. Valige väljal <strong>Looja</strong> aruande koostamise eest vastutav kasutaja. Loodud aruande <strong>Sularaha</strong> vaatamiseks kasutage lehel <strong>Sularahakontod</strong> olevat nuppu <strong>Sularahaaruanded</strong>.</td>
</tr>
<tr class="even">
<td>Kassa – valuutakursi korrigeerimine, FIFO ja LIFO (ainult Poola puhul)</td>
<td>Arvutage valuutakursi korrigeerimine Poola standardite alusel. Määrake vahekaardi <strong>Kaasatavad kirjed</strong> funktsiooniga <strong>Filtreeri</strong> sularahakonto, mille kohta ülesanne kävitada. Märkige ruut <strong>Ümberarvutus</strong> valuutakursi korrigeerimise erinevuse ümberarvutamiseks kõigi avatud perioodide puhul. Kaubavarude hinna määramise FIFO-meetodi (esimesena sisse, esimesena välja) ja kaubavarude hinna määramise LIFO-meetodi (viimasena sisse, esimesena välja) kasutamisel arvutatakse valuutakursi korrigeerimine järgmiselt.
<ul>
<li><strong>FIFO-meetod</strong>– süsteem otsib varasema kandekuupäevaga (väiksema tellimuse numbriga) kulukannet ja tasakaalustab selle varasema kandekuupäevaga (väiksema tellimuse numbriga) sissetulekukandega.</li>
<li><strong>LIFO-meetod</strong>– süsteem otsib hilisema kandekuupäevaga (suurema tellimuse numbriga) kulukannet ja tasakaalustab selle hilisema kandekuupäevaga (suurema tellimuse numbriga) sissetulekukandega.</li>
</ul>
Tasakaalustatud summa kajastub lehe <strong>Sularahakanne</strong> väljal <strong>Tasakaalustatud valuuta</strong>. Valuutakursi korrigeerimise erinevuse korral kajastub summa väljal <strong>Valuutakursi korrigeerimise summa</strong> ja tabelis <strong>Sularahakanne</strong> luuakse kanne dokumenditüübita <strong>Valuutakursi erinevus</strong>. Kasumi/kahjumi kannete pearaamatukontod määratakse tabelis <strong>Valuuta</strong> (<strong>Valuutakursi finantskasum</strong> ja <strong>Valuutakursi finantskahjum</strong>).</td>
</tr>
<tr class="odd">
<td>Välisvaluuta ümberarvutamine – kassa</td>
<td>Saate selle ülesande abil tagada aruandluskuupäeval piisava saldo vaikevaluutas, kui toimingud on sisestatud välisvaluutades. Määrake vahekaardi <strong>Kaasatavad kirjed</strong> funktsiooniga <strong>Filtreeri</strong> sularahakonto, mille kohta ülesanne kävitada. Määrake ülesande dialoogiboksis väljade <strong>Lähtevaluuta</strong> ja <strong>Sihtvaluuta</strong> abil kande valuutad. Süsteem võrdleb valitud kuupäeva valuutakursi abil teisendatud valuuta summat vaikevaluuta summaga. Kahe summa vaheline erinevus (v.a eelmine valuutakursi korrigeerimine) on arvutatud valuutakursi korrigeerimine. See ülesanne loob heakskiidetud sularahakande tüübiga <strong>Valuutakursi korrigeerimine</strong>. Pearaamatu kanne koostamisel kasutatakse sularaha pearaamatukontot ja tabelis <strong>Valuuta</strong> väljal <strong>Realiseerimata kasum</strong> või <strong>Realiseerimata kahjum</strong> määratud pearaamatukontot.</td>
</tr>
</tbody>
</table>

## <a name="inquiries-and-reports"></a>Päringud ja aruanded

| Päringud või aruandlus                             | Kirjeldus                                                                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sularahakannete kuvamine                        | Saatelehe töölehe rea puhul kasutage pearaamatu kannete, sularahasaldo ja muu teabe kuvamiseks toimingupaani nuppu **Päringud**.                                                                                  |
| Sularahakanne                              | Sularahakannete kuvamiseks avage **Sularaha- ja pangahaldus** &gt; **Päringud ja aruanded** &gt; **Sularahakanded**. Määrake funktsiooniga **Filtreeri** lisakriteeriumid sularahakannete valiku piiramiseks. |
| Registreerimise tööleht (Eesti ja Venemaa puhul) | Aruanne jaotises **Sularaha- ja pangahaldus** &gt; **Päringud ja aruanded** &gt; **Registreerimise tööleht** kajastab kõiki väljastatud kassa korvamis- ja väljaminekuordereid.                                   |
| Kassaraamat (Läti, Leedu ja Venemaa puhul)     | Aruanne jaotises **Sularaha- ja pangahaldus** &gt; **Päringud ja aruanded** &gt; **Kassaraamatu aruanne** kajastab tegelikke sularahaliikumisi (sissetulekud ja kulud).                                                            |





