---
title: Dynamics 365 Commerce ja Microsoft Teams integratsiooni lubamine
description: See teema kirjeldab, kuidas lubada Microsoft Dynamics 365 Commerce ja Microsoft Teams integratsiooni.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c4d596f27ffe15a97dc04e2ce7e85d21f8e7161f
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908391"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a><span data-ttu-id="ae865-103">Dynamics 365 Commerce ja Microsoft Teams integratsiooni lubamine</span><span class="sxs-lookup"><span data-stu-id="ae865-103">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ae865-104">See teema kirjeldab, kuidas lubada Microsoft Dynamics 365 Commerce ja Microsoft Teams integratsiooni.</span><span class="sxs-lookup"><span data-stu-id="ae865-104">This topic describes how to enable Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="ae865-105">Teamsile teabe andmiseks rakendusest Dynamics 365 Commerce ja müügikoha rakenduse ning Teamsi vaheliste ülesandehalduse funktsioonide teabega sünkroonimiseks peate lubama Commerce'i keskuse integreerimisfunktsioonid.</span><span class="sxs-lookup"><span data-stu-id="ae865-105">To provision Teams with information from Dynamics 365 Commerce and synchronize the task management features between Teams and the point of sale (POS) application, you must enable the integration features in Commerce headquarters.</span></span>

> [!NOTE]
> <span data-ttu-id="ae865-106">Teamsi integreerimise lubamisel nõustute jagama andmeid Teamsiga.</span><span class="sxs-lookup"><span data-stu-id="ae865-106">When you enable Teams integration, you consent to share your data with Teams.</span></span> <span data-ttu-id="ae865-107">Andmed, mida jagatakse Teamsiga, võivad olla teises riigis kui teie Commerce'i andmed ja nende puhul võivad kehtida erinevad vastavusstandardid.</span><span class="sxs-lookup"><span data-stu-id="ae865-107">Data that is shared with Teams might reside in a different country than your Commerce data, and it might be subject to different compliance standards.</span></span> <span data-ttu-id="ae865-108">Lisateavet vt [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="ae865-108">For more information, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="ae865-109">Lisateavet Microsofti privaatsuspoliitikate kohta vt [Microsofti privaatsusavaldusest](https://aka.ms/privacy).</span><span class="sxs-lookup"><span data-stu-id="ae865-109">For information about Microsoft privacy policies, see the [Microsoft Privacy Statement](https://aka.ms/privacy).</span></span>

## <a name="enable-teams-integration"></a><span data-ttu-id="ae865-110">Teamsi integratsiooni lubamine</span><span class="sxs-lookup"><span data-stu-id="ae865-110">Enable Teams integration</span></span>

<span data-ttu-id="ae865-111">Enne, kui saate Microsoft Teams integratsiooni Commerce'iga lubada, peate registreerima Teamsi rakenduse oma rentnikuga Azure'i portaalis.</span><span class="sxs-lookup"><span data-stu-id="ae865-111">Before you can enable Microsoft Teams integration with Commerce, you must register the Teams application with your tenant in the Azure portal.</span></span>

<span data-ttu-id="ae865-112">Teamsi rakenduse registreerimiseks oma rentnikuga Azure'i portaalis järgige järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="ae865-112">To register the Teams application with your tenant in the Azure portal, follow these steps.</span></span>

1. <span data-ttu-id="ae865-113">Järgige samme jaotises [Kiirstart: rakenduse registreerimine Microsofti identiteediplatvormis](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app), et registreerida Teamsi rakendus oma rentnikuga Azure'i portaalis.</span><span class="sxs-lookup"><span data-stu-id="ae865-113">Follow the steps in [Quickstart: Register an app in the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) to register the Teams application with your tenant in the Azure portal.</span></span>
1. <span data-ttu-id="ae865-114">Kopeerige **Rakenduse (kliendi) ID** väärtus registreeritud rakenduse lehel **Ülevaade**.</span><span class="sxs-lookup"><span data-stu-id="ae865-114">Copy the **Application (client) ID** value from the **Overview** page for the registered app.</span></span> <span data-ttu-id="ae865-115">Kasutate seda väärtust Teamsi integreerimise lubamiseks Commerce peakeskuses.</span><span class="sxs-lookup"><span data-stu-id="ae865-115">You will use this value to enable Teams integration in Commerce headquarters.</span></span>
1. <span data-ttu-id="ae865-116">Kopeerige tunnistuse väärtus, mis [lisati tunnistusele](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) etapis 1.</span><span class="sxs-lookup"><span data-stu-id="ae865-116">Copy the certificate value that was entered when you [added a certificate](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) in step 1.</span></span> <span data-ttu-id="ae865-117">Tunnistust nimetatakse ka avalikuks võtmeks või rakenduse võtmeks.</span><span class="sxs-lookup"><span data-stu-id="ae865-117">The certificate is also known as the public key or application key.</span></span> <span data-ttu-id="ae865-118">Kasutate seda väärtust Teamsi integreerimise lubamiseks Commerce peakeskuses.</span><span class="sxs-lookup"><span data-stu-id="ae865-118">You will use this value to enable Teams integration in Commerce headquarters.</span></span>

