---
title: Tootekonfiguratsioonii tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada tootekonfiguratsioonidega töötamisel tekkivaid probleeme.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 77d0c21fbb5a8479ca5e7bdb759c1373b6b255a4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841547"
---
# <a name="troubleshoot-the-product-configurator"></a><span data-ttu-id="38089-103">Tootekonfiguratsioonii tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="38089-103">Troubleshoot the product configurator</span></span>

<span data-ttu-id="38089-104">Selles teemas kirjeldatakse, kuidas lahendada tootekonfiguratsiooniga töötamisel tekkivaid probleeme.</span><span class="sxs-lookup"><span data-stu-id="38089-104">This topic describes how to fix issues that you might encounter while you work with the product configurator.</span></span>

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a><span data-ttu-id="38089-105">Kauba tekst kirjutatakse üle, kui konfigureerin toote müügitellimuse real.</span><span class="sxs-lookup"><span data-stu-id="38089-105">Item text is overwritten when I configure a product on a sales order line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="38089-106">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="38089-106">Issue description</span></span>

<span data-ttu-id="38089-107">See probleem ilmneb, kui loote müügitellimuse rea seadistatavale kaubale ja seejärel muudate kauba teksti.</span><span class="sxs-lookup"><span data-stu-id="38089-107">This issue occurs when you create a sales order line for a configurable item and then modify the item text.</span></span> <span data-ttu-id="38089-108">Kui konfigureerite kauba ja seejärel valite **OK**, kirjutatakse tekst üle standardse tekstiga.</span><span class="sxs-lookup"><span data-stu-id="38089-108">When you configure the item and then select **OK**, the text is overwritten with the standard text.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="38089-109">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="38089-109">Issue resolution</span></span>

<span data-ttu-id="38089-110">Selline käitumine on oodatud.</span><span class="sxs-lookup"><span data-stu-id="38089-110">This behavior is expected.</span></span> <span data-ttu-id="38089-111">Tekstiväli sisaldab variandi nime, mis on täidetud ainult pärast rea konfigureerimist.</span><span class="sxs-lookup"><span data-stu-id="38089-111">The text field includes the variant name, which is filled in only after you configure the line.</span></span> <span data-ttu-id="38089-112">Seetõttu peate muutma teksti pärast rea konfigureerimist, mitte varem.</span><span class="sxs-lookup"><span data-stu-id="38089-112">Therefore, you must change the text after you've configured the line, not before.</span></span>

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a><span data-ttu-id="38089-113">Täisarvu atribuudid ümardatakse valesti, kui toote konfiguratsiooni mudelid on arvutatud.</span><span class="sxs-lookup"><span data-stu-id="38089-113">Integer attributes are incorrectly rounded when product configuration models are calculated.</span></span>

### <a name="issue-description"></a><span data-ttu-id="38089-114">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="38089-114">Issue description</span></span>

<span data-ttu-id="38089-115">See probleem võib ilmneda, kui sooritate järgmise seeria tegevusi:</span><span class="sxs-lookup"><span data-stu-id="38089-115">This issue can occur when you perform the following series of actions:</span></span>

1. <span data-ttu-id="38089-116">Seadistage järgmised atribuudid tootmise konfiguratsiooni mudelis:</span><span class="sxs-lookup"><span data-stu-id="38089-116">Set up the following attributes on a production configuration model:</span></span>

    - <span data-ttu-id="38089-117">Sisestus (täisarv)</span><span class="sxs-lookup"><span data-stu-id="38089-117">Input (integer)</span></span>
    - <span data-ttu-id="38089-118">Protsent (kümnendarv)</span><span class="sxs-lookup"><span data-stu-id="38089-118">Percent (decimal)</span></span>
    - <span data-ttu-id="38089-119">Tulemus (täisarv)</span><span class="sxs-lookup"><span data-stu-id="38089-119">Result (integer)</span></span>

2. <span data-ttu-id="38089-120">Looge järgmiste sätetega kalkulatsioon:</span><span class="sxs-lookup"><span data-stu-id="38089-120">Create a calculation that has the following expression:</span></span>

    <span data-ttu-id="38089-121">*Tulemus* = *sisend* × *protsent* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="38089-121">*Result* = *Input* × *Percent* ÷ 100</span></span>

