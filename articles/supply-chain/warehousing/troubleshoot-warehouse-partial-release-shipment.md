---
title: Osaliste väljastuste ja osaliste saadetiste tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada osaliste väljastuste ja osaliste saadetistega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1c9246376505e163a4a41bf141a98deed0fd511f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263224"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a><span data-ttu-id="3cf1b-103">Osaliste väljastuste ja osaliste saadetiste tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="3cf1b-103">Troubleshoot partial releases and partial shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3cf1b-104">Selles teemas kirjeldatakse, kuidas lahendada osaliste väljastuste ja osaliste saadetistega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-104">This topic describes how to fix common issues that you might encounter while you work with partial releases and partial shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a><span data-ttu-id="3cf1b-105">Müügitellimuse väljastamise olek jääb osaliselt väljastatud olekusse ka pärast müügitellimuse arveldamist.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-105">The release status of a sales order remains Partially released even after the sales order is invoiced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3cf1b-106">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3cf1b-106">Issue description</span></span>

<span data-ttu-id="3cf1b-107">Müügitellimus on kättetoimetamise tellimus, kuid ühel või mitmel kaubal on erinev tarneviis.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-107">A sales order is a delivery order, but one or more items on it have a different mode of delivery.</span></span> <span data-ttu-id="3cf1b-108">Pärast tellimuse arveldamist on sellel veel väljastamise olekuks *Osaliselt väljastatud*.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-108">After the order is invoiced, it still has a release status of *Partially released*.</span></span>

<span data-ttu-id="3cf1b-109">Näiteks on müügitellimusel kaks kaupa: üks tarnimiseks ja üks komplekteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-109">For example, a sales order has two items: one for delivery and one for pickup.</span></span> <span data-ttu-id="3cf1b-110">Nii tarne kui ka komplekteerimine on tehtud.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-110">Both the delivery and the pickup have been done.</span></span> <span data-ttu-id="3cf1b-111">Seetõttu on mõlemad read arveldatud.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-111">Therefore, both lines have been invoiced.</span></span> <span data-ttu-id="3cf1b-112">Kuid väljastamise olekuks kuvatakse endiselt *Osaliselt väljastatud*, mis on eksitav.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-112">However, the release status is still shown as *Partially released*, which is misleading.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3cf1b-113">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="3cf1b-113">Issue resolution</span></span>

<span data-ttu-id="3cf1b-114">Väljastamise olek rakendub ainult tellimuse ridadele, kus kaubad on laohalduse jaoks lubatud.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-114">The release status applies only to order lines where the items are enabled for warehouse management.</span></span> <span data-ttu-id="3cf1b-115">Seetõttu jääb selle stsenaariumi korral väljastamise olekuks *Osaliselt väljastatud*.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-115">Therefore, the release status remains *Partially released* in this scenario.</span></span> <span data-ttu-id="3cf1b-116">Microsoft on seda probleemi hinnanud ja on määranud, et see on funktsiooni piirang.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="3cf1b-117">Väljastamise oleku värskendamiseks võib saatelehe ja arveldamise protsessi osana lisada laiendi.</span><span class="sxs-lookup"><span data-stu-id="3cf1b-117">An extension could be added as part of the packing slip and invoicing process to update the release status.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]