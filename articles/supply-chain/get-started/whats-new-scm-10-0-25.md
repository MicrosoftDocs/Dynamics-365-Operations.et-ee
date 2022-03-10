---
title: Dynamics 365 Supply Chain Management 10.0.25 (aprill 2022) eelversioon
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Supply Chain Management 10.0.25 uusi või muutunud funktsioone.
author: kamaybac
ms.date: 02/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 068e65d0bd76d7a9af36c6c3539d0c813efd528a
ms.sourcegitcommit: 2e554371f5005ef26f8131ac27eb171f0bb57b4e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/04/2022
ms.locfileid: "8384534"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10025-april-2022"></a>Dynamics 365 Supply Chain Management 10.0.25 (aprill 2022) eelversioon

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Selles teemas loetletakse rakenduse Microsoft Dynamics 365 Supply Chain Management eelversiooni 10.0.25 uued või muutunud funktsioonid. Selle versiooni number on 10.0.1149 ja see on saadaval järgmiselt:

- **Väljaande eelversioon:** veebruar 2022
- **Väljalaske üldine kättesaadavus (iseseisev värskendamine):** märts 2022
- **Väljalaske üldine kättesaadavus (automaatne värskendamine):** aprill 2022

## <a name="features-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selles versioonis sisalduvad funktsioonid. Võime värskendada seda teemat, et lisada sellesse funktsioone, mis on loodud pärast selle esialgset avaldamist tehtud veaparandusi.

