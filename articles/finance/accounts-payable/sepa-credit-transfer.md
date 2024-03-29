---
title: SEPA kreeditiülekande ülevaade
description: See artikkel annab üldist teavet ISO 20022 krediidiedastuste kohta, mis hõlmab ühtse euromaksete piirkonna (SEPA) kreeditiülekandeid ja mis tahes muid hankijatele mõeldud elektroonilisi makseid.
author: mrolecki
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "11124"
- intro-internal
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 671594b1ac6f10fae7c95ed9210e16f168e8dea1
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716070"
---
# <a name="sepa-credit-transfer-overview"></a>SEPA kreeditiülekande ülevaade

[!include [banner](../includes/banner.md)]

See artikkel annab üldist teavet ISO 20022 krediidiedastuste kohta, mis hõlmab ühtse euromaksete piirkonna (SEPA) kreeditiülekandeid ja mis tahes muid hankijatele mõeldud elektroonilisi makseid. SEPA kreeditiülekanne on ühe ettevõtte või isiku spetsiifiline makse tüüp eurodes teisele ettevõttele või isikule. Artikkel selgitab ka seda, kuidas seadistada ja edastada kreediti ülekande maksefaili.

## <a name="what-is-a-credit-transfer-message"></a>Mis on kreeditiülekande sõnum?
Kreeditiülekande sõnum on taotlus, mille algatav osapool (teie ettevõte) saadab fondide liigutamiseks oma enda kontolt kreeditorile. On palju kreeditiülekande sõnumite riigi-/piirkonna- ja pangaspetsiifilisi rakendusi. Mõnda neist kasutatakse ühe riigi/piirkonna piires ja mõned muutuvad standarditeks. Üks hästi loodud globaalne standard on ISO 20022 ja selle algatamise sõnumid, nagu kreeditiülekanne. Järgmine joonis näitab valitud kreeditiülekande sõnumite seoseid ja hõlmavust. 
![Kreeditiülekanne.](./media/credit-transfer.jpg) Kreediti ülekandeteated 

## <a name="what-are-iso-20022-and-sepa-payments"></a>Mis on ISO 20022 ja SEPA-maksed?
Ühtse euromaksete piirkonna (SEPA) on määranud Euroopa Komisjon, kelle korraldusel tuleb kõiki elektroonilisi makseid käsitleda kodumaistena, olenemata riigist/piirkonnast, kus üksikisik, ettevõte või organisatsioon ja pank asuvad. Riiklikel maksetel ja riikidevahelistel maksetel pole mingit vahet. SEPA hõlmab 28 Euroopa Liidu liikmesriiki ning samuti Islandit, Liechtensteini, Norrat, Šveitsi, Monacot ja San Marinot. SEPA aitab Euroopa majanduspiirkonnas (EMP) luua maksekannete jaoks ühtse turu. Lõppkokkuvõttes eeldatakse, et SEPA vähendab maksevormingute arvu, millega pangad, ettevõtted ja üksiksikud peavad tegelema. Euroopa Komisjon määras SEPA maksetele juriidilise aluse makseteenuste direktiiviga (PSD). Euroopa Maksenõukogu (EPC) toetab SEPA-d läbi järgmiste tegevuste.

-   See määrab SEPA elektrooniliste maksete standardid, kasutades ISO-20022 universaalse finantsvaldkonna sõnumiskeemi XML-vormingut.
-   See kehtestab euromaksete käsitsemise reeglid ja juhised.

EPC, mis koosneb Euroopa pankadest, arendab SEPA maksevahendite kaubandus- ja tehnilist raamistikku. Kasutatakse kolme SEPA maksete tüüpi.

-   Kreeditülekanded
-   Otsekorraldused
-   Kaardid

## <a name="what-is-a-sepa-credit-transfer"></a>Mis on SEPA kreeditülekanne?
SEPA kreeditülekanne on ühe ettevõtte või isiku makse teisele ettevõttele või isikule. Maksed peavad olema eurodes ja sisaldama mõlema osapoole puhul rahvusvahelist pangakonto numbrit (IBAN) ja panga koodi (BIC). (BIC on tuntud ka kui Society for Worldwide Interbank Financial Telecommunication \[SWIFT\] kood.) Täiendavalt tuleb kandekulusid jagada mitme osapoole vahel. Pooltevahelised kreeditülekanded peavad kasutama XML-faile, mis vastavad ISO 20022 maksete töötlemise standarditele ja XML-vormingule, nagu EPC on täpsustanud.

## <a name="how-is-a-credit-transfer-implemented"></a>Kuidas kreeditülekannet rakendatakse?
Euroopa riikide krediidiülekande maksevorming rakendatakse 365 Finantside elektroonilise aruandluse (ER) Microsoft Dynamics ja makseviiside abil. Mõned teistes piirkondades kasutatavad kreeditiülekande vormingud kasutavad endiselt pärandmakseraamistikku. Paljude muude vormingute hulgas on saadaval kaksteist ISO 20022 kreeditiülekande failivormingut. Need ekspordivormingud vastavad SEPA ISO 20022 XML-standardile. Neid kasutatakse mitteeuroste makseülekannete loomiseks riikidele/piirkondadele, kus neid kasutatakse, ja euromaksete loomiseks, nagu on määratud EPC väljastatava trükise SEPA Credit Transfer Scheme Rulebook versioonis 8.2. Enne kreeditiülekannete rakendamist peate pöörduma oma panga poole, et saada tarkvara, mida elektrooniliste pangafailide üleslaadimiseks vaja on. Seda tarkvara kasutatakse maksetellimusi sisaldavate XML-failide edastamiseks panka.

