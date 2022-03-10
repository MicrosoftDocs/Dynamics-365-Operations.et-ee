---
title: Töörühma kalendri loomine
description: Vaadake ja looge töörühma kalendreid rakenduses Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8ee39f35f9d81f47c5438ddf48451d24ab0c0ed3
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065248"
---
# <a name="view-team-and-company-calendars"></a>Meeskonna ja ettevõtte kalendrite kuvamine


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Rakenduses Dynamics 365 Human Resources saate vaadata töörühma ja ettevõtte kalendreid. Töörühma kalendrites kuvatakse ainult otsesed aruanded, nagu on rea hierarhias määratletud.

## <a name="view-your-team-calendar-as-an-employee"></a>Meeskonna kalendri kuvamine töövõtjana

- Valige tööruumis **Töövõtja iseteenindus** suvand **Meeskonna puudumiste kalender**, mis asub jaotises **Kokkuvõte**.

## <a name="view-your-team-calendar-as-a-manager"></a>Meeskonna kalendri kuvamine haldurina

1. Tööruumis **Töövõtja iseteenindus** valige suvand **Minu töörühm**.

2. Valige suvand **Puhkused ja puudumine** ning seejärel valige **Kuva halduri puudumiste kalender**.

Haldurid pääsevad juurde ka meeskonna kalendri jaotistele **Minu meeskonna ootel olevad vaba aja taotlused**, **Kinnitatud eemaloleku aeg** ja **Eemaloleku taotlused**. 

## <a name="view-your-absence-manager-calendar-as-the-absence-manager"></a>Puudumiste halduri kalendri kuvamine puudumiste haldajana

> [!NOTE]
> Puudumiste halduri kalendri vaatamiseks peate funktsiooni **(Eelvaade) Puudumiste haldur puhkuste haldamiseks** esmalt Funktsioonihalduses sisse lülitama. Lisateavet eelvaatefunktsioonide sisselülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

Puudumiste halduri rolli kasutajad saavad vaadata oma kalendris puhkuste taotlusi. Puhkusekalendrile juurdepääsemiseks järgige järgmisi samme.

1. Tööruumis **Töötaja iseteenindus** valige **Puudumiste haldur** ja seejärel **Puudumiste halduri kalender**.

2. Väljale **Kuupäev** sisestage soovitud kuupäevad.

3. Värskendage vaate valikuid vastavalt vajadusele.

Puudumiste halduri kalender näitab kõiki kirjeid töötajate kohta, kes on puhkuse hierarhias puudumiste haldurile sellest teada andnud.

## <a name="view-a-company-calendar"></a>Ettevõtte kalendri kuvamine

Personaliosakonna töötaja rollis olevad inimesed saavad vaadata ettevõtte kalendreid. Ettevõtte kalendrid kuvavad kõik töötajad. Vaikimisi kuvatakse kalendris tänane kuupäev pluss 28 päeva, kuid saate kuupäevavahemikku muuta. Saate kalendrit filtreerida ka suvandite **Nimi**, **Personalinumber** ja **Puhkuse tüüp** põhjal.

1. Töörühmas **Puhkused ja puudumised** valige suvand **Lingid**.

2. Valige suvand **Puhkuste ja puudumiste kalender**.

Rakenduse Human resources rollid pääsevad juurde ka meeskonna kalendri jaotistele **Puhkuse ja puudumise taotlused**, **Kinnitatud eemaloleku aeg** ja **Eemaloleku taotlused**. 

Kalendrid sisaldavad nüüd täiendavaid filtreid ja suvandeid. Kõik kalendrid hõlmavad vaate suvandeid järgmiste kohta.

- Kinnitatud taotlused
- Ootel taotlused
- Puhkusetaotlustega töötajad
- Puhkusetaotlusteta töötajad
- Töötajate sünnipäevad
- Vaba aja taotlused 
- Puhkusetaotlused

Kalendri konfiguratsioon väljal **Puhkuste ja puudumiste parameetrid** määrab saadaolevad vaate suvandid.

Kalendreid saate filtreerida ka halduri või osakonna alusel. Esmase ametikoha määramisega määratletakse töötajad, kes kuvatakse nende filtrite seadistamisel. 

> [!IMPORTANT]
> Funktsioonihalduses saate lülitada sisse funktsiooni **Ettevõtteülese puhkuse vaate**. Seejärel peate lubama funktsiooni lehel **Human Resourcesi ühiskasutuses parameetrid**, et kuvada juriidilise isiku filter kalendrites. Lisateabe saamiseks vt jaotist [Puhkuse ja puudumise parameetrite konfigureerimine](hr-leave-and-absence-parameters.md).
> 
> Kalendri saate filtreerida juriidilise isiku alusel. Kõigi töötajate vaatamiseks, olenemata juriidilisest isikust, tühjendage filtriväli ja valige **Sisesta**. 

Lisateavet kalendri sätete kohta vt teemast [Kalendri parameetrite konfigureerimine](hr-leave-and-absence-parameters.md?configure-calendar-parameters).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
