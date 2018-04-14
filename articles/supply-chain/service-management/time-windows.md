---
title: Kellaaja aknad
description: Hooldustellimuse ridade planeerimise optimeerimiseks saate kasutada kellaaja aknaid.
author: YuyuScheller
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9b215e1645c0f0f60437dc363530e2af3d262c4e
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="time-windows"></a><span data-ttu-id="e6982-103">Kellaaja aknad</span><span class="sxs-lookup"><span data-stu-id="e6982-103">Time windows</span></span>  

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="e6982-104">Hooldustellimuse ridade planeerimise optimeerimiseks saate kasutada kellaaja aknaid.</span><span class="sxs-lookup"><span data-stu-id="e6982-104">You can use time windows to optimize the scheduling of service order lines.</span></span> <span data-ttu-id="e6982-105">Süsteemi saate seadistada nii, et see loob hooldustellimusi automaatselt.</span><span class="sxs-lookup"><span data-stu-id="e6982-105">You can set up the system so that it automatically creates service orders.</span></span> <span data-ttu-id="e6982-106">Kellaaja aknas määratud kriteeriumite põhjal saate võimalikult palju hooldustellimuse ridu ühendada võimalikult väheste hooldustellimustega.</span><span class="sxs-lookup"><span data-stu-id="e6982-106">Based on the criteria specified by a time window, you can connect as many service order lines as possible to as few service orders as possible.</span></span>

<span data-ttu-id="e6982-107">Ajaaken määrab, kui kaugele hooldustellimus saab oma arvutatud kuupäeva suhtes liikuda.</span><span class="sxs-lookup"><span data-stu-id="e6982-107">Time windows specify how far a service order line can move from its calculated date.</span></span> <span data-ttu-id="e6982-108">Arvutatud kuupäev on kuupäev, millal hooldustellimuse rida oli plaanitud toimuma.</span><span class="sxs-lookup"><span data-stu-id="e6982-108">The calculated date is the date when the service order line was scheduled to occur.</span></span> <span data-ttu-id="e6982-109">Kuupäev põhineb selle intervallisättel ning hooldusperioodil, mille määrasite lehel **Hooldustellimuste loomine**.</span><span class="sxs-lookup"><span data-stu-id="e6982-109">The date is based on its interval setting and the service period that you defined in the **Create service orders** page.</span></span> <span data-ttu-id="e6982-110">Kellaaja akna määrate järgmises tabelis olevaid väärtusi kasutades.</span><span class="sxs-lookup"><span data-stu-id="e6982-110">You define a time window by using the values in the following table.</span></span>

| <span data-ttu-id="e6982-111">Meetod</span><span class="sxs-lookup"><span data-stu-id="e6982-111">Method</span></span> | <span data-ttu-id="e6982-112">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e6982-112">Description</span></span>                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6982-113">Nädal</span><span class="sxs-lookup"><span data-stu-id="e6982-113">Week</span></span>   | <span data-ttu-id="e6982-114">Kuupäev, mil hooldustellimuse rida saab liigutada igale esialgse arvutatud päevaga sama nädala vabale päevale.</span><span class="sxs-lookup"><span data-stu-id="e6982-114">The date that the service order line can be moved to any open day in the same week as the initial calculated date.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="e6982-115">Kuu</span><span class="sxs-lookup"><span data-stu-id="e6982-115">Month</span></span>  | <span data-ttu-id="e6982-116">Kuupäev, mil hooldustellimuse rida saab liigutada igale esialgse arvutatud päevaga sama kuu vabale päevale.</span><span class="sxs-lookup"><span data-stu-id="e6982-116">The date that the service order line can be moved to any open day in the same month as the initial calculated date.</span></span> <span data-ttu-id="e6982-117">Hooldustellimuse rea arvutatud kuupäev on näiteks 15. veebruar 2017.</span><span class="sxs-lookup"><span data-stu-id="e6982-117">For example, the calculated date for a service order line is February 15, 2017.</span></span> <span data-ttu-id="e6982-118">Hooldustellimuse rida saab planeerida igale nädalapäevale vahemikus 1. veebruar ja 28. veebruar 2017.</span><span class="sxs-lookup"><span data-stu-id="e6982-118">The service order line can be scheduled for any weekday between February 1 and February 28, 2017.</span></span> |
| <span data-ttu-id="e6982-119">Käsitsi</span><span class="sxs-lookup"><span data-stu-id="e6982-119">Manual</span></span> | <span data-ttu-id="e6982-120">Te määrate maksimaalse päevade arvu selle järgi, kui palju enne või pärast esialgset arvutatud kuupäeva hooldustellimuse rida liigutada tohib.</span><span class="sxs-lookup"><span data-stu-id="e6982-120">You define the maximum number of days before or after the initial calculated date that the service order line can be moved.</span></span>                                                                                                                                                                           |

<span data-ttu-id="e6982-121">Kui hooldusleppe rea jaoks ei ole kellaaja akent määratud, tuleb hooldusleppest tulenev hooldustellimuse rida teostada sellel kuupäeval, millele see oli esialgselt planeeritud.</span><span class="sxs-lookup"><span data-stu-id="e6982-121">If you do not specify a time window for a service agreement line, the service order line that is derived from the service agreement must be on the exact date for which it was originally scheduled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6982-122">Seotud teemad</span><span class="sxs-lookup"><span data-stu-id="e6982-122">Related topics</span></span>

[<span data-ttu-id="e6982-123">Kellaaja akende loomine</span><span class="sxs-lookup"><span data-stu-id="e6982-123">Create time windows</span></span>](create-time-windows.md)


