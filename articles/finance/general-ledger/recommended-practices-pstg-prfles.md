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
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 097d1c6d1fbe64dadc69cdb275a0aef38922036d
ms.sourcegitcommit: 5bfd6511d710deb539b4030eb0e9c48d25513595
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/19/2022
ms.locfileid: "8014103"
---
# <a name="recommended-practices-for-posting-profiles"></a>Sisestusreeglite soovitatavad tavad

Sisestusreeglite konfigureerimisel kogu süsteemis on mitu soovitatavat tava, mida järgida. Selles teemas kirjeldatakse erinevaid stsenaariume ja vastavaid soovitatavaid tavasid.

## <a name="setting-the-do-not-allow-manual-entry-flag"></a>Sätte Ära luba käsitsi sisestuse lippu

Sisestusreeglites kasutatava mis tahes põhikonto puhul peab olema märgitud ruut Ära luba **käsitsi** **sisestamist** põhikontode leheküljel. Säte takistab kasutajatel töölehe sisestust käsitsi põhikontole sisestada. Seega aitab see tagada, et alammoodulis jääks pearaamatuga tasakaalustamata ning hõlbustab vastavusseviimisprotsessi hõlbustamist.

Kui korrigeerimisi on vaja süsteemi juhitaval ja automaatselt sisestatav kontol, saate kasutada ühte neist lähenemisviisist:

- Looge teisene põhikonto, kuhu saab korrigeerimisi sisestada. Seejärel kasutage kontode grupeerimiseks ja summeerimiseks oma finantsaruannetes summakontot või eririda.
- Tühistage algsed kanded sobivas alamvõtmes, tehke vajalikud parandused ja sisestage seejärel kanne uuesti sama alamvõtme kaudu.

## <a name="changing-posting-profiles-after-transactions-exist"></a>Sisestusreeglite muutmine pärast kannete olemasolu

Kui muudate sisestusreeglit pärast kannete olemasolu, võib vastavusseviimine nurjuda ning teie alammooduli ja pearaamatu saldo võib muutuda tasakaalust väljas. Üldiselt on soovitatav sisestusreeglit **pärast kannete olemasolu mitte** muuta.

Kui muudatused on nõutavad, kasutage süsteemi terviklikkuse tagamiseks järgmisi juhiseid.

- Tehke muudatused perioodi sulgemisel.
- Tehke muudatused, kui süsteemis ei toimu muid kandeid.
- Kontrollige pearaamatut ja viige see vastavusse alammooduliga enne ja pärast muudatuste tegemist.
- Sisestatud kandeid ei uuendata, kui muudate sisestusreeglit. Kaalutlege hoolikalt, kas muudatusi on vaja korrigeerida.
- Kui muudate lao sisestusprofiile, kaaluge, kuidas muudatused mõjutavad teie vaba kaubavaru ja pearaamatu saldot. Mõned muudatused võivad nõuda lao nullväärtuse toomist, lao sulgemist ja seejärel lao tagasi toomist pärast muudatuste tegemist.
- Enne tootmises tegemist katsetage alati oma muudatusi mittetootmiskeskkonnas.

## <a name="using-database-logging-to-audit-changes-to-posting-profiles"></a>Andmebaasi logimise kasutamine sisestusreeglite muudatuste auditeerimiseks

Kaaluge andmebaasi logimist iga sisestusreegli jaoks ja sisestamisega seotud parameetrite tabelite jaoks. Seejärel, kui parameetrit või profiili muudetakse, on teil täielik auditikirje selle kohta, milline väärtus muudeti, millal seda muudeti ja milline oli eelmine väärtus. See teave võib olla teie vastavusseviimise protsessi ajal kriitiline ja teie audiitor võib nõuda tugidokumente.

Lisateavet vt andmebaasi [logimise konfigureerimine](../../fin-ops-core/dev-itpro/sysadmin/configure-manage-database-log.md).

Kasutage järgmist tabelit viitena tavatabeli nimedele, mis on seotud sisestusreeglite ja seotud sisestusparameetriga.

