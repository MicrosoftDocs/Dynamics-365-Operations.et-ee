---
title: Koondplaanide ülevaade
description: Ettevõtte igapäevaste tööoperatsioonide toetamiseks, erinevate jälgimist vajavate planeerimisstrateegiate simuleerimiseks ja ettevõtte eeskirjade juurutamiseks (nt sisetegevuse puhul ja kliendi rahulolu saavutamiseks) saate kasutada erinevaid koondplaane.
author: t-benebo
ms.date: 05/28/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ReqParameters, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "7911"
- intro-internal
ms.assetid: a116b7de-3d6d-4321-87ba-5a5d99c2f64e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b3d30d9ef2f08c2cb7b2ca022ff1a816567a247
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468745"
---
# <a name="master-plans-overview"></a>Koondplaanide ülevaade

[!include [banner](../includes/banner.md)]

Ettevõtte igapäevaste tööoperatsioonide toetamiseks, erinevate jälgimist vajavate planeerimisstrateegiate simuleerimiseks ja ettevõtte eeskirjade juurutamiseks (nt sisetegevuse puhul ja kliendi rahulolu saavutamiseks) saate kasutada erinevaid koondplaane.

Koondplaane saate konfigureerida lehel **Koondplaanid**.

Plaane on kahesuguseid:

- **Staatiline plaan** – koondplaneerimise arvutamine kasutab netovajaduste plaani loomiseks praeguseid andmeid. Plaan püsib muutumatu järgmise koondplaneerimise käivitamiseni või plaani käsitsi muutmiseni. Seda plaani saavad kasutada ettevõtte erinevad töötajad, näiteks sisseostjad või tooteplaanijad, toetudes sellele oma otsuste langetamisel ja igapäevaste tegevuste teostamisel.
- **Dünaamiline plaan** – see plaan käivitub sama netovajaduste plaaniga, mis loodi koondplaneerimisega. Siiski saate dünaamilist plaani värskendada iga kord, kui koondandmed muutuvad. Selle põhjuseks võib olla näiteks uue müügitellimuse loomine. See võimaldab jälgida tellimusevõrgu muutusi ja kauba kättesaadavust, häirimata teiste tööks vajalikku staatilist plaani.

Ettevõttel on võimalus kasutada vaid dünaamilist plaani või staatilist ja dünaamilist plaani korraga. Iga koondplaani saab konfigureerida peegeldama konkreetset strateegiat või tegelema prooviga. Näited on järgmised.

- Kõrgemate kaubavarude tasemete seadistamine defitsiidi vastu kindlustamiseks.
- Pikemate ohutuspiiride seadistamine ebausaldusväärsete hankijate vastu kindlustamiseks.

Alustava dünaamilise plaani saate seadistada ka nii, et seda värskendatakse koos uute vajaduste plaaniga iga kord koondplaneerimise käivitamisel. Need sätted saate määrata lehel **Koondplaneerimise parameetrid**.

## <a name="additional-resources"></a>Lisaressursid

- [Laovarude sätted](coverage-settings.md)
- [Taktikalise ja operatiivse plaanimise eraldamine koondplaanimisel](https://community.dynamics.com/ax/b/dynamicsaxmanufacturingrdteamblog/posts/separating-tactical-and-operative-planning-for-master-scheduling)
- [Koondplaanimine: kas kasutada staatilist ja dünaamilist koondplaani või kasutada ühte plaani?](https://community.dynamics.com/ax/b/msdynaxlessonslearned/archive/2014/01/16/master-planning-use-a-static-and-dynamic-master-plan-or-use-one-plan)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
