---
title: Puhkuste ja puudumiste parameetrite konfigureerimine
description: Selles teemas kirjeldatakse, kuidas määratleda inimressursside parameetreid puhkuse ja puudumise jaoks Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7bd1aebd633af0530c550f8ec7510a0c09985ca1
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067348"
---
# <a name="configure-leave-and-absence-parameters"></a>Puhkuste ja puudumiste parameetrite konfigureerimine


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Enne puhkuse- ja puudumisplaanide seadistamist rakenduses Dynamics 365 Human Resources on hea kontrollida kõigi seotud **inimressursside parameetrite** sätteid, sealhulgas järgmist.

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

    - Määrake pakett-töö **Edasikandmise aegumisaja algusaeg** **·**.  
    
    - Valige **Jah** suvanditele **Luba töötajatele puhkuse ostmine** ja **Luba töötajatele puhkuse müümine**. Kui valite nende suvandite jaoks **Jah**, saate luua puhkuse ostu- ja müügipoliitikad ja võimaldada töövõtjatel esitada puhkuse ostu-ja müügitaotlusi.

## <a name="configure-calendar-parameters"></a>Kõnekeskuse parameetrite konfigureerimine

1. Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.

2. Jaotises **Seadistus** valige suvand **Puhkuste ja puudumiste parameetrid**.

3. Vahekaardil **Kalender** muutke kalendri sätteid vastavalt vajadusele.

4. Valige käsk **Salvesta**.

## <a name="see-also"></a>Vt ka

- [Puhkuste ja puudumiste ülevaade](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