| Lehe nimi | Navigeerimispaan | Tabeli nimi |
|-----------|-----------------|------------|
| Ostureskontro parameetrid | Ostureskontro &gt;&gt; seadistuse ostureskontro parameetrid | Üksuse VendParm |
| Hankija sisestusreeglid | Ostureskontro &gt;&gt; seadistuse hankija sisestusreeglid | Üksuse VendPosting |
| Tasukood | Ostureskontro &gt; kulude &gt; häälestuse kulude kood või &gt; müügireskontro kulude &gt; häälestuse kood | Ümardamistabel |
| Makseviisid | &gt; Ostureskontro makse &gt; seadistusmeetodid | VendPaymMode |
| Skontod | &gt; Ostureskontro makse &gt; seadistus skontod või &gt; müügireskontro makse seadistus &gt; skontod | CashDisc |
| Maksetasu (Hankija) | Ostureskontro &gt;&gt; makseseadistuse maksetasu | VendPaymFee |
| Müügireskontro parameetrid | Müügireskontro &gt;&gt; seadistuse müügireskontro parameetrid | CustParm |
| Kliendi sisestusreeglid | Müügireskontro &gt;&gt; seadistuse kliendi sisestusreeglid | CustPosting |
| Makseviisid | &gt; Müügireskontro maksete &gt; seadistusmeetodid | Üksuse CustPaymMode |
| Maksetasu (klient) | &gt; Müügireskontro maksete &gt; seadistuse makseviisid | CustPaymFee |
| Vara rentimise parameetrid | Vara lepingu &gt;&gt; seadistuse vara parameetreid | Konto AssetLeasePostingAccounts<br>VaraLeaseJournalParameters<br>Rakendus AssetLeaseExecutoryCostPostingAccounts |
| Pangakontod | Sularaha- ja &gt; pangahalduse &gt; pangakontod | BankAccountsTable |
| Pangakande tüübid | Sularaha- ja pangahalduse &gt;&gt; seadistuse pangakannete tüübid | BankTransType |
| Eemaldamisreeglid | Konsolideerimiste &gt; häälestamise &gt; eemaldamisreegel | LedgerEliminationRule<br>LedgerEliminationRuleLines |
| Kulukategooriad | Kuluhalduse &gt;&gt; häälestuse üldised &gt; kulukategooriad | ProjCategories |
| Põhivara parameetrid | Põhivara &gt;&gt; seadistuse põhivara parameetrid | AssetParameters |
| Põhivarade sisestusreeglid | Põhivara seadistamine &gt;&gt; põhivarade sisestusreeglid | Konto AssetLedgerAccounts<br>AssetDisposalParameters |
| Valuuta ümberhindamise kontod | Pearaamatu &gt; valuutade valuuta &gt; ümberarvutamise kontod | Konto CurrencyLedgerGainLossAccount |
| Automaatsete kannete kontod | Pearaamatu &gt; sisestamisseadistuse &gt; kontod automaatsete kannete jaoks | LedgerSystemAccounts |
| Kontserni raamatupidamine | Pearaamatu sisestamise &gt; häälestus &gt; Kontsernisisesed kontod | Kontsernisisene pearaamat |
| Kande sisestamisdefinitsioonid | Pearaamatu &gt; sisestamisseadistuse &gt; kande sisestamisdefinitsioonid | Töölehele sisestamisedefinitionTrans |
| Sisestamisdefinitsioonid | Pearaamatu &gt; sisestamisseadistuse &gt; sisestamisdefinitsioonid | Töölehele journalizingDefintion |
| Sisestamine (varud) | Laohalduse &gt; häälestuse &gt; sisestamine &gt; sisestamisel | InventPosting |
| Kulutüüpide koodid | Omahinna &gt; omahinna seadistamise &gt; kulutüübi koodid | Table'i ITMCostTypeTable |
| Ressursid | Tootmise juhtimise &gt; seadistuse &gt;&gt; ressursid | WrkCtrTable(i) |
| Ressursigrupid | Tootmise juhtimise &gt;&gt; häälestuse ressursside &gt; ressursigrupid | Grupp WrkCtrResourceGroup |
| Tootmisgrupid | Tootmise juhtimise &gt; seadistuse &gt;&gt; tootmisgrupp | ProdGroup |
| Kulukategooriad | Tootmisjuhtimise &gt; seadistuse &gt; protsesside &gt; kulukategooriad | ProjCategory |
| Projektigrupid | Projektihalduse ja raamatupidamise &gt; häälestuse &gt;&gt; projektigruppide sisestamine | ProjGroup |
| Pearaamatu sisestamise seadistus (projektid) | Projektihalduse ja raamatupidamise &gt; häälestus &gt; Pearaamatusse &gt; sisestamise häälestus | ProjPosting |
| Kulude vaikevastaskontod | Projektihalduse ja raamatupidamise &gt; seadistuse &gt; kulude sisestamise &gt; vaikevastaskontod | ProjDefaultOffsetSetup |
| Tagasimaksehalduse sisestusreeglid | Tagasimaksehalduse tagasimakse &gt; halduse sisestusseadistus &gt; Tagasimakse halduse sisestusprofiilid | TAMRebatePosting |
| Pearaamatu sisestusgrupp (maks) | Maksu &gt;&gt; seadistuse käibemaksu &gt; pearaamatu sisestamisgrupp | TaxAccountGroup |

