---
title: Hankija maksete kinnipidamise tingimuste loomine ja rakendamine
description: Selles teemas antakse teavet hankija maksete kinnipidamise tingimuste seadistamise ja haldamise kohta.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410213"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="e1eb6-103">Hankija maksete kinnipidamise tingimuste loomine ja rakendamine</span><span class="sxs-lookup"><span data-stu-id="e1eb6-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="e1eb6-104">Projekti jaoks hankija maksete kinnipidamise tingimuste seadistamine on kasulik, kui teie organisatsioon soovib pidada kinni osa hankijale tehtavatest maksetest.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="e1eb6-105">Näiteks kui soovite pidada hankijale tehtava makse kinni seni, kuni tarnitud tooted vastavad teie ootustele.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="e1eb6-106">Hankija maksete kinnipidamise tingimused saate täpsustada hankija lepingu tingimuste läbirääkimisel.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="e1eb6-107">Hankija makse kinnipidamise tingimuste loomine</span><span class="sxs-lookup"><span data-stu-id="e1eb6-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="e1eb6-108">Saate sisestada kinnipeetava hankija makse protsendimäära ja vabastatavate, eelnevalt kinnipeetud summade protsendimäära.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="e1eb6-109">Summad peetakse automaatselt hankija arvelt kinni, kuni leping jõuab määratud etappi.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="e1eb6-110">Pärast hankija makse kinnipidamise tingimuste seadistamist saate neid rakendada mis tahes projektide puhul, millega hankija töötab.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="e1eb6-111">Hankija maksete kinnipidamise tingimuste seadistamiseks ja haldamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="e1eb6-112">Avage **Projektihaldus ja raamatupidamine** > **Kinnipidamine** > **Hankija maksete kinnipidamise tingimused**.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="e1eb6-113">Valige **Uus**, et lisada uus hankija maksete kinnipidamise tingimus.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="e1eb6-114">Uue tingimuse **Reegli ID** väärtus sisestatakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="e1eb6-115">Sisestage väljale **Kirjeldus** lühike kirjeldus ja valige kiirkaardil **Tingimused** suvand **Lisa rida**, et lisada järgmised tingimuste väärtused.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="e1eb6-116">**Tarnitud ühikute protsendimäär**: sisestage tingimuse täitmise protsent.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="e1eb6-117">Summad peetakse automaatselt hankija arvetest kinni, kuni projekti lõpuleviimine on jõudnud etappi, mis on võrdne kehtestatud protsendimääraga.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="e1eb6-118">Näiteks kui sisestate 50,00, peetakse summasid kinni seni, kuni projekt on 50 protsenti täidetud.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="e1eb6-119">**Kinnipeetav protsendimäär**: sisestage hankija arvest kinnipeetava summa protsendimäär.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="e1eb6-120">Näiteks kui sisestate sellele väljale 10,00, siis peetakse hankija arvest kinni 10 protsenti summast, kuni projekt jõuab täitmisprotsendini, mille valisite väljal **Tarnitud ühikute protsendimäär**.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="e1eb6-121">**Vabastatav protsendimäär**: valige suvand **Lisa rida**, et lisada eelnevalt kinnipeetud summade protsendimäär, mida soovite vabastada valitud projekti täitmise tasemel.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="e1eb6-122">Kui teil on projekti erinevate tasemete täitmisel mitu vahe-eesmärki, sisestage iga kinnipidamise reegli jaoks eraldi hankija makse kinnipidamise tingimus.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="e1eb6-123">Igale reale saate määrata erineva kinnipeetava protsendimäära ja iga projekti taseme täitmisel vabastatava protsendimäära.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="e1eb6-124">Pärast hankija jaoks hankija makse kinnipidamise tingimuste loomist saate neid tingimusi projektis rakendada.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="e1eb6-125">Projektis hankija kinnipidamise tingimuste rakendamine</span><span class="sxs-lookup"><span data-stu-id="e1eb6-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="e1eb6-126">Avage **Projektihaldus ja raamatupidamine** > **Projektid** > **Kõik projektid** ja avage projektide loetelu lehel projekti vorm.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="e1eb6-127">Klõpsake kiirkaardil **Hankija lepingud** valikut **Lisa rida**.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="e1eb6-128">Tehke väljal **Konto kood** üks järgmistest valikutest.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="e1eb6-129">**Tabel**: hankija makse kinnipidamise tingimused kehtivad ühele hankijale.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="e1eb6-130">**Grupp**: hankija makse kinnipidamise tingimused kehtivad kõikidele hankijagrupi hankijatele.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="e1eb6-131">**Kõik**: hankija makse kinnipidamise tingimused kehtivad kõikidele hankijatele.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="e1eb6-132">Valige väljal **Hankija/hankijagrupp** hankija või hankijagrupp, kellele hankija makse kinnipidamise tingimused kehtivad.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="e1eb6-133">Kui tegite eelmises etapis valiku **Kõik**, siis ei ole see väli saadaval.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="e1eb6-134">Väljal **Hankija makse kinnipidamise tingimused** valige kinnipidamise tingimused, mille olete eelneva protsessi käigus loonud.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="e1eb6-135">Kui projekti puhul on seadistatud ka hankija maksmisel tasumise tingimused, sisestage väljale **Maksmisel tasumise künnise protsendimäär** projekti künnise protsendimäär.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="e1eb6-136">Hankija makse kinnipidamise tingimused kuvatakse ka hankijale loodavates ostutellimustes.</span><span class="sxs-lookup"><span data-stu-id="e1eb6-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
