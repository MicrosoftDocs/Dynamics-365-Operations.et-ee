---
title: Kvaliteedi ja mittevastavuse haldamise lubamine
description: See teema annab ülevaate protsessist kvaliteedi ja mittevastavuse haldus funktsioonide seadistamiseks ja konfigureerimiseks Microsoftis Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d5da648e31d07d054246f5d308a6c6cdeb506c
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956250"
---
# <a name="enable-quality-and-nonconformance-management"></a><span data-ttu-id="94d05-103">Kvaliteedi ja mittevastavuse haldamise lubamine</span><span class="sxs-lookup"><span data-stu-id="94d05-103">Enable quality and nonconformance management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94d05-104">See teema annab ülevaate protsessist kvaliteedi ja mittevastavuse haldus funktsioonide seadistamiseks ja konfigureerimiseks Microsoftis Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="94d05-104">This topic provides an overview of the process for setting up and configuring quality and nonconformance management features in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a><span data-ttu-id="94d05-105">Kvaliteedi ja mittevastavuse haldamise lubamine</span><span class="sxs-lookup"><span data-stu-id="94d05-105">Enable quality and nonconformance management</span></span>

<span data-ttu-id="94d05-106">Järgige neid samme, et lubada kvaliteedijuhtimine oma süsteemis.</span><span class="sxs-lookup"><span data-stu-id="94d05-106">Follow these steps to enable quality management on your system.</span></span>

1. <span data-ttu-id="94d05-107">Avage **Varude haldus \> Seadistus \> Varude ja laohalduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="94d05-107">Go to **Inventory management \> Setup \> Inventory and warehouse management parameters**.</span></span>
1. <span data-ttu-id="94d05-108">Seadke vahekaardil **Kvaliteedijuhtimine** suvandi **Kasuta kvaliteedijuhtimist** väärtuseks *Jah*.</span><span class="sxs-lookup"><span data-stu-id="94d05-108">On the **Quality management** tab, set the **Use quality management** option to *Yes*.</span></span>
1. <span data-ttu-id="94d05-109">Sisestage väljale **Tunnimäär** tunnitasu kohalikus valuutas.</span><span class="sxs-lookup"><span data-stu-id="94d05-109">In the **Hourly rate** field, enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="94d05-110">Tunnimäära kasutatakse mittevastavusega seotud toimingute kulude arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="94d05-110">The hourly rate is used to calculate costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="94d05-111">Tunnimäär ja arvutatud kulud annavad viiteteavet mittevastavuse kohta.</span><span class="sxs-lookup"><span data-stu-id="94d05-111">The hourly rate and calculated costs provide reference information for a nonconformance.</span></span> <span data-ttu-id="94d05-112">Need ei mõjuta teisi funktsioone.</span><span class="sxs-lookup"><span data-stu-id="94d05-112">They don't interact with other functionality.</span></span>
1. <span data-ttu-id="94d05-113">Valige **Aruande seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="94d05-113">Select **Report setup**.</span></span>
1. <span data-ttu-id="94d05-114">Lisage erinevatele aruande tüüpidele uued read ja valige dokumenditüüp, mida igas aruandes kasutada.</span><span class="sxs-lookup"><span data-stu-id="94d05-114">Add new lines for the various report types, and select the type of document to use for each report.</span></span>
1. <span data-ttu-id="94d05-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="94d05-115">Close the page.</span></span>
1. <span data-ttu-id="94d05-116">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="94d05-116">Close the page.</span></span>

## <a name="quality-management-configuration-process"></a><span data-ttu-id="94d05-117">Kvaliteedijuhtimise konfigureerimisprotsess</span><span class="sxs-lookup"><span data-stu-id="94d05-117">Quality management configuration process</span></span>

<span data-ttu-id="94d05-118">Enne kui saate alustada kvaliteedijuhtimise funktsioonide kasutamist ja luua kvaliteettellimusi, peate konfigureerima süsteemi ja selle eeltingimusi.</span><span class="sxs-lookup"><span data-stu-id="94d05-118">Before you can start to use the quality management features and generate quality orders, you must configure the system and prerequisites.</span></span> <span data-ttu-id="94d05-119">Siin on nimekiri sammudest, mis on vajalikud kvaliteedijuhtimise konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="94d05-119">Here is a list of the steps that are required to configure quality management.</span></span>

