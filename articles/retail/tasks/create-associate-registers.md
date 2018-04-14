--- 
title: " Registrite loomine ja seostamine"
description: "See protseduur näitab, kuidas luua kassaregistrit."
author: rubencdelgado
manager: AnnBe
ms.date: 10/05/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c88045f6aeeb1f6c8e9d9f43c04c489a82c2d8c8
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="create-and-associate-registers"></a><span data-ttu-id="9a076-103"> Registrite loomine ja seostamine</span><span class="sxs-lookup"><span data-stu-id="9a076-103">Create and associate registers</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9a076-104">See protseduur näitab, kuidas luua kassaregistrit.</span><span class="sxs-lookup"><span data-stu-id="9a076-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="9a076-105">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="9a076-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="9a076-106">Avage Jaemüük ja kaubandus > Kanali häälestus > Kassa Seadistus > Registrid.</span><span class="sxs-lookup"><span data-stu-id="9a076-106">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="9a076-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="9a076-107">Click New.</span></span>
3. <span data-ttu-id="9a076-108">Sisestage väljale Registri number uue registri ID.</span><span class="sxs-lookup"><span data-stu-id="9a076-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="9a076-109">Registri ID sisaldab tavaliselt koode, mis aitavad vastendada registrit kauplusega, mille juurde see kuulub, ja asukohaga kaupluses.</span><span class="sxs-lookup"><span data-stu-id="9a076-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="9a076-110">Tippige väljale Nimi registri kirjeldav nimi.</span><span class="sxs-lookup"><span data-stu-id="9a076-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="9a076-111">Sisestage või valige väärtus väljal Kaupluse kood.</span><span class="sxs-lookup"><span data-stu-id="9a076-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="9a076-112">Sisestage või valige väärtus väljal Riistvaraprofiil.</span><span class="sxs-lookup"><span data-stu-id="9a076-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="9a076-113">Riistvaraprofiile kasutatakse jaemüügi välisseadmete määramiseks, mis registriga ühendatakse, nt sularahasahtel ja kviitungiprinter.</span><span class="sxs-lookup"><span data-stu-id="9a076-113">Hardware profiles are used to specify the retail peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="9a076-114">Sisestage või valige väärtus väljal Visuaalne profiil.</span><span class="sxs-lookup"><span data-stu-id="9a076-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="9a076-115">Visuaalseid profiile kasutatakse kassa taustal ja sisselogimislehel kasutatavate piltide ning kassa kujunduste määramiseks.</span><span class="sxs-lookup"><span data-stu-id="9a076-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="9a076-116">Sisestage väärtus väljale EFT kassaregistri number.</span><span class="sxs-lookup"><span data-stu-id="9a076-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="9a076-117">EFT kassaregistri numbrit kasutatakse makse töötleja teavitamiseks selle kohta, milline makseterminal autoriseerimistaotlusi saadab.</span><span class="sxs-lookup"><span data-stu-id="9a076-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="9a076-118">Seda väärtust nimetatakse sageli terminali ID-ks või TID-ks.</span><span class="sxs-lookup"><span data-stu-id="9a076-118">This value is often called the "Terminal ID" or “TID”.</span></span> <span data-ttu-id="9a076-119">TID on üldjuhul leitav makseseadme kleebiselt.</span><span class="sxs-lookup"><span data-stu-id="9a076-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="9a076-120">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9a076-120">Click Save.</span></span>


