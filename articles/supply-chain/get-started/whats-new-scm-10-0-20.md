---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 Supply Chain Management 10.0.20. (august 2021)?
description: See artikkel kirjeldab funktsioone, mis on uued või muutunud Dynamics 365 Supply Chain Management 10.0.20-
author: kamaybac
ms.date: 05/28/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d99a7a7d0261ba0afd19efbb237dff329527723d
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219150"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10020-august-2021"></a>Mis on uut ja mida on muudetud rakenduses Dynamics 365 Supply Chain Management 10.0.20. (august 2021)?

[!include [banner](../includes/banner.md)]

See artikkel loetleb funktsioonid, mis on Microsofti versioonis Dynamics 365 Supply Chain Management 10.0.20 uued või muutunud. Selle versiooni number on 10.0.886 ja see on saadaval järgmiselt:

- **Väljalaske eelversioon:** mai 2021
- **Väljalaske üldine kättesaadavus (automaatne värskendamine):** juuli 2021
- **Väljalaske üldine kättesaadavus (automaatne värskendamine):** august 2021

## <a name="features-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

See väljalase hõlmab järgmisi funktsioone. Veerg *Funktsioon* pakub linke [väljalaskeplaani](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) kus saate vaadata iga funktsiooni ametlikke väljalaskekuupäevi. Veerg *Lisateave* pakub üksikasju/linke seotud dokumentatsioonile.

Suurem osa neist funktsioonidest tuleb enne kasutamist [Funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) abil lubada.

