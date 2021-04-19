---
title: Saidi kujunduse valimine
description: See teema kirjeldab, kuidas seada või muuta saidi kujundust rakenduses Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1e11e2ffafa29dfe4ad7a4a8e4d14e9d7c74c31f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794063"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="cc497-103">Saidi kujunduse valimine</span><span class="sxs-lookup"><span data-stu-id="cc497-103">Select a site theme</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cc497-104">See teema kirjeldab, kuidas seada või muuta saidi kujundust rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cc497-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="cc497-105">Saidi paigutust ja stiili (nt fonte, suurusi ja värve) määratletakse teemaga, mille valite ja rakendate saidile.</span><span class="sxs-lookup"><span data-stu-id="cc497-105">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="cc497-106">Kujundus luuakse ja rakendatakse teie ettevõtte arendaja poolt.</span><span class="sxs-lookup"><span data-stu-id="cc497-106">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="cc497-107">Kujunduste ülevaate saamiseks vaadake jaotist [Kujunduse ülevaadet](e-commerce-extensibility/theming.md).</span><span class="sxs-lookup"><span data-stu-id="cc497-107">For an overview of themes, see [Theming overview](e-commerce-extensibility/theming.md).</span></span> <span data-ttu-id="cc497-108">Lisateavet kujunduse loomise ja juurutamise kohta vt jaotisest [Uue kujunduse loomine](e-commerce-extensibility/create-theme.md).</span><span class="sxs-lookup"><span data-stu-id="cc497-108">For more information about how to create and deploy themes, see [Create a new theme](e-commerce-extensibility/create-theme.md).</span></span>

<span data-ttu-id="cc497-109">Kui loote esmalt saidi, kasutab see vaikimisi kujundust nimega **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="cc497-109">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="cc497-110">See vaikekujundus on osa Commerce'i mooduliteegist.</span><span class="sxs-lookup"><span data-stu-id="cc497-110">This default theme is provided as part of the Commerce module library.</span></span> <span data-ttu-id="cc497-111">Kui olete oma saidi jaoks täiendavad kujundused juurutanud, saate saiti konfigureerida nii, et see kasutab selle asemel ühte neist.</span><span class="sxs-lookup"><span data-stu-id="cc497-111">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="cc497-112">Saidi kujunduse valimine</span><span class="sxs-lookup"><span data-stu-id="cc497-112">Select the site theme</span></span>

<span data-ttu-id="cc497-113">Saidil rakendatava kujunduse valimiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="cc497-113">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="cc497-114">Saidi autorluse keskkonnas minge saidile.</span><span class="sxs-lookup"><span data-stu-id="cc497-114">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="cc497-115">Avage suvand **Saidi haldus** \> **Laiendatavus**.</span><span class="sxs-lookup"><span data-stu-id="cc497-115">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="cc497-116">Jaotises **Kujundus** valige rippmenüüst kujundus.</span><span class="sxs-lookup"><span data-stu-id="cc497-116">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="cc497-117">Valitud kujunduse rakendamiseks saidile valige suvand **Salvesta ja avalda**.</span><span class="sxs-lookup"><span data-stu-id="cc497-117">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="cc497-118">Teie valitud kujundus avaldatakse saidil kohe, kui valite suvandi **Salvesta ja avalda** lehel **Laiendatavus**.</span><span class="sxs-lookup"><span data-stu-id="cc497-118">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="cc497-119">Oma saidi kujunduse eelvaateks enne selle rakendamist saate kasutada oma arendus- või liivakasti keskkonda.</span><span class="sxs-lookup"><span data-stu-id="cc497-119">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cc497-120">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="cc497-120">Additional resources</span></span>

[<span data-ttu-id="cc497-121">Logo lisamine</span><span class="sxs-lookup"><span data-stu-id="cc497-121">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="cc497-122">CSS-i alistusfailidega töötamine</span><span class="sxs-lookup"><span data-stu-id="cc497-122">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="cc497-123">Leheikooni lisamine</span><span class="sxs-lookup"><span data-stu-id="cc497-123">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="cc497-124">Tervitussõnumi lisamine</span><span class="sxs-lookup"><span data-stu-id="cc497-124">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="cc497-125">Autoriõiguste teatise lisamine</span><span class="sxs-lookup"><span data-stu-id="cc497-125">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="cc497-126">Saidile keelte lisamine</span><span class="sxs-lookup"><span data-stu-id="cc497-126">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="cc497-127">Telemeetria toetamiseks saidile skriptikoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="cc497-127">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="cc497-128">Kujundamise ülevaade</span><span class="sxs-lookup"><span data-stu-id="cc497-128">Theming overview</span></span>](e-commerce-extensibility/theming.md)

[<span data-ttu-id="cc497-129">Uue teema loomine</span><span class="sxs-lookup"><span data-stu-id="cc497-129">Create a new theme</span></span>](e-commerce-extensibility/create-theme.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
