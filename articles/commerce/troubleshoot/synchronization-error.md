---
title: Vaikemakseteenusega seotud tellimuse sünkroonimise tõrge
description: See teema annab tõrkeotsingu juhised, mis aitavad parandada tõrget, mis võib ilmneda võrgutellimuse sünkroonimisel.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dd7c400f26b6fc7fbe1d4fec43a52295eb363333
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585279"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="caf4e-103">Vaikemakseteenusega seotud tellimuse sünkroonimise tõrge</span><span class="sxs-lookup"><span data-stu-id="caf4e-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="caf4e-104">See teema annab tõrkeotsingu juhised, mis aitavad parandada tõrget, mis võib ilmneda võrgutellimuse sünkroonimisel.</span><span class="sxs-lookup"><span data-stu-id="caf4e-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="caf4e-105">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="caf4e-105">Description</span></span>

<span data-ttu-id="caf4e-106">Võrgutellimuse sünkroonimisel kuvatakse järgmine tõrketeade: "Krediitkaarditehingute töötlemiseks peab olema vaikemakseteenus."</span><span class="sxs-lookup"><span data-stu-id="caf4e-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![Puuduv vaikimisi makseteenuse tõrge](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="caf4e-108">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="caf4e-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="caf4e-109">Commerce Headquartersi vaikimisi makseteenuse kinnitamine või seadistamine</span><span class="sxs-lookup"><span data-stu-id="caf4e-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="caf4e-110">Commerce Headquarters\`i vaikimisi makseteenuse kinnitamine või seadistamine, järgi järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="caf4e-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="caf4e-111">Avage **Müügireskontro \> Maksete seadistus \> Makseteenused**.</span><span class="sxs-lookup"><span data-stu-id="caf4e-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="caf4e-112">Veenduge, et **Uute krediitkaartide suvandi vaikeprotsessor** on seadistatud valikule **Jah** ühe makseteenuse puhul.</span><span class="sxs-lookup"><span data-stu-id="caf4e-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="caf4e-113">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="caf4e-113">Additional resources</span></span>

[<span data-ttu-id="caf4e-114">Krediitkaardi seadistamine, autoriseerimine ja hõivamine</span><span class="sxs-lookup"><span data-stu-id="caf4e-114">Credit card setup, authorization, and capture</span></span>](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)
