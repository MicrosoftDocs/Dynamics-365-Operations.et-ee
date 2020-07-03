---
title: Ülevaade
description: Rakenduse Dynamics 365 Human Resources tööruum Puhkused ja puudumised pakub paindlikku raamistikku uute puhkuseplaanide ja taotluste haldamise töövoogude loomiseks ning töötajate intuitiivset iseteeninduse lehte vabade päevade taotlemiseks.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
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
ms.openlocfilehash: ec72d2d741f7f8428a7daa97bb982e9fc00b8c3f
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428963"
---
# <a name="overview"></a>Ülevaade

Dynamics 365 Human Resources aitab teil pakkuda oma töötajatele suurepäraseid puhkusesoodustusi. Tööruum **Puhkused ja puudumised** pakub paindlikku raamistikku uute puhkuseplaanide ja taotluste haldamise töövoogude loomiseks ning töötajate intuitiivset iseteeninduse lehte vabade päevade taotlemiseks. Analüüs aitab teie organisatsioonil mõõta ja jälgida puhkuseplaanide saldosid ja kasutust.

## <a name="set-up-leave-and-absence"></a>Puhkuste ja puudumiste seadistamine

Enne oma töötajate jaoks puhkuseplaanide loomist peate läbima paar seadistuse etappi.

- [Puhkuste ja puudumiste parameetrite konfigureerimine](hr-leave-and-absence-parameters.md)
- [Tööajakalendri loomine](hr-leave-and-absence-working-time-calendar.md)
- [Puhkusetaotluse töövoo loomine](hr-leave-and-absence-workflow.md)

## <a name="create-and-manage-leave-plans"></a>Puhkuseplaanide loomine ja haldamine

Enne töötajale puhkuseplaanide loomist peate looma puhkuste ja puudumiste tüübid. Pärast puhkuseplaani loomist saate töötajaid plaanis registreerida. Saate käivitada ka koondamisprotsessi, luua teatisi ja vaadata oma plaanide analüüsi.

- [Puhkuste ja puudumiste tüüpide konfigureerimine](hr-leave-and-absence-types.md)
- [Puhkuse ja puudumise plaani loomine](hr-leave-and-absence-plans.md)
- [Töötajate puhkuste plaani määramine](hr-leave-and-absence-enroll.md)
- [Puhkuse ja puudumise plaanide koondamine](hr-leave-and-absence-accrue.md)
- [Puhkuste ja puudumiste analüüsi vaatamine](hr-leave-and-absence-analytics.md)

## <a name="request-time-off-and-manage-requests"></a>Eemaloleku aja taotlemine ja taotluste haldamine

Teie töövõtjad võivad esitada eemaloleku aja taotlusi ja saate neid hallata tööruumis **Töövõtja iseteeninduskeskus**.

- [Taotle vaba aega](hr-employee-self-service-request-time-off.md)
- [Puhkuste ja puudumiste taotluste haldamine](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-known-issues"></a>Puhkuste ja puudumiste teadaolevad probleemid

### <a name="rounding-precision"></a>Ümardamistäpsus

Suvandit **Ümardamistäpsus** ei saa määrata, kui määrate suvandi **Ümardamine tüüp**. Suvandi **Ümardamistäpsust** saate määrata ainult üksuse **Puhkuse ja puudumise tüüp** abil. 

1. Valige jaotises **Puhkuse ja puudumise tüübid** suvand **Ava Excelis** üksuse **Puhkuse ja puudumise tüüp** avamiseks.

2. Kui fail avaneb ja on lubatud, valige **Kujundus**.

3. Tabelis **Puhkuse ja puudumise tüüp** valige redigeerimiseks pliiatsi suvand.

4. Valige **RoundingPrecision** ja **RoundingType** ning seejärel valige **Lisa** nende lisamiseks väljade loendisse.

5. Valige suvand **Värskenda** ja seejärel nupp **Valmis**.

6. Sisestage või valige igale puhkuse tüübile **Ümardamistüüp**, kui neid pole juba määratud. 

7. Sisestage õigetele tüüpidele **Ümardamistäpsus**.

8. Muudatuste sisestamiseks Human Resourcesisse valige **Avalda**.

## <a name="leave-and-absence-preview-features"></a>Puhkuste ja puudumiste eelvaatefunktsioonid

Saate proovida uusi puhkuste ja puudumiste eelvaatefunktsioone keskkonnas **Liivakast**. Lisateavet eelvaatefunktsioonide sisselülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md). 

[!include [banner](includes/preview-feature.md)]

Eelvaatefunktsioonid hõlmavad järgmist.

- **Puhkuse juurdekasv ettevõtte- või puhkuseplaani alusel** – saate käivitada juurdekasvu protsessi kõikide ettevõtete või ühe ettevõtte jaoks. Samuti saate käivitada juurdekasvu protsessi konkreetse ettevõtte konkreetse puhkuse või puudumiste plaani jaoks. 

- **Puhkuse ost** – saate lubada ja luua töötajate jaoks puhkuse ostu põhimõtted ostutaotluste esitamiseks. Töötajad saavad esitada ostutaotlusi ning nende saldot uuendatakse taotluse kajastamiseks automaatselt.  

- **Kinnitatud puhkusetaotlustele manuste lisamine** – saate lisada manuse puhkusetaotlusele, mis on juba kinnitatud. 

