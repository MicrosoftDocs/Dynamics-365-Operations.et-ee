--- 
title: " Registrite loomine ja seostamine"
description: "See protseduur näitab, kuidas luua kassaregistrit."
author: rubencdelgado
manager: AnnBe
ms.date: 10/05/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6a95019e50bcc060165dab3e6aa2b3ca8a897bf3
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="create-and-associate-registers"></a><span data-ttu-id="496bd-103"> Registrite loomine ja seostamine</span><span class="sxs-lookup"><span data-stu-id="496bd-103">Create and associate registers</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="496bd-104">See protseduur näitab, kuidas luua kassaregistrit.</span><span class="sxs-lookup"><span data-stu-id="496bd-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="496bd-105">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="496bd-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="496bd-106">Avage Jaemüük ja kaubandus > Kanali häälestus > Kassa Seadistus > Registrid.</span><span class="sxs-lookup"><span data-stu-id="496bd-106">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="496bd-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="496bd-107">Click New.</span></span>
3. <span data-ttu-id="496bd-108">Sisestage väljale Registri number uue registri ID.</span><span class="sxs-lookup"><span data-stu-id="496bd-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="496bd-109">Registri ID sisaldab tavaliselt koode, mis aitavad vastendada registrit kauplusega, mille juurde see kuulub, ja asukohaga kaupluses.</span><span class="sxs-lookup"><span data-stu-id="496bd-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="496bd-110">Tippige väljale Nimi registri kirjeldav nimi.</span><span class="sxs-lookup"><span data-stu-id="496bd-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="496bd-111">Sisestage või valige väärtus väljal Kaupluse kood.</span><span class="sxs-lookup"><span data-stu-id="496bd-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="496bd-112">Sisestage või valige väärtus väljal Riistvaraprofiil.</span><span class="sxs-lookup"><span data-stu-id="496bd-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="496bd-113">Riistvaraprofiile kasutatakse jaemüügi välisseadmete määramiseks, mis registriga ühendatakse, nt sularahasahtel ja kviitungiprinter.</span><span class="sxs-lookup"><span data-stu-id="496bd-113">Hardware profiles are used to specify the retail peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="496bd-114">Sisestage või valige väärtus väljal Visuaalne profiil.</span><span class="sxs-lookup"><span data-stu-id="496bd-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="496bd-115">Visuaalseid profiile kasutatakse kassa taustal ja sisselogimislehel kasutatavate piltide ning kassa kujunduste määramiseks.</span><span class="sxs-lookup"><span data-stu-id="496bd-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="496bd-116">Sisestage väärtus väljale EFT kassaregistri number.</span><span class="sxs-lookup"><span data-stu-id="496bd-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="496bd-117">EFT kassaregistri numbrit kasutatakse makse töötleja teavitamiseks selle kohta, milline makseterminal autoriseerimistaotlusi saadab.</span><span class="sxs-lookup"><span data-stu-id="496bd-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="496bd-118">Seda väärtust nimetatakse sageli terminali ID-ks või TID-ks.</span><span class="sxs-lookup"><span data-stu-id="496bd-118">This value is often called the "Terminal ID" or “TID”.</span></span> <span data-ttu-id="496bd-119">TID on üldjuhul leitav makseseadme kleebiselt.</span><span class="sxs-lookup"><span data-stu-id="496bd-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="496bd-120">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="496bd-120">Click Save.</span></span>


