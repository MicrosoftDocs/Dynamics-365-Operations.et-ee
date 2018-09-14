--- 
title: "Finantsdimensioonide määratlemine"
description: "Selles ülesandejuhendis selgitatakse üksuse tagatud finantsdimensiooni ja kohandatud finantsdimensiooni lisamist."
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 20a7781486c6e0612c27af02a1bccbc48c55a932
ms.contentlocale: et-ee
ms.lasthandoff: 09/14/2018

---
# <a name="define-financial-dimensions"></a><span data-ttu-id="57d6f-103">Finantsdimensioonide määratlemine</span><span class="sxs-lookup"><span data-stu-id="57d6f-103">Define financial dimensions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="57d6f-104">Selles ülesandejuhendis selgitatakse üksuse tagatud finantsdimensiooni ja kohandatud finantsdimensiooni lisamist.</span><span class="sxs-lookup"><span data-stu-id="57d6f-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="57d6f-105">Juhendis kasutatakse demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="57d6f-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="57d6f-106">Üksuse tagatud finantsdimensiooni loomine</span><span class="sxs-lookup"><span data-stu-id="57d6f-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="57d6f-107">Avage Pearaamat > Kontoplaan > Dimensioonid > Finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="57d6f-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="57d6f-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="57d6f-108">Click New.</span></span>
3. <span data-ttu-id="57d6f-109">Valige väljal Kasutaja väärtused süsteemi määratletud üksus, millele finantsdimensioon rajada.</span><span class="sxs-lookup"><span data-stu-id="57d6f-109">In the User values from field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="57d6f-110">Sisestage väljale Dimensiooni nimi finantsdimensiooni kirjeldav väärtus.</span><span class="sxs-lookup"><span data-stu-id="57d6f-110">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="57d6f-111">Nimi võib erineda süsteemi määratletud üksusest, kuid ei tohi sisaldada tühikuid ega erimärke.</span><span class="sxs-lookup"><span data-stu-id="57d6f-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>  
5. <span data-ttu-id="57d6f-112">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="57d6f-112">Click Activate.</span></span>
    * <span data-ttu-id="57d6f-113">Finantsdimensiooni aktiveerimine värskendab tabelit finantsdimensiooni nimega ja eemaldab kustutatud dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="57d6f-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="57d6f-114">Dimensiooniväärtusi saate sisestada enne finantsdimensiooni aktiveerimist, kuid finantsdimensiooni ei saa kasutada enne, kui see on aktiveeritud.</span><span class="sxs-lookup"><span data-stu-id="57d6f-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="57d6f-115">Klõpsake aktiveerimisteates suvandit Sule.</span><span class="sxs-lookup"><span data-stu-id="57d6f-115">Click Close on the activation message.</span></span>
7. <span data-ttu-id="57d6f-116">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="57d6f-116">Click Activate.</span></span>
    * <span data-ttu-id="57d6f-117">Dimensiooni aktiveerimise saab planeerida partiiga käitamiseks kindlal kuupäeval ja kellaajal.</span><span class="sxs-lookup"><span data-stu-id="57d6f-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="57d6f-118">Klõpsake suvandit Dimensiooniväärtused.</span><span class="sxs-lookup"><span data-stu-id="57d6f-118">Click Dimension values.</span></span>
    * <span data-ttu-id="57d6f-119">Mõned dimensiooniväärtused on ettevõttekohased.</span><span class="sxs-lookup"><span data-stu-id="57d6f-119">Some dimension values are company specific.</span></span> <span data-ttu-id="57d6f-120">Saate nende ettevõttekohasust kontrollida, kui ettevõtte nimi kuvatakse dimensiooniväärtuste loendis.</span><span class="sxs-lookup"><span data-stu-id="57d6f-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="57d6f-121">Kohanadtud finantsdimensiooni loomine</span><span class="sxs-lookup"><span data-stu-id="57d6f-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="57d6f-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="57d6f-122">Close the page.</span></span>
2. <span data-ttu-id="57d6f-123">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="57d6f-123">Click New.</span></span>
3. <span data-ttu-id="57d6f-124">Väljal Kasuta väärtusi valige suvand <Custom dimension> (kohandatud dimensioon).</span><span class="sxs-lookup"><span data-stu-id="57d6f-124">In the Use values from field, select <Custom dimension>.</span></span>
4. <span data-ttu-id="57d6f-125">Sisestage väljale Dimensiooni nimi finantsdimensiooni kirjeldav väärtus.</span><span class="sxs-lookup"><span data-stu-id="57d6f-125">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="57d6f-126">Nimi ei tohi sisaldada tühikuid ega erimärke.</span><span class="sxs-lookup"><span data-stu-id="57d6f-126">The name cannot contain spaces or special characters.</span></span>  
    * <span data-ttu-id="57d6f-127">Samuti saate määrata kontomaski, et piirata dimensiooniväärtuste puhul sisestatava teabe hulka ja tüüpi.</span><span class="sxs-lookup"><span data-stu-id="57d6f-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    * <span data-ttu-id="57d6f-128">Saate sisestada märke, mis jäävad samaks igale dimensiooniväärtusele, näiteks tähti või sidekriipsu.</span><span class="sxs-lookup"><span data-stu-id="57d6f-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="57d6f-129">Saate sisestada ka trelle (#) ning ja-märke (&) kohatäidetena tähtede ja numbrite jaoks, mis muutuvad iga kord, kui luuakse dimensiooniväärtus.</span><span class="sxs-lookup"><span data-stu-id="57d6f-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="57d6f-130">Kasutage numbrimärki (#) kohatäitena numbrile ning ja-märki (&) kohatäitena tähele.</span><span class="sxs-lookup"><span data-stu-id="57d6f-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="57d6f-131">Näide. Dimensiooniväärtuse piiramiseks tähtedele CC ja kolmele arvule sisestage vormingumaskina CC-###.</span><span class="sxs-lookup"><span data-stu-id="57d6f-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="57d6f-132">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="57d6f-132">Click Activate.</span></span>
    * <span data-ttu-id="57d6f-133">Finantsdimensiooni aktiveerimine värskendab tabelit finantsdimensiooni nimega ja eemaldab kustutatud dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="57d6f-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="57d6f-134">Dimensiooniväärtusi saate sisestada enne finantsdimensiooni aktiveerimist, kuid finantsdimensiooni ei saa kasutada enne, kui see on aktiveeritud.</span><span class="sxs-lookup"><span data-stu-id="57d6f-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="57d6f-135">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="57d6f-135">Click Activate.</span></span>
    * <span data-ttu-id="57d6f-136">Dimensiooni aktiveerimise saab planeerida partiiga käitamiseks kindlal kuupäeval ja kellaajal.</span><span class="sxs-lookup"><span data-stu-id="57d6f-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
7. <span data-ttu-id="57d6f-137">Klõpsake suvandit Dimensiooniväärtused.</span><span class="sxs-lookup"><span data-stu-id="57d6f-137">Click Dimension values.</span></span>
8. <span data-ttu-id="57d6f-138">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="57d6f-138">Click New.</span></span>
9. <span data-ttu-id="57d6f-139">Sisestage väljale Dimensiooni väärtus oma finantsdimensiooni väärtust kirjeldav nimi.</span><span class="sxs-lookup"><span data-stu-id="57d6f-139">In the Dimension value field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="57d6f-140">Sisestage väljale Kirjeldus oma finantsdimensiooni väärtuse kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="57d6f-140">In the Description field, type a description that describes your financial dimension value.</span></span>


