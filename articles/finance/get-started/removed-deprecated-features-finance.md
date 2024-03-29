---
title: Dynamics 365 Finance'i eemaldatud või aegunud funktsioonid
description: See artikkel kirjeldab funktsioone, mis on eemaldatud või plaanitud rakendusest Dynamics 365 Finance eemaldamiseks.
author: kfend
ms.date: 10/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 516b2b6091fa620b21eebba25f56ff55aa282ffc
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643790"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Dynamics 365 Finance'i eemaldatud või aegunud funktsioonid

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab funktsioone, mis on eemaldatud või plaanitud rakendusest Dynamics 365 Finance eemaldamiseks.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

See loend peaks aitama teil neid eemaldusi ja aegumisi oma plaanides arvesse võtta. 

> [!NOTE]
> Finantside ja toimingute rakenduste objektide üksikasjaliku teabe leiate tehnilistest [viitearuannetest](/dynamics/s-e/global/axtechrefrep_61). Saate võrrelda nende aruannete erinevaid versioone, et saada teavet objektide kohta, mida on igas finantsi ja toimingute rakenduste versioonis muudetud või eemaldatud.

## <a name="features-removed-or-deprecated-in-the-finance-10031-release"></a>Finance'i väljalaskest 10.0.31 eemaldatud või aegunud funktsioonid

### <a name="edifact-paymul-at-configuration-under-payment-model"></a>EDIFACT PAYMUL(AT) konfiguratsioon maksemudeli <a0/& all

| &nbsp;  | &nbsp;  |
|---|---|
| **Aegumise/eemaldamise põhjus** | Asendatud uue vorminguga, mis põhineb ISO 20022 pain.001.001.09. | 
| **Asendatud teise funktsiooniga?**   | Jah |
| **Mõjutatud tootealad**         | Avaldus |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Taunitav: Austria pangad amortiseerivad EDICFACT-PAYMUL piiriüleste maksete jaoks 2022. aasta novembriks ja asendab selle XML-versiooni pain.001.001.09N. Globaalse konfiguratsiooni hoidlasse on lisatud uus konfiguratsioon, mis võimaldab kasutajatel täita piiriüleste maksete taotlust. |

## <a name="features-removed-or-deprecated-in-the-finance-10030-release"></a>Finance'i väljalaskest 10.0.30 eemaldatud või aegunud funktsioonid

### <a name="revenue-recognition"></a>Tulu tuvastamine