<span data-ttu-id="38089-122">Sel juhul ei ümardata täisarvu tulemust alati õigesti.</span><span class="sxs-lookup"><span data-stu-id="38089-122">In this case, the integer result isn't always correctly rounded.</span></span> <span data-ttu-id="38089-123">Näiteks on sisend 1 000 ja protsent on 2,40.</span><span class="sxs-lookup"><span data-stu-id="38089-123">For example, the input is 1,000, and the percentage is 2.40.</span></span> <span data-ttu-id="38089-124">Seetõttu eeldatakse, et tulemuse täisarv on 24, kuna 2,40 protsenti 1 000 on 24 (või 24,00 kümnendkoha vormis).</span><span class="sxs-lookup"><span data-stu-id="38089-124">Therefore, you expect the integer result to be 24, because 2.40 percent of 1,000 is 24 (or 24.00 in decimal form).</span></span> <span data-ttu-id="38089-125">Selle asemel kuvatakse tulemus 23.</span><span class="sxs-lookup"><span data-stu-id="38089-125">Instead, the result is shown as 23.</span></span> <span data-ttu-id="38089-126">Kuid kui protsent on 2,39, ümardatakse arvutus 24 asemel 23-ni.</span><span class="sxs-lookup"><span data-stu-id="38089-126">However, when the percentage is 2.39, the calculation is rounded to 24 instead of 23.</span></span> <span data-ttu-id="38089-127">Kui protsent on 2,50, ümardatakse arvutus 25-ni, nagu oodatud.</span><span class="sxs-lookup"><span data-stu-id="38089-127">When the percentage is 2.50, the calculation is rounded to 25, as expected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="38089-128">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="38089-128">Issue resolution</span></span>

<span data-ttu-id="38089-129">See probleem ilmneb seetõttu, et Microsoft Solver Foundation esindab sisemiselt numbreid, kasutades fraktsioone.</span><span class="sxs-lookup"><span data-stu-id="38089-129">This issue occurs because of the way that Microsoft Solver Foundation internally represents numbers by using fractions.</span></span> <span data-ttu-id="38089-130">Eelmise näite puhul on arvutuse tulemus, mille protsent on 2,40: 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375.</span><span class="sxs-lookup"><span data-stu-id="38089-130">For the preceding example, the result of the calculation where the percentage is 2.40 is represented as 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375.</span></span> <span data-ttu-id="38089-131">Kui .NET annab selle väärtuse täisarvuna, tagastatakse see kui 23.</span><span class="sxs-lookup"><span data-stu-id="38089-131">When .NET casts this value as an integer, it will return 23.</span></span>

<span data-ttu-id="38089-132">Seda käitumist ei muudeta, kuna teised stsenaariumid sõltuvad sellest.</span><span class="sxs-lookup"><span data-stu-id="38089-132">This behavior won't be changed, because other scenarios depend on it.</span></span> <span data-ttu-id="38089-133">Eelneva näite puhul saate probleemi lahendada, kehtestades täiendava kümnendkoha atribuudi ja arvutuse.</span><span class="sxs-lookup"><span data-stu-id="38089-133">For the preceding example, you can fix the issue by introducing an additional decimal attribute and a calculation.</span></span>

<span data-ttu-id="38089-134">Näiteks saate seadistada järgmised atribuudid tootmise konfiguratsiooni mudelis:</span><span class="sxs-lookup"><span data-stu-id="38089-134">For example, you can set up the following attributes on a production configuration model:</span></span>

- <span data-ttu-id="38089-135">Sisestus (täisarv)</span><span class="sxs-lookup"><span data-stu-id="38089-135">Input (integer)</span></span>
- <span data-ttu-id="38089-136">Protsent (kümnendarv)</span><span class="sxs-lookup"><span data-stu-id="38089-136">Percent (decimal)</span></span>
- <span data-ttu-id="38089-137">ResultDecimal (kümnendarv)</span><span class="sxs-lookup"><span data-stu-id="38089-137">ResultDecimal (decimal)</span></span>
- <span data-ttu-id="38089-138">ResultInteger (täisarv)</span><span class="sxs-lookup"><span data-stu-id="38089-138">ResultInteger (integer)</span></span>

<span data-ttu-id="38089-139">Seejärel saate lisada järgmisi arvutusi:</span><span class="sxs-lookup"><span data-stu-id="38089-139">You can then add the following calculations:</span></span>

- <span data-ttu-id="38089-140">*ResultDecimal* = *sisend* × *protsent* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="38089-140">*ResultDecimal* = *Input* × *Percent* ÷ 100</span></span>
- <span data-ttu-id="38089-141">*ResultInteger* = *ResultDecimal*</span><span class="sxs-lookup"><span data-stu-id="38089-141">*ResultInteger* = *ResultDecimal*</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]