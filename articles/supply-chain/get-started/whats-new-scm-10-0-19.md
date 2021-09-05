---
title: Mis on uut või mida on muudetud rakenduse Dynamics 365 Supply Chain Management versioonis 10.0.19 (juuni 2021)
description: Selles teemas kirjeldatakse Dynamics 365 Supply Chain Management 10.0.19 uusi või muutunud funktsioone.
author: kamaybac
ms.date: 04/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-23
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 74720e387d5db7de841228e6573fb40c5d22588b
ms.sourcegitcommit: 2b04b5a5c883d216072bb91123f9c7709a41f69a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2021
ms.locfileid: "7384655"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-version-10019-june-2021"></a>Mis on uut või mida on muudetud rakenduse Dynamics 365 Supply Chain Management versioonis 10.0.19 (juuni 2021)

[!include [banner](../includes/banner.md)]

Selles teemas loendatakse Microsoft Dynamics 365 Supply Chain Managementi versiooni 10.0.19 uusi või muutunud funktsioone. Selle versiooni number on 10.0.837 ja see on saadaval järgmiselt:

- **Eelvaateversiooni välja andmine:** aprill 2021
- **Väljalaske üldine kättesaadavus (automaatne värskendamine):** juuni 2021
- **Väljalaske üldine kättesaadavus (automaatne värskendamine):** juuni 2021

## <a name="features-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

See väljalase hõlmab järgmisi funktsioone. Veerg *Funktsioon* pakub linke [väljalaskeplaani](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) kus saate vaadata iga funktsiooni ametlikke väljalaskekuupäevi. Veerg *Lisateave* pakub üksikasju/linke seotud dokumentatsioonile.

Suurem osa neist funktsioonidest tuleb enne kasutamist [Funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) abil lubada.

