---
title: Makseviisi seadistamine ISO20022 otsekorralduse puhul
description: See protseduur näitab, kuidas seadistada ISO20022 otsekorralduse või mis tahes muu maksetüübi puhul kliendi makseviisi, kasutades faili loomiseks elektroonilist aruandlust.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38afbc3a49d9020540a56e58ce51196b53d6a9e1
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143428"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a><span data-ttu-id="2c8ee-103">Makseviisi seadistamine ISO20022 otsekorralduse puhul</span><span class="sxs-lookup"><span data-stu-id="2c8ee-103">Setup method of payment for ISO20022 direct debit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2c8ee-104">See protseduur näitab, kuidas seadistada ISO20022 otsekorralduse või mis tahes muu maksetüübi puhul kliendi makseviisi, kasutades faili loomiseks elektroonilist aruandlust.</span><span class="sxs-lookup"><span data-stu-id="2c8ee-104">This procedure shows how to set up the customer method of payment for ISO20022 direct debit or any other payment type using electronic reporting.</span></span> 



<span data-ttu-id="2c8ee-105">Enne selle ülesande lõpetamist tuleb seadistada ekspordivormingu konfiguratsioonid ja maksekontod.</span><span class="sxs-lookup"><span data-stu-id="2c8ee-105">Before you complete this task, you must set up export format configurations and payment accounts.</span></span>



<span data-ttu-id="2c8ee-106">Protseduuri loomisel kasutati demoettevõtte DEMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="2c8ee-106">This procedure was created using the demo data company DEMF.</span></span>



<span data-ttu-id="2c8ee-107">See on kolmas viiest protseduurist, mis näitab kliendi makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="2c8ee-107">This is the third of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="2c8ee-108">Avage Müügireskontro > Maksete seadistus > Makseviisid.</span><span class="sxs-lookup"><span data-stu-id="2c8ee-108">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="2c8ee-109">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="2c8ee-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="2c8ee-110">Näiteks saate filtrida välja Makseviis väärtuse ELECTRONIC järgi.</span><span class="sxs-lookup"><span data-stu-id="2c8ee-110">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
3. <span data-ttu-id="2c8ee-111">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="2c8ee-111">Click Edit.</span></span>
4. <span data-ttu-id="2c8ee-112">Täpsustage väljal Maksekonto väärtusi DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="2c8ee-112">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
5. <span data-ttu-id="2c8ee-113">Laiendage jaotist Failivormingud.</span><span class="sxs-lookup"><span data-stu-id="2c8ee-113">Expand the File formats section.</span></span>
6. <span data-ttu-id="2c8ee-114">Valige väljal Üldine elektrooniline aruandlus suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="2c8ee-114">Select Yes in the Generic electronic reporting field.</span></span>
7. <span data-ttu-id="2c8ee-115">Sisestage väärtus väljale Ekspordivormingu konfiguratsioon või valige see.</span><span class="sxs-lookup"><span data-stu-id="2c8ee-115">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="2c8ee-116">Valige loendist ISO20022 otsekorraldus (DE).</span><span class="sxs-lookup"><span data-stu-id="2c8ee-116">In the list, select ISO20022 Direct debit (DE).</span></span>  <span data-ttu-id="2c8ee-117">Kui loend on tühi, siis pole imporditud ja aktiivset kliendi makse ekspordivormingu konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="2c8ee-117">If the list is empty, the customer payment export format configuration has not been imported and active.</span></span>  
8. <span data-ttu-id="2c8ee-118">Valige väljal Nõua luba suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="2c8ee-118">Select Yes in the Require mandate field.</span></span>
    * <span data-ttu-id="2c8ee-119">Valige parameeter Nõua luba kliendi maksevormingutele, mis nõuavad loa teabe lisamist makseteatele (nt SEPA otsekorraldus).</span><span class="sxs-lookup"><span data-stu-id="2c8ee-119">Select the Require mandate parameter for customer payment formats, which require including mandate information in the payment message, like SEPA direct debit.</span></span>  
9. <span data-ttu-id="2c8ee-120">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="2c8ee-120">Click Save.</span></span>

