---
title: Dynamics 365 Commerce ja Microsoft Teams integratsiooni ülevaade
description: See artikkel annab ülevaate ja Microsoft Dynamics 365 Commerce integratsiooni Microsoft Teams.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 928322c6a391510621bfebbb57d3930f91e69e24
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282899"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a>Dynamics 365 Commerce ja Microsoft Teams integratsiooni ülevaade

[!include [banner](includes/banner.md)]

See artikkel annab ülevaate ja Microsoft Dynamics 365 Commerce integratsiooni Microsoft Teams.

Dynamics 365 Commerce integreerub rakendusega Teams, et aidata kliente ja nende töötajaid, parandades tööviljakust kahe rakenduse vahelisi ülesandeid sünkroonides. Rakenduse Commerce and Teams sujuvam ülesande haldus võimaldab kaupluste juhatajal ja töötajal luua ülesannete loendeid, määrata ülesandeid mitmele kauplusele ja jälgida toimingute olekut kauplustes olenemata millisest rakendusest seda tehti.

Commerce and Teamsi integreerimine on saadaval rakenduse Commerce versiooni 10.0.18 väljalaskest.

## <a name="key-features"></a>Võtmefunktsioonid

Need on mõned Commerce ja Microsoft Teams integratsiooni põhifunktsioonid:

- Kasutage rakendust Teams kasutades Commerce'is määratletud teavet, nagu organisatsiooniline struktuur ja teave kaupluste, töötajate, õiguste ja ärikonteksti kohta.
- Saate hõlpsalt sünkroonida Commerce ja Teams vahelisi jooksvaid muudatusi (nt uute poodide lisamine või uute töötajate palkamine), kuid säilitada Commerce organisatsioonilist struktuuri andmete põhiallikana.
- Integreerige Commerce ja Teams vahelisi ülesannete haldust, et aidata salvestada töötajaid, kaupluste juhatajaid, piirkonnajuhid ja kommunikatsioonijuhid ülesandehaldust ükskõik kummast rakendusest.

## <a name="prerequisites-for-using-integration-features"></a>Integratsioonifunktsiooni kasutamise eeltingimused

Enne Microsoft Teams integratsioonifunktsiooni kasutamist peavad olema täidetud järgmised eeltingimused:

- Microsoft 365 Äristandardi litsents (see litsents sisaldab Teamsi).
- Azure Active Directory (Azure AD) kontod kõigile kaupluse juhatajatele ja töötajatele
- Azure AD autentimisega konfigureeritud kassasüsteemid

## <a name="conceptual-architecture"></a>Kontseptuaalne arhitektuur

Järgmine näide näitab kontseptuaalset Dynamics 365 Commerce ja Microsoft Teams integratsiooni ülesehitust, kasutades näitena San Francisco kauplust. Nii Teamsi kui ka Commerce kassarakendus kasutab hoidlana Microsoft Plannerit, nii et Teamsis avaldatud ülesanded ilmuvad kassarakenduses ja kassahaldurite loodud sihtülesanded ilmuvad Teamsis, mistõttu rakenduste vahel toimub tõrgeteta ülesannete haldus.    

![Commerce`i ja Teams`i integratsiooni ülesehitus.](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a>Lisaressursid

[Dynamics 365 Commerce ja Microsoft Teams integratsiooni lubamine](enable-teams-integration.md)

[Microsoft Teams sätted rakendusest Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Ülesannete halduse sünkroonimine Microsoft Teams ja Dynamics 365 Commerce kassade vahel](synchronize-tasks-teams-pos.md)

[Kasutaja rollide haldamine rakenduses Microsoft Teams](manage-user-roles-teams.md)

[Kaupluste ja töörühmade vastendamine, kui töörühmad on olemas rakenduses Microsoft Teams](map-stores-existing-teams.md)

[Dynamics 365 Commerce ja Microsoft Teams integratsiooni KKK](teams-integration-faq.md)
