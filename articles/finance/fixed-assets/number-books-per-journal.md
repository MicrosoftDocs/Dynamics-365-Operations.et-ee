---
title: Raamatute arv töölehe kohta
description: Selles teemas kirjeldatakse seost töölehtede ja vararaamatute vahel, kui loote põhivara soetamise või kulumisoovituse pakett-töö kaudu. Saate määratleda iga soetamise ja kulumi jaoks kaasatud raamatute maksimaalse arvu.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: fb2a25d9e2ffc26f0a37a09cdf3e28a7ca4b84bc
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892403"
---
# <a name="number-of-books-per-journal"></a><span data-ttu-id="66edc-104">Raamatute arv töölehe kohta</span><span class="sxs-lookup"><span data-stu-id="66edc-104">Number of books per journal</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66edc-105">Selles teemas kirjeldatakse seost töölehtede ja vararaamatute vahel, kui loote põhivara soetamise või kulumisoovituse pakett-töö kaudu.</span><span class="sxs-lookup"><span data-stu-id="66edc-105">This topic describes the relationship between journals and asset books when you create a fixed asset acquisition or depreciation proposal through a batch job.</span></span> <span data-ttu-id="66edc-106">Saate määratleda iga soetamise ja kulumi jaoks kaasatud raamatute maksimaalse arvu, kasutades välju vahekaardi **Üldine** jaotises **Raamatute arv töölehe kohta** lehel **Põhivara parameetrid** (**Põhivara \> Seadistamine \> Põhivara parameetrid**).</span><span class="sxs-lookup"><span data-stu-id="66edc-106">You can define the maximum number of books that are included for each acquisition and for depreciation by using the fields in the **Number of books per journal** section on the **General** tab of the **Fixed assets parameters** page (**Fixed assets \> Setup \> Fixed assets parameters**).</span></span> <span data-ttu-id="66edc-107">Need väljad võimaldavad teil jaotada vararaamatute arvu soetuse töölehe ja kulumi töölehe kohta.</span><span class="sxs-lookup"><span data-stu-id="66edc-107">These fields let you distribute the number of asset books per acquisition journal and depreciation journal.</span></span>

<span data-ttu-id="66edc-108">Soetussoovituse puhul on vaikeväärtuseks vähemalt 10 000 raamatut.</span><span class="sxs-lookup"><span data-stu-id="66edc-108">For an acquisition proposal, the default value is at least 10,000 books.</span></span> <span data-ttu-id="66edc-109">Kulumisoovituse puhul on vaikeväärtuseks vähemalt 2000 raamatut.</span><span class="sxs-lookup"><span data-stu-id="66edc-109">For a depreciation proposal, the default value is at least 2,000 books.</span></span>

<span data-ttu-id="66edc-110">Näiteks kui on 4000 põhivara ja kaks raamatut on seotud iga varaga, sisestatakse üks raamat praegusele kihile ja teine raamat sisestatakse maksukihile.</span><span class="sxs-lookup"><span data-stu-id="66edc-110">For example, if there are 4,000 fixed assets, and two books are associated with each asset, one book will be posted to the current layer, and the other book will be posted to the tax layer.</span></span> <span data-ttu-id="66edc-111">Kui soetate 4 000 põhivara pakktöötluse kaudu, sisaldab pakett-töö, mis loob ühe põhivara soetamise töölehe, 4000 vara raamatut.</span><span class="sxs-lookup"><span data-stu-id="66edc-111">If you acquire 4,000 fixed assets through batch processing, the batch job that creates one fixed asset acquisition journal will contain 4,000 asset books.</span></span>

> [!NOTE]
> <span data-ttu-id="66edc-112">Loodud töölehte kasutatakse jätkuvalt, kuni pakett-töö on lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="66edc-112">The journal that is created will continue to be used until the batch job is completed.</span></span>
>
> <span data-ttu-id="66edc-113">Tuletatud raamatuid ei kaasata maksimaalsesse raamatute arvu töölehe kohta.</span><span class="sxs-lookup"><span data-stu-id="66edc-113">The derived books aren't included in the maximum number of books per journal.</span></span>

<span data-ttu-id="66edc-114">Saate kasutada pakktöötlust, et käitada kulum samale soetatud varade kogumile.</span><span class="sxs-lookup"><span data-stu-id="66edc-114">You can use  batch processing to run depreciation for the same set of acquired assets.</span></span> <span data-ttu-id="66edc-115">Näiteks loob pakett-töö kaks kulumi töölehte, millest kumbki koosneb 2000st vararaamatust.</span><span class="sxs-lookup"><span data-stu-id="66edc-115">For example, a batch job creates two depreciation journals, each of which consists of 2,000 asset books.</span></span> <span data-ttu-id="66edc-116">Esimene tööleht sisaldab raamatuid, mis on seotud põhivaradega, mis on nummerdatud 1 kuni 2000.</span><span class="sxs-lookup"><span data-stu-id="66edc-116">The first journal will contain books that are associated with the fixed assets that are numbered 1 through 2,000.</span></span> <span data-ttu-id="66edc-117">Teine tööleht sisaldab siis raamatuid, mis on seotud põhivaradega, mis on nummerdatud 2001 kuni 4000.</span><span class="sxs-lookup"><span data-stu-id="66edc-117">The second journal will then contain books that are associated with the fixed assets that are numbered 2,001 through 4,000.</span></span>

