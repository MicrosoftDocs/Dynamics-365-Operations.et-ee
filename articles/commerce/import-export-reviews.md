---
title: Hinnangute ja arvustuste importimine ja eksportimine
description: See artikkel kirjeldab, kuidas importida ja eksportida toote hinnanguid ja ülevaateid moodulis Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 97407f62d462c0ae370e9ea0d2799d3f30ecacfa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863397"
---
# <a name="import-and-export-ratings-and-reviews"></a>Hinnangute ja arvustuste importimine ja eksportimine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas importida ja eksportida toote hinnanguid ja ülevaateid moodulis Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce pakub [hinnanguid ja kommentaare](ratings-reviews-overview.md) kanali kanali lahendusena. Kui lülitute Dynamics 365 Commerce üle hinnangutele ja vaatate üle lahenduse, võite soovida teisaldada oma olemasolevad hinnangud ja ülevaated andmete üle Äriplatvormile. Ärinõuete alusel võite soovida eksportida ka hinnanguid ja ülevaateid Commerce'ist. Konnektor Power Automate võimaldab teil importida hinnanguid ja ülevaateid Commerce'isse ja eksportida neid Commerce'ist.

> [!NOTE]
> Lisateavet selle kohta, kuidas loogikavoogudega alustada, Power Automate vt teemast [Pilve voo loomine Power Automate](/power-automate/get-started-logic-flow).

## <a name="prerequisites"></a>Eeltingimused

Enne hinnangute ja hinnangute importimist ja eksportimist peate täitma järgmised eeltingimused:

- Hinnangud ja ülevaatuslahendus peavad olema äriplatvormi e-posti saidi puhul lubatud. Lisateavet vt nõustumise hinnanguid [ja kommentaare kasutama](opt-in-ratings-reviews.md).
- Dynamics 365 hinnangud ja ülevaated Power App Connector peab olema konfigureeritud lubama toimingute "edasta ülevaated" või "ekspordi ülevaated" lubamiseks rakenduses Power Automate. Lisateavet vt – hinnangud [Dynamics 365 Commerce ja ülevaated (eelvaade).](/connectors/dynamics365ratingsre/)
- Teenuse-teenuse (S2S) autentimine peab olema konfigureeritud nii, et see kutsuks turvaliselt hinnangud ja vaataks üle rakenduse programmeerimisliidese (API) väljast Commerce. Lisateavet vt "Teenuseteenuse [autentimise konfigureerimine"](service-to-service-auth.md).

## <a name="import-ratings-and-reviews"></a>Hinnangute ja kommentaaride importimine

Hinnangute importimiseks ja läbivaatamiseks olemasolevast süsteemist Commerce'i peate lisama Dynamics 365 Power Automate Power Automate hinnangud ja ülevaate ühenduse olemasolevale voole või uuele. Lisateavet vt – hinnangud [Dynamics 365 Commerce ja ülevaated (eelvaade).](/connectors/dynamics365ratingsre/)

> [!IMPORTANT]
> Enne selle protseduuri sooritamist peate konfigureerima [S2S-i autentimise](service-to-service-auth.md).

Hinnangute ja hinnangute importimiseks Commerce'i, kasutades Dynamics 365 hinnanguid ja ülevaateid Power Automate konnektorit, järgige neid samme.

1. Valige tegevus **Kasutaja ülevaate esitamine**.
1. Looge ühendus, kasutades Azure Active Directory () rakenduse teavet Azure AD, mis loodi S2S-i autentimise konfigureerimisel. Lisateavet vt teenuselt [teenusele autentimise konfigureerimine](service-to-service-auth.md).
1. Kasutaja **läbivaatuse esitamine** võtab korraga üle ühe ülevaate. Seega korrake tegevust. Kasutage lähteüleüleste ülevaateid hulgiüleste reviews esitamiseks loendina.
    
## <a name="export-ratings-and-reviews"></a>Ekspordi hinnangud ja ülevaated

Hinnangute eksportimiseks ja äriandmete läbivaatamiseks peate olemasolevale voole või uuele voole lisama Dynamics 365 Power Automate Power Automate hinnangud ja ülevaate ühenduse. Lisateavet vt – hinnangud [Dynamics 365 Commerce ja ülevaated (eelvaade).](/connectors/dynamics365ratingsre/)

Äri hinnangute ja hinnangute eksportimiseks, kasutades Dynamics 365 hinnanguid ja ülevaateid Power Automate konnektorit, järgige neid samme.

1. Valige suvand **Ekspordi kõik ülevaated**.
1. Tegevuse lõpule viimine. 

## <a name="additional-resources"></a>Lisaressursid

[Hinnangute ja arvustuste ülevaade](ratings-reviews-overview.md)

[Hinnangute ja arvustuste kasutamise valimine](opt-in-ratings-reviews.md)

[Hinnangute ja arvustuste haldus](manage-reviews.md)

[Hinnangute ja arvustuste konfigureerimine](configure-ratings-reviews.md)

[Toote hinnangute sünkroonimine](sync-product-ratings.md)

[Lubage hinnangute ja ülevaadete käsitsi avaldamine moderaatori poolt](manual-publish-rating-reviews.md)

[Teenusest teenusesse autentimise konfigureerimine](service-to-service-auth.md)

[Hinnangud ja arvustused KKK](ratings-reviews-faq.md)
