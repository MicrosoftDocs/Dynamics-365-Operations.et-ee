---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent Core HR (24. september 2018)
description: Selles teemas kirjeldatakse funktsioone, mis on kas uued või muutunud rakenduses Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 078b513b828b97a5cfaf613970edd581fb091f9e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551316"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-24-2018"></a><span data-ttu-id="26d4c-103">Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent Core HR (24. september 2018)</span><span class="sxs-lookup"><span data-stu-id="26d4c-103">What's new or changed in Dynamics 365 Talent - Core HR (September 24, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="26d4c-104">**Järk 8.1.1015.0**</span><span class="sxs-lookup"><span data-stu-id="26d4c-104">**Build 8.1.1015.0**</span></span>

<span data-ttu-id="26d4c-105">Teema kirjeldab funktsioone, mis on Core HR-is kas uued või muudetud.</span><span class="sxs-lookup"><span data-stu-id="26d4c-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="currency-added-to-benefits"></a><span data-ttu-id="26d4c-106">Soodustustele lisatud valuuta</span><span class="sxs-lookup"><span data-stu-id="26d4c-106">Currency added to Benefits</span></span>

<span data-ttu-id="26d4c-107">Värskendatud soodustusplaanid sisaldavad nüüd soodustuse valuutat.</span><span class="sxs-lookup"><span data-stu-id="26d4c-107">Benefit plans have been updated to include the currency of the benefit.</span></span> <span data-ttu-id="26d4c-108">See uus väli on saadaval ka töötaja registreeritud soodustuste puhul.</span><span class="sxs-lookup"><span data-stu-id="26d4c-108">This new field is also available on worker enrolled benefits.</span></span> <span data-ttu-id="26d4c-109">See uus väli on osa turbeprivileegist Soodustuste haldamine ja Soodustuste loendi kuvamine.</span><span class="sxs-lookup"><span data-stu-id="26d4c-109">This new field is part of the Maintain benefits and View a list of benefits security privilege.</span></span>

## <a name="update-proration-process--leave-and-absence"></a><span data-ttu-id="26d4c-110">Värskendatud proportsionaalse arvestuse protsess – puhkused ja puudumised</span><span class="sxs-lookup"><span data-stu-id="26d4c-110">Update proration process – Leave and Absence</span></span>

<span data-ttu-id="26d4c-111">Organisatsioonid tasustavad puhkeaega erinevalt töövõtjate organisatsiooniga liitumise ja sealt lahkumise põhjal.</span><span class="sxs-lookup"><span data-stu-id="26d4c-111">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="26d4c-112">Mõne organisatsioonist lahkuva töötaja puhul tuleb preemia välja maksta lõpetamiskuupäeval, mõne puhul sõltub arvestuse protsessi peatamine viimasest tööpäevast.</span><span class="sxs-lookup"><span data-stu-id="26d4c-112">For employees leaving the organization, some may need to end the award on the termination date, while others rely on the last day worked to stop the accrual process.</span></span> <span data-ttu-id="26d4c-113">Need muudatused võimaldavad organisatsioonil valida töösuhte lõpetamisprotsessi käigus, millal registreering lõpetada.</span><span class="sxs-lookup"><span data-stu-id="26d4c-113">These changes provide organizations the ability to choose when to end enrollment during the termination process.</span></span> <span data-ttu-id="26d4c-114">Need uued suvandid on osa privileegidest Töötajaga töösuhte lõpetamine ja Töötajaga töösuhte lõpetamine juhataja iseteeninduses.</span><span class="sxs-lookup"><span data-stu-id="26d4c-114">These new options are part of the privileges for Terminate a worker and Terminate a worker from manager self service.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="26d4c-115">Muud muudatused</span><span class="sxs-lookup"><span data-stu-id="26d4c-115">Other changes</span></span>

<span data-ttu-id="26d4c-116">Selles versioonis sisaldub mitu täiendavat veaparandust.</span><span class="sxs-lookup"><span data-stu-id="26d4c-116">This release includes several additional bug fixes.</span></span>

## <a name="known-issue"></a><span data-ttu-id="26d4c-117">Teadaolev probleem</span><span class="sxs-lookup"><span data-stu-id="26d4c-117">Known Issue</span></span>

-   <span data-ttu-id="26d4c-118">**Probleem:** töötajale uue manuse lisamisel on nupud **Uus** ja **Redigeeri** hallid. **Lahendus:** enne manuselehe avamist veenduge, et kiirinfod lehel **Töötaja** oleksid suletud.</span><span class="sxs-lookup"><span data-stu-id="26d4c-118">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the fact boxes on the **Worker** page are closed.</span></span> <span data-ttu-id="26d4c-119">Kui kiirinfod on lehe **Töötaja** laadimisel suletud, on manusenupud lubatud.</span><span class="sxs-lookup"><span data-stu-id="26d4c-119">If the fact boxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="26d4c-120">(See probleem lahendatakse järgmisel platvormivärskendusel.)</span><span class="sxs-lookup"><span data-stu-id="26d4c-120">(This issue will be fixed in the next platform update.)</span></span>