<span data-ttu-id="66edc-118">Pakett-töötluse töö välistab suletud raamatud.</span><span class="sxs-lookup"><span data-stu-id="66edc-118">The batch processing job excludes closed books.</span></span> <span data-ttu-id="66edc-119">Näiteks pakett-töös kulumi puhul suletakse 2000st esimesest raamatust 10.</span><span class="sxs-lookup"><span data-stu-id="66edc-119">For example, in a batch job for depreciation, 10 of the first 2,000 books are closed.</span></span> <span data-ttu-id="66edc-120">Sellel juhul sisaldab esimene tööleht raamatuid, mis on seotud põhivaradega, mis on nummerdatud 1 kuni 2011.</span><span class="sxs-lookup"><span data-stu-id="66edc-120">In this case, the first journal will contain books that are associated with the fixed assets that are numbered 1 through 2,011.</span></span> <span data-ttu-id="66edc-121">Teine tööleht sisaldab siis raamatuid, mis on seotud põhivaradega, mis on nummerdatud 2,012 kuni 4,000.</span><span class="sxs-lookup"><span data-stu-id="66edc-121">The second journal will then contain books that are associated with the fixed assets that are numbered 2,012 through 4,000.</span></span>

> [!NOTE]
> <span data-ttu-id="66edc-122">Kui teil on erinevate eraldajatega põhivara ID-d (nt – või /) ja loote põhivarakandeid pakett-töödes, peate käivitama iga eraldajatüübi jaoks eraldi pakett-töö.</span><span class="sxs-lookup"><span data-stu-id="66edc-122">If you have fixed asset IDs with different separators (such as – or /), and you create fixed asset transactions in batch jobs, you must run a separate batch job for each type of separator.</span></span> <span data-ttu-id="66edc-123">Süsteem ei saa samas pakett-töös töödelda erinevaid eraldajaid.</span><span class="sxs-lookup"><span data-stu-id="66edc-123">The system can't process different separators within the same batch job.</span></span>

<span data-ttu-id="66edc-124">Kui dubleeritud vara ID-d ei ole samas töölehel, rakendatakse raamatute arvu limiiti.</span><span class="sxs-lookup"><span data-stu-id="66edc-124">The limit on the number of books is applied if duplicate asset IDs don't exist in the same journal.</span></span> <span data-ttu-id="66edc-125">Kui aga vara ID on sama, mis raamatu ID, siis on võimalik ületada raamatute arv töölehe kohta, et hoida vara ID samas töölehel.</span><span class="sxs-lookup"><span data-stu-id="66edc-125">However, if the asset ID is the same as the book ID, the number of books per journal can be exceeded to keep the asset ID in the same journal.</span></span>

<span data-ttu-id="66edc-126">Näiteks on 5001 põhivara ID-d, kolm raamatut on seostatud iga põhivara ID-ga ja iga vararaamat sisestatakse samasse sisestamiskihti.</span><span class="sxs-lookup"><span data-stu-id="66edc-126">For example, there are 5,001 fixed asset IDs, three books are associated with each fixed asset ID, and each asset book is posted to the same posting layer.</span></span> <span data-ttu-id="66edc-127">Käivitate kulumi kolmel järestikusel kuul ilma summeerimata.</span><span class="sxs-lookup"><span data-stu-id="66edc-127">You run depreciation for three consecutive months, without summarizing.</span></span>  <span data-ttu-id="66edc-128">Kulumi tööleht luuakse pakett-töö kaudu ja süsteem loob seitse töölehte, millel on 667 põhivara ID-d ja kolm raamatut iga põhivara ID kohta.</span><span class="sxs-lookup"><span data-stu-id="66edc-128">The depreciation journal will be created through a batch job, and the system will create seven journals that have 667 fixed asset IDs and three books for each fixed asset ID.</span></span> <span data-ttu-id="66edc-129">Tulemuseks on 2001 raamatut.</span><span class="sxs-lookup"><span data-stu-id="66edc-129">The result will be 2,001 books.</span></span> <span data-ttu-id="66edc-130">Seetõttu on kolme kuu järel samal töölehel sama vara ID-ga 6003 töölehe rida.</span><span class="sxs-lookup"><span data-stu-id="66edc-130">Therefore, in three months, there will be 6,003 journal lines to maintain the same asset IDs in the same journal.</span></span> <span data-ttu-id="66edc-131">Süsteem loob ka ühe töölehe, millel on 332 põhivara ID-d ja kolm raamatut iga põhivara ID kohta.</span><span class="sxs-lookup"><span data-stu-id="66edc-131">The system will also create one journal that has 332 fixed asset IDs and three books for each fixed asset ID.</span></span> <span data-ttu-id="66edc-132">Kolme kuu pärast on kokku 2988 rida.</span><span class="sxs-lookup"><span data-stu-id="66edc-132">In three months, there will be 2,988 lines.</span></span>

> [!NOTE] 
> <span data-ttu-id="66edc-133">Kui parameeter **Summeri kulum** on kulumisoovituse loomisel sisse lülitatud, ei ole välja **Raamatute arv töölehe kohta - kulumisoovitus** väärtusel mingit mõju.</span><span class="sxs-lookup"><span data-stu-id="66edc-133">If the **Summarize depreciation** parameter is turned on when you're creating a depreciation proposal, then the value in the **Number of books per journal - Depreciation proposal** field has no effect.</span></span> <span data-ttu-id="66edc-134">Sel juhul on raamatute arv töölehe kohta 6000, mis on sisemine määratletud piir.</span><span class="sxs-lookup"><span data-stu-id="66edc-134">In this case number of books per journal is 6000, which is the internal defined limit.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
