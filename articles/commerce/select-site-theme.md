---
title: Saidi kujunduse valimine
description: See teema kirjeldab, kuidas seada või muuta saidi kujundust rakenduses Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 66fcff9fa18d3c98e022ef91d15903fbba8b6b61
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982394"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="c79f6-103">Saidi kujunduse valimine</span><span class="sxs-lookup"><span data-stu-id="c79f6-103">Select a site theme</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c79f6-104">See teema kirjeldab, kuidas seada või muuta saidi kujundust rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c79f6-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c79f6-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="c79f6-105">Overview</span></span>

<span data-ttu-id="c79f6-106">Saidi paigutust ja stiili (nt fonte, suurusi ja värve) määratletakse teemaga, mille valite ja rakendate saidile.</span><span class="sxs-lookup"><span data-stu-id="c79f6-106">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="c79f6-107">Kujundus luuakse ja rakendatakse teie ettevõtte arendaja poolt.</span><span class="sxs-lookup"><span data-stu-id="c79f6-107">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="c79f6-108">Kujunduste ülevaate saamiseks vaadake jaotist [Kujunduse ülevaadet](e-commerce-extensibility/theming.md).</span><span class="sxs-lookup"><span data-stu-id="c79f6-108">For an overview of themes, see [Theming overview](e-commerce-extensibility/theming.md).</span></span> <span data-ttu-id="c79f6-109">Lisateavet kujunduse loomise ja juurutamise kohta vt jaotisest [Uue kujunduse loomine](e-commerce-extensibility/create-theme.md).</span><span class="sxs-lookup"><span data-stu-id="c79f6-109">For more information about how to create and deploy themes, see [Create a new theme](e-commerce-extensibility/create-theme.md).</span></span>

<span data-ttu-id="c79f6-110">Kui loote esmalt saidi, kasutab see vaikimisi kujundust nimega **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="c79f6-110">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="c79f6-111">See vaikekujundus on osa Commerce'i mooduliteegist.</span><span class="sxs-lookup"><span data-stu-id="c79f6-111">This default theme is provided as part of the Commerce module library.</span></span> <span data-ttu-id="c79f6-112">Kui olete oma saidi jaoks täiendavad kujundused juurutanud, saate saiti konfigureerida nii, et see kasutab selle asemel ühte neist.</span><span class="sxs-lookup"><span data-stu-id="c79f6-112">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="c79f6-113">Saidi kujunduse valimine</span><span class="sxs-lookup"><span data-stu-id="c79f6-113">Select the site theme</span></span>

<span data-ttu-id="c79f6-114">Saidil rakendatava kujunduse valimiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="c79f6-114">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="c79f6-115">Saidi autorluse keskkonnas minge saidile.</span><span class="sxs-lookup"><span data-stu-id="c79f6-115">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="c79f6-116">Avage suvand **Saidi haldus** \> **Laiendatavus**.</span><span class="sxs-lookup"><span data-stu-id="c79f6-116">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="c79f6-117">Jaotises **Kujundus** valige rippmenüüst kujundus.</span><span class="sxs-lookup"><span data-stu-id="c79f6-117">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="c79f6-118">Valitud kujunduse rakendamiseks saidile valige suvand **Salvesta ja avalda**.</span><span class="sxs-lookup"><span data-stu-id="c79f6-118">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="c79f6-119">Teie valitud kujundus avaldatakse saidil kohe, kui valite suvandi **Salvesta ja avalda** lehel **Laiendatavus**.</span><span class="sxs-lookup"><span data-stu-id="c79f6-119">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="c79f6-120">Oma saidi kujunduse eelvaateks enne selle rakendamist saate kasutada oma arendus- või liivakasti keskkonda.</span><span class="sxs-lookup"><span data-stu-id="c79f6-120">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c79f6-121">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c79f6-121">Additional resources</span></span>

[<span data-ttu-id="c79f6-122">Logo lisamine</span><span class="sxs-lookup"><span data-stu-id="c79f6-122">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="c79f6-123">CSS-i alistusfailidega töötamine</span><span class="sxs-lookup"><span data-stu-id="c79f6-123">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="c79f6-124">Leheikooni lisamine</span><span class="sxs-lookup"><span data-stu-id="c79f6-124">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="c79f6-125">Tervitussõnumi lisamine</span><span class="sxs-lookup"><span data-stu-id="c79f6-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="c79f6-126">Autoriõiguste teatise lisamine</span><span class="sxs-lookup"><span data-stu-id="c79f6-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="c79f6-127">Saidile keelte lisamine</span><span class="sxs-lookup"><span data-stu-id="c79f6-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="c79f6-128">Telemeetria toetamiseks saidile skriptikoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="c79f6-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="c79f6-129">Kujundamise ülevaade</span><span class="sxs-lookup"><span data-stu-id="c79f6-129">Theming overview</span></span>](e-commerce-extensibility/theming.md)

[<span data-ttu-id="c79f6-130">Uue teema loomine</span><span class="sxs-lookup"><span data-stu-id="c79f6-130">Create a new theme</span></span>](e-commerce-extensibility/create-theme.md)

