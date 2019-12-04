---
title: Süsteemi määratletud ja kasutaja määratletud tabelipiirangud
description: 'See artikkel selgitab kahte toote konfiguratsioonimudeli komponentide tabelipiirangu tüüpi: kasutaja määratletud ja süsteemi määratletud. Tabelipiirangud kajastavad lubatud atribuudikombinatsioonide matriitse, kus iga rida määratleb ühe võimalike atribuudiväärtuste kogumi.'
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8fac49cde1a6098b99e6373bf9221d3357a053a2
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814509"
---
# <a name="system-defined-and-user-defined-table-constraints"></a><span data-ttu-id="ebe8f-104">Süsteemi määratletud ja kasutaja määratletud tabelipiirangud</span><span class="sxs-lookup"><span data-stu-id="ebe8f-104">System-defined and user-defined table constraints</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ebe8f-105">See artikkel selgitab kahte toote konfiguratsioonimudeli komponentide tabelipiirangu tüüpi: kasutaja määratletud ja süsteemi määratletud.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-105">This article explains the two types of table constraints for components in a product configuration model -  user-defined and system-defined.</span></span> <span data-ttu-id="ebe8f-106">Tabelipiirangud kajastavad lubatud atribuudikombinatsioonide matriitse, kus iga rida määratleb ühe võimalike atribuudiväärtuste kogumi.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-106">Table constraints represent matrices of the allowed attribute combinations, where each row defines one set of possible attribute values.</span></span>

<span data-ttu-id="ebe8f-107">Tabelipiirangud tähistavad toote konfiguratsioonimudelisse kuuluvate komponentide puhul lubatud atribuudikombinatsioonide maatrikseid.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-107">Table constraints represent matrices of the combinations of attributes that are allowed for components in a product configuration model.</span></span> <span data-ttu-id="ebe8f-108">Tabeli iga rida määratleb ühe võimalike atribuudiväärtuste komplekti.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-108">Each row in the table defines one set of possible attribute values.</span></span> <span data-ttu-id="ebe8f-109">Saate toote konfiguratsioonimudelis deklareerida kaht tüüpi piiranguid.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-109">You can declare two types of constraints in a product configuration model:</span></span>

-   <span data-ttu-id="ebe8f-110">**Avaldisepiirang** – saate luua avaldise, mis määratleb atribuutide vahelised seosed, et toote konfigureerimisel oleks võimalik valida ainult ühilduvaid väärtusi.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-110">**Expression constraint** – Create an expression that defines relations between attributes to guarantee that only compatible values can be selected during product configuration.</span></span>
-   <span data-ttu-id="ebe8f-111">**Tabelipiirangu** – saate luua tabeli, mis määratleb kõik määratud atribuudikomplekti puhul lubatud kombinatsioonid.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-111">**Table constraint** – Create a table that defines all the combinations that are allowed for a specified set of attributes.</span></span> <span data-ttu-id="ebe8f-112">Saadaval on kaht tüüpi tabelipiiranguid: kasutaja määratletud tabelipiirangud ja süsteemi määratletud tabelipiirangud.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-112">Two types of table constraints are available: user-defined table constraints and system-defined table constraints.</span></span>

<span data-ttu-id="ebe8f-113">See artikkel kirjeldab toote konfiguratsioonimudelisse kuuluvate komponentide kasutaja määratletud ja süsteemi määratletud tabelipiiranguid.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-113">This article describes user-defined and system-defined table constraints for components in a product configuration model.</span></span>

## <a name="user-defined-table-constraints"></a><span data-ttu-id="ebe8f-114">Kasutaja määratletud tabelipiirangud</span><span class="sxs-lookup"><span data-stu-id="ebe8f-114">User-defined table constraints</span></span>
<span data-ttu-id="ebe8f-115">Kasutaja määratletud tabelipiirang on teatud tüüpi maatriks, mida kasutatakse atribuuditüüpidega määratletud atribuudiväärtuste kombinatsiooni kirjeldamiseks.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-115">A user-defined table constraint is a type of matrix that is used to describe the combinations of attribute values that are defined by attribute types.</span></span> <span data-ttu-id="ebe8f-116">Näiteks kui toodate kõlareid, saate kasutaja määratud tabelipiirangus lisada korpuseviimistluse ja esivõre jaoks kaks veergu.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-116">For example, if you produce speakers, you can include columns for the cabinet finish and the front grill in the user-defined table constraint.</span></span> <span data-ttu-id="ebe8f-117">Korpuseviimistluse atribuuditüübil on neli väärtust ja esivõre atribuuditüübil on kolm väärtust.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-117">The attribute type for the cabinet finish has four values, and the attribute type for the front grill has three values.</span></span> <span data-ttu-id="ebe8f-118">Seetõttu on piirangute puudumisel võimalikud 4 x 3 = 12 kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-118">Therefore, if constraints aren't used, there are 4 × 3 = 12 possible combinations.</span></span> <span data-ttu-id="ebe8f-119">Selles näites on aga lubatud ainult kuus kombinatsiooni, nagu näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-119">However, in this example, only six combinations are allowed, as shown in the following table.</span></span> <span data-ttu-id="ebe8f-120">See teave kuvatakse lehe **Tabelipiirangu redigeerimine** vahekaardil **Lubatud kombinatsioonid**.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-120">This information is displayed on the **Allowed combinations** tab on the **Edit table constraint** page.</span></span>

