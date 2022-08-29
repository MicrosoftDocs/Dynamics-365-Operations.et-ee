---
title: Dynamics 365 Commerce ja Microsoft Teams integratsiooni KKK
description: See artikkel annab vastused korduma kippuvatele küsimustele ja Microsoft Dynamics 365 Commerce integratsioonile Microsoft Teams.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 79e8c6899d84c3d6147c0a0c2834a7ad2f7b6927
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292050"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a>Dynamics 365 Commerce ja Microsoft Teams integratsiooni KKK

[!include [banner](includes/banner.md)]

See artikkel annab vastused korduma kippuvatele küsimustele ja Microsoft Dynamics 365 Commerce integratsioonile Microsoft Teams.

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a>Kes poes saab Commerce'i Teamsi ettevalmistamise ajal töörühmade omanikuks? 

Kõik kaupluste juhatajad lisatakse automaatselt vastavasse töörühmagruppi omanikena, et nad saaksid sooritada toiminguid, nagu privaatse kanali lisamine ning liikmete lisamine või kustutamine. 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a>Kuidas määrata Commerce'i peakontoris töötajale "sidehalduri" roll? 

Kommunikatsioonihaldurid Microsoft Teams rakenduses saavad luua ja avaldada ülesannete loendeid. Organisatsiooni töötajatel, kellest saavad kommunikatsioonihaldurid, peab olema Commerce peakontoris määratud jaemüügi ülesandehalduri roll.

Jaemüügi ülesandehalduri rolli määramiseks töötajale Commerce peakontoris toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus \> Töötajad \> Kasutajad**.
1. Valige töötaja.
1. Kiirkaardil **Kasutaja rollid** valige suvand **Määra rollid**.
1. Dialoogiboksis **Määra kasutajale rollid** valige roll **Jaemüügi ülesannete haldur** ja seejärel valige **OK**.

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a>Kuidas teha konkreetne organisatsiooni hierarhia üleslaadimiseks Microsoft Teams rakenduses kättesaadavaks?

Commerce peakontoris on iga organisatsiooni hierarhia seostatud ühe või mitme eesmärgiga. Veenduge, et hierarhial, kuhu soovite eraldise Microsoft Teams teha, oleks seostatud **jaemüügi aruandluse** eesmärgiga, nagu näha järgmises näitepildis. 

![Organisatsiooni hierarhia eesmärgi näide Commerce'i peakontoris.](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a>Kuidas lubada kaupluse töötajatel Azure Active Directory (Azure AD) kasutades Commerce kassasse sisse logida?

Teavet Commerce POS-i sisselogimiskogemuse konfigureerimise kohta Azure AD autentimise kasutamiseks vt [Luba Azure Active Directory autentimine POS sisselogimiseks](aad-pos-logon.md).

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a>Kuidas vastendada kauplusi ja vastavaid meeskondi Commerce peakontoris, kui minu organisatsioon on juba loonud Microsoft Teams meeskonnad?

Lisateavet kaupluste ja töörühmade vastendamise kohta olemasolevate töörühmade korral vaadake jaotisest [Kaupluste ja vastavate töörühmade vastendamine, kui teie organisatsioonil on olemas eelnevalt olemas olevad meeskonnad rakenduses Microsoft Teams](map-stores-existing-teams.md).

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a>Kuidas tühjendada seansi talletusse salvestatud Microsoft Graph API tookenit?

Kasutaja, kes on kassasse sisse loginud Azure Active Directory (Azure AD) kontoga, peaks kassast välja logima või sulgema rakenduse, et seansi ladustamine kustutada. 

> [!TIP]
> Soovitatav on töötajatel kassaterminali alati lukustada või seansist välja logida, kui terminali ei kasutata. 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a>Mis juhtub, kui kauplusel ei ole kaupluse juhatajaid?

Kui kauplusel ei ole juhatajaid, siis kaupluse või Teamsi gruppi ei looda. 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a>Mis juhtub, kui kaupluse juhataja ettevõttest lahkub?

Kõik omanikurolliga isikud saavad Commerce peakontoris lisada uue kauplusehalduri ja uuesti ette valmistada Teamsi, et uuel halduril oleks Teamsi grupi jaoks vajalikud privileegid. 

## <a name="additional-resources"></a>Lisaressursid

[Dynamics 365 Commerce ja Microsoft Teams integratsiooni ülevaade](commerce-teams-integration.md)

[Dynamics 365 Commerce ja Microsoft Teams integratsiooni lubamine](enable-teams-integration.md)

[Microsoft Teams sätted rakendusest Dynamics 365 Commerce](provision-teams-from-commerce.md)

[Ülesannete halduse sünkroonimine Microsoft Teams ja Dynamics 365 Commerce kassade vahel](synchronize-tasks-teams-pos.md)

[Kasutaja rollide haldamine rakenduses Microsoft Teams](manage-user-roles-teams.md)

[Kaupluste ja töörühmade vastendamine, kui töörühmad on olemas rakenduses Microsoft Teams](map-stores-existing-teams.md)
