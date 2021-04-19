---
title: Osaliste väljastuste ja osaliste saadetiste tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada osaliste väljastuste ja osaliste saadetistega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5534099f81a97a1dcf4908784fd71dd03cf94eaf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828150"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a><span data-ttu-id="34910-103">Osaliste väljastuste ja osaliste saadetiste tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="34910-103">Troubleshoot partial releases and partial shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34910-104">Selles teemas kirjeldatakse, kuidas lahendada osaliste väljastuste ja osaliste saadetistega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.</span><span class="sxs-lookup"><span data-stu-id="34910-104">This topic describes how to fix common issues that you might encounter while you work with partial releases and partial shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a><span data-ttu-id="34910-105">Müügitellimuse väljastamise olek jääb osaliselt väljastatud olekusse ka pärast müügitellimuse arveldamist.</span><span class="sxs-lookup"><span data-stu-id="34910-105">The release status of a sales order remains Partially released even after the sales order is invoiced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="34910-106">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="34910-106">Issue description</span></span>

<span data-ttu-id="34910-107">Müügitellimus on kättetoimetamise tellimus, kuid ühel või mitmel kaubal on erinev tarneviis.</span><span class="sxs-lookup"><span data-stu-id="34910-107">A sales order is a delivery order, but one or more items on it have a different mode of delivery.</span></span> <span data-ttu-id="34910-108">Pärast tellimuse arveldamist on sellel veel väljastamise olekuks *Osaliselt väljastatud*.</span><span class="sxs-lookup"><span data-stu-id="34910-108">After the order is invoiced, it still has a release status of *Partially released*.</span></span>

<span data-ttu-id="34910-109">Näiteks on müügitellimusel kaks kaupa: üks tarnimiseks ja üks komplekteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="34910-109">For example, a sales order has two items: one for delivery and one for pickup.</span></span> <span data-ttu-id="34910-110">Nii tarne kui ka komplekteerimine on tehtud.</span><span class="sxs-lookup"><span data-stu-id="34910-110">Both the delivery and the pickup have been done.</span></span> <span data-ttu-id="34910-111">Seetõttu on mõlemad read arveldatud.</span><span class="sxs-lookup"><span data-stu-id="34910-111">Therefore, both lines have been invoiced.</span></span> <span data-ttu-id="34910-112">Kuid väljastamise olekuks kuvatakse endiselt *Osaliselt väljastatud*, mis on eksitav.</span><span class="sxs-lookup"><span data-stu-id="34910-112">However, the release status is still shown as *Partially released*, which is misleading.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="34910-113">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="34910-113">Issue resolution</span></span>

<span data-ttu-id="34910-114">Väljastamise olek rakendub ainult tellimuse ridadele, kus kaubad on laohalduse jaoks lubatud.</span><span class="sxs-lookup"><span data-stu-id="34910-114">The release status applies only to order lines where the items are enabled for warehouse management.</span></span> <span data-ttu-id="34910-115">Seetõttu jääb selle stsenaariumi korral väljastamise olekuks *Osaliselt väljastatud*.</span><span class="sxs-lookup"><span data-stu-id="34910-115">Therefore, the release status remains *Partially released* in this scenario.</span></span> <span data-ttu-id="34910-116">Microsoft on seda probleemi hinnanud ja on määranud, et see on funktsiooni piirang.</span><span class="sxs-lookup"><span data-stu-id="34910-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="34910-117">Väljastamise oleku värskendamiseks võib saatelehe ja arveldamise protsessi osana lisada laiendi.</span><span class="sxs-lookup"><span data-stu-id="34910-117">An extension could be added as part of the packing slip and invoicing process to update the release status.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]