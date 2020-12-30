---
title: " Registrite loomine ja seostamine"
description: See protseduur näitab, kuidas luua kassaregistrit.
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 001bdd61f9266798dadae2ac7c96a4f4c19dbb94
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411733"
---
# <a name="create-and-associate-registers"></a><span data-ttu-id="bfe3e-103"> Registrite loomine ja seostamine</span><span class="sxs-lookup"><span data-stu-id="bfe3e-103">Create and associate registers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bfe3e-104">See protseduur näitab, kuidas luua kassaregistrit.</span><span class="sxs-lookup"><span data-stu-id="bfe3e-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="bfe3e-105">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="bfe3e-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="bfe3e-106">Avage Jaemüük ja kaubandus > Kanali häälestus > Kassa Seadistus > Registrid.</span><span class="sxs-lookup"><span data-stu-id="bfe3e-106">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="bfe3e-107">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="bfe3e-107">Click New.</span></span>
3. <span data-ttu-id="bfe3e-108">Sisestage väljale Registri number uue registri ID.</span><span class="sxs-lookup"><span data-stu-id="bfe3e-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="bfe3e-109">Registri ID sisaldab tavaliselt koode, mis aitavad vastendada registrit kauplusega, mille juurde see kuulub, ja asukohaga kaupluses.</span><span class="sxs-lookup"><span data-stu-id="bfe3e-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="bfe3e-110">Tippige väljale Nimi registri kirjeldav nimi.</span><span class="sxs-lookup"><span data-stu-id="bfe3e-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="bfe3e-111">Sisestage või valige väärtus väljal Kaupluse kood.</span><span class="sxs-lookup"><span data-stu-id="bfe3e-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="bfe3e-112">Sisestage või valige väärtus väljal Riistvaraprofiil.</span><span class="sxs-lookup"><span data-stu-id="bfe3e-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="bfe3e-113">Riistvaraprofiile kasutatakse registriga ühendatavate välisseadmete määramiseks, nt sularahasahtel ja kviitungiprinter.</span><span class="sxs-lookup"><span data-stu-id="bfe3e-113">Hardware profiles are used to specify the peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="bfe3e-114">Sisestage või valige väärtus väljal Visuaalne profiil.</span><span class="sxs-lookup"><span data-stu-id="bfe3e-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="bfe3e-115">Visuaalseid profiile kasutatakse kassa taustal ja sisselogimislehel kasutatavate piltide ning kassa kujunduste määramiseks.</span><span class="sxs-lookup"><span data-stu-id="bfe3e-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="bfe3e-116">Sisestage väärtus väljale EFT kassaregistri number.</span><span class="sxs-lookup"><span data-stu-id="bfe3e-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="bfe3e-117">EFT kassaregistri numbrit kasutatakse makse töötleja teavitamiseks selle kohta, milline makseterminal autoriseerimistaotlusi saadab.</span><span class="sxs-lookup"><span data-stu-id="bfe3e-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="bfe3e-118">Seda väärtust nimetatakse sageli terminali ID-ks või TID-ks.</span><span class="sxs-lookup"><span data-stu-id="bfe3e-118">This value is often called the "Terminal ID" or "TID".</span></span> <span data-ttu-id="bfe3e-119">TID on üldjuhul leitav makseseadme kleebiselt.</span><span class="sxs-lookup"><span data-stu-id="bfe3e-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="bfe3e-120">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="bfe3e-120">Click Save.</span></span>

