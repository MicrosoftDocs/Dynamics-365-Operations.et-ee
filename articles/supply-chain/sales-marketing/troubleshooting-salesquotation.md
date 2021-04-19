---
title: Müügipakkumiste tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada müügipakkumistega töötamisel tekkivaid probleeme.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 09529ba729170be7281e2ae04008d3ba4a58e060
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824746"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="6ac27-103">Müügipakkumiste tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="6ac27-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="6ac27-104">Selles teemas kirjeldatakse, kuidas lahendada müügipakkumistega töötamisel tekkivaid probleeme.</span><span class="sxs-lookup"><span data-stu-id="6ac27-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="6ac27-105">Ma ei saa muuta teenusüksuse puhul müügipakkumise müügikogust.</span><span class="sxs-lookup"><span data-stu-id="6ac27-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6ac27-106">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="6ac27-106">Issue description</span></span>

<span data-ttu-id="6ac27-107">Kui proovite määrate müügipakkumise real müügikoguse (väli **SalesQty**) kauba jaoks, mille tüüp on *Teenus*, kuvatakse järgmine teade: „Värskendamine pole välja „Kogus” puhul lubatud”.</span><span class="sxs-lookup"><span data-stu-id="6ac27-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6ac27-108">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="6ac27-108">Issue resolution</span></span>

<span data-ttu-id="6ac27-109">Te ei saa määrata kogust toodete jaoks, mis on teenusüksused.</span><span class="sxs-lookup"><span data-stu-id="6ac27-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="6ac27-110">Näiteks kui pakute teenust kauba installimiseks, ei ole mõtet kogust salvestada, kuna füüsiline kaup puudub.</span><span class="sxs-lookup"><span data-stu-id="6ac27-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="6ac27-111">Olemas on ainult teenus.</span><span class="sxs-lookup"><span data-stu-id="6ac27-111">There is only a service.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]