| Funktsiooniala | Funktsioon | Lisateave |
|---|---|---|
| Varud&nbsp;ja&nbsp;logistika | [Müüja edastatud panga üksikasjade kinnitamine ja salvestamine](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/approve-save-vendor-submitted-bank-details) | [Hankija pangakonto teabe haldamine](../../finance/accounts-payable/maintain-vendor-bank-info.md) |
| Varud ja logistika | [Kontaktisiku andmeüksuse ekspordi optimeerimine](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization)  | Kui see on lubatud, ei põhjusta viidatud andmete muudatused seotud müügitellimuste (või ridade) kaasamist järgmisse astmelisse eksporti. Kui see funktsioon on keelatud, kaasatakse viidatud andmete muudatustega seotud kontaktid järgmisse täiendavasse eksporti. |
| Varud ja logistika | [Lao käivitamisvõimaluste astmelised täiustused koos skaalaüksustega](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/incremental-enhancements-warehouse-execution-capabilities-scale-units) |[Sõnumi töötleja sõnumid](../cloud-edge/cloud-edge-message-processor-messages.md)<br><br>[Laovarude korrigeerimine](../cloud-edge/cloud-edge-warehouse-inventory-adjustment.md)<br><br>[Laohaldustöökoormused pilv- ja perimeeterskaalaüksuste jaoks](../cloud-edge/cloud-edge-workload-warehousing.md) |
| Varud ja logistika | [Müügipakkumise lehel dokumendi sissejuhatuse ja dokumendi lõppväljade otsingufunktsioonid](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | See funtsiooni lisab otsingufunktsioonide **Dokumendi sissejuhatus** ja **Dokumendi järeldus** väljal **Müügipakkumiste** lehel.<br><br>Funktsioon on vaikimisi lubatud. |
| Varud ja logistika | [Lao käivitamine oma kohandatud riistvara servaskaala ühikutega](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-edge-scale-units-custom-hardware) | [Juurutage servaskaala ühikud kohandatud riistvaras LBD-ga](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Tootmine | [Lao käivitamine oma kohandatud riistvara servaskaala ühikutega](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-edge-scale-units-custom-hardware) | [Perimeeterskaalaüksuste juurutamine kohandatud riistvara jaoks LBD abil](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Planeerimine | [Planeerimise optimeerimise lõpmatu võimsuse ajastamine](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/schedule-infinite-capacity-support-planning-optimization) | [Piiramatu võimsusega planeerimine](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| Planeerimine | Päringupõhise plaanitud tellimuse kinnitamine | [Kindlad plaanitud tellimused](../master-planning/planning-optimization/planned-order-firming.md) |
| Tooteteabe haldus | [Variandi soovituste lehe täiustused](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/variant-suggestions-page-improvements) | [Eelmääratletud tootevariantide loomine](../pim/tasks/create-predefined-product-variants.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selle väljalaske funktsioonide täiustused. Igaüks neist võimaldab olemasoleva funktsiooni järk-haaval täiustada. Kuna need on ainult täiustused, siis neid ei loetleta [väljalaskeplaanis](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Kindlustamaks, et need täiustused ei satu vastuollu olemasolevate kohanduste või eelistustega, lülitatakse iga neist vaikimisi välja (kui pole märgitud teisiti). Kui soovite mõnda neist funktsioonidest kasutada, peate need eraldi lubama [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Funktsiooniala | Funktsiooni&nbsp;nimi&nbsp;funtsiooni&nbsp;halduses | Lisateave |
|---|---|---|
| Müük ja turundus | Müügiajaloo puhastamise jõudluse parendused | Müügiajaloo puhastamine võib võtta kaua aega, kui seda käitatakse harva suure müügiuuendustega keskkondades. Kestuse vähendamiseks ja töökindluse parandamiseks tükeldab see funktsioon puhastuse piiratud kestusega partiidele. Võimaluse korral võimendatakse andmebaasi võimalusi lukustamise minimeerimiseks ja kannete tabelite ühendamise vältimiseks puhastamise ajal. |
| Müük ja turundus | Värskenda kontsernisiseste tellimuste taotletud kviitungi kuupäev kinnitatud kuupäevale | See funktsioon võimaldab kontsernisisese otsetarne kasutamisel kontrollida, mis juhtub müügi- ja ostukuupäeva välja väärtustega. Saate valida, kas süsteem uuendab taotletud kuupäevi või jäetakse nende uuendamine vahele. Kui uuendamise vahele jätate, tähistavad taotletud kuupäevad kliendi taotletud kuupäeva. Uuendamise lubamisel tähistavad taotletud kuupäevad (tarnekuupäeva kontrolli kasutamisel) algselt ainult seda, mida klient taotles. Tarnekuupäeva kontroll, kui see erineb väljast *Pole*, alistab algselt taotletud teabe. Saate selle suvandi seada, kasutades uut **Nõutava vastuvõtukuupäeva värskendamise kinnitatud kuupäeva** sättega kontsernisisese hankija või kliendi sätetes.<br><br>Kui see funktsioon on keelatud, kirjutab süsteem nõutava sissetulekukuupäeva üle algsetele müügitellimustele, mis põhinevad tarnekuupäeva kontrollreeglil, kuid nõutav tarnekuupäev jääb samaks. |
| Laohaldus | Ümmarda kogused lattu väljastamiseks lähima müügiüksuseni | See funktsioon lisab suvandi, mis võib piirata tellimuskoguseid lattu vabastamisel. Kui see on lubatud, ümardatakse tellimuse kogused allapoole lähima täismüügiühikuni ja tellimused, mis sisaldavad alla ühe müügiühiku koguseid, lükatakse vabastamiseks tagasi. |
| Laohaldus | Organisatsiooniülene voomeetod „Graafiku töö loomine” | Selle funktsiooni lubamisel konfigureeritakse *Plaanitud töö loomise* voomeetod lisatakse paralleelselt kõigi juriidiliste isikute lõikes. See mõjutab ka mitmeid lisasätteid. Üksikasjadega tutvumiseks vaadake [Voo ajal töö loomise plaanimine](../warehousing/configure-wave-schedule-work-creation.md). |

## <a name="new-and-updated-documentation-resources"></a>Uued ja värskendatud dokumentatsiooni ressursid

Oleme hiljuti lisanud või oluliselt uuendanud järgmisi abiteemasid. Need ei ole tingimata seotud sellele väljalaskele lisatud uute funktsioonidega, nagu on loetletud eelmises jaotises, kuid need võivad aidata teil olemasolevatest funktsioonidest rohkem kasu saada.

| Funktsiooniala | Uued või värskendatud teemad |
|---|---|
| Tehnilise muudatuse haldamine | [Tehnilise muudatuse haldamine KKKs](../engineering-change-management/change-management-faq.md) |
| Hanked | [Kategooriataotlused hankijatelt](../procurement/category-requests-from-vendors.md) |
| Tooteteabe haldus | [Mõõtühiku haldamine](../pim/tasks/manage-unit-measure.md)<br><br>[Toote konfiguratsioonimudeli arvutamised](../pim/config-model-calculations.md) |
| Tootmise juhtimine | [Töö ID-de ühtsed numbrijärjestused](../production-control/unified-job-ids.md) |
| Transpordihaldus | [LTL-klassid](../transportation/ltl-class.md)<br><br>[NMFC-koodid](../transportation/nmfc-codes.md) |
| Laohaldus | [Lao partii ja seeria reserveerimishierarhiate tõrkeotsing](../warehousing/troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md) |
| Laohaldus, voo loomine ja töötlemine | [Voo loomine ja töötlemine](../warehousing/wave-processing.md)<br><br>[Voo töötlemise laoparameetrid](../warehousing/wave-warehouse-parameters.md)<br><br>[Voomallid](../warehousing/wave-templates.md)<br><br>[Vooeraldus](../warehousing/wave-allocation-method.md)<br><br>[Voo ajal töö loomise plaanimine](../warehousing/configure-wave-schedule-work-creation.md)<br><br>[Konteinerisse määramine](../warehousing/wave-containerization.md)<br><br>[Voo täitmise teatised](../warehousing/wave-execution-notifications.md) |

## <a name="additional-resources"></a>Lisaressursid

### <a name="platform-updates-for-finance-and-operations-apps"></a>Teenuse Finance and Operations rakenduste platvormivärskendused

Microsoft Dynamics 365 Supply Chain Management 10.0.19 sisaldab platvormivärskendusi. Lisateavet leiate teemast [Platvormi Finance and Operations rakenduste versiooni 10.0.19 värskendused (juuni 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19.md).

### <a name="bug-fixes"></a>Veaparandused

Lisateabe saamiseks veaparanduste kohta, mis sisalduvad 10.0.19 uuendustes, logige sisse teenusesse Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=575415).

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365 2021. aasta väljalaske 1. voo plaan

Kas teile pakuvad huvi meie ärirakenduste või platvormi uued ja hiljuti väljaantud võimalused?

Vaadake teemat [Dynamics 365: 2021. aasta väljalaske 1. voo plaan](/dynamics365-release-plan/2021wave1/). Käsitleme ühes dokumendis kõiki üksikasju otsast lõpuni ja ülevalt alla, millest võite plaanide tegemisel lähtuda.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Eemaldatud ja aegunud Supply Chain Managementi funktsioonid

Teemas [Eemaldatud või aegunud Dynamics 365 Supply Chain Managementi funktsioonid](removed-deprecated-features-scm-updates.md) kirjeldatakse funktsioone, mis on eemaldatud või aegunud või kavandatakse eemaldada Supply Chain Managementist.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

Enne mis tahes funktsiooni eemaldamist tootest, teavitatakse aegumisest 12 kuud ette teemas [Eemaldatud või aegunud Dynamics 365 Supply Chain Managementi funktsioonid](removed-deprecated-features-scm-updates.md).

Murranguliste muudatuste puhul, mis mõjutavad ainult kompileerimise aega, kuid on binaarselt ühilduvad liivakasti- ja tootmiskeskkondadega, on aegumise aeg vähem kui 12 kuud. Need on tavaliselt funktsionaalsed uuendused, mida tuleb teha kompilaatori jaoks.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
