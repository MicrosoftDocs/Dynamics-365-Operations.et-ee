---
title: Jaemüügikannete finantsdimensioonide redigeerimine
description: Selles teemas kirjeldatakse, kuidas redigeerida Microsoft Dynamics 365 Commerce'is jaemüügikannete finantsdimensioone.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 381d8bb0939f6c4c163477990e49382201487375
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019903"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a><span data-ttu-id="f0d3c-103">Jaemüügikannete finantsdimensioonide redigeerimine</span><span class="sxs-lookup"><span data-stu-id="f0d3c-103">Edit financial dimensions for retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0d3c-104">Selles teemas kirjeldatakse, kuidas redigeerida Microsoft Dynamics 365 Commerce'is jaemüügikannete finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="f0d3c-104">This topic describes how to edit financial dimensions for retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="edit-financial-dimensions"></a><span data-ttu-id="f0d3c-105">Finantsdimensioonide redigeerimine</span><span class="sxs-lookup"><span data-stu-id="f0d3c-105">Edit financial dimensions</span></span>

<span data-ttu-id="f0d3c-106">Commerce'i peakontoris jaemüügikannete finantsdimensioonide redigeerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="f0d3c-106">To edit financial dimensions for retail transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f0d3c-107">Avage leht **Finantsdimensioonide konfiguratsioon rakenduste integreerimiseks**.</span><span class="sxs-lookup"><span data-stu-id="f0d3c-107">Open the **Financial dimensions configuration for integrating applications** page.</span></span>
1. <span data-ttu-id="f0d3c-108">Valige aktiivne kirje **Vaikedimensioonide integratsioon**.</span><span class="sxs-lookup"><span data-stu-id="f0d3c-108">Select the active **Default dimensions integration** record.</span></span>
1. <span data-ttu-id="f0d3c-109">Veenduge, et kõik kiirkaardil **Finantsdimensioonid** olevad dimensioonid, mida soovite Exceli töölehel redigeerida, oleksid loendis **Valitud**.</span><span class="sxs-lookup"><span data-stu-id="f0d3c-109">On the **Financial dimensions** FastTab, make sure that all the dimensions that you want to edit in the Excel worksheet are present in the **Selected** list.</span></span> <span data-ttu-id="f0d3c-110">Lisateavet leiate artiklist [Andmeüksused](../fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration.md#data-entities).</span><span class="sxs-lookup"><span data-stu-id="f0d3c-110">For more information, see [Data entities](../fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration.md#data-entities).</span></span>
1. <span data-ttu-id="f0d3c-111">Laadige alla ja avage Exceli fail lehelt **Väljavõtted**, lehelt **Jaemüügikanded** või tööruumi **Kaupluse finantsandmed** paanilt **Kande kinnitamise tõrked**.</span><span class="sxs-lookup"><span data-stu-id="f0d3c-111">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="f0d3c-112">Kande finantsdimensiooni muutmiseks valige **Kujundus** ja seejärel rea **Kanne (auditeeritav)** kõrval olev pliiatsisümbol.</span><span class="sxs-lookup"><span data-stu-id="f0d3c-112">To change the transaction financial dimension, select **Design**, and then select the pencil symbol next to the **Transaction (auditable)** row.</span></span>
1. <span data-ttu-id="f0d3c-113">Leidke ja valige väli **FinancialDimensionDisplayValue**, valige Exceli töölehe päiseosas lahter ja seejärel suvand **Lisa silt**.</span><span class="sxs-lookup"><span data-stu-id="f0d3c-113">Find and select the **FinancialDimensionDisplayValue** field, select a cell in the header part of the Excel worksheet, and then select **Add label**.</span></span>
1. <span data-ttu-id="f0d3c-114">Valige eelmises sammus valitud lahtri all olev lahter, valige **Lisa väärtus** ja seejärel **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="f0d3c-114">Select a cell below the cell that you selected in the previous step, select **Add Value**, and then select **Refresh**.</span></span> <span data-ttu-id="f0d3c-115">Finantsdimensioonid lisatakse Exceli töölehele ning neid saab seejärel redigeerida ja avaldada.</span><span class="sxs-lookup"><span data-stu-id="f0d3c-115">The financial dimensions are added to the Excel worksheet, and they can then be edited and published.</span></span>
1. <span data-ttu-id="f0d3c-116">Kanderidade dimensioonide muutmiseks valige rida **Müügikanded (auditeeritav)**, valige pliiatsisümbol ning järgige uuesti samme 6 ja 7.</span><span class="sxs-lookup"><span data-stu-id="f0d3c-116">To change the dimensions on the transaction lines, select the **Sales transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>
1. <span data-ttu-id="f0d3c-117">Makseridade dimensioonide muutmiseks valige rida **Maksekanded (auditeeritav)**, valige pliiatsisümbol ning järgige uuesti samme 6 ja 7.</span><span class="sxs-lookup"><span data-stu-id="f0d3c-117">To change the dimensions on the payment lines, select the **Payment transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f0d3c-118">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f0d3c-118">Additional resources</span></span>

[<span data-ttu-id="f0d3c-119">Selvehulgimüügi- ja kassahalduskannete redigeerimine ning auditeerimine</span><span class="sxs-lookup"><span data-stu-id="f0d3c-119">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="f0d3c-120">Veebitellimuse ja asünkroonse klienditellimuse kannete redigeerimine ning auditeerimine</span><span class="sxs-lookup"><span data-stu-id="f0d3c-120">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="f0d3c-121">Exceli töövihiku loomine jaemüügikannete redigeerimiseks</span><span class="sxs-lookup"><span data-stu-id="f0d3c-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="f0d3c-122">Väljade lisamine Exceli töövihikusse jaemüügikannete redigeerimiseks</span><span class="sxs-lookup"><span data-stu-id="f0d3c-122">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]