---
title: Dynamics 365 Commerce ja Microsoft Teams integratsiooni lubamine
description: See teema kirjeldab, kuidas lubada Microsoft Dynamics 365 Commerce ja Microsoft Teams integratsiooni.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c0dbf7a3c7fa3532e35cac240c1abb8adbdbe489
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842647"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>Dynamics 365 Commerce ja Microsoft Teams integratsiooni lubamine

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

See teema kirjeldab, kuidas lubada Microsoft Dynamics 365 Commerce ja Microsoft Teams integratsiooni.

Teamsile teabe andmiseks rakendusest Dynamics 365 Commerce ja müügikoha rakenduse ning Teamsi vaheliste ülesandehalduse funktsioonide teabega sünkroonimiseks peate lubama Commerce'i keskuse integreerimisfunktsioonid.

> [!NOTE]
> Teamsi integreerimise lubamisel nõustute jagama andmeid Teamsiga. Andmed, mida jagatakse Teamsiga, võivad olla teises riigis kui teie Commerce'i andmed ja nende puhul võivad kehtida erinevad vastavusstandardid. Lisateavet vt [Microsoft Trust Center](https://www.microsoft.com/trust-center). Lisateavet Microsofti privaatsuspoliitikate kohta vt [Microsofti privaatsusavaldusest](https://aka.ms/privacy).

## <a name="enable-teams-integration"></a>Teamsi integratsiooni lubamine

Enne, kui saate Microsoft Teams integratsiooni Commerce'iga lubada, peate registreerima Teamsi rakenduse oma rentnikuga Azure'i portaalis.

Teamsi rakenduse registreerimiseks oma rentnikuga Azure'i portaalis järgige järgmisi samme.

1. Järgige samme jaotises [Kiirstart: rakenduse registreerimine Microsofti identiteediplatvormis](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app), et registreerida Teamsi rakendus oma rentnikuga Azure'i portaalis.
1. Kopeerige **Rakenduse (kliendi) ID** väärtus registreeritud rakenduse lehel **Ülevaade**. Kasutate seda väärtust Teamsi integreerimise lubamiseks Commerce peakeskuses.
1. Kopeerige tunnistuse väärtus, mis [lisati tunnistusele](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) etapis 1. Tunnistust nimetatakse ka avalikuks võtmeks või rakenduse võtmeks. Kasutate seda väärtust Teamsi integreerimise lubamiseks Commerce peakeskuses.

Commerce'i peakeskuses Teamsi integratsiooni lubamiseks toimige järgmiselt.

1. Valige suvandid **Retail ja Commerce \> Kanali häälestus \> Microsoft Teams integratsiooni konfiguratsioon**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Määrake suvand **Luba Microsoft Teams integratsioon** valikule **Jah**.
1. Väljades **Rakenduse ID** ja **Rakenduse võti** sisestage väärtused, mis te olete saanud rakenduse Teams registreerimisel Azure'i portaalis.
1. Valige toimingupaanil nupp **Salvesta**.

Järgmine joonis kuvab näidet Teamsi integreerimise konfigureerimise kohta Commerce'i peakeskuses.

![Teamsi integreerimise konfiguratsioon Commerce'i peakeskuses](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a>Teamsi integratsiooni keelamine

Commerce'i peakeskuses Microsoft Teams integratsiooni keelamiseks toimige järgmiselt.

1. Valige suvandid **Retail ja Commerce \> Kanali häälestus \> Microsoft Teams integratsiooni konfiguratsioon**.
1. Valige Toimingupaanil nupp **Redigeeri**.
3. Määrake suvand **Luba Microsoft Teams integratsioon** valikule **Ei**.
4. Tühjendage väärtused väljadelt **Rakenduse ID** ja **Rakenduse võti**.
1. Valige toimingupaanil nupp **Salvesta**.

> [!NOTE]
> Pärast Teamsi integreerimise keelamist Commerce'iga ei kuva kassaterminalid enam ülesandeid, mis on avaldatud Teamsi rakendusest.

## <a name="additional-resources"></a>Lisaressursid

[Dynamics 365 Commerce ja Microsoft Teams integratsiooni ülevaade](commerce-teams-integration.md)

[Microsoft Teams sätted rakendusest Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Ülesannete halduse sünkroonimine Microsoft Teams ja Dynamics 365 Commerce kassade vahel](synchronize-tasks-teams-pos.md)

[Kasutaja rollide haldamine rakenduses Microsoft Teams](manage-user-roles-teams.md)

[Kaupluste ja töörühmade vastendamine, kui töörühmad on olemas rakenduses Microsoft Teams](map-stores-existing-teams.md)

[Dynamics 365 Commerce ja Microsoft Teams integratsiooni KKK](teams-integration-faq.md)
