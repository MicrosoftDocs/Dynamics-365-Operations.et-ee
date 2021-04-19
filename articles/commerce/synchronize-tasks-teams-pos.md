---
title: Ülesannete halduse sünkroonimine Microsoft Teams ja Dynamics 365 Commerce kassade vahel
description: See teema kirjeldab, kuidas sünkroonida ülesannete haldust Microsoft Teams ja Dynamics 365 Commerce müügikoha vahel.
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
ms.openlocfilehash: ca0cb32ac3ee508ddcd5346a895fb9904fa92517
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842650"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a>Ülesannete halduse sünkroonimine Microsoft Teams ja Dynamics 365 Commerce kassade vahel

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

See teema kirjeldab, kuidas sünkroonida ülesannete haldust Microsoft Teams ja Dynamics 365 Commerce müügikoha vahel.

Teams'i integreerimise üks peamisi eesmärke on võimaldada kassarakenduse ja Teams-i ülesannete halduse sünkroonimist. Nii saavad poe töötajad ülesannete haldamiseks kasutada kas POS-rakendust või Teamsit ega pea rakendusi vahetama.

Kuna Plannerit kasutatakse Teamsi ülesannete hoidlana, peab olema seos Teamsi ja Dynamics 365 Commerce vahel. Selle lingi loomiseks kasutatakse konkreetse poe meeskonna kindlat plaani ID-d.

Järgmised protseduurid näitavad, kuidas seadistada POS- ja Teams-rakenduste vahel ülesannete haldamise sünkroonimine.

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

## <a name="link-pos-and-teams-for-task-management"></a>Kassa ja Teams linkimine ülesannete haldamiseks

Kassa ja Microsoft Teams rakenduste linkimiseks Commerce peakontori ülesandehalduse jaoks järgige neid samme.

1. Minge **Retail ja Commerce \> Ülesandehaldus \>Ülesannete integreerimine rakendusega Microsoft Teams**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Määrake suvandi **Luba ülesandehalduse integratsioon** väärtuseks **Jah**.
1. Valige toimingupaanil nupp **Salvesta**.
1. Tegumiribal valige **Ülesandehalduse seadistamine**. Peaksite saama teatise, mis näitab, et luuakse partiitöö nimega **Teamsi ettevalmistamine**.
1. Minge **Süsteemihaldus \> Päringud \> Partiitööd** ja leidke viimane töö, mille kirjeldus on **Teamsi ettevalmistamine**. Oodake, kuni töö on lõpuni viidud.
1. Käitage **CDX-töö 1070**, et avaldada plaani ID ja talletada viited jaemüügiserveris.

## <a name="additional-resources"></a>Lisaressursid

[Dynamics 365 Commerce ja Microsoft Teams integratsiooni ülevaade](commerce-teams-integration.md)

[Dynamics 365 Commerce ja Microsoft Teams integratsiooni lubamine](enable-teams-integration.md)

[Microsoft Teams sätted rakendusest Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Kasutaja rollide haldamine rakenduses Microsoft Teams](manage-user-roles-teams.md)

[Kaupluste ja töörühmade vastendamine, kui töörühmad on olemas rakenduses Microsoft Teams](map-stores-existing-teams.md)

[Dynamics 365 Commerce ja Microsoft Teams integratsiooni KKK](teams-integration-faq.md)
