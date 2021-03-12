---
title: Pildi fokaalpunktide kohandamine
description: Selle teema all kirjeldatakse, kuidas kohandada piltide fokaalpunkte rakenduse Microsoft Dynamics 365 Commerce saidiehituses.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9c8fc9a1f944d24aff3ab2923ca2715209a674e4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972928"
---
# <a name="customize-image-focal-points"></a><span data-ttu-id="e940b-103">Pildi fokaalpunktide kohandamine</span><span class="sxs-lookup"><span data-stu-id="e940b-103">Customize image focal points</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e940b-104">Selle teema all kirjeldatakse, kuidas kohandada piltide fokaalpunkte rakenduse Microsoft Dynamics 365 Commerce saidiehituses.</span><span class="sxs-lookup"><span data-stu-id="e940b-104">This topic describes how to customize image focal points in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="e940b-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="e940b-105">Overview</span></span>

<span data-ttu-id="e940b-106">Kui pilt laaditakse üles Kaubanduse saidiehituse meediumiteeki, püüab süsteem määrata pildi fokaalpunkti.</span><span class="sxs-lookup"><span data-stu-id="e940b-106">When an image is uploaded to the Commerce site builder Media Library, the system attempts to determine the focal point of the image.</span></span> <span data-ttu-id="e940b-107">Näiteks, kui pildil on inimene, seab süsteem fokaalpunkti vaikimisi inimese näole.</span><span class="sxs-lookup"><span data-stu-id="e940b-107">For example, if the image has a person on it, the system will set the focal point to the face of the person by default.</span></span> <span data-ttu-id="e940b-108">Enamikul juhtudel töötab automaatselt seatud fokaalpunkt hästi kõigi vaateportide korral, kuid mõnikord on vaja fokaalpunkti reguleerida, et tagada pildi teatud osa alatine nähtavus.</span><span class="sxs-lookup"><span data-stu-id="e940b-108">In most cases the automatically set focal point works well for all viewports, but sometimes you may want to adjust the focal point to ensure that a specific part of the image is always visible.</span></span>

### <a name="define-a-custom-focal-point-for-an-image"></a><span data-ttu-id="e940b-109">Pildi kohandatud fokaalpunkti määramine</span><span class="sxs-lookup"><span data-stu-id="e940b-109">Define a custom focal point for an image</span></span>

<span data-ttu-id="e940b-110">Pildi kohandatud fokaalpunkti määramiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e940b-110">To define a custom focal point for an image, follow these steps.</span></span>

1. <span data-ttu-id="e940b-111">Valige Kaubanduse saidiehitaja vasakpoolsel navigeerimispaanil suvand **Meediumiteek**.</span><span class="sxs-lookup"><span data-stu-id="e940b-111">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="e940b-112">Põhiaknas valige pilt, mida soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="e940b-112">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="e940b-113">Klõpsake käsuribal käsku **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="e940b-113">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="e940b-114">Valige pilt, et siseneda **Redigeerimisrežiimi**.</span><span class="sxs-lookup"><span data-stu-id="e940b-114">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="e940b-115">Valikus **Redigeerimisrežiim** valige **Muuda fokaalpunkti**.</span><span class="sxs-lookup"><span data-stu-id="e940b-115">Under **Edit Mode**, select **Change Focal Point**.</span></span> <span data-ttu-id="e940b-116">Pildil kuvatakse ümmargust fokaalpunkti tähist.</span><span class="sxs-lookup"><span data-stu-id="e940b-116">A circular focal point control appears over the image.</span></span>
1. <span data-ttu-id="e940b-117">Valige fokaalpunkti tähis ja liigutage see soovitud fokaalpunkti.</span><span class="sxs-lookup"><span data-stu-id="e940b-117">Select the focal point control to move it over the desired focal point.</span></span>
1. <span data-ttu-id="e940b-118">Kui olete lõpetanud, valige tegumiribal käsk **Salvesta** ja seejärel valige **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="e940b-118">When you're done, on the command bar select **Save**, and then select **Finish editing**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e940b-119">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e940b-119">Additional resources</span></span>

[<span data-ttu-id="e940b-120">Digitaalse varahalduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="e940b-120">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="e940b-121">Piltide üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="e940b-121">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="e940b-122">Video üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="e940b-122">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="e940b-123">Failide üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="e940b-123">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="e940b-124">Piltide kärpimine</span><span class="sxs-lookup"><span data-stu-id="e940b-124">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="e940b-125">Staatiliste failide üleslaadimine ja kasutamine</span><span class="sxs-lookup"><span data-stu-id="e940b-125">Upload and serve static files</span></span>](upload-serve-static-files.md)
