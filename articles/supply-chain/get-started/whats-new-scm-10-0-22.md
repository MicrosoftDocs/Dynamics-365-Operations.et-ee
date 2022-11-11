---
title: Mis onuut või mida on muudetud rakenduses Dynamics 365 Supply Chain Management 10.0.22 (november 2021)
description: See artikkel kirjeldab funktsioone, mis on Microsoft Dynamics 365 Supply Chain Management 10.0.22 uued või muutunud.
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: b95f131a45c11748cfd4c66c47e5a51c765ed486
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740406"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10022-november-2021"></a>Mis onuut või mida on muudetud rakenduses Dynamics 365 Supply Chain Management 10.0.22 (november 2021)

[!include [banner](../includes/banner.md)]

See artikkel loetleb funktsioonid, mis on Microsofti versioonis Dynamics 365 Supply Chain Management 10.0.22 uued või muutunud. Selle versiooni number on 10.0.995 ja see on saadaval järgmiselt:

- **Avaldamise eelvaade:** september 2021
- **Väljalaske üldine kättesaadavus (ise värskendamine):** oktoober 2021
- **Väljalaske üldine kättesaadavus (automaatne värskendus):** november 2021

## <a name="features-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selles versioonis sisalduvad funktsioonid. Veerg *Funktsioon* pakub linke [väljalaskeplaani](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) kus saate vaadata iga funktsiooni ametlikke väljalaskekuupäevi. Veerg *Lisateave* pakub üksikasju/linke seotud dokumentatsioonile. Funktsiooni sisselülitamise määratlemiseks vaadake veergu *Lubatud*. Lisateavet funktsioonihalduse kasutamise kohta vt [Funktsioonihalduse ülevaade](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Võime seda artiklit värskendada, et kaasata funktsioonid, mis muutsid selle koostesse pärast selle artikli algset avaldamist.

| Funktsiooniala | Funktsioon | Lisateave | Lubaja:   |
|---|---|---|---|
| Planeerimine | [Planeerimise optimeerimise tugi võimetepõhisele ressursside jaotamisele](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capability-based-resource-allocation) | [Planeerimine koos ressursside valikuga vastavalt võimalustele](../master-planning/planning-optimization/capability-based-scheduling.md) | Funktsiooni haldus (*Planeerimise optimeerimise lõpmatu võimsuse ajastamine*) |

## <a name="feature-enhancements-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selle väljalaske funktsioonide täiustused. Kõik need täiustused parandavad olemasolevat funktsiooni järk-järgult. Kuna need on ainult täiustused, siis neid ei loetleta [väljalaskeplaanis](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Kindlustamaks, et need täiustused ei satu vastuollu olemasolevate kohanduste või eelistustega, lülitatakse iga neist vaikimisi välja (kui pole märgitud teisiti). Kui soovite mõnda neist funktsioonidest kasutada, peate need eraldi lubama [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Moodul | Funktsiooni nimi funktsioonihalduses | Lisateave |
|---|---|---|
| Hajutatud hübriidtopoloogia | *(Funktsioonihaldus pole nõutud.)* | <p>See vabastus laiendab laohalduse töökoormuse väljamineva koormuse planeerimise võimalusi pilve- ja servaskaala üksuste puhul.</p><p>Lisateavet vt [Laohalduse töökoormused pilv- ja perimeeterskaalaüksuste jaoks](../cloud-edge/cloud-edge-workload-warehousing.md).</p> |
| Tehnilise muudatuse haldamine | Tehnikatoodetele variantide loomine | <p>See funktsioon võimaldab teil luua mitmeid variante tehnika tootele, mis põhineb selle värvil, suurusel, stiilil või konfiguratsiooni dimensioonil.</p><p>Lisateavet vt teemast [Tehnikatoodete variantide loomine](../engineering-change-management/engineering-variants.md).</p> |
| Varude ja laohaldus | Varude nähtavuse integreerimine broneerimise nihkega | <p>Seda funktsiooni saab lubada ainult siis, kui *Varude nähtavuse integreerimise* funktsioon on lubatud. See pakub funktsioone lao nähtavuse puhul tehtud tasakaalustusreserveeringute jaoks.</p><p>Lisateavet vt teemast [Varude nähtavuse reserveeringud](../inventory/inventory-visibility-reservations.md).</p> |

## <a name="new-and-updated-documentation-resources"></a>Uued ja värskendatud dokumentatsiooni ressursid

Oleme hiljuti lisanud või oluliselt uuendanud järgmised spikriartiklid. Need artiklid ei pea tingimata olema seotud uute funktsioonidega, mis selle väljalaske jaoks lisati, nagu on loetletud eelmises jaotises. Kuid need võivad aidata teil rohkem funktsionaalsust olemasolevatest funktsioonidest kätte saada.

| Funktsiooniala | Uued või värskendatud artiklid |
|---|---|
| Tehnilise muudatuse haldamine | [Tehnika muudatuste halduse ülevaates](../engineering-change-management/product-engineering-overview.md) loetletakse nüüd kõik funktsioonihalduses saadaolevad seotud valikulised funktsioonid |
| Koondplaneerimine | [Nõudluse prognoosi häälestus](../master-planning/demand-forecasting-setup.md) |
| Koondplaneerimine | [Netonõuded ja sidumisteave](../master-planning/planning-optimization/net-requirements.md) |
| Laohaldus | [Lattu väljastamine](../warehousing/release-to-warehouse-process.md) annab täieliku lattu vabastamise protsessi üksikasjaliku ülevaate |

## <a name="additional-resources"></a>Lisaressursid

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platvormi värskendused finantside ja toimingute rakenduste jaoks

Microsoft Dynamics 365 Supply Chain Management 10.0.22 sisaldab platvormivärskendusi. Lisateavet vt platvormi värskendustest [versioonile 10.0.22 finantside ja toimingute rakendustest (november 2021).](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22.md)

### <a name="bug-fixes"></a>Veaparandused

Lisateabe saamiseks veaparanduste kohta, mis sisalduvad 10.0.22 uuendustes, logige sisse teenusesse Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=615299).

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