<span data-ttu-id="ae865-119">Commerce'i peakeskuses Teamsi integratsiooni lubamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ae865-119">To enable Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ae865-120">Valige suvandid **Retail ja Commerce \> Kanali häälestus \> Microsoft Teams integratsiooni konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="ae865-120">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams integration configuration**.</span></span>
1. <span data-ttu-id="ae865-121">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="ae865-121">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ae865-122">Määrake suvand **Luba Microsoft Teams integratsioon** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="ae865-122">Set the **Enable Microsoft Teams integration** option to **Yes**.</span></span>
1. <span data-ttu-id="ae865-123">Väljades **Rakenduse ID** ja **Rakenduse võti** sisestage väärtused, mis te olete saanud rakenduse Teams registreerimisel Azure'i portaalis.</span><span class="sxs-lookup"><span data-stu-id="ae865-123">In the **Application ID** and **Application key** fields, enter the values you obtained when you registered the Teams application in the Azure portal.</span></span>
1. <span data-ttu-id="ae865-124">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ae865-124">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="ae865-125">Järgmine joonis kuvab näidet Teamsi integreerimise konfigureerimise kohta Commerce'i peakeskuses.</span><span class="sxs-lookup"><span data-stu-id="ae865-125">The following illustration shows an example of the configuration of Teams integration in Commerce headquarters.</span></span>

![Teamsi integreerimise konfiguratsioon Commerce'i peakeskuses](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a><span data-ttu-id="ae865-127">Teamsi integratsiooni keelamine</span><span class="sxs-lookup"><span data-stu-id="ae865-127">Disable Teams integration</span></span>

<span data-ttu-id="ae865-128">Commerce'i peakeskuses Microsoft Teams integratsiooni keelamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ae865-128">To disable Microsoft Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ae865-129">Valige suvandid **Retail ja Commerce \> Kanali häälestus \> Microsoft Teams integratsiooni konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="ae865-129">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="ae865-130">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="ae865-130">On the Action Pane, select **Edit**.</span></span>
3. <span data-ttu-id="ae865-131">Määrake suvand **Luba Microsoft Teams integratsioon** valikule **Ei**.</span><span class="sxs-lookup"><span data-stu-id="ae865-131">Set the **Enable Microsoft Teams integration** option to **No**.</span></span>
4. <span data-ttu-id="ae865-132">Tühjendage väärtused väljadelt **Rakenduse ID** ja **Rakenduse võti**.</span><span class="sxs-lookup"><span data-stu-id="ae865-132">Clear the values from the **Application ID** and **Application Key** fields.</span></span>
1. <span data-ttu-id="ae865-133">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ae865-133">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="ae865-134">Pärast Teamsi integreerimise keelamist Commerce'iga ei kuva kassaterminalid enam ülesandeid, mis on avaldatud Teamsi rakendusest.</span><span class="sxs-lookup"><span data-stu-id="ae865-134">After you disable Teams integration with Commerce, POS terminals will no longer show tasks that are published from the Teams application.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ae865-135">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ae865-135">Additional resources</span></span>

[<span data-ttu-id="ae865-136">Dynamics 365 Commerce ja Microsoft Teams integratsiooni ülevaade</span><span class="sxs-lookup"><span data-stu-id="ae865-136">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="ae865-137">Microsoft Teams sätted rakendusest Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ae865-137">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="ae865-138">Ülesannete halduse sünkroonimine Microsoft Teams ja Dynamics 365 Commerce kassade vahel</span><span class="sxs-lookup"><span data-stu-id="ae865-138">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="ae865-139">Kasutaja rollide haldamine rakenduses Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ae865-139">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="ae865-140">Kaupluste ja töörühmade vastendamine, kui töörühmad on olemas rakenduses Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ae865-140">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="ae865-141">Dynamics 365 Commerce ja Microsoft Teams integratsiooni KKK</span><span class="sxs-lookup"><span data-stu-id="ae865-141">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
