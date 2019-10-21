---
title: RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine
description: Selles teemas toodud juhised selgitavad, kuidas kasutaja saab luua uue elektroonilise aruandluse (ER) konfiguratsiooni, mis sisaldab rakenduse metaandmeid, et kujundada elektroonilise aruandluse mudelivastenduse konfiguratsioone teenuses Regulatory configuration service (RCS).
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3a33eefca98e14ed0435f8f1a7a9f90a69498ee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182159"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a><span data-ttu-id="30267-103">RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="30267-103">Prepare application metadata to be used in RCS</span></span>
[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="30267-104">Järgnevad juhised selgitavad, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis olev kasutaja saab luua uue elektroonilise aruandluse (ER) konfiguratsiooni, mis sisaldab rakenduse metaandmeid, et kujundada elektroonilise aruandluse mudelivastenduse konfiguratsioone teenuses Regulatory configuration service (RCS).</span><span class="sxs-lookup"><span data-stu-id="30267-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains application metadata for designing ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="30267-105">Seda konfiguratsiooni kasutatakse elektroonilise mudelivastenduse näite konfiguratsiooni kujundamiseks väliskaubanduse kannetele juurdepääsemiseks.</span><span class="sxs-lookup"><span data-stu-id="30267-105">This configuration will be used for designing a sample ER model mapping configuration to access foreign trade transactions.</span></span> <span data-ttu-id="30267-106">Selles näites loote konfiguratsiooni näidisettevõttele Litware, Inc. Neid etappe saab teha mis tahes ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="30267-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company.</span></span> <span data-ttu-id="30267-107">Etappide lõpuleviimiseks, peate esmalt läbima etapid teemas [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="30267-107">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="30267-108">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="30267-108">Prerequisites</span></span>
1.  <span data-ttu-id="30267-109">Avage **Organisatsiooni haldamine** > **Tööruumid** > **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="30267-109">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2.  <span data-ttu-id="30267-110">Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja märgitud kui **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="30267-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="30267-111">Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md) toodud juhised.</span><span class="sxs-lookup"><span data-stu-id="30267-111">If you don’t see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3.  <span data-ttu-id="30267-112">Klõpsake valikut **Metaandmete konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="30267-112">Click **Metadata configurations**.</span></span> 
4.  <span data-ttu-id="30267-113">Oletame, et RCS-i kasutatakse rakenduse Finance and Operation ER-lahenduse kujundamiseks, mis loob elektroonilisi dokumente, mis sisaldavad väliskaubanduse äritegevuse domeeni teavet.</span><span class="sxs-lookup"><span data-stu-id="30267-113">Assume that RCS will be used to design an ER solution for a Finance and Operation application that will generate electronic documents that contain information from foreign trade business domain.</span></span> <span data-ttu-id="30267-114">ER-i andmemudeli ja nõutavate andmete allikate vahelise vastendamise määramiseks peab meil RCS-is olema ligipääs rakenduse Finance and Operation metaandmetele.</span><span class="sxs-lookup"><span data-stu-id="30267-114">To specify the mapping between ER data model and sources of required data, in RCS we need to have access to metadata of the Finance and Operation application.</span></span> <span data-ttu-id="30267-115">Seega konfigureerime ER-lahenduse projekteerimise osana uue ER-i metaandmete konfiguratsiooni, mis sisaldab kõiki metaandmeid, mis on valitud äridomeeni ER-aruannete genereerimiseks praegu nõutavad.</span><span class="sxs-lookup"><span data-stu-id="30267-115">Therefore, as part of designing ER solution we configure a new ER metadata configuration containing all metadata that is currently required for generation ER reports for selected business domain.</span></span> 

## <a name="add-metadata-configuration"></a><span data-ttu-id="30267-116">Metaandmete konfigureerimise lisamine</span><span class="sxs-lookup"><span data-stu-id="30267-116">Add metadata configuration</span></span> 
1.  <span data-ttu-id="30267-117">Klõpsake valikut **Loo konfiguratsioon**, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="30267-117">Click **Create configuration** to open the drop dialog.</span></span> 
2.  <span data-ttu-id="30267-118">Sisestage väljale **Nimi** "Väliskaubanduse metaandmed".</span><span class="sxs-lookup"><span data-stu-id="30267-118">In the **Name** field, type 'Foreign trade metadata'.</span></span> 
3.  <span data-ttu-id="30267-119">Klõpsake **Loo konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="30267-119">Click **Create configuration**.</span></span> 
4.  <span data-ttu-id="30267-120">Klõpsake valikut **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="30267-120">Click **Designer**.</span></span> 
5.  <span data-ttu-id="30267-121">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="30267-121">Click **Add**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="30267-122">Saate valida kogu rakenduse või valitud mudeli või valitud mooduli metaandmed.</span><span class="sxs-lookup"><span data-stu-id="30267-122">You can select all metadata for the entire application or selected models or selected modules.</span></span> <span data-ttu-id="30267-123">Arvestage, et sel juhul lisatakse automaatselt järgmised metaandmed: kirjete tabelid, loetelud ja laiendatud andmetüübid.</span><span class="sxs-lookup"><span data-stu-id="30267-123">Be aware that in this case the following metadata will be automatically added: tables of records, enumerations, and extended data types.</span></span> <span data-ttu-id="30267-124">Kui on vaja täiendavaid metaandmete tüüpe, tuleb need lisada käsitsi.</span><span class="sxs-lookup"><span data-stu-id="30267-124">When additional types of metadata are needed, they must be added manually.</span></span> 
 
<span data-ttu-id="30267-125">Meil on mõned väliskaubanduse kannetega seotud metaandmed, valides metaandmete üksused käsitsi.</span><span class="sxs-lookup"><span data-stu-id="30267-125">We have some foreign trade transactions related metadata by selecting metadata items manually.</span></span> 
  
6.  <span data-ttu-id="30267-126">Klõpsake suvandit **Andmeallika lisamine**.</span><span class="sxs-lookup"><span data-stu-id="30267-126">Click **Add data source**.</span></span> 
7.  <span data-ttu-id="30267-127">Klõpsake suvandit **Tabeli kirjed**.</span><span class="sxs-lookup"><span data-stu-id="30267-127">Click **Table records**.</span></span> 
8.  <span data-ttu-id="30267-128">Kasutage kiirfiltrit, et filtreerida **Nime** välja väärtusega "Intrastat".</span><span class="sxs-lookup"><span data-stu-id="30267-128">Use the Quick Filter to filter on the **Name** field with a value of 'Intrastat'.</span></span> 
9.  <span data-ttu-id="30267-129">Valige tabeli kirje **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="30267-129">Select the **Intrastat** table record.</span></span> 
10. <span data-ttu-id="30267-130">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="30267-130">Click **OK**.</span></span>
  
<span data-ttu-id="30267-131">Lisasime Intrastati kirjetabeli metaandmete teabe.</span><span class="sxs-lookup"><span data-stu-id="30267-131">We added metadata information about the Intrastat table of records.</span></span> 
  
11. <span data-ttu-id="30267-132">Laiendage puul valikut **Table records Intrastat**\>**Relations**.</span><span class="sxs-lookup"><span data-stu-id="30267-132">In the tree, expand **Table records Intrastat**\>**Relations**.</span></span> 
12. <span data-ttu-id="30267-133">Tehke puul valik **Table records Intrastat**\>**Relations\IntrastatCommodity (Table records EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="30267-133">In the tree, select **Table records Intrastat**\>**Relations\IntrastatCommodity (Table records EcoResCategory)**.</span></span>   
13. <span data-ttu-id="30267-134">Klõpsake käsku **Lisa metaandmeid**.</span><span class="sxs-lookup"><span data-stu-id="30267-134">Click **Add metadata**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="30267-135">Valitud kirjetabeli nõutavate seoste metaandmed tuleb lisada käsitsi.</span><span class="sxs-lookup"><span data-stu-id="30267-135">Metadata about required relations for selected table of records must be added manually.</span></span> 
  
16. <span data-ttu-id="30267-136">Klõpsake suvandit **Andmeallika lisamine**.</span><span class="sxs-lookup"><span data-stu-id="30267-136">Click **Add data source**.</span></span> 
17. <span data-ttu-id="30267-137">Klõpsake valikut **Loetelu**.</span><span class="sxs-lookup"><span data-stu-id="30267-137">Click **Enumeration**.</span></span> 
18. <span data-ttu-id="30267-138">Kasutage kiirfiltrit, et filtreerida **Nime** välja väärtusega "IntrastatDirection".</span><span class="sxs-lookup"><span data-stu-id="30267-138">Use the Quick Filter to filter on the **Name** field with a value of 'IntrastatDirection'.</span></span> 
19. <span data-ttu-id="30267-139">Valige **IntrastatDirectioni loetelu** kirje.</span><span class="sxs-lookup"><span data-stu-id="30267-139">Select the **IntrastatDirection enumeration** record.</span></span> 
20. <span data-ttu-id="30267-140">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="30267-140">Click **OK**.</span></span> 
21. <span data-ttu-id="30267-141">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="30267-141">Click **Save**.</span></span>  
22. <span data-ttu-id="30267-142">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="30267-142">Close the page.</span></span> 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a><span data-ttu-id="30267-143">Täitke metaandmete konfiguratsiooni mustandversioon</span><span class="sxs-lookup"><span data-stu-id="30267-143">Complete the draft version of metadata configuration</span></span>
1.  <span data-ttu-id="30267-144">Klõpsake valikut **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="30267-144">Click **Change status**.</span></span> 
2.  <span data-ttu-id="30267-145">Klõpsake valikut **Vii lõpule**.</span><span class="sxs-lookup"><span data-stu-id="30267-145">Click **Complete**.</span></span> 
3.  <span data-ttu-id="30267-146">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="30267-146">Click **OK**.</span></span> 
4.  <span data-ttu-id="30267-147">Valige lõpule viidud versioon **1**.</span><span class="sxs-lookup"><span data-stu-id="30267-147">Select the completed version **1**.</span></span> 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a><span data-ttu-id="30267-148">Eksportige metaandmete konfiguratsiooni lõpule viidud versioon rakendusest XML-failina</span><span class="sxs-lookup"><span data-stu-id="30267-148">Export the completed version of metadata configuration from application as XML file</span></span>
1.  <span data-ttu-id="30267-149">Klõpsake valikut **Vahetus**.</span><span class="sxs-lookup"><span data-stu-id="30267-149">Click **Exchange**.</span></span> 
2.  <span data-ttu-id="30267-150">Klõpsake **Ekspordi XML-failina**.</span><span class="sxs-lookup"><span data-stu-id="30267-150">Click **Export as XML file**.</span></span> 
3.  <span data-ttu-id="30267-151">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="30267-151">Click **OK**.</span></span> 
    
<span data-ttu-id="30267-152">Loodud ER-i metaandmete konfiguratsioon salvestati XML-failina, mida saab importida RCS-i ja kasutada väliskaubanduse äritegevuse domeeni metaandmete teabe allikana.</span><span class="sxs-lookup"><span data-stu-id="30267-152">The created ER metadata configuration has been saved as XML file that can be imported to RCS and used as the source of information about metadata for the foreign trade business domain.</span></span> <span data-ttu-id="30267-153">Selle teabe põhjal saame määratleda vastendamise rakenduse metaandmete ja ER-i andmemudeli vahel.</span><span class="sxs-lookup"><span data-stu-id="30267-153">Based on this information, we can specify the mapping between application metadata and ER data model.</span></span>
