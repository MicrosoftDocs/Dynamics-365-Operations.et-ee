--- 
title: Makseviisi seadistamine ISO20022 kreeditkorralduse jaoks
description: "See protseduur näitab, kuidas seadistada ISO20022 kreeditülekande või mis tahes muu maksetüübi puhul hankija makseviisi, kasutades faili loomiseks elektroonilist aruandlust."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6c45324b1523e29aa5c6274b289fa823bf66ea12
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="e2316-103">Makseviisi seadistamine ISO20022 kreeditkorralduse jaoks</span><span class="sxs-lookup"><span data-stu-id="e2316-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e2316-104">See protseduur näitab, kuidas seadistada ISO20022 kreeditülekande või mis tahes muu maksetüübi puhul hankija makseviisi, kasutades faili loomiseks elektroonilist aruandlust.</span><span class="sxs-lookup"><span data-stu-id="e2316-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="e2316-105">Enne selle ülesande lõpetamist tuleb eksportida vormingu konfiguratsioonid ja seadistada maksekontod.</span><span class="sxs-lookup"><span data-stu-id="e2316-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="e2316-106">Selle ülesande loomisel kasutati demoettevõtte DEMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="e2316-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="e2316-107">See on kolmas viiest protseduurist, mis illustreerib hankija makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="e2316-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="e2316-108">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="e2316-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="e2316-109">Avage Ostureskontro > Makse seadistus > Makseviisid.</span><span class="sxs-lookup"><span data-stu-id="e2316-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="e2316-110">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="e2316-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="e2316-111">Näiteks saate filtrida välja Makseviis väärtuse SEPA CT järgi.</span><span class="sxs-lookup"><span data-stu-id="e2316-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="e2316-112">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="e2316-112">Click Edit.</span></span>
4. <span data-ttu-id="e2316-113">Valige väljal Periood suvand Kokku.</span><span class="sxs-lookup"><span data-stu-id="e2316-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="e2316-114">Valige väljalt Makse tüüp suvand Elektrooniline makse.</span><span class="sxs-lookup"><span data-stu-id="e2316-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="e2316-115">Laiendage jaotist Failivormingud.</span><span class="sxs-lookup"><span data-stu-id="e2316-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="e2316-116">Valige väljal Üldine elektrooniline aruandlus suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="e2316-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="e2316-117">Sisestage väärtus väljale Ekspordivormingu konfiguratsioon või valige see.</span><span class="sxs-lookup"><span data-stu-id="e2316-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="e2316-118">Valige loendist väärtus ISO20022 kreeditiülekanne (DE).</span><span class="sxs-lookup"><span data-stu-id="e2316-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="e2316-119">Kui loend on tühi, siis pole imporditud ja aktiivset hankija makse ekspordivormingu konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="e2316-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="e2316-120">Valige väljalt Konto tüüp suvand Pank.</span><span class="sxs-lookup"><span data-stu-id="e2316-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="e2316-121">Täpsustage väljal Maksekonto väärtusi DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="e2316-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="e2316-122">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e2316-122">Click Save.</span></span>


