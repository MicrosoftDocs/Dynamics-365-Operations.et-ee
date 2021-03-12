---
title: Jaemüügi funktsiooniprofiili loomine
description: See teema kirjeldab, kuidas luua rakenduses Microsoft Dynamics 365 Commerce funktsiooniprofiil.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: a53fc77a7d457534428929bd431175be7cf450f7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979643"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="ac604-103">Jaemüügi funktsiooniprofiili loomine</span><span class="sxs-lookup"><span data-stu-id="ac604-103">Create a retail functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ac604-104">See teema kirjeldab, kuidas luua rakenduses Microsoft Dynamics 365 Commerce funktsiooniprofiil.</span><span class="sxs-lookup"><span data-stu-id="ac604-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ac604-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="ac604-105">Overview</span></span>

<span data-ttu-id="ac604-106">Kaubanduse funktsiooniprofiil võimaldab erinevaid võrgukanalites kasutatavaid seadistusi.</span><span class="sxs-lookup"><span data-stu-id="ac604-106">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="ac604-107">Iga kanal peab määrama funktsiooniprofiili.</span><span class="sxs-lookup"><span data-stu-id="ac604-107">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="ac604-108">Funktsiooniprofiili loomine</span><span class="sxs-lookup"><span data-stu-id="ac604-108">Create a functionality profile</span></span>

<span data-ttu-id="ac604-109">Funktsiooniprofiili loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="ac604-109">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="ac604-110">Avage navigeerimispaanil **Moodulid \> Kanali seadistus \> Kassa profiilid \> Funktsiooniprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="ac604-110">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="ac604-111">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ac604-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ac604-112">Sisestage väljale **Profiil** profiili ID (alumisel pildil oleval näitel „FN006”).</span><span class="sxs-lookup"><span data-stu-id="ac604-112">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="ac604-113">Sisestage väljale **Kirjeldus** väärtus (alumisel pildil oleval näitel „Adventure Worksi profiil”).</span><span class="sxs-lookup"><span data-stu-id="ac604-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="ac604-114">Valige jaotises **Üldine** riik lokaadi **ISO** jaoks.</span><span class="sxs-lookup"><span data-stu-id="ac604-114">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="ac604-115">Muutke jaotises **Üldine** vastavalt vajadusele teisi seadistusi.</span><span class="sxs-lookup"><span data-stu-id="ac604-115">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="ac604-116">Valige jaotises **Üldine** meilikviitungite jaoks suvand **Kviitungi profiili ID**.</span><span class="sxs-lookup"><span data-stu-id="ac604-116">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="ac604-117">Muutke jaotises **Funktsioonid** vastavalt vajadusele seadistusi.</span><span class="sxs-lookup"><span data-stu-id="ac604-117">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="ac604-118">Muutke jaotises **Summa** vastavalt vajadusele seadistusi.</span><span class="sxs-lookup"><span data-stu-id="ac604-118">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="ac604-119">Muutke jaotises **Teabekoodid** vastavalt vajadusele seadistusi.</span><span class="sxs-lookup"><span data-stu-id="ac604-119">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="ac604-120">Muutke jaotises **Kviitungi nummerdamine** vastavalt vajadusele seadistusi.</span><span class="sxs-lookup"><span data-stu-id="ac604-120">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="ac604-121">Järgmisel pildil on näidatud funktsiooniprofiili näide.</span><span class="sxs-lookup"><span data-stu-id="ac604-121">The following image shows an example functionality profile.</span></span>
  
![Funktsiooniprofiili näide](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="ac604-123">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ac604-123">Additional resources</span></span>

[<span data-ttu-id="ac604-124">Teabekoodid ja teabekoodide grupid</span><span class="sxs-lookup"><span data-stu-id="ac604-124">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="ac604-125">Uue aadressiraamatu loomine</span><span class="sxs-lookup"><span data-stu-id="ac604-125">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="ac604-126">Ekraani paigutuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="ac604-126">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="ac604-127">Retail Hardware Stationi konfigureerimine ja installimine</span><span class="sxs-lookup"><span data-stu-id="ac604-127">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 
