---
title: Jaemüügi funktsiooniprofiili loomine
description: See teema kirjeldab, kuidas luua rakenduses Microsoft Dynamics 365 Commerce funktsiooniprofiil.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b8d481597485775796290f61de19ef7682cb9f43
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791993"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="1d72d-103">Jaemüügi funktsiooniprofiili loomine</span><span class="sxs-lookup"><span data-stu-id="1d72d-103">Create a retail functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1d72d-104">See teema kirjeldab, kuidas luua rakenduses Microsoft Dynamics 365 Commerce funktsiooniprofiil.</span><span class="sxs-lookup"><span data-stu-id="1d72d-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1d72d-105">Kaubanduse funktsiooniprofiil võimaldab erinevaid võrgukanalites kasutatavaid seadistusi.</span><span class="sxs-lookup"><span data-stu-id="1d72d-105">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="1d72d-106">Iga kanal peab määrama funktsiooniprofiili.</span><span class="sxs-lookup"><span data-stu-id="1d72d-106">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="1d72d-107">Funktsiooniprofiili loomine</span><span class="sxs-lookup"><span data-stu-id="1d72d-107">Create a functionality profile</span></span>

<span data-ttu-id="1d72d-108">Funktsiooniprofiili loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="1d72d-108">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="1d72d-109">Avage navigeerimispaanil **Moodulid \> Kanali seadistus \> Kassa profiilid \> Funktsiooniprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="1d72d-109">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="1d72d-110">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1d72d-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="1d72d-111">Sisestage väljale **Profiil** profiili ID (alumisel pildil oleval näitel „FN006”).</span><span class="sxs-lookup"><span data-stu-id="1d72d-111">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="1d72d-112">Sisestage väljale **Kirjeldus** väärtus (alumisel pildil oleval näitel „Adventure Worksi profiil”).</span><span class="sxs-lookup"><span data-stu-id="1d72d-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="1d72d-113">Valige jaotises **Üldine** riik lokaadi **ISO** jaoks.</span><span class="sxs-lookup"><span data-stu-id="1d72d-113">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="1d72d-114">Muutke jaotises **Üldine** vastavalt vajadusele teisi seadistusi.</span><span class="sxs-lookup"><span data-stu-id="1d72d-114">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="1d72d-115">Valige jaotises **Üldine** meilikviitungite jaoks suvand **Kviitungi profiili ID**.</span><span class="sxs-lookup"><span data-stu-id="1d72d-115">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="1d72d-116">Muutke jaotises **Funktsioonid** vastavalt vajadusele seadistusi.</span><span class="sxs-lookup"><span data-stu-id="1d72d-116">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="1d72d-117">Muutke jaotises **Summa** vastavalt vajadusele seadistusi.</span><span class="sxs-lookup"><span data-stu-id="1d72d-117">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="1d72d-118">Muutke jaotises **Teabekoodid** vastavalt vajadusele seadistusi.</span><span class="sxs-lookup"><span data-stu-id="1d72d-118">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="1d72d-119">Muutke jaotises **Kviitungi nummerdamine** vastavalt vajadusele seadistusi.</span><span class="sxs-lookup"><span data-stu-id="1d72d-119">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="1d72d-120">Järgmisel pildil on näidatud funktsiooniprofiili näide.</span><span class="sxs-lookup"><span data-stu-id="1d72d-120">The following image shows an example functionality profile.</span></span>
  
![Funktsiooniprofiili näide](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="1d72d-122">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1d72d-122">Additional resources</span></span>

[<span data-ttu-id="1d72d-123">Teabekoodid ja teabekoodide grupid</span><span class="sxs-lookup"><span data-stu-id="1d72d-123">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="1d72d-124">Uue aadressiraamatu loomine</span><span class="sxs-lookup"><span data-stu-id="1d72d-124">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="1d72d-125">Ekraani paigutuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="1d72d-125">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="1d72d-126">Retail Hardware Stationi konfigureerimine ja installimine</span><span class="sxs-lookup"><span data-stu-id="1d72d-126">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