| Funktsiooniala | Funktsioon | Lisateave | Lubaja:   |
|---|---|---|---|
| Varud&nbsp;ja&nbsp;logistika | [Ohtlike materjalide täiustused](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/hazardous-materials-enhancements) | Peagi tulekul | Funktsioonihaldus:<br>*Ohtlike materjalide täiustused* |
| Varud&nbsp;ja&nbsp;logistika | [Pakkimistöö pakkimisjaamade jaoks](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/packing-work-packing-stations) | Peagi tulekul | Funktsioonihaldus:<br>*Pakkimistöö pakkimisjaamade jaoks* |
| Varud&nbsp;ja&nbsp;logistika | [Skannige vöötkoode laos, kasutades GS1-vormingu standardeid](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | [GS1 vöötkoodid ja QR-koodid](../warehousing/gs1-barcodes.md) | Funktsioonihaldus:<br>*GS1 vöötkoodide skannimine* |
| Tootmine | [Materjali tarbimine ja reserveerimised tootmispinna käivitamise liideses](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/material-consumption-reservations-production-floor-execution-interface) | [Kuidas töötajad kasutavad tootmisosakonna käivitusliidest](../production-control/production-floor-execution-use.md) | Funktsioonihaldus:<br>*(Eelversioon) Materjali tarbimise registreerimine tootmisosakonna täideviimisliideses (mitte-WMS)*<br><br>Ja/või:<br><br>Funktsioonihaldus:<br>*(Eelvaade) Materjalikulu registreerimine tootmisosakonna käivitusliideses (WMS-loaga)* |
| Tootmine | [Registreeri materjali tarbimine kaaluühikutes](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/register-material-consumption-scale-units) | [Tootmise täideviimise töökoormused pilv- ja perimeeterskaalaüksuste jaoks](../cloud-edge/cloud-edge-workload-manufacturing.md) | Funktsioonihaldus:<br>*Materjalikulu registreerimine mobiilirakenduse skaalaüksuses* |
| Planeerimine | [Optimeerimise soovituste plaanimine olemasoleva tarne optimeerimiseks](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-suggestions-optimize-existing-supply) | [Tegevusteated](../master-planning/action-messages.md) | Vaikimisi lubatud |
| Planeerimine | Plaanitud tellimuste lihtsustamine | [Plaanitud tellimuste lihtsustamine](../master-planning/planning-optimization/planned-orders-simplified.md ) | Funktsioonihaldus:<br>*Plaanitud tellimuste lihtsustamine* |

## <a name="feature-enhancements-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selle väljalaske funktsioonide täiustused. Kõik need täiustused parandavad olemasolevat funktsiooni järk-järgult. Kuna need on ainult täiustused, siis neid ei loetleta [väljalaskeplaanis](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Kindlustamaks, et need täiustused ei satu vastuollu olemasolevate kohanduste või eelistustega, lülitatakse iga neist vaikimisi välja (kui pole märgitud teisiti).

Kui soovite mõne neist funktsioonidest sisse ja välja lülitada, peate seda funktsioonihalduses [tegema](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Moodul | Funktsiooni nimi funktsioonihalduses | Lisateave |
|---|---|---|
| Varude ja laohaldus | (Poola) Võimaldab siduda mitu SAD-arvet ühe ostutellimuse reaga ühes SAD-is | See funktsioon võimaldab teil ostutellimuse read tükeldada ja linkida need ühe haldusdokumendiga (SAD), kui need ostutellimuse read sisestati mitmele erinevale arvele (nt erinevatele saadetistele). |
| Hanked | Mitme ostutaotluse konsolideerimine üheks ostutellimuseks aruandluskuupäeva järgi | See funktsioon võimaldab mitme ostutaotluse konsolideerimist ühele ostutellimusele, kui erinevatel ostutaotlustel on erinevad raamatupidamiskuupäevad. Ostutellimuse loomise ja nõudluse konsolideerimise ostupoliitika reeglid saab seadistada nii, et see automatiseeriks otsuse taotluse ridade grupeerimiseks raamatupidamiskuupäeva järgi ostutellimuse tasemel. Ostutellimuse konsolideerimist raamatupidamiskuupäeva järgi ei toetata, kui eelarve juhtimine on lubatud, kuna raamatupidamise kuupäeva kasutatakse eelarvereserveeringute ja pandiõiguse jaoks. Seetõttu tuleb see säilitada üleminekul ostutaotluselt ostutellimusele. |
| Hanked | Kuva pärandi vaikimisi pakkumiskutse vastuse välja sätted | See funktsioon ennistada pärandi pakkumiskutse vastusevälja sätted, mis eemaldati eelnevalt kasutajaliidesest. Need sätted ei paku boksist funktsionaalsust, kuid neid saab vajaduse järgi kohandada. Lubage see funktsioon, kui teie organisatsioon on juba lisanud funktsioonid pakkumiskutse vastusevälja vaikesätetele või kui plaanite seda teha. Kui see funktsioon on lubatud, pääsete sätete juurde, **avades** hankeparameetrite lehe, **·** **avades vahekaardi Pakkumiskutse ja valides vaikimisi pakkumiskutse vastuseväljad**. |
| Hanked | Hankija finantsdimensioonide ühendamine ostutellimuse aktiivse dimensioonilingi finantsdimensiooniga | See funktsioon võimaldab teil ühendada aktiivse dimensiooni lingiga finantsdimensioonide hankijad pärast ostutaotluse kinnitust, kui seadistate lingi rahalise dimensiooni ja saidi varude dimensiooni vahel. Ostutellimuse loomise ja nõudluse konsolideerimise ostupoliitika reegleid saab seadistada, et juhtida otsuse rahalisi dimensioone ühendama aktiivse dimensioonilingi finantsdimensiooniga hankijate ostutellimuse päise tasemel. |
| Tootmise juhtimine | (Venemaa) Luba tootmise valemi/koosluse jaoks asukoha vaikeseadistus ja automaatne GTD reserveerimine/tarbimine tootmises | See funktsioon võimaldab lisavalikuid tootmisele imporditud toormaterjalidest (ainult Venemaa lokaliseerimine):<ul><li>Tootmisvalemite ja koosluste automaatse vaikeasukoha seadistamine nii ressursigruppides kui ka ladudes.</li><li>Toormaterjalide automaatne reserveerimine *GTD-numbridimensiooni järgi* WMS-aktiveeritud ladudes vastavalt mitte-WMS-i reserveerimisalgoritmile. See kehtib juhul, *·* **·** *kui* toormaterjali komplekteerimise tööpoliitika eksisteerib siis, kui töö loomise meetodiks on määratud Mitte kunagi ning ladu, asukoha ja kaubakoodi häälestus vastab tootmistellimuste (partii) laokannetele.</li><li>Toormaterjalide automaatne tarbimine *GTD-numbri* dimensiooni järgi komplekteerimislehe sisestamisel vastavalt eelnevalt kirjeldatud soetatud reserveeringule.</li></ul> |
| Laohaldus | (Eelvaade) Skaalaüksuse tugi sissetulevate ja väljaminevate laotellimuste jaoks | Selle funktsiooniga loob süsteem väljaminevad laotellimused lattu vabastamise protsessi ajal ja loob sissetulevad laotellimused, kui üleviimistellimused sisestatakse lähetatuna. Süsteem sünkroonib seejärel iga sissetuleva või väljamineva lao tellimuse tellimuse saatmise või vastuvõtmise eest vastutava kaaluüksusega. Pange tähele, et pärast selle funktsiooni lubamist tuleb lao käivitamise töökoormused täiendada. Lisateavet vt [Laohalduse töökoormused pilv- ja perimeeterskaalaüksuste jaoks](../cloud-edge/cloud-edge-workload-warehousing.md).<br><br>See funktsioon nõuab *dekodeerimistööd ASN-funktsioonist* ja võimaldab üleviimistellimuste vastuvõtmise võimalust, kasutades litsentsiplaadi vastuvõtuprotsessi laohalduse mobiilirakenduses. |

## <a name="feature-state-changes-in-this-release"></a>Funktsiooni oleku muudatused selles väljalaskes

Järgmises tabelis loetletakse funktsioonid, mis muutusid kohustuslikuks või mis algavad vaikimisi kell 10.0.25. Kõik need funktsioonid lülitatakse teie süsteemi jaoks automaatselt sisse kohe, kui uuendate 10.0.25. Kohustuslikke funktsioone ei saa välja lülitada, kuid vaikimisi sisse lülitatud funktsioone saab funktsioonihalduse abil endiselt [välja lülitada](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Tabelis loetletakse ka funktsioonid, mis olid eelnevalt avalikus eelvaates, kuid on muutunud üldiselt kättesaadavaks 10.0.25, mis tähendab, et neid on nüüd soovitatav kasutada tootmiskeskkondades. Need funktsioonid lülitatakse vaikimisi välja, kui pole märgitud teisiti, seega [peate](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) nende lubamiseks kasutama Funktsioonihaldust, kui soovite neid kasutada.

| Moodul | Funktsiooni nimi | Funktsiooni olek |
| --- | --- | --- |
| Varahaldus | [Töökäskude rühmitamise reeglite rakendamine hooldusplaani käitades](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md) | Üldiselt saadaval |
| Varahaldus | [Loenduripõhised hoolduse täiustused](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md) | Üldiselt saadaval |
| Kuluhaldus | [Kuluarvutuse tase](../cost-management/cost-calculation-level.md) | Üldiselt saadaval |
| Kuluhaldus | Luba kasutaja määratletud partiinumbri seadistamine varude sulgemise tühistamise jaoks | Üldiselt saadaval |
| Kuluhaldus | [Varude sulgemise edenemise üksikasjad](whats-new-scm-10-0-21.md) | Üldiselt saadaval |
| Kuluhaldus | [Varude standardomahinna ümberhindamise finantsdimensioonide vaikimisi valikud](../cost-management/manage-standard-cost-updates.md) | Üldiselt saadaval |
| Kuluhaldus | Laoväärtuse aruande andmete puhastamine | Vaikimisi sees |
| Kuluhaldus | [Laoväärtuse aruannete talletamine](../cost-management/inventory-value-report-storage.md) | Vaikimisi sees |
| Kuluhaldus | Kuva varude sulgemislogi ruudustikuna | Vaikimisi sees |
| Tehnilise muudatuse haldamine | [Luba olemasolevate toodete muudatuste haldamine](../engineering-change-management/change-management-existing-products.md) | Vaikimisi sees |
| Tehnilise muudatuse haldamine | [Tehnika muutmise haldus](../engineering-change-management/product-engineering-overview.md) | Vaikimisi sees |
| Tehnilise muudatuse haldamine | [Tootmise tehnilised teatised](../engineering-change-management/engineering-change-management.md) | Vaikimisi sees |
| Tehnilise muudatuse haldamine | [Paranenud tehnilise muudatuse halduse atribuudi pärimine](../engineering-change-management/engineering-attributes-and-search.md) | Vaikimisi sees |
| Tehnilise muudatuse haldamine | [Valemite ja nende koostisosade muudatuste haldamine](../engineering-change-management/manage-formula-changes.md) | Vaikimisi sees |
| Tehnilise muudatuse haldamine | [Toote valmisoleku kontrollid](../engineering-change-management/product-readiness.md) | Vaikimisi sees |
| Tehnilise muudatuse haldamine | [Tehnikatoodetele variantide loomine](../engineering-change-management/engineering-variants.md) | Vaikimisi sees |
| Varude ja laohaldus | Koosluseversioonile navigeerimine koosluseridadelt | Kohustuslik |
| Koondplaneerimine | [Plaanitud hulgi- ja partiina tellimuste partiideks jaotatud kinnitamine ja konsolideerimine](whats-new-scm-10-0-20.md) | Üldiselt saadaval |
| Koondplaneerimine | Ressursside koos hooldusega plaanimine | Üldiselt saadaval |
| Koondplaneerimine | Koondplaani häälestusviisardi funktsioonide lubamine | Kohustuslik |
| Koondplaneerimine | [Prognoosimudeli valimine nõudluse prognoosi üksikasjades](../master-planning/manual-adjustments-baseline-forecast.md) | Kohustuslik |
| Koondplaneerimine | [Koondplaneerimise edenemise visualiseerimine](../master-planning/tasks/monitor-master-planning-run.md) | Kohustuslik |
| Koondplaneerimine | [Plaanitud tellimuste paralleelne kinnitamine](../master-planning/planning-optimization/planned-order-firming.md) | Kohustuslik |
| Koondplaneerimine | [Filtreerimisega plaanitud tellimuse kinnitamine](../master-planning/planning-optimization/planned-order-firming.md) | Vaikimisi sees |
| Koondplaneerimine | [Plaanitud tellimuste salvestatud vaated](saved-views-scm.md) | Vaikimisi sees |
| Hanked | Keela ostutaotluse jaotamise lähtestamise nupp | Üldiselt saadaval |
| Hanked | [Luba hankega seotud töövoogude lähtestamine](whats-new-scm-10-0-20.md) | Üldiselt saadaval |
| Hanked | Võimalus kinnitada hankijakoostööst aktsepteeritud ostutellimused partiina | Kohustuslik |
| Hanked | Ostulepingu suletud olek | Kohustuslik |
| Hanked | Ridade lisamine ostulepinguga seotud ostutellimuse arvetele | Vaikimisi sees |
| Hanked | Lisa väli „Tellitud kogus” lehele „Toote sissetuleku sisestamine” | Vaikimisi sees |
| Hanked | [Lubage hankijatel taotleda hankekategooriaid hankijate koostöö kaudu](../procurement/category-requests-from-vendors.md) | Vaikimisi sees |
| Hanked | Ostutellimuste alates ja kuni summade tasud | Vaikimisi sees |
| Hanked | Tasude seadistamine saidi ja laoga | Vaikimisi sees |
| Hanked | Luba ostulõivu arvutamine aastatariifi alusel | Vaikimisi sees |
| Hanked | [Ostulepingu vastutav isik](../procurement/purchase-agreements.md) | Vaikimisi sees |
| Hanked | [Ostutellimuste salvestatud vaated](saved-views-scm.md) | Vaikimisi sees |
| Tooteteabe haldus | [Vaiketellimuse koguste range kinnitamine](../production-control/default-order-settings.md) | Kohustuslik |
| Tooteteabe haldus | Koosluse aruande eeltöötlus aegumise vältimiseks | Vaikimisi sees |
| Tooteteabe haldus | Jaota finantsdimensioonid kaubamalle kasutades vaikimisi eraldi | Vaikimisi sees |
| Tooteteabe haldus | Luba kaubamallide jaoks tootedimensioonigrupid | Vaikimisi sees |
| Tooteteabe haldus | Loo tootevariantide nimed nomenklatuuri alusel uuesti | Vaikimisi sees |
| Tooteteabe haldus | [Variandi soovituste lehe täiustused](../pim/tasks/create-predefined-product-variants.md) | Vaikimisi sees |
| Tootmise juhtimine | Tegeliku kaalu koguse komplekteerimise paranenud tootlikkus | Üldiselt saadaval |
| Tootmise juhtimine | Töökaardi terminali lehele on lisatud uus nupp Pausi peatamiseks | Kohustuslik |
| Tootmise juhtimine | [Identifitseerimisnumbri automaatse genereerimise lubamine lõpetamisest teatamisel töökaardi vahendis](../production-control/production-floor-execution-configure.md) | Kohustuslik |
| Tootmise juhtimine | Luba alltöövõtu kaupade osaline sissetulek ja parandage probleem hankija tüüpi koosluseridade praagi arvutamisega | Kohustuslik |
| Tootmise juhtimine | [Funktsioon töökaardi seadme ja töökaardi terminali lukustamiseks, et neid saaks puhastada](../production-control/production-floor-execution-configure.md) | Kohustuslik |
| Tootmise juhtimine | Täiustused dialoogides Kinnita ja Ülekandmistööd | Kohustuslik |
| Tootmise juhtimine | [Töökaardi vahendile on lisatud lõpetatuks märkimise litsentsiplaat](../production-control/production-floor-execution-configure.md) | Kohustuslik |
| Tootmise juhtimine | [Sildi printimine töökaardi vahendilt](../production-control/production-floor-execution-configure.md) | Kohustuslik |
| Tootmise juhtimine | [Tootmisosakonna täideviimine](../production-control/production-floor-execution-configure.md) | Kohustuslik |
| Tootmise juhtimine | [Tootmisosakonna täideviimisliidese varahoolduse funktsioon](../production-control/production-floor-execution-configure.md) | Vaikimisi sees |
| Tootmise juhtimine | [Tootmisosakonna täideviimisliidese töö otsing](../production-control/production-floor-execution-configure.md) | Vaikimisi sees |
| Tootmise juhtimine | [Vaikimisi tootmisbroneeringu alistamine](../production-control/override-default-reservation-principle.md) | Vaikimisi sees |
| Tootmise juhtimine | [Kuva tootmisosakonna täideviimisliidese täielikud seeria-, partii- ja numbrimärginumbrid](whats-new-scm-10-0-21.md) | Vaikimisi sees |
| Müük ja turundus | [Müügitellimuse üksikasjade jõudlustäiustus](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | Üldiselt saadaval |
| Müük ja turundus | Müügipakkumise üksikasjade jõudlustäiustus | Üldiselt saadaval |
| Müük ja turundus | Müügitellimusele viitavate andmete ekspordipoliitika | Kohustuslik |
| Müük ja turundus | [Müügitellimusest ostutellimuseni ridade kustutamise poliitika](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-purchase-order-line-deletion-policy) | Kohustuslik |
| Müük ja turundus | [Müügipakkumisele viitavate andmete ekspordipoliitika](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy)| Kohustuslik |
| Müük ja turundus | [Kontaktisiku andmeüksuse ekspordi optimeerimine](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | Vaikimisi sees |
| Müük ja turundus | Lubage müügipakkumise dokumendi sissejuhatuse ja dokumendi järelduste väljade otsing | Vaikimisi sees |
| Müük ja turundus | [Parandage klientide aruande „100 esimest” jõudlust](whats-new-scm-10-0-23.md) | Vaikimisi sees |
| Müük ja turundus | Prognoositava kliendisaldo ümberarvutamine | Vaikimisi sees |
| Müük ja turundus | [Müügi tagastustellimuse rea registreerimine kümnendkoha täpsusega koos tegeliku kaaluga ja ilma selleta](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | Vaikimisi sees |
| Müük ja turundus | [Müügi ja turunduse salvestatud vaated](saved-views-scm.md) | Vaikimisi sees |
| Müük ja turundus | Ühe klõpsuga müügitellimuse kinnitus | Vaikimisi sees |
| Laohaldus | [Asukohadirektiividega ristiliaadimismallid](../warehousing/planned-cross-docking.md) | Üldiselt saadaval |
| Laohaldus | [Keelake oodatud kviitungid kvaliteettellimustest, mille valim on blokeeritud varudes](../inventory/inventory-blocking.md) | Üldiselt saadaval |
| Laohaldus | Litsentsiplaadi vastuvõtu ajalugu | Üldiselt saadaval |
| Laohaldus | [Materjali käsitlemise seadmete liides](../warehousing/mhax.md) | Üldiselt saadaval |
| Laohaldus | [Ümmarda kogused lattu väljastamiseks lähima müügiüksuseni](whats-new-scm-10-0-19.md) | Üldiselt saadaval |
| Laohaldus | Laorakenduse tööloendite skaalaüksuse tugi | Üldiselt saadaval |
| Laohaldus | Saadetise voo sildi üksikasjad | Üldiselt saadaval |
| Laohaldus | [Kasutage pakkimisjaamas konteinerite sulgemiseks / uuesti avamiseks kiiremat API-d](whats-new-scm-10-0-21.md) | Üldiselt saadaval |
| Laohaldus | [Kinnitage täiendamise tööde jaoks valitud mallid](whats-new-scm-10-0-20.md) | Üldiselt saadaval |
| Laohaldus | Täiendamise malli lubamine, et kasutada olemasolevat viivitamatut täiendamise tööd (üksuste üleselt) | Kohustuslik |
| Laohaldus | WHS-i kasutaja loomisele GUID-de automaatne määramine | Kohustuslik |
| Laohaldus | Jäädvusta lao rakenduses koorma kaupade vastuvõtmise ajal tootevariandid ja jälgimisdimensioonid | Kohustuslik |
| Laohaldus | [Jälgimisdimensioonide kaudu juhitavate kaupade varude oleku muutmine](../inventory/inventory-statuses.md) | Kohustuslik |
| Laohaldus | [Muuda töö töökausta](../warehousing/change-work-pool-on-work.md) | Kohustuslik |
| Laohaldus | [Kogumi positsioon on täis](../warehousing/cluster-position-full.md) | Kohustuslik |
| Laohaldus | [Kogumi kõrvalepaneku funktsioon](../warehousing/putaway-clusters.md) | Kohustuslik |
| Laohaldus | [Kinnitamine ja üleviimine](../warehousing/confirm-and-transfer.md) | Kohustuslik |
| Laohaldus | [Pakett-töö väljuva saadetise kinnitamine](../warehousing/confirm-outbound-shipments-from-batch-jobs.md) | Kohustuslik |
| Laohaldus | [Saate kontrollida, kas mobiilsetes seadmetes kuvatakse vastuvõtu kokkuvõttelehte](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | Kohustuslik |
| Laohaldus | [Varude käsitsi paigutamise toimingu edasilükatud töötlemine](../warehousing/deferred-processing-manual-inventory-movement.md) | Kohustuslik |
| Laohaldus | Ära luba luua koormaid, mis ei vasta voo koorma loomise malli nõuetele | Kohustuslik |
| Laohaldus | [Täiustatud litsentsiplaadi sildipaigutused](../warehousing/document-routing-layout-for-license-plates.md) | Kohustuslik |
| Laohaldus | [Mitme SKU asukohakorralduste kõigi toimingute hindamine](../troubleshooting/warehousing/evaluate-multiple-location-directive-actions.md) | Kohustuslik |
| Laohaldus | Peida koguväärtuse väli lehtedel "Kõik koormused" ja "Koormuse üksikasjad" | Kohustuslik |
| Laohaldus | Litsentsiplaadi sildi koostekonfiguratsioon | Kohustuslik |
| Laohaldus | Koorma rea käsitsi korrigeerimine administraatorile või sarnastele usaldusväärsetele kasutajatele | Kohustuslik |
| Laohaldus | [Asukoha litsentsiplaadi paigutus](../warehousing/location-license-plate-positioning.md) | Kohustuslik |
| Laohaldus | [Asukoha tootedimensioonide segamine](../warehousing/location-product-dimension-mixing.md) | Kohustuslik |
| Laohaldus | Muuda mobiilse seadme varude liikumise varude oleku väli redigeeritavaks | Kohustuslik |
| Laohaldus | Käsitsi müügirea komplekteerimise teenus administraatorile või sarnastele usaldusväärsetele kasutajatele | Kohustuslik |
| Laohaldus | [Üleviimistellimusega lähetatud litsentsiplaatide kasutamise takistamine kõikides teistes ladudes peale sihtlao](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | Kohustuslik |
| Laohaldus | Viip välja „Asukoht/litsentsiplaat” mitmetähenduslike väärtuste lahendamiseks | Kohustuslik |
| Laohaldus | [Kvaliteedikontroll](../warehousing/quality-check.md) | Kohustuslik |
| Laohaldus | [Uue laorakenduse kasutajasätted, ikoonid ja etappide pealkirjad](../warehousing/install-configure-warehouse-management-app.md) | Kohustuslik |
| Laohaldus | [Täiendav asukohatsoon](../warehousing/additional-location-zones.md) | Vaikimisi sees |
| Laohaldus | [Laorakenduses ülekandetellimuste loomine ja töötlemine](../warehousing/create-transfer-order-from-warehouse-app.md) | Vaikimisi sees |
| Laohaldus | Luba lao mobiilsete seadmete jaoks kiire kinnitamine | Vaikimisi sees |
| Laohaldus | [Maksimaalne täitmisaeg laohalduse laoseisu kirjete puhastustööks](../warehousing/onhand-cleanup.md) | Vaikimisi sees |
| Laohaldus | [Väljamineva töökoormuse visualiseerimine](../warehousing/outbound-workload-visualization.md) | Vaikimisi sees |
| Laohaldus | [Laorakenduse sündmuste töötlemine](../warehousing/warehouse-app-events.md) | Vaikimisi sees |
| Laohaldus | [Koorma planeerimise töölaua salvestatud vaade](saved-views-scm.md) | Vaikimisi sees |
| Laohaldus | [Töö üksikasjade lehe salvestatud vaade](saved-views-scm.md) | Vaikimisi sees |
| Laohaldus | [Voo töötlemise salvestatud vaade](saved-views-scm.md) | Vaikimisi sees |
| Laohaldus | [Koormuse töötlemise salvestatud vaated](saved-views-scm.md) | Vaikimisi sees |
| Laohaldus | [Saadetise töötlemise salvestatud vaated](saved-views-scm.md) | Vaikimisi sees |
| Laohaldus | [Voo pakett-töö üksikasjad](../warehousing/wave-processing.md) | Vaikimisi sees |
| Laohaldus | [Voo täitmise teatised](../warehousing/wave-execution-notifications.md) | Vaikimisi sees |

## <a name="additional-resources"></a>Lisaressursid

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finantside ja toimingute rakenduste platvormi värskendused

Microsoft Dynamics 365 Supply Chain Management 10.0.25 sisaldab platvormivärskendusi. Lisateavet vt Platvormi värskendustest [versioonile 10.0.25 Finance and Operations rakendustest (aprill 2022).](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-25.md)

### <a name="bug-fixes"></a>Veaparandused

Lisateabe saamiseks veaparanduste kohta, mis sisalduvad 10.0.25 uuendustes, logige sisse teenusesse Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=654580&dbType=3&qc=3799fa965b008dd980d27cf740e4582e6384ec6601ae8a35b7eaec6f1287a868).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 ja majandusharu pilved: 2022 väljalaskevoo 1 plaan

Kas teile pakuvad huvi meie ärirakenduste või platvormi uued ja hiljuti väljaantud võimalused?

Vaadake [Dynamics 365 ja majandusharu pilved: 2022 väljalaskevoo 1 plaan](/dynamics365-release-plan/2022wave1/). Käsitleme ühes dokumendis kõiki üksikasju otsast lõpuni ja ülevalt alla, millest võite plaanide tegemisel lähtuda.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Eemaldatud ja aegunud Supply Chain Managementi funktsioonid

Teemas [Eemaldatud või aegunud Dynamics 365 Supply Chain Managementi funktsioonid](removed-deprecated-features-scm-updates.md) kirjeldatakse funktsioone, mis on eemaldatud või aegunud või kavandatakse eemaldada Supply Chain Managementist.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

Enne mis tahes funktsiooni eemaldamist tootest, teavitatakse aegumisest 12 kuud ette teemas [Eemaldatud või aegunud Dynamics 365 Supply Chain Managementi funktsioonid](removed-deprecated-features-scm-updates.md).

Murranguliste muudatuste puhul, mis mõjutavad ainult kompileerimise aega, kuid on binaarselt ühilduvad liivakasti- ja tootmiskeskkondadega, on aegumise aeg vähem kui 12 kuud. Need on tavaliselt funktsionaalsed uuendused, mida tuleb teha kompilaatori jaoks.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
