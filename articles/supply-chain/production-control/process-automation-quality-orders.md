---
title: Protsessi automatiseerimisvoogude kutsumine kvaliteettellimuste loomiseks
description: See artikkel annab ressursse äriprotsesside Power Automate automatiseerimiseks, kasutades kvaliteettellimuste näidet.
author: johanhoffmann
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a9c1cb7664963e60dcf6e50c7367f33382373832
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890708"
---
# <a name="invoke-process-automation-flows-to-create-quality-orders"></a>Protsessi automatiseerimisvoogude kutsumine kvaliteettellimuste loomiseks

[!include [banner](../includes/banner.md)]

Organisatsioonidel on järjest suurem nõudlus standardsete äriprotsesside automatiseerimiseks, mugavamaks suhtluse pakkumiseks personaliga ja erinevate andmeimpulsside ja -süsteemide kasutamine äriprotsesside automaatseks käivitamiseks. Automaatse protsessi automatiseerimise (RPA) puhul saavad ettevõtted kasutada koodita kogemust, et automatiseerida korduvad protsessid, mis koguvad nii efektiivsust Microsoft Power Automate ja täpsust.

Allalaaditava automatiseerimise lahenduse mall Supply Chain Management näitab, kuidas saab kasutada äriprotsesside automatiseerimiseks, kasutades Power Automate näitena kvaliteettellimusi.

Saate automatiseerimislahenduse malli alla laadida [siin](https://aka.ms/D365SCMQualityOrderRPASolution).

Selle funktsiooni ja selle võimalustest ülevaate saamiseks vaadake järgmist videot: [kasutage kvaliteettellimuste loomiseks RPA-d rakenduses Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)

![Automatiseerimisvalikud RPA-ga.](media/rpa-automation-options.png "Automatiseerimisvalikud RPA-ga")

Lahenduse Power Automate mall hõlmab pilve automatiseerimisvoogu ja töölaua automatiseerimisvoogu, mis automatiseerib kvaliteettellimuste loomise Supply Chain Management.

Automatiseerimist saab käivitada reageerida paljudele sündmustele ja signaalidele, k.a kasutajasisend või masina signaalid (k.a IoT-internet). *Q-tellimus* Power Application näidises sisaldub lahendusrakenduse näide. See võimaldab kasutajal skannida kauba QR-koodi, sisestada kogust ja lisada pilte kaameraga.

Lahenduse parameetrid kaasatakse automatiseerimise konfigureerimiseks tootmisteenuses konkreetse kasutusjuhtumi jaoks.

![Loo kvaliteettellimus.](media/rpa-create-quality-roder.png "Loo kvaliteettellimus")

Täielikku etapit-sammulise juhendit selle kohta, kuidas kvaliteettellimuse loomise automaatseks automatiseerimiseks näidislahendust alla laadida, installida ja kasutada, vt [Automate kvaliteettellimuse loomine Dynamics 365 Supply Chain Management Desktop koos rakendusega Robotic Process Automation kasutades Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).

