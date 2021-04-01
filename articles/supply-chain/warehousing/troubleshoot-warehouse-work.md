---
title: Laotöö tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada laotööga tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
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
ms.openlocfilehash: b1814f7b23efda2cabdb7bfc7bea4de6e3d6ec2f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237055"
---
# <a name="troubleshoot-warehouse-work"></a><span data-ttu-id="cd4d0-103">Laotöö tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="cd4d0-103">Troubleshoot warehouse work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd4d0-104">Selles teemas kirjeldatakse, kuidas lahendada laotööga tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-104">This topic describes how to fix common issues that you might encounter while you work with warehouse work in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a><span data-ttu-id="cd4d0-105">Ma ei saa liigutada identifitseerimisnumbrid seerianumbriga kaupadega, kui jälgimise dimensiooni grupis on tühi väljaminek ja tühi sissetulek lubatud.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-105">I can't move license plates that have serial number items when blank issue and blank receipt are allowed on the tracking dimension group.</span></span>

### <a name="issue-description"></a><span data-ttu-id="cd4d0-106">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="cd4d0-106">Issue description</span></span>

<span data-ttu-id="cd4d0-107">Te ei saa teisaldada identifitseerimisnumbrit kasutades **Teisaldamine** menüükäsku, kui seerianumbril on jälgimise dimensiooni grupis *Tühjad väljaminekud lubatud* ja *Tühjad vastuvõtmised lubatud* ning kui mitu identifitseerimisnumbrit on samas asukohas, millest mõnel on seerianumbrid ja mõnel neist ei ole.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-107">You can't move a license plate by using a **Movement** menu item if the serial number has settings of *Blank issue allowed* and *Blank receipt allowed* on the tracking dimension group, and if there are multiple license plates in the same location, some of which have serial numbers and some of which don't have them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="cd4d0-108">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="cd4d0-108">Issue resolution</span></span>

<span data-ttu-id="cd4d0-109">See probleem parandatakse muudatustega, mida kasutatakse [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span><span class="sxs-lookup"><span data-stu-id="cd4d0-109">This issue will be fixed by changes that are deployed in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span></span> <span data-ttu-id="cd4d0-110">Need muudatused muudavad **Seerianumbri** välja valikuliseks, kui tühi sissetulek ja tühi väljaminek on lubatud.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-110">Those changes will make the **Serial number** field optional when blank receipt and blank issue are allowed.</span></span>

## <a name="i-receive-the-following-error-message-in-the-warehouse-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a><span data-ttu-id="cd4d0-111">Kui teisaldamise töötlemisel kuvatakse lao rakenduses järgmine tõrketeade: "Lao omanik %1 pole selles protsessis lubatud."</span><span class="sxs-lookup"><span data-stu-id="cd4d0-111">I receive the following error message in the warehouse app when I process movements: "The inventory owner %1 is not allowed in this process."</span></span>

### <a name="issue-description"></a><span data-ttu-id="cd4d0-112">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="cd4d0-112">Issue description</span></span>

<span data-ttu-id="cd4d0-113">**Omaniku** jälgimise dimensioon puudub, kui liikumiste tegemiseks kasutatakse lao rakendust.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-113">The **Owner** tracking dimension is missing when the warehouse app is used to make movements.</span></span> <span data-ttu-id="cd4d0-114">Regulaarne lao ülekandmise tööleht Supply Chain Management rakendusest näib töötavad plaanipäraselt ja seda saab sisestada ainult siis, kui **Omaniku** dimensioon on täidetud.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-114">A regular inventory transfer journal from the Supply Chain Management client appears to work as intended and can be posted only if the **Owner** dimension is filled in.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="cd4d0-115">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="cd4d0-115">Issue resolution</span></span>

<span data-ttu-id="cd4d0-116">Microsoft on seda probleemi hinnanud ja on määranud, et see on funktsiooni piirang.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="cd4d0-117">Praegu toetavad laohalduse protsessid ainult selle juriidilise isiku omanduses olevat laovaru.</span><span class="sxs-lookup"><span data-stu-id="cd4d0-117">Currently, warehouse management processes support only inventory that is owned by the legal entity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]