---
title: Ärivestlus mooduliga Power Virtual Agents
description: See artikkel kirjeldab Commerce Vestlust mooduliga Power Virtual Agents, mis integreerib Microsofti Power Virtual Agents veebisaitidega Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-07
ms.openlocfilehash: 838990cb638479c9c90ba0e38794ecedd55e95b3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690948"
---
# <a name="commerce-chat-with-power-virtual-agents-module"></a>Ärivestlus mooduliga Power Virtual Agents

[!include [banner](includes/banner.md)]

See artikkel kirjeldab Commerce Vestlust mooduliga Power Virtual Agents, mis integreerib Microsofti Power Virtual Agents veebisaitidega Dynamics 365 Commerce.

Ärivestlus funktsiooniga volitab Power Virtual Agents Dynamics 365 e-äri kliente Power Virtual Agents kasutama oma päringute jaoks vestlusfunktsioone. Dynamics 365 Commerce Alates 10.0.30 väljalaskest saab seda funktsiooni kaasata e-kaubanduse veebisaitidele, kasutades Commerce Commerce Commerce’i Power Virtual Agents vestlus mooduliga, mis on Ärimooduli teeki osa.

Ärivestlus funktsiooniga Power Virtual Agents aitab äril saavutada järgmised eesmärgid:

- Suurendage isikupärastatud koostööd oma tarbijaga ja parandage kinnipidamist.
- Klienditeeninduse suurendamine iseteenindusvestluste integreerimise kaudu.
- Kliendi üleüldise rahulolu suurendamiseks ja seega müügi kasvuks.

> [!NOTE]
> Dynamics 365Portaali Power Virtual Agents klienditeeninduse ja rakenduste erinevuste kohta leiate teavet Commerce’i [vestlusmoodulite ülevaatest](/commerce-chat-modules-overview.md).

## <a name="prerequisites-for-using-power-virtual-agents"></a><a id="prereq"></a> Kasutamise eeltingimused Power Virtual Agents

Ärivestluse funktsiooni kasutamiseks Power Virtual Agents peate kõigepealt looma oma e-äri Power Virtual Agents veebisaidi jaoks vestluse. Juhiseid vt teemast [Power virtual agent agent 2012](/power-virtual-agents/authoring-first-bot).

Pärast vestlusvestluse konfigureerimist peate **Commerce’i vestlusekogemuse konfigureerimiseks kopeerima Osanike ID ja rentniku ID** **vestlusparameetrite** väärtused. Teavet nende väärtuste kopeerimise kohta vt oma [parameetri toomiseks Power Virtual Agents](/power-virtual-agents/publication-connect-bot-to-custom-application#retrieve-your-power-virtual-agents-bot-parameters).

## <a name="configure-your-e-commerce-site"></a>Konfigureerige oma e-äri sait 

Üks soovitatav viis oma e-äri saidi vestluskogemuse juurutamiseks on lisada ärivestluse Power Virtual Agents moodul ühiskasutuses päise killus, mida kasutatakse teie saidi lehtedel.

Vestlusmooduli lisamiseks saidi päise killustaks Commerce’i saidi koostajas, järgige neid samme.

1. Minge oma saidi ärisaidi koostajas **killustajatele**.
1. Valige suvand **Uus**.
1. Dialoogiaknas **Tükitüki** valimine valige **mooduliga Commerce Vestlus Power Virtual Agents**, sisestage killusta nimi ja seejärel valige **OK**.
1. Valige liigendusvaates **Msdmeeter365 pva vestlusühenduse pesa**.
1. Järgige parempoolsel atribuutide paanil järgmisi samme.

    1. Kasutaja **parameetrite all** webtšeri **Bot Framework vestluse CDN-i URL-i** väljal jätke vaikeväärtus (nt `https://cdn.botframework.com/botframework-webchat/latest/webchat.js`).
    1. Jätke väljale **Bot Framework Direct Line Autentimise URL** vaikeväärtuseks (nt `https://powerva.microsoft.com/api/botmanagement/v1/directline/directlinetoken`).
    1. Sisestage **väljale Lisa ID Osasse** Power Virtual Agents Kasutamise eeltingimused **kopeeritud** Osamaksu ID [Power Virtual Agents](#prereq) väärtus.
    1. Sisestage **väljale Rentniku ID kopeeritud** rentniku ID **väärtus**.

1. Valige **Salvesta**, valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. **Minge killustele** ja avage oma saidi päise killust.
1. **Valige konteineri vaikepesas** kolmikpunkt (**...**) ja seejärel valige käsk Lisa **kill**.
1. Dialoogiaknas **Vali** moodulid valige varem loodud vestluse tükk ja seejärel valige **OK**.
1. Valige **Salvesta**, valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="proactive-chat-parameters"></a>Ennetavad vestluseparameetrid

Ennetava vestluse konfiguratsiooniparameetrite täieliku loendi leiate Commerce’i vestlusmooduli [ennetavast vestluseparameetritest](chat-proactive-chat-parameters.md).

> [!NOTE]
> Praegu ei Power Virtual Agents toetata B2C Azure Active Directory (Azure AD B2C) autentimist. See toetab ainult anonüümseid Retail Cloud Scale Unit (RCSU) kutseid, et saada toote saadavus või suhelda teiste anonüümsete API-dega. Kõned autenditud API-de autentimiseks Power Virtual Agents vestluse kaudu nõuavad selgesõnalist kliendi sisselogimist.

## <a name="additional-resources"></a>Lisaressursid

[Ärivestluse funktsioonide ülevaade](commerce-chat-overview.md)

[Ärivestlus Koos Dllchanneliga klienditeeninduse mooduli jaoks](commerce-chat-module.md)

[Ärivestluse mooduli ennetavad vestluseparameetrid](chat-proactive-chat-parameters.md)
