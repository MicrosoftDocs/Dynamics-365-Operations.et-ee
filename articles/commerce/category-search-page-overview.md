---
title: Kategooria vaikesihtlehe ja otsingutulemuste lehe ülevaade
description: See artikkel annab ülevaate vaikekategooria leheküljest ja otsingutulemuste lehest Dynamics 365 Commerce.
author: ashishmsft
ms.date: 06/30/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.assetid: ''
ms.openlocfilehash: 1f2e4eb8825dd690f926f7f0bdfc39f1eb5fb83c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276369"
---
# <a name="default-category-landing-page-and-search-results-page-overview"></a>Kategooria vaikesihtlehe ja otsingutulemuste lehe ülevaade

[!include [banner](includes/banner.md)]

See artikkel annab e-Commerce’i vaikimisi kategooria lehekülje ja Microsoft Dynamics 365 Commerce otsingutulemuste lehe ülevaate.

## <a name="default-category-landing-page"></a>Kategooria vaikesihtleht

Kategooria vaikesihtleht on leht, kuhu veebisaidi kasutajad tavaliselt navigeerimishierarhias kategooria valimisel viiakse. Kategooria leht võimaldab teil sirvida ja saate lisaks sortida ning viimistleda kategoriseeritud tooteid.

![Kategooria vaikesihtleht.](./media/SimpleCategoryLandingDressCategory.png)

Lehe ülaosas on päis, mis näitab kõiki tootekategooriaid ja teisi lehti, mida tootejuht on kategoriseerinud. Konfiguratsioon tehakse kanali navigeerimishierarhia konfiguratsiooni osana. Lehe allosas on jalus, mis sisaldab kiirlinke erinevatele artiklitele, mis võivad ostukotta huvituda.

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

- **Täpsemaid sortimissuvandeid** kasutavad veebisaidi omad nutikate kriteeriumide alusel toodete sortimiseks. Tootesoovituste [lubamisega](product-recommendations.md) on saadaval järgmised sortimisvalikud. Lisateabe saamiseks vt tootesoovituste [tüüpe](product-recommendations.md#types-of-product-recommendations).

    - Uus
    - Parim müük
    - Populaarsed

- **Lehejaotus** võimaldab veebisaidi külastajatel liikuda ühelt kategoriseeritud toodete tulemuste lehelt teisele lehele.
- **Koguarv** näitab kategoorias määratletud toodete koguarvu.

## <a name="enrich-a-category-landing-page"></a>Kategooria sihtlehe rikastamine

Kui soovite, et kategooria sihtlehel oleks kindla kategooria jaoks palju kohandatum kogemus, saate selle kategooria jaoks nö rikastada kategooria sihtlehte. Näiteks saate ostja tähelepanu tõmbamiseks lisada turundusvideo ja mõne kategooria loo jutustamise. Lisateavet vaadake teemast [Kategooria sihtlehe rikastamine](enrich-category-page.md).

![Rikastatud kategooria sihtleht.](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a>Automaatse soovitamise ja otsingutulemuste lehed

Veebisaidi kasutajad saavad saiti uurida kas minnes kategooriasse navigeerimishierarhiast või sisestades otsinguväljale otsingusõna.

Kohe, kui kasutajad hakkavad otsinguväljale tippima, kogevad nad kõikehõlmavat automaatse soovitamise funktsiooni, mis soovitab otsingusõnu.

Siin on mõned soovituste tüübid, mis võidakse kuvada.

- **Märksõnu** kasutatakse kaupade otsimiseks kõikide kanalile sorditud toodete seast.
- **Tooted** pakuvad otseseid linke toote üksikasjade lehele.
- **Määratletud kategooria otsingusoovitused** loetlevad erinevad kategooriad ja võimaldavad kasutajatel otsida märksõna kindlas kategoorias.

![Kõikehõlmavad automaatsed soovitused.](./media/ImmersiveAutoSuggestUX.png)

Kui kasutajad valivad ühe märksõna või määratletud kategooria otsingusoovituse või kui nende sisestatud otsingusõnale puuduvad soovitused, suunatakse need ümber otsingutulemuste lehele. Seejärel saavad kasutajad soovitud kauba leidmiseks otsingutulemuste loendit sirvida, sortida ja täpsustada.

![Sihtkoha otsing.](./media/SearchLanding.png)

Otsingutulemuste lehe jaoks on olulised järgmised komponendid.

- **Tootepaigutuse paanid** näitavad kasutaja otsingu tooteid. Vaikimisi sorditakse need paanid kasutaja otsingu pilvepõhise otsingu asjakohasuse skoori alusel.
- **Piiritlusatribuudid ja valiku kokkuvõte** on filtrid, mis esitavad arve ja mida saab kasutada kaupade täpsustamiseks. Tootejuht konfigureerib need nn kanali kategooriate ja toote atribuutide metaandmete konfiguratsiooni osana.
- **Standardseid sortimissuvandeid** kasutavad veebisaidi aadressid toodete sortimiseks. Vaikimisi on saadaval järgmised sortimissuvandid.

    - Hind – madalast kõrgeni
    - Hind – kõrgest madalani
    - Toote nimi – \[A–Z\]
    - Toote nimi – \[Z–A\]
    - Hinnangud – madalast kõrgeni
    - Hinnangud – kõrgest madalani
    - Vaikimisi 
    
    > [!NOTE]
    > Kui **display-järjekorra** väärtused on toodetele määratletud navigeerimise müügitellimuses, takse kategoorialehel vaikimisi sordides Display-järjestuses määratletud **väärtused**. Muul juhul toimub sortimine tootenumbri **alusel**.)
    
- **Täpsemaid sortimissuvandeid** kasutavad veebisaidi omad nutikate kriteeriumide alusel toodete sortimiseks. Tootesoovituste [lubamisega](product-recommendations.md) on saadaval järgmised sortimisvalikud. Lisateabe saamiseks vt tootesoovituste [tüüpe](product-recommendations.md#types-of-product-recommendations).

    - Uus
    - Parim müük
    - Populaarsed

- **Lehejaotus** võimaldab veebisaidi külastajatel liikuda ühelt kategoriseeritud toodete tulemuste lehelt teisele lehele.
- **Koguarv** näitab kategoorias määratletud ja otsingukriteeriumitega ühtivate toodete koguarvu.

>[!NOTE]
>Need pilvepõhised otsinguvõimalused on saadaval alates versioonist 10.0.8. Veenduge, et jaotises **Kaubanduse parameetrid > konfiguratsiooniparameetrid** on kirje ProductSearch.UseAzureSearch väärtuseks määratud „tõene”. 
![Pilvepõhise otsingu konfiguratsiooniparameetrid.](./media/CloudPoweredSearchConfigurationParameters.png)

>Täiustatud sortimisvalikute (nt uus, parimate müük ja [trendid](product-recommendations.md)) kasutamiseks tuleb teil lubada tootesoovitused oma keskkonnas. Täpsemad sortimissuvandid on saadaval koos Commerce SDK versiooniga 9.35+ ja Commerce version 10.0.20.

## <a name="additional-resources"></a>Lisaressursid

[Pilvepõhise otsingu ülevaade](cloud-powered-search-overview.md)

[Avalehe ülevaade](quick-tour-home-page.md)

[Toote üksikasjade lehe ülevaade](quick-tour-pdp.md)

[Ostukorvi ja väljaregistreerimise ülevaade](quick-tour-cart-checkout.md)

[Kontohalduse lehtede ülevaade](quick-tour-account-management.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
