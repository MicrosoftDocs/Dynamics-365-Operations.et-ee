---
title: "SEPA kreeditiülekande ülevaade"
description: "Selles artiklis kirjeldatakse ISO 20022 kreeditkorraldusega, mis sisaldavad ühtse euromaksete piirkonna (SEPA) krediidi- ja muud elektroonilised maksed hankijatele. SEPA kreeditkorralduse on teatud tüüpi makse eurodes ühe ettevõtte või individuaalsete teisele äriühingule või üksikute. On samuti kirjeldatakse, kuidas luua ja edastada krediidi ülekanne makse faili."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11124
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 848df5e3898f37284d7746c59bff8b38d35ac883
ms.lasthandoff: 03/31/2017


---

# <a name="sepa-credit-transfer-overview"></a>SEPA kreeditiülekande ülevaade

Selles artiklis kirjeldatakse ISO 20022 kreeditkorraldusega, mis sisaldavad ühtse euromaksete piirkonna (SEPA) krediidi- ja muud elektroonilised maksed hankijatele. SEPA kreeditkorralduse on teatud tüüpi makse eurodes ühe ettevõtte või individuaalsete teisele äriühingule või üksikute. On samuti kirjeldatakse, kuidas luua ja edastada krediidi ülekanne makse faili.

## <a name="what-is-a-credit-transfer-message"></a>Mis on krediidi ülekande sõnum?
Krediidi ülekande sõnum on taotleda rahalisi vahendeid ise võlausaldajale saadab algatav pool (firma nimi). Sõnumeid on palju riigi-/ regioonikohaste ja konkreetse panga rakendusi, tehtud. Mõned neist kasutatakse ühe riigi, ja mõned on järjest standarditele. Üks hästi tõestatud ülemaailmne standard on ISO 20022 ja selle algatamise sõnumeid sh tehtud. Järgmine joonis kujutab suhete ja valitud krediidi sõnumite edastamise katte. 
![Laenu võtnud emaslooma](./media/credit-transfer.jpg) krediidi sõnumite edastamise\[/caption\] 

## <a name="what-are-iso-20022-and-sepa-payments"></a>Millised on ISO 20022, SEPA makseid?
Ühtse euromaksete piirkonna (SEPA) on määranud Euroopa Komisjon, kelle korraldusel tuleb kõiki elektroonilisi makseid käsitleda kodumaistena, olenemata riigist/piirkonnast, kus üksikisik, ettevõte või organisatsioon ja pank asuvad. Siseriiklikud maksed ja välismaksed on. Ühtse euromaksete piirkonna kuuluvad 28 liikmesriikide ning Euroopa Liidu (EL), ja ka Islandi, Liechtensteini, Norra, Šveits, Monaco, ja San Marino. SEPA aitab Euroopa majanduspiirkonnas (EMP) luua maksekannete jaoks ühtse turu. Lõppkokkuvõttes eeldatakse, et SEPA vähendab maksevormingute arvu, millega pangad, ettevõtted ja üksiksikud peavad tegelema. Euroopa Komisjon määras SEPA maksetele juriidilise aluse makseteenuste direktiiviga (PSD). Euroopa Maksenõukogu (EPC) toetab SEPA-d läbi järgmiste tegevuste.

-   See määrab SEPA elektrooniliste maksete standardid, kasutades ISO-20022 universaalse finantsvaldkonna sõnumiskeemi XML-vormingut.
-   See kehtestab euromaksete käsitsemise reeglid ja juhised.

EPC, mis koosneb Euroopa pankadest, arendab SEPA maksevahendite kaubandus- ja tehnilist raamistikku. Kasutatakse kolme SEPA maksete tüüpi.

-   Kreeditülekanded
-   Otsekorraldused
-   Kaardid

