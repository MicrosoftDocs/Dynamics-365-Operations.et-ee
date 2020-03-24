---
title: Põhikonto kategooriate seadistamine
description: Selles teemas selgitatakse, kuidas seadistada põhikonto kategooriaid rakenduses Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
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
ms.openlocfilehash: 1fabdcd61c60e630e3f32bc4f0c13c44f50259a6
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/28/2020
ms.locfileid: "3091918"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="14fa6-103">Põhikonto kategooriate seadistamine</span><span class="sxs-lookup"><span data-stu-id="14fa6-103">Set up main account categories</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="14fa6-104">Selles teemas selgitatakse, kuidas seadistada põhikonto kategooriaid.</span><span class="sxs-lookup"><span data-stu-id="14fa6-104">This topic explains how to set up main account categories.</span></span> <span data-ttu-id="14fa6-105">Põhikonto kategooriaid kasutatakse vaikearuanneteks finantsaruandluses ja Power BI-s.</span><span class="sxs-lookup"><span data-stu-id="14fa6-105">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="14fa6-106">Vaikimisi loodud põhikonto kategooriaid saab ümber nimetada, kuid mitte kustutada.</span><span class="sxs-lookup"><span data-stu-id="14fa6-106">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="14fa6-107">Luua saab täiendavaid kontokategooriaid ning kasutada neid aruandluseks ja analüüsiks.</span><span class="sxs-lookup"><span data-stu-id="14fa6-107">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="14fa6-108">Teemas kasutatakse demoettevõtet USMF.</span><span class="sxs-lookup"><span data-stu-id="14fa6-108">This topic uses the USMF demo company.</span></span>

## <a name="create-a-main-account-category"></a><span data-ttu-id="14fa6-109">Põhikonto kategooria loomine</span><span class="sxs-lookup"><span data-stu-id="14fa6-109">Create a main account category</span></span>
1. <span data-ttu-id="14fa6-110">Avage **Navigeerimispaan > Moodulid > Pearaamat > Kontoplaan > Kontod > Põhikontode kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="14fa6-110">In the navigation pane, go to **Modules > General Ledger > Chart of accounts > Accounts > Main account categories**.</span></span>
2. <span data-ttu-id="14fa6-111">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="14fa6-111">Select **New**.</span></span>
3. <span data-ttu-id="14fa6-112">**Sisestage kordumatu nimi väljale Põhikonto kategooria.**</span><span class="sxs-lookup"><span data-stu-id="14fa6-112">In the **Main account category** field, enter a unique name.</span></span>
4. <span data-ttu-id="14fa6-113">Sisestage väljale **Kirjeldus** põhikonto kategooria kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="14fa6-113">In the **Description field**, enter a description for the main account category.</span></span>
5. <span data-ttu-id="14fa6-114">Valige väljal **Põhikonto tüüp** kategooriaga seotav põhikonto tüüp.</span><span class="sxs-lookup"><span data-stu-id="14fa6-114">In the **Main account type** field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="14fa6-115">Põhikontode linkimine kontokategooriaga</span><span class="sxs-lookup"><span data-stu-id="14fa6-115">Link main accounts to account category</span></span>
1. <span data-ttu-id="14fa6-116">Klõpsake suvandit **Põhikontode linkimine.**</span><span class="sxs-lookup"><span data-stu-id="14fa6-116">Click **Link main accounts**.</span></span>
2. <span data-ttu-id="14fa6-117">Valige loendist põhikontod, mida põhikonto kategooriale määrata, kontrollides **lingitud** veeru välju.</span><span class="sxs-lookup"><span data-stu-id="14fa6-117">In the list, select the main accounts to assign to the main account category by checking the boxes in the **Linked** column.</span></span> <span data-ttu-id="14fa6-118">Põhikontode määramine põhikontode kategooriasse koondab kontode saldod, kui seda kategooriat kasutatakse finantsaruandluseks ja analüüsiks.</span><span class="sxs-lookup"><span data-stu-id="14fa6-118">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="14fa6-119">Põhikontode valimiseks märkige või tühjendage suvand **Lingitud.**</span><span class="sxs-lookup"><span data-stu-id="14fa6-119">Select or clear the **Linked** option to choose the main accounts.</span></span>
4. <span data-ttu-id="14fa6-120">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="14fa6-120">Select **OK**.</span></span>
5. <span data-ttu-id="14fa6-121">Valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="14fa6-121">Select **Yes**.</span></span>
