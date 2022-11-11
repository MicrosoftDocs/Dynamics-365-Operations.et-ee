---
title: Mis onuut või mida on muudetud rakenduses Dynamics 365 Supply Chain Management 10.0.30 (november 2022)
description: See artikkel kirjeldab funktsioone, mis on uued või muudetud rakenduses Microsoft Dynamics 365 Supply Chain Management 10.0.30.
author: kamaybac
ms.date: 11/07/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-09-08
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 20674ebd9d49b077371998f53d2b22c74f888fc6
ms.sourcegitcommit: 613be2f35e600ae1a1fa7ea2ae30e78984ca398a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748460"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10030-november-2022"></a>Mis onuut või mida on muudetud rakenduses Dynamics 365 Supply Chain Management 10.0.30 (november 2022)

[!include [banner](../includes/banner.md)]

See artikkel loetleb funktsioonid, mis on Microsofti versioonis Dynamics 365 Supply Chain Management 10.0.30 uued või muutunud. Sellel versioonil on järgu number 10.0.1362 see on saadaval järgmises graafikus.

- **Avaldamise eelvaade:** september 2022
- **Väljalaske üldine kättesaadavus (ise värskendamine):** oktoober 2022
- **Väljalaske üldine kättesaadavus (automaatne värskendus):** november 2022

## <a name="features-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selles versioonis sisalduvad funktsioonid. Võime seda artiklit värskendada, et kaasata funktsioonid, mis lisati koostesse pärast selle artikli algset avaldamist.

| Funktsiooniala | Funktsioon | Lisateave | Lubaja:   |
|---|---|---|---|
| Varud ja logistika | [Jälgige eraldamistes kergelt reserveeritud koguseid.](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/track-soft-reserved-quantities-within-allocations) | [Inventory Visibility varude eraldamine](../inventory/inventory-visibility-allocation.md) |  Lubatud teenuse [konfiguratsiooni järgi](../inventory/inventory-visibility-configuration.md) |
| Tootmine | [Anduriandmete teabega seadmete s monitorimine](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/monitor-equipment-sensor-data-intelligence) | [Sensor Data Intelligence’i avaleht](../sensor-data-intelligence/sdi-home-page.md) | Funktsioonihaldus:<br>*(Eelversioon) Anduri andmeanalüüs* |
| Laohaldus | [Mitmetasandilised demeetrid laohalduse mobiilirakenduse jaoks](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/multi-level-detours-warehouse-management-mobile-app) | [Mobiilse seadme menüükäskude sammude ümbersuunamise konfigureerimine](../warehousing/warehouse-app-detours.md) | Funktsioonihaldus:<br>*Mitmetasandilised kõrvalepõiked Warehouse Managementi mobiilirakenduses* |

## <a name="feature-enhancements-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selle väljalaske funktsioonide täiustused. Kõik need täiustused parandavad olemasolevat funktsiooni järk-järgult. Kuna need on ainult täiustused, siis neid ei loetleta [väljalaskeplaanis](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Kindlustamaks, et need täiustused ei satu vastuollu olemasolevate kohanduste või eelistustega, lülitatakse iga neist vaikimisi välja (kui pole märgitud teisiti).

Kui soovite mõne neist funktsioonidest sisse ja välja lülitada, peate seda funktsioonihalduses [tegema](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Moodul | Funktsiooni nimi funktsioonihalduses | Lisateave |
|---|---|---|
| Tootmise juhtimine | Laoseisu teave tootmistellimustel väljastuslehele | Lisab veeru vaba laoseisu kogusele reaüksuse jaoks vabastatavate tootmistellimuste **ridade jaotises** |
| Transpordihaldus | Saadetiste määramine seotud protsessisegmentidesse | See funktsioon võimaldab süsteemil saadetise veokulusid täpsemini osadeks määrata, sh mitme saadetisega koormatele, mis tarnitakse erinevatesse segmentimissihtkohtadesse ühes protsessis. See määrab iga saadetise sobivama marsruudisegmendiga, mis põhineb saadetise ja segmendi sihtaadressidel. Funktsioon arvutab siis iga saadetise veokulu proportsioonina koorma veose kogukulust, mis põhineb saadetise suhtelisel kaalul, mahul, kogusel ja läbitud vahemaal. See funktsioon kehtib ainult transpordihalduse (TMS) mooduliga hallatavate saadetiste puhul. |

## <a name="additional-resources"></a>Lisaressursid

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finantside ja toimingute rakenduste platvormi värskendused

Microsoft Dynamics 365 Supply Chain Management 10.0.30 sisaldab platvormivärskendusi. Lisateavet vt platvormi värskendustest [versioonile 10.0.30 Finance and Operations rakendustest (november 2022).](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md)

### <a name="bug-fixes"></a>Veaparandused

Teavet versiooni 10.0.30 igas värskenduses kaasatud vigaparanduste kohta logige sisse elutsükli teenustesse (LCS) [ja vaadake KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468) artiklit.

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
