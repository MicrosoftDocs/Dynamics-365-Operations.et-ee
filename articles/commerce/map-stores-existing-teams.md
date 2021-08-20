---
title: Kaupluste ja töörühmade vastendamine, kui töörühmad on olemas rakenduses Microsoft Teams
description: See teema käsitleb, kuidas vastendada gruppe ja vastavaid meeskondi Dynamics 365 Commerce peakontoris, kui teie organisatsioon on juba enne Microsoft Teams Commerce integratsioonimeeskondi loonud.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 6faba58304e1fe9e9ba2ce1a76fbf1cc783466bf01b0d4e3774e8ed090485bb1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757365"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a>Kaupluste ja töörühmade vastendamine, kui töörühmad on olemas rakenduses Microsoft Teams

[!include [banner](includes/banner.md)]

See teema käsitleb, kuidas vastendada gruppe ja vastavaid meeskondi Dynamics 365 Commerce peakontoris, kui teie organisatsioon on juba enne Microsoft Teams Commerce integratsioonimeeskondi loonud.

Organisatsioonil võib olla meeskondi, mis on loodud mõnede või kõigi oma poodide jaoks enne Dynamics 365 Commerce ja Microsoft Teams integreerimist. Sel juhul peate Commerce POS-i vahel ülesannete sünkroonimise loomiseks vastendama kauplusi ja vastavaid meeskondi Microsoft Teams Commerce peakontoris.

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a>Kaupluste ja vastavate töörühmade vastendamine Commerce peakontoris 

Kaupluste ja vastavate töörühmade vastendamiseks Commerce peakontoris järgige järgmisi samme.

1. Minge jaotisse **Süsteemihaldus \> Tööruum \> Andmehaldus**.
1. Valige **Ekspordi**. 
1. Valige toimingupaanil nupp **Uus**.
1. Jaotises **Grupi nimi** sisestage "Ekspordi Teams vastendamine".
1. Valige kiirsakis **Valitud üksused** suvand **Lisa üksus**. Ilmub dialoogiboks **Lisa üksus**.  
1. Valige ripploendist **Üksuse nime** **Teams vastendamine allika ja töörühma vahel**.
1. Valige ripploendist **Sihtandmete vorming** suvand **CSV**.
1. Valige **Lisa** ja seejärel **Sulge**.
1. Tegevuspaanist üleval ja vasakul valige suvand **Ekspordi kohe**.
1. Valige **Üksuse töötlemise olek** alt **Lae fail alla**.
1. Eksporditud CSV-failis sisestage väärtused **SOURCETYPE**, **SOURCEID** ja **TEAMID** järgmiselt:
    - **SOURCETYPE** puhul "RetailStore". 
    - **SOURCEID** puhul sisestage kaupluse number (nt San Francisco kaupluse puhul "000135"). Kaupluse numbrid leiate asukohast **Retail ja Commerce \> Kanalid \> Kauplused**.
    - **TEAMID** puhul sisestage vastav meeskonna ID Microsoft Teams asukohast (nt " 5f8bc92b-6aa8-451e-85d1-3949c01ddc6c"). Meeskonna ID teavet võite leida veebilehelt [admin.teams.microsoft.com](https://admin.teams.microsoft.com).
1. Salvestage CSV-fail oma kohalikku arvutisse.
1. Minge jaotisse **Süsteemihaldus \> Tööruum \> Andmehaldus** ja valige suvand **Impordi**.
1. Valige kiirsakis **Valitud üksused** suvand **Lisa fail**. Ilmub dialoogiboks **Lisa fail**.
1. Valige ripploendist **Üksuse nime** **Teams vastendamine allika ja töörühma vahel**.
1. Valige ripploendist **Algandmete vorming** suvand **CSV**.
1. Valige **Üleslaadimine ja lisamine**, seejärel valige eelnevalt salvestatud CSV-fail ja seejärel valige käsk **Ava**.
1. Valige dialoogiboksis **Lisa fail** suvand **Sulge**.
1. Valige toimingupaanil **Salvesta** ja seejärel **Impordi**.

Järgmises näitepildis on näidatud Commerce-i **Ekspordi töörühmade vastendamise** grupp koos elementidega **Lisa üksus** ja eksporditud CSV-faili rõhutatud päistega.

![Commerce-i töörühmade vastendamise grupi eksportimine koos üksuse lisamise elementidega ja eksporditud CSV-faili rõhutatud päistega.](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> Eeltoodud sammude järgselt järgige ülesandehalduse sünkroonimiseks jaotise [Microsoft Teams ja kassa vahelise toiminguhalduse ja sünkroonimine](synchronize-tasks-teams-pos.md) etappe. 

## <a name="additional-resources"></a>Lisaressursid

[Dynamics 365 Commerce ja Microsoft Teams integratsiooni ülevaade](commerce-teams-integration.md)

[Dynamics 365 Commerce ja Microsoft Teams integratsiooni lubamine](enable-teams-integration.md)

[Microsoft Teams sätted rakendusest Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Ülesannete halduse sünkroonimine Microsoft Teams ja Dynamics 365 Commerce kassade vahel](synchronize-tasks-teams-pos.md)

[Kasutaja rollide haldamine rakenduses Microsoft Teams](manage-user-roles-teams.md)

[Dynamics 365 Commerce ja Microsoft Teams integratsiooni KKK](teams-integration-faq.md)
