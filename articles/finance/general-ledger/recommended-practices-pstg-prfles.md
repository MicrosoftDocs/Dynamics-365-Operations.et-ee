---
title: Sisestusreeglite soovitatavad tavad
description: Selles teemas kirjeldatakse sisestusreeglite konfigureerimise soovitatavaid tavasid.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, MainAccount, SysDatabaseLogSetup, CustGroup, VendGroup, InventItemGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 211dc42b80089eb1f59a435f09d6e9d9f956736b
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734271"
---
# <a name="recommended-practices-for-posting-profiles"></a>Sisestusreeglite soovitatavad tavad

Sisestusreeglite konfigureerimisel kogu süsteemis on mitu soovitatavat tava, mida järgida. Selles teemas kirjeldatakse erinevaid stsenaariume ja vastavaid soovitatavaid tavasid.

## <a name="setting-the-do-not-allow-manual-entry-flag"></a>Sätte Ära luba käsitsi sisestuse lippu

**Sisestusreeglites** kasutatava mis **tahes põhikonto** puhul peab olema märgitud ruut Ära luba käsitsi sisestamist põhikontode leheküljel. Säte takistab kasutajatel töölehe sisestust käsitsi põhikontole sisestada. Seega aitab see tagada, et alammoodulis jääks pearaamatuga tasakaalustamata ning hõlbustab vastavusseviimisprotsessi hõlbustamist.

Kui korrigeerimisi on vaja süsteemi juhitaval ja automaatselt sisestatav kontol, saate kasutada ühte neist lähenemisviisist:

- Looge teisene põhikonto, kuhu saab korrigeerimisi sisestada. Seejärel kasutage kontode grupeerimiseks ja summeerimiseks oma finantsaruannetes summakontot või eririda.
- Tühistage algsed kanded sobivas alamvõtmes, tehke vajalikud parandused ja sisestage seejärel kanne uuesti sama alamvõtme kaudu.

## <a name="changing-posting-profiles-after-transactions-exist"></a>Sisestusreeglite muutmine pärast kannete olemasolu

Kui muudate sisestusreeglit pärast kannete olemasolu, võib vastavusseviimine nurjuda ning teie alammooduli ja pearaamatu saldo võib muutuda tasakaalust väljas. Üldiselt on soovitatav sisestusreeglit **pärast** kannete olemasolu mitte muuta.

Kui muudatused on nõutavad, kasutage süsteemi terviklikkuse tagamiseks järgmisi juhiseid.

- Tehke muudatused perioodi sulgemisel.
- Tehke muudatused, kui süsteemis ei toimu muid kandeid.
- Kontrollige pearaamatut ja viige see vastavusse alammooduliga enne ja pärast muudatuste tegemist.
- Sisestatud kandeid ei uuendata, kui muudate sisestusreeglit. Kaalutlege hoolikalt, kas muudatusi on vaja korrigeerida.
- Kui muudate lao sisestusprofiile, kaaluge, kuidas muudatused mõjutavad teie vaba kaubavaru ja pearaamatu saldot. Mõned muudatused võivad nõuda lao nullväärtuse toomist, lao sulgemist ja seejärel lao tagasi toomist pärast muudatuste tegemist.
- Enne tootmises tegemist katsetage alati oma muudatusi mittetootmiskeskkonnas.

## <a name="using-database-logging-to-audit-changes-to-posting-profiles"></a>Andmebaasi logimise kasutamine sisestusreeglite muudatuste auditeerimiseks

Kaaluge andmebaasi logimist iga sisestusreegli jaoks ja sisestamisega seotud parameetrite tabelite jaoks. Seejärel, kui parameetrit või profiili muudetakse, on teil täielik auditikirje selle kohta, milline väärtus muudeti, millal seda muudeti ja milline oli eelmine väärtus. See teave võib olla teie vastavusseviimise protsessi ajal kriitiline ja teie audiitor võib nõuda tugidokumente.

Lisateavet vt andmebaasi logimise [konfigureerimine](../../fin-ops-core/dev-itpro/sysadmin/configure-manage-database-log.md).

Kasutage järgmist tabelit viitena tavatabeli nimedele, mis on seotud sisestusreeglite ja seotud sisestusparameetriga.

