---
title: Dynamics 365 Supply Chain Managementi versiooni 10.0.24 eelversioon (veebruar 2022)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Supply Chain Management 10.0.24 uusi või muutunud funktsioone.
author: kamaybac
ms.date: 12/03/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: f6402d7f9f433ca621c475bd62553529943dbe62
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920544"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10024-february-2022"></a>Dynamics 365 Supply Chain Managementi versiooni 10.0.24 eelversioon (veebruar 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Selles teemas loetletakse rakenduse Microsoft Dynamics 365 Supply Chain Management eelversiooni 10.0.24 uued või muutunud funktsioonid. Selle versiooni number on 10.0.1084 ja see on saadaval järgmiselt:

- **Väljalaske eelvaade:** detsember 2021
- **Väljalaske üldine kättesaadavus (iseseisev värskendamine):** jaanuar 2022
- **Väljalaske üldine kättesaadavus (automaatne värskendamine):** veebruar 2022

## <a name="features-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selles versioonis sisalduvad funktsioonid. Võime värskendada seda teemat, et lisada sellesse funktsioone, mis on loodud pärast selle esialgset avaldamist tehtud veaparandusi.

| Funktsiooniala | Funktsioon | Lisateave | Lubaja:   |
|---|---|---|---|
| Hajutatud hübriidtopoloogia | [Täiustatud lao käivitamise töökoormused kaaluüksustes](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-warehouse-execution-workloads-scale-units) | [Laohaldustöökoormused pilv- ja perimeeterskaalaüksuste jaoks](../cloud-edge/cloud-edge-workload-warehousing.md) | Vaikimisi lubatud. |
| Planeerimine | [Plaanimise optimeerimise tugi lisatellimuse marginaali ja väljamineku kasumi jaoks](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-reorder-margin-issue-margin) | [Ohutuspiirid](../master-planning/planning-optimization/safety-margins.md) | Vaikimisi lubatud. |

## <a name="feature-enhancements-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selle väljalaske funktsioonide täiustused. Kõik need täiustused parandavad olemasolevat funktsiooni järk-järgult. Kuna need on ainult täiustused, siis neid ei loetleta [väljalaskeplaanis](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Kindlustamaks, et need täiustused ei satu vastuollu olemasolevate kohanduste või eelistustega, lülitatakse iga neist vaikimisi välja (kui pole märgitud teisiti).

Kui soovite mõne neist funktsioonidest sisse ja välja lülitada, peate seda [funktsioonihalduses tegema](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Moodul | Funktsiooni nimi funktsioonihalduses | Lisateave |
|---|---|---|
| Tootmise juhtimine | Tootmistellimuste vajaduse korral materjali saadavuse kontroll | See funktsioon muudab kiiremaks tootmistellimuse **avamiseks lehekülje** vabastamise, mis on saadaval tootmispinna **halduse** tööruumis. Ilma selle funktsioonita kontrollib süsteem automaatselt, kas materjalid on saadaval kõigi loetletud tootmistellimuste jaoks kohe, kui avate lehekülje, mis võib võtta palju aega, kui teil on palju tellimusi. Kui see funktsioon on lubatud, pakub süsteem hoopis tööriistariba nuppu, mille abil saate käivitada materjalide kontrolli ainult valitud tellimustele ja vajadusel. |
| Tootmise juhtimine | (Eelversioon) Materjali tarbimise registreerimine tootmisosakonna täideviimisliideses (mitte-WMS) | See funktsioon võimaldab töötajatel kasutada tootmispinna käivitamise liidest materjalitarbimise, partiinumbrite ja seerianumbrite registreerimiseks. See funktsioon toetab ainult kaupu, mis ei ole lubatud täpsemate laoprotsesside (WMS) kasutamiseks. WMS-iga lubatud kaupade tugi on plaanitud tulevaseks väljalaskeks.<p>Osa tootjaid, eriti neid, kes kuuluvad protsessitööstusesse, peavad iga partii või tootmistellimuse puhul eraldi registreerima tarbitud materjali hulga. Töötajad võivad näiteks kaalu kasutada oma töös tarbitud materjali kaalu kaalumiseks. Täieliku materjalijälgitavuse tagamiseks peavad need organisatsioonid registreerima ka iga toote tootmises kasutatud partiinumbrid. |
| Tootmise juhtimine | Teata pilve ja servaskaala ühiku laohalduse töökoormusest lõpetatuna | See funktsioon võimaldab töötajatel kasutada laohalduse mobiilirakendust, et teatada tootmise või partii tellimuse lõpetatuna, kui rakendus töötab laohalduse töökoormusega pilves või servaskaala üksuses. Lisateavet vt lõpetatuna [kinnitamine ja kaaluühiku panemine.](../cloud-edge/cloud-edge-workload-manufacturing.md#RAF) |
| Tootmise juhtimine | Käivita tootmistellimuse laohalduse töökoormuses pilve ja servaskaala ühiku puhul | See funktsioon võimaldab töötajatel kasutada laohalduse mobiilirakendust, et käivitada tootmis- või partiitellimus, kui rakendus töötab pilves või servaskaala üksuses laohalduse töökoormuse suhtes. |
| Laohaldus | Uued koorma planeerimise töölaua leheküljed | Lubab kaks uut koorma planeerimise töölaualehte: sissetuleva koorma planeerimise töölaud ja väljamineva **koorma** **plaanimise** töölaud. |

## <a name="new-and-updated-documentation-resources"></a>Uued ja värskendatud dokumentatsiooni ressursid

Oleme hiljuti lisanud või oluliselt uuendanud järgmisi abiteemasid. Need teemad ei ole tingimata seotud uute funktsioonidega, mis sellele väljalaskele lisati, nagu on loetletud eelmises jaotises. Kuid need võivad aidata teil rohkem funktsionaalsust olemasolevatest funktsioonidest kätte saada.

| Funktsiooniala | Uued või värskendatud teemad |
|---|---|
| Kuluhaldus | [Laoväärtuse aruanded](../cost-management/inventory-value-report-storage.md) |
| Kuluhaldus | [Varude väärtuse aruande näited ja loogika](../cost-management/inventory-value-report-examples.md) |
| Koondplaneerimine | [Kuupäeva ja kellaaja parameetrid, mida planeerimise optimeerimine ei kasuta](../master-planning/planning-optimization/date-time-used.md) |
| Koondplaneerimine | [Nõudluse prognoosi häälestus](../master-planning/demand-forecasting-setup.md) |
| Koondplaneerimine | [Puhvervaru abil üksuste minimaalse laovaru uuendamine](../master-planning/safety-stock-journal.md) |
| Tootmise juhtimine | [Tootmisosakonna täideviimisliidese kohandamine](../production-control/production-floor-execution-customize.md) |
| Tootmise juhtimine | [Tootmisosakonna täideviimisliidese kujundamine](../production-control/production-floor-execution-styles.md) |
| Müük ja turundus | [Müügiajaloo puhastamise jõudluse täiustused](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) |
| Laohaldus | [Mobiilse seadme kasutaja kontod](../warehousing/mobile-device-work-users.md) |

## <a name="additional-resources"></a>Lisaressursid

### <a name="platform-updates-for-finance-and-operations-apps"></a>Teenuse Finance and Operations rakenduste platvormivärskendused

Microsoft Dynamics 365 Supply Chain Management 10.0.24 sisaldab platvormivärskendusi. Lisateavet leiate teemast [Platvormivärskendused Finance and Operations rakenduste versiooni 10.0.24 jaoks (veebruar 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-24.md).

### <a name="bug-fixes"></a>Veaparandused

Lisateabe saamiseks veaparanduste kohta, mis sisalduvad 10.0.24 uuendustes, logige sisse teenusesse Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=641306&dbType=3&qc=5b1d5e49c96b8a5cfb5601889a413e6f3773ba6500f9bc47310dcc5c54fff42f).

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
