---
title: Hinnangute ja kommentaaride importimine ja eksportimine
description: See teema kirjeldab, kuidas importida ja eksportida toote hinnanguid ja ülevaateid moodulis Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 3ae85f21f7a78d56621aed60527207badcee9c75
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968405"
---
# <a name="import-and-export-ratings-and-reviews"></a>Hinnangute ja kommentaaride importimine ja eksportimine

[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas importida ja eksportida toote hinnanguid ja ülevaateid moodulis Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce pakub [hinnanguid ja](ratings-reviews-overview.md) kommentaare kanali kanali lahendusena. Kui lülitute üle hinnangutele ja vaatate üle lahenduse, võite soovida teisaldada oma olemasolevad hinnangud ja ülevaated andmete üle Dynamics 365 Commerce Äriplatvormile. Ärinõuete alusel võite soovida eksportida ka hinnanguid ja ülevaateid Commerce'ist. Power Automate Konnektor võimaldab teil importida hinnanguid ja ülevaateid Commerce'isse ja eksportida neid Commerce'ist.

> [!NOTE]
> Lisateavet selle kohta, kuidas loogikavoogudega Power Automate alustada, vt [teemast Pilve voo loomine Power Automate](/power-automate/get-started-logic-flow).

## <a name="prerequisites"></a>Eeltingimused

Enne hinnangute ja hinnangute importimist ja eksportimist peate täitma järgmised eeltingimused:

- Hinnangud ja ülevaatuslahendus peavad olema äriplatvormi e-posti saidi puhul lubatud. Lisateavet vt jaotisest [Nõustu hinnangute ja kommentaaride kasutamisega.](opt-in-ratings-reviews.md)
- Dynamics 365 hinnangud ja ülevaated Power App Connector peab olema konfigureeritud lubama toimingute "edasta ülevaated" või "ekspordi ülevaated" lubamiseks Power Automate rakenduses. Lisateavet vt : [Dynamics 365 Commerce hinnangud ja ülevaated](/connectors/dynamics365ratingsre/) (eelvaade).
- Teenuse-teenuse (S2S) autentimine peab olema konfigureeritud nii, et see kutsuks turvaliselt hinnangud ja vaataks üle rakenduse programmeerimisliidese (API) väljast Commerce. Lisateavet vt ["Teenuseteenuse autentimise konfigureerimine".](service-to-service-auth.md)

## <a name="import-ratings-and-reviews"></a>Hinnangute ja kommentaaride importimine

Hinnangute importimiseks ja läbivaatamiseks olemasolevast süsteemist Commerce'i peate lisama Dynamics 365 hinnangud ja ülevaate ühenduse olemasolevale voole Power Automate Power Automate või uuele. Lisateavet vt : [Dynamics 365 Commerce hinnangud ja ülevaated](/connectors/dynamics365ratingsre/) (eelvaade).

> [!IMPORTANT]
> Enne selle protseduuri sooritamist peate konfigureerima [S2S-i](service-to-service-auth.md) autentimise.

Hinnangute ja hinnangute importimiseks Commerce'i, kasutades Dynamics 365 hinnanguid ja ülevaateid Power Automate konnektorit, järgige neid samme.

1. Valige tegevus **Kasutaja ülevaate** esitamine.
1. Looge ühendus, kasutades Azure Active Directory ( ) rakenduse Azure AD teavet, mis loodi S2S-i autentimise konfigureerimisel. Lisateavet vt [konfigureerimisteenuselt teenusele](service-to-service-auth.md) autentimine.
1. Kasutaja **läbivaatuse** esitamine võtab korraga üle ühe ülevaate. Seega korrake tegevust. Kasutage lähteüleüleste ülevaateid hulgiüleste reviews esitamiseks loendina.
    
## <a name="export-ratings-and-reviews"></a>Ekspordi hinnangud ja ülevaated

Hinnangute eksportimiseks ja äriandmete läbivaatamiseks peate olemasolevale voole või uuele voole lisama Dynamics 365 hinnangud ja Power Automate Power Automate ülevaate ühenduse. Lisateavet vt : [Dynamics 365 Commerce hinnangud ja ülevaated](/connectors/dynamics365ratingsre/) (eelvaade).

Äri hinnangute ja hinnangute eksportimiseks, kasutades Dynamics 365 hinnanguid ja ülevaateid Power Automate konnektorit, järgige neid samme.

1. Valige suvand **Ekspordi kõik** ülevaated.
1. Tegevuse lõpule viimine. 

## <a name="additional-resources"></a>Lisaressursid

[Hinnangute ja arvustuste ülevaade](ratings-reviews-overview.md)

[Hinnangute ja arvustuste kasutamise valimine](opt-in-ratings-reviews.md)

[Hinnangute ja arvustuste haldus](manage-reviews.md)

[Hinnangute ja arvustuste konfigureerimine](configure-ratings-reviews.md)

[Toote hinnangute sünkroonimine](sync-product-ratings.md)

[Lubage hinnangute ja ülevaadete käsitsi avaldamine moderaatori poolt](manual-publish-rating-reviews.md)

[Teenusepõhise autentimise konfigureerimine](service-to-service-auth.md)

[Hinnangud ja arvustused KKK](ratings-reviews-faq.md)
