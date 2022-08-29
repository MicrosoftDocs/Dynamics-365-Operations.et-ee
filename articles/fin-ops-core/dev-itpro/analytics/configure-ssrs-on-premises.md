---
title: SQL Serveri aruandlusteenuste konfigureerimine kohapealseteks juurutamisteks
description: See artikkel annab teavet SQL Serveri aruandlusteenuste (SSRS) konfigureerimise kohta ettevõttepoolseks juurutamiseks.
author: PeterRFriis
ms.date: 06/23/2017
ms.topic: article
ms.prod: dynamics-365
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.custom: 55651
ms.assetid: ''
ms.service: ''
ms.openlocfilehash: 9acb681ce07c3a7da82a630c7a87a4271a411b51
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275408"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a>SQL Serveri aruandlusteenuste konfigureerimine kohapealseteks juurutamisteks

[!include [banner](../includes/banner.md)]

Kasutage selle artikli samme SQL Serveri aruandlusteenuste (SSRS) konfigureerimiseks juurutamiseks Microsoft Dynamics 365 Finance + Operations (on-premises).

1. Avage aruandlusteenuste konfiguratsioonihalduri rakendus.
2. Jätke alles välja **Serveri nimi**, mis peaks olema praeguse seadme nimi, ning väljade **Report Server Instance**, **MSSQLSERVER** vaikeväärtus.
3. Klõpsake käsku **Ühenda**.

    [![Aruandlusteenuste konfiguratsiooni ühendus.](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)

4. Klõpsake vahekaarti **Teenusekonto** ja kontrollige, kas sätted vastavad järgmisele joonisele.

    [![Vahekaart Teenuse konto.](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)

5. Klõpsake vahekaarti **Veebiteenuse URL** ja kontrollige, kas sätted vastavad järgmisele joonisele.

    [![Vahekaart Veebiteenuse URL.](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)

6. Klõpsake vahekaarti **Andmebaas** ning kontrollige, kas **Andmebaasi nimi** ja **Identimisteabe sätted** vastavad järgmisele joonisele.

    > [!NOTE]
    > Peate looma uue andmebaasi. Selleks klõpsake nuppu **Muuda andmebaasi** ja kontrollige, kas uue andmebaasi nimi on **DynamicsAxReportServer**.

    [![vahekaart andmebaas.](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)

7. Klõpsake vahekaarti **Veebiportaali URL** ja kontrollige, kas sätted vastavad järgmisele joonisele.

    > [!NOTE]
    > Portaali loomiseks ja õigesti konfigureerimiseks peate klõpsama käsku **Rakenda**.

    [![vahekaart veebiportaali url.](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)

    Kui portaal on konfigureeritud, vastab vahekaart **Veebiportaal** järgmisele joonisele.

    [![vahekaart veebi portaal.](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)

8. Klõpsake aruannete URL-i, et kuvada SQL Serveri aruandlusteenuste veebiportaal.
9. Kui olete portaalis, looge uus kaust nimega **Dynamics**.

    [![dünaamika kaust.](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)

10. Klõpsake lehel **Aruandlusteenuste konfiguratsioonihaldur** vahekaarti **Meilisätted** ja kontrollige, kas sätted vastavad järgmisele joonisele.

    [![vahekaart meilisätted.](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)

11. Klõpsake vahekaarti **Täitmiskonto** ja kontrollige, kas sätted vastavad järgmisele joonisele.

    [![vahekaart täitmis konto.](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)

    Ärge muutke vahekaardi **Krüptimisvõtmed** vaikesätteid.

    [![vahekaart krüptimis sätted.](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)

12. Klõpsake vahekaarti **Tellimuse sätted** ja kontrollige, kas sätted vastavad järgmisele joonisele.

    [![vahekaart tellimuse sätted.](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)

    Ärge muutke vahekaardi **Eskaleeritud juurutus** vaikesätteid.

    [![vahekaart eskaleeritud juurutus.](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)

    Ärge muutke vahekaardi **Power BI integratsioon vaikesätteid**.

    [![vahekaart power bi integratsioon.](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)

13. Klõpsake akna **Aruandlusteenuste konfiguratsioonihaldur** sulgemiseks nuppu **Välju**.

    [![aruandlusteenuste konfiguratsioonihalduri sulgemine.](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
