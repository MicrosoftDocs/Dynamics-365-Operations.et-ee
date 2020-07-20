---
title: Kategooria vaikesihtlehe ja otsingutulemuste lehe ülevaade
description: Selles teemas antakse rakenduse Dynamics 365 Commerce kategooria vaikesihtlehe ja otsingutulemuste lehe ülevaade.
author: ashishmsft
manager: annbe
ms.date: 06/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e85449c10fa4a768a144ce423a77bd1fc2c94352
ms.sourcegitcommit: ce397c2759f642c595e30fef58a770b50360b2bd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/01/2020
ms.locfileid: "3527464"
---
# <a name="default-category-landing-page-and-search-results-page-overview"></a>Kategooria vaikesihtlehe ja otsingutulemuste lehe ülevaade

[!include [banner](includes/banner.md)]

Selles teemas antakse rakenduse Microsoft Dynamics 365 Commerce e-kaubanduse kategooria vaikesihtlehe ja otsingutulemuste lehe ülevaade.

## <a name="default-category-landing-page"></a>Kategooria vaikesihtleht

Kategooria vaikesihtleht on leht, kuhu veebisaidi kasutajad tavaliselt navigeerimishierarhias kategooria valimisel viiakse. Kategooria leht võimaldab teil sirvida ja saate lisaks sortida ning viimistleda kategoriseeritud tooteid.

![Kategooria vaikesihtleht](./media/SimpleCategoryLandingDressCategory.png)

Lehe ülaosas on päis, mis näitab kõiki tootekategooriaid ja teisi lehti, mida tootejuht on kategoriseerinud. Konfiguratsioon tehakse kanali navigeerimishierarhia konfiguratsiooni osana. Lehe allosas on jalus, mis sisaldab kiirlinke erinevatele teemadele, millest klient võib olla huvitatud.

Kategooria jaoks on olulised järgmised komponendid.

- **Tootepaigutuse paanid** näitavad tooteid, mille tootejuht on määratlenud kategoorias navigatsioonihierarhia konfiguratsiooni osana.
- **Piiritlusatribuudid ja valiku kokkuvõte** on filtrid, mis esitavad arve ja mida saab kasutada kaupade täpsustamiseks. Tootejuht konfigureerib need kanali kategooriate ja toote atribuutidega seotud metaandmete konfiguratsiooni osana.
- **Sortimissuvandeid** kasutavad veebisaidi külastajad toodete sortimiseks. Vaikimisi on saadaval järgmised sortimissuvandid.

    - Hind – madalast kõrgeni
    - Hind – kõrgest madalani
    - Toote nimi – \[A–Z\]
    - Toote nimi – \[Z–A\]
    - Hinnangud – madalast kõrgeni
    - Hinnangud – kõrgest madalani

- **Lehejaotus** võimaldab veebisaidi külastajatel liikuda ühelt kategoriseeritud toodete tulemuste lehelt teisele lehele.
- **Koguarv** näitab kategoorias määratletud toodete koguarvu.

## <a name="enrich-a-category-landing-page"></a>Kategooria sihtlehe rikastamine

Kui soovite, et kategooria sihtlehel oleks kindla kategooria jaoks palju kohandatum kogemus, saate selle kategooria jaoks nö rikastada kategooria sihtlehte. Näiteks saate ostja tähelepanu tõmbamiseks lisada turundusvideo ja mõne kategooria loo jutustamise. Lisateavet vaadake teemast [Kategooria sihtlehe rikastamine](enrich-category-page.md).

![Rikastatud kategooria sihtleht](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a>Automaatse soovitamise ja otsingutulemuste lehed

Veebisaidi kasutajad saavad saiti uurida kas minnes kategooriasse navigeerimishierarhiast või sisestades otsinguväljale otsingusõna.

Kohe, kui kasutajad hakkavad otsinguväljale tippima, kogevad nad kõikehõlmavat automaatse soovitamise funktsiooni, mis soovitab otsingusõnu.

Siin on mõned soovituste tüübid, mis võidakse kuvada.

- **Märksõnu** kasutatakse kaupade otsimiseks kõikide kanalile sorditud toodete seast.
- **Tooted** pakuvad otseseid linke toote üksikasjade lehele.
- **Määratletud kategooria otsingusoovitused** loetlevad erinevad kategooriad ja võimaldavad kasutajatel otsida märksõna kindlas kategoorias.

![Kõikehõlmavad automaatsed soovitused](./media/ImmersiveAutoSuggestUX.png)

Kui kasutajad valivad ühe märksõna või määratletud kategooria otsingusoovituse või kui nende sisestatud otsingusõnale puuduvad soovitused, suunatakse need ümber otsingutulemuste lehele. Seejärel saavad kasutajad soovitud kauba leidmiseks otsingutulemuste loendit sirvida, sortida ja täpsustada.

![Sihtkoha otsing](./media/SearchLanding.png)

Otsingutulemuste lehe jaoks on olulised järgmised komponendid.

- **Tootepaigutuse paanid** näitavad kasutaja otsingu tooteid. Vaikimisi sorditakse need paanid kasutaja otsingu pilvepõhise otsingu asjakohasuse skoori alusel.
- **Piiritlusatribuudid ja valiku kokkuvõte** on filtrid, mis esitavad arve ja mida saab kasutada kaupade täpsustamiseks. Tootejuht konfigureerib need nn kanali kategooriate ja toote atribuutide metaandmete konfiguratsiooni osana.
- **Sortimissuvandeid** kasutavad veebisaidi külastajad toodete sortimiseks. Vaikimisi on saadaval järgmised sortimissuvandid.

    - Hind – madalast kõrgeni
    - Hind – kõrgest madalani
    - Toote nimi – \[A–Z\]
    - Toote nimi – \[Z–A\]
    - Hinnangud – madalast kõrgeni
    - Hinnangud – kõrgest madalani
    - Vaikimisi

- **Lehejaotus** võimaldab veebisaidi külastajatel liikuda ühelt kategoriseeritud toodete tulemuste lehelt teisele lehele.
- **Koguarv** näitab kategoorias määratletud ja otsingukriteeriumitega ühtivate toodete koguarvu.

>[!NOTE]
>Need pilvepõhised otsinguvõimalused on saadaval alates versioonist 10.0.8. Veenduge, et jaotises **Kaubanduse parameetrid > konfiguratsiooniparameetrid** on kirje ProductSearch.UseAzureSearch väärtuseks määratud „tõene”. 
![Pilvepõhise otsingu konfiguratsiooniparameetrid](./media/CloudPoweredSearchConfigurationParameters.png)

## <a name="additional-resources"></a>Lisaressursid

[Pilvepõhise otsingu ülevaade](cloud-powered-search-overview.md)

[Avalehe ülevaade](quick-tour-home-page.md)

[Toote üksikasjade lehe ülevaade](quick-tour-pdp.md)

[Ostukorvi ja väljaregistreerimise ülevaade](quick-tour-cart-checkout.md)

[Kontohalduse lehtede ülevaade](quick-tour-account-management.md)

