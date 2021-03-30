---
title: Müügipakkumiste tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada müügipakkumistega töötamisel tekkivaid probleeme.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 9a9cc821d2fe9accad1dae210271682cdd2ce4ba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232202"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="5a6f9-103">Müügipakkumiste tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="5a6f9-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="5a6f9-104">Selles teemas kirjeldatakse, kuidas lahendada müügipakkumistega töötamisel tekkivaid probleeme.</span><span class="sxs-lookup"><span data-stu-id="5a6f9-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="5a6f9-105">Ma ei saa muuta teenusüksuse puhul müügipakkumise müügikogust.</span><span class="sxs-lookup"><span data-stu-id="5a6f9-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5a6f9-106">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="5a6f9-106">Issue description</span></span>

<span data-ttu-id="5a6f9-107">Kui proovite määrate müügipakkumise real müügikoguse (väli **SalesQty**) kauba jaoks, mille tüüp on *Teenus*, kuvatakse järgmine teade: „Värskendamine pole välja „Kogus” puhul lubatud”.</span><span class="sxs-lookup"><span data-stu-id="5a6f9-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5a6f9-108">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="5a6f9-108">Issue resolution</span></span>

<span data-ttu-id="5a6f9-109">Te ei saa määrata kogust toodete jaoks, mis on teenusüksused.</span><span class="sxs-lookup"><span data-stu-id="5a6f9-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="5a6f9-110">Näiteks kui pakute teenust kauba installimiseks, ei ole mõtet kogust salvestada, kuna füüsiline kaup puudub.</span><span class="sxs-lookup"><span data-stu-id="5a6f9-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="5a6f9-111">Olemas on ainult teenus.</span><span class="sxs-lookup"><span data-stu-id="5a6f9-111">There is only a service.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]