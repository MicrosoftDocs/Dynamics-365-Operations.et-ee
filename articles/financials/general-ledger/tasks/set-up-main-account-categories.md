---
title: Põhikonto kategooriate seadistamine
description: Põhikonto kategooriaid kasutatakse vaikearuanneteks finantsaruandluses ja Power BI-s.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e33df434b6a4361872bad10250fe3547d7c4affa
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834802"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="003c8-103">Põhikonto kategooriate seadistamine</span><span class="sxs-lookup"><span data-stu-id="003c8-103">Set up main account categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="003c8-104">Põhikonto kategooriaid kasutatakse vaikearuanneteks finantsaruandluses ja Power BI-s.</span><span class="sxs-lookup"><span data-stu-id="003c8-104">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="003c8-105">Vaikimisi loodud põhikonto kategooriaid saab ümber nimetada, kuid mitte kustutada.</span><span class="sxs-lookup"><span data-stu-id="003c8-105">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="003c8-106">Luua saab täiendavaid kontokategooriaid ning kasutada neid aruandluseks ja analüüsiks.</span><span class="sxs-lookup"><span data-stu-id="003c8-106">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="003c8-107">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="003c8-107">This task uses the USMF demo company.</span></span>


## <a name="create-a-main-account-category"></a><span data-ttu-id="003c8-108">Põhikonto kategooria loomine</span><span class="sxs-lookup"><span data-stu-id="003c8-108">Create a main account category</span></span>
1. <span data-ttu-id="003c8-109">Minge jaotisse Pearaamat > Kontoplaan > Kontod > Põhikonto kategooriad.</span><span class="sxs-lookup"><span data-stu-id="003c8-109">Go to General ledger > Chart of accounts > Accounts > Main account categories.</span></span>
2. <span data-ttu-id="003c8-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="003c8-110">Click New.</span></span>
3. <span data-ttu-id="003c8-111">Sisestage kordumatu nimi väljale Põhikonto kategooria.</span><span class="sxs-lookup"><span data-stu-id="003c8-111">In the Main account category field, enter a unique name.</span></span>
4. <span data-ttu-id="003c8-112">Sisestage väljale Kirjeldus põhikonto kategooria kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="003c8-112">In the Description field, enter a description for the main account category.</span></span>
5. <span data-ttu-id="003c8-113">Valige väljal Põhikonto tüüp kategooriaga seotav põhikonto tüüp.</span><span class="sxs-lookup"><span data-stu-id="003c8-113">In the Main account type field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="003c8-114">Põhikontode linkimine kontokategooriaga</span><span class="sxs-lookup"><span data-stu-id="003c8-114">Link main accounts to account category</span></span>
1. <span data-ttu-id="003c8-115">Klõpsake suvandit Põhikontode linkimine.</span><span class="sxs-lookup"><span data-stu-id="003c8-115">Click Link main accounts.</span></span>
2. <span data-ttu-id="003c8-116">Valige loendist põhikonto, mille soovite määrata põhikonto kategooriale.</span><span class="sxs-lookup"><span data-stu-id="003c8-116">In the list, select the main accounts to assign to the main account category.</span></span>
    * <span data-ttu-id="003c8-117">Põhikontode määramine põhikontode kategooriasse koondab kontode saldod, kui seda kategooriat kasutatakse finantsaruandluseks ja analüüsiks.</span><span class="sxs-lookup"><span data-stu-id="003c8-117">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="003c8-118">Põhikontode valimiseks märkige või tühjendage suvand Lingitud.</span><span class="sxs-lookup"><span data-stu-id="003c8-118">Select or clear the Linked option to choose the main accounts.</span></span>
4. <span data-ttu-id="003c8-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="003c8-119">Click OK.</span></span>
5. <span data-ttu-id="003c8-120">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="003c8-120">Click Yes.</span></span>