## <a name="what-is-a-sepa-credit-transfer"></a>Mis on SEPA kreeditülekanne?
SEPA kreeditülekanne on ühe ettevõtte või isiku makse teisele ettevõttele või isikule. Maksed peavad olema eurodes ja sisaldama mõlema osapoole puhul rahvusvahelist pangakonto numbrit (IBAN) ja panga koodi (BIC). (BIC on ka ülemaailmse pankadevahelise finantsinfo ühingu \[SWIFT\] koodi.) Lisaks peab tehingu kulude jaotuse vahelist suhtlust. Pooltevahelised kreeditülekanded peavad kasutama XML-faile, mis vastavad ISO 20022 maksete töötlemise standarditele ja XML-vormingule, nagu EPC on täpsustanud.

## <a name="how-is-a-credit-transfer-implemented"></a>Kuidas rakendatakse kreeditkorralduse?
Krediidi ülekanne makse vormi Euroopa riikides rakendatakse elektroonilise aruandluse (ER) ja tasumise funktsionaalsust meetodeid kasutades Dynamics 365 toiminguteks. Mõned krediidi ülekande formaadid, mida kasutatakse muudes piirkondades kasutada pärand makse raames. Hulgas paljud muud formaadid on kaksteist ISO 20022 krediidi ülekande failivormingud on saadaval. Need ekspordi vormingud vastavad SEPA ISO 20022 XML standardile. Neid kasutatakse muudes makseülekannete riigis kasutatakse ja SEPA krediidi Transfer kava reeglistik mis Patendikonventsiooni vabastab versioon 8.2 määratletud euromakseid loomiseks. Enne, kui te saaksite tehtud, pöörduge panga poole ja saada tarkvara, mis on vajalikud e-panganduse faile üles laadida. Kasutate tarkvara XML faile, mis sisaldavad maksekorraldusi panka.

## <a name="what-credit-transfer-formats-are-currently-supported-in-dynamics-365-for-operations"></a>Mis krediidi ülekande praegu formaate Dynamics 365 toimingute puhul?
Tuleks alati avage jagatud varade kogu Microsoft Dynamics elutsükli teenused (LCS) ning vaadata kõige uuemad saadaval vara tüüpi failide **GER konfiguratsiooni**. Järgmine lõik: "Mida ma pean luua?", antakse link teema, kus selgitatakse, kuidas luua LCS hoidla vaadata saadaolevaid konfiguratsioone ja importida valitud konfiguratsioonid.

