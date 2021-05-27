---
title: Andmeväljade lisamine maksukonfiguratsioonidele
description: Käesolev teema kirjeldab maksukonfiguratsioonide kohandamist andmeväljade lisamise abil.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ebb186a4cb9ca61399909625233b579acd2c0ec5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022783"
---
# <a name="add-data-fields-in-tax-configurations"></a><span data-ttu-id="5cf1f-103">Andmeväljade lisamine maksukonfiguratsioonidele</span><span class="sxs-lookup"><span data-stu-id="5cf1f-103">Add data fields in tax configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5cf1f-104">See teema kirjeldab, kuidas kohandada maksu konfiguratsioone, kasutades [andmevälju, mis on lisatud maksuintegratsioonis](tax-service-add-data-fields-tax-integration-by-extension.md).</span><span class="sxs-lookup"><span data-stu-id="5cf1f-104">This topic explains how to customize tax configurations by using [data fields that are added in the tax integration](tax-service-add-data-fields-tax-integration-by-extension.md).</span></span>

## <a name="customize-the-tax-data-model"></a><span data-ttu-id="5cf1f-105">Maksuandmete mudeli kohandamine</span><span class="sxs-lookup"><span data-stu-id="5cf1f-105">Customize the tax data model</span></span>

1. <span data-ttu-id="5cf1f-106">Avage rakenduses Microsoft Dynamics 365 Finance jaotis **Elektrooniline aruandlus** \> **Maksukonfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-106">In Microsoft Dynamics 365 Finance, go to **Electronic Reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="5cf1f-107">Konfiguratsioonipuus valige **Maksuandmete mudel – Euroopa**.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-107">In the configuration tree, select **Tax Data Model - Europe**.</span></span> <span data-ttu-id="5cf1f-108">Valige toimingupaanilt suvand **Loo konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-108">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="5cf1f-109">Valige ripploendist valik **Tuletatud maksustatav dokumendimudel nimest: Maksu andmemudel -- Euroopa, Microsoft**, sisestage uue maksuandmete mudeli nimi ja seejärel valige käsk **Loo konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-109">In the drop-down dialog box, select the **Taxable document model derived from Name: Tax Data Model -- Europe, Microsoft** option, enter a name for the new tax data model, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="5cf1f-110">Valige äsja loodud maksuandmete mudel ja seejärel valige tegevuspaanil suvand **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-110">Select the tax data model that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="5cf1f-111">Laiendage andmemudelipuud, valige **Read** ja seejärel valik **Uus**.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-111">Expand the data model tree, select **Lines**, and then select **New**.</span></span>
6. <span data-ttu-id="5cf1f-112">Dialoogiboksis **Sõlme loomine** sisestage nimi, määrake kauba tüüp ja seejärel valige käsk **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-112">In the **Create node** dialog box, enter a name, specify the item type, and then select **Add**.</span></span>
7. <span data-ttu-id="5cf1f-113">Lisage kõik nõutavad veerud.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-113">Add any required columns.</span></span>
8. <span data-ttu-id="5cf1f-114">Valige toimingupaanil käsk **Salvesta** ja seejärel **Lõpeta**.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-114">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="5cf1f-115">Sulgege leht ja vaadake oma maksuandmete mudeli lõpetatud versiooni.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-115">Close the page, and view the completed version of your tax data model.</span></span>

## <a name="customize-the-tax-configuration"></a><span data-ttu-id="5cf1f-116">Maksukonfiguratsiooni kohandamine</span><span class="sxs-lookup"><span data-stu-id="5cf1f-116">Customize the tax configuration</span></span>

1. <span data-ttu-id="5cf1f-117">Jaotises Finants avage menüü **Elektrooniline aruandlus** \> **Maksukonfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-117">In Finance, go to **Electronic reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="5cf1f-118">Konfiguratsioonipuus valige **Maksukonfiguratsioon – Euroopa**.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-118">In the configuration tree, select **Tax Configuration -- Europe**.</span></span> <span data-ttu-id="5cf1f-119">Valige toimingupaanilt suvand **Loo konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-119">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="5cf1f-120">Valige ripploendist valik **Tuletatud maksuteenuse konfiguratsioon nimest: Maksukonfiguratsioon -- Euroopa, Microsoft**, sisestage uue maksukonfiguratsiooni nimi ja seejärel valige käsk **Loo konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-120">In the drop-down dialog box, select the **Tax service configuration derived from Name: Tax Configuration -- Europe, Microsoft** option, enter a name for the new tax configuration, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="5cf1f-121">Valige äsja loodud maksukonfiguratsioon ja seejärel valige tegevuspaanil suvand **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-121">Select the tax configuration that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="5cf1f-122">Valige jaotises **Atribuudid** väljal **Andmemudel** varem loodud kohandatud maksuandmete mudel.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-122">In the **Properties** section, in the **Data model** field, select the customized tax data model that you created earlier.</span></span>
6. <span data-ttu-id="5cf1f-123">Valige väljal **Andmemudeli versioon** maksuandmete mudeli lõpetatud versioon.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-123">In the **Data model version** field, select the completed version of the tax data model.</span></span>
7. <span data-ttu-id="5cf1f-124">Valige **Lisa** ja lisage nõutavad maksumeetmed.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-124">Select **Add**, and add the required tax measures.</span></span>
8. <span data-ttu-id="5cf1f-125">Valige toimingupaanil käsk **Salvesta** ja seejärel **Lõpeta**.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-125">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="5cf1f-126">Sulgege leht ja vaadake oma maksukonfiguratsiooni lõpetatud versiooni.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-126">Close page, and view the completed version of your tax configuration.</span></span>

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a><span data-ttu-id="5cf1f-127">Rakendage maksufunktsioone kohandatud maksukonfiguratsioonis</span><span class="sxs-lookup"><span data-stu-id="5cf1f-127">Implement tax features in the customized tax configuration</span></span>

1. <span data-ttu-id="5cf1f-128">Jaotises Regulatory Configuration Services (RCS) avage **Globaliseerumise funktsioonid** \> **Maks**.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-128">In Regulatory Configuration Service (RCS), go to **Globalization Features** \> **Tax**.</span></span>
2. <span data-ttu-id="5cf1f-129">Valige **Lisa**, sisestage uue funktsiooni kohta teave ja seejärel valige käsk **Loo funktsioon**.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-129">Select **Add**, enter information about the new feature, and then select **Create feature**.</span></span>
3. <span data-ttu-id="5cf1f-130">Valige funktsioon vahekaardil **Versioon** ja seejärel käsk **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-130">On the **Versions** tab, select the feature, and then select **Edit**.</span></span>
4. <span data-ttu-id="5cf1f-131">Valige vahekaardi **Üldine** väljal **Konfiguratsiooni versioon** kohandatud maksukonfiguratsioon ja versioon.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-131">On the **General** tab, in the **Configuration version** field, select the customized tax configuration and version.</span></span>
5. <span data-ttu-id="5cf1f-132">Dialoogiboksis **Veergude haldamine** valige päise- ja reaveerud, mida soovite oma kohandatud maksumeetmesse kaasata ja seejärel valige paremnoolenupp nende lisamiseks loendisse **Valitud veerud**.</span><span class="sxs-lookup"><span data-stu-id="5cf1f-132">In the **Manage columns** dialog box, select the header and line columns that you want to include in your customized tax measure, and then select the right arrow button to add them to the **Selected columns** list.</span></span>