## <a name="what-credit-transfer-formats-are-currently-supported"></a>Milliseid krediitkaardimakse vorminguid praegu toetatakse?
Saate alati minna teenuses Microsoft Dynamics Lifecycle services (LCS) olevasse ühiste varade teeki ja vaadata kõige ajakohasemat loendit saadaolevatest failidest, mille vara tüüp on **GER-i konfiguratsioon**. Järgmises jaotises "Mida on vaja seadistada?", antakse link artikli juurde, mis selgitab LCS-i hoidla loomise teavet saadaval olnud konfiguratsioonide ülevaatamiseks ja valitud konfiguratsioonide importimiseks.

## <a name="what-do-i-have-to-set-up"></a>Mida pean seadistamiseks tegema?
-   Enne kui saate kreeditiülekande faile luua, tuleb teie elektroonilise aruandluse konfiguratsioonidesse importida vähemalt üks aktiivne kreeditiülekande konfiguratsioon. Juhiste saamiseks vaadake teemat [Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).
-   Kui konfigureerite ostureskontro makseviise, märkige ruut **Üldine elektrooniline aruandlus** ja valige ekspordivormingu konfiguratsioonina sobiv kreeditülekande vorming (näiteks **ISO 20022 kreeditiülekanne (AT)**).
-   Samuti tuleb seadistada juriidilise isiku ja pangakonto andmed.
-   Kehtivate kreeditiülekande maksete loomiseks on vaja pangakonto numbreid, IBAN-sid ja mõnikord SWIFT-koode (BIC-id). Seega tuleb need seadistada nii hankija pangakonto kui ka ülekannet taotleva organisatsiooni pangakonto jaoks.
-   Vaja võib olla täiendavat teavet, nagu käibemaksunumbrid osapooltele, kellele viidatakse kreeditiülekande sõnumis. See teave tuleb seadistada hankijatele ja juriidilisele isikule selle taotlemisel.
-   Mõned ostureskontro makseviisid (peamiselt ISO 20022-põhised makseviisid) võivad nõuda valiku **Maksevormingu koodikomplektid** jaoks täiendavat seadistust, nagu **Teenuse tüüp** = **SLEV**. Neid koode kasutatakse maksetöötluse käigus maksekannete täiendavaks sildistamiseks. Maksekoodide vaikeväärtuseid, nagu **Kategooria eesmärk**, **Tasu maksja**, **Kohalik vahend** ja **Teenustase**, saab määrata kahes kohas. Esimene koht on **Ostureskontro maksetöölehe päis** ja teine **Ostureskontro makseviisid**. Maksetöölehe ridade loomisel edastatakse maksetöölehe päisel olevad maksekoodi väärtused töölehe reale; kui neid pole määratud, kasutatakse makseviiside väärtuseid.

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>Millised parameetrid on kreeditülekannete maksete loomiseks saadaval?
Spetsiifiliste parameetrite loend sõltub kreeditiülekande vormingust. Järgmises tabelis on näidatud parameetrid, mis on hankija maksetöölehel Saksamaa jaoks ISO 20022 kreeditiülekande maksefaili loomisel saadaval. Kasutades vahekaardi **Käivita taustal** valikuid, saate luua makse pakettrežiimis.

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
<li><strong>Struktureeritud</strong> – selle valiku abil saate kasutada struktureeritud vormingut, kus üks makserida tasakaalustatakse ühe arvega. See valik ei ole saadaval Prantsusmaa, Saksamaa ega Hollandi riigi-/ regioonipõhiste ekspordivormingute puhul.</li>
<li><strong>Ustrd</strong> – selle valiku abil saate kasutada struktureerimata vormingut, kus makse tasakaalustatakse mitme arvega. Tasakaalustatud arvete numbrid liidetakse ja kasutatakse rahaülekande teabena. ISO 20022 juhiste kohaselt on struktureerimata rahaülekande teave piiratud 140 märgiga.</li>
</ul></td>
</tr>
<tr class="even">
<td>Arvete arv</td>
<td>Sisestage arvete arv, millelt aruanne <strong>Maksesoovitus</strong> prinditakse.</td>
</tr>
<tr class="odd">
<td>Järjekorranumber</td>
<td>Sisestage faili tähistav järjekorranumber. Järjekorranumber kuvatakse aruandes <strong>Osalemismärkus</strong>.</td>
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
Rahvusvahelist pangakonto numbrit (IBAN) ja panga identifikaatorkoodi (BIC) kasutatakse kõigi kontode tuvastamiseks paljudes riikides/piirkondades üle maailma. Need hõlmavad 34 SEPA riiki/piirkonda. Sisestage BIC väljale **SWIFT-kood** ja IBAN väljale **IBAN**. Nii kreeditori kui ka kliendi pangakonto puhul asuvad need väljad lehe **Pangakontod** vahekaardi **Pangakonto** kiirkaardil **Täiendav identifitseerimine**. BIC kasutamist SEPA maksete puhul enam ei jõustata.

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>Kuidas maksefail panka edastada?
Maksete loomisel luuakse maksefail ja teil palutakse salvestada see veebibrauserist mõnda olemasolevasse asukohta. Järgmine etapp on XML-faili panka saatmine. See protsess erineb pankade lõikes. Järgige oma panga juhiseid failide edastamiseks panka töötlemiseks.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
