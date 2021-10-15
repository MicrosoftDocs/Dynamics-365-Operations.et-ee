---
title: Mis on Dynamics 365 Supply Chain Managementi versioonis 10.0.21 uut või mida on muudetud (oktoober 2021)
description: Selles teemas kirjeldatakse Dynamics 365 Supply Chain Management 10.0.21 uusi või muutunud funktsioone.
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 894686446436a390ec2d019672e3a2b8b0e5f5ef
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579732"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10021-october-2021"></a>Mis on Dynamics 365 Supply Chain Managementi versioonis 10.0.21 uut või mida on muudetud (oktoober 2021)

[!include [banner](../includes/banner.md)]

Selles teemas loendatakse Microsoft Dynamics 365 Supply Chain Managementi versiooni 10.0.21 uusi või muutunud funktsioone. Selle versiooni number on 10.0.960 ja see on saadaval järgmiselt:

- **Eelvaateversiooni välja andmine:** august 2021
- **Väljalaske üldine kättesaadavus (enesevärskendus):** september 2021
- **Väljalaske üldine kättesaadavus (automaatne värskendamine):** oktoober 2021

## <a name="features-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

See väljalase hõlmab järgmisi funktsioone. Veerg *Funktsioon* pakub linke [väljalaskeplaani](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) kus saate vaadata iga funktsiooni ametlikke väljalaskekuupäevi. Veerg *Lisateave* pakub üksikasju/linke seotud dokumentatsioonile.

Suurem osa neist funktsioonidest tuleb enne kasutamist [Funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) abil lubada.

