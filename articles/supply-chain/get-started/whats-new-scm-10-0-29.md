---
title: Dynamics 365 Supply Chain Management 10.0.29 eelversioon (oktoober 2022)
description: See artikkel kirjeldab funktsioone, mis on Microsoft Dynamics 365 Supply Chain Management 10.0.29 uued või muutunud.
author: kamaybac
ms.date: 08/12/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 62e06f2348ca3524beaaef5d8879c199db56696f
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689279"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10029-october-2022"></a>Mis on Dynamics 365 Supply Chain Managementi versioonis 10.0.29 uut või mida on muudetud (oktoober 2022)

[!include [banner](../includes/banner.md)]

See artikkel loetleb funktsioonid, mis on Microsofti versioonis Dynamics 365 Supply Chain Management 10.0.29 uued või muutunud. Sellel versioonil on järgu number 10.0.1326 see on saadaval järgmises graafikus.

- **Eelvaateversiooni välja andmine:** august 2022
- **Väljalaske üldine kättesaadavus (enesevärskendus):** september 2022
- **Väljalaske üldine kättesaadavus (automaatne värskendamine):** oktoober 2022

## <a name="features-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selles versioonis sisalduvad funktsioonid. Võime seda artiklit värskendada, et kaasata funktsioonid, mis lisati koostesse pärast selle artikli algset avaldamist.

| Funktsiooniala | Funktsioon | Lisateave | Lubaja:   |
|---|---|---|---|
| Varud ja logistika | [WMS-kaupade eraldamine ja reserveerimine varude nähtavuses](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/allocate-reserve-whs-items-inventory-visibility) | Peagi tulekul | Vaikimisi lubatud |
| Varud ja logistika | [Sujuvamaks laoseisu loendite eellaadimine](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/query-inventory-visibility-summary-entity) | [Inventory Visibility rakenduse kasutamine](../inventory/inventory-visibility-power-platform.md) | Lubatud teenuse konfiguratsiooni järgi |
| Tellimuspõhise tarne automatiseerimine | [Tellimuspõhise tarne automatiseerimine](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-to-order-supply-automation) | [Tellimuspõhise tarne automatiseerimine](../master-planning/make-to-order-supply-automation.md) | Funktsioonihaldus:<br>*Tellimuspõhise tarne automatiseerimine* |
| Planeerimine | [Vaadake ja rakendage üksikasjalikke vihjeid DDMRP-le.](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/view-apply-detailed-insights-ddmrp) | [Nõudlusepõhiste materjalinõuete planeerimise ülevaade](../master-planning/planning-optimization/ddmrp-overview.md) | Funktsioonihaldus:<br>*(Eelversioon) Planeerimise optimeerimise DDMRP* |
| Tootmise juhtimine | [Lõpetatud kaupade enne töölehele sisestamist füüsiliselt kättesaadavaks tegemine](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-finished-goods-physically-before-posting) | [Lõpetatud kaupade enne töölehele sisestamist füüsiliselt kättesaadavaks tegemine](../production-control/deferred-posting.md) | Funktsioonihaldus:<br>*(Eelversioon) Lõpetatud kaupade enne töölehele sisestamist füüsiliselt kättesaadavaks tegemine* |
| Laohaldus | [Vastavate andmete otsige lao mobiilsest rakendusest.](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/look-up-relevant-data-within-warehouse-mobile-app) | [Andmepäringud Warehouse Managementi mobiilirakenduse kõrvalepõigete kaudu](../warehousing/warehouse-app-data-inquiry.md) | Funktsioonihaldus:<br>*Warehouse managementi rakenduse andmepäringu voog* |

## <a name="feature-enhancements-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selle väljalaske funktsioonide täiustused. Kõik need täiustused parandavad olemasolevat funktsiooni järk-järgult. Kuna need on ainult täiustused, siis neid ei loetleta [väljalaskeplaanis](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Kindlustamaks, et need täiustused ei satu vastuollu olemasolevate kohanduste või eelistustega, lülitatakse iga neist vaikimisi välja (kui pole märgitud teisiti).