1. <span data-ttu-id="94d05-120">[Kvaliteedi ja mittevastavuse haldamise lubamine](#enable-qm).</span><span class="sxs-lookup"><span data-stu-id="94d05-120">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="94d05-121">Valikuline: [Testvahendite konfigureerimine](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="94d05-121">Optional: [Configure test instruments](quality-test-instruments.md).</span></span>
1. <span data-ttu-id="94d05-122">[Testide konfigureerimine](quality-tests.md).</span><span class="sxs-lookup"><span data-stu-id="94d05-122">[Configure tests](quality-tests.md).</span></span>
1. <span data-ttu-id="94d05-123">[Konfigureerige testi muutujad ja tulemused](quality-test-variables.md).</span><span class="sxs-lookup"><span data-stu-id="94d05-123">[Configure test variables and outcomes](quality-test-variables.md).</span></span>
1. <span data-ttu-id="94d05-124">[Konfigureerige testgrupid](quality-test-groups.md).</span><span class="sxs-lookup"><span data-stu-id="94d05-124">[Configure test groups](quality-test-groups.md).</span></span>
1. <span data-ttu-id="94d05-125">Valikuline: [konfigureerige kvaliteedigrupid ja linkige toodetega](quality-groups.md).</span><span class="sxs-lookup"><span data-stu-id="94d05-125">Optional: [Configure quality groups, and link to products](quality-groups.md).</span></span>
1. <span data-ttu-id="94d05-126">Valikuline: [konfigureerige kvaliteediseosed](quality-associations.md).</span><span class="sxs-lookup"><span data-stu-id="94d05-126">Optional: [Configure quality associations](quality-associations.md).</span></span>

<span data-ttu-id="94d05-127">Kui konfiguratsioon on lõpule viidud, saate alustada kvaliteettellimuste loomisest ja töötlemisest.</span><span class="sxs-lookup"><span data-stu-id="94d05-127">After the configuration is completed, you can start to create and process quality orders.</span></span> <span data-ttu-id="94d05-128">Lisateavet kvaliteeditellimuste loomise ja kasutamise kohta leiate teemast [Kvaliteeditellimused](quality-orders.md).</span><span class="sxs-lookup"><span data-stu-id="94d05-128">For more information about how to create and work with quality orders, see [Quality orders](quality-orders.md).</span></span>

## <a name="nonconformance-management-configuration-process"></a><span data-ttu-id="94d05-129">Mittevastavuse halduse konfigureerimisprotsess</span><span class="sxs-lookup"><span data-stu-id="94d05-129">Nonconformance management configuration process</span></span>

<span data-ttu-id="94d05-130">Enne kui saate alustada mittevastavuse halduse funktsioonide kasutamist ja luua mittevastavusi, peate konfigureerima süsteemi ja selle eeltingimusi.</span><span class="sxs-lookup"><span data-stu-id="94d05-130">Before you can start to use the nonconformance management features and generate nonconformances, you must configure the system and prerequisites.</span></span> <span data-ttu-id="94d05-131">Siin on nimekiri sammudest, mis on vajalikud mittevastavuste halduse konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="94d05-131">Here is a list of the steps that are required to configure nonconformance management.</span></span>

1. <span data-ttu-id="94d05-132">[Kvaliteedi ja mittevastavuse haldamise lubamine](#enable-qm).</span><span class="sxs-lookup"><span data-stu-id="94d05-132">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="94d05-133">[Mittevastavuste kinnitamise eest vastutavad töötajate konfigureerimine](quality-responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="94d05-133">[Configure workers who are responsible for approving nonconformances](quality-responsible-workers.md).</span></span>
1. <span data-ttu-id="94d05-134">[Konfigureerige probleemi tüübid](quality-problem-types.md).</span><span class="sxs-lookup"><span data-stu-id="94d05-134">[Configure problem types](quality-problem-types.md).</span></span>
1. <span data-ttu-id="94d05-135">[Saate konfigureerida vahelao tsoone](quality-quarantine-zones.md).</span><span class="sxs-lookup"><span data-stu-id="94d05-135">[Configure quarantine zones](quality-quarantine-zones.md).</span></span>
1. <span data-ttu-id="94d05-136">[Diagnostikatüüpide konfigureerimine](quality-diagnostic-types.md).</span><span class="sxs-lookup"><span data-stu-id="94d05-136">[Configure diagnostic types](quality-diagnostic-types.md).</span></span>
1. <span data-ttu-id="94d05-137">[Operatsioonide konfigureerimine](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="94d05-137">[Configure operations](quality-operations.md).</span></span>
1. <span data-ttu-id="94d05-138">Valikuline: [konfigureerige kvaliteeditasusid](quality-charges.md).</span><span class="sxs-lookup"><span data-stu-id="94d05-138">Optional: [Configure quality charges](quality-charges.md).</span></span>

<span data-ttu-id="94d05-139">Kui konfiguratsioon on lõpule viidud, saate alustada mittevastavuste loomise ja töötlemisega.</span><span class="sxs-lookup"><span data-stu-id="94d05-139">After the configuration is completed, you can start to create and process nonconformances.</span></span> <span data-ttu-id="94d05-140">Lisateavet lehel mittevastavuste loomise ja nendega töötamise kohta leiate teemast [Mittevastavuste loomine ja töötlemine](tasks/create-process-non-conformance.md).</span><span class="sxs-lookup"><span data-stu-id="94d05-140">For more information about how to create and work with nonconformances, see [Create and process nonconformances](tasks/create-process-non-conformance.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="94d05-141">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="94d05-141">Additional resources</span></span>

- [<span data-ttu-id="94d05-142">Kvaliteedijuhtimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="94d05-142">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="94d05-143">Kvaliteedi ja mittevastavuse haldamise lubamine</span><span class="sxs-lookup"><span data-stu-id="94d05-143">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="94d05-144">Laoprotsesside kvaliteedijuhtimine</span><span class="sxs-lookup"><span data-stu-id="94d05-144">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
