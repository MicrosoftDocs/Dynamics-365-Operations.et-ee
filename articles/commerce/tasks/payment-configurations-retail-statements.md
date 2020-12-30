---
title: " Jaemüügi väljavõtete maksekonfiguratsioonid"
description: See protseduur selgitab Commerce’i kaupluse makseviiside konfiguratsioone, mis mõjutavad väljavõtete loomise ja sisestamise viisi.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 390ccdfde3f9bb93770d456af7532a42e81955a1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411712"
---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="d5cba-103"> Jaemüügi väljavõtete maksekonfiguratsioonid</span><span class="sxs-lookup"><span data-stu-id="d5cba-103">Payment configurations for Retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5cba-104">See protseduur selgitab Commerce’i kaupluse makseviiside konfiguratsioone, mis mõjutavad väljavõtete loomise ja sisestamise viisi.</span><span class="sxs-lookup"><span data-stu-id="d5cba-104">This procedure demonstrates configurations for Commerce store payment methods, which affect how statements get created and posted.</span></span>

<span data-ttu-id="d5cba-105">Salvestamisel kasutatakse demoettevõtte USRT-i.</span><span class="sxs-lookup"><span data-stu-id="d5cba-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="d5cba-106">Minge jaotisse Jaemüük ja kaubandus > Kanalid > Kauplused > Kõik kauplused.</span><span class="sxs-lookup"><span data-stu-id="d5cba-106">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="d5cba-107">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="d5cba-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d5cba-108">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d5cba-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d5cba-109">Klõpsake tegumiribal valikut Seadistus.</span><span class="sxs-lookup"><span data-stu-id="d5cba-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="d5cba-110">Klõpsake suvandit Makseviisid.</span><span class="sxs-lookup"><span data-stu-id="d5cba-110">Click Payment methods.</span></span>
6. <span data-ttu-id="d5cba-111">Laiendage või ahendage jaotist Sisestamine.</span><span class="sxs-lookup"><span data-stu-id="d5cba-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="d5cba-112">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="d5cba-112">Click Edit.</span></span>
    * <span data-ttu-id="d5cba-113">Valige, kas selle makseviisi puhul saadud summad sisestatakse pearaamatukontole või pangakontole.</span><span class="sxs-lookup"><span data-stu-id="d5cba-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="d5cba-114">Valige konto, millele selle makseviisi puhul saadud summad tuleb sisestada.</span><span class="sxs-lookup"><span data-stu-id="d5cba-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="d5cba-115">Valige konto, kuhu sisestada võimalikud erinevused vastuvõetud kannete kogusumma ja selle makseviisi puhul arvutatud summa vahel.</span><span class="sxs-lookup"><span data-stu-id="d5cba-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="d5cba-116">Sellele väljale saate sisestada summa, mida kontrollida, kui erinevuse summa tuleb sisestada teisele erinevusekontole.</span><span class="sxs-lookup"><span data-stu-id="d5cba-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="d5cba-117">Selle abil saate jälgida suuri erinevusi.</span><span class="sxs-lookup"><span data-stu-id="d5cba-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="d5cba-118">Valige konto, kuhu sisestada võimalikud erinevused vastuvõetud kannete kogusumma ja arvestatud summa vahel, kui see ületab väljal Suurim erinevuse summa määratletud väärtust.</span><span class="sxs-lookup"><span data-stu-id="d5cba-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="d5cba-119">Valige suvand Jah, kui soovite sisestada panka hoiustatava raha summad eraldi kontole.</span><span class="sxs-lookup"><span data-stu-id="d5cba-119">Select "Yes" to post bank drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="d5cba-120">Sellel väljal saate valida, kas panka hoiustatava raha summad tuleks sisestada pearaamatukontole või pangakontole.</span><span class="sxs-lookup"><span data-stu-id="d5cba-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="d5cba-121">Valige konto, millele tuleks panka hoiustatava raha summad sisestada.</span><span class="sxs-lookup"><span data-stu-id="d5cba-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="d5cba-122">Valige pangakande tüüp, mida kasutada panka hoiustatava raha summade sisestamisel pangakontole.</span><span class="sxs-lookup"><span data-stu-id="d5cba-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="d5cba-123">Valige suvand Jah, kui soovite sisestada seifi viidava raha summad eraldi kontole.</span><span class="sxs-lookup"><span data-stu-id="d5cba-123">Select "Yes" to post safe drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="d5cba-124">Valige, kas seifi viidava raha summad tuleks sisestada pearaamatukontole või pangakontole.</span><span class="sxs-lookup"><span data-stu-id="d5cba-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="d5cba-125">Valige konto, millele tuleks seifi viidava raha summad sisestada.</span><span class="sxs-lookup"><span data-stu-id="d5cba-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="d5cba-126">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d5cba-126">Click Save.</span></span>

