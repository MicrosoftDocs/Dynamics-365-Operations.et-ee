---
title: Kaal peab olema positiivne
description: Kaal peab olema positiivne
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924299"
---
# <a name="weight-must-be-positive"></a><span data-ttu-id="1cb16-103">Kaal peab olema positiivne</span><span class="sxs-lookup"><span data-stu-id="1cb16-103">Weight must be positive</span></span>

<span data-ttu-id="1cb16-104">Tõrkekood: WeightMustBePositive</span><span class="sxs-lookup"><span data-stu-id="1cb16-104">Error code: WeightMustBePositive</span></span>

## <a name="symptoms"></a><span data-ttu-id="1cb16-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="1cb16-105">Symptoms</span></span>

<span data-ttu-id="1cb16-106">Süsteem näitab järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="1cb16-106">The system shows the following error message:</span></span>

> <span data-ttu-id="1cb16-107">Kaal peab olema positiivne.</span><span class="sxs-lookup"><span data-stu-id="1cb16-107">Weight must be positive.</span></span>

## <a name="cause"></a><span data-ttu-id="1cb16-108">Põhjus</span><span class="sxs-lookup"><span data-stu-id="1cb16-108">Cause</span></span>

<span data-ttu-id="1cb16-109">**Brutokaalu** väli on seatud väärtusele *0* (null) või negatiivsele väärtusele.</span><span class="sxs-lookup"><span data-stu-id="1cb16-109">The **Gross Weight** field is set to *0* (zero) or a negative value.</span></span>

## <a name="resolution"></a><span data-ttu-id="1cb16-110">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="1cb16-110">Resolution</span></span>

<span data-ttu-id="1cb16-111">Kaalu määratlemiseks järgige ühte järgmistest sammudest.</span><span class="sxs-lookup"><span data-stu-id="1cb16-111">To specify a weight, follow one of these steps.</span></span>

- <span data-ttu-id="1cb16-112">Seadke väärtus väljale **Brutokaal**.</span><span class="sxs-lookup"><span data-stu-id="1cb16-112">In the **Gross weight** field, set a value.</span></span> <span data-ttu-id="1cb16-113">Siis valige ripploendist ühik.</span><span class="sxs-lookup"><span data-stu-id="1cb16-113">Then select a unit in the drop-down list.</span></span>
- <span data-ttu-id="1cb16-114">Valige **Hangi süsteemi kaal** et arvestada  **Brutokaalu** väärtus.</span><span class="sxs-lookup"><span data-stu-id="1cb16-114">Select **Get system weight** to calculate the **Gross weight** value.</span></span>
