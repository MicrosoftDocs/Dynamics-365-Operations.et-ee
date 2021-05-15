---
title: Mittevastavuste probleemitüübid
description: See teema kirjeldab, kuidas luua ja kasutada mittevastavuste probleemitüüpe.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df509365f5c900898921acfbda380b5e20c7a251
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956629"
---
# <a name="problem-types-for-nonconformances"></a><span data-ttu-id="79acc-103">Mittevastavuste probleemitüübid</span><span class="sxs-lookup"><span data-stu-id="79acc-103">Problem types for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79acc-104">See teema kirjeldab, kuidas luua ja kasutada mittevastavuste probleemitüüpe.</span><span class="sxs-lookup"><span data-stu-id="79acc-104">This topic describes how to create and use problem types for nonconformances.</span></span>

<span data-ttu-id="79acc-105">Kasutage lehte **Probleemi tüübid**, et määratleda erinevate mittevastavustüüpide jaoks tekkida võivate kvaliteediprobleemide klassifikatsioon.</span><span class="sxs-lookup"><span data-stu-id="79acc-105">You use the **Problem types** page to define a classification of the quality problems that might occur for the various nonconformance types.</span></span> <span data-ttu-id="79acc-106">Iga loodud probleemitüübi jaoks peate määrama mittevastavuste tüübid, millega probleemitüüpi saab kasutada.</span><span class="sxs-lookup"><span data-stu-id="79acc-106">For each problem type that you create, you must specify the types of nonconformances that the problem type can be used with.</span></span> <span data-ttu-id="79acc-107">Saate seadistada järgmisi mittevastavuste tüüpe:</span><span class="sxs-lookup"><span data-stu-id="79acc-107">You can set up the following nonconformance types:</span></span>

- <span data-ttu-id="79acc-108">**Sisemine** – Seda tüüpi mittevastavused on seotud vaba kaubavaruga (nt kvaliteettellimused või garantiitellimused).</span><span class="sxs-lookup"><span data-stu-id="79acc-108">**Internal** – Nonconformances of this type are related to on-hand inventory (for example, quality orders or quarantine orders).</span></span>
- <span data-ttu-id="79acc-109">**Klient** – Seda tüüpi mittevastavused on seotud müügitellimustega.</span><span class="sxs-lookup"><span data-stu-id="79acc-109">**Customer** – Nonconformances of this type are related to sales orders.</span></span>
- <span data-ttu-id="79acc-110">**Hankija** – Seda tüüpi mittevastavused on seotud ostutellimustega.</span><span class="sxs-lookup"><span data-stu-id="79acc-110">**Vendor** – Nonconformances of this type are related to purchase orders.</span></span>
- <span data-ttu-id="79acc-111">**Teenuse taotlus** – Seda tüüpi mittevastavused on seotud teenusetellimustega.</span><span class="sxs-lookup"><span data-stu-id="79acc-111">**Service request** – Nonconformances of this type are related to service orders.</span></span>
- <span data-ttu-id="79acc-112">**Tootmine** – Seda tüüpi mittevastavused on seotud partiitellimuste või tootmistellimustega.</span><span class="sxs-lookup"><span data-stu-id="79acc-112">**Production** – Nonconformances of this type are related to batch orders or production orders.</span></span>
- <span data-ttu-id="79acc-113">**Kaastoote tootmine** – Seda tüüpi mittevastavused on seotud kaastoodete partiitellimustega.</span><span class="sxs-lookup"><span data-stu-id="79acc-113">**Co-product production** – Nonconformances of this type are related to batch orders for co-products.</span></span>

<span data-ttu-id="79acc-114">Uue probleemitüübi loomisel valige tegevuspaanil **Mittevastavuse tüübid**, et luua loend ühest või enamast mittevastavuse tüübist, mis on probleemi tüübi jaoks autoriseeritud.</span><span class="sxs-lookup"><span data-stu-id="79acc-114">When you create a new problem type, select **Non conformance types** on the Action Pane to create a list of one or more nonconformance types that are authorized for the problem type.</span></span> <span data-ttu-id="79acc-115">Näiteks võib defektikoodiga seotud probleemitüüp kehtida kõigile mittevastavuse tüüpidele.</span><span class="sxs-lookup"><span data-stu-id="79acc-115">For example, a problem type that is related to a defect code might apply to all nonconformance types.</span></span> <span data-ttu-id="79acc-116">Siiski võib kliendikaebustega seotud probleemitüüpi rakenduda ainult **Klient** ja **Teenuse taotlus** mittevastavuse tüüpidele.</span><span class="sxs-lookup"><span data-stu-id="79acc-116">However, a problem type that is related to customer complaints might apply only to the **Customer** and **Service request** nonconformance types.</span></span>

## <a name="examples-of-problem-types"></a><span data-ttu-id="79acc-117">Probleemitüüpide näited</span><span class="sxs-lookup"><span data-stu-id="79acc-117">Examples of problem types</span></span>

<span data-ttu-id="79acc-118">Siin on mõned näited probleemi tüüpide stsenaariumidest, mida saab kasutada erinevate mittevastavuse tüüpidega:</span><span class="sxs-lookup"><span data-stu-id="79acc-118">Here are some examples of scenarios for problem types that can be used with the different nonconformance types:</span></span>

