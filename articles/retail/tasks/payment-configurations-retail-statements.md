--- 
title: " Jaemüügi väljavõtete maksekonfiguratsioonid"
description: "See protseduur selgitab jaekaupluse makseviiside konfiguratsioone, mis mõjutavad jaemüügi väljavõtete loomise ja sisestamise viisi."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: df936a3d6753b428a7010a6db83fecb5478c9873
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="db0d4-103"> Jaemüügi väljavõtete maksekonfiguratsioonid</span><span class="sxs-lookup"><span data-stu-id="db0d4-103">Payment configurations for Retail statements</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="db0d4-104">See protseduur selgitab jaekaupluse makseviiside konfiguratsioone, mis mõjutavad jaemüügi väljavõtete loomise ja sisestamise viisi.</span><span class="sxs-lookup"><span data-stu-id="db0d4-104">This procedure demonstrates configurations for Retail store payment methods, which affect how Retail statements get created and posted.</span></span>

<span data-ttu-id="db0d4-105">Salvestamisel kasutatakse demoettevõtte USRT-i.</span><span class="sxs-lookup"><span data-stu-id="db0d4-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="db0d4-106">Avage Jaemüük ja kaubandus > Kanalid > Jaemüügikauplused > Kõik jaemüügikauplused.</span><span class="sxs-lookup"><span data-stu-id="db0d4-106">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="db0d4-107">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="db0d4-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="db0d4-108">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="db0d4-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="db0d4-109">Klõpsake tegumiribal valikut Seadistus.</span><span class="sxs-lookup"><span data-stu-id="db0d4-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="db0d4-110">Klõpsake suvandit Makseviisid.</span><span class="sxs-lookup"><span data-stu-id="db0d4-110">Click Payment methods.</span></span>
6. <span data-ttu-id="db0d4-111">Laiendage või ahendage jaotist Sisestamine.</span><span class="sxs-lookup"><span data-stu-id="db0d4-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="db0d4-112">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="db0d4-112">Click Edit.</span></span>
    * <span data-ttu-id="db0d4-113">Valige, kas selle makseviisi puhul saadud summad sisestatakse pearaamatukontole või pangakontole.</span><span class="sxs-lookup"><span data-stu-id="db0d4-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="db0d4-114">Valige konto, millele selle makseviisi puhul saadud summad tuleb sisestada.</span><span class="sxs-lookup"><span data-stu-id="db0d4-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="db0d4-115">Valige konto, kuhu sisestada võimalikud erinevused vastuvõetud kannete kogusumma ja selle makseviisi puhul arvutatud summa vahel.</span><span class="sxs-lookup"><span data-stu-id="db0d4-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="db0d4-116">Sellele väljale saate sisestada summa, mida kontrollida, kui erinevuse summa tuleb sisestada teisele erinevusekontole.</span><span class="sxs-lookup"><span data-stu-id="db0d4-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="db0d4-117">Selle abil saate jälgida suuri erinevusi.</span><span class="sxs-lookup"><span data-stu-id="db0d4-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="db0d4-118">Valige konto, kuhu sisestada võimalikud erinevused vastuvõetud kannete kogusumma ja arvestatud summa vahel, kui see ületab väljal Suurim erinevuse summa määratletud väärtust.</span><span class="sxs-lookup"><span data-stu-id="db0d4-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="db0d4-119">Valige suvand Jah, kui soovite sisestada panka hoiustatava raha summad eraldi kontole.</span><span class="sxs-lookup"><span data-stu-id="db0d4-119">Select "Yes" to post bank drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="db0d4-120">Sellel väljal saate valida, kas panka hoiustatava raha summad tuleks sisestada pearaamatukontole või pangakontole.</span><span class="sxs-lookup"><span data-stu-id="db0d4-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="db0d4-121">Valige konto, millele tuleks panka hoiustatava raha summad sisestada.</span><span class="sxs-lookup"><span data-stu-id="db0d4-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="db0d4-122">Valige pangakande tüüp, mida kasutada panka hoiustatava raha summade sisestamisel pangakontole.</span><span class="sxs-lookup"><span data-stu-id="db0d4-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="db0d4-123">Valige suvand Jah, kui soovite sisestada seifi viidava raha summad eraldi kontole.</span><span class="sxs-lookup"><span data-stu-id="db0d4-123">Select "Yes" to post safe drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="db0d4-124">Valige, kas seifi viidava raha summad tuleks sisestada pearaamatukontole või pangakontole.</span><span class="sxs-lookup"><span data-stu-id="db0d4-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="db0d4-125">Valige konto, millele tuleks seifi viidava raha summad sisestada.</span><span class="sxs-lookup"><span data-stu-id="db0d4-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="db0d4-126">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="db0d4-126">Click Save.</span></span>


