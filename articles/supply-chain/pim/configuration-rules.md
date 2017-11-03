---
title: Konfiguratsioonireeglid
description: "Selles artiklis antakse üldteavet konfiguratsioonireeglite kohta. Konfiguratsioonireeglid määratlevad koosluse kaupade vahelised seosed toodete puhul, mis kasutavad dimensioonipõhist konfiguratsioonitehnoloogiat."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 37f70d2620023915b23425d41dfb0043ef856492
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="configuration-rules"></a><span data-ttu-id="adf20-104">Konfiguratsioonireeglid</span><span class="sxs-lookup"><span data-stu-id="adf20-104">Configuration rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="adf20-105">Selles artiklis antakse üldteavet konfiguratsioonireeglite kohta.</span><span class="sxs-lookup"><span data-stu-id="adf20-105">This article provides general information about configuration rules.</span></span> <span data-ttu-id="adf20-106">Konfiguratsioonireeglid määratlevad koosluse kaupade vahelised seosed toodete puhul, mis kasutavad dimensioonipõhist konfiguratsioonitehnoloogiat.</span><span class="sxs-lookup"><span data-stu-id="adf20-106">Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.</span></span>

<span data-ttu-id="adf20-107">Konfiguratsioonireeglid on saadaval dimensioonipõhiste konfiguratsioonimudelite määratlemisel.</span><span class="sxs-lookup"><span data-stu-id="adf20-107">Configuration rules are available when you define dimension-based configuration models.</span></span> <span data-ttu-id="adf20-108">Konfiguratsioonireegleid kasutatakse koosluses kindlate kaubakombinatsioonide jõustamiseks või keelamiseks.</span><span class="sxs-lookup"><span data-stu-id="adf20-108">Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM).</span></span> <span data-ttu-id="adf20-109">Kui kooslus on loodud ja nende vastavatele konfiguratsioonigruppidele on asjakohased kaubad määratud, saab määratleda ühe või mitu konfiguratsioonireeglit.</span><span class="sxs-lookup"><span data-stu-id="adf20-109">After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined.</span></span> <span data-ttu-id="adf20-110">Kui kaks elementi kuuluvad kokku, kasutatakse kaasamise tagamiseks tehtemärki **Vali**.</span><span class="sxs-lookup"><span data-stu-id="adf20-110">If two items belong together, the **Select** operator is used to ensure inclusion.</span></span> <span data-ttu-id="adf20-111">Kui kaks kauba on teineteist välistavad, kasutatakse välistuse tagamiseks operaatorit **Tühista valik**.</span><span class="sxs-lookup"><span data-stu-id="adf20-111">If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion.</span></span>  

<span data-ttu-id="adf20-112">**Märkus.** See teave kehtib ainult dimensioonipõhist konfiguratsioonitehnoloogiat kasutavate tooteetalonide puhul.</span><span class="sxs-lookup"><span data-stu-id="adf20-112">**Note:** This information applies only to product masters that use the dimension-based configuration technology.</span></span>  

<span data-ttu-id="adf20-113">Olemasolevad konfiguratsioonid jäävad konfiguratsioonireeglite hilisemal muutmisel endisteks.</span><span class="sxs-lookup"><span data-stu-id="adf20-113">Existing configurations aren't affected by subsequent changes to the configuration rules.</span></span> <span data-ttu-id="adf20-114">Siiski on oluline seadistada reeglid enne uue konfiguratsiooni määratlemist ja need üle kontrollida, kui arvate, et reegleid on muudetud.</span><span class="sxs-lookup"><span data-stu-id="adf20-114">However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed.</span></span>  

<span data-ttu-id="adf20-115">**Märkus.** Meetod **Vali** tähendab, et tuletatud konfiguratsioonigrupp, kaubakood ja konfiguratsioon valitakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="adf20-115">**Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected.</span></span> <span data-ttu-id="adf20-116">Meetodi **Tühista valik** puhul ei saa tuletatud konfiguratsioonigruppi, kaubakoodi ja konfiguratsiooni valida.</span><span class="sxs-lookup"><span data-stu-id="adf20-116">For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.</span></span>

<a name="see-also"></a><span data-ttu-id="adf20-117">Vt ka</span><span class="sxs-lookup"><span data-stu-id="adf20-117">See also</span></span>
--------

[<span data-ttu-id="adf20-118">Dimensioonipõhine tootekonfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="adf20-118">Dimension-based product configuration</span></span>](dimension-based-product-configuration.md)




