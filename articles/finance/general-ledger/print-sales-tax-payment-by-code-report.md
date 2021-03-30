---
title: Käibemaksu tasumise printimine koodide aruande järgi
description: Selles teemas antakse teavet seadistuste ja toimingute kohta, mis on nõutavad käibemaksu tasumise printimiseks koodide aruande järgi arvestus- või maksukoodi valuutas.
author: anasyash
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 6f66db74867bdd3e9b4364e247058e0534191f2e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205056"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a><span data-ttu-id="35b89-103">Käibemaksu tasumise printimine koodide aruande järgi</span><span class="sxs-lookup"><span data-stu-id="35b89-103">Print the Sales tax payment by code report</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35b89-104">Aruande **Käibemaksu tasumine koodide lõikes** printimiseks avage **Maks** \> **Päringud ja aruanded** \> **Käibemaksu aruanded** \> **Käibemaksu tasumine koodide lõikes**.</span><span class="sxs-lookup"><span data-stu-id="35b89-104">To print the **Sales tax payment by code** report, go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span> <span data-ttu-id="35b89-105">Vaikimisi luuakse aruandesummad juriidilise isiku arvestusvaluutas kõigi aruandluse koodide kohta, mis on seadistatud lehel **Käibemaksuaruandluse koodid**.</span><span class="sxs-lookup"><span data-stu-id="35b89-105">By default, report amounts are generated in the accounting currency of the legal entity for all reporting codes that are set up on the **Sales tax reporting codes** page.</span></span>

<span data-ttu-id="35b89-106">Selle aruande saate luua ka nii, et see kuvaks käibemaksu maksesummad käibemaksukoodide valuutades kõigi aruandekoodide korral, mis on määratud käibemaksukoodidele lehel **Käibemaksukoodid**.</span><span class="sxs-lookup"><span data-stu-id="35b89-106">You can also generate this report so that it shows the sales tax payment amounts in the currencies of sales tax codes for all reporting codes that are assigned to sales tax codes on the **Sales tax codes** page.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="35b89-107">Funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="35b89-107">Turn on the feature</span></span>

<span data-ttu-id="35b89-108">Lülitage tööruumis **Funktsioonihaldus** sisse järgmine funktsioon: **Loo käibemaksumakse koodide aruande järgi käibemaksukoodi valuutas**.</span><span class="sxs-lookup"><span data-stu-id="35b89-108">In the **Feature management** workspace, turn on the following feature: **Generate the Sales tax payment by code report in the sales tax code currency**.</span></span>

## <a name="run-the-report"></a><span data-ttu-id="35b89-109">Aruande käivitamine</span><span class="sxs-lookup"><span data-stu-id="35b89-109">Run the report</span></span>

1. <span data-ttu-id="35b89-110">Avage  **Maks** \> **Päringud ja aruanded** \> **Käibemaksu aruanded** \> **Käibemaksu tasumine koodide lõikes**.</span><span class="sxs-lookup"><span data-stu-id="35b89-110">Go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span>
2. <span data-ttu-id="35b89-111">Valige väljal **Aruandevaluuta** üks järgmistest väärtustest.</span><span class="sxs-lookup"><span data-stu-id="35b89-111">In the **Report currency** field, select one of the following values:</span></span>

    - <span data-ttu-id="35b89-112">**Arvestusvaluuta** – saate printida aruandesummad arvestusvaluuta.</span><span class="sxs-lookup"><span data-stu-id="35b89-112">**Accounting currency** – Print the report amounts in the accounting currency.</span></span>
    - <span data-ttu-id="35b89-113">**Käibemaksukoodi valuuta** – saate printida aruandesummad käibemaksukoodide valuutades.</span><span class="sxs-lookup"><span data-stu-id="35b89-113">**Sales tax code currency** – Print the report amounts in the currencies of sales tax codes.</span></span>

    ![Käibemaksu tasumine koodi dialoogiboksi järgi](media/Sales-tax-payment-by-code.png)

<span data-ttu-id="35b89-115">Järgnev illustratsioon näitab aruande loodud näidet.</span><span class="sxs-lookup"><span data-stu-id="35b89-115">The following illustration shows an example of the report that is generated.</span></span> <span data-ttu-id="35b89-116">Aruanne näitab, et aruandluskoodil **101** on valuuta **EUR**, kui selle määratud aruandluskoodiga käibemaksukoodi jaoks on välja **Käibemaksu valuuta** väärtuseks määratud **EUR**.</span><span class="sxs-lookup"><span data-stu-id="35b89-116">The report shows that reporting code **101** has the **EUR** currency if the **Sales tax currency** field is set to **EUR** for the sales tax code that the reporting code is assigned to.</span></span>

![Näide käibemaksu tasumisest koodide aruande järgi](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]