---
title: Puhkuste ja puudumiste parameetrite konfigureerimine
description: See artikkel kirjeldab inimressursside parameetrite määratlemist puhkusel ja puudumiste puhul Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3a39c74eef3865c03ccb9dd5aa2fece7f25e639a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891375"
---
# <a name="configure-leave-and-absence-parameters"></a>Puhkuste ja puudumiste parameetrite konfigureerimine

>[!Important]
>Selles artiklis märgitud funktsioonid on klientide jaoks praegu saadaval eraldiseisev Dynamics 365 Human Resources. Osa või kõik funktsioonid on saadaval osana Finance'i taristu tulevasest väljalaskest pärast Finance'i versiooni 10.0.26.


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Enne puhkuse ja puudumiste plaanide Dynamics 365 Human Resources **seadistamist** on hea mõte kontrollida kõikide seotud inimressursside parameetrite sätteid, sealhulgas:

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

    - Määrake aegumise **edasikaatmise** pakett-töö **algusaeg**.  
    
    - Valige **Jah** suvanditele **Luba töötajatele puhkuse ostmine** ja **Luba töötajatele puhkuse müümine**. Kui valite nende suvandite jaoks **Jah**, saate luua puhkuse ostu- ja müügipoliitikad ja võimaldada töövõtjatel esitada puhkuse ostu-ja müügitaotlusi.

## <a name="configure-calendar-parameters"></a>Kõnekeskuse parameetrite konfigureerimine

1. Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.

2. Jaotises **Seadistus** valige suvand **Puhkuste ja puudumiste parameetrid**.

3. Vahekaardil **Kalender** muutke kalendri sätteid vastavalt vajadusele.

4. Valige käsk **Salvesta**.

## <a name="see-also"></a>Vt ka

- [Puhkuste ja puudumiste ülevaade](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
