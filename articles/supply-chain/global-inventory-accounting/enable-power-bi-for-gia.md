---
title: Global Inventory Accounting teenuses Power BI lubamine
description: See teema kirjeldab, kuidas lubada Microsoft Power BI teenuses Global Inventory Accounting.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d7979ed18b98ee6133774cd91bc866d6fca92d5f
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273143"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a><span data-ttu-id="d07ac-103">Global Inventory Accounting teenuses Power BI lubamine</span><span class="sxs-lookup"><span data-stu-id="d07ac-103">Enable Power BI for Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="d07ac-104">Oma [PowerBI.com](https://powerbi.com/) kontolt rakenduse Microsoft Dynamics 365 tööruumi saate kinnitada paanid, armatuurlaudad ja aruanded.</span><span class="sxs-lookup"><span data-stu-id="d07ac-104">You can pin tiles, dashboards, and reports from your [PowerBI.com](https://powerbi.com/) account to your Microsoft Dynamics 365 application workspace.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d07ac-105">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="d07ac-105">Prerequisites</span></span>

<span data-ttu-id="d07ac-106">Power BI aruandluse lubamiseks peavad olema täidetud järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="d07ac-106">The following prerequisites must be in place before you can enable Power BI reporting:</span></span>

- <span data-ttu-id="d07ac-107">Te peate olema Dynamics 365 rakenduse süsteemiadministraator.</span><span class="sxs-lookup"><span data-stu-id="d07ac-107">You must be a system administrator in the Dynamics 365 application.</span></span>
- <span data-ttu-id="d07ac-108">Teil peab olema [PowerBI.com](https://powerbi.com/) konto.</span><span class="sxs-lookup"><span data-stu-id="d07ac-108">You must have a [PowerBI.com](https://powerbi.com/) account.</span></span>
- <span data-ttu-id="d07ac-109">Kontol peab olema vähemalt üks töölaud ja üks Power BI aruanne.</span><span class="sxs-lookup"><span data-stu-id="d07ac-109">You must have at least one dashboard and one report in your Power BI account.</span></span>
- <span data-ttu-id="d07ac-110">Peate olema Azure Active Directory (Azure AD) konto administraator.</span><span class="sxs-lookup"><span data-stu-id="d07ac-110">You must be an administrator for your Azure Active Directory (Azure AD) account.</span></span>
- <span data-ttu-id="d07ac-111">Azure AD domeen peab olema sama domeen, mida kasutate oma [PowerBI.com](https://powerbi.com/) konto jaoks.</span><span class="sxs-lookup"><span data-stu-id="d07ac-111">The Azure AD domain must be the same domain that you used for your [PowerBI.com](https://powerbi.com/) account.</span></span>

## <a name="setup"></a><span data-ttu-id="d07ac-112">Seadistus</span><span class="sxs-lookup"><span data-stu-id="d07ac-112">Setup</span></span>

<span data-ttu-id="d07ac-113">Power BI integratsiooni seadistamiseks läbige need etapid.</span><span class="sxs-lookup"><span data-stu-id="d07ac-113">To set up the Power BI integration, follow these steps.</span></span>

1. <span data-ttu-id="d07ac-114">Logige sisse rakendusse [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="d07ac-114">Sign in to [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="d07ac-115">Minge **ühiskasutuse varateeki**, valige varatüübiks **Power BI aruandemudel** ja laadige alla **Global Inventory Accounting** pakett.</span><span class="sxs-lookup"><span data-stu-id="d07ac-115">Go to **Shared asset library**, select **Power BI report model** as the asset type, and download the **Global Inventory Accounting** package.</span></span> 
1. <span data-ttu-id="d07ac-116">Logige sisse [PowerBI.com](https://app.powerbi.com/) ja laadige üles **Global Inventory Accounting** Power BI aruande fail järgmiste sammude abil.</span><span class="sxs-lookup"><span data-stu-id="d07ac-116">Sign in to [PowerBI.com](https://app.powerbi.com/), and upload the **Global Inventory Accounting** Power BI report file by following these steps:</span></span>

    1. <span data-ttu-id="d07ac-117">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d07ac-117">Select **New**.</span></span>
    1. <span data-ttu-id="d07ac-118">Valige **Laadi fail üles**.</span><span class="sxs-lookup"><span data-stu-id="d07ac-118">Select **Upload a file**.</span></span>
    1. <span data-ttu-id="d07ac-119">Valige **Global Inventory Accounting** Power BI aruande fail.</span><span class="sxs-lookup"><span data-stu-id="d07ac-119">Select the **Global Inventory Accounting** Power BI report file.</span></span>

1. <span data-ttu-id="d07ac-120">Konfigureerige **Global Inventory Accounting** Power BI aruanne järgmiste sammude abil.</span><span class="sxs-lookup"><span data-stu-id="d07ac-120">Configure the **Global Inventory Accounting** Power BI report by following these steps:</span></span>

    1. <span data-ttu-id="d07ac-121">Minge tööruumi **Minu tööruum**, leidkeGlobal Inventory Accounting andmekogum ja seejärel valige menüü **Suvandid** käsk **Sätted**.</span><span class="sxs-lookup"><span data-stu-id="d07ac-121">Go to **My workspace**, find the dataset for Global Inventory Accounting, and then, on the **Options** menu, select **Settings**.</span></span>
    1. <span data-ttu-id="d07ac-122">**Globaalse laoarvestuse sätetes** laiendage **Parameetrid** ja uuendage kõiki parameetreid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="d07ac-122">In **Settings for Global inventory accounting**, expand **Parameters**, and update all parameters as required.</span></span>

1. <span data-ttu-id="d07ac-123">Registreerige rakendus vastavalt jaotisele [PowerBI.com integreerimise konfigureerimine](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span><span class="sxs-lookup"><span data-stu-id="d07ac-123">Register the application as described in [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span></span>
1. <span data-ttu-id="d07ac-124">Integreerige **Global Inventory Accounting** Power BI aruande fail teenusesse Dynamics 365 Supply Chain Management järgmiste sammude abil.</span><span class="sxs-lookup"><span data-stu-id="d07ac-124">Integrate the **Global Inventory Accounting** Power BI report file into Dynamics 365 Supply Chain Management by following these steps:</span></span>

    1. <span data-ttu-id="d07ac-125">Valige suvandid **Süsteemihaldus \> Häälestus \> PowerBI.com konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="d07ac-125">Go to **System administration \> Setup \> PowerBI.com configuration**.</span></span>
    1. <span data-ttu-id="d07ac-126">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="d07ac-126">Select **Edit**.</span></span>
    1. <span data-ttu-id="d07ac-127">Valige **Luba PowerBI.Com integreerimine**.</span><span class="sxs-lookup"><span data-stu-id="d07ac-127">Select **Enable PowerBI.Com integration**.</span></span>
    1. <span data-ttu-id="d07ac-128">Sisestage väljale **Avalduse ID** rakenduse ID.</span><span class="sxs-lookup"><span data-stu-id="d07ac-128">In the **Application ID** field, enter the application ID.</span></span>
    1. <span data-ttu-id="d07ac-129">Sisestage väljale **Avalduse võti** rakenduse võti.</span><span class="sxs-lookup"><span data-stu-id="d07ac-129">In the **Application key** field, enter the application key.</span></span>
    1. <span data-ttu-id="d07ac-130">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d07ac-130">Select **Save**.</span></span>

1. <span data-ttu-id="d07ac-131">Värskendage lehekülge nii, et ilmuks Power BI sisselogimise dialoogiaken.</span><span class="sxs-lookup"><span data-stu-id="d07ac-131">Refresh the page so that the Power BI sign-in dialog box appears.</span></span>
1. <span data-ttu-id="d07ac-132">Valige vahekaardil **Valikud** suvand **Ava aruandekataloog** ja seejärel valige varasemalt üleslaaditud **Global Inventory Accounting** Power BI aruande fail.</span><span class="sxs-lookup"><span data-stu-id="d07ac-132">On the **Options** tab, select **Open report catalog**, and then select the **Global Inventory Accounting** Power BI report file that you uploaded earlier.</span></span>
1. <span data-ttu-id="d07ac-133">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="d07ac-133">Refresh the page.</span></span> <span data-ttu-id="d07ac-134">Peaksite nägema, et teie aruanne on lisatud.</span><span class="sxs-lookup"><span data-stu-id="d07ac-134">You should see that your report has been added.</span></span>
1. <span data-ttu-id="d07ac-135">Valige **Power BI aruanded** all link **Global Inventory Accounting**.</span><span class="sxs-lookup"><span data-stu-id="d07ac-135">Under **Power BI reports**, select the **Global Inventory Accounting** link.</span></span>

<span data-ttu-id="d07ac-136">Lisateabe saamiseks vt [PowerBI.com integratsiooni konfigureerimine](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span><span class="sxs-lookup"><span data-stu-id="d07ac-136">For more information, see [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span></span>
