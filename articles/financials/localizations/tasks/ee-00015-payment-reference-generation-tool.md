--- 
title: "Makseviite genereerimise tööriist (Ida-Euroopa)"
description: "See protseduur juhatab teid läbi makseviidete koostamise protseduuri."
author: v-oloski
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Estonia
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c49a53cf83b93bbb6b1a4a27b03eb1a12f966eae
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="payment-reference-generation-tool-eastern-europe"></a><span data-ttu-id="10778-103">Makseviite genereerimise tööriist (Ida-Euroopa)</span><span class="sxs-lookup"><span data-stu-id="10778-103">Payment reference generation tool (Eastern Europe)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="10778-104">See protseduur juhatab teid läbi makseviidete koostamise protseduuri.</span><span class="sxs-lookup"><span data-stu-id="10778-104">This procedure walks you through generating the payment references.</span></span> <span data-ttu-id="10778-105">Ülesande loomisel kasutati demoettevõtte DEMF, mille juriidilise isiku esmase aadressi riigiks/regiooniks on määratud Eesti, andmeid.</span><span class="sxs-lookup"><span data-stu-id="10778-105">This task was created using the demo data company DEMF with the country/region of legal entity primary address updated to be Estonia.</span></span> <span data-ttu-id="10778-106">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="10778-106">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="specify-a-number-sequence-for-payment-references"></a><span data-ttu-id="10778-107">Määratlege viitenumbrite jaoks numbriseeria vorming.</span><span class="sxs-lookup"><span data-stu-id="10778-107">Specify a number sequence for payment references</span></span>
1. <span data-ttu-id="10778-108">Minge jaotisse Müügireskontro > Seadistus > Müügireskontro parameetrid.</span><span class="sxs-lookup"><span data-stu-id="10778-108">Go to Accounts receivable > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="10778-109">Klõpsake vahekaarti Numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="10778-109">Click the Number sequences tab.</span></span>
3. <span data-ttu-id="10778-110">Viiteveerus.</span><span class="sxs-lookup"><span data-stu-id="10778-110">In the Reference column.</span></span> <span data-ttu-id="10778-111">Leidke ja valige kirje "Makseviide".</span><span class="sxs-lookup"><span data-stu-id="10778-111">find and select 'Payment reference' record.</span></span>
4. <span data-ttu-id="10778-112">Sisestage või valige väärtus väljal Numbriseeria kood.</span><span class="sxs-lookup"><span data-stu-id="10778-112">In the Number sequence code field, enter or select a value.</span></span>
    * <span data-ttu-id="10778-113">Võite valida eraldi, vastloodud numbrilise ja pideva numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="10778-113">You may want to select a dedicated, newly created numeric and continuous number sequence.</span></span> <span data-ttu-id="10778-114">Demo eesmärgil kasutage "Acco_18".</span><span class="sxs-lookup"><span data-stu-id="10778-114">For demo purposes, you can use  'Acco_18'.</span></span>  
5. <span data-ttu-id="10778-115">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="10778-115">Click Save.</span></span>

## <a name="create-payment-reference-numbers"></a><span data-ttu-id="10778-116">Loo makse viitenumbrid</span><span class="sxs-lookup"><span data-stu-id="10778-116">Create payment reference numbers</span></span>
1. <span data-ttu-id="10778-117">Avage Müügireskonto > Perioodilised ülesanded > Viitenumbrite loomine.</span><span class="sxs-lookup"><span data-stu-id="10778-117">Go to Accounts receivable > Periodic tasks > Create payment reference numbers.</span></span>
2. <span data-ttu-id="10778-118">Väljal Viitenumbrite loomine valige Jah.</span><span class="sxs-lookup"><span data-stu-id="10778-118">Select Yes in the Create payment reference numbers field.</span></span>
    * <span data-ttu-id="10778-119">Juba klientidele määratud viitenumbrite kustutamiseks valige käsk "Kustuta maksete viitenumbrid".</span><span class="sxs-lookup"><span data-stu-id="10778-119">Select 'Delete payment reference numbers' to remove reference numbers already assigned to customers.</span></span> <span data-ttu-id="10778-120">Võite piirata klientide hulka, kellelt soovite eemaldada või kellele lisada viitenumbri. Selleks kasutage jaotist "Kirjenda kaasamiseks" ja määrake klientidele või kliendirühmadele kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="10778-120">You may limit the customers for which you want to remove or create reference numbers by using 'Record to include' section and applying criteria for customers or customer groups.</span></span>  
3. <span data-ttu-id="10778-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="10778-121">Click OK.</span></span>