| Lehe nimi | Navigeerimispaan | Tabeli nimi |
|-----------|-----------------|------------|
| Ostureskontro parameetrid | Ostureskontro &gt; seadistuse &gt; ostureskontro parameetrid | Üksuse VendParm |
| Hankija sisestusreeglid | Ostureskontro &gt; seadistuse &gt; hankija sisestusreeglid | Üksuse VendPosting |
| Tasukood | Ostureskontro &gt; kulude häälestuse &gt; kulude kood või müügireskontro kulude &gt; häälestuse &gt; kood | Ümardamistabel |
| Makseviisid | Ostureskontro &gt; makse seadistusmeetodid &gt; | VendPaymMode |
| Skontod | Ostureskontro &gt; makse seadistus &gt; skontod või müügireskontro &gt; makse seadistus &gt; skontod | CashDisc |
| Maksetasu (Hankija) | Ostureskontro &gt; makseseadistuse &gt; maksetasu | VendPaymFee |
| Müügireskontro parameetrid | Müügireskontro &gt; seadistuse &gt; müügireskontro parameetrid | CustParm |
| Kliendi sisestusreeglid | Müügireskontro &gt; seadistuse &gt; kliendi sisestusreeglid | CustPosting |
| Makseviisid | Müügireskontro &gt; maksete seadistusmeetodid &gt; | Üksuse CustPaymMode |
| Maksetasu (klient) | Müügireskontro &gt; maksete seadistuse &gt; makseviisid | CustPaymFee |
| Vara rentimise parameetrid | Vara lepingu seadistuse &gt;&gt; vara parameetreid | Konto AssetLeasePostingAccounts<br>VaraLeaseJournalParameters<br>Rakendus AssetLeaseExecutoryCostPostingAccounts |
| Pangakontod | Sularaha- ja pangahalduse &gt; pangakontod &gt; | BankAccountsTable |
| Pangakande tüübid | Sularaha- ja pangahalduse seadistuse &gt;&gt; pangakannete tüübid | BankTransType |
| Eemaldamisreeglid | Konsolideerimiste häälestamise &gt; eemaldamisreegel &gt; | LedgerEliminationRule<br>LedgerEliminationRuleLines |
| Kulukategooriad | Kuluhalduse häälestuse &gt;&gt; üldised &gt; kulukategooriad | ProjCategories |
| Põhivara parameetrid | Põhivara seadistuse &gt;&gt; põhivara parameetrid | AssetParameters |
| Põhivarade sisestusreeglid | Põhivara seadistamine &gt; põhivarade &gt; sisestusreeglid | Konto AssetLedgerAccounts<br>AssetDisposalParameters |
| Valuuta ümberhindamise kontod | Pearaamatu valuutade &gt; valuuta ümberarvutamise &gt; kontod | Konto CurrencyLedgerGainLossAccount |
| Automaatsete kannete kontod | Pearaamatu sisestamisseadistuse &gt; kontod &gt; automaatsete kannete jaoks | LedgerSystemAccounts |
| Kontserni raamatupidamine | Pearaamatu sisestamise &gt; häälestus &gt; Kontsernisisesed kontod | Kontsernisisene pearaamat |
| Kande sisestamisdefinitsioonid | Pearaamatu sisestamisseadistuse &gt; kande &gt; sisestamisdefinitsioonid | Töölehele sisestamisedefinitionTrans |
| Sisestamisdefinitsioonid | Pearaamatu sisestamisseadistuse &gt; sisestamisdefinitsioonid &gt; | Töölehele journalizingDefintion |
| Sisestamine (varud) | Laohalduse häälestuse &gt; sisestamine &gt; sisestamisel &gt; | InventPosting |
| Kulutüüpide koodid | Omahinna omahinna &gt; seadistamise kulutüübi &gt; koodid | Table'i ITMCostTypeTable |
| Ressursid | Tootmise juhtimise seadistuse &gt;&gt; ressursid &gt; | WrkCtrTable(i) |
| Ressursigrupid | Tootmise juhtimise häälestuse &gt;&gt; ressursside &gt; ressursigrupid | Grupp WrkCtrResourceGroup |
| Tootmisgrupid | Tootmise juhtimise seadistuse &gt;&gt; tootmisgrupp &gt; | ProdGroup |
| Kulukategooriad | Tootmisjuhtimise seadistuse &gt; protsesside &gt; kulukategooriad &gt; | ProjCategory |
| Projektigrupid | Projektihalduse ja raamatupidamise häälestuse &gt;&gt; projektigruppide &gt; sisestamine | ProjGroup |
| Pearaamatu sisestamise seadistus (projektid) | Projektihalduse ja raamatupidamise häälestus &gt; Pearaamatusse &gt; sisestamise &gt; häälestus | ProjPosting |
| Kulude vaikevastaskontod | Projektihalduse ja raamatupidamise seadistuse &gt; kulude &gt;&gt; sisestamise vaikevastaskontod | ProjDefaultOffsetSetup |
| Tagasimakse halduse sisestamise profiilid | Tagasimaksehalduse tagasimakse &gt; halduse sisestusseadistus Tagasimakse &gt; halduse sisestusprofiilid | TAMRebatePosting |
| Pearaamatu sisestusgrupp (maks) | Maksu &gt; seadistuse &gt; käibemaksu pearaamatu &gt; sisestamisgrupp | TaxAccountGroup |

