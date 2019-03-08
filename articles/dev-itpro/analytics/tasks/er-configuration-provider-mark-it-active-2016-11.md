---
title: Konfiguratsiooni pakkujate loomine ja nende aktiivseks märkimine
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua konfiguratsiooni pakkuja elektroonilise aruandluse (ER) puhul.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13a27c2fec2a2b226e9ae8d5b8f9a61e8b79ceb0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "362230"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="7f532-103">Konfiguratsiooni pakkujate loomine ja nende aktiivseks märkimine</span><span class="sxs-lookup"><span data-stu-id="7f532-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7f532-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua konfiguratsiooni pakkuja elektroonilise aruandluse (ER) puhul.</span><span class="sxs-lookup"><span data-stu-id="7f532-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="7f532-105">Iga elektroonilise aruandluse konfiguratsioon viitab pakkujale kui konfiguratsiooni autorile.</span><span class="sxs-lookup"><span data-stu-id="7f532-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="7f532-106">Selles näites loote konfiguratsiooni pakkuja näidisettevõttele Litware, Inc. Neid etappe teha mis tahes ettevõttes, kuna ER-konfiguratsiooni pakkujate on kõigil ettevõtetel ühised.</span><span class="sxs-lookup"><span data-stu-id="7f532-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="7f532-107">Pakkuja loomine</span><span class="sxs-lookup"><span data-stu-id="7f532-107">Create a provider</span></span>
1. <span data-ttu-id="7f532-108">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="7f532-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="7f532-109">Klõpsake suvandit Konfiguratsiooni pakkujad.</span><span class="sxs-lookup"><span data-stu-id="7f532-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="7f532-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="7f532-110">Click New.</span></span>
    * <span data-ttu-id="7f532-111">Pakkuja kirjel on kordumatu nimi ja URL.</span><span class="sxs-lookup"><span data-stu-id="7f532-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="7f532-112">Vaadake selle lehe sisu üle ja jätke see protseduur vahele, kui kirje Litware, Inc.-i (http://www.litware.com) kohta on juba olemas.</span><span class="sxs-lookup"><span data-stu-id="7f532-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (http://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="7f532-113">Sisestage väljale Nimi suvand Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="7f532-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="7f532-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="7f532-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="7f532-115">Sisestage internetiaadressi väljale väärtus http://www.litware.com.</span><span class="sxs-lookup"><span data-stu-id="7f532-115">In the Internet address field, type 'http://www.litware.com'.</span></span>
    * http://www.litware.com  
6. <span data-ttu-id="7f532-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="7f532-116">Click Save.</span></span>
7. <span data-ttu-id="7f532-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="7f532-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="7f532-118">Valimine aktiivse pakkujana</span><span class="sxs-lookup"><span data-stu-id="7f532-118">Select as an active provider</span></span>
1. <span data-ttu-id="7f532-119">Valige pakkuja Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="7f532-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="7f532-120">Klõpsake valikut Määra aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="7f532-120">Click Set active.</span></span>

