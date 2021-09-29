---
title: Dynamics 365 Supply Chain Management eelvaade 10.0.22 (november 2021)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Supply Chain Management 10.0.22 uusi või muutunud funktsioone.
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c4aac62b36cd271e1c5fc3bcbbfdd785963fc368
ms.sourcegitcommit: 24e20b3b96834b23311f1bf5dbab28baf3323728
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/08/2021
ms.locfileid: "7484068"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10022-november-2021"></a>Dynamics 365 Supply Chain Management eelvaade 10.0.22 (november 2021)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Selles teemas loetletakse rakenduse Microsoft Dynamics 365 Supply Chain Management eelversiooni 10.0.22 uued või muutunud funktsioonid. Selle versiooni number on 10.0.995 ja see on saadaval järgmiselt:

- **Avaldamise eelvaade:** september 2021
- **Väljalaske üldine kättesaadavus (ise värskendamine):** oktoober 2021
- **Väljalaske üldine kättesaadavus (automaatne värskendus):** november 2021

## <a name="features-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selles versioonis sisalduvad funktsioonid. Veerg *Funktsioon* pakub linke [väljalaskeplaani](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) kus saate vaadata iga funktsiooni ametlikke väljalaskekuupäevi. Veerg *Lisateave* pakub üksikasju/linke seotud dokumentatsioonile. Funktsiooni sisselülitamise määratlemiseks vaadake veergu *Lubatud*. Lisateavet funktsioonihalduse kasutamise kohta vt [Funktsioonihalduse ülevaade](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Võime värskendada seda teemat, et lisada sellesse funktsioone, mis on loodud pärast selle esialgset avaldamist tehtud veaparandusi.

| Funktsiooniala | Funktsioon | Lisateave | Lubaja:   |
|---|---|---|---|
| Planeerimine | [Planeerimise optimeerimise tugi võimetepõhisele ressursside jaotamisele](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capability-based-resource-allocation) | [Planeerimine koos ressursside valikuga vastavalt võimalustele](../master-planning/planning-optimization/capability-based-scheduling.md) | Funktsiooni haldus (*Planeerimise optimeerimise lõpmatu võimsuse ajastamine*) |

## <a name="feature-enhancements-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selle väljalaske funktsioonide täiustused. Kõik need täiustused parandavad olemasolevat funktsiooni järk-järgult. Kuna need on ainult täiustused, siis neid ei loetleta [väljalaskeplaanis](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Kindlustamaks, et need täiustused ei satu vastuollu olemasolevate kohanduste või eelistustega, lülitatakse iga neist vaikimisi välja (kui pole märgitud teisiti). Kui soovite mõnda neist funktsioonidest kasutada, peate need eraldi lubama [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Funktsiooniala | Funktsiooni nimi funktsioonihalduses | Lisateave |
|---|---|---|
| Kuluhaldus | Standardkulu ümardamise ümberhindamiste jaoks seotud kannete loomine | <p>Kui tehakse kannete finantsarvestus (nt müügitellimuse arve või laokanne), loob süsteem iga seotud standardkulu ümardamise ümberhindluse jaoks eraldi kande ja seob selle finantsi sisestuskandega seotud kandena.</p><p>Ilma selle funktsioonita salvestab süsteem standardkulu ümardamise ümberhindlused samale kande sisestamisele. Selline käitumine võib mõnikord põhjustada vastuolulisi kuupäeva andmeid, kuna ümberhindamised kasutavad seansi või süsteemi kuupäeva, samas kui finantssisestused kasutavad sisestuskuupäeva.</p> |
| Hajutatud hübriidtopoloogia | *(Funktsioonihaldus pole nõutud.)* | <p>See vabastus laiendab laohalduse töökoormuse väljamineva koormuse planeerimise võimalusi pilve- ja servaskaala üksuste puhul.</p><p>Lisateavet vt [Laohalduse töökoormused pilv- ja perimeeterskaalaüksuste jaoks](../cloud-edge/cloud-edge-workload-warehousing.md).</p> |
| Tehnilise muudatuse haldamine | Tehnikatoodetele variantide loomine | <p>See funktsioon võimaldab teil luua mitmeid variante tehnika tootele, mis põhineb selle värvil, suurusel, stiilil või konfiguratsiooni dimensioonil.</p><p>Lisateavet vt teemast [Tehnikatoodete variantide loomine](../engineering-change-management/engineering-variants.md).</p> |
| Varude ja laohaldus | Varude nähtavuse integreerimine broneerimise nihkega | <p>Seda funktsiooni saab lubada ainult siis, kui *Varude nähtavuse integreerimise* funktsioon on lubatud. See pakub funktsioone lao nähtavuse puhul tehtud tasakaalustusreserveeringute jaoks.</p><p>Lisateavet vt teemast [Varude nähtavuse reserveeringud](../inventory/inventory-visibility-reservations.md).</p> |
| Müük ja turundus | Postitamiseks valitavate müügitellimuste arvu piiramine | <p>See funktsioon on automaatselt lubatud. Funktsioon lisab lehele **Müügireskontro parameetrid** sätte **Müügitellimuste maks. arv sisestamisel**. See väli võimaldab teil määratleda maksimaalse müügitellimuste arvu, mida saab valida kinnituste, komplekteerimislehtede, saatelehtede ja arvete sisestamisel müügitellimuste loendilehelt. Vaikeväärtus on *100*.</p><p>See funktsioon aitab parandada müügitellimuste loendilehe jõudlust, kui valitud on märkimisväärne arv müügitellimusi. See ei mõjuta müügitellimuste arvu, mida töötleb perioodiline ülesanne.</p> |

## <a name="new-and-updated-documentation-resources"></a>Uued ja värskendatud dokumentatsiooni ressursid

Oleme hiljuti lisanud või oluliselt uuendanud järgmisi abiteemasid. Need teemad ei ole tingimata seotud uute funktsioonidega, mis sellele väljalaskele lisati, nagu on loetletud eelmises jaotises. Kuid need võivad aidata teil rohkem funktsionaalsust olemasolevatest funktsioonidest kätte saada.

| Funktsiooniala | Uued või värskendatud teemad |
|---|---|
| Tehnilise muudatuse haldamine | [Tehnika muudatuste halduse ülevaates](../engineering-change-management/product-engineering-overview.md) loetletakse nüüd kõik funktsioonihalduses saadaolevad seotud valikulised funktsioonid |
| Koondplaneerimine | [Nõudluse prognoosi häälestus](../master-planning/demand-forecasting-setup.md) |
| Koondplaneerimine | [Netonõuded ja sidumisteave seoses planeerimise optimeerimisega](../master-planning/planning-optimization/net-requirements.md) |
| Laohaldus | [Lattu väljastamine](../warehousing/release-to-warehouse-process.md) annab täieliku lattu vabastamise protsessi üksikasjaliku ülevaate |

## <a name="additional-resources"></a>Lisaressursid

### <a name="platform-updates-for-finance-and-operations-apps"></a>Teenuse Finance and Operations rakenduste platvormivärskendused

Microsoft Dynamics 365 Supply Chain Management 10.0.22 sisaldab platvormivärskendusi. Lisateavet leiate teemast [Platvormivärskendused Finance and Operations rakenduste versiooni 10.0.22i jaoks (veebruar 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22.md). <!-- KFM: Confirm link -->

### <a name="bug-fixes"></a>Veaparandused

Lisateabe saamiseks veaparanduste kohta, mis sisalduvad 10.0.22 uuendustes, logige sisse teenusesse Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=615299).

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
