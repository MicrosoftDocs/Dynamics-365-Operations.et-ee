---
title: Kuluobjekti kontrollerite pääsuõigused
description: See artikkel annab teavet kuluobjekti kontrollerite juurdepääsuõiguste kohta.
author: AndersGirke
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c40be758c5e5d1d1fb025630ed8321ae46251892
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903185"
---
# <a name="access-rights-for-cost-object-controllers"></a>Kuluobjekti kontrollerite pääsuõigused

[!include [banner](../includes/banner.md)]

Tööruum **Kulude juhtimine** on keskne punkt, kus juhid saavad oma kuluobjektide toimivust vaadata. See tööruum laseb juhtidel tarbida kuluarvestuse andmeid, isegi kui nad ei ole kuluarvestajad. Turvalisuse huvides peaks juhtidel olema lubatud näha ainult neid kuluarvestuse andmeid, mis on seotud konkreetsete kuluobjektidega, mille eest nad vastutavad.

Kuluarvestuses on neli kordumatut rolli.

| Rolli nimi               | Litsents      |
|-------------------------|--------------|
| Kuluarvestuse haldur | Tegevus     |
| Kuluarvestaja         | Operations   |
| Kuluarvestuse ametnik   | Operations   |
| Kuluobjekti kontroller  | Töörühma liikmed |

See artikkel selgitab, kuidas määrata kuluobjekti **kontrolleri** roll haldurile.

Kui juhile on määratud **kuluobjekti kontrollija** roll, saab juht teha järgmisi toiminguid.

- Avage (kliendis) tööruum **Kulude juhtimine**.

    - Saate minna süvitsi ja teil on vaatamiseks juurdepääs lehtedele, mis toetavad süvitsimineku kogemust.

- Avage (mobiilirakenduses) tööruum **Kulude juhtimine**.

> [!NOTE]
> Roll **Kuluobjekti kontrollija** ei kontrolli seda, millistele kuluobjektidele on kasutajal juurdepääs ja milliste andmeid ta vaadata saab. Rea tasemel turvalisus tagatakse dimensioonihierarhiate ja juurdepääsuloendi hierarhia kaudu.

## <a name="grant-access-rights"></a>Pääsuõiguste andmine
Järgmine näide on selle kohta, milline dimensioonihierarhia välja võib näha.

**Dimensioonihierarhia üksikasjad**

| Dimensioonihierarhia nimi | Dimensioon    | Dimensiooni hierarhia tüübi nimi      | Juurdepääsuloendi hierarhia |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisatsioon             | Kulukeskused | Dimensiooni klassifitseerimishierarhia | **Jah**               |

Võite kasutada hierarhiakujundajas kiirkaarti **Kasutajad** vähemalt ühe kasutaja ID sisestamiseks igasse sõlme.

|             Sõlmpunktid                 | Kasutajad            | Dimensiooniliikmest     |   Dimensiooniliikmeni   |
|-----------------------------------|------------------|---------------------------|-------------------------|
| Organisatsioon                      | Benjamin, Claire |                           |                         |
| &nbsp;&nbsp;Administraator                 | aprill            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Finantsid   | Alicia           | CC002                     | CC003                   |
|                                   |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Personaliosakond        | Arnie            | CC001                     | CC001                   |
| &nbsp;&nbsp;Tootmine            | David            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Pakendamine | Ellen            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Assembler  | Chris            | CC006                     | CC006                   |

> [!NOTE]
> Kuluarvestajad tuleks määrata hierarhia ülemisele tasandile, et nad näeksid kuluarvestuses kõiki kirjeid.

Enne, kui juurdepääsuloendi hierarhiat ja selle turbesätteid rakendada saab, tuleb valiku **Luba kuvamise juurdepääs kuluobjekti dimensiooniliikmete jaoks** väärtuseks määrata **Jah** vahekaardil **Üldine** lehel **Kuluarvestuse parameetrid** (**Kuluarvestus** > **Seadistus** > **Parameetrid**).

Juurdepääsuloendi hierarhia sätteid kasutatakse järgmistel aladel kuvatavate andmete juhtimiseks.

- **Kulude juhtimise** tööruum (kliendis):

    - Süvitsiminekuks kasutatavatel lehtedel olevad andmed

- **Kulude juhtimise** tööruum (mobiilirakenduses):

    - Saldod kaartidel

- Rakendus Microsoft Power BI:

    - Power BI visualiseeringutel kuvatavad andmed
    - Dynamics Power BI 365 Finance kliendis manustatud andmete visualiseerimised

> [!IMPORTANT]
> - Enne kui juurdepääsuloendi hierarhia saab Power BI-s olevaid andmeid mõjutada, tuleb juurdepääsuloendi hierarhia ja rea tasemel turve Power BI-s siduda. Lisateavet leiate teemast [Kuluarvestuse sisupaketi jaoks turbe seadistamine](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - See artikkel näitab eeltingimusi, mis peavad enne kulujuhtimise tööruumi **kasutamist olema täidetud**.

Lisaressursid

- [Kulujuhtimise tööruum](cost-control-workspace.md)
- [Dimensioonihierarhia](dimension-hierarchy.md)
- [Kuluarvestuse sisupaketi turbe seadistamine](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
