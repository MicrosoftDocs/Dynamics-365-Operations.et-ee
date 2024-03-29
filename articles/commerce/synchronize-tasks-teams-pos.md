---
title: Ülesannete halduse sünkroonimine Microsoft Teams ja Dynamics 365 Commerce kassade vahel
description: See artikkel kirjeldab, kuidas sünkroonida ülesannete haldust Microsoft Teams müügikoha Dynamics 365 Commerce ja kassa vahel.
author: gvrmohanreddy
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f339ae031f11ad850dab47f84bc9823cf6776e74
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746093"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a>Ülesannete halduse sünkroonimine Microsoft Teams ja Dynamics 365 Commerce kassade vahel

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas sünkroonida ülesannete haldust Microsoft Teams müügikoha Dynamics 365 Commerce ja kassa vahel.

Teams'i integreerimise üks peamisi eesmärke on võimaldada kassarakenduse ja Teams-i ülesannete halduse sünkroonimist. Nii saavad poe töötajad ülesannete haldamiseks kasutada kas POS-rakendust või Teamsit ega pea rakendusi vahetama.

Kuna Plannerit kasutatakse Teamsi ülesannete hoidlana, peab olema seos Teamsi ja Dynamics 365 Commerce vahel. Selle lingi loomiseks kasutatakse konkreetse poe meeskonna kindlat plaani ID-d.

Järgmised protseduurid näitavad, kuidas seadistada POS- ja Teams-rakenduste vahel ülesannete haldamise sünkroonimine.

## <a name="link-pos-and-teams-for-task-management"></a>Kassa ja Teams linkimine ülesannete haldamiseks

Kassa ja Microsoft Teams rakenduste linkimiseks Commerce peakontori ülesandehalduse jaoks järgige neid samme.

> [!NOTE]
> Enne, kui proovite integreerida ülesandehaldust Teamsiga, veenduge, et teil on lubatud ja [Dynamics 365 Commerce integratsioon Microsoft Teams](enable-teams-integration.md). 

1. Minge **Retail ja Commerce \> Ülesandehaldus \>Ülesannete integreerimine rakendusega Microsoft Teams**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Määrake suvandi **Luba ülesandehalduse integratsioon** väärtuseks **Jah**.
1. Valige toimingupaanil nupp **Salvesta**.
1. Tegumiribal valige **Ülesandehalduse seadistamine**. Peaksite saama teatise, mis näitab, et luuakse pakett-töö, mille nimi **on** Meeskonna sätted.
1. Minge **Süsteemihaldus \> Päringud \> Partiitööd** ja leidke viimane töö, mille kirjeldus on **Teamsi ettevalmistamine**. Oodake, kuni töö on töö lõpetanud.
1. Käitage **CDX-töö 1070**, et avaldada plaani ID ja talletada viited jaemüügiserveris.

## <a name="publish-a-test-task-list-in-teams"></a>Katseülesande loendi avaldamine Teamsis

Järgmine protseduur eeldab, et teie kauplusemeeskonnad kasutavad Microsoft Teams esmakordselt ülesandehalduse integreerimist Commerce'iga.

Katseülesannete loendi avaldamiseks Teamis järgige neid samme.

1. Logige Teami suhtlushaldurina sisse. Tavaliselt on kommunikatsioonijuhid kasutajad, kellel on Commerce'i **piirkonnajuhi** roll.
1. Valige vasakul navigeerimispaanil **Planner ülesanded** alusel.
1. Vahekaardil **Avaldatud loendid** valige all vasakul **Uus loend** ja nimetage uus loend **Testülesannete loend**.
1. Valige **Loo**. Uus loend kuvatakse jaotises **Mustandid**.
1. **Ülesande pealkirja** all andke esimesele ülesandele pealkiri **Teams integreerimise testimine**. Seejärel valige **Sisesta**.
1. Valige loendist **Mustandid** ülesandeloend. Seejärel valige ülemises parempoolses nurgas  **Avalda** .
1. Dialoogiboksis **Valige, kes avaldab**, valige meeskonnad, kes peaksid vastu võtma testülesannete loendi.
1. Avaldamisplaani läbivaatamiseks klõpsake nuppu **Edasi**. Kui peate muudatusi tegema, valige suvand  **Tagasi**. 
1. Valige käsk **Jätkamiseks kinnita** ja valige valige käsk **Avalda**.
1. Kui avaldamine on lõpule viidud, ilmub **avaldatud loendite** vahekaardi ülaosas teade, kui teie ülesannete loend on edukalt kohale toimetatud.

Lisateavet vt [Avalda ülesannete loendid, et luua ja jälgida organisatsiooni tööd](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).

> [!NOTE]
> Kui ülesandeloend on Töörühmades edukalt avaldatud, kuvatakse ülesanded kassas. Seejärel peavad kassajuhid ja kassapidajad kassasse Azure AD sisse logima. Lisateabe saamiseks vaadake kassa sisselogimise [artikli Azure Active Directory puhul autentimise lubamist](aad-pos-logon.md). 

## <a name="additional-resources"></a>Lisaressursid

[Dynamics 365 Commerce ja Microsoft Teams integratsiooni ülevaade](commerce-teams-integration.md)

[Dynamics 365 Commerce ja Microsoft Teams integratsiooni lubamine](enable-teams-integration.md)

[Microsoft Teams sätted rakendusest Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Kasutaja rollide haldamine rakenduses Microsoft Teams](manage-user-roles-teams.md)

[Kaupluste ja töörühmade vastendamine, kui töörühmad on olemas rakenduses Microsoft Teams](map-stores-existing-teams.md)

[Dynamics 365 Commerce ja Microsoft Teams integratsiooni KKK](teams-integration-faq.md)
