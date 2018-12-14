---
title: Rakendust Talent ei kuvata Microsoft Dynamics 365 rakenduste hulgas (CDS1.0)
description: "Selles teemas selgitatakse, mida teha, kui klient ei näe Microsoft Dynamics 365 rakenduste hulgas valikut Microsoft Dynamics 365 for Talent."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.contentlocale: et-ee
ms.lasthandoff: 12/04/2018

---

# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a><span data-ttu-id="65b0e-103">Rakendust Talent ei kuvata Microsoft Dynamics 365 rakenduste hulgas (CDS1.0)</span><span class="sxs-lookup"><span data-stu-id="65b0e-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (CDS1.0)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="65b0e-104">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="65b0e-104">**Issue**</span></span>

<span data-ttu-id="65b0e-105">Klient ei näe Microsoft Dynamics 365 rakenduste hulgas valikut Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="65b0e-105">The customer doesn't see the Microsoft Dynamics 365 for Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="65b0e-106">**Eraldusvõime**</span><span class="sxs-lookup"><span data-stu-id="65b0e-106">**Resolution**</span></span>

<span data-ttu-id="65b0e-107">Kasutajale peab Microsoft PowerAppsis olema keskkonna jaoks lisatud roll Keskkonna looja.</span><span class="sxs-lookup"><span data-stu-id="65b0e-107">The user must be added to the Environment Maker role for the environment in Microsoft PowerApps.</span></span>

1. <span data-ttu-id="65b0e-108">PowerAppsi plaani 2 litsentsi omav administraatorkasutaja peab avama lehe [PowerAppsi administraatori portaal](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="65b0e-108">The admin user who has a PowerApps Plan 2 license must open the [PowerApps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="65b0e-109">Valige **Keskkonnad** ja seejärel õige keskkond rakendusele Talent.</span><span class="sxs-lookup"><span data-stu-id="65b0e-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="65b0e-110">Tehke vahekaardi **Turve** vahekaardil **Keskkonnarollid** valik **Keskkonna looja**.</span><span class="sxs-lookup"><span data-stu-id="65b0e-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Vahekaart Keskkonnarollid](media/environment-roles.png)

4. <span data-ttu-id="65b0e-112">Lisage vahekaardil **Kasutajad** kasutaja või organisatsioon.</span><span class="sxs-lookup"><span data-stu-id="65b0e-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Vahekaart Kasutajad](media/environment-maker.png)

5. <span data-ttu-id="65b0e-114">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="65b0e-114">Select **Save**.</span></span>
6. <span data-ttu-id="65b0e-115">Kasutaja peab kohe sisse logima lehele [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="65b0e-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="65b0e-116">Valige kasutajarakenduste uuendamiseks **Sünkrooni**.</span><span class="sxs-lookup"><span data-stu-id="65b0e-116">Select **Sync** to update the user apps.</span></span>

    ![Nupp Sünkrooni](media/get-more.png)

    <span data-ttu-id="65b0e-118">Pärast sünkroonimise lõpuleviimist ilmub rakendus Talent avalehel.</span><span class="sxs-lookup"><span data-stu-id="65b0e-118">After synchronization is completed, Talent will appear on the home page.</span></span>