| Funktsiooniala | Funktsioon | Lisateave |
|---|---|---|
| Varud&nbsp;ja&nbsp;logistika | [Müügitellimuse üksikasjade jõudlustäiustus](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | See funktsioon muudab müügitellimuse avamisel kasutajaliidese paindlikumaks, eriti tellimused, mis sisaldavad palju ridu. |
| Tootmine | [Protsessi automatiseerimisvoogude kutsumine kvaliteettellimuste loomiseks](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/invoke-process-automation-flows-create-quality-orders) | [Protsessi automatiseerimisvoogude kutsumine kvaliteettellimuste loomiseks](../production-control/process-automation-quality-orders.md ) |
| Tootmine | [Kasutajaliidese juhtelementide laadid tootmisosakonna käivitamiseks](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-manufacturing) | [Tootmisosakonna täideviimisliidese konfigureerimine](../production-control/production-floor-execution-configure.md) |
| Planeerimine | [Planeerimise optimeerimise lõpmatu võimsuse ajastamine](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/schedule-infinite-capacity-support-planning-optimization) | [Piiramatu võimsusega planeerimine](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| Tooteteabe haldus | [Valemite ja nende koostisosade muudatuste haldamine](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/engineering-change-management-support-process-manufacturing) | [Valemite ja nende koostisainete muudatuste haldamine](../engineering-change-management/manage-formula-changes.md) |
| Tooteteabe haldus | [Toote valmisoleku kontrollid](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/product-readiness-checks) | [Toote valmisolek](../engineering-change-management/product-readiness.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selle väljalaske funktsioonide täiustused. Igaüks neist võimaldab olemasoleva funktsiooni järk-haaval täiustada. Kuna need on ainult täiustused, siis neid ei loetleta [väljalaskeplaanis](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Kindlustamaks, et need täiustused ei satu vastuollu olemasolevate kohanduste või eelistustega, lülitatakse iga neist vaikimisi välja (kui pole märgitud teisiti). Kui soovite mõnda neist funktsioonidest kasutada, peate need eraldi lubama [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Moodul | Funktsiooni&nbsp;nimi&nbsp;funtsiooni&nbsp;halduses | Lisateave |
|---|---|---|
| Koondplaneerimine | Korrigeeritud nõudluse prognoosi paralleelne lubamine | See funktsioon võimaldab korrigeeritud nõudluse prognoosi paralleelset lubada **Korrigeeritud nõudluse prognoosiks** lehel. Selle funktsiooni eesmärk on suurendada jõudlust suure arvu eelarvete autoriseerimisel. Autoriseerimisel saab kasutaja autoriseerimise dialoogis määrata **Lõimede arvu**. |
| Koondplaneerimine | Plaanitud hulgi- ja partiina tellimuste partiideks jaotatud kinnitamine ja konsolideerimine | See funktsioon võimaldab teil planeeritud hulgi- ja partiidena tellimuste kinnitamiseks ja konsolideerimiseks kasutada pakett-töid. |
| Tootmise juhtimine | Kopeeri üldised marsruudid | See funktsioon parandab kopeerimisprotsessi funktsiooni, et lubada kasutajatel kopeerida protsesse, mis pole kaubapõhised. See võimaldab süsteemil värskendada kogu asjakohast teavet (nt sait, protsessigrupp, ressursinõuded ja erinevad ajad) pärast seda, kui kopeerimisprotsessi funktsiooni on kasutatud kaubale veel määramata protsessi ülekirjutamiseks. |
| Tootmise juhtimine | Uuenda seotud ressursitingimused, kui marsruudi toimingut muudetakse | See funktsioon võimaldab süsteemil värskendada seotud ressursinõudeid pärast seda, kui kasutaja muudab olemasoleva marsruudi etapi toimimist. |
| Tooteteabe haldus | Materjalide aruanne sisaldab eeltöötlust, et vältida aegumist | Selle funktsiooniga töödeldakse koosluste aruannet. See aitab vältida ajalõppu, kui aruandel on suur andmete koormus. |
| Hanked | Luba hankega seotud töövoogude lähtestamine | Selle eelvaate funktsiooni abil saate lähtestada järgmised töövood: Purchase Order, Vendor Change ja Purchase Requisitions. |
| Transpordihaldus | Luba hankija arve töölehe loomine veose arve tühistamisel | Kui see funktsioon on lubatud, luuakse vastav hankijaarvete tööleht vastavusseviimise põhjustel ainult siis, kui kasutate makse hankija valikut. Vastasel juhul luuakse arve tööleht alati. |
| Laohaldus | Kinnitage täiendamise tööde jaoks valitud mallid | See funktsioon aitab tagada, et kasutajad valivad täiendustöö seadistamisel kehtivaid täiendamismalle. See takistab kasutajatel luua täiendamistööd ilma mallita ja valides malle tüübiga *Voo nõudlus* mis ei loo mingit täiendustööd ja võib võtta palju aega. |

## <a name="new-and-updated-documentation-resources"></a>Uued ja värskendatud dokumentatsiooni ressursid

Oleme hiljuti lisanud või oluliselt uuendanud järgmised spikriartiklid. Need ei ole tingimata seotud sellele väljalaskele lisatud uute funktsioonidega, nagu on loetletud eelmises jaotises, kuid need võivad aidata teil olemasolevatest funktsioonidest rohkem kasu saada.

| Funktsiooniala | Uued või värskendatud artiklid |
|---|---|
| Tehnilise muudatuse haldamine | [Toote töötsükli olekud ja kanded](../engineering-change-management/product-lifecycle-state-transactions.md) |
| Varud | [Varude nähtavuse lisandmoodul](../inventory/inventory-visibility.md)<br><br>[Kvaliteedi- ja mittevastavuse halduse ülevaade](../inventory/quality-management-processes.md) (pluss kõik seotud kvaliteedijuhtimise artiklid) |
| Hanked | [Hankija sertide haldamine](../../finance/public-sector/manage-vendor-certification.md) |
| Tootmise juhtimine | [Tootmisosakonna täideviimisliidese kujundamine](../production-control/production-floor-execution-styles.md) |
| Laohaldus | [Warehouse Management mobiilirakendusele astmeikoonide ja pealkirjade määramine](../warehousing/step-icons-titles.md)<br><br>[Laovarude manuaalse liigutamise edasilükatud töötlemine](../warehousing/deferred-processing-manual-inventory-movement.md) |

## <a name="additional-resources"></a>Lisaressursid

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platvormi värskendused finantside ja toimingute rakenduste jaoks

Microsoft Dynamics 365 Supply Chain Management 10.0.20 sisaldab platvormivärskendusi. Lisateavet vt platvormi värskendustest [versioonile 10.0.20 finantside ja toimingute rakendustest (juuli 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20.md).

### <a name="bug-fixes"></a>Veaparandused

Lisateabe saamiseks veaparanduste kohta, mis sisalduvad 10.0.20 uuendustes, logige sisse teenusesse Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=586707&dbType=3&qc=d0dad8eee2af234e8c288e2a7df14c579004518673d014be511f900cfed008f8). 

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365 2021. aasta väljalaske 1. voo plaan

Kas teile pakuvad huvi meie ärirakenduste või platvormi uued ja hiljuti väljaantud võimalused?

Vaadake teemat [Dynamics 365: 2021. aasta väljalaske 1. voo plaan](/dynamics365-release-plan/2021wave1/). Käsitleme ühes dokumendis kõiki üksikasju otsast lõpuni ja ülevalt alla, millest võite plaanide tegemisel lähtuda.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Eemaldatud ja aegunud Supply Chain Managementi funktsioonid

Artikli [eemaldatud või taunitud Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) funktsioonid kirjeldavad funktsioone, mis on tarneahela halduses eemaldatud või plaaniliselt eemaldatud või taunitud.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

Enne mis tahes funktsiooni eemaldamist tootest teatatakse amortiseerumisest [Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) artikli 12 kuu jooksul enne eemaldamist eemaldatud või taunitud funktsioonides.

Murranguliste muudatuste puhul, mis mõjutavad ainult kompileerimise aega, kuid on binaarselt ühilduvad liivakasti- ja tootmiskeskkondadega, on aegumise aeg vähem kui 12 kuud. Need on tavaliselt funktsionaalsed uuendused, mida tuleb teha kompilaatori jaoks.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

