--- 
title: "Elektroonilise aruandluse (ER) konfiguratsioonipakkuja loomine ja aktiivseks märkimine"
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua konfiguratsiooni pakkuja elektroonilise aruandluse (ER) puhul."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8392e789f546e32a00736c02eccf47d00893cc8b
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-configuration-provider-and-mark-it-as-active-for-electronic-reporting-er"></a><span data-ttu-id="ccac8-103">Elektroonilise aruandluse (ER) konfiguratsioonipakkuja loomine ja aktiivseks märkimine</span><span class="sxs-lookup"><span data-stu-id="ccac8-103">Create a configuration provider and mark it as active for electronic reporting (ER)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ccac8-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua konfiguratsiooni pakkuja elektroonilise aruandluse (ER) puhul.</span><span class="sxs-lookup"><span data-stu-id="ccac8-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="ccac8-105">Iga elektroonilise aruandluse konfiguratsioon viitab pakkujale kui konfiguratsiooni autorile.</span><span class="sxs-lookup"><span data-stu-id="ccac8-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="ccac8-106">Selles näites loote konfiguratsiooni pakkuja näidisettevõttele Litware, Inc. Neid etappe teha mis tahes ettevõttes, kuna ER-konfiguratsiooni pakkujate on kõigil ettevõtetel ühised.</span><span class="sxs-lookup"><span data-stu-id="ccac8-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="ccac8-107">Pakkuja loomine</span><span class="sxs-lookup"><span data-stu-id="ccac8-107">Create a provider</span></span>
1. <span data-ttu-id="ccac8-108">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="ccac8-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="ccac8-109">Klõpsake suvandit Konfiguratsiooni pakkujad.</span><span class="sxs-lookup"><span data-stu-id="ccac8-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="ccac8-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ccac8-110">Click New.</span></span>
    * <span data-ttu-id="ccac8-111">Pakkuja kirjel on kordumatu nimi ja URL.</span><span class="sxs-lookup"><span data-stu-id="ccac8-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="ccac8-112">Vaadake selle lehe sisu üle ja jätke see protseduur vahele, kui kirje Litware, Inc.-i (`http://www.litware.com`) kohta on juba olemas.</span><span class="sxs-lookup"><span data-stu-id="ccac8-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (`http://www.litware.com`) already exists.</span></span>  
4. <span data-ttu-id="ccac8-113">Sisestage väljale Nimi suvand Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="ccac8-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="ccac8-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="ccac8-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="ccac8-115">Sisestage internetiaadressi väljale väärtus `http://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="ccac8-115">In the Internet address field, type `http://www.litware.com`.</span></span>
6. <span data-ttu-id="ccac8-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ccac8-116">Click Save.</span></span>
7. <span data-ttu-id="ccac8-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ccac8-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="ccac8-118">Valimine aktiivse pakkujana</span><span class="sxs-lookup"><span data-stu-id="ccac8-118">Select as an active provider</span></span>
1. <span data-ttu-id="ccac8-119">Valige pakkuja Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="ccac8-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="ccac8-120">Klõpsake valikut Määra aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="ccac8-120">Click Set active.</span></span>


