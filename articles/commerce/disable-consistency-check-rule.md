---
title: Jaemüügikande süsteemsuskontrolli reeglite keelamine
description: Selles teemas kirjeldatakse kande süsteemsuskontrolli reeglite keelamise funktsiooni teenuses Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 37209f1c1de19335f5f9fa6636ab55dd8b2fccc1
ms.sourcegitcommit: 02640a0f63daa9e509146641824ed623c4d69c7f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/16/2020
ms.locfileid: "3265522"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="57fd5-103">Jaemüügikande süsteemsuskontrolli reeglite keelamine</span><span class="sxs-lookup"><span data-stu-id="57fd5-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57fd5-104">Jaemüüjatel võib olla kordumatuid äristsenaariume ja protsesse.</span><span class="sxs-lookup"><span data-stu-id="57fd5-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="57fd5-105">Seetõttu ei kehti kõigi jaemüüjate kohta kõik reeglid, mis on kaubanduse kande süsteemsuskontrolli vaikimisi kaasatud.</span><span class="sxs-lookup"><span data-stu-id="57fd5-105">Therefore, not all the rules that are included by default in the commerce transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="57fd5-106">Nende muudatustega arvestamiseks sisaldab Microsoft Dynamics 365 Commerce funktsiooni, mida saab kasutada mittekohaldatavate reeglite keelamiseks.</span><span class="sxs-lookup"><span data-stu-id="57fd5-106">To accommodate differences, Microsoft Dynamics 365 Commerce provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="57fd5-107">Kui soovite näha loendit reeglitest, mis on teie keskkonnas kande süsteemsuskontrollis saadaval, ja soovite vaadata iga reegli olekut, avage **Jaemüük ja kaubandus \> Peakontori seadistamine \> Parameetrid \> Kaubanduse parameetrid** ja valige vahekaart **Kande kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="57fd5-107">To view the list of rules that are available in the transaction consistency checker in your environment, and to see the status of each rule, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="57fd5-108">Vaikimisi on iga reegli olekuks seatud **Lubatud**.</span><span class="sxs-lookup"><span data-stu-id="57fd5-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="57fd5-109">Nii kasutatakse kannete kontrollimiseks, enne kui need kaubanduse väljavõtetesse lisatakse, kõiki reegleid.</span><span class="sxs-lookup"><span data-stu-id="57fd5-109">Therefore, all the rules are used to validate transactions before they are pulled into the commerce statements.</span></span> <span data-ttu-id="57fd5-110">Reegli keelamiseks seadke selle olekuks **Keelatud**.</span><span class="sxs-lookup"><span data-stu-id="57fd5-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="57fd5-111">Keelatud reegleid ei võeta arvesse, kui kandeid väljavõtte arvutamise protsessi ajal kontrollitakse.</span><span class="sxs-lookup"><span data-stu-id="57fd5-111">Disabled rules aren't considered when transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="57fd5-112">Kogu kontrollimisprotsessist möödumiseks (olenemata lubatud reeglitest) avage **Jaemüük ja kaubandus \> Peakontori seadistamine \> Parameetrid \> Kaubanduse parameetrid** ja siis määrake vahekaardil **Kande kinnitamine** suvandi **Keela kaubanduse kannete süsteemsuskontroll** olekuks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="57fd5-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Commerce transactions** option to **Yes**.</span></span> <span data-ttu-id="57fd5-113">Kui selle suvandi olekuks on seatud **Ei**, ei saa seda kasutajaliidese kaudu seada tagasi olekusse **Jah**.</span><span class="sxs-lookup"><span data-stu-id="57fd5-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>