| Funktsiooniala | Funktsioon | Lisateave |
|---|---|---|
| Varud&nbsp;ja&nbsp;logistika | [Global Inventory Accounting on lisandmoodul Dynamics 365 Supply Chain Management](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/global-inventory-accounting-add-in-dynamics-365-supply-chain-management) | [Globaalse laoarvestuse kodulehekülg](../global-inventory-accounting/global-inventory-accounting-home.md) |
| Varud&nbsp;ja&nbsp;logistika | [Funktsiooni nimi: sisestage vaba kaubavaru korrigeerimised, kasutades vastaskontodega ühendatud konfigureeritavaid põhjusekoode](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/post-on-hand-adjustments-using-configurable-reason-codes-connected-offset-accounts) | [Varude inventuuri põhjusekoodid](../warehousing/reason-codes-for-counting-journals.md) |
| Varud&nbsp;ja&nbsp;logistika | [Müügipakkumisele viitavate andmete ekspordipoliitika](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy) | Valige, kas hinnapakkumistega viidatud andmete muudatuste tõttu kaasatakse need hinnapakkumised (või read) järgmisele ekspordile. Kui otsustate selliseid pakkumisi või ridu mitte kaasata, siis järkjärguline eksportimine toimub kiiremini.<br><br>See funktsioon lisab sätte **Vahele jäetud müügipakkumise viidatud andmed muudatuste jälgimise ajal** **Müügireskontro parameetrid** lehele. |
| Varud&nbsp;ja&nbsp;logistika | Pitseeritud pakkumine <!-- KFM: Add RP link when available --> | [Pitseeritud pakkumine pakkumiskutsete puhul](../procurement/sealed-bidding.md) |
| Varud&nbsp;ja&nbsp;logistika | [Skannige vöötkoode laos, kasutades GS1-vormingu standardeid](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | [GS1 vöötkoodid ja QR-koodid](../warehousing/gs1-barcodes.md) |
| Varud&nbsp;ja&nbsp;logistika | [Varude nähtavuse lisandmooduli esialgne reserveerimine](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/soft-reservation-inventory-visibility-add-in) | [Varude nähtavuse reserveeringud](../inventory/inventory-visibility-reservations.md) |
| Varud&nbsp;ja&nbsp;logistika | [Mahaarvamise ja tegeliku kaalu täiustused tagasimaksehalduse jaoks](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/deduction-catch-weight-enhancements-rebate-management) | [Mahaarvamise töölaual mahaarvamiste haldamine](../rebate-management/deduction-workbench.md )<br><br>[Tagasimaksete töötlemine, läbivaatamine ja sisestamine](../rebate-management/process-review-post.md)<br><br>[Tagasimakse halduse tehingud](../rebate-management/rebate-management-deals.md) |
| Varud&nbsp;ja&nbsp;logistika | [Laorakenduse etapi juhised](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Mobiilirakenduse Warehouse Management etapi pealkirjade ja juhiste kohandamine](../warehousing/mobile-app-titles-instructions.md) |
| Varud&nbsp;ja&nbsp;logistika | [Väljaminev kulu tööpauside ja jälgimisvärskenduste jälitamine](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/work-breaks-tracking-updates-landed-cost) | [Värskenda ärapanemiseks jälgimist](../landed-cost/update-tracking-putaway.md )<br><br>[Transiidis olevate kaupade töötlemine](../landed-cost/in-transit-processing.md) |
| Koondplaneerimine | [Planeerimise optimeerimise negatiivsed päevad](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/negative-days-support-planning-optimization) | [Viivituse kõikumine (negatiivsed päevad)](../master-planning/planning-optimization/delay-tolerance.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selle väljalaske funktsioonide täiustused. Igaüks neist võimaldab olemasoleva funktsiooni järk-haaval täiustada. Kuna need on ainult täiustused, siis neid ei loetleta [väljalaskeplaanis](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Kindlustamaks, et need täiustused ei satu vastuollu olemasolevate kohanduste või eelistustega, lülitatakse iga neist vaikimisi välja (kui pole märgitud teisiti). Kui soovite mõnda neist funktsioonidest kasutada, peate need eraldi lubama [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Funktsiooniala | Funktsiooni&nbsp;nimi&nbsp;funtsiooni&nbsp;halduses | Lisateave |
|---|---|---|
| Kuluhaldus | Varude sulgemise edenemise üksikasjad | See eelvaate funktsioon võimaldab varude sulgemise edenemise üksikasjalikku kuva. |
| Hanked | Vältige eelarvereservi ületarbimist, kui töövoos on mitu ostutaotlust | See eelvaate funktsioon parandab tõrkekontrolli, kui kasutajad esitavad ja kinnitavad ostutaotlusi, mis ületavad üldise eelarve reserveerimisrea järelejäänud saldot. See aitab vältida üldise eelarvereserveeringu ülepidamist, kui töövoos on mitu ostutaotlust. |
| Tootmise juhtimine | Kuva tootmisosakonna täideviimisliidese täielikud seeria-, partii- ja numbrimärginumbrid | See funktsioon pakub täiustatud kogemust seeria-, partii- ja litsentsiplaadinumbrite loendite vaatamiseks tootmispinna käivitamise liideses. Kuva muutused piiratud arvu märkidega kaardivaates loendivaatesse, mis pakub täisväärtuste näitamiseks piisavalt ruumi. Loend võimaldab ka otsida kindlaid numbreid. |
| Müük ja turundus | Postitamiseks valitavate müügitellimuste arvu piiramine | See funktsioon võimaldab teil määratleda maksimaalse müügitellimuste arvu, mida saab valida kinnituste, komplekteerimislehtede, saatelehtede ja arvete sisestamisel müügitellimuste loendilehelt. See lubatakse automaatselt. Funktsioon lisab lehele **Müügireskontro parameetrid** sätte **Müügitellimuste maksimumarv sisestamisel**. Uue sätte vaikeväärtus on *100*. See funktsioon aitab parandada müügitellimuste loendilehe jõudlust, kui valitud on märkimisväärne arv müügitellimusi. See ei mõjuta müügitellimuste arvu, mida töötleb perioodiline ülesanne. |
| Laohaldus | ASN-idest kõrvalepaneku töö eradamine | See funktsioon on vajalik saadetise eelteatiste (ASN-ide) saatmiseks ja vastuvõtuks, kui käitate laohalduse töökoormust kaaluühikul (osana jaotatud topoloogiast). See lisab uue andmebaasi tabeli, mis on mõeldud put lisatöö teabe salvestamiseks. Varem talletati seda teavet tabelites ka ASN-ide jaoks. |
| Laohaldus | Pesa segaühikud | Lubab süsteemil pesaüksused asukohtadesse, mis sisaldavad segaühikuid (nt kastid ja kastid). Iga pesastatud mallirea puhul võimaldab see funktsioon teil valida, kas rida peaks kaupu avama segaühiku või ühe ühiku asukohta. |
| Laohaldus | Kasutage pakkimisjaamas konteinerite sulgemiseks / uuesti avamiseks kiiremat API-d | Kui see eelvaate funktsioon on lubatud, luuakse konteineritega seotud laokanded, kasutades uut kerge kaalu protsessi, mis parandab konteinerite sulgemise või taasavamise jõudlust pakkejaama käsitsi töötlemisel. |

## <a name="new-and-updated-documentation-resources"></a>Uued ja värskendatud dokumentatsiooni ressursid

Oleme hiljuti lisanud või oluliselt uuendanud järgmisi abiteemasid. Need ei ole tingimata seotud sellele väljalaskele lisatud uute funktsioonidega, nagu on loetletud eelmises jaotises, kuid need võivad aidata teil olemasolevatest funktsioonidest rohkem kasu saada.

| Funktsiooniala | Uued või värskendatud teemad |
|---|---|
| Koondplaneerimine | [Varude eelarved](../master-planning/inventory-forecast.md) |
| Koondplaneerimine | [Parameetrid, mida planeerimise optimeerimine ei kasuta](../master-planning/planning-optimization/not-used-parameters.md) |
| Koondplaneerimine | [Täiendamismeetodid ja koguse muutmine](../master-planning/planning-optimization/replenishment-methods-quantity-modification.md) |
| Koondplaneerimine | [Piiramatu võimsusega planeerimine](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| Koondplaneerimine | [Plaaniajaloo ja plaanimislogide kuvamine](../master-planning/planning-optimization/plan-history-logs.md) |
| Laohaldus | [Konteineri pakkimise strateegiad](../warehousing/container-packing-strategy-overview.md) |
| Laohaldus | [Tsüklilise inventuuri näidisstsenaariumid](../warehousing/cycle-counting-scenarios.md) |
| Laohaldus | [Sissetulevate ASN-ide importimine V2 andmeüksuse kaudu](../warehousing/import-asn-v2-data-entity.md) |
| Laohaldus | [Müügitellimuste ja üleviimistellimuste ülekorjamine](../warehousing/over-picking-for-sales-and-transfer-orders.md) |
| Laohaldus | [Voosildi printimise ajastamine voo ajal](../warehousing/configure-task-based-wave-label-printing.md) |
| Laohaldus | [Mis on uut või muudetud Warehouse Management laohalduse mobiilirakenduses](../warehousing/whats-new-wma.md) |

## <a name="additional-resources"></a>Lisaressursid

### <a name="platform-updates-for-finance-and-operations-apps"></a>Teenuse Finance and Operations rakenduste platvormivärskendused

Microsoft Dynamics 365 Supply Chain Management 10.0.21 sisaldab platvormivärskendusi. Lisateavet leiate teemast [Finance and Operationsi rakenduste versiooni 10.0.21 platvormivärskendused (oktoober 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21.md).

### <a name="bug-fixes"></a>Veaparandused

Lisateabe saamiseks veaparanduste kohta, mis sisalduvad 10.0.21 uuendustes, logige sisse teenusesse Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=605166&dbType=3&qc=4b9449bf0d947113983bd0697140bf4d8727bfafd5566aa682cb38db343374de).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 ja majandusharu pilved: 2021 väljalaskevoo 2 plaan

Kas teile pakuvad huvi meie ärirakenduste või platvormi uued ja hiljuti väljaantud võimalused?

Vaadake [Dynamics 365 ja majandusharu pilved: 2021 väljalaskevoo 2 plaan](/dynamics365-release-plan/2021wave2/). Käsitleme ühes dokumendis kõiki üksikasju otsast lõpuni ja ülevalt alla, millest võite plaanide tegemisel lähtuda.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Eemaldatud ja aegunud Supply Chain Managementi funktsioonid

Teemas [Eemaldatud või aegunud Dynamics 365 Supply Chain Managementi funktsioonid](removed-deprecated-features-scm-updates.md) kirjeldatakse funktsioone, mis on eemaldatud või aegunud või kavandatakse eemaldada Supply Chain Managementist.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

Enne mis tahes funktsiooni eemaldamist tootest, teavitatakse aegumisest 12 kuud ette teemas [Eemaldatud või aegunud Dynamics 365 Supply Chain Managementi funktsioonid](removed-deprecated-features-scm-updates.md).

Murranguliste muudatuste puhul, mis mõjutavad ainult kompileerimise aega, kuid on binaarselt ühilduvad liivakasti- ja tootmiskeskkondadega, on aegumise aeg vähem kui 12 kuud. Need on tavaliselt funktsionaalsed uuendused, mida tuleb teha kompilaatori jaoks.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
