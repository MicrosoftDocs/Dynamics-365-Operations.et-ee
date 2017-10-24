---
title: "Kuluobjekti kontrollijate pääsuõiguste määratlemine"
description: "See teema käsitleb kuluobjekti kontrollijate pääsuõigusi."
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: YuyuScheller
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 44ef687dcc5c7f515494894b3784bf5eceb99eed
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="access-rights-of-a-cost-object-controller"></a>Kuluobjekti kontrollija pääsuõigused

[!include[banner](../includes/banner.md)]

Tööruum **Kulude juhtimine** on keskne punkt, kus juhid saavad oma kuluobjektide toimivust vaadata. See tööruum laseb juhtidel tarbida kuluarvestuse andmeid, isegi kui nad ei ole kuluarvestajad. Turvalisuse huvides peaks juhtidel olema lubatud näha ainult neid kuluarvestuse andmeid, mis on seotud konkreetsete kuluobjektidega, mille eest nad vastutavad.

Kuluarvestuses on neli kordumatut rolli.

| Rolli nimi               | Litsents      |
|-------------------------|--------------|
| Kuluarvestuse haldur | Tegevus     |
| Kuluarvestaja         | Operations   |
| Kuluarvestuse ametnik   | Operations   |
| Kuluobjekti kontroller  | Töörühma liikmed |

Selles teemas selgitatakse, kuidas määrata juhile **kuluobjekti kontrollija** rolli.

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

|                                   | Kasutajad            | Dimensiooniliikmete vahemikud   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| **Sõlmed**                         | **Kasutaja ID**      | **Lähtedimensiooni liige** | **Sihtdimensiooni liige** |
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

- Microsoft Power BI:

    - Power BI visualisatsioonidel kuvatavad andmed
    - Andmete Power BI visualisatsioonid, mis on manustatud rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, klienti

> [!IMPORTANT]
> - Enne kui juurdepääsuloendi hierarhia saab Power BI-s olevaid andmeid mõjutada, tuleb juurdepääsuloendi hierarhia ja rea tasemel turve Power BI-s siduda. Lisateavet leiate teemast [Kuluarvestuse sisupaketi jaoks turbe seadistamine](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - Selles teemas näidatakse eeltingimusi, mis peavad olema täidetud enne **kulude juhtimise** tööruumi kasutamist.

Vt ka

- [Kulujuhtimise tööruum](cost-control-workspace.md)
- [Dimensioonihierarhia](dimension-hierarchy.md)
- [Kuluarvestuse sisupaketi turbe seadistamine](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)

