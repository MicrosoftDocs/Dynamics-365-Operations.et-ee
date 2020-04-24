---
title: Käibemaksu tasumise printimine koodide aruande järgi
description: Selles teemas antakse teavet seadistuste ja toimingute kohta, mis on nõutavad käibemaksu tasumise printimiseks koodide aruande järgi arvestus- või maksukoodi valuutas.
author: anasyash
manager: AnnBe
ms.date: 04/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 3c3b251aadfa997f453e60b0842f89a6f09eb9cb
ms.sourcegitcommit: 88347d0f0ac862a77f269a05f1801d30dc93586e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2020
ms.locfileid: "3260251"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a><span data-ttu-id="e38cb-103">Käibemaksu tasumise printimine koodide aruande järgi</span><span class="sxs-lookup"><span data-stu-id="e38cb-103">Print the Sales tax payment by code report</span></span> 

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="e38cb-104">Aruande **Käibemaksu tasumine koodide lõikes** printimiseks avage **Maks** \> **Päringud ja aruanded** \> **Käibemaksu aruanded** \> **Käibemaksu tasumine koodide lõikes**.</span><span class="sxs-lookup"><span data-stu-id="e38cb-104">To print the **Sales tax payment by code** report, go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span> <span data-ttu-id="e38cb-105">Vaikimisi luuakse aruandesummad juriidilise isiku arvestusvaluutas kõigi aruandluse koodide kohta, mis on seadistatud lehel **Käibemaksuaruandluse koodid**.</span><span class="sxs-lookup"><span data-stu-id="e38cb-105">By default, report amounts are generated in the accounting currency of the legal entity for all reporting codes that are set up on the **Sales tax reporting codes** page.</span></span>

<span data-ttu-id="e38cb-106">Selle aruande saate luua ka nii, et see kuvaks käibemaksu maksesummad käibemaksukoodide valuutades kõigi aruandekoodide korral, mis on määratud käibemaksukoodidele lehel **Käibemaksukoodid**.</span><span class="sxs-lookup"><span data-stu-id="e38cb-106">You can also generate this report so that it shows the sales tax payment amounts in the currencies of sales tax codes for all reporting codes that are assigned to sales tax codes on the **Sales tax codes** page.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="e38cb-107">Funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="e38cb-107">Turn on the feature</span></span>

<span data-ttu-id="e38cb-108">Lülitage tööruumis **Funktsioonihaldus** sisse järgmine funktsioon: **Loo käibemaksumakse koodide aruande järgi käibemaksukoodi valuutas**.</span><span class="sxs-lookup"><span data-stu-id="e38cb-108">In the **Feature management** workspace, turn on the following feature: **Generate the Sales tax payment by code report in the sales tax code currency**.</span></span>

## <a name="run-the-report"></a><span data-ttu-id="e38cb-109">Aruande käivitamine</span><span class="sxs-lookup"><span data-stu-id="e38cb-109">Run the report</span></span>

1. <span data-ttu-id="e38cb-110">Avage  **Maks** \> **Päringud ja aruanded** \> **Käibemaksu aruanded** \> **Käibemaksu tasumine koodide lõikes**.</span><span class="sxs-lookup"><span data-stu-id="e38cb-110">Go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span>
2. <span data-ttu-id="e38cb-111">Valige väljal **Aruandevaluuta** üks järgmistest väärtustest.</span><span class="sxs-lookup"><span data-stu-id="e38cb-111">In the **Report currency** field, select one of the following values:</span></span>

    - <span data-ttu-id="e38cb-112">**Arvestusvaluuta** – saate printida aruandesummad arvestusvaluuta.</span><span class="sxs-lookup"><span data-stu-id="e38cb-112">**Accounting currency** – Print the report amounts in the accounting currency.</span></span>
    - <span data-ttu-id="e38cb-113">**Käibemaksukoodi valuuta** – saate printida aruandesummad käibemaksukoodide valuutades.</span><span class="sxs-lookup"><span data-stu-id="e38cb-113">**Sales tax code currency** – Print the report amounts in the currencies of sales tax codes.</span></span>

    ![Käibemaksu tasumine koodi dialoogiboksi järgi](media/Sales-tax-payment-by-code.png)

<span data-ttu-id="e38cb-115">Järgnev illustratsioon näitab aruande loodud näidet.</span><span class="sxs-lookup"><span data-stu-id="e38cb-115">The following illustration shows an example of the report that is generated.</span></span> <span data-ttu-id="e38cb-116">Aruanne näitab, et aruandluskoodil **101** on valuuta **EUR**, kui selle määratud aruandluskoodiga käibemaksukoodi jaoks on välja **Käibemaksu valuuta** väärtuseks määratud **EUR**.</span><span class="sxs-lookup"><span data-stu-id="e38cb-116">The report shows that reporting code **101** has the **EUR** currency if the **Sales tax currency** field is set to **EUR** for the sales tax code that the reporting code is assigned to.</span></span>

![Näide käibemaksu tasumisest koodide aruande järgi](media/Sales-tax-payment-by-code-2.png)