## <a name="what-do-i-have-to-set-up"></a>Mida pean seadistamiseks tegema?
-   Enne loomist tehtud faile, peab vähemalt üks aktiivne krediidi ülekande konfiguratsiooni importida ER koosseisud. Lisateabe saamiseks vaadake [lae elektrooniline aruandlus koosseisud elutsükli teenuste](https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).
-   Kontodele makstavad makseviisid konfigureerimisel valida on **üldise elektroonilise aruandluse** ruut ja valige sobiv krediidi ülekande formaadis (näiteks **ISO 20022 kreeditkorralduse (AT)**) kui ekspordi vormi konfiguratsioon.
-   Peate seadistama ka juriidilise isiku ja pangakonto teavet Dynamics 365 toiminguteks.
-   Pangakonto numbrit, IBAN-ID ja mõnikord SWIFT koodid (innovaatikakeskust) või muud ID-d on vaja selleks, et luua sobiv tehtud maksed. Seetõttu peate seadistama need hankija pangakonto ja selle pangakonto organisatsioon, mis taotleb üleandmise eest.
-   Lisateavet võidakse nõuda näiteks käibemaks (VAT) numbrid lepinguosalistele, mis on nimetatud üleandmise krediidi sõnumis. See teave tuleb seadistada hankijatele ja juriidilisel isikul seda.
-   Mõned kontod maksta makseviisid enamasti ISO 20022 – vastavalt makseviisid võib nõuda täiendavaid seadistus **makse vormi koodikogumite**, nagu **teenuse liik** = **SLEV**. Neid koode kasutatakse täiendavaid sildistamine maksetehingute makse töötlemise ajal. Vaikimisi väärtused makse koodi, nagu **kategooria eesmärk**, **tasuta kuller**, **kohaliku vahend** ja **teenindamise tasemel** saab määrata kahes kohas. Esiteks on **kontode maksta makse töölehe päis** ja teine on **moodustab makstavate maksete meetodid**. Pärast makse töölehe ridade loomist, makse kood väärtustele, makse töölehe päise on töölehe reale üle viia, kui ei ole seatud, makseviisid väärtusi kasutatakse.

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>Milliseid parameetreid on saadaval tekitama krediidi vähendamisest?
Konkreetsete parameetrite sõltub krediidi ülekande formaadis. Järgmises tabelis on parameetrid, mis on saadaval ISO 20022 krediidi ülekanne makse faili Saksamaa loomisel hankija maksežurnaali. Kohta saadaolevate suvandite ning **taustal** jaotises käivitada makse kogumitena.

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
<td>Partii broneerimine</td>
<td>Märkige see ruut partii reserveerimise sildi lisamiseks XML-faili.</td>
</tr>
<tr class="even">
<td>Töötluskuupäev</td>
<td>Sisestage kuupäev, millal pank peaks makseid töötlema.</td>
</tr>
<tr class="odd">
<td>Vorming</td>
<td>Valige rahaülekande teabe vorming, olenevalt teie riigi/regiooni või panga nõudmistest.
<ul>
<li><strong>Strd</strong> – selle valiku, kasutada struktureeritud formaat, kui üks makserida tasakaalustatakse ühe arve. See suvand pole saadaval, Prantsusmaa, Saksamaa ja Hollandi riigi-/ regioonikohaste ekspordi formaadid.</li>
<li><strong>Ustrd</strong> – selle valiku abil saate kasutada struktureerimata vormingut, kus makse tasakaalustatakse mitme arvega. Tasakaalustatud arvete numbrid liidetakse ja kasutatakse rahaülekande teabena. Vastavalt ISO 20022 suunised, struktureerimata rahaülekande teave on kuni 140 tähemärki.</li>
</ul></td>
</tr>
<tr class="even">
<td>Arvete arv</td>
<td>Sisestage tegevuse selle ning <strong>maksesoovituse</strong> aruande printida.</td>
</tr>
<tr class="odd">
<td>Järjekorranumber</td>
<td>Sisestage faili tähistav järjekorranumber. Järjekorranumber kuvatakse selle <strong>käivad Märkus</strong> aruande.</td>
</tr>
<tr class="even">
<td>Prindi osalemismärkus</td>
<td>Märkige see ruut aruande <strong>Osalemismärkus</strong> printimiseks.</td>
</tr>
<tr class="odd">
<td>Prindi kontrollaruanne</td>
<td>Märkige see ruut makseteavet sisaldava aruande printimiseks.</td>
</tr>
<tr class="even">
<td>Kaaskirja printimine</td>
<td>Märkige see ruut aruande <strong>Maksesoovitus</strong> printimiseks.</td>
</tr>
</tbody>
</table>

## <a name="what-are-ibans-and-bics"></a>Mis on IBANid ja BICd?
Rahvusvaheline pangakonto Number (IBAN) ja panga tunnuskoodi (BIC) abil määratakse kindlaks iga konto paljudes riikides/piirkondades üle terve maailma. Nendeks on 34 SEPA riigis. Sisestage BIC on selle **SWIFT kood** välja ja IBAN ja selle **IBAN** välja. Võlausaldaja pangakonto ja kliendi pangakonto asuvad need väljad on **rentnikult isikut tõendavat** FastTab kohta on **pangakonto** vahekaardil on **pangakontode** lehel. SEPA maksete BIC kasutamist enam ei kohaldata.

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>Kuidas maksefail panka edastada?
Maksete loomisel makse fail on loodud ja teil palutakse Salvesta brauseris saadaval kõikjale. Järgmine samm on XML faili saatmiseks panka. See protsess erineb pankade lõikes. Järgige oma panga juhiseid failide edastamiseks panka töötlemiseks.


