---
title: Mittevastavuste kinnitamise eest vastutavad töötajad
description: See teema kirjeldab, kuidas konfigureerida mittevastavuste kinnitamise eest vastutavaid töötajaid.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d3f647de2c188661c2c9c5f31e2642c3f8ca0b5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021776"
---
# <a name="workers-responsible-for-approving-nonconformances"></a><span data-ttu-id="7faec-103">Mittevastavuste kinnitamise eest vastutavad töötajad</span><span class="sxs-lookup"><span data-stu-id="7faec-103">Workers responsible for approving nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7faec-104">See teema kirjeldab, kuidas konfigureerida mittevastavuste kinnitamise eest vastutavaid töötajaid.</span><span class="sxs-lookup"><span data-stu-id="7faec-104">This topic describes how to configure workers that are responsible for approving nonconformances.</span></span>

<span data-ttu-id="7faec-105">Mittevastavused tuleb heaks kiita, enne kui kasutajad saavad sisestada üksikasju nagu parandused või toimingud.</span><span class="sxs-lookup"><span data-stu-id="7faec-105">Nonconformances must be approved before users can start to enter details such as corrections or operations.</span></span> <span data-ttu-id="7faec-106">Enne kui kasutajad saavad mittevastavusi kinnitada või tagasi lükata, peab nende kasutaja ID (kasutajakirje) olema lingitud töötaja kirjega.</span><span class="sxs-lookup"><span data-stu-id="7faec-106">Before users can approve or reject nonconformances, their user ID (user record) must be linked to a worker record.</span></span> <span data-ttu-id="7faec-107">Saate valikuliselt konfigureerida kvaliteedi eest vastutavaid töötajaid ja seejärel lubada ühel töötajal kinnitada töö teise töötaja nimel.</span><span class="sxs-lookup"><span data-stu-id="7faec-107">You can optionally configure workers that are responsible for quality and then allow one worker to approve work on behalf of another worker.</span></span>

## <a name="enable-a-user-for-nonconformance-processing"></a><span data-ttu-id="7faec-108">Luba kasutajal mittevastavuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="7faec-108">Enable a user for nonconformance processing</span></span>

<span data-ttu-id="7faec-109">Enne kui kasutaja saab mittevastavusi kinnitada või tagasi lükata, peab tema kasutaja ID (kasutajakirje) olema lingitud töötaja kirjega.</span><span class="sxs-lookup"><span data-stu-id="7faec-109">Before a user can approve or reject nonconformances, you must link their user record to a worker record.</span></span> <span data-ttu-id="7faec-110">Kinnitamise väljad saab seejärel automaatselt seadistada ja praeguse kasutaja saab ajatabelisse automaatselt lisada.</span><span class="sxs-lookup"><span data-stu-id="7faec-110">The approval fields can then be automatically set, and the current user can be automatically filled in for the timesheet.</span></span> <span data-ttu-id="7faec-111">Dokumendi märkuste kasutamiseks peab kasutajal olema kasutajasuvandites aktiveeritud suvand Dokumenditöötlus.</span><span class="sxs-lookup"><span data-stu-id="7faec-111">Before the user can use the document notes, you must activate document handling in their user options.</span></span>

1. <span data-ttu-id="7faec-112">Minge jaotisse **Süsteemihaldus \> Kasutajad \> Kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="7faec-112">Go to **System administration \> Users \> Users**.</span></span>
1. <span data-ttu-id="7faec-113">Otsige ja avage kasutaja, kes peaks saama mittevastavusi kinnitada või tagasi lükata.</span><span class="sxs-lookup"><span data-stu-id="7faec-113">Find and open the user who should be able to approve or reject nonconformances.</span></span>
1. <span data-ttu-id="7faec-114">Seadke **Isik** väljale praeguse kasutajakirjega seotud töötaja nimi.</span><span class="sxs-lookup"><span data-stu-id="7faec-114">Set the **Person** field to the name of the worker that is related to the current user record.</span></span>
1. <span data-ttu-id="7faec-115">Tegevuspaanil valige **Kasutaja suvandid**.</span><span class="sxs-lookup"><span data-stu-id="7faec-115">On the Action Pane, select **User options**.</span></span>
1. <span data-ttu-id="7faec-116">Praeguse kasutajakirje **Suvandid** lehel seadke vahekaardil **Eelistused** suvandi **Luba dokumendi käsitlemine** väärtuseks *Jah*.</span><span class="sxs-lookup"><span data-stu-id="7faec-116">On the **Options** page for the current user record, on the **Preferences** tab, set the **Enable document handling** option to *Yes*.</span></span>
1. <span data-ttu-id="7faec-117">Sulgege lehed.</span><span class="sxs-lookup"><span data-stu-id="7faec-117">Close the pages.</span></span>

## <a name="define-workers-that-are-responsible-for-quality"></a><span data-ttu-id="7faec-118">Kvaliteedi eest vastutavate töötajate määratlemine</span><span class="sxs-lookup"><span data-stu-id="7faec-118">Define workers that are responsible for quality</span></span>

1. <span data-ttu-id="7faec-119">Avage **Varude haldus \> Seadistus \> Kvaliteedijuhtimine \> Kvaliteedi vastutavad töötajad**.</span><span class="sxs-lookup"><span data-stu-id="7faec-119">Go to **Inventory management \> Setup \> Quality control \> Workers responsible for quality**.</span></span>
2. <span data-ttu-id="7faec-120">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="7faec-120">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="7faec-121">Väljal **Töötaja** valige töötaja, kes sisestab kvaliteediandmed.</span><span class="sxs-lookup"><span data-stu-id="7faec-121">In the **Worker** field, select the worker that enters quality data.</span></span>
4. <span data-ttu-id="7faec-122">Väljal **Vastutav töötaja** valige töötaja, kelle nimel valitud töötaja töö sisestab.</span><span class="sxs-lookup"><span data-stu-id="7faec-122">In the **Worker responsible** field, select the worker that the selected worker enters work on behalf of.</span></span> <span data-ttu-id="7faec-123">Kui mittevastavused on loodud ja värskendatud, sisestatakse see töötaja vaikimisi **Töötaja** väljadele.</span><span class="sxs-lookup"><span data-stu-id="7faec-123">When nonconformances are created and updated, this worker will be entered by default in **Worker** fields.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7faec-124">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="7faec-124">Additional resources</span></span>

- [<span data-ttu-id="7faec-125">Kvaliteedijuhtimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="7faec-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="7faec-126">Kvaliteedi ja mittevastavuse haldamise lubamine</span><span class="sxs-lookup"><span data-stu-id="7faec-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="7faec-127">Kvaliteedikulud</span><span class="sxs-lookup"><span data-stu-id="7faec-127">Quality charges</span></span>](quality-charges.md)
- [<span data-ttu-id="7faec-128">Mittevastavuste garantiitsoonid</span><span class="sxs-lookup"><span data-stu-id="7faec-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="7faec-129">Mittevastavuste diagnostika tüübid</span><span class="sxs-lookup"><span data-stu-id="7faec-129">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="7faec-130">Kvaliteeditasud mittevastavustele</span><span class="sxs-lookup"><span data-stu-id="7faec-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="7faec-131">MIttevastavuste toimingud</span><span class="sxs-lookup"><span data-stu-id="7faec-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="7faec-132">Laoprotsesside kvaliteedijuhtimine</span><span class="sxs-lookup"><span data-stu-id="7faec-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