| <span data-ttu-id="ebe8f-121">Kabinetiviimistlus</span><span class="sxs-lookup"><span data-stu-id="ebe8f-121">Cabinet finish</span></span> | <span data-ttu-id="ebe8f-122">Esivõre</span><span class="sxs-lookup"><span data-stu-id="ebe8f-122">Front grill</span></span> |
|----------------|-------------|
| <span data-ttu-id="ebe8f-123">Must</span><span class="sxs-lookup"><span data-stu-id="ebe8f-123">Black</span></span>          | <span data-ttu-id="ebe8f-124">Must</span><span class="sxs-lookup"><span data-stu-id="ebe8f-124">Black</span></span>       |
| <span data-ttu-id="ebe8f-125">Must</span><span class="sxs-lookup"><span data-stu-id="ebe8f-125">Black</span></span>          | <span data-ttu-id="ebe8f-126">Metall</span><span class="sxs-lookup"><span data-stu-id="ebe8f-126">Metal</span></span>       |
| <span data-ttu-id="ebe8f-127">Tamm</span><span class="sxs-lookup"><span data-stu-id="ebe8f-127">Oak</span></span>            | <span data-ttu-id="ebe8f-128">Must</span><span class="sxs-lookup"><span data-stu-id="ebe8f-128">Black</span></span>       |
| <span data-ttu-id="ebe8f-129">Roosipuu</span><span class="sxs-lookup"><span data-stu-id="ebe8f-129">Rosewood</span></span>       | <span data-ttu-id="ebe8f-130">Valge</span><span class="sxs-lookup"><span data-stu-id="ebe8f-130">White</span></span>       |
| <span data-ttu-id="ebe8f-131">Valge</span><span class="sxs-lookup"><span data-stu-id="ebe8f-131">White</span></span>          | <span data-ttu-id="ebe8f-132">Must</span><span class="sxs-lookup"><span data-stu-id="ebe8f-132">Black</span></span>       |
| <span data-ttu-id="ebe8f-133">Valge</span><span class="sxs-lookup"><span data-stu-id="ebe8f-133">White</span></span>          | <span data-ttu-id="ebe8f-134">Valge</span><span class="sxs-lookup"><span data-stu-id="ebe8f-134">White</span></span>       |

<span data-ttu-id="ebe8f-135">Kasutaja määratletud tabelipiirangud määratletakse staatilise tabelisisendiga, mis toimib sarnaselt avaldisepiiranguga.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-135">User-defined table constraints are defined by static table input that works the same way as an expression constraint.</span></span> <span data-ttu-id="ebe8f-136">Kasutaja määratletud tabelipiirangu kasutamise eelis on see, et tabeleid on sageli lihtsam luua, mõista ja hallata kui pikki avaldisepiiranguid.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-136">When you use a user-defined table constraint, the advantage is that tables are often easier to create, understand, and maintain than long expression constraints.</span></span>

## <a name="system-defined-table-constraints"></a><span data-ttu-id="ebe8f-137">Süsteemi määratletud tabelipiirangud</span><span class="sxs-lookup"><span data-stu-id="ebe8f-137">System-defined table constraints</span></span>
<span data-ttu-id="ebe8f-138">Süsteemi määratletud tabelipiirang loob tabeli atribuuditüübi ja välja vahele dünaamilise vastenduse.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-138">A system-defined table constraint creates a dynamic mapping between an attribute type and a field in a table.</span></span> <span data-ttu-id="ebe8f-139">Kui süsteemi määratletud tabelipiirangu sisaldub toote konfiguratsioonimudelis, tagab vastendamine, et atribuuditüübi asemel kuvatakse tabelis olevad andmed.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-139">When a system-defined table constraint is included in a product configuration model, the mapping guarantees that the data in the table is shown instead of the values of the attribute type.</span></span> <span data-ttu-id="ebe8f-140">Tulemuseks on dünaamiline piirang, kuna tabeli sisu saab muuta (nt teistes moodulites).</span><span class="sxs-lookup"><span data-stu-id="ebe8f-140">The result is a dynamic constraint, because the table contents can be modified (for example, by other modules).</span></span>  

<span data-ttu-id="ebe8f-141">Süsteemi määratletud tabelipiirangu loomisel saate valida tabeli, soovi korral määratleda kasutatava päringu ja seejärel seostada atribuuditüübid valitud tabeli väljadega.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-141">When you create a system-defined table constraint, you select a table, optionally define the query to use, and then associate attribute types to the fields in the selected table.</span></span> <span data-ttu-id="ebe8f-142">Väljade tüübid peavad ühtima atribuuditüüpide tüüpidega.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-142">The types of fields must match the types of attribute types.</span></span>  

<span data-ttu-id="ebe8f-143">Enne kui tabeli piirang saab toote konfiguratsioonimudelis jõustuda, tuleb tabeli piirang kaasata ühte mudeli kompondi piirangusse kaasata.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-143">Before a table constraint can take effect on a product configuration model, the table constraint must be included in a constraint on one of the model's components.</span></span> <span data-ttu-id="ebe8f-144">Protseduur on uue piirangu loomiseks, tabeli piirangu tüübi valimiseks ja seejärel kasutatava tabeli piirangu määratluse valimiseks.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-144">The procedure is to create a new constraint, select the table constraint type, and then select the table constraint definition to use.</span></span> <span data-ttu-id="ebe8f-145">Viimaks tuleb kõik tabelipiirangu väljad vastendada toote konfiguratsioonimudeli atribuutidega.</span><span class="sxs-lookup"><span data-stu-id="ebe8f-145">Finally, all fields in the table constraint must be mapped to attributes in the product configuration model.</span></span>

<a name="additional-resources"></a><span data-ttu-id="ebe8f-146">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ebe8f-146">Additional resources</span></span>
--------

[<span data-ttu-id="ebe8f-147">Toote konfiguratsioonimudelite ülevaade</span><span class="sxs-lookup"><span data-stu-id="ebe8f-147">Product configuration models overview</span></span>](product-configuration-models.md)



