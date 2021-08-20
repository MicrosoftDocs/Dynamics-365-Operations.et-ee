---
title: Maksuarvutus (eelversioon)
description: Selles teemas selgitatakse maksuarvestuse võimekuse üldist ulatust ja funktsioone.
author: wangchen
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4e01247cddad4201760fd56e00e05a8373a1ca6ef7c26ae5e1f5cca63bd8a456
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775090"
---
# <a name="tax-calculation-preview"></a>Maksuarvutus (eelversioon)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Maksuarvestus on hüperskaleeritav mitmetasandiline teenus, mis võimaldab global tax engine maksu määramise ja arvutamise protsessi automatiseerida ja seda lihtsustada. Maksumootor on täielikult konfigureeritav. Elemendid, mida saab konfigureerida, sisaldavad, kuid ei ole piiratud maksustatavate andmemudelite, maksukoodide, maksu kohaldatavusmaatriksi ja maksuarvutuse valemiga. Maksumootor töötab teenuste Microsoft Azure põhiplatvormil ja pakub tänapäevasttehnoloogiat ja kõrgetasemelist skaleeritavust.

Maksuarvutus integreerub Dynamics 365 Finance ja Dynamics 365 Supply Chain Management-iga. Lõpuks integreerub see ka Dynamics 365 Project Operations Dynamics 365 Commerce ja teiste esimese ja kolmanda osapoole rakendustega.

> [!IMPORTANT]
> Kui lubate maksuarvestuse teenuse, võidakse teha mõningaid seotud andmete toiminguid andmekeskuses, mis ei ole andmekeskus, mis haldab teie teenuse andmeid. Vaadake [Maksuarvutuse tingimused](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) üle enne teenuse lubamist. Teie privaatsus on meie jaoks oluline. Lisateabe saamiseks lugege meie [privaatsusavaldust](https://go.microsoft.com/fwlink/?LinkId=521839).

Maksuarvestuse on mikroteenuse põhine maksumootor, mis pakub astmelisi skaleeritavust. Saate teha järgmisi toiminguid:

- Konfigureerige maksuarvestus Regulatory Configuration Service'i (RCS) kaudu. RCS on elektroonilise aruandluse (ER) kujundaja täiustatud versioon ja saadaval eraldi teenusena.
- Konfigureerige maksumaatriks maksukoodide ja -määrade automaatseks määramiseks.
- Konfigureerige maksumaatriks maksu registreerimise number automaatseks määramiseks.
- Konfigureerige maksuarvutuse kujundajat valemite ja tingimuste määratlemiseks.
- Jagage maksu määramist ja arvutuslahendust juriidiliste isikute lõikes.

Maksuarvutusteenuse kasutamiseks installige maksuarvutuse teenuse lisandmoodul oma projektist Microsoft Dynamics Lifecycle Services (LCS). Seejärel lõpetage seadistus RCS-s ja lubage maksu arvutamise teenus finantside ja Supply Chain Management. Lisateavet leiate teemast [Maksuteenusega alustamine](./global-get-started-with-tax-calculation-service.md).

## <a name="availability"></a>Kättesaadavus

Maksuarvutus on avaliku eelvaateprogrammi kaudu saadaval ainult liivakasti keskkondades ja valitud klientide jaoks. Lõpuks muutub see üldiselt kättesaadavaks kõigile klientidele ja tootmiskeskkondades.

Uusi funktsioone edastatakse, mistõttu kontrollige kindlasti kõige ajasemat dokumentatsiooni, et teada saada toetatud funktsioonide laovarudest ja ulatusest.

Maksuarvestus on juurutatud järgmistes Azure'i geograafilistes asukohtades. See juurutatakse ka rohkematele Azure'i geograafilistele aseukohtades, sõltuvalt klientide vajadustest:

- Ameerika Ühendriigid
- Euroopa

> [!NOTE]
> Maksuarvestus ei toeta kohapealset juurutamist Dynamics 365-s. Samuti ei toeta see varasemaid versioone, nt Dynamics AX 2012.

## <a name="feature-highlights"></a>Esiletõstetud funktsioonid

- Konfigureerige maksumaatriks maksude automaatseks määramiseks ja arvutamiseks
- Tugi mitme maksu registreerimisnumbritele
- Üleviimistellimuse tugi maksu määramiseks ja arvutamiseks
- Üleviimistellimuse tugi mitme maksu registreerimisnumbri määramiseks

## <a name="supported-transactions"></a>Toetatud kanded

Maksuarvestus võib olla juriidiliste isikute ja kannete puhul võimaldatud. Toetatud on järgmised kanded:

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

[Maksuteenusega alustamine](./global-get-started-with-tax-calculation-service.md)

[Mitu käibemaksukohustuslase numbrit](./emea-multiple-vat-registration-numbers.md)

[Maksufunktsiooni tugi üleviimistellimuse jaoks](./tasks/tax-feature-support-for-transfer-order.md)

[Kuidas koostada maksuteenuste laiendit](./tax-service-add-data-fields-tax-integration-by-extension.md)