[Tulu tuvastamine](../../finance/accounts-receivable/revenue-recognition-overview.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **Aegumise/eemaldamise põhjus** |Asendatud täiustatud funktsioonidega, kordustellimuse [arveldamine](../../finance/accounts-receivable/subscription-billing-summary.md)
| **Asendatud teise funktsiooniga?**   | Jah |
| **Mõjutatud tootealad** | Avaldus |
| **Juurutamissuvand** | Kõik |
| **Olek** | Taunitud: pärast 2023. aasta aprillini ei saa Dynamics 365 Financei tulu tuvastamise funktsioon enam vigaparanduste tuge. Klientidel palutakse kasutada täiustatud funktsioone, kordustellimuse [arveldust](../../finance/accounts-receivable/subscription-billing-summary.md). 2023. aasta oktoobers pole tulu tuvastamise funktsioon enam saadaval. Klientidel palutakse liikuda täiustatud kordustellimuse arveldusfunktsiooni juurde. Kogumifunktsiooni puhul, mis on tulu tuvastamise osa, ei ole praegu planeeritud asendusfunktsioone.|

## <a name="features-removed-or-deprecated-in-the-finance-10029-release"></a>Finance'i väljalaskest 10.0.29 eemaldatud või aegunud funktsioonid

### <a name="stock-transfer-orders-that-have-tax-on-the-transfer-price"></a>Lao üleviimistellimused, mille sisehinnale kehtib maks

[Lao üleviimistellimused, mille sisehinnale kehtib maks](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **Aegumise/eemaldamise põhjus** | Asendatud täiustatud funktsioonidega, [lao üleviimistellimused India jaoks](../../finance/localizations/apac-ind-stock-transfer.md)|
| **Asendatud teise funktsiooniga?**   | Jah |
| **Mõjutatud tootealad** | Avaldus |
| **Juurutamissuvand** | Kõik |
| **Olek** | Taunitud: pärast 2023. a. aprillit ei **saa** lao üleviimishinna funktsiooniga lao üleviimistellimused enam vigaste paranduste ja turbeparandustega tuge. Klientidel palutakse kasutada täiustatud funktsioone – India [lao üleviimistellimusi](../../finance/localizations/apac-ind-stock-transfer.md). Pärast 2023. aasta oktoober pole laoülekandetellimused, **mis omavad** ülekande hinna funktsioonil maksu, enam saadaval ja klientidel palutakse need teisaldada täiustatud funktsioonidele. |

### <a name="bank-statement-import-and-export-of-positive-pay-file"></a>Positiivse maksefaili pangaväljavõtte import ja eksport

| &nbsp;  | &nbsp;  |
|---|---|
| **Aegumise/eemaldamise põhjus** |Asendatud täiustatud funktsioonidega, importige pangaväljavõtted ja eksportige positiivse makse failid.| 
| **Asendatud teise funktsiooniga?**   | Jah |
| **Mõjutatud tootealad**         | Avaldus |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Taunitav: XSLT-funktsioon failide importimiseks ja eksportimiseks ei saa enam tuge paranduste ja turbeparandustega. Klientidel palutakse kasutada täiustatud funktsioone: [...](../../finance/accounts-payable/set-up-positive-pay-er.md)[seadistage positiivsed maksefailid elektroonilise aruandluse abil ja seadistage laiendatud panga vastavusseviimise importimine elektroonilise aruandluse abil](../../finance/accounts-payable/import-bai2-er.md). Pärast 2022. aasta septembrit pole XSLT-funktsioonid enam saadaval ja klientidel palutakse need teisaldada täiustatud funktsioonidele.|


## <a name="features-removed-or-deprecated-in-the-finance-10026-release"></a>Finance'i väljalaskest 10.0.26 eemaldatud või aegunud funktsioonid

### <a name="sales-tax-report-for-finland-design-based-on-reporting-codes"></a>Soome käibemaksuaruanne (aruandluskoodide põhjal põhinev kujundus)

[Soome käibemaksu aruanne](../localizations/emea-fin-sales-tax-payment-report-finland.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Asendatud uue KM-i deklaratsiooni kujundusega KM-i [deklaratsiooniga Soome jaoks](../localizations/emea-fin-vat-declaration.md) |
| **Asendatud teise funktsiooniga?**   | Jah |
| **Mõjutatud tootealad**         | Avaldus |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Taunitud: 1. märtsiks 2023 ei toeta me enam Soome käibemaksuaruannet (Soome aruande küljendus). Uus **KM-deklaratsiooni TXT (FI**) **ja KM-deklaratsiooni Exceli (FI)** elektroonilise aruandluse (ER) vormingud tuuakse sisse maksudeklaratsiooni **mudeli** alusel. |

## <a name="features-removed-or-deprecated-in-the-finance-10024-release"></a>Finance'i väljalaskest 10.0.24 eemaldatud või aegunud funktsioonid

### <a name="sales-tax-report-for-sweden-design-based-on-reporting-codes"></a>Rootsi käibemaksuaruanne (aruandluskoodide põhjal põhinev kujundus)

[Rootsi käibemaksu aruanne](../localizations/emea-swe-sales-tax-payment-report-sweden.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Asendatud uue KM-i deklaratsiooni kujundusega, [KM-i deklaratsioon Rootsi jaoks](../localizations/emea-swe-vat-declaration-sweden.md) |
| **Asendatud teise funktsiooniga?**   | Jah |
| **Mõjutatud tootealad**         | Avaldus |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Taunitud: 1. detsembriks 2022 ei toeta me enam Rootsi käibemaksuaruannet (Rootsi aruande küljendus). Maksudeklaratsiooni **mudelis tutvustatakse uut KM-deklaratsiooni XML-i (SE** **) ja KM-deklaratsiooni Exceli (SE)** elektroonilise aruandluse (ER) **vormingut**. |

### <a name="vat-statement-for-austria-design-based-on-reporting-codes"></a>Austria KM-aruanne (aruandluskoodide põhjal kujundus)

[KM-aruande üksikasjad Austria puhul](../localizations/emea-aut-vat-statement-details.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Asendatud uue KM-i deklaratsiooni kujundusega, [KM-i deklaratsiooniga Austria jaoks](../localizations/emea-aut-vat-declaration-austria.md) |
| **Asendatud teise funktsiooniga?**   | Jah |
| **Mõjutatud tootealad**         | Avaldus |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Taunitud: 1. detsembriks 2022 **ei toeta me enam KM-i deklaratsiooni (AT) elektroonilise aruandluse (ER)** **vormingut KM-i deklaratsiooni mudeli all**. Uus **KM-deklaratsiooni XML-i (AT)** **ja KM-deklaratsiooni Exceli (AT)** vormingud tuuakse sisse maksudeklaratsiooni **mudeli** alusel. |

### <a name="elster-declaration-for-germany-design-based-on-reporting-codes"></a>ELSTER-i deklaratsioon Saksamaa jaoks (aruandluskoodide põhjal kujundus)

[KM-aruanne](../localizations/emea-de-vat-declaration.md)</br>
[Saate häälestada saksamaa elektroonilist maksudeklaratsiooni.](../../fin-ops-core/dev-itpro/analytics/tasks/setup-electronic-tax-declaration-germany.md)</br>
[KM-deklaratsiooni (ELSTER) elektrooniline edastamine](../localizations/tasks/de-00003-electronic-transmission-elster.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Asendatud uue KM-i deklaratsiooni kujundusega, [KM-i deklaratsiooniga Saksamaa jaoks](../localizations/emea-deu-vat-declaration-germany.md) |
| **Asendatud teise funktsiooniga?**   | Jah |
| **Mõjutatud tootealad**         | Avaldus |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Taunitud: 1. detsembriks 2022 **ei plaani me enam Elsteri (DE)** **ja Elsteri** mudeli elektroonilise aruandluse (ER) vorminguid toetada. Uus **KM-deklaratsiooni XML-i (DE)** **ja KM-deklaratsiooni Exceli (DE)** vormingud tuuakse sisse maksudeklaratsiooni **mudeli** alusel. |

### <a name="ob-declaration-for-netherlands-design-based-on-reporting-codes"></a>OB-deklaratsioon Hollandi jaoks (aruandluskoodide põhjal kujundus)

[OB-deklaratsioon](../localizations/emea-nl-vat-declaration.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Asendatud uue KM-i deklaratsiooni kujundusega, [Hollandi KM-i deklaratsiooniga](../localizations/emea-nl-vat-declaration-netherlands.md) |
| **Asendatud teise funktsiooniga?**   | Jah |
| **Mõjutatud tootealad**         | Avaldus |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Taunitud: 1. detsembriks 2022 **ei plaani me enam toetada OB-deklaratsiooni (NL)** **ja OB-deklaratsioonimudeli** elektroonilise aruandluse (ER) vorminguid. Uue **KM-deklaratsiooni XML-i (NL)** **ja KM-deklaratsiooni Exceli (NL)** vormingud tuuakse sisse maksudeklaratsiooni **mudeli** alusel. |

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
| **Mõjutatud tootealad**         | Dynamics 365 finantside, tarneahela halduse ja projektitoimingute tooted|
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegumine: 01. aprilliks 2022 ei plaani me enam Lifecycle Services (LCS) hoidlat elektroonilise aruandluse Microsoft Dynamics (ER) konfiguratsioonide talletusvalikuna toetada. Uued Microsofti ER-i konfiguratsioonid avaldatakse allalaadimiseks ainult globaalsest hoidlast. Globaalsele hoidlale pääseb juurde Dynamics 365 toodetest ja RCS-ist. Lisateavet vt [ER-i konfiguratsioonide importimine RCS-st](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) ja [Regulatory Configuration Service – Lifecycle Services salvestuse aegumine](../localizations/rcs-lcs-repo-dep-faq.md). |

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

