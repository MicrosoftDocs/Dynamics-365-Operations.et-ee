---
title: Isiklikud kulud kuluaruandes
description: Selles teemas selgitatakse kaht võimalust töötaja isiklike kulude käsitlemiseks rakenduses Microsoft Dynamics 365 for Finance and Operations.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b072fa9e78563d3e89b4d60e9ce61473902fee76
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/30/2019
ms.locfileid: "1794980"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="ae241-103">Isiklikud kulud kuluaruandes</span><span class="sxs-lookup"><span data-stu-id="ae241-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae241-104">Ärireiside jooksul võib mõnikord juhtuda, et töötaja maksab isiklike kulude eest ettevõtte krediitkaartidega.</span><span class="sxs-lookup"><span data-stu-id="ae241-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="ae241-105">Kui te ei määratle protsessi isiklike kulude käsitlemiseks, võib kuluaruannete kinnitamine katkeda, kui töötajad esitavad detailsed kuluaruanded.</span><span class="sxs-lookup"><span data-stu-id="ae241-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="ae241-106">Rakenduses Microsoft Dynamics 365 for Finance and Operations on töötaja isiklike kulude käsitlemiseks kaks järgmist võimalust.</span><span class="sxs-lookup"><span data-stu-id="ae241-106">In Microsoft Dynamics 365 for Finance and Operations, there are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="ae241-107">**Maksab töövõtja** – teie organisatsioon ei maksa isiklike kulude eest, mis kuvatakse ettevõtte krediitkaardi arvel.</span><span class="sxs-lookup"><span data-stu-id="ae241-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="ae241-108">Selle asemel luuakse aruanne, mis näitab isiklikke kulusid koos ettevõtte kuludega, mis tasuti ettevõtte krediitkaardiga.</span><span class="sxs-lookup"><span data-stu-id="ae241-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="ae241-109">**Maksab ettevõte** – teie organisatsioon maksab kogu ettevõtte krediitkaardiarve ja siis debiteerib töötaja kontot isiklike kulutuste eest.</span><span class="sxs-lookup"><span data-stu-id="ae241-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="ae241-110">Saate organisatsiooni kasutatava võimaluse valida lehel **Kulutuste haldamise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="ae241-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
