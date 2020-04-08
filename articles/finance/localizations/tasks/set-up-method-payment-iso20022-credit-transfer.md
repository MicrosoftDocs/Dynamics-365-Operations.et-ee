---
title: Makseviisi seadistamine ISO20022 kreeditkorralduse jaoks
description: See protseduur näitab, kuidas seadistada ISO20022 kreeditülekande või mis tahes muu maksetüübi puhul hankija makseviisi, kasutades faili loomiseks elektroonilist aruandlust.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6d60502cd7f749b71cf39cc38d8a39dcbb7b108
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140113"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="83b97-103">Makseviisi seadistamine ISO20022 kreeditkorralduse jaoks</span><span class="sxs-lookup"><span data-stu-id="83b97-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="83b97-104">See protseduur näitab, kuidas seadistada ISO20022 kreeditülekande või mis tahes muu maksetüübi puhul hankija makseviisi, kasutades faili loomiseks elektroonilist aruandlust.</span><span class="sxs-lookup"><span data-stu-id="83b97-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="83b97-105">Enne selle ülesande lõpetamist tuleb eksportida vormingu konfiguratsioonid ja seadistada maksekontod.</span><span class="sxs-lookup"><span data-stu-id="83b97-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="83b97-106">Selle ülesande loomisel kasutati demoettevõtte DEMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="83b97-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="83b97-107">See on kolmas viiest protseduurist, mis illustreerib hankija makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="83b97-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="83b97-108">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="83b97-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="83b97-109">Avage Ostureskontro > Makse seadistus > Makseviisid.</span><span class="sxs-lookup"><span data-stu-id="83b97-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="83b97-110">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="83b97-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="83b97-111">Näiteks saate filtrida välja Makseviis väärtuse SEPA CT järgi.</span><span class="sxs-lookup"><span data-stu-id="83b97-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="83b97-112">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="83b97-112">Click Edit.</span></span>
4. <span data-ttu-id="83b97-113">Valige väljal Periood suvand Kokku.</span><span class="sxs-lookup"><span data-stu-id="83b97-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="83b97-114">Valige väljalt Makse tüüp suvand Elektrooniline makse.</span><span class="sxs-lookup"><span data-stu-id="83b97-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="83b97-115">Laiendage jaotist Failivormingud.</span><span class="sxs-lookup"><span data-stu-id="83b97-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="83b97-116">Valige väljal Üldine elektrooniline aruandlus suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="83b97-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="83b97-117">Sisestage väärtus väljale Ekspordivormingu konfiguratsioon või valige see.</span><span class="sxs-lookup"><span data-stu-id="83b97-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="83b97-118">Valige loendist väärtus ISO20022 kreeditiülekanne (DE).</span><span class="sxs-lookup"><span data-stu-id="83b97-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="83b97-119">Kui loend on tühi, siis pole imporditud ja aktiivset hankija makse ekspordivormingu konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="83b97-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="83b97-120">Valige väljalt Konto tüüp suvand Pank.</span><span class="sxs-lookup"><span data-stu-id="83b97-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="83b97-121">Täpsustage väljal Maksekonto väärtusi DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="83b97-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="83b97-122">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="83b97-122">Click Save.</span></span>

