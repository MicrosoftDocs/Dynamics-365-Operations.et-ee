---
title: Dynamics 365 Financei eemaldatud või aegunud funktsioonid
description: See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Dynamics 365 Finance'ist.
author: roschlom
ms.date: 04/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 8cacf2fbef8873288493f71b43d22dc186e6d18e
ms.sourcegitcommit: 35fdcc6501e099c54a58583b1e3aba16f02a5ccc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2021
ms.locfileid: "5980893"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Dynamics 365 Financei eemaldatud või aegunud funktsioonid

[!include [banner](../includes/banner.md)]

See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Dynamics 365 Finance'ist.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

See loend peaks aitama teil neid eemaldusi ja aegumisi oma plaanides arvesse võtta. 

> [!NOTE]
> Üksikasjalikku teavet rakenduse Finance and Operationsi rakenduste objektide kohta leiate teemast [Tehnilise teabe aruanded](/dynamics/s-e/global/axtechrefrep_61). Saate võrrelda nende aruannete eri versioone, et õppida objektide kohta, mida on igas Finance and Operationsi rakenduste versioonis muudetud või eemaldatud.

## <a name="features-removed-or-deprecated-in-the-finance-10020-release"></a>Finance'i väljalaskest 10.0.20 eemaldatud või aegunud funktsioonid

### <a name="rtir-query-invoice-data-request-hu-electronic-reporting-er-format-configuration"></a>"RTIR-päringu arve andmetaotluse (HU)" vormingu konfiguratsioon

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Välja arvatud Ungari veebiarveldussüsteemiga koostoimimise elektroonilisest sõnumside töötlemisest |
| **Asendatud teise funktsiooniga?**   | Ei |
| **Mõjutatud tootealad**         | Avaldus |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud: 15. aprilliks 2022 ei kavatse me enam toetada vormingu "RTIR Päringuarve andmetaotlus (HU)" konfiguratsiooni. |

### <a name="french-fec-audit-file-electronic-reporting-er-format-for-france-under-german-audit-file-output-format"></a>"Prantsuse FEC auditi fail" Elektroonilise aruandluse (ER) vorming Prantsusmaa jaoks "Saksa auditfaili väljund" vorming

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Asendatud uue "FEC-auditi faili (FR)" vorminguga |
| **Asendatud teise funktsiooniga?**   | Jah |
| **Mõjutatud tootealad**         | Avaldus |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Katkestatud: 1. maiks 2022 plaanime enam mitte toetada "Prantsusmaa FEC auditifaili" elektroonilise aruandluse (ER) vormingut Prantsuse "Saksa auditifaili väljund" vormingu all. Uus FEC auditifaili (FR) vorming tutvustatakse hoopis "Andme ekspordi mudeli" all. |

## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a>Finance'i väljalaskest 10.0.17 eemaldatud või aegunud funktsioonid

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a>LCS-i hoidla elektrooniliste aruandluskonfiguratsioonide talletusvalikuna

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Asendatud uue regulatiivse konfiguratsiooniteenuse (RCS) globaalse hoidlaga |
| **Asendatud teise funktsiooniga?**   | Jah |
| **Mõjutatud tootealad**         | Dynamics 365 Finance, Supply Chain Management, ja Project Operations tooted|
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegumine: 01. aprilliks 2022 ei plaani me enam Lifecycle Services (LCS) hoidlat elektroonilise aruandluse Microsoft Dynamics (ER) konfiguratsioonide talletusvalikuna toetada. Uued Microsofti ER-i konfiguratsioonid avaldatakse allalaadimiseks ainult globaalsest hoidlast. Globaalsele hoidlale pääseb juurde Dynamics 365 toodetest ja RCS-ist. Lisateabe saamiseks vt teemat [(ER) konfiguratsioonide importimine RCS-ist](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a>Finance'i väljalaskest 10.0.16 eemaldatud või aegunud funktsioonid

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a>Elektroonilised aruandlusvormingud "Km-i deklaratsioon (CZ)" ja "Kontrolldeklaratsiooni eksport (CZ)" Tšehhi Vabariigile

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Asendatud uute vormingutega |
| **Asendatud teise funktsiooniga?**   | Jah |
| **Mõjutatud tootealad**         | Avaldus |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Iganenud: 22. jaanuarist 2022 ei plaani me enam toetada "KM-i deklaratsiooni (CZ)", "Kontrolldeklaratsiooni ekspordi (CZ)" elektroonilis aruandlusvorminguid (ER). Selle asemel võetakse "Maksudeklaratsiooni" mudeli all kasutusele uued KM-i deklaratsiooni XML (CZ), Käibemaksudeklaratsiooni Excel (CZ), Käibemaksu kontrolldeklaratsioon XML (CZ) vormingud. |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a>"Pearaamatu kannete ekspordi vorming (BE)" Elektroonilise aruandluse vorming ja vastava "Pearaamatu kannete ekspordi (BE)" Belgia mudel

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Asendada uue ER-vorminguga "Standardse auditi faili (SAF-T)" mudeli all.  |
| **Asendatud teise funktsiooniga?**   | Jah |
| **Mõjutatud tootealad**         | Avaldus |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Iganenud: 1. detsembril 2021 plaanime lõpetada "Pearaamatu kannete ekspordi vormingu (BE)" elektroonilise aruandluse (ER) vormingu ja vastava mudeli "Pearaamatu kannete eksport (BE)" toetamise. Mudeli "Standardse auditi faili (SAF-T)" asemel võetakse kasutusele uus "Pearaamatu andmete ekspordi (BE)" vorming koos "Pearaamatu andmemudeli vastendamisega". |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a>"VAT 100" aruanne Ühendkuningriigile SSRS vormingus

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Asendatakse uue ER-vorminguga -"KM-i deklaratsiooni Excel (UK)" vorming "Maksudeklaratsiooni mudeli" all.  |
| **Asendatud teise funktsiooniga?**   | Jah |
| **Mõjutatud tootealad**         | Avaldus |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Iganenud: 1. detsembril 2021 plaanime lõpetada SSRS-vormingus "KM 100 aruande" toetamise. Uus "KM-i deklaratsiooni Excel (UK)" vorming jaotises "Maksudeklaratsiooni mudel" võeti kasutusele [MTD KM funktsioonis](../localizations/emea-gbr-mtd-vat-integration.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a>Finance'i väljalaskest 10.0.15 eemaldatud või aegunud funktsioonid

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11 Dynamics 365 tugi on iganenud

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Kehtib alates 2020. detsembrist, Microsoft Internet Explorer 11 tugi kõigile Dynamics 365 toodetele on iganenud ja Internet Explorer 11 ei toetata pärast 2021. aasta augustit.<br><br>See mõjutab kliente, kes kasutavad Dynamics 365 tooteid, mis on mõeldud kasutamiseks Internet Explorer 11 liidese kaudu. Pärast 2021. aasta augustit, Internet Explorer 11 ei toetata selliste Dynamics 365 toodete puhul. |
| **Asendatud teise funktsiooniga?**   | Soovitame klientide minna üle Microsoft Edge-le.|
| **Mõjutatud tootealad**         | Kõik Dynamics 365 tooted |
| **Juurutamissuvand**              | Kõik|
| **Olek**                         | Aegunud. Internet Explorer 11 ei toetata pärast 2021. aasta augustit.|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Finance'i väljalaskest 10.0.12 eemaldatud või aegunud funktsioonid

### <a name="not-deprecated-polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Pole iganenud: Poola SSRS-i aruanded: Arvestatud käibemaksu register, sisendkäibemaksu register, EL-i koondkäibemaksu register – funktsiooni viide PL-00014

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Juriidiliselt pole vajalik.  |
| **Asendatud teise funktsiooniga?**   | Jah (Exceli vorming standardse auditifaili jaoks KM-i deklaratsiooniga – JPK_VDEK) |
| **Mõjutatud tootealad**         | Avaldus |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Pole iganenud: Aegub 27. juuliks 2021, plaanime jätkuvalt toetada SSRS-i aruandeid: **Arvestatud käibemaksu register, sisendkäibemaksu register, EL-i koondkäibemaksu register – funktsiooni viide PL-00014**. Kasutusele on võetud Exceli vormingu standardse auditifaili näide koos KM deklaratsiooniga (JPK_VDEK). |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Finance'i väljalaskest 10.0.11 eemaldatud või aegunud funktsioonid

### <a name="norwegian-standard-main-accounts"></a>Norwegian Standardi põhikontod

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Ümberkujundamine  |
| **Asendatud teise funktsiooniga?**   | Jah (asendatud ER-i vormingu rakendusekohaste parameetritega) |
| **Mõjutatud tootealad**         | Rakendus |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud: alates 2021. a 1. aprillist ei kavatse me enam toetada standardsete põhikontodega seotud funktsioone: viiteväli, seotud tabel, andmeüksus. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Finance'i väljalaskest 10.0.7 eemaldatud või aegunud funktsioonid

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Töövoo taotluse muutmise dialoogiboks ei sisalda enam kasutaja valiku ripploendit

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Muudetud funktsiooniks, mis sisaldab konto gruppide valikut.  |
| **Asendatud teise funktsiooniga?**   | Jah |
| **Mõjutatud tootealad**         | Töövoog |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegub: 1. detsembril 2020. Me ei plaani enam toetada Hiina kandetüüpide seadistust ilma konto gruppide valikuta. Lisateavet uue kujunduse kohta leiate teemast [Mis on uut versioonis 10.0.7](whats-new-changed-10-0-7.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Varasemad teatised eemaldatud või aegunud funktsioonidest
Lisateavet funktsioonide kohta, mis on eelnevatest versioonidest eemaldatud või aegunud, vt teemat [Varasematest versioonidest eemaldatud või aegunud funktsioonid](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
