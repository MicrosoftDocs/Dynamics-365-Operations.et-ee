---
title: Maksuarvutusteenus (Eelversioon)
description: Selles teemas selgitatakse maksuarvutusteenuse üldist ulatust ja funktsioone.
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818220"
---
# <a name="tax-calculation-service-preview"></a>Maksuarvutusteenus (Eelversioon)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Maksuarvestuse teenus on hyper-skaleeritav mitmetasandiline teenus, mis võimaldab global tax engine maksu määramise ja arvutamise protsessi automatiseerida ja seda lihtsustada. Maksumootor on täielikult konfigureeritav. Elemendid, mida saab konfigureerida, sisaldavad, kuid ei ole piiratud maksustatavate andmemudelite, maksukoodide, maksu kohaldatavusmaatriksi ja maksuarvutuse valemiga. Maksumootor töötab teenuste Microsoft Azure põhiplatvormil ja pakub tänapäevasttehnoloogiat ja kõrgetasemelist skaleeritavust.

Maksuarvutuse teenus integreerub Dynamics 365 Finance ja Dynamics 365 Supply Chain Management-iga. Lõpuks integreerub see ka Dynamics 365 Project Operations Dynamics 365 Commerce ja teiste esimese ja kolmanda osapoole rakendustega.

Maksuarvestuse teenus on Microsoftipõhine maksumootor, mis pakub astmelisi skaleeritavust. Saate teha järgmisi toiminguid:

- Konfigureerige maksu arvutamise teenus regulatiivse konfiguratsiooniteenuse (RCS) kaudu. RCS on elektroonilise aruandluse (ER) kujundaja täiustatud versioon ja saadaval eraldi teenusena.
- Konfigureerige maksumaatriks maksukoodide ja -määrade automaatseks määramiseks.
- Konfigureerige maksumaatriks maksu registreerimise number automaatseks määramiseks.
- Konfigureerige maksuarvutuse kujundajat valemite ja tingimuste määratlemiseks.
- Jagage maksu määramist ja arvutuslahendust juriidiliste isikute lõikes.

Maksuarvutusteenuse kasutamiseks installige maksuarvutuse teenuse lisandmoodul oma projektist Microsoft Dynamics Lifecycle Services (LCS). Seejärel lõpetage seadistus RCS-s ja lubage maksu arvutamise teenus finantside ja Supply Chain Management. Lisateavet leiate teemast [Maksuteenusega alustamine](https://go.microsoft.com/fwlink/?linkid=2138482).

## <a name="availability"></a>Kättesaadavus

Maksuarvutusteenus on avaliku eelvaateprogrammi kaudu saadaval ainult liivakasti keskkondades ja valitud klientide jaoks. Lõpuks muutub see üldiselt kättesaadavaks kõigile klientidele ja tootmiskeskkondades.

Uued funktsioonid tarnitakse ka edaspidi maksuarvestuse teenuses. Seetõttu kontrollige kindlasti kõige ajasemat dokumentatsiooni, et teada saada toetatud funktsioonide laovarudest ja ulatusest.

Maksu arvutamise teenus on juurutatud järgmistes Azure'i geograafilistes asukohtades. See juurutatakse ka rohkematele Azure'i geograafilistele aseukohtades, sõltuvalt klientide vajadustest:

- Ameerika Ühendriigid
- Euroopa
- Prantsusmaa
- Ühendkuningriik

> [!NOTE]
> Maksu arvutamise teenus ei toeta kohapealset juurutamist Dynamics 365-s. Samuti ei toeta see varasemaid versioone, nt Dynamics AX 2012.

## <a name="feature-highlights"></a>Esiletõstetud funktsioonid

- Konfigureerige maksumaatriks maksude automaatseks määramiseks ja arvutamiseks
- Tugi mitme käibemaksu(VAT) registreerimisnumbritele
- Üleviimistellimuse tugi maksu määramiseks ja arvutamiseks
- Üleviimistellimuse tugi mitme käibemaksu registreerimisnumbri määramiseks

## <a name="supported-transactions"></a>Toetatud kanded

Maksu arvutamise teenused võivad olla juriidiliste isikute ja kannete puhul võimaldatud. Toetatud on järgmised kanded:

- Müügiprotsess

    - Müügipakkumine
    - Müügitellimus
    - Kinnitus
    - Komplekteerimisleht
    - Saateleht
    - Müügiarve
    - Kreeditarve
    - Tagastustellimus
    - Mitmesugused tasude päis
    - Mitmesuguste kulude rida

- Ostuprotsess

    - Ostutellimus
    - Kinnitus
    - Saabunud kaupade loend
    - Toote sissetulek
    - Ostuarve
    - Mitmesugused tasude päis
    - Mitmesuguste kulude rida
    - Kreeditarve
    - Tagastustellimus
    - Ostutaotlus
    - Ostutaotluse rea lisakulud
    - Pakkumiskutse
    - Pakkumispäise lisakulunõue
    - Pakkumisrea lisakulunõue

- Inventuuriprotsess

    - Kandetellimus-- lähetus
    - Kandetellimus-- kättesaamine

## <a name="related-resources"></a>Seotud ressursid

[Maksuteenusega alustamine](https://go.microsoft.com/fwlink/?linkid=2138482)

[Mitu käibemaksukohustuslase numbrit](https://go.microsoft.com/fwlink/?linkid=2153387)

[Maksufunktsiooni tugi üleviimistellimuse jaoks](https://go.microsoft.com/fwlink/?linkid=2153388)

[Kuidas koostada maksuteenuste laiendit](https://go.microsoft.com/fwlink/?linkid=2138483)
