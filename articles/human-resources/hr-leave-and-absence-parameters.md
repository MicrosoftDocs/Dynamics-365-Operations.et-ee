---
title: Puhkuste ja puudumiste parameetrite konfigureerimine
description: Määratlege rakenduses Dynamics 365 Human Resources puhkuste ja puudumiste inimressursside parameetrid.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eb992cbfbed33f88e125d3a8b721f8815414599a
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3197977"
---
# <a name="configure-leave-and-absence-parameters"></a>Puhkuste ja puudumiste parameetrite konfigureerimine

Enne puhkuste ja puudumiste plaanide seadistamist rakenduses Dynamics 365 Human Resources on hea mõte kontrollida kõigi seostuvate inimressursside parameetrite sätteid, sealhulgas järgnev.

- Puhkusetaotluste numbriseeria
- Perekonna meditsiinialase ja puhkuseseaduse (FMLA) sätted
- Töövõtja iseteeninduse sätted puhkuste ja puudumiste taotluste jaoks
- Puhkuste ja puudumiste parameetrid

## <a name="view-and-change-human-resources-parameters"></a>Inimressursside parameetrite kuvamine ja muutmine

1. Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.

2. Jaotises **Seadistus** valige suvand**Inimressursside parameetrid**.

3. Vahekaardil **Numbriseeriad** kontrollige suvandit **Numbriseeria kood** suvandi **Puhkusetaotluse ID** jaoks ja muutke vastavalt vajadusele. See säte määrab järjestuse, mida kasutatakse puhkusetaotlustele automaatselt ID-de määramiseks.

4. Vahekaardil **FMLA** kontrollige FMLA sätteid ja muutke vastavalt vajadusele.

5. Määrake vahekaardil **Töövõtja iseteenindus**, kas haldurid saavad oma töötajate nimel sisestada puhkuste ja puudumiste taotlusi.

6. Vahekaardil **Puhkused ja puudumised** kontrollige sätteid ja muutke vastavalt vajadusele.

7. Valige käsk **Salvesta**.

## <a name="view-and-change-leave-and-absence-parameters"></a>Puhkuste ja puudumiste kalendri parameetrite kuvamine ja muutmine

1. Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.

2. Jaotises **Seadistus** valige suvand **Puhkuste ja puudumiste parameetrid**.

3. Vahekaardil **Üldine** määrake järgmised parameetrid.
 
    - Määrake **Puhkuste ja puudumiste ühikuks** kas tunnid või päevad. Päevade määramisel saate teha valiku **Luba pooliku päeva määratlus**, et lubada töötajatel puhkusetaotlustes valida kas päeva esimene või teine pool. 

    - Valige **Töötatud kuude kehtivusaeg**, et määrata, millal viitvõlgade määrad puhkuseplaanide korral jõustuvad, kasutades töötatud kuude arvu.

    - Saldode kuvamiseks alates tänasest või viitvõlaperioodi algusest valige **Saldo arvutamine**. Kui valite **Saldo alates tänasest**, kuvatakse saldos kõigi viitvõlgade, korrigeerimiste ja taotluste kogusumma alates tänasest. Kui valite **Saldo alates viitvõlaperioodist**, kuvatakse saldos kõigi viitvõlgade, korrigeerimiste ja taotluste kogusumma alates puhkuseplaani sagedusega määratletud viitvõlaperioodist. 

## <a name="configure-calendar-parameters"></a>Kõnekeskuse parameetrite konfigureerimine

1. Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.

2. Jaotises **Seadistus** valige suvand **Puhkuste ja puudumiste parameetrid**.

3. Vahekaardil **Kalender** muutke kalendri sätteid vastavalt vajadusele.

4. Valige käsk **Salvesta**.

## <a name="see-also"></a>Vt ka

- [Puhkuste ja puudumiste ülevaade](hr-leave-and-absence-overview.md)
