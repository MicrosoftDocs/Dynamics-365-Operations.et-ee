---
title: Talentit ei kuvata Microsoft Dynamics 365 rakenduste hulgas (Common Data Service 1.0)
description: Selles teemas selgitatakse, mida teha, kui klient ei näe Microsoft Microsoft Dynamics 365 rakenduste hulgas valikut Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7f0cc1c7ec1234b7eedaade0ffadb66965ed2121
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772984"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a><span data-ttu-id="af8a3-103">Talentit ei kuvata Microsoft Dynamics 365 rakenduste hulgas (Common Data Service 1.0)</span><span class="sxs-lookup"><span data-stu-id="af8a3-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (Common Data Service 1.0)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="af8a3-104">**Väljastamine**</span><span class="sxs-lookup"><span data-stu-id="af8a3-104">**Issue**</span></span>

<span data-ttu-id="af8a3-105">Klient ei näe Microsoft Dynamics365 rakenduste hulgas valikut Microsoft Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="af8a3-105">The customer doesn't see the Microsoft Dynamics 365 Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="af8a3-106">**Eraldusvõime**</span><span class="sxs-lookup"><span data-stu-id="af8a3-106">**Resolution**</span></span>

<span data-ttu-id="af8a3-107">Kasutajale peab Microsoft Power Appsis olema keskkonna jaoks lisatud roll Keskkonna looja.</span><span class="sxs-lookup"><span data-stu-id="af8a3-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="af8a3-108">Power Appsi plaani 2 litsentsi omav administraatorkasutaja peab avama lehe [Power Appsi Haldusportaal](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="af8a3-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="af8a3-109">Valige **Keskkonnad** ja seejärel õige keskkond rakendusele Talent.</span><span class="sxs-lookup"><span data-stu-id="af8a3-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="af8a3-110">Tehke vahekaardi **Turve** vahekaardil **Keskkonnarollid** valik **Keskkonna looja**.</span><span class="sxs-lookup"><span data-stu-id="af8a3-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Vahekaart Keskkonnarollid](media/environment-roles.png)

4. <span data-ttu-id="af8a3-112">Lisage vahekaardil **Kasutajad** kasutaja või organisatsioon.</span><span class="sxs-lookup"><span data-stu-id="af8a3-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Vahekaart Kasutajad](media/environment-maker.png)

5. <span data-ttu-id="af8a3-114">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="af8a3-114">Select **Save**.</span></span>
6. <span data-ttu-id="af8a3-115">Kasutaja peab kohe sisse logima lehele [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="af8a3-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="af8a3-116">Valige kasutajarakenduste uuendamiseks **Sünkrooni**.</span><span class="sxs-lookup"><span data-stu-id="af8a3-116">Select **Sync** to update the user apps.</span></span>

    ![Nupp Sünkrooni](media/get-more.png)

    <span data-ttu-id="af8a3-118">Pärast sünkroonimise lõpuleviimist ilmub rakendus Talent avalehel.</span><span class="sxs-lookup"><span data-stu-id="af8a3-118">After synchronization is completed, Talent will appear on the home page.</span></span>
