---
title: Mis on Dynamics 365 Supply Chain Managementi versioonis 10.0.21 uut või mida on muudetud (oktoober 2021)
description: See artikkel kirjeldab funktsioone, mis on uued või muutunud Dynamics 365 Supply Chain Management 10.0.21-s.
author: kamaybac
ms.date: 10/28/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a78b4c37bfca9fedbd46cd8a16b47bd4444fbfee
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849528"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10021-october-2021"></a>Mis on Dynamics 365 Supply Chain Managementi versioonis 10.0.21 uut või mida on muudetud (oktoober 2021)

[!include [banner](../includes/banner.md)]

See artikkel loetleb funktsioonid, mis on Microsofti versioonis Dynamics 365 Supply Chain Management 10.0.21 uued või muutunud. Selle versiooni number on 10.0.960 ja see on saadaval järgmiselt:

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
| Varud&nbsp;ja&nbsp;logistika | [Pitseeritud pakkumine](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sealed-bidding) | [Pitseeritud pakkumine pakkumiskutsete puhul](../procurement/sealed-bidding.md) |
| Varud&nbsp;ja&nbsp;logistika | [Varude nähtavuse lisandmooduli esialgne reserveerimine](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/soft-reservation-inventory-visibility-add-in) | [Varude nähtavuse reserveeringud](../inventory/inventory-visibility-reservations.md) |
| Varud&nbsp;ja&nbsp;logistika | [Mahaarvamise ja tegeliku kaalu täiustused tagasimaksehalduse jaoks](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/deduction-catch-weight-enhancements-rebate-management) | [Mahaarvamise töölaual mahaarvamiste haldamine](../rebate-management/deduction-workbench.md )<br><br>[Tagasimaksete töötlemine, läbivaatamine ja sisestamine](../rebate-management/process-review-post.md)<br><br>[Tagasimakse halduse tehingud](../rebate-management/rebate-management-deals.md) |
| Varud&nbsp;ja&nbsp;logistika | [Laorakenduse etapi juhised](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Mobiilirakenduse Warehouse Management etapi pealkirjade ja juhiste kohandamine](../warehousing/mobile-app-titles-instructions.md) |
| Varud&nbsp;ja&nbsp;logistika | [Väljaminev kulu tööpauside ja jälgimisvärskenduste jälitamine](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/work-breaks-tracking-updates-landed-cost) | [Värskenda ärapanemiseks jälgimist](../landed-cost/update-tracking-putaway.md )<br><br>[Transiidis olevate kaupade töötlemine](../landed-cost/in-transit-processing.md) |
| Koondplaneerimine | [Planeerimise optimeerimise negatiivsed päevad](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/negative-days-support-planning-optimization) | [Viivituse kõikumine (negatiivsed päevad)](../master-planning/planning-optimization/delay-tolerance.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selle väljalaske funktsioonide täiustused. Igaüks neist võimaldab olemasoleva funktsiooni järk-haaval täiustada. Kuna need on ainult täiustused, siis neid ei loetleta [väljalaskeplaanis](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Kindlustamaks, et need täiustused ei satu vastuollu olemasolevate kohanduste või eelistustega, lülitatakse iga neist vaikimisi välja (kui pole märgitud teisiti). Kui soovite mõnda neist funktsioonidest kasutada, peate need eraldi lubama [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Moodul | Funktsiooni&nbsp;nimi&nbsp;funtsiooni&nbsp;halduses | Lisateave |
|---|---|---|
| Kuluhaldus | Varude sulgemise edenemise üksikasjad | See eelvaate funktsioon võimaldab varude sulgemise edenemise üksikasjalikku kuva. |
| Hanked | Vältige eelarvereservi ületarbimist, kui töövoos on mitu ostutaotlust | See eelvaate funktsioon parandab tõrkekontrolli, kui kasutajad esitavad ja kinnitavad ostutaotlusi, mis ületavad üldise eelarve reserveerimisrea järelejäänud saldot. See aitab vältida üldise eelarvereserveeringu ülepidamist, kui töövoos on mitu ostutaotlust. |
| Tootmise juhtimine | Kuva tootmisosakonna täideviimisliidese täielikud seeria-, partii- ja numbrimärginumbrid | See funktsioon pakub täiustatud kogemust seeria-, partii- ja litsentsiplaadinumbrite loendite vaatamiseks tootmispinna käivitamise liideses. Kuva muutused piiratud arvu märkidega kaardivaates loendivaatesse, mis pakub täisväärtuste näitamiseks piisavalt ruumi. Loend võimaldab ka otsida kindlaid numbreid. |
| Müük ja turundus | Postitamiseks valitavate müügitellimuste arvu piiramine | See funktsioon võimaldab teil määratleda maksimaalse müügitellimuste arvu, mida saab valida kinnituste, komplekteerimislehtede, saatelehtede ja arvete sisestamisel müügitellimuste loendilehelt. See lubatakse automaatselt. Funktsioon lisab lehele **Müügireskontro parameetrid** sätte **Müügitellimuste maksimumarv sisestamisel**. Uue sätte vaikeväärtus on *100*. See funktsioon aitab parandada müügitellimuste loendilehe jõudlust, kui valitud on märkimisväärne arv müügitellimusi. See ei mõjuta müügitellimuste arvu, mida töötleb perioodiline ülesanne. |
| Laohaldus | ASN-idest kõrvalepaneku töö eradamine | See funktsioon on vajalik saadetise eelteatiste (ASN-ide) saatmiseks ja vastuvõtuks, kui käitate laohalduse töökoormust kaaluühikul (osana jaotatud topoloogiast). See lisab uue andmebaasi tabeli, mis on mõeldud put lisatöö teabe salvestamiseks. Varem talletati seda teavet tabelites ka ASN-ide jaoks. |
| Laohaldus | Pesa segaühikud | Lubab süsteemil pesaüksused asukohtadesse, mis sisaldavad segaühikuid (nt kastid ja kastid). Iga pesastatud mallirea puhul võimaldab see funktsioon teil valida, kas rida peaks kaupu avama segaühiku või ühe ühiku asukohta. |
| Laohaldus | Kasutage pakkimisjaamas konteinerite sulgemiseks / uuesti avamiseks kiiremat API-d | Kui see eelvaate funktsioon on lubatud, luuakse konteineritega seotud laokanded, kasutades uut kerge kaalu protsessi, mis parandab konteinerite sulgemise või taasavamise jõudlust pakkejaama käsitsi töötlemisel. |

## <a name="features-turned-on-by-default-in-this-release"></a>Funktsioonid on selles versioonis vaikimisi sisse lülitatud

Järgmises tabelis on loetletud funktsioonid, mis on versioonis 10.0.21 vaikimisi sisse lülitatud. Enamiku aatomiliselt sisse lülitatud funktsioone saab sisse lülitada jaotises [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Funktsiooni nimi | Lubamise kuupäev | Funktsioon lisati | Funktsiooni olek | Moodul |
| :--- | :--- | :--- | :--- | :--- |
| Vaba kaubavaru aruande talletamine | 9/1/2021 | 4/1/2020 | Vaikimisi sees | Varude ja laohaldus |
| Ülekandetellimuse tühistamine | 9/1/2021 | 7/13/2020 | Vaikimisi sees | Varude ja laohaldus |
| Ava varude tööleht | 9/1/2021 | 8/17/2020 | Vaikimisi sees | Varude ja laohaldus |
| Varude haldamise salvestatud vaated | 9/1/2021 | 30.9.2020 | Vaikimisi sees | Varude ja laohaldus |
| Koosluseversioonile navigeerimine koosluseridadelt | 9/1/2021 | 11/11/2019 | Vaikimisi sees | Varude ja laohaldus |
| Mõõtühiku ja ühikukoguse kasutamine laotöölehtedel | 9/1/2021 | 11/11/2019 | Vaikimisi sees | Varude ja laohaldus |
| Luba tühjade partii atribuutide väärtused | 9/1/2021 | 11/11/2019 | Vaikimisi sees | Varude ja laohaldus |
| Suurenda automaatselt lao üleviimistellimuse ridade numbreid | 9/1/2021 | 10/11/2019 | Vaikimisi sees | Varude ja laohaldus |
| Varude töölehe kinnitamise töövoog | 9/1/2021 | 1/6/2020 | Vaikimisi sees | Varude ja laohaldus |
| Luba varude kvaliteedihalduse parameetrite hoiatuse funktsioon | 9/1/2021 | 10/7/2019 | Vaikimisi sees | Varude ja laohaldus |
| Loo müügirealt üleviimistellimus | 9/1/2021 | 8/31/2019 | Vaikimisi sees | Varude ja laohaldus |
| Prognoosimudeli valimine nõudluse prognoosi üksikasjades | 9/1/2021 | 10/11/2019 | Vaikimisi sees | Koondplaneerimine |
| Koondplaneerimise edenemise visualiseerimine | 9/1/2021 | 10/7/2019 | Vaikimisi sees | Koondplaneerimine |
| Automaatkinnitamine planeerimise optimeerimiseks | 9/1/2021 | 10/11/2019 | Vaikimisi sees | Koondplaneerimine |
| Plaanitud tellimuste paralleelne kinnitamine | 9/1/2021 | 8/31/2019 | Vaikimisi sees | Koondplaneerimine |
| Pakkumise esitamise edu sõnum | 9/1/2021 | 5/15/2019 | Vaikimisi sees | Hanked |
| Ostutellimusele on lisatud pakkumiskutse viite link | 9/1/2021 | 8/31/2019 | Vaikimisi sees | Hanked |
| Võimalus kinnitada hankijakoostööst aktsepteeritud ostutellimused partiina | 9/1/2021 | 9/10/2019 | Vaikimisi sees | Hanked |
| cXML-i täiustuste ostmine | 9/1/2021 | 11/11/2019 | Vaikimisi sees | Hanked |
| Kuvage link &quot;Ava avaldatud hinnapäringud&quot; paanina | 9/1/2021 | 30.9.2020 | Vaikimisi sees | Hanked |
| Pakkumiskutse küsimused ja vastused | 9/1/2021 | 2/19/2020 | Vaikimisi sees | Hanked |
| Toote ohtlike materjalide teave ja saatmisdokumentatsioon | 9/1/2021 | 6/14/2020 | Vaikimisi sees | Tooteteabe haldus |
| Vaiketellimuse koguste range kinnitamine | 9/1/2021 | 6/24/2020 | Vaikimisi sees | Tooteteabe haldus |
| Päritoluriigi haldamise funktsioon | 9/1/2021 | 7/13/2020 | Vaikimisi sees | Tooteteabe haldus |
| Väljastatud toodete salvestatud vaated | 9/1/2021 | 30.9.2020 | Vaikimisi sees | Tooteteabe haldus |
| Täiustused dialoogides Kinnita ja Ülekandmistööd | 9/1/2021 | 10/11/2019 | Vaikimisi sees | Tootmise juhtimine |
| Töökaardi vahendile on lisatud lõpetatuks märkimise litsentsiplaat | 9/1/2021 | 8/31/2019 | Vaikimisi sees | Tootmise juhtimine |
| Töökaardi terminali lehele on lisatud uus nupp Pausi peatamiseks | 9/1/2021 | 2/19/2020 | Vaikimisi sees | Tootmise juhtimine |
| Lubage allhankelepingu alusel sõlmitud kaupade osaline vastuvõtmine ja parandage hankija tüüpi BOM-ridade praagi arvutamisega seotud probleem. | 9/1/2021 | 11/11/2019 | Vaikimisi sees | Tootmise juhtimine |
| Tootmisjuhtimise salvestatud vaated | 9/1/2021 | 8/17/2020 | Vaikimisi sees | Tootmise juhtimine |
| Dynamics 365 Guides tootmise jaoks | 9/1/2021 | 7/13/2020 | Vaikimisi sees | Tootmise juhtimine |
| Tootmisosakonna täideviimine | 9/1/2021 | 30.9.2020 | Vaikimisi sees | Tootmise juhtimine |
| Funktsioon töökaardi seadme ja töökaardi terminali lukustamiseks, et neid saaks puhastada | 9/1/2021 | 5/10/2020 | Vaikimisi sees | Tootmise juhtimine |
| Tasude eraldamine müügitellimusel | 9/1/2021 | 30.9.2020 | Vaikimisi sees | Müük ja turundus |
| Postitamiseks valitavate müügitellimuste arvu piiramine | 9/1/2021 | 9/1/2021 | Vaikimisi sees | Müük ja turundus |
| Müügitellimuse värskendamise ajaloo puhastamine | 9/1/2021 | 9/1/2021 | Vaikimisi sees | Müük ja turundus |
| Muutke tsüklilise inventuuri töö numbriseeriat | 9/1/2021 | 10/7/2019 | Vaikimisi sees | Laohaldus |
| Toimingupõhine voonõude täiendamine | 9/1/2021 | 10/7/2019 | Kohustuslik | Laohaldus |
| Peida summa väli lehtedel &quot;Kogu laadung&quot; ja &quot;Kooremi üksikasjad&quot; | 9/1/2021 | 10/7/2019 | Vaikimisi sees | Laohaldus |
| Voosildi printimine | 9/1/2021 | 2/19/2020 | Kohustuslik | Laohaldus |
| Ostutellimuse varude kannete seostamine koormusega | 9/1/2021 | 1/6/2020 | Kohustuslik | Laohaldus |
| Täiustatud litsentsiplaadi sildipaigutused | 9/1/2021 | 2/19/2020 | Vaikimisi sees | Laohaldus |
| Organisatsiooniülene töö blokeerimine | 9/1/2021 | 2/19/2020 | Kohustuslik | Laohaldus |
| Töörea üksikasjad | 9/1/2021 | 10/11/2019 | Vaikimisi sees | Laohaldus |
| Muuda mobiilse seadme varude liikumise varude oleku väli redigeeritavaks | 9/1/2021 | 10/16/2019 | Vaikimisi sees | Laohaldus |
| Pakett-töös väljuvate saadetiste kinnitamine | 9/1/2021 | 7/13/2020 | Vaikimisi sees | Laohaldus |
| Saate kontrollida, kas mobiilsetes seadmetes kuvatakse vastuvõtu kokkuvõttelehte | 9/1/2021 | 4/1/2020 | Vaikimisi sees | Laohaldus |
| Viip mitmetähendusliku &#39;Loc / LP&#39; nimede lahendamiseks | 9/1/2021 | 4/1/2020 | Vaikimisi sees | Laohaldus |
| Jäädvusta lao rakenduses koorma kaupade vastuvõtmise ajal tootevariandid ja jälgimisdimensioonid | 9/1/2021 | 5/10/2020 | Vaikimisi sees | Laohaldus |
| Ärge lubage luua koormaid, mis ei vasta voo koormuse koostamismalli nõuetele. | 9/1/2021 | 8/17/2020 | Vaikimisi sees | Laohaldus |
| Mitme SKU asukohakorralduste kõigi toimingute hindamine | 9/1/2021 | 30.9.2020 | Vaikimisi sees | Laohaldus |

## <a name="new-and-updated-documentation-resources"></a>Uued ja värskendatud dokumentatsiooni ressursid

Oleme hiljuti lisanud või oluliselt uuendanud järgmised spikriartiklid. Need ei ole tingimata seotud sellele väljalaskele lisatud uute funktsioonidega, nagu on loetletud eelmises jaotises, kuid need võivad aidata teil olemasolevatest funktsioonidest rohkem kasu saada.

| Funktsiooniala | Uued või värskendatud artiklid |
|---|---|
| Koondplaneerimine | [Varude eelarved](../master-planning/inventory-forecast.md) |
| Koondplaneerimine | [Parameetrid, mida planeerimise optimeerimine ei kasuta](../master-planning/planning-optimization/not-used-parameters.md) |
| Koondplaneerimine | [Täiendamismeetodid ja koguse muutmine](../master-planning/planning-optimization/replenishment-methods-quantity-modification.md) |
| Koondplaneerimine | [Piiramatu võimsusega planeerimine](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| Koondplaneerimine | [Plaaniajaloo ja plaanimislogide kuvamine](../master-planning/planning-optimization/plan-history-logs.md) |
| Laohaldus | [Konteineri pakkimise strateegiad](../warehousing/container-packing-strategy-overview.md) |
| Laohaldus | [Tsüklilise inventuuri näidisstsenaariumid](../warehousing/cycle-counting-scenarios.md) |
| Laohaldus | [Sissetulevate ASN-ide importimine V3 andmeüksuse kaudu](../warehousing/import-asn-data-entity.md) |
| Laohaldus | [Müügitellimuste ja üleviimistellimuste ülekorjamine](../warehousing/over-picking-for-sales-and-transfer-orders.md) |
| Laohaldus | [Voosildi printimise ajastamine voo ajal](../warehousing/configure-task-based-wave-label-printing.md) |
| Laohaldus | [Mis on uut või muudetud Warehouse Management laohalduse mobiilirakenduses](../warehousing/whats-new-wma.md) |

## <a name="additional-resources"></a>Lisaressursid

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finantside ja toimingute rakenduste platvormi värskendused

Microsoft Dynamics 365 Supply Chain Management 10.0.21 sisaldab platvormivärskendusi. Lisateavet vt Platvormi värskendustest [versioonile 10.0.21 Finance and Operations rakendustest (oktoober 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21.md).

### <a name="bug-fixes"></a>Veaparandused

Lisateabe saamiseks veaparanduste kohta, mis sisalduvad 10.0.21 uuendustes, logige sisse teenusesse Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=605166&dbType=3&qc=4b9449bf0d947113983bd0697140bf4d8727bfafd5566aa682cb38db343374de).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 ja majandusharu pilved: 2021 väljalaskevoo 2 plaan

Kas teile pakuvad huvi meie ärirakenduste või platvormi uued ja hiljuti väljaantud võimalused?

Vaadake [Dynamics 365 ja majandusharu pilved: 2021 väljalaskevoo 2 plaan](/dynamics365-release-plan/2021wave2/). Käsitleme ühes dokumendis kõiki üksikasju otsast lõpuni ja ülevalt alla, millest võite plaanide tegemisel lähtuda.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Eemaldatud ja aegunud Supply Chain Managementi funktsioonid

Artikli [eemaldatud või taunitud Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) funktsioonid kirjeldavad funktsioone, mis on tarneahela halduses eemaldatud või plaaniliselt eemaldatud või taunitud.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

Enne mis tahes funktsiooni eemaldamist tootest teatatakse amortiseerumisest [Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) artikli 12 kuu jooksul enne eemaldamist eemaldatud või taunitud funktsioonides.

Murranguliste muudatuste puhul, mis mõjutavad ainult kompileerimise aega, kuid on binaarselt ühilduvad liivakasti- ja tootmiskeskkondadega, on aegumise aeg vähem kui 12 kuud. Need on tavaliselt funktsionaalsed uuendused, mida tuleb teha kompilaatori jaoks.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
