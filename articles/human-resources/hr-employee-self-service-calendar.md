---
title: Töörühma kalendri loomine
description: Vaadake ja looge töörühma kalendreid rakenduses Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cedff4031c6455b446af9c56a770a00f3b2efc80
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052093"
---
# <a name="view-team-and-company-calendars"></a>Meeskonna ja ettevõtte kalendrite kuvamine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Rakenduses Dynamics 365 Human Resources saate vaadata töörühma ja ettevõtte kalendreid. Töörühma kalendrites kuvatakse ainult otsesed aruanded, nagu on rea hierarhias määratletud.

## <a name="view-your-team-calendar-as-an-employee"></a>Meeskonna kalendri kuvamine töövõtjana

1. Valige tööruumis **Töövõtja iseteenindus** suvand **Meeskonna puudumiste kalender**, mis asub jaotises **Kokkuvõte**.

## <a name="view-your-team-calendar-as-a-manager"></a>Meeskonna kalendri kuvamine haldurina

1. Tööruumis **Töövõtja iseteenindus** valige suvand **Minu töörühm**.

2. Valige suvand **Puhkused ja puudumine** ning seejärel valige **Kuva halduri puudumiste kalender**.

Haldurid pääsevad juurde ka meeskonna kalendri jaotistele **Minu meeskonna ootel olevad vaba aja taotlused**, **Kinnitatud eemaloleku aeg** ja **Eemaloleku taotlused**. 

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

Kalendri konfiguratsioon väljal Puhkuste ja puudumiste parameetrid määrab saadaolevad vaate suvandid.

Kalendreid saate filtreerida ka halduri või osakonna alusel. Esmase ametikoha määramisega määratletakse töötajad, kes kuvatakse nende filtrite seadistamisel. 

>[!IMPORTANT]
>Puhkuste ja puudumiste kuvamine ettevõtete lõikes on praegu eelversioonis. Peate selle lubama keskkonnas **Liivakast**. Lisateavet eelvaatefunktsioonide lubamise kohta vt [Funktsioonide haldus](hr-admin-manage-features.md).<br><br>
>Seejärel peate lubama funktsiooni **Human Resourcesi ühiskasutuses parameetrid**, et kuvada juriidilise isiku filter kalendrites. Lisateabe saamiseks vt jaotist [Puhkuse ja puudumise parameetrite konfigureerimine](hr-leave-and-absence-parameters.md).<br><br>
>Kalendri saate filtreerida juriidilise isiku alusel. Kui soovite näha kõiki töövõtjaid sõltumata juriidilisest isikust, tühjendage filtriväli ja valige sisestusklahv. 

Lisateavet kalendri sätete kohta vt teemast [Kalendri parameetrite konfigureerimine](hr-leave-and-absence-parameters.md?configure-calendar-parameters).



[!INCLUDE[footer-include](../includes/footer-banner.md)]