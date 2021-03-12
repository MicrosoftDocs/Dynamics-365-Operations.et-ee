---
title: Puhkuste ja puudumiste parameetrite konfigureerimine
description: Määratlege rakenduses Dynamics 365 Human Resources puhkuste ja puudumiste inimressursside parameetrid.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e1b2de94f9d9ac1ada16b6ef0e7628edbc9d683f
ms.sourcegitcommit: d02fae79d5c02a4bc4f4b16a410c2f5ce026c204
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2021
ms.locfileid: "4997097"
---
# <a name="configure-leave-and-absence-parameters"></a>Puhkuste ja puudumiste parameetrite konfigureerimine

Enne puhkuste ja puudumiste plaanide seadistamist rakenduses Dynamics 365 Human Resources on hea mõte kontrollida kõigi seostuvate inimressursside parameetrite sätteid, sealhulgas järgnev.

- Puhkusetaotluste numbriseeria
- Perekonna meditsiinialase ja puhkuseseaduse (FMLA) sätted
- Töövõtja iseteeninduse sätted puhkuste ja puudumiste taotluste jaoks
- Puhkuste ja puudumiste parameetrid

## <a name="view-and-change-human-resources-parameters"></a>Inimressursside parameetrite kuvamine ja muutmine

1. Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.

2. Jaotises **Seadistus** valige suvand **Inimressursside parameetrid**.

3. Vahekaardil **Numbriseeriad** kontrollige suvandit **Numbriseeria kood** suvandi **Puhkusetaotluse ID** jaoks ja muutke vastavalt vajadusele. See säte määrab järjestuse, mida kasutatakse puhkusetaotlustele automaatselt ID-de määramiseks.

4. Vahekaardil **FMLA** kontrollige FMLA sätteid ja muutke vastavalt vajadusele.

5. Määrake vahekaardil **Töövõtja iseteenindus**, kas haldurid saavad oma töötajate nimel sisestada puhkuste ja puudumiste taotlusi.

7. Valige käsk **Salvesta**.

>[!IMPORTANT]
>Puhkuste ja puudumiste kuvamine ettevõtete lõikes on praegu eelversioonis. Peate selle lubama keskkonnas **Liivakast**, et kuvada puhkuse ja puudumise suvand. Lisateavet eelvaatefunktsioonide lubamise kohta vt [Funktsioonide haldus](hr-admin-manage-features.md).

## <a name="view-and-change-human-resources-shared-parameters"></a>Human Resourcesi ühiskasutuses parameetrite kuvamine ja muutmine

1. Lehel **Personalihaldus** valige vahekaart **Lingid**.

2. Jaotises **Häälestus** valige suvand **Human Resourcesi ühiskasutuses parameetrid**.

3. Valige vahekaardil **Eeljuurdepääs** suvandi **Luba ettevõtteülene puhkuste vaade** jaoks väärtus **Jah**, et lubada puhkuste kuvamine kogu ettevõttes.

4. Valige käsk **Salvesta**.

## <a name="view-and-change-leave-and-absence-parameters"></a>Puhkuste ja puudumiste kalendri parameetrite kuvamine ja muutmine

1. Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.

2. Jaotises **Seadistus** valige suvand **Puhkuste ja puudumiste parameetrid**.

3. Vahekaardil **Üldine** määrake järgmised parameetrid.
 
    - Määrake **Puhkuste ja puudumiste ühikuks** kas tunnid või päevad. Päevade määramisel saate teha valiku **Luba pooliku päeva määratlus**, et lubada töötajatel puhkusetaotlustes valida kas päeva esimene või teine pool. 

    - Valige **Töötatud kuude kehtivusaeg**, et määrata, millal viitvõlgade määrad puhkuseplaanide korral jõustuvad, kasutades töötatud kuude arvu.

    - Saldode kuvamiseks alates tänasest või viitvõlaperioodi algusest valige **Saldo arvutamine**. Kui valite **Saldo alates tänasest**, kuvatakse saldos kõigi viitvõlgade, korrigeerimiste ja taotluste kogusumma alates tänasest. Kui valite **Saldo alates viitvõlaperioodist**, kuvatakse saldos kõigi viitvõlgade, korrigeerimiste ja taotluste kogusumma alates puhkuseplaani sagedusega määratletud viitvõlaperioodist. 

    - Saate seadistada pakett-töö edasikandmise aegumise algusaja.  
    
    - Valige **Jah** suvanditele **Luba töötajatele puhkuse ostmine** ja **Luba töötajatele puhkuse müümine**. Kui valite nende suvandite jaoks **Jah**, saate luua puhkuse ostu- ja müügipoliitikad ja võimaldada töövõtjatel esitada puhkuse ostu-ja müügitaotlusi.

## <a name="configure-calendar-parameters"></a>Kõnekeskuse parameetrite konfigureerimine

1. Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.

2. Jaotises **Seadistus** valige suvand **Puhkuste ja puudumiste parameetrid**.

3. Vahekaardil **Kalender** muutke kalendri sätteid vastavalt vajadusele.

4. Valige käsk **Salvesta**.

## <a name="see-also"></a>Vt ka

- [Puhkuste ja puudumiste ülevaade](hr-leave-and-absence-overview.md)
