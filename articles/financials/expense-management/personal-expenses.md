---
title: Isiklikud kulud kuluaruandes
description: "Selles teemas selgitatakse kaht võimalust töötaja isiklike kulude käsitlemiseks rakenduses Microsoft Dynamics 365 for Finance and Operations."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e21605dbe9d4f8182b868183e33a12e9b7e62422
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="9cf2c-103">Isiklikud kulud kuluaruandes</span><span class="sxs-lookup"><span data-stu-id="9cf2c-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9cf2c-104">Ärireiside jooksul võib mõnikord juhtuda, et töötaja maksab isiklike kulude eest ettevõtte krediitkaartidega.</span><span class="sxs-lookup"><span data-stu-id="9cf2c-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="9cf2c-105">Kui te ei määratle protsessi isiklike kulude käsitlemiseks, võib kuluaruannete kinnitamine katkeda, kui töötajad esitavad detailsed kuluaruanded.</span><span class="sxs-lookup"><span data-stu-id="9cf2c-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="9cf2c-106">Rakenduses Microsoft Dynamics 365 for Finance and Operations on töötaja isiklike kulude käsitlemiseks kaks järgmist võimalust.</span><span class="sxs-lookup"><span data-stu-id="9cf2c-106">In Microsoft Dynamics 365 for Finance and Operations, there are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="9cf2c-107">**Maksab töövõtja** – teie organisatsioon ei maksa isiklike kulude eest, mis kuvatakse ettevõtte krediitkaardi arvel.</span><span class="sxs-lookup"><span data-stu-id="9cf2c-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="9cf2c-108">Selle asemel luuakse aruanne, mis näitab isiklikke kulusid koos ettevõtte kuludega, mis tasuti ettevõtte krediitkaardiga.</span><span class="sxs-lookup"><span data-stu-id="9cf2c-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="9cf2c-109">**Maksab ettevõte** – teie organisatsioon maksab kogu ettevõtte krediitkaardiarve ja siis debiteerib töötaja kontot isiklike kulutuste eest.</span><span class="sxs-lookup"><span data-stu-id="9cf2c-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="9cf2c-110">Saate organisatsiooni kasutatava võimaluse valida lehel **Kulutuste haldamise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="9cf2c-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>

