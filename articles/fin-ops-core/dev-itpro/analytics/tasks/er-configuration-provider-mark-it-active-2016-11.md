---
title: Konfiguratsiooni pakkujate loomine ja nende märkimine aktiivseks
description: Selles teemas selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua konfiguratsiooni pakkuja.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11ff1d531b0467cf75ec98b092fe6010f4fa95c0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569783"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="02f17-103">Konfiguratsiooni pakkujate loomine ja nende märkimine aktiivseks</span><span class="sxs-lookup"><span data-stu-id="02f17-103">Create configuration providers and mark them as active</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="02f17-104">Selles teemas selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua konfiguratsiooni pakkuja elektroonilise aruandluse (ER) puhul.</span><span class="sxs-lookup"><span data-stu-id="02f17-104">This topic explains how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="02f17-105">Iga elektroonilise aruandluse konfiguratsioon viitab pakkujale kui konfiguratsiooni autorile.</span><span class="sxs-lookup"><span data-stu-id="02f17-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="02f17-106">Selles näites loote konfiguratsiooni pakkuja näidisettevõttele Litware, Inc. Neid etappe teha mis tahes ettevõttes, kuna ER-konfiguratsiooni pakkujate on kõigil ettevõtetel ühised.</span><span class="sxs-lookup"><span data-stu-id="02f17-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>

## <a name="create-a-provider"></a><span data-ttu-id="02f17-107">Pakkuja loomine</span><span class="sxs-lookup"><span data-stu-id="02f17-107">Create a provider</span></span>
1. <span data-ttu-id="02f17-108">Avage ülemises vasakpoolses nurgas **Navigeerimispaan** ja valige **Organisatsiooni administreerimine**.</span><span class="sxs-lookup"><span data-stu-id="02f17-108">Go to the **navigation pane** in the upper left corner and select **Organization administration**.</span></span>
2. <span data-ttu-id="02f17-109">Avage **Tööruumid > Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="02f17-109">Go to **Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="02f17-110">Avage **Seotud lingid > Konfiguratsiooni pakkujad**.</span><span class="sxs-lookup"><span data-stu-id="02f17-110">Go to **Related links > Configuration providers**.</span></span>
4. <span data-ttu-id="02f17-111">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="02f17-111">Select **New**.</span></span>
    - <span data-ttu-id="02f17-112">Pakkuja kirjel on kordumatu nimi ja URL.</span><span class="sxs-lookup"><span data-stu-id="02f17-112">A provider record has a unique name and URL.</span></span> <span data-ttu-id="02f17-113">Vaadake selle lehe sisu üle ja jätke see protseduur vahele, kui kirje Litware, Inc.-i (https://www.litware.com) kohta on juba olemas.</span><span class="sxs-lookup"><span data-stu-id="02f17-113">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
5. <span data-ttu-id="02f17-114">Trükkige nime väljale `Litware, Inc.`.</span><span class="sxs-lookup"><span data-stu-id="02f17-114">In the Name field, type `Litware, Inc.`.</span></span>
6. <span data-ttu-id="02f17-115">Sisestage internetiaadressi väljale väärtus `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="02f17-115">In the Internet address field, type `https://www.litware.com`.</span></span>
7. <span data-ttu-id="02f17-116">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="02f17-116">Select **Save**.</span></span>
8. <span data-ttu-id="02f17-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="02f17-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="02f17-118">Valimine aktiivse pakkujana</span><span class="sxs-lookup"><span data-stu-id="02f17-118">Select as an active provider</span></span>
1. <span data-ttu-id="02f17-119">Valige pakkuja Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="02f17-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="02f17-120">Valige **Määra aktiivseks**.</span><span class="sxs-lookup"><span data-stu-id="02f17-120">Select **Set active**.</span></span>

![Elektroonilise aruandluse tööruumi leht](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]