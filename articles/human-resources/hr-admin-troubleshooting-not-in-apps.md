---
title: Human Resources ei ilmu Microsoft Dynamics 365 rakenduste hulgas
description: Selles artiklis selgitatakse, mida teha, kui klient ei näe rakendust Microsoft Dynamics 365 Human Resources Microsoft Dynamics 365 rakenduste.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17a454cd32a08db105a13577c32368ad819bed1c
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053372"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="b7e78-103">Human Resources ei ilmu Microsoft Dynamics 365 rakenduste hulgas</span><span class="sxs-lookup"><span data-stu-id="b7e78-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b7e78-104">**Väljastamine**</span><span class="sxs-lookup"><span data-stu-id="b7e78-104">**Issue**</span></span>

<span data-ttu-id="b7e78-105">Klient ei näe rakendust Dynamics 365 Human Resources Microsoft Dynamics 365 rakenduste hulgas.</span><span class="sxs-lookup"><span data-stu-id="b7e78-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="b7e78-106">**Eraldusvõime**</span><span class="sxs-lookup"><span data-stu-id="b7e78-106">**Resolution**</span></span>

<span data-ttu-id="b7e78-107">Kasutajale peab Microsoft Power Appsis olema keskkonna jaoks lisatud roll Keskkonna looja.</span><span class="sxs-lookup"><span data-stu-id="b7e78-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="b7e78-108">Power Appsi plaani 2 litsentsi omav administraatorkasutaja peab avama lehe [Power Appsi Haldusportaal](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="b7e78-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="b7e78-109">Valige **Keskkonnad** ja seejärel õige keskkond rakendusele Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b7e78-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="b7e78-110">Tehke vahekaardi **Turve** vahekaardil **Keskkonnarollid** valik **Keskkonna looja**.</span><span class="sxs-lookup"><span data-stu-id="b7e78-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Vahekaart Keskkonnarollid](media/environment-roles.png)

4. <span data-ttu-id="b7e78-112">Lisage vahekaardil **Kasutajad** kasutaja või organisatsioon.</span><span class="sxs-lookup"><span data-stu-id="b7e78-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Vahekaart Kasutajad](media/environment-maker.png)

5. <span data-ttu-id="b7e78-114">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b7e78-114">Select **Save**.</span></span>

6. <span data-ttu-id="b7e78-115">Kasutaja peab kohe sisse logima lehele [Microsoft Dynamics 365](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="b7e78-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="b7e78-116">Valige kasutajarakenduste uuendamiseks **Sünkrooni**.</span><span class="sxs-lookup"><span data-stu-id="b7e78-116">Select **Sync** to update the user apps.</span></span>

    ![Nupp Sünkrooni](media/get-more.png)

    <span data-ttu-id="b7e78-118">Pärast sünkroonimise lõpuleviimist ilmub rakendus Human Resources avalehel.</span><span class="sxs-lookup"><span data-stu-id="b7e78-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]