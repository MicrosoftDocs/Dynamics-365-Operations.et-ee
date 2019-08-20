---
title: Seisundi hindamine
description: Selles teemas selgitatakse, kuidas koostada seisundi hindamise malli ja registreerida vara varahalduses.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5294325f67f0484b39194b5bd9784a2e612001a4
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783200"
---
# <a name="condition-assessment"></a><span data-ttu-id="51004-103">Seisundi hindamine</span><span class="sxs-lookup"><span data-stu-id="51004-103">Condition assessment</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="51004-104">Selles teemas selgitatakse, kuidas koostada seisundi hindamise malli ja registreerida vara varahalduses.</span><span class="sxs-lookup"><span data-stu-id="51004-104">This topic explains how to create a condition assessment template and registration on an asset in Asset Management.</span></span> <span data-ttu-id="51004-105">Seisundi hindamine toimub korrapäraste ajavahemike järel ning esmane eesmärk on luua ja säilitada vara tingimusandmed.</span><span class="sxs-lookup"><span data-stu-id="51004-105">Condition assessment is performed at regular intervals, and the primary objective is to create and maintain condition data on assets.</span></span> <span data-ttu-id="51004-106">Ennetava hoolduse seisukohast on oluline jälgida põhiteavet, näiteks praegust seisundit ja järelejäänud eluiga.</span><span class="sxs-lookup"><span data-stu-id="51004-106">Seen from a preventive maintenance perspective, it is important to monitor key information such as current condition, and remaining life span.</span></span> <span data-ttu-id="51004-107">Lisaks, kui teete seisundi hindamist korrapäraste ajavahemike järel, siis on teil võimalik jälgida ja võrrelda tingimusi masinatel oma tehases.</span><span class="sxs-lookup"><span data-stu-id="51004-107">Furthermore, if you carry out condition assessment at regular intervals, you will be able to monitor and compare conditions on the machinery in your factory.</span></span>

<span data-ttu-id="51004-108">Seisundi hindamist saab kasutada, et mõõta ja jälgida paljusid tingimusi teie seadmetel.</span><span class="sxs-lookup"><span data-stu-id="51004-108">Condition assessment can be used to measure and monitor many conditions on your equipment.</span></span> <span data-ttu-id="51004-109">Näide: te võite mõõta oma masinate vibratsioone.</span><span class="sxs-lookup"><span data-stu-id="51004-109">Example: You could measure vibrations on your machinery.</span></span> <span data-ttu-id="51004-110">Pärast seda, kui olete registreerinud vibratsiooni mõõtmised varahalduses eri tüüpi seadmete kohta, saate otsida viimaseid registreeritud hinnangut ja vaadata vibratsiooni mõõtmisi.</span><span class="sxs-lookup"><span data-stu-id="51004-110">After you have registered vibration measurements in Asset Management on various types of equipment, you can search for the latest registered assessment and view vibration measurements.</span></span>

<span data-ttu-id="51004-111">Seisundi hindamine on loodud varadele.</span><span class="sxs-lookup"><span data-stu-id="51004-111">Condition assessment is created on assets.</span></span> <span data-ttu-id="51004-112">Enne tingimuse hindamise protseduuri tegemist seadistage vara tüübi seisundi hindamise mall.</span><span class="sxs-lookup"><span data-stu-id="51004-112">You set up a condition assessment template on an asset type before you carry out the condition assessment procedure.</span></span> <span data-ttu-id="51004-113">Põhjus mallide kasutamiseks seisundi hindamisel on vältida sarnaste varade tingimusandmete varieerumist.</span><span class="sxs-lookup"><span data-stu-id="51004-113">The reason for using templates for condition assessment is to avoid variation of condition data on similar assets.</span></span> <span data-ttu-id="51004-114">Seisundi hindamise seadistamise ja kasutamise järjestus varahalduses on järgmine: esmalt seadistage nõutavad seisundi hindamise mallid.</span><span class="sxs-lookup"><span data-stu-id="51004-114">The sequence for setting up and using condition assessment in Asset Management is: First you set up the required condition assessment templates.</span></span> <span data-ttu-id="51004-115">Järgmisena seostage mallid varade tüüpidega vormil **Varade tüübid**.</span><span class="sxs-lookup"><span data-stu-id="51004-115">Next, you associate templates with asset types in the **Asset types** form.</span></span> <span data-ttu-id="51004-116">Lõpuks saate luua seisundi hindamise registreerimisi vara kohta vormil **Vara**.</span><span class="sxs-lookup"><span data-stu-id="51004-116">Finally, you can create condition assessment registrations on an asset in the **Asset** form.</span></span>

## <a name="create-a-condition-assessment-template"></a><span data-ttu-id="51004-117">Seisundi hindamismalli loomine</span><span class="sxs-lookup"><span data-stu-id="51004-117">Create a condition assessment template</span></span>

1. <span data-ttu-id="51004-118">Valige **Varahaldus** > **Häälestus** > **Varade tüübid** > **Seisundi hindamine**.</span><span class="sxs-lookup"><span data-stu-id="51004-118">Select **Asset management** > **Setup** > **Asset types** > **Condition assessment**.</span></span>
2. <span data-ttu-id="51004-119">Valige uue malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="51004-119">Select **New** to create a new template.</span></span>
3. <span data-ttu-id="51004-120">Sisestage malli ID väljale **Mall**.</span><span class="sxs-lookup"><span data-stu-id="51004-120">Insert and ID for the template in the **Template** field.</span></span>
4. <span data-ttu-id="51004-121">Sisestage malli nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="51004-121">Insert a name for the template in the **Name** field.</span></span>
5. <span data-ttu-id="51004-122">Lisage kiirkaardile **Seisundi hindamise read** nõutavad read seisundi hindamiseks, sealhulgas sobiva tingimuse tüüp ja mõõtühik.</span><span class="sxs-lookup"><span data-stu-id="51004-122">On the **Condition assessment lines** FastFab, add the lines required for the condition assessment, including selection of the appropriate condition type and measurement unit.</span></span>
6. <span data-ttu-id="51004-123">Kiirkaardile **Vara tüübid** lisage vara tüübid, mille puhul peaks kasutama tingimuse hindamise malli.</span><span class="sxs-lookup"><span data-stu-id="51004-123">On the **Asset types** FastTab, add the asset types that should use the condition assessment template.</span></span>
7. <span data-ttu-id="51004-124">Väljadel **Read** ja **Vara tüübid** lehe ülaosas rühmas **Üksikasjad** kuvatakse valitud tingimuse hindamismalliga seotud hinnanguridade ja varatüüpide arv.</span><span class="sxs-lookup"><span data-stu-id="51004-124">In the **Lines** and **Asset types** fields in the **Details** group at the top of the screen, you will see the number of assessment lines and asset types related to the selected condition assessment template.</span></span>


## <a name="create-condition-assessment-registration-on-an-asset"></a><span data-ttu-id="51004-125">Vara seisundi hindamise registreerimise loomine</span><span class="sxs-lookup"><span data-stu-id="51004-125">Create condition assessment registration on an asset</span></span>

1. <span data-ttu-id="51004-126">Valige **Varahaldus** > **Ühised** > **Varad** > **Kõik varad**.</span><span class="sxs-lookup"><span data-stu-id="51004-126">Select **Asset management** > **Common** > **Assets** > **All Assets**.</span></span>
2. <span data-ttu-id="51004-127">Valige loendist või hankija, kellele soovite kontakti luua.</span><span class="sxs-lookup"><span data-stu-id="51004-127">In the list, select the asset for which you want to create a condition assessment registration.</span></span>
3. <span data-ttu-id="51004-128">Klõpsake vahekaardi **Üldine** nuppu **Hõlbustusvahendid**.</span><span class="sxs-lookup"><span data-stu-id="51004-128">On the **General** tab, click **Condition assessment**.</span></span>
4. <span data-ttu-id="51004-129">Uue reegli loomiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="51004-129">Click **New** to make a new registration.</span></span>
5. <span data-ttu-id="51004-130">Valige seisundi hindamise kuupäev väljal **Kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="51004-130">Select the date for the condition assessment in the **Date** field.</span></span>
6. <span data-ttu-id="51004-131">Valige töötaja nimi, kes tegi hinnangu registreerimise väljal **Töötaja**.</span><span class="sxs-lookup"><span data-stu-id="51004-131">Select the name of the worker who carried out the assessment registration in the **Worker** field.</span></span>
7. <span data-ttu-id="51004-132">Väljal **Read** näete seisundi hindamisel seadistatud hindamisridade arvu.</span><span class="sxs-lookup"><span data-stu-id="51004-132">In the **Lines** field, you see the number of assessment lines set up on the condition assessment.</span></span>
8. <span data-ttu-id="51004-133">Valige mall seisundi hindamiseks väljal **Mall**.</span><span class="sxs-lookup"><span data-stu-id="51004-133">Select a template for the condition assessment in the **Template** field.</span></span> <span data-ttu-id="51004-134">Malli nimi sisestatakse automaatselt väljale **Nimi** ja seotud registreerimisread sisestatakse kiirkaardile **Seisundi hindamise read**.</span><span class="sxs-lookup"><span data-stu-id="51004-134">The name of the template is automatically inserted in the **Name** field, and the related registration lines are inserted on the **Condition assessment lines** FastTab.</span></span>
9. <span data-ttu-id="51004-135">Kiirkaardile **Märkmed** saate sisestada valitud seisundi hindamisega seotud märkmeid.</span><span class="sxs-lookup"><span data-stu-id="51004-135">You can insert notes relating to the selected condition assessment on the **Notes** FastTab.</span></span>
10. <span data-ttu-id="51004-136">Iga seisundi hindamise rea kohta sisestage mõõtmisandmed väljale **Väärtus**.</span><span class="sxs-lookup"><span data-stu-id="51004-136">For each condition assessment line, insert measurement data in the **Value** field.</span></span>
11. <span data-ttu-id="51004-137">Saate sisestada valitud registreerimisreaga seotud kommentaari kiirkaardi **Seisundi hindamise read** väljale **Kommentaarid**.</span><span class="sxs-lookup"><span data-stu-id="51004-137">You can insert a comment relating to the selected registration line on the **Condition assessment lines** FastTab > **Comments** field.</span></span> <span data-ttu-id="51004-138">Kui lisate reale kommentaari, valitakse automaatselt märkeruut **Kommentaar**.</span><span class="sxs-lookup"><span data-stu-id="51004-138">If you add a comment on a line, the **Comment** check box is automatically selected.</span></span>

<span data-ttu-id="51004-139">Pärast seda, kui olete teinud seisundi hindamise registreerimise, saate seisundi hindamise aruande printida.</span><span class="sxs-lookup"><span data-stu-id="51004-139">After you have made a condition assessment registration on an asset, you can print a condition assessment report.</span></span>

>[!NOTE]
><span data-ttu-id="51004-140">Samuti saate registreerida seisundi hindamise töökäsul (**Varahaldus** > **Ühised** > **Töökäsud** > **Kõik töökäsud** > **Seisundi hindamise** nupp.)</span><span class="sxs-lookup"><span data-stu-id="51004-140">You can also register condition assessment on a work order (**Asset management** > **Common** > **Work orders** > **All Work orders** > **Condition assessment** button.)</span></span>
