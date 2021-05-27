---
title: Te ei saa prognoositud ühiku kulusid värskendada, kui impordite prognoositud nõudluse kirjeid
description: Kui kasutate andmeüksuseid nõudluse prognoosi kirjete importimiseks, ei uuendata olemasolevate kirjete omahinda nii, et see vastaks imporditud andmetele.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026443"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a><span data-ttu-id="33f06-103">Te ei saa prognoositud ühiku kulusid värskendada, kui impordite prognoositud nõudluse kirjeid</span><span class="sxs-lookup"><span data-stu-id="33f06-103">You can't update the forecasted unit cost when you import demand forecast records</span></span>

<span data-ttu-id="33f06-104">KB number: 4614109</span><span class="sxs-lookup"><span data-stu-id="33f06-104">KB number: 4614109</span></span>

## <a name="symptoms"></a><span data-ttu-id="33f06-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="33f06-105">Symptoms</span></span>

<span data-ttu-id="33f06-106">Kui kasutate andmeüksuseid nõudluse prognoosi kirjete importimiseks, ei uuendata olemasolevate kirjete **Prognoositud omahinda** nii, et see vastaks imporditud andmetele.</span><span class="sxs-lookup"><span data-stu-id="33f06-106">When you use data entities to import demand forecast records, the **Forecasted unit cost** value for existing records isn't updated so that it matches the imported data.</span></span>

## <a name="cause"></a><span data-ttu-id="33f06-107">Põhjus</span><span class="sxs-lookup"><span data-stu-id="33f06-107">Cause</span></span>

<span data-ttu-id="33f06-108">**Prognoositudd ühikuhind** on kirjutuskaitstud väli.</span><span class="sxs-lookup"><span data-stu-id="33f06-108">**Forecasted unit cost** is a read-only field.</span></span> <span data-ttu-id="33f06-109">Väärtus põhineb toote ühikuhinnal ja seda ei saa importimise kaudu otse määrata.</span><span class="sxs-lookup"><span data-stu-id="33f06-109">The value is based on the product unit cost and can't be set directly through import.</span></span>

## <a name="resolution"></a><span data-ttu-id="33f06-110">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="33f06-110">Resolution</span></span>

<span data-ttu-id="33f06-111">Kuna väli on kirjutuskaitstud, ei saa te selle jaoks väärtusi importida.</span><span class="sxs-lookup"><span data-stu-id="33f06-111">Because the field is read only, you can't import values for it.</span></span> <span data-ttu-id="33f06-112">Väärtus arvutatakse vastavalt olemasolevale äriloogikale.</span><span class="sxs-lookup"><span data-stu-id="33f06-112">The value will be calculated according to the existing business logic.</span></span>