Kui soovite mõne neist funktsioonidest sisse ja välja lülitada, peate seda funktsioonihalduses [tegema](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Moodul | Funktsiooni nimi funktsioonihalduses | Lisateave |
|---|---|---|
| Kuluhaldus | Hinnaarvutuse ootel kaastoote optimeerimine | See funktsioon parandab konflikti, mis võib vahel ilmneda, kui kaastoote hinnad arvutatakse mitme lõime abil. See tagab süsteemi, et iga kaastoote hind arvutatakse ainult üks kord. Selle arvutuse tulemust kasutatakse seejärel sisendina kõigi muude arvutuste puhul. Kui ootel hind on juba olemas, kasutatakse seda hinda. |
| Koondplaneerimine | Planeerimise optimeerimise grupikanded | See funktsioon võib aidata vähendada plaanitud tellimuste arvu, mis luuakse ühe müügitellimuse rea tarnimiseks planeerimise optimeerimise kasutamisel. Kui see funktsioon on sisse lülitatud, grupeerib planeerimise optimeerimine tellimuse rea kõik laokanded täieliku koguse jaoks üheks vajaduseks. (Selline käitumine vastab integreeritud plaanimismootori käitumisele.) Pakkumine ja nõudlus grupeeritakse eraldi. Seetõttu aitab see funktsioon vähendada kande mahtu, kui olete kandeid tükeldanud ja kui kasutate dimensioone (nt partiinumbreid või seerianumbreid), mis ei ole laovarude dimensioonid. |
| Hanked | Pane hankija ostutellimuste jaoks ootele | Selle funktsiooniga saate panna hankija ostutellimuste jaoks ootele. See lisab uue ostutellimuse *ootetüübi*, mis märgib hankija ostutellimuste jaoks ootele. Te ei saa luua uusi ostutellimusi hankijatele, kes on ostutellimuste jaoks ootel, kuid saate nende hankijate jaoks siiski jätkata mis tahes avatud arvete või maksetega. |
| Müük ja turundus | Arvuta rea netosumma importimisel | See funktsioon võimaldab teil kontrollida, kas süsteem peaks ridade kogusummad *ümber* arvutama, kui impordite andmeid müügitellimuse ridade, *müügipakkumise* ridade või tagastustellimuse ridade üksuse kaudu, *kasutades* OData või topeltkirjutust. See mõjutab ainult **seda**, kui teil on olemas ka kaubanduslelepingu hindamispoliitikad, mis piiravad muudatusi müügitellimuse ridade, müügipakkumise ridade ja/või tagastustellimuse ridade netosumma väljal. See lisab sätte Arvuta rea **netosumma Müügireskontrole** **, > seadistus > müügireskontro parameetrite** lehele. Kui see säte on seatud väärtusele *Jah*, arvutab süsteem alati vajaduse korral rea summad ümber (ignoreerides seega mis tahes kaubanduslelepingu hindamispoliitikat rea netosumma puhul). Kui sätte *väärtuseks on määratud Ei*, ei arvuta süsteem rea netosummat automaatselt ka siis, kui rea hinna, koguse ja/või allahindluse sissetulevad muudatused vadaksid rea netosumma ümberarvutamise. See funktsioon on vaikimisi lubatud ja algselt seadistab rea **netosumma arvutamise väärtuseks** *Jah*. Säte *Ei* vasta süsteemi käitumisele enne versiooni 10.0.23 ja seda pakutakse peamiselt pärandi integreerimisstsenaariumide toetamiseks.<br><br>Lisateavet vt teemast Rea [netosummade ümberarvutamine müügitellimuste, pakkumiste ja tagastuste importimisel](../sales-marketing/calc-line-net-amounts-import.md). |
| Müük ja turundus | Müügi kogusummade arvutamine mitme lõime abil | See funktsioon aitab parandada jõudlust, lubades süsteemil kasutada paralleeltöötlust partii müügi kogusummade arvutamisel. Funktsioon lisab dialoogiboksi Müügi kogusummade **arvutamine** uue lõimede **arvu**. Kui valite arvutuse pakktöötlusena, saate selle välja abil seadistada maksimaalse lõimede arvu. Kui seate väärtuseks *0* (null) või *1*, kasutatakse üksikut lõime. 1-st kõrgemal olevad väärtused võimaldavad töötlust. |
| Müük ja turundus | Värskenda kontsernisiseseks kasutuseks käsitsi sisestatud hindu ja allahindlusi | See funktsioon toetab kontsernisiseste tellimuste käsitsi muutmise poliitikaid. See hõlmab käsitsi muutmise poliitikate üleviimist kontsernisiseste müügi- ja ostutellimuste vahel. Varem toetati käsitsi muutmise poliitikaid ainult mitte kontsernisiseste tellimuste puhul. Kui see funktsioon on lubatud, annab süsteem teile võimaluse värskendada hindu ja allahindlusi pärast kontsernisisese tellimuse muudatuste salvestamist. Selle valikuga saate valida, kas soovite kontsernisisesele tellimusele rakendada uusi hindade ja allahindluste üksikasju või jätta tellimuse muutmata. |

## <a name="new-and-updated-documentation-resources"></a>Uued ja värskendatud dokumentatsiooni ressursid

Oleme hiljuti lisanud või oluliselt värskendanud järgmised spikriartiklid. Need artiklid ei pea tingimata olema seotud uute funktsioonidega, mis selle väljalaske jaoks lisati, nagu on loetletud eelmistes jaotistes. Kuid need võivad aidata teil rohkem olemasolevatest funktsioonidest välja saada.

| Funktsiooniala | Uued või värskendatud artiklid |
|---|---|
| Koondplaneerimine, CTP | [Müügitellimuse tarnekuupäevade arvutamine CTP-d kasutades](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) |
| Koondplaneerimine, DDMRP | [Nõudlusepõhiste materjalinõuete planeerimise ülevaade](../master-planning/planning-optimization/ddmrp-overview.md)<br>[Lülitage süsteemi jaoks sisse DDMRP-funktsioon](../master-planning/planning-optimization/ddmrp-enable.md)<br>[Varude paigutamine](../master-planning/planning-optimization/ddmrp-inventory-positioning.md)<br>[Puhvri profiil ja tasemed](../master-planning/planning-optimization/ddmrp-buffer-profile-and-levels.md)<br>[Nõudlusepõhine planeerimine](../master-planning/planning-optimization/ddmrp-planning.md)<br>[Visuaalne ja koostööd võimaldav täitmine](../master-planning/planning-optimization/ddmrp-visual-and-collaborative-execution.md) |
| Laohaldus | [Saadetise konteinerite pakkimine](../warehousing/packing-containers.md)<br>[Väljaminevate konteinerite pakkimise ja saadetiste töötlemise pakkimistöö](../warehousing/packing-work.md) |

## <a name="feature-state-changes-in-this-release"></a>Funktsiooni oleku muudatused selles väljalaskes

Järgmises tabelis loetletakse funktsioonid, mis muutsid kohustuslikuks või mis muutsid seda vaikimisi versioonis 10.0.29. Kõik need funktsioonid lülitatakse teie süsteemi jaoks automaatselt sisse kohe, kui te uuendate versiooniks 10.0.29. Kohustuslikke funktsioone ei saa välja lülitada, kuid vaikimisi sisse lülitatud funktsioone saab funktsioonihalduse abil endiselt [välja lülitada](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tabelis loetletakse ka funktsioonid, mis olid eelnevalt avalikus eelvaates, kuid on muutunud kättesaadavaks versioonis 10.0.29. See muudatus näitab, et funktsioonid on nüüd tootmiskeskkondades kasutamiseks soovitatavad. Need funktsioonid lülitatakse vaikimisi välja, kui pole märgitud teisiti. Seetõttu peate nende kasutamiseks [funktsioonihaldust](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kasutama.

| Moodul | Funktsiooni nimi | Uue funktsiooni olek |
| --- | --- | --- |
| Varahaldus | [Tootmisosakonna täideviimisliidese varahoolduse funktsioon](../production-control/production-floor-execution-configure.md) | Kohustuslik |
| Kuluhaldus | [Sulgemise ja storneerimise korrigeerimise tühistamise sildi muutmine](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/change-terminology-inventory-closing-cancellation-inventory-closing-reverse) | Kohustuslik |
| Kuluhaldus | Koosluse kalkulatsiooni üksikasjade ristkuluversioonide puhastamine | Kohustuslik |
| Kuluhaldus | [Kaubahindade ladustamise võrdlemine](../cost-management/compare-item-price.md) | Kohustuslik |
| Kuluhaldus | [Kuluarvutuse tase](../cost-management/cost-calculation-level.md) | Vaikimisi sees |
| Kuluhaldus | Luba kasutaja määratletud partiinumbri seadistamine varude sulgemise tühistamise jaoks | Vaikimisi sees |
| Kuluhaldus | [Varude sulgemise edenemise üksikasjad](whats-new-scm-10-0-21.md) | Vaikimisi sees |
| Kuluhaldus | [Laoväärtuse aruannete talletamine](../cost-management/inventory-value-report-storage.md) | Kohustuslik |
| Kuluhaldus | Laoväärtuse aruande andmete puhastamine | Kohustuslik |
| Kuluhaldus | Liikuva keskmise varukulu järjestus | Kohustuslik |
| Kuluhaldus | Kuva varude sulgemislogi ruudustikuna | Kohustuslik |
| Kuluhaldus | Mitte täielikult tasakaalustatud kannetega üksuste kokkuvõttevormis kuvamine | Kohustuslik |
| Varude ja laohaldus | Luba tühjade partii atribuutide väärtused | Kohustuslik |
| Varude ja laohaldus | Suurenda automaatselt lao üleviimistellimuse ridade numbreid | Kohustuslik |
| Varude ja laohaldus | Loo müügirealt üleviimistellimus | Kohustuslik |
| Varude ja laohaldus | Keela varude töölehe rea väli töövoos | Kohustuslik |
| Varude ja laohaldus | Luba varude kvaliteedihalduse parameetrite hoiatuse funktsioon | Kohustuslik |
| Varude ja laohaldus | (Hiina) Jäta välja kuu keskmise kulu füüsiline kviitung ja väljaminevad kulud | Vaikimisi sees |
| Varude ja laohaldus | [Varude töölehe kinnitamise töövoog](../inventory/inventory-journal-workflow.md) | Kohustuslik |
| Varude ja laohaldus | [Vaba kaubavaru aruande talletamine](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/inventory-on-hand-report-storage) | Kohustuslik |
| Varude ja laohaldus | [Laohalduse salvestatud vaated](saved-views-scm.md) | Kohustuslik |
| Varude ja laohaldus | Üleviimistellimuse tühistamine | Kohustuslik |
| Varude ja laohaldus | Mõõtühiku ja ühikukoguse kasutamine laotöölehtedel | Kohustuslik |
| Varude ja laohaldus | Laotöölehe vabastamine | Kohustuslik |
| Tootmine | [Laos lubatud materjalide automaatne valimine automaatselt sisestatud komplekteerimislehtede jaoks](whats-new-scm-10-0-23.md) | Üldiselt saadaval |
| Tootmine | Varude dimensioonide kuvamise lubamine tootmisprotsessi toimingute materjalide loendis | Kohustuslik |
| Tootmine | [Võimaldab sisestada partii- ja seerianumbreid, kui need märgitakse töökaardi vahendil lõpetatuks](../production-control/report-finished-job-device.md) | Vaikimisi sees |
| Tootmine | Tegeliku kaalu koguse komplekteerimise paranenud tootlikkus | Vaikimisi sees |
| Tootmine | [Tootmisosakonna täideviimisliidese töö otsing](../production-control/production-floor-execution-configure.md) | Kohustuslik |
| Tootmine | [Tootmise käivitussüsteemi integreerimine](../production-control/mes-integration.md) | Vaikimisi sees |
| Tootmine | [Tootmisosakonna täideviimisliidese vaade Minu päev](../production-control/production-floor-execution-configure.md) | Vaikimisi sees |
| Tootmine | [Tootmistellimuste vajaduse korral materjali saadavuse kontroll](whats-new-scm-10-0-24.md) | Vaikimisi sees |
| Tootmine | [Vaikimisi tootmisbroneeringu alistamine](../production-control/override-default-reservation-principle.md) | Kohustuslik |
| Tootmine | [Materjali tarbimise registreerimine tootmisosakonna täideviimisliideses (mitte-WMS)](../production-control/production-floor-execution-configure.md) | Üldiselt saadaval |
| Tootmine | [Aruanne tegeliku kaalu üksuste kohta tootmisosakonna täideviimisliidesest](../production-control/production-floor-execution-configure.md) | Üldiselt saadaval |
| Tootmine | [Tootmisosakonna täideviimisliidese kaas- ja kõrvalsaaduste aruanne](../production-control/production-floor-execution-configure.md) | Vaikimisi sees |
| Tootmine | [Plaanimisüksuste aruanne tootmisosakonna täideviimisliideses](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | Vaikimisi sees |
| Tootmine | [Tootmise juhtimise salvestatud vaated](saved-views-scm.md) | Kohustuslik |
| Tootmine | [Kuva tootmisosakonna täideviimisliidese täielikud seeria-, partii- ja numbrimärginumbrid](../production-control/production-floor-execution-configure.md) | Kohustuslik |
| Tootmine | [Kinnitage tooraine aegumiskuupäev kavandatud tarbimiskuupäeva suhtes](whats-new-scm-10-0-23.md) | Vaikimisi sees |
| Koondplaneerimine | [Automaatkinnitamine planeerimise optimeerimiseks](../master-planning/planning-optimization/planned-order-firming.md) | Kohustuslik |
| Koondplaneerimine | [Plaanitud hulgi- ja partiina tellimuste partiideks jaotatud kinnitamine ja konsolideerimine](whats-new-scm-10-0-20.md) | Vaikimisi sees |
| Koondplaneerimine | [Laoseisuga kaupade kaasamine, kui eeltöötlusfiltrid on lubatud](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/master-planning-include-items-on-hand-when-pre-processing-filters-are-enabled) | Vaikimisi sees |
| Koondplaneerimine | [Planeerimise optimeerimise lõpmatu võimsuse ajastamine](../master-planning/planning-optimization/infinite-capacity-planning.md) | Vaikimisi sees |
| Koondplaneerimine | [Planeerimise optimeerimise marginaalid](../master-planning/planning-optimization/safety-margins.md) | Kohustuslik |
| Koondplaneerimine | [Planeerimise optimeerimise negatiivsed päevad](../master-planning/planning-optimization/delay-tolerance.md) | Kohustuslik |
| Koondplaneerimine | [Korrigeeritud nõudluse prognoosi paralleelne lubamine](whats-new-scm-10-0-20.md) | Kohustuslik |
| Koondplaneerimine | [Filtreerimisega plaanitud tellimuse kinnitamine](../master-planning/planning-optimization/planned-order-firming.md) | Kohustuslik |
| Koondplaneerimine | [Plaanitud tootmistellimused planeerimise optimeerimiseks](../master-planning/planning-optimization/production-planning.md) | Kohustuslik |
| Koondplaneerimine | [Ostu kaubanduslepped planeerimise optimeerimiseks](../master-planning/planning-optimization/purchase-trade-agreement.md) | Kohustuslik |
| Koondplaneerimine | [Plaanitud tellimuste salvestatud vaated](saved-views-scm.md) | Kohustuslik |
| Hanked | Ostutellimuste alates ja kuni summad | Kohustuslik |
| Hanked | Keela ostutaotluse jaotuse lähtestamise nupp | Vaikimisi sees |
| Hanked | [Luba hankega seotud töövoogude lähtestamine](whats-new-scm-10-0-20.md) | Vaikimisi sees |
| Hanked | [Ostutellimuse ridade arvu piiramine partiiülesande kohta](whats-new-scm-10-0-27.md) | Vaikimisi sees |
| Hanked | [Hankija finantsdimensioonide ühendamine ostutellimuse aktiivse dimensioonilingi finantsdimensiooniga](whats-new-scm-10-0-25.md) | Kohustuslik |
| Hanked | [Laos olevate toodete registreeritud koguste ja laos olevate toodete jääkide sisestamine kviitungite ja hankija arvete jaoks](whats-new-scm-10-0-26.md) | Üldiselt saadaval |
| Hanked | [Vältige eelarvereservi ületarbimist, kui töövoos on mitu ostutaotlust](whats-new-scm-10-0-21.md) | Vaikimisi sees |
| Hanked | [Ostulepingu vastutav isik](../procurement/purchase-agreements.md) | Kohustuslik |
| Hanked | [Ostutellimuste salvestatud vaated](saved-views-scm.md) | Kohustuslik |
| Tooteteabe haldus | Koosluse aruande eeltöötlus aegumise vältimiseks | Kohustuslik |
| Tooteteabe haldus | Jaota finantsdimensioonid kaubamalle kasutades vaikimisi eraldi | Kohustuslik |
| Tooteteabe haldus | Luba kaubamallide jaoks tootedimensioonigrupid | Kohustuslik |
| Tooteteabe haldus | Kauba ja vöötkoodi üksuse täiustused | Kohustuslik |
| Tooteteabe haldus | Loo tootevariantide nimed nomenklatuuri alusel uuesti | Kohustuslik |
| Tooteteabe haldus | [Väljastatud toodete salvestatud vaated](saved-views-scm.md) | Kohustuslik |
| Tooteteabe haldus | [Variandi soovituste lehe täiustused](../pim/tasks/create-predefined-product-variants.md) | Kohustuslik |
| Müük ja turundus | [Tasude eraldamine müügitellimusel](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/miscellaneous-charges-enhancements) | Kohustuslik |
| Müük ja turundus | Müügitellimuse värskendamise ajaloo puhastamine | Kohustuslik |
| Müük ja turundus | [Müügi värskendamise ajaloo puhastamine vanuse põhjal](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) | Kohustuslik |
| Müük ja turundus | [Kontaktisiku andmeüksuse ekspordi optimeerimine](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | Kohustuslik |
| Müük ja turundus | Kopeeri müügi kreeditarve lõppallahindluse grupp | Kohustuslik |
| Müük ja turundus | [Lubage müügipakkumise dokumendi sissejuhatuse ja dokumendi järelduste väljade otsing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | Kohustuslik |
| Müük ja turundus | [Parandage klientide aruande „100 esimest” jõudlust](whats-new-scm-10-0-23.md) | Kohustuslik |
| Müük ja turundus | Ootekirjete lisamine ajaloo puhastamise ülesannetesse | Kohustuslik |
| Müük ja turundus | Müügitellimuse ridade arvu piiramine partiiülesande kohta | Vaikimisi sees |
| Müük ja turundus | [Postitamiseks valitavate müügitellimuste arvu piiramine](whats-new-scm-10-0-21.md) | Kohustuslik |
| Müük ja turundus | Prognoositava kliendisaldo ümberarvutamine | Kohustuslik |
| Müük ja turundus | [Müügi tagastustellimuse rea registreerimine kümnendkoha täpsusega koos tegeliku kaaluga ja ilma selleta](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | Kohustuslik |
| Müük ja turundus | [Müügi ja turunduse salvestatud vaated](saved-views-scm.md) | Kohustuslik |
| Müük ja turundus | [Ühe klõpsuga müügitellimuse kinnitus](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/single-click-sales-order-confirmation) | Kohustuslik |
| Transpordihaldus | Veoarve ridadest veoarvete eraldamise lubamine ilma hankija arve töölehe lisamiseta | Vaikimisi sees |
| Transpordihaldus | [Luba hankija arve töölehe loomine veose arve tühistamisel](whats-new-scm-10-0-20.md) | Vaikimisi sees |
| Transpordihaldus | [Väikepaki saatmine](../warehousing/small-parcel-shipping.md) | Kohustuslik |
| Transpordihaldus | [USMCA päritolutunnistuse dokument](../transportation/usmca-certification-of-origin.md) | Vaikimisi sees |
| Laohaldus | [Täiendav asukohatsoon](../warehousing/additional-location-zones.md) | Kohustuslik |
| Laohaldus | [Tühista töö](../warehousing/cancel-warehouse-work.md) | Kohustuslik |
| Laohaldus | [Saadetise konsolideerimine](../warehousing/configure-shipment-consolidation-policies.md) | Kohustuslik |
| Laohaldus | [Laorakenduses ülekandetellimuste loomine ja töötlemine](../warehousing/create-transfer-order-from-warehouse-app.md) | Kohustuslik |
| Laohaldus | Asukohadirektiividega ristiliaadimismallid | Vaikimisi sees |
| Laohaldus | [ASN-idest kõrvalepaneku töö eradamine](whats-new-scm-10-0-21.md) | Kohustuslik |
| Laohaldus | [Edasilükatud asetamistoimingud](../warehousing/deferred-processing-manual-inventory-movement.md) | Kohustuslik |
| Laohaldus | Edasilükatud – konteiner | Vaikimisi sees |
| Laohaldus | Edasilükatud asetamise töötlemine – lubage auditimalli funktsioon, kui käivitaja sündmus on seatud väärtusele Eelmine | Kohustuslik |
| Laohaldus | [Keelake oodatud kviitungid kvaliteettellimustest, mille valim on blokeeritud varudes](../inventory/inventory-blocking.md) | Vaikimisi sees |
| Laohaldus | Luba lao mobiilsete seadmete jaoks kiire kinnitamine | Kohustuslik |
| Laohaldus | [Täiustatud parser GS1 vöötkoodide jaoks](../warehousing/gs1-barcodes.md) | Üldiselt saadaval |
| Laohaldus | [Paindlik tellimusele kinnitatud litsentsiplaadi reserveering](../warehousing/flexible-warehouse-level-dimension-reservation.md) | Kohustuslik |
| Laohaldus | [Paindlik laotaseme dimensiooni reserveerimine](../warehousing/flexible-warehouse-level-dimension-reservation.md) | Kohustuslik |
| Laohaldus | [Kauba konsolideerimise asukoha kasutamine](../warehousing/item-consolidation-location-utilization.md) | Vaikimisi sees |
| Laohaldus | Litsentsiplaadi vastuvõtu ajalugu | Vaikimisi sees |
| Laohaldus | [Saadetise käsitsi konsolideerimine](../warehousing/consolidate-shipments-manual-workbench.md) | Vaikimisi sees |
| Laohaldus | [Käsitsi ülekanderea komplekteerimise teenus administraatorile või sarnastele usaldusväärsetele kasutajatele](whats-new-scm-10-0-28.md) | Üldiselt saadaval |
| Laohaldus | [Materjali käsitlemise seadmete liides](../warehousing/mhax.md) | Kohustuslik |
| Laohaldus | [Uued koorma planeerimise töölaua leheküljed](whats-new-scm-10-0-24.md) | Üldiselt saadaval |
| Laohaldus | [Väljamineva töökoormuse visualiseerimine](../warehousing/outbound-workload-visualization.md) | Kohustuslik |
| Laohaldus | [Plaanitud ristlaadimine](../warehousing/planned-cross-docking.md) | Kohustuslik |
| Laohaldus | [Laorakenduse sündmuste töötlemine](../warehousing/warehouse-app-events.md) | Kohustuslik |
| Laohaldus | Kaastoote ja kõrvalsaaduse ladustamise töömalli päringu täiustamine | Kohustuslik |
| Laohaldus | [Ümmarda kogused lattu väljastamiseks lähima müügiüksuseni](whats-new-scm-10-0-19.md) | Kohustuslik |
| Laohaldus | [Koorma planeerimise töölaua salvestatud vaade](saved-views-scm.md) | Kohustuslik |
| Laohaldus | [Töö üksikasjade lehe salvestatud vaade](saved-views-scm.md) | Kohustuslik |
| Laohaldus | [Voo töötlemise salvestatud vaade](saved-views-scm.md) | Kohustuslik |
| Laohaldus | [Koormuse töötlemise salvestatud vaated](saved-views-scm.md) | Kohustuslik |
| Laohaldus | [Saadetise töötlemise salvestatud vaated](saved-views-scm.md) | Kohustuslik |
| Laohaldus | [GS1 vöötkoodide skannimine](../warehousing/gs1-barcodes.md) | Üldiselt saadaval |
| Laohaldus | Saadetise voo sildi üksikasjad | Kohustuslik |
| Laohaldus | [Pesa segaühikud](whats-new-scm-10-0-21.md) | Kohustuslik |
| Laohaldus | [Kasutage pakkimisjaamas konteinerite sulgemiseks / uuesti avamiseks kiiremat API-d](whats-new-scm-10-0-21.md) | Vaikimisi sees |
| Laohaldus | [Kinnitage täiendamise tööde jaoks valitud mallid](whats-new-scm-10-0-20.md) | Vaikimisi sees |
| Laohaldus | [Laorakenduse ülendatud väljad](../warehousing/warehouse-app-promoted-fields.md) | Kohustuslik |
| Laohaldus | [Laorakenduse etapi juhised](../warehousing/mobile-app-titles-instructions.md) | Kohustuslik |
| Laohaldus | [Laoasukoha olek](../warehousing/warehouse-location-status.md) | Kohustuslik |
| Laohaldus | [Warehouse management appi kõrvalepõiked](../warehousing/warehouse-app-detours.md) | Vaikimisi sees |
| Laohaldus | [Voo pakett-töö üksikasjad](../warehousing/wave-processing.md) | Kohustuslik |
| Laohaldus | [Voo täitmise teatised](../warehousing/wave-execution-notifications.md) | Kohustuslik |

## <a name="additional-resources"></a>Lisaressursid

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finantside ja toimingute rakenduste platvormi värskendused

Microsoft Dynamics 365 Supply Chain Management 10.0.29 sisaldab platvormivärskendusi. Lisateavet vt Platvormi värskendustest [versioonile 10.0.29 Finance and Operations rakendustest (oktoober 2022).](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md)

### <a name="bug-fixes"></a>Veaparandused

Teavet versiooni 10.0.29 igas versiooniga 10.0.29 lisatud uuenduses sisaldub vigaparanduste kohta, logige sisse elutsükli teenustesse (LCS) [ja vaadake KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 ja majandusharu pilved: 2022 väljalaskevoo 1 plaan

Kas teile pakuvad huvi meie ärirakenduste või platvormi uued ja hiljuti väljaantud võimalused?

Vaadake [Dynamics 365 ja majandusharu pilved: 2022 väljalaskevoo 2 plaan](/dynamics365-release-plan/2022wave2/). Käsitleme ühes dokumendis kõiki üksikasju otsast lõpuni ja ülevalt alla, millest võite plaanide tegemisel lähtuda.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Eemaldatud ja aegunud Supply Chain Managementi funktsioonid

Artikli [eemaldatud või taunitud Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) funktsioonid kirjeldavad funktsioone, mis on tarneahela halduses eemaldatud või plaaniliselt eemaldatud või taunitud.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

Enne mis tahes funktsiooni eemaldamist tootest teatatakse amortiseerumisest [Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) artikli 12 kuu jooksul enne eemaldamist eemaldatud või taunitud funktsioonides.

Murranguliste muudatuste puhul, mis mõjutavad ainult kompileerimise aega, kuid on binaarselt ühilduvad liivakasti- ja tootmiskeskkondadega, on aegumise aeg vähem kui 12 kuud. Need on tavaliselt funktsionaalsed uuendused, mida tuleb teha kompilaatori jaoks.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
