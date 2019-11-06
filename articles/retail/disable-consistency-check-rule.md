---
title: Jaemüügikande süsteemsuskontrolli reeglite keelamine
description: Selles teemas kirjeldatakse jaemüügikande süsteemsuskontrolli reeglite keelamise funktsiooni teenuses Microsoft Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586293"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="de8b2-103">Jaemüügikande süsteemsuskontrolli reeglite keelamine</span><span class="sxs-lookup"><span data-stu-id="de8b2-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="de8b2-104">Jaemüüjatel võib olla kordumatuid äristsenaariume ja protsesse.</span><span class="sxs-lookup"><span data-stu-id="de8b2-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="de8b2-105">Seetõttu ei kehti kõigi jaemüüjate kohta kõik reeglid, mis on jaemüügikande süsteemsuskontrolli vaikimisi kaasatud.</span><span class="sxs-lookup"><span data-stu-id="de8b2-105">Therefore, not all the rules that are included by default in the retail transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="de8b2-106">Nende muudatustega arvestamiseks sisaldab Microsoft Dynamics 365 Retail funktsiooni, mida saab kasutada mittekohaldatavate reeglite keelamiseks.</span><span class="sxs-lookup"><span data-stu-id="de8b2-106">To accommodate differences, Microsoft Dynamics 365 Retail provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="de8b2-107">Kui soovite näha loendit reeglitest, mis on teie keskkonnas jaemüügikande süsteemsuskontrollis saadaval, ja soovite vaadata iga reegli olekut, avage **Retail \> Peakontori seadistamine \> Parameetrid \> Jaemüügi parameetrid** ja valige vahekaart **Kande kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="de8b2-107">To view the list of rules that are available in the retail transaction consistency checker in your environment, and to see the status of each rule, go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="de8b2-108">Vaikimisi on iga reegli olekuks seatud **Lubatud**.</span><span class="sxs-lookup"><span data-stu-id="de8b2-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="de8b2-109">Nii kasutatakse jaemüügikannete kontrollimiseks, enne kui need jaemüügi väljavõtetesse lisatakse, kõiki reegleid.</span><span class="sxs-lookup"><span data-stu-id="de8b2-109">Therefore, all the rules are used to validate retail transactions before they are pulled into the retail statements.</span></span> <span data-ttu-id="de8b2-110">Reegli keelamiseks seadke selle olekuks **Keelatud**.</span><span class="sxs-lookup"><span data-stu-id="de8b2-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="de8b2-111">Keelatud reegleid ei võeta arvesse, kui jaemüügikandeid väljavõtte arvutamise protsessi ajal kontrollitakse.</span><span class="sxs-lookup"><span data-stu-id="de8b2-111">Disabled rules aren't considered when retail transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="de8b2-112">Kogu kontrollimisprotsessist möödumiseks (olenemata lubatud reeglitest) avage **Retail \> Peakontori seadistamine \> Parameetrid \> Jaemüügi parameetrid** ja siis määrake vahekaardil **Kande kinnitamine** suvandi **Keela jaemüügikannete süsteemsuskontroll** olekuks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="de8b2-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Retail transactions** option to **Yes**.</span></span> <span data-ttu-id="de8b2-113">Kui selle suvandi olekuks on seatud **Ei**, ei saa seda kasutajaliidese kaudu seada tagasi olekusse **Jah**.</span><span class="sxs-lookup"><span data-stu-id="de8b2-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>
