---
title: Dynamics 365 Commerce ja Microsoft Teams integratsiooni lubamine
description: See artikkel kirjeldab, kuidas lubada ja Microsoft Dynamics 365 Commerce integreerida Microsoft Teams.
author: gvrmohanreddy
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f8b84938c2047ab1102864cc203e0ec853160bb1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274309"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>Dynamics 365 Commerce ja Microsoft Teams integratsiooni lubamine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas lubada ja Microsoft Dynamics 365 Commerce integreerida Microsoft Teams.

Teamsile teabe andmiseks rakendusest Dynamics 365 Commerce ja müügikoha rakenduse ning Teamsi vaheliste ülesandehalduse funktsioonide teabega sünkroonimiseks peate lubama Commerce'i keskuse integreerimisfunktsioonid.

> [!NOTE]
> Teamsi integreerimise lubamisel nõustute jagama andmeid Teamsiga. Andmed, mida jagatakse Teamsiga, võivad olla teises riigis kui teie Commerce'i andmed ja nende puhul võivad kehtida erinevad vastavusstandardid. Lisateavet vt [Microsoft Trust Center](https://www.microsoft.com/trust-center). Lisateavet Microsofti privaatsuspoliitikate kohta vt [Microsofti privaatsusavaldusest](https://aka.ms/privacy).

## <a name="enable-teams-integration"></a>Teamsi integratsiooni lubamine

Enne, kui saate Microsoft Teams integratsiooni Commerce'iga lubada, peate registreerima Teamsi rakenduse oma rentnikuga Azure'i portaalis.

Teamsi rakenduse registreerimiseks oma rentnikuga Azure'i portaalis järgige järgmisi samme.

1. Järgige samme jaotises [Kiirstart: rakenduse registreerimine Microsofti identiteediplatvormis](/azure/active-directory/develop/quickstart-register-app), et registreerida Teamsi rakendus oma rentnikuga Azure'i portaalis.
1. Valige vahekaardil **Rakenduse** registreerimine rakendus, mille lõite eelmises sammus. Seejärel valige vahekaardil **Autentimine** suvand **Lisa platvorm**.
1. Valige dialoogiboksis **veeb**. Seejärel sisestage **väljale Ümbersuunamise URL-id** URL **\<HQUrl\> vormingus /oauth**. Asendage **\<HQUrl\>** oma Commerce headquartersi URL-iga (nt `https://hxennugbjtweufmdeo385f47fadb6aa9a0aos.cloudax.int.dynamics.com/oauth`).
1. Kopeerige **registreeritud** rakenduse ülevaate lehel rakenduse (kliendi **) ID** väärtus. Peate selle väärtuse andma, et lubada teamsi integreerimist järgmises jaotises Commerce headquartersis.
1. Kliendisaladuse lisamiseks [järgige juhendit](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret) "Lisa kliendi saladus". Seejärel kopeerige **kliendi salaväärtuse** väärtus. Peate selle väärtuse andma, et lubada teamsi integreerimist järgmises jaotises Commerce headquartersis.
1. Valige **API õigused** ja seejärel valige **luba**.
1. Dialoogiaknas **Taotluse API õigused** valige Microsoft Graph **,** valige Delegeeritud **õigused,** laiendage Grupp, **·** **valige Group.ReadWrite.All** ja seejärel valige lisa **õigused**.
1. Dialoogiaknas **Taotluse API** õigused valige suvand Lisa õigus, **·** **valige Microsoft Graph**,**valige** rakenduse õigused, **laiendage** grupp, **valige Group.ReadWrite.All** ja seejärel valige suvand **Add permissions (Lisa õigusi).**
1. Dialoogiaknas **Api õiguste** taotlemine valige **suvand Lisa õigus**. Vahekaardil Minu **organisatsioon kasutab API-sid** jaemüügiteenuse **Microsoft Teams otsimiseks** ja valige see.
1. Valige **delegeeritud õigused**, laiendage **TaskPublishing**, valige **TaskPublising.ReadWrite.All** ja seejärel valige **lisa õigused**. Lisateavet vt kliendirakenduse [konfigureerimine veebi API-le juurdepääsemiseks](/azure/active-directory/develop/quickstart-configure-app-access-web-apis).

Commerce'i peakeskuses Teamsi integratsiooni lubamiseks toimige järgmiselt.

1. Valige suvandid **Retail ja Commerce \> Kanali häälestus \> Microsoft Teams integratsiooni konfiguratsioon**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Määrake suvand **Luba Microsoft Teams integratsioon** valikule **Jah**.
1. Sisestage **väljale Rakenduse ID** rakenduse (kliendi) ID **väärtus,** mille te kogunud rakenduse Teams Azure portaalis registreerinud olete.
1. Sisestage **rakendusvõtme väljale** "Salaväärtus", **mille** olete saanud kliendisaladuse sisestamisel Azure’i portaali.
1. Valige toimingupaanil nupp **Salvesta**.

Järgmine joonis kuvab näidet Teamsi integreerimise konfigureerimise kohta Commerce'i peakeskuses.

![Teamsi integreerimise konfiguratsioon Commerce'i peakeskuses.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

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