- <span data-ttu-id="79acc-119">**Klient:** Klient esitas kaebuse, klient tegi tagastuse või ei täidetud kvaliteedispetsifikatsioone.</span><span class="sxs-lookup"><span data-stu-id="79acc-119">**Customer:** A customer filed a complaint, a customer made a return, or quality specifications weren't met.</span></span>
- <span data-ttu-id="79acc-120">**Hankija:** Toode on kahjustatud, kvaliteedispetsifikatsioone ei täidetud või saadi vale toode.</span><span class="sxs-lookup"><span data-stu-id="79acc-120">**Vendor:** The product was damaged, quality specifications weren't met, or the wrong product was received.</span></span>
- <span data-ttu-id="79acc-121">**Teenuse taotlus:** Kvaliteedispetsifikatsioone ei täidetud, klient esitas kaebuse või nõutakse masina hooldust.</span><span class="sxs-lookup"><span data-stu-id="79acc-121">**Service request:** Quality specifications weren't met, a customer filed a complaint, or machine maintenance is required.</span></span>
- <span data-ttu-id="79acc-122">**Tootmine:** Ei täidetud kvaliteedispetsifikatsioone, nõutakse masina hooldust või toode sai kahjustada.</span><span class="sxs-lookup"><span data-stu-id="79acc-122">**Production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>
- <span data-ttu-id="79acc-123">**Kaastoote tootmine:** Ei täidetud kvaliteedispetsifikatsioone, nõutakse masina hooldust või toode sai kahjustada.</span><span class="sxs-lookup"><span data-stu-id="79acc-123">**Co-product production:** Quality specifications weren't met, machine maintenance is required, or the product was damaged.</span></span>

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a><span data-ttu-id="79acc-124">Probleemi tüübi loomine ja selle mittevastavuse tüüpidele määramine</span><span class="sxs-lookup"><span data-stu-id="79acc-124">Create a problem type and assign it to nonconformance types</span></span>

1. <span data-ttu-id="79acc-125">Avage **Laohaldus \> Seadistus \> Kvaliteedijuhtimine \> Probleemi tüübid**.</span><span class="sxs-lookup"><span data-stu-id="79acc-125">Go to **Inventory management \> Setup \> Quality management \> Problem types**.</span></span>
1. <span data-ttu-id="79acc-126">Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="79acc-126">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="79acc-127">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="79acc-127">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="79acc-128">**Probleemi tüüp** – Sisestage probleemitüübi kordumatu ID või nimi.</span><span class="sxs-lookup"><span data-stu-id="79acc-128">**Problem type** – Enter a unique ID or name for the problem type.</span></span>
    - <span data-ttu-id="79acc-129">**Kirjeldus** – Sisestage probleemi tüübi detailne kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="79acc-129">**Description** – Enter a detailed description of the problem type.</span></span>

1. <span data-ttu-id="79acc-130">Kui uus rida on endiselt valitud, valige tegevuspaanil **mittevastavuse tüübid**.</span><span class="sxs-lookup"><span data-stu-id="79acc-130">While the new row is still selected, select **Non conformance types** on the Action Pane.</span></span>
1. <span data-ttu-id="79acc-131">Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="79acc-131">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="79acc-132">Seejärel seadistage uue rea jaoks **Mittevastavuse tüüp** väli mittevastavuse tüübi jaoks, mida soovite probleemi tüübi jaoks lubada.</span><span class="sxs-lookup"><span data-stu-id="79acc-132">Then, for the new row, set the **Non conformance type** field to the nonconformance type that you want to allow for the problem type.</span></span>
1. <span data-ttu-id="79acc-133">Korrake eelmist sammu iga täiendava mittevastavuse tüübi korral, mida soovite probleemi tüübile autoriseerida.</span><span class="sxs-lookup"><span data-stu-id="79acc-133">Repeat the previous step for each additional nonconformance type that you want to authorize for the problem type.</span></span>
1. <span data-ttu-id="79acc-134">Sulgege lehed.</span><span class="sxs-lookup"><span data-stu-id="79acc-134">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="79acc-135">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="79acc-135">Additional resources</span></span>

- [<span data-ttu-id="79acc-136">Kvaliteedijuhtimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="79acc-136">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="79acc-137">Kvaliteedi ja mittevastavuse haldamise lubamine</span><span class="sxs-lookup"><span data-stu-id="79acc-137">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="79acc-138">Mittevastavuste kinnitamise eest vastutavad töötajad</span><span class="sxs-lookup"><span data-stu-id="79acc-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="79acc-139">Mittevastavuste garantiitsoonid</span><span class="sxs-lookup"><span data-stu-id="79acc-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="79acc-140">Mittevastavuste diagnostika tüübid</span><span class="sxs-lookup"><span data-stu-id="79acc-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="79acc-141">Kvaliteeditasud mittevastavustele</span><span class="sxs-lookup"><span data-stu-id="79acc-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="79acc-142">MIttevastavuste toimingud</span><span class="sxs-lookup"><span data-stu-id="79acc-142">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="79acc-143">Laoprotsesside kvaliteedijuhtimine</span><span class="sxs-lookup"><span data-stu-id="79acc-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