## <a name="changing-groups-after-transactions-exist"></a>Gruppide muutmine pärast kannete olemasolu

Kasutage hoiatust, kui muudate gruppe koondandmetes. Kui kasutate sisestusreeglite määratlemiseks gruppe, võib mis tahes muudatus grupis koondkirjes avaldada negatiivset mõju pearaamatu vastavusseviimise võimalusele alammooduliga. Näiteks saate konfigureerida lao sisestusreeglid müügitellimuste tuluks nii, et iga kaubagrupi jaoks kasutatakse erinevat tulukontot. Kui muudate kaubale määratud kaubagruppi pärast kannete olemasolu, sisestatakse uute kannete tulu värskendatud kontole. Kõik enne muudatust sisestatud tulud jäävad aga algsele kontole.

## <a name="testing-posting-profiles"></a>Sisestusreeglite testimine

Enne oma otseülekannet ja pärast sisestusreeglite või seotud parameetrite muudatuste või täienduste tegemist peaksite testima iga stsenaariumi. Vähemalt peaksite testima iga sisestustüüpi, et kontrollida sisestuse korrektset toimimist. Soovitatav on siiski testida iga sisestusreegli kannet ja nende kombinatsiooni.

Näiteks on teil kaks kliendi sisestusreeglit, millest igaühel on kolm kliendigrupile omast kirjet. Sel juhul peaksite testima iga kandetüüpi.

**Sisestusreeglid:**

- **GEN** – üldine sisestusprofiil, kus on üks grupp töötajatele, üks klientidele ja teine kontsernisiseseks. Iga grupp osutab erinevale müügireskontro kaubanduskontole.
- **PRE** – ettemakse sisestusr reeglid, kus on üks kirje kõigi ettemaksete kohta, mis osutab kliendi ettemakstud kontodele.

### <a name="testing-scenarios"></a>Stsenaariumite testimine

- Vabas vormis arve töötajagrupi **kliendile**, kes kasutab **GEN-i** sisestusreeglit
- Vabas vormis arve töötajagrupi **kliendile**, kes kasutab **EELsisestureeglit**
- Müügitellimuse arve töötajagrupi kliendile, **kes kasutab** **GEN-i** sisestusreeglit
- Müügitellimuse arve töötajagrupi kliendile, **kes** kasutab eels **sisestamisreeglit**
- Kliendi maksetööleht töötajagrupi **kliendile,** kes kasutab **GEN-i** sisestusreeglit
- Kliendi maksetööleht töötajagrupi **kliendile,** kes kasutab EEL **sisestusreeglit**

Eelneva näite puhul korrake iga kliendigrupi puhul ühte testimisstsenaariumi ja korrake iga testimisstsenaariumide gruppi iga täiendava kandetüübi puhul (nt projektiarved ja teenusehaldus).

## <a name="reconciling-the-ledger-to-the-subledger"></a>Pearaamatu vastavusse viimine alammooduliga

Pearaamat tuleks igal perioodil viia vastavusse alammooduliga. Mitmed moodulid sisaldavad boksist erinevaid aruandeid, mida saab kasutada selle vastavusseviimise abiks. Sõltuvalt kohalikest nõuetest peate võib-olla välja töötama kohandatud aruanded või laiendama olemasolevaid aruandeid aruandlusnõuete täitmiseks.

Soovitame teil teha m ajaperioodi sulgemisel ja viia kõik alammoodulid enne ülekannet pearaamatusse vastavusse. Soovitame teil teha ka kõik avatud saldod ja avatud kanded enne algset üleminekut. Selle protsessi osana peaksite käivitama täieliku vastavusseviimise, et tagada saldode ja avatud kannete siirded pärandsüsteemidega ning et kõik alammoodulid tasakaalustavad pearaamatuga enne uute kannete loomist.
