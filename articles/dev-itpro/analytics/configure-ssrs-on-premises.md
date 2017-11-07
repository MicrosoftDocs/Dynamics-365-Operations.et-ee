---
title: SQL Serveri aruandlusteenuste konfigureerimine kohapealseks juurutamiseks
description: See teema annab teavet SQL Serveri aruandlusteenuste (SSRS) konfigureerimise kohta kohapealseks juurutuseks.
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5ee1b93b92516e14e9581c3b2fe6a2527403ae1e
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="configure-sql-server-reporting-services-for-an-on-premises-deployment"></a>SQL Serveri aruandlusteenuste konfigureerimine kohapealseks juurutamiseks

Kasutage selles teemas toodud etappe SQL Serveri aruandlusteenuste (SSRS) konfigureerimiseks oma rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (kohapealne) juurutuse puhul.

1. Avage aruandlusteenuste konfiguratsioonihalduri rakendus.
2. Jätke alles välja **Serveri nimi**, mis peaks olema praeguse seadme nimi, ning väljade **Report Server Instance**, **MSSQLSERVER** vaikeväärtus. 
3. Klõpsake käsku **Ühenda**.
   
   [![Aruandlusteenuste konfiguratsiooni ühendus](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)
   
4. Klõpsake vahekaarti **Teenusekonto** ja kontrollige, kas sätted vastavad järgmisele joonisele.

    [![Vahekaart Teenusekonto](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)
    
5. Klõpsake vahekaarti **Veebiteenuse URL** ja kontrollige, kas sätted vastavad järgmisele joonisele. 

    [![Vahekaart Veebiteenuse URL](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png) 
    
6. Klõpsake vahekaarti **Andmebaas** ning kontrollige, kas **Andmebaasi nimi** ja **Identimisteabe sätted** vastavad järgmisele joonisele. **Märkus.** Peate looma uue andmebaasi. Selleks klõpsake nuppu **Muuda andmebaasi** ja kontrollige, kas uue andmebaasi nimi on **DynamicsAxReportServer**.

    [![vahekaart andmebaas](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)
    
7. Klõpsake vahekaarti **Veebiportaali URL** ja kontrollige, kas sätted vastavad järgmisele joonisele. **Märkus.** Portaali loomiseks ja õigesti konfigureerimiseks peate klõpsama käsku **Rakenda**.

    [![vahekaart veebiportaali url](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)
    
  Kui portaal on konfigureeritud, vastab vahekaart **Veebiportaal** järgmisele joonisele.
    [![vahekaart veebiportaal](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)
    
8. Klõpsake aruannete URL-i, et kuvada SQL Serveri aruandlusteenuste veebiportaal. 
9.  Kui olete portaalis, looge uus kaust nimega **Dynamics**.

    [![kaust dynamics](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)
    
10. Klõpsake lehel **Aruandlusteenuste konfiguratsioonihaldur** vahekaarti **Meilisätted** ja kontrollige, kas sätted vastavad järgmisele joonisele.

    [![vahekaart meilisätted](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)
    
11. Klõpsake vahekaarti **Täitmiskonto** ja kontrollige, kas sätted vastavad järgmisele joonisele.

    [![vahekaart täitmiskonto](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)
    
  Ärge muutke vahekaardi **Krüptimisvõtmed** vaikesätteid. [![krüptimisvõtmete vahekaart](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)
    
12. Klõpsake vahekaarti **Tellimuse sätted** ja kontrollige, kas sätted vastavad järgmisele joonisele.

    [![vahekaart tellimuse sätted](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)
    
  Ärge muutke vahekaardi **Eskaleeritud juurutus** vaikesätteid. [![eskaleeritud juurutuse vahekaart](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)
    
  Ärge muutke vahekaardi **Power BI integratsioon** vaikesätteid. [![power bi integratsiooni vahekaart](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png) 
    
13. Klõpsake akna **Aruandlusteenuste konfiguratsioonihaldur** sulgemiseks nuppu **Välju**.

    [![aruandlusteenuste konfiguratsioonihalduri sulgemine](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)
    


