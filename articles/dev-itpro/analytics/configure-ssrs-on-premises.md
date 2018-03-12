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
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 7be3e9970e2599c159e7c9d414b54876d0116350
ms.openlocfilehash: 2b5abc98f5788c5091e5be61688cfd0d4076a510
ms.contentlocale: et-ee
ms.lasthandoff: 03/09/2018

---
# <a name="configure-sql-server-reporting-services-for-an-on-premises-deployment"></a><span data-ttu-id="b0203-103">SQL Serveri aruandlusteenuste konfigureerimine kohapealseks juurutamiseks</span><span class="sxs-lookup"><span data-stu-id="b0203-103">Configure SQL Server Reporting Services for an on-premises deployment</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b0203-104">Kasutage selles teemas toodud etappe SQL Serveri aruandlusteenuste (SSRS) konfigureerimiseks oma rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (kohapealne) juurutuse puhul.</span><span class="sxs-lookup"><span data-stu-id="b0203-104">Use the steps in this topic to configure SQL Server Reporting Services (SSRS) for your Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises) deployment.</span></span>

1. <span data-ttu-id="b0203-105">Avage aruandlusteenuste konfiguratsioonihalduri rakendus.</span><span class="sxs-lookup"><span data-stu-id="b0203-105">Open the Reporting Services Configuration Manager application.</span></span>
2. <span data-ttu-id="b0203-106">Jätke alles välja **Serveri nimi**, mis peaks olema praeguse seadme nimi, ning väljade **Report Server Instance**, **MSSQLSERVER** vaikeväärtus.</span><span class="sxs-lookup"><span data-stu-id="b0203-106">Leave the default **Server name**, which should be the name of the current machine, and the **Report Server Instance**, **MSSQLSERVER**.</span></span> 
3. <span data-ttu-id="b0203-107">Klõpsake käsku **Ühenda**.</span><span class="sxs-lookup"><span data-stu-id="b0203-107">Click **Connect**.</span></span>
   
   <span data-ttu-id="b0203-108">[![Aruandlusteenuste konfiguratsiooni ühendus](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span><span class="sxs-lookup"><span data-stu-id="b0203-108">[![Reporting services configuration connection](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span></span>
   
4. <span data-ttu-id="b0203-109">Klõpsake vahekaarti **Teenusekonto** ja kontrollige, kas sätted vastavad järgmisele joonisele.</span><span class="sxs-lookup"><span data-stu-id="b0203-109">Click the **Service Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="b0203-110">[![Vahekaart Teenusekonto](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span><span class="sxs-lookup"><span data-stu-id="b0203-110">[![Service account tab](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span></span>
    
5. <span data-ttu-id="b0203-111">Klõpsake vahekaarti **Veebiteenuse URL** ja kontrollige, kas sätted vastavad järgmisele joonisele.</span><span class="sxs-lookup"><span data-stu-id="b0203-111">Click the **Web Service URL** tab and verify that the settings match the following graphic.</span></span> 

    <span data-ttu-id="b0203-112">[![Vahekaart Veebiteenuse URL](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span><span class="sxs-lookup"><span data-stu-id="b0203-112">[![Web service URL tab](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span></span> 
    
6. <span data-ttu-id="b0203-113">Klõpsake vahekaarti **Andmebaas** ning kontrollige, kas **Andmebaasi nimi** ja **Identimisteabe sätted** vastavad järgmisele joonisele.</span><span class="sxs-lookup"><span data-stu-id="b0203-113">Click the **Database** tab and verify that the **Database Name** and **Credential settings** match the following graphic.</span></span> <span data-ttu-id="b0203-114">**Märkus.** Peate looma uue andmebaasi.</span><span class="sxs-lookup"><span data-stu-id="b0203-114">**Note:** You will need to create a new database.</span></span> <span data-ttu-id="b0203-115">Selleks klõpsake nuppu **Muuda andmebaasi** ja kontrollige, kas uue andmebaasi nimi on **DynamicsAxReportServer**.</span><span class="sxs-lookup"><span data-stu-id="b0203-115">To do this, click **Change Database**, and then verify that the new database name is: **DynamicsAxReportServer**.</span></span>

    <span data-ttu-id="b0203-116">[![vahekaart andmebaas](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span><span class="sxs-lookup"><span data-stu-id="b0203-116">[![database tab](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span></span>
    
7. <span data-ttu-id="b0203-117">Klõpsake vahekaarti **Veebiportaali URL** ja kontrollige, kas sätted vastavad järgmisele joonisele.</span><span class="sxs-lookup"><span data-stu-id="b0203-117">Click the **Web Portal URL** tab and verify that the settings match the following graphic.</span></span> <span data-ttu-id="b0203-118">**Märkus.** Portaali loomiseks ja õigesti konfigureerimiseks peate klõpsama käsku **Rakenda**.</span><span class="sxs-lookup"><span data-stu-id="b0203-118">**Note:** You must click **Apply** to create and properly configure the Portal.</span></span>

    <span data-ttu-id="b0203-119">[![vahekaart veebiportaali url](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span><span class="sxs-lookup"><span data-stu-id="b0203-119">[![web portal url tab](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span></span>
    
  <span data-ttu-id="b0203-120">Kui portaal on konfigureeritud, vastab vahekaart **Veebiportaal** järgmisele joonisele.</span><span class="sxs-lookup"><span data-stu-id="b0203-120">After the Portal is configured, the **Web Portal** tab will match the following graphic.</span></span>
    <span data-ttu-id="b0203-121">[![vahekaart veebiportaal](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span><span class="sxs-lookup"><span data-stu-id="b0203-121">[![web portal tab](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span></span>
    
8. <span data-ttu-id="b0203-122">Klõpsake aruannete URL-i, et kuvada SQL Serveri aruandlusteenuste veebiportaal.</span><span class="sxs-lookup"><span data-stu-id="b0203-122">Click the reports URL to view the SQL Server Reporting Services web portal.</span></span> 
9.  <span data-ttu-id="b0203-123">Kui olete portaalis, looge uus kaust nimega **Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="b0203-123">When you are in the portal, create a new folder named **Dynamics**.</span></span>

    <span data-ttu-id="b0203-124">[![kaust dynamics](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span><span class="sxs-lookup"><span data-stu-id="b0203-124">[![dynamics folder](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span></span>
    
10. <span data-ttu-id="b0203-125">Klõpsake lehel **Aruandlusteenuste konfiguratsioonihaldur** vahekaarti **Meilisätted** ja kontrollige, kas sätted vastavad järgmisele joonisele.</span><span class="sxs-lookup"><span data-stu-id="b0203-125">In the **Reporting Services Configuration Manager**, click the **E-mail Settings** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="b0203-126">[![vahekaart meilisätted](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span><span class="sxs-lookup"><span data-stu-id="b0203-126">[![email settings tab](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span></span>
    
11. <span data-ttu-id="b0203-127">Klõpsake vahekaarti **Täitmiskonto** ja kontrollige, kas sätted vastavad järgmisele joonisele.</span><span class="sxs-lookup"><span data-stu-id="b0203-127">Click the **Execution Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="b0203-128">[![vahekaart täitmiskonto](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span><span class="sxs-lookup"><span data-stu-id="b0203-128">[![execution account tab](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span></span>
    
  <span data-ttu-id="b0203-129">Ärge muutke vahekaardi **Krüptimisvõtmed** vaikesätteid. [![krüptimisvõtmete vahekaart](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span><span class="sxs-lookup"><span data-stu-id="b0203-129">Don’t change the default settings on the **Encryption Keys** tab. [![encryption keys tab](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span></span>
    
12. <span data-ttu-id="b0203-130">Klõpsake vahekaarti **Tellimuse sätted** ja kontrollige, kas sätted vastavad järgmisele joonisele.</span><span class="sxs-lookup"><span data-stu-id="b0203-130">Click the **Subscription Settings** tab, and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="b0203-131">[![vahekaart tellimuse sätted](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span><span class="sxs-lookup"><span data-stu-id="b0203-131">[![subscription settings tab](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span></span>
    
  <span data-ttu-id="b0203-132">Ärge muutke vahekaardi **Eskaleeritud juurutus** vaikesätteid. [![eskaleeritud juurutuse vahekaart](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span><span class="sxs-lookup"><span data-stu-id="b0203-132">Don’t change the default settings on the **Scale-out Deployment** tab. [![scale-out deployment tab](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span></span>
    
  <span data-ttu-id="b0203-133">Ärge muutke vahekaardi **Power BI integratsioon** vaikesätteid. [![power bi integratsiooni vahekaart](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span><span class="sxs-lookup"><span data-stu-id="b0203-133">Don’t change the default settings on the **Power BI Integration** tab. [![power bi integration tab](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span></span> 
    
13. <span data-ttu-id="b0203-134">Klõpsake akna **Aruandlusteenuste konfiguratsioonihaldur** sulgemiseks nuppu **Välju**.</span><span class="sxs-lookup"><span data-stu-id="b0203-134">Click **Exit** to close the **Reporting Services Configuration Manager**.</span></span>

    <span data-ttu-id="b0203-135">[![aruandlusteenuste konfiguratsioonihalduri sulgemine](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span><span class="sxs-lookup"><span data-stu-id="b0203-135">[![close reporting services configuration manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span></span>
    


