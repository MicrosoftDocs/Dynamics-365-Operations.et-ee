---
title: Vaikemakseteenusega seotud tellimuse sünkroonimise tõrge
description: See teema annab tõrkeotsingu juhised, mis aitavad parandada tõrget, mis võib ilmneda võrgutellimuse sünkroonimisel.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: fa174bbb257379f6ce906dd21180bbcb19f8bc3f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021123"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a><span data-ttu-id="99f65-103">Vaikemakseteenusega seotud tellimuse sünkroonimise tõrge</span><span class="sxs-lookup"><span data-stu-id="99f65-103">Order synchronization error related to the default payment service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="99f65-104">See teema annab tõrkeotsingu juhised, mis aitavad parandada tõrget, mis võib ilmneda võrgutellimuse sünkroonimisel.</span><span class="sxs-lookup"><span data-stu-id="99f65-104">This topic provides troubleshooting guidance that can help fix an error that might occur when an online order is synced.</span></span>

## <a name="description"></a><span data-ttu-id="99f65-105">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="99f65-105">Description</span></span>

<span data-ttu-id="99f65-106">Võrgutellimuse sünkroonimisel kuvatakse järgmine tõrketeade: "Krediitkaarditehingute töötlemiseks peab olema vaikemakseteenus."</span><span class="sxs-lookup"><span data-stu-id="99f65-106">When you sync an online order, you receive the following error message: "There must be a default payment service to process credit card transactions."</span></span>

![Puuduv vaikimisi makseteenuse tõrge](media/default-payment-method-error.jpg)

## <a name="resolution"></a><span data-ttu-id="99f65-108">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="99f65-108">Resolution</span></span>

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a><span data-ttu-id="99f65-109">Commerce Headquartersi vaikimisi makseteenuse kinnitamine või seadistamine</span><span class="sxs-lookup"><span data-stu-id="99f65-109">Confirm or set the default payment service in Commerce headquarters</span></span>

<span data-ttu-id="99f65-110">Commerce Headquarters\`i vaikimisi makseteenuse kinnitamine või seadistamine, järgi järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="99f65-110">To confirm or set the default payment service in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="99f65-111">Avage **Müügireskontro \> Maksete seadistus \> Makseteenused**.</span><span class="sxs-lookup"><span data-stu-id="99f65-111">Go to **Accounts receivable \> Payment setup \> Payment services**.</span></span>
1. <span data-ttu-id="99f65-112">Veenduge, et **Uute krediitkaartide suvandi vaikeprotsessor** on seadistatud valikule **Jah** ühe makseteenuse puhul.</span><span class="sxs-lookup"><span data-stu-id="99f65-112">Make sure that the **Default processor for new credit cards** option is set to **Yes** for one payment service.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="99f65-113">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="99f65-113">Additional resources</span></span>

[<span data-ttu-id="99f65-114">Krediitkaardi seadistamine, autoriseerimine ja hõivamine</span><span class="sxs-lookup"><span data-stu-id="99f65-114">Credit card setup, authorization, and capture</span></span>](../../finance/accounts-receivable/credit-card-authorizations.md)