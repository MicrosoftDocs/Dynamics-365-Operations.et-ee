---
title: Teenusepõhise autentimise konfigureerimine
description: See teema kirjeldab, kuidas konfigureerida teenuse-teenuse autentimist, et kutsuda turvaliselt teenuse API-sid Microsoft Dynamics 365 Commerce hinnangutele ja hinnangutele.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: da780de5f15d72bdac85a261eae809125c830260
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968402"
---
# <a name="configure-service-to-service-authentication"></a>Teenusepõhise autentimise konfigureerimine

[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas konfigureerida teenuse-teenuse (S2S) autentimist, et turvaliselt kutsuda teenuse rakenduse Microsoft Dynamics 365 Commerce programmeerimisliidest (API-d) hinnangutele ja hinnangutele.

Dynamics 365 Commerce pakub [hinnanguid ja](ratings-reviews-overview.md) kommentaare kanali kanali lahendusena. See lahendus võimaldab juurdepääsu teenuse API-dele väljaspool Commerce'i, nii et saab teha erinevaid ülesandeid. Need ülesanded hõlmavad hinnangute ja ülevaadete importimist teie välissüsteemist Commerce'i ja hinnangute eksportimist Commerce'ist. Et lubada Äril turvaliselt helistada hinnangutele ja ülevaateid teenuse API-dele, peate esmalt konfigureerima S2S-i autentimise, täites selles teemas protseduurid.

## <a name="add-a-new-app-registration"></a>Lisa uus rakenduse registreerimine

Enne rakenduse uue registreerimise lisamist peate looma rakenduse Azure'i portaali [abil](https://portal.azure.com). Rakenduse registreerimiseks () ja autentimise lubamiseks järgige juhiseid jaotises Azure Active Directory Azure AD Kasuta kohandatud [Azure Active Directory konnektoriga rakenduses Power Automate](/connectors/custom-connectors/azure-active-directory-authentication).

Koguge Azure'i portaalist järgmisi ID-sid. Vajate neid ID-sid järgmistes sammudes.

- Klientrakenduse ID
- Kliendikausta (rentniku) ID

Rakenduse uue registreerimiseks Commerce'i saidi koostajas järgige neid samme.

1. Avage **Avaleht \> Arvustused \> Seaded**.
1. Valige **suvandi Teenuselt teenusele (S2S)** autentimiseks suvand **Manage** (Halda).

    ![Commerce'i saidilooja jaotises Teenuseteenuse (S2S) autentimise haldamine.](media/Ratings-reviews-settings-service-to-service-authentication.png)

1. Parempoolsel **S2S-rakenduse kirjete** paanil valige käsk Lisa uus **S2S-rakenduse** registreerimine.
1. Dialoogiboksis **Lisa S2S-rakenduse** kirje sisestage järgmine nõutav teave. Kasutage väärtusi oma Azure'i rakenduse registreerimisest.

    - **Nimi:** sisestage oma rakenduse nimi (nt **Fabrikam** App).
    - **Kliendi rakenduse ID** – sisestage rakenduse ID (nt). **00000000-0000-0000-0000-000000000000**
    - **Kataloogi (rentniku) ID** – sisestage kausta ID (nt **00000000-0000-0000-0000-000000000000**).

    ![Dialoogiboksi S2S-i rakenduse kirje lisamine Commerce'i saidi koostajas.](media/Ratings-reviews-settings-S2S-APP-entry.png)

1. Valige käsk **Esita**. Rakenduse nimi peaks ilmuma **S2S-rakenduse kirjete paani** loendis.
1. Sulgege **S2S-rakenduse kirjete** paan.
1. Valige käsk **Salvesta**.

## <a name="edit-an-existing-app-registration"></a>Olemasoleva rakenduse registreerimise redigeerimine

Olemasoleva rakenduse registreerimise redigeerimiseks Commerce'i saidi koostajas järgige neid samme.

1. Avage **Avaleht \> Arvustused \> Seaded**.
1. Valige **suvandi Teenuselt teenusele (S2S)** autentimiseks suvand **Manage** (Halda).
1. **Paanil S2S-rakenduse kirjed valige redigeeritav kirje kõrval sümbol** sümbol.
1. Värskendage väärtused **väljadel** Nimi, **Kliendi rakenduse ID ja Kataloogi** **(rentnik) ID vastavalt** vajadusele.
1. Valige käsk **Esita**.
1. Sulgege **S2S-rakenduse kirjete** paan.
1. Valige käsk **Salvesta**.

## <a name="remove-an-existing-app-registration"></a>Eemalda olemasolev rakenduse registreerimine

Commerce'i saidi koostajast olemasoleva rakenduse registreerimise eemaldamiseks järgige neid samme.

1. Avage **Avaleht \> Arvustused \> Seaded**.
1. Valige **suvandi Teenuselt teenusele (S2S)** autentimiseks suvand **Manage** (Halda).
1. **S2S-rakenduse** kirjetepaanil valige cancani sümbol kande kõrval, mille soovite eemaldada. Kirje eemaldatakse loendist.
1. Sulgege **S2S-rakenduse kirjete** paan.
1. Valige käsk **Salvesta**.

## <a name="additional-resources"></a>Lisaressursid

[Hinnangute ja arvustuste ülevaade](ratings-reviews-overview.md)

[Hinnangute ja arvustuste kasutamise valimine](opt-in-ratings-reviews.md)

[Hinnangute ja arvustuste haldus](manage-reviews.md)

[Hinnangute ja arvustuste konfigureerimine](configure-ratings-reviews.md)

[Toote hinnangute sünkroonimine](sync-product-ratings.md)

[Lubage hinnangute ja ülevaadete käsitsi avaldamine moderaatori poolt](manual-publish-rating-reviews.md)

[Hinnangute ja kommentaaride importimine ja eksportimine](import-export-reviews.md)

[Hinnangud ja arvustused KKK](ratings-reviews-faq.md) 
