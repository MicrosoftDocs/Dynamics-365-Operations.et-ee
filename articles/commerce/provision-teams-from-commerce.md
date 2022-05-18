---
title: Microsoft Teams ettevalmistamine rakendusest Dynamics 365 Commerce
description: See teema kirjeldab, kuidas ette valmistada Microsoft Teams kasutades Dynamics 365 Commerce organisatsiooni andmeid.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 54c85d1b6b51b7b2608200a7fa8e343ac6d008d0
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690496"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a>Microsoft Teams ettevalmistamine rakendusest Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas ette valmistada Microsoft Teams kasutades Dynamics 365 Commerce organisatsiooni andmeid.

Kui te ei ole veel jaekaupluste meeskondi seadistanud, on töörühmade ettevalmistamine rakenduses Dynamics 365 Commerce lihtne. Kasutades Commerce'is hästi määratletud teavet, mida soovite Teamsis kasutada, saate aidata oma kaupluse töötajatel Teamsis alustada. See teave sisaldab organisatsiooni hierarhiat, kaupluse nimesid, töötaja teavet ja Azure Active Directory (Azure AD) kontosid. 

Teamsi ettevalmistamiseks on kaks peamist sammu:

1. Looge Teamsis igale kauplusele meeskond ja lisage sobiva töörühma liikmetena kaupluse töötajad. Kui töötaja on seostatud rohkem kui ühe kauplusega, on seda näha töörühma liikmelisuses. Luuakse kommunikatsioonimeeskond, mis kaasab piirkonna haldurid liikmetena, et aidata avaldada ülesandeid Teamsis.
1. Laadige oma organisatsioonihierarhia Teamsi üles rakendusest Commerce.

## <a name="provision-teams-in-commerce-headquarters"></a>Teamsi ettevalmistamine Commerce'i peakontoris

Enne Microsoft Teams ettevalmistamist viige lõpule järgmised ülesanded.

- Kinnitage, et kõik piirkonnajuhid oleksid tehtud kommunikatsioonijuhtideks.
- Kinnitage, et iga kaupluse juhataja ja töötaja Azure'i konto oleks seostatud juhataja või töötaja kirjega Commerce'i peakontoris.

Teamsi ettevalmistamiseks Commerce'i peakontoris toimige järgmiselt.

1. Valige suvandid **Retail ja Commerce \> Kanali häälestus \> Microsoft Teams integratsiooni konfiguratsioon**.
1. Klõpsake toimingupaanil suvandit **Töörühmade ettevalmistamine**. Luuakse partiitöö nimega **Töörühmade ettevalmistamine**.
1. Minge **Süsteemihaldus \> Päringud \> Partiitööd** ja leidke viimane töö, mille kirjeldus on **Teamsi ettevalmistamine**. Oodake, kuni töö on lõpuni viidud.

> [!TIP]
> Kui ükski teie piirkonna halduritest, kaupluste juhatajatest ja kaupluse töötajatest pole seotud Teams litsentsiga, võidakse kuvada järgmine tõrketeade: "Määratud SKU-kategooriate päring kasutajale nurjus." Probleemi lahendamiseks valige tegevuspaanil suvand **Sünkrooni töörühmad ja liikmed**.

<!-- ![Dynamics 365 Commerce - Teams integration configuration.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a>Teams ettevalmistamise valideerimine Teamsi halduskeskuses

Microsoft Teams halduskeskuses Microsoft Teams andmete ettevalmistamise kinnitamiseks järgige järgmisi samme.
    
1. Minge [Teams halduskeskusesse](https://admin.teams.microsoft.com/) ja logige sisse oma e-äri rentniku administraatorina.
1. Selle laiendamiseks valige vasakul navigeerimispaanil **Teams** ja seejärel valige suvand **Halda töörühmasid**.
1. Veenduge, et iga Commerce'i jaemüügikaupluse jaoks oleks loodud üks meeskond.
1. Valige meeskond ja kinnitage, et kaupluse töötajad on sellele liikmeteks lisatud.
1. Valige vasakul navigeerimispaanil **Kasutajad** ja kinnitage, et kõik kaupluse töötajad on kasutajateks lisatud.

Järgmine näide on lehe **Töörühmade haldamine** kohta Teams halduskeskuses.

![Töörühmade haldamise lehe näide Teams halduskeskuses.](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a>Laadige Commerce'i organisatsioonihierarhia Teamsi
    
Commerce hierarhiat saab kasutada ülesannete avaldamiseks rakenduses Microsoft Teams kõigile või valitud kauplustesse, mis kasutavad sama hierarhia struktuuri.

Faili üleslaadimiseks Commerce'i organisatsiooni hierarhiast Teamsi toimige järgmiselt.
    
1. Commerce'i peakontoris minge asukohta **Jaemüük ja kaubandus \> Kanali seadistamine \> Microsoft Teams integratsiooni konfiguratsioon**.
1. Valige **Allalaadimise sihthierarhia** ja valige seejärel **Jaemüügikauplused regiooni järgi**, et laadida alla organisatsiooni hierarhia komaeraldusega väärtused (CSV).
1. Installige Microsoft Teams PowerShelli moodul, järgides etappie jaotises [Microsoft TeamsPowerShelli installimine](/microsoftteams/teams-powershell-install).
1. Kui ilmub aknas Teams PowerShell teade, logige sisse, kasutades oma rentniku Azure AD administraatori kontot.
1. Järgige samme jaotises [Meeskonna sihthierarhia seadistamine](/microsoftteams/set-up-your-team-hierarchy) CSV-faili üleslaadimiseks sihthierarhia jaoks.

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a>Veenduge, et organisatsiooni hierarhia oleks Teamsi üles laaditud.

Veendumaks, et organisatsiooni hierarhia on Microsoft Teams üles laaditud toimige järgmiselt.

1. Logige Teami suhtlushaldurina sisse.
1. Valige vasakul navigeerimispaanil **Planner ülesanded** alusel.
1. Looge vahekaardil **Avaldatud loendid** uus loend, mis sisaldab fiktiivset ülesannet.
1. Valige **Avalda**. Organisatsioonihierarhia peaks ilmuma dialoogiboksis **Vali, kellele avaldada**, nagu näha järgmises näites.

![Organisatsioonihierarhia näide dialoogiaknas Vali, kellele avaldada.](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a>Lisaressursid

[Dynamics 365 Commerce ja Microsoft Teams integratsiooni ülevaade](commerce-teams-integration.md)

[Dynamics 365 Commerce ja Microsoft Teams integratsiooni lubamine](enable-teams-integration.md)

[Ülesannete halduse sünkroonimine Microsoft Teams ja Dynamics 365 Commerce kassade vahel](synchronize-tasks-teams-pos.md)

[Kasutaja rollide haldamine rakenduses Microsoft Teams](manage-user-roles-teams.md)

[Kaupluste ja töörühmade vastendamine, kui töörühmad on olemas rakenduses Microsoft Teams](map-stores-existing-teams.md)

[Dynamics 365 Commerce ja Microsoft Teams integratsiooni KKK](teams-integration-faq.md)