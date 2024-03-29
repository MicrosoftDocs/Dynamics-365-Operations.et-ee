---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Supply Chain Management 10.0.10 (mai 2020)
description: See artikkel kirjeldab funktsioone, mis on uued või muutunud Dynamics 365 Supply Chain Management 10.0.10-
author: kamaybac
ms.date: 04/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-21
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: c377a910cca8bbf1fd640b6c9a99810be1a8d40f
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708690"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10010-may-2020"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Supply Chain Management 10.0.10 (mai 2020)

[!include [banner](../includes/banner.md)]

See artikkel loetleb funktsioonid, mis on kas uued või muudetud rakenduses Microsoft Dynamics 365 Supply Chain Management 10.0.10. Selle versiooni number on 10.0.420 ja see on saadaval järgmiselt:

- **Eelvaateversiooni välja andmine:** märts 2020
- **Üldine saadavus (enesevärskendus):** aprill 2020
- **Automaatvärskendus:** mai 2020

## <a name="features-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

See väljalase hõlmab järgmisi funktsioone. Funktsioonide pealkirjad on lingitud saidiga [Väljalaske plaanid](/dynamics365/release-plans/) lisateabe andmiseks. Täiendavad lingid viitavad täiendavatele dokumentidele või videotele, mis on selle funktsiooni jaoks praegu saadaval. Suurem osa neist funktsioonidest tuleb enne kasutamist [Funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) abil lubada.

- [Täiustatud on olemasolevaid tegeliku kaalu silte laohaldusega](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/enhancement-use-existing-catch-weight-tags-warehouse-management)

- [Sissetuleva koormuse halduse täiustused laohalduse jaoks](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/warehouse-management-inbound-load-management-enhancement)<br> - Lisateabe saamiseks vt [Ostutellimuste sissetulevate koormate laohaldus](../warehousing/inbound-load-handling.md).

- [Laohalduse sildi printimise täiustused](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/label-printing-enhancements-warehouse-management)<br> – lisateabe saamiseks vt dokumendi protsessi [sildi paigutust](../warehousing/document-routing-layout-for-license-plates.md).

- [Koondplaneerimine hõlmab kaupu, millel on vaba kaubavaru, kui eeltöötlusfiltrid on lubatud](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/master-planning-include-items-on-hand-when-pre-processing-filters-are-enabled)

- [Tootmisala uued andmeüksused](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/new-data-entities-manufacturing-area)

- [Kvaliteedijuhtimine laoprotsesside jaoks](/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/quality-management-warehouse-processes)<br> - Lisateabe saamiseks vt [Kvaliteedijuhtimine laoprotsesside jaoks](../inventory/quality-management-for-warehouses-processes.md).

## <a name="additional-resources"></a>Lisaressursid

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platvormi värskendused finantside ja toimingute rakenduste jaoks

Dynamics 365 Supply Chain Management 10.0.10 sisaldab platvormivärskendusi. Lisateavet vt platvormi värskendustest [versioonile 10.0.10 finantside ja toimingute rakendustest](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34.md).

### <a name="bug-fixes"></a>Veaparandused

Lisateabe saamiseks veaparanduste kohta, mis sisalduvad selles värskenduses, logige sisse teenusesse Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=424137&dbType=3&qc=bf63d49dcc96e51eb42ac1dd66c6c5e5d7548f1e176f729e324ea3353b9860cb).

### <a name="dynamics-365-2020-release-wave-1-plan"></a>Dynamics 365 2020. aasta väljalaske 1. voo plaan

Kas teile pakuvad huvi meie ärirakenduste või platvormi uued ja hiljuti väljaantud võimalused?

Vaadake teemat [Dynamics 365: 2020. aasta väljalaske 1. voo plaan](/dynamics365-release-plan/2020wave1/index). Käsitleme ühes dokumendis kõiki üksikasju otsast lõpuni ja ülevalt alla, millest võite plaanide tegemisel lähtuda.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Eemaldatud ja aegunud Supply Chain Managementi funktsioonid

Artikli [eemaldatud või taunitud Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) funktsioonid kirjeldavad funktsioone, mis on tarneahela halduses eemaldatud või plaaniliselt eemaldatud või taunitud.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

Enne mis tahes funktsiooni eemaldamist tootest teatatakse amortiseerumisest [Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) artikli 12 kuu jooksul enne eemaldamist eemaldatud või taunitud funktsioonides.

Murranguliste muudatuste puhul, mis mõjutavad ainult kompileerimise aega, kuid on binaarselt ühilduvad liivakasti- ja tootmiskeskkondadega, on aegumise aeg vähem kui 12 kuud. Need on tavaliselt funktsionaalsed uuendused, mida tuleb teha kompilaatori jaoks.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