## <a name="changing-groups-after-transactions-exist"></a>Gruppide muutmine pärast kannete olemasolu

Kasutage hoiatust, kui muudate gruppe koondandmetes. Kui kasutate sisestusreeglite määratlemiseks gruppe, võib mis tahes muudatus grupis koondkirjes avaldada negatiivset mõju pearaamatu vastavusseviimise võimalusele alammooduliga. Näiteks saate konfigureerida lao sisestusreeglid müügitellimuste tuluks nii, et iga kaubagrupi jaoks kasutatakse erinevat tulukontot. Kui muudate kaubale määratud kaubagruppi pärast kannete olemasolu, sisestatakse uute kannete tulu värskendatud kontole. Kõik enne muudatust sisestatud tulud jäävad aga algsele kontole.

## <a name="testing-posting-profiles"></a>Sisestusreeglite testimine

Enne oma otseülekannet ja pärast sisestusreeglite või seotud parameetrite muudatuste või täienduste tegemist peaksite testima iga stsenaariumi. Vähemalt peaksite testima iga sisestustüüpi, et kontrollida sisestuse korrektset toimimist. Soovitatav on siiski testida iga sisestusreegli kannet ja nende kombinatsiooni.

Näiteks on teil kaks kliendi sisestusreeglit, millest igaühel on kolm kliendigrupile omast kirjet. Sel juhul peaksite testima iga kandetüüpi.

**Sisestusreeglid:**

- **GEN** – üldine sisestusprofiil, kus on üks grupp töötajatele, üks klientidele ja teine kontsernisiseseks. Iga grupp osutab erinevale müügireskontro kaubanduskontole.
- **PRE** – ettemakse sisestusr reeglid, kus on üks kirje kõigi ettemaksete kohta, mis osutab kliendi ettemakstud kontodele.

### <a name="testing-scenarios"></a>Stsenaariumite testimine

- Vabas vormis arve töötajagrupi kliendile **, kes** kasutab GEN-i **sisestusreeglit**
- Vabas vormis arve töötajagrupi kliendile **, kes** kasutab **EELsisestureeglit**
- Müügitellimuse arve töötajagrupi kliendile, kes **kasutab** GEN-i **sisestusreeglit**
- Müügitellimuse arve töötajagrupi kliendile, kes **kasutab** eels **sisestamisreeglit**
- Kliendi maksetööleht töötajagrupi kliendile **, kes** kasutab GEN-i **sisestusreeglit**
- Kliendi maksetööleht töötajagrupi kliendile **, kes** kasutab EEL **sisestusreeglit**

Eelneva näite puhul korrake iga kliendigrupi puhul ühte testimisstsenaariumi ja korrake iga testimisstsenaariumide gruppi iga täiendava kandetüübi puhul (nt projektiarved ja teenusehaldus).

## <a name="reconciling-the-ledger-to-the-subledger"></a>Pearaamatu vastavusse viimine alammooduliga

Pearaamat tuleks igal perioodil viia vastavusse alammooduliga. Mitmed moodulid sisaldavad boksist erinevaid aruandeid, mida saab kasutada selle vastavusseviimise abiks. Sõltuvalt kohalikest nõuetest peate võib-olla välja töötama kohandatud aruanded või laiendama olemasolevaid aruandeid aruandlusnõuete täitmiseks.

Soovitame teil teha m ajaperioodi sulgemisel ja viia kõik alammoodulid enne ülekannet pearaamatusse vastavusse. Soovitame teil teha ka kõik avatud saldod ja avatud kanded enne algset üleminekut. Selle protsessi osana peaksite käivitama täieliku vastavusseviimise, et tagada saldode ja avatud kannete siirded pärandsüsteemidega ning et kõik alammoodulid tasakaalustavad pearaamatuga enne uute kannete loomist.
