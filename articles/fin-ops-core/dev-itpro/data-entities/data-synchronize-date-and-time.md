---
title: Imporditööde kuupäeva ja kellaaja sünkroonimine
description: Kasutage imporditöödes ajavööndite teisendamise probleemide vältimiseks UTC ajavööndeid.
author: Sunil-Garg
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae04b09a68e64d6d70c0329e689ab08c3903fca0
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798715"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a><span data-ttu-id="2174b-103">Imporditööde kuupäeva ja kellaaja sünkroonimine</span><span class="sxs-lookup"><span data-stu-id="2174b-103">Synchronize date and time in import jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2174b-104">Oluline on määrata imporditöö ajavööndiks koordineeritud maailmaaeg (UTC).</span><span class="sxs-lookup"><span data-stu-id="2174b-104">It's important to set the time zone for your import job to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="2174b-105">Erineva sätte kasutamisel võite näha imporditud andmetes ootamatuid kuupäevi ja kellaaegu.</span><span class="sxs-lookup"><span data-stu-id="2174b-105">You might see unexpected dates and times in your imported data if you use a different setting.</span></span> <span data-ttu-id="2174b-106">Ilma õige sätteta teisendab impordiprotsess UTC kuupäeva kohalikku vormingusse ja seejärel teisendavad süsteemisätted selle uuesti.</span><span class="sxs-lookup"><span data-stu-id="2174b-106">Without the correct setting, the import process converts the UTC date to the local format, and then system settings converts it again.</span></span>

<span data-ttu-id="2174b-107">See topeltteisendus põhjustab rakenduste vahelise muutuse.</span><span class="sxs-lookup"><span data-stu-id="2174b-107">This dual conversion causes dates to change between applications.</span></span> <span data-ttu-id="2174b-108">Näiteks võib topeltteisenduse tõttu töötaja kuupäev olla erinevate kohalike ajavööndite tõttu rakendustes Dynamics 365 Human Resources ja Dynamics 365 Finance erinev.</span><span class="sxs-lookup"><span data-stu-id="2174b-108">For example, the dual conversion could cause an employee's start date to be different between Dynamics 365 Human Resources and Dynamics 365 Finance due to differences in local time zones.</span></span> <span data-ttu-id="2174b-109">Imporditöö seadmine UTC peale lahendab selle probleemi.</span><span class="sxs-lookup"><span data-stu-id="2174b-109">Setting the import job to UTC resolves this problem.</span></span>

1. <span data-ttu-id="2174b-110">Valige rakenduses Dynamics 365 Finance and Operations suvand **Andmehaldus**.</span><span class="sxs-lookup"><span data-stu-id="2174b-110">In Dynamics 365 Finance and Operations, select **Data management**.</span></span>

2. <span data-ttu-id="2174b-111">Valige suvand **Impordi projektid** ja valige seejärel projekt.</span><span class="sxs-lookup"><span data-stu-id="2174b-111">Select **Import projects**, and then select the project.</span></span>

3. <span data-ttu-id="2174b-112">Suvandis **Allika kuupäevavorming** valige **CSV-Unicode**.</span><span class="sxs-lookup"><span data-stu-id="2174b-112">Under **Source date format**, select **CSV-Unicode**.</span></span>

   <span data-ttu-id="2174b-113">[![Allika kuupäevavormingu muutmine UTC-le](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span><span class="sxs-lookup"><span data-stu-id="2174b-113">[![Change source date format to UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span></span>

4. <span data-ttu-id="2174b-114">Muutke suvandi **Ajavöönd** väärtuseks **Koordineeritud maailmaaja vöönd** ja muutke suvandi **Keel** väärtuseks **En-US**.</span><span class="sxs-lookup"><span data-stu-id="2174b-114">Change **Timezone** to **Coordinated Universal Timezone**, and change **Language** to **En-US**.</span></span>


