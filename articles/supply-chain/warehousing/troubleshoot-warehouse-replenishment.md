---
title: Lao täiendamise tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada lao täiendamisega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
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
ms.openlocfilehash: 8dfb58c9156df106f58dfdc0ee2e0ef8defb9d9f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263200"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="e069b-103">Lao täiendamise tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="e069b-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e069b-104">Selles teemas kirjeldatakse, kuidas lahendada lao täiendamisega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.</span><span class="sxs-lookup"><span data-stu-id="e069b-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="e069b-105">Saan järgneva tõrketeate: "Töö %1 blokeeringut ei saa tühistada, kuna see on lõpule viimata täiendamistöö."</span><span class="sxs-lookup"><span data-stu-id="e069b-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="e069b-106">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e069b-106">Issue description</span></span>

<span data-ttu-id="e069b-107">Komplekteerimise töö on blokeeritud sõltuva täiendamistöö tõttu.</span><span class="sxs-lookup"><span data-stu-id="e069b-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e069b-108">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="e069b-108">Issue resolution</span></span>

<span data-ttu-id="e069b-109">Kui kasutate voo nõudluse täiendamist, kui komplekteerimise asukoht tuleb komplekteerida, et täita allika tellimuse nõudlust, loob süsteem nii täiendamise töö kui ka komplekteerimise töö.</span><span class="sxs-lookup"><span data-stu-id="e069b-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="e069b-110">Kuid see blokeerib komplekteerimise töö seni, kuni täiendamise töö on lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="e069b-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="e069b-111">Selline käitumine on tahtlik, sest komplekteerimise asukohas ei ole piisavalt varusid, kui täiendamise töö on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="e069b-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="e069b-112">Täitke täiendamise töö ja seejärel töödelge komplekteerimise töö.</span><span class="sxs-lookup"><span data-stu-id="e069b-112">Complete the replenishment work, and then process the picking work.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]