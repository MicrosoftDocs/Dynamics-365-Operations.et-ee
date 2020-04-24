---
title: Kellaaja aknad
description: Hooldustellimuse ridade planeerimise optimeerimiseks saate kasutada kellaaja aknaid.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63a166806c2c8ac84cc1d71d6ec84fcb28033feb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206515"
---
# <a name="time-windows"></a><span data-ttu-id="8e318-103">Kellaaja aknad</span><span class="sxs-lookup"><span data-stu-id="8e318-103">Time windows</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e318-104">Hooldustellimuse ridade planeerimise optimeerimiseks saate kasutada kellaaja aknaid.</span><span class="sxs-lookup"><span data-stu-id="8e318-104">You can use time windows to optimize the scheduling of service order lines.</span></span> <span data-ttu-id="8e318-105">Süsteemi saate seadistada nii, et see loob hooldustellimusi automaatselt.</span><span class="sxs-lookup"><span data-stu-id="8e318-105">You can set up the system so that it automatically creates service orders.</span></span> <span data-ttu-id="8e318-106">Kellaaja aknas määratud kriteeriumite põhjal saate võimalikult palju hooldustellimuse ridu ühendada võimalikult väheste hooldustellimustega.</span><span class="sxs-lookup"><span data-stu-id="8e318-106">Based on the criteria specified by a time window, you can connect as many service order lines as possible to as few service orders as possible.</span></span>

<span data-ttu-id="8e318-107">Ajaaken määrab, kui kaugele hooldustellimus saab oma arvutatud kuupäeva suhtes liikuda.</span><span class="sxs-lookup"><span data-stu-id="8e318-107">Time windows specify how far a service order line can move from its calculated date.</span></span> <span data-ttu-id="8e318-108">Arvutatud kuupäev on kuupäev, millal hooldustellimuse rida oli plaanitud toimuma.</span><span class="sxs-lookup"><span data-stu-id="8e318-108">The calculated date is the date when the service order line was scheduled to occur.</span></span> <span data-ttu-id="8e318-109">Kuupäev põhineb selle intervallisättel ning hooldusperioodil, mille määrasite lehel **Hooldustellimuste loomine**.</span><span class="sxs-lookup"><span data-stu-id="8e318-109">The date is based on its interval setting and the service period that you defined in the **Create service orders** page.</span></span> <span data-ttu-id="8e318-110">Kellaaja akna määrate järgmises tabelis olevaid väärtusi kasutades.</span><span class="sxs-lookup"><span data-stu-id="8e318-110">You define a time window by using the values in the following table.</span></span>

| <span data-ttu-id="8e318-111">Meetod</span><span class="sxs-lookup"><span data-stu-id="8e318-111">Method</span></span> | <span data-ttu-id="8e318-112">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8e318-112">Description</span></span>                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e318-113">Nädal</span><span class="sxs-lookup"><span data-stu-id="8e318-113">Week</span></span>   | <span data-ttu-id="8e318-114">Kuupäev, mil hooldustellimuse rida saab liigutada igale esialgse arvutatud päevaga sama nädala vabale päevale.</span><span class="sxs-lookup"><span data-stu-id="8e318-114">The date that the service order line can be moved to any open day in the same week as the initial calculated date.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="8e318-115">Kuu</span><span class="sxs-lookup"><span data-stu-id="8e318-115">Month</span></span>  | <span data-ttu-id="8e318-116">Kuupäev, mil hooldustellimuse rida saab liigutada igale esialgse arvutatud päevaga sama kuu vabale päevale.</span><span class="sxs-lookup"><span data-stu-id="8e318-116">The date that the service order line can be moved to any open day in the same month as the initial calculated date.</span></span> <span data-ttu-id="8e318-117">Hooldustellimuse rea arvutatud kuupäev on näiteks 15. veebruar 2017.</span><span class="sxs-lookup"><span data-stu-id="8e318-117">For example, the calculated date for a service order line is February 15, 2017.</span></span> <span data-ttu-id="8e318-118">Hooldustellimuse rida saab planeerida igale nädalapäevale vahemikus 1. veebruar ja 28. veebruar 2017.</span><span class="sxs-lookup"><span data-stu-id="8e318-118">The service order line can be scheduled for any weekday between February 1 and February 28, 2017.</span></span> |
| <span data-ttu-id="8e318-119">Käsitsi</span><span class="sxs-lookup"><span data-stu-id="8e318-119">Manual</span></span> | <span data-ttu-id="8e318-120">Te määrate maksimaalse päevade arvu selle järgi, kui palju enne või pärast esialgset arvutatud kuupäeva hooldustellimuse rida liigutada tohib.</span><span class="sxs-lookup"><span data-stu-id="8e318-120">You define the maximum number of days before or after the initial calculated date that the service order line can be moved.</span></span>                                                                                                                                                                           |

<span data-ttu-id="8e318-121">Kui hooldusleppe rea jaoks ei ole kellaaja akent määratud, tuleb hooldusleppest tulenev hooldustellimuse rida teostada sellel kuupäeval, millele see oli esialgselt planeeritud.</span><span class="sxs-lookup"><span data-stu-id="8e318-121">If you do not specify a time window for a service agreement line, the service order line that is derived from the service agreement must be on the exact date for which it was originally scheduled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e318-122">Seotud teemad</span><span class="sxs-lookup"><span data-stu-id="8e318-122">Related topics</span></span>

[<span data-ttu-id="8e318-123">Kellaaja akende loomine</span><span class="sxs-lookup"><span data-stu-id="8e318-123">Create time windows</span></span>](create-time-windows.md)

