---
title: Rendi kasutajarollide määramine
description: See teema kirjeldab varade rentimisel kasutatavaid turberolle. Lisaks selgitatakse, kuidas määrata nendele rollidele kasutajaid.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 05728f5027dc079dd413dde1c3aa78cddcea136b
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881056"
---
# <a name="assign-lease-user-roles"></a><span data-ttu-id="38fc3-104">Rendi kasutajarollide määramine</span><span class="sxs-lookup"><span data-stu-id="38fc3-104">Assign lease user roles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38fc3-105">See teema kirjeldab varade rentimisel kasutatavaid turberolle.</span><span class="sxs-lookup"><span data-stu-id="38fc3-105">This topic describes the security roles that are used in Asset leasing.</span></span> <span data-ttu-id="38fc3-106">Lisaks selgitatakse, kuidas määrata nendele rollidele kasutajaid.</span><span class="sxs-lookup"><span data-stu-id="38fc3-106">It also explains how to assign users to those roles.</span></span>

<span data-ttu-id="38fc3-107">Vara rentimisele juurdepääsu eristavad kolm kasutajarolli.</span><span class="sxs-lookup"><span data-stu-id="38fc3-107">Three user roles differentiate access in Asset leasing.</span></span> <span data-ttu-id="38fc3-108">Üks on sobiv rentide haldamiseks, üks sobiv rentide vaatamiseks ja üks sobiv rentniku kohustuste täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="38fc3-108">One role is appropriate for maintaining leases, one is appropriate for viewing leases, and one is appropriate for performing a lease clerk's duties.</span></span> <span data-ttu-id="38fc3-109">Igal rollil on iga rendi lehe jaoks kindlad õigused ja võimaldab igal kasutajal vaadata, luua, muuta või kustutada rente vastavalt oma töökohustustele.</span><span class="sxs-lookup"><span data-stu-id="38fc3-109">Each role has specific permissions for all lease pages, and each lets users view, create, edit, or delete leases, according to their job duties.</span></span>

| <span data-ttu-id="38fc3-110">Roll</span><span class="sxs-lookup"><span data-stu-id="38fc3-110">Role</span></span>           | <span data-ttu-id="38fc3-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="38fc3-111">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="38fc3-112">Rendi haldamine</span><span class="sxs-lookup"><span data-stu-id="38fc3-112">Maintain Lease</span></span> | <span data-ttu-id="38fc3-113">Selle rolliga kasutajad saavad rente lisada, muuta, kustutada ja vaadata.</span><span class="sxs-lookup"><span data-stu-id="38fc3-113">Users in this role can add, edit, delete, and view leases.</span></span> <span data-ttu-id="38fc3-114">See roll on mõeldud igapäevastele kasutajatele, kelle ülesannete hulka kuuluvad igakuise töölehe kirjete loomine ja sisestamine ning uute rendikirje lisamine.</span><span class="sxs-lookup"><span data-stu-id="38fc3-114">This role is designed for daily users whose tasks include creating and posting monthly journal entries and adding new leases.</span></span> <span data-ttu-id="38fc3-115">See roll annab juurdepääsu kõikidele vara rentimise funktsioonidele.</span><span class="sxs-lookup"><span data-stu-id="38fc3-115">This role gives access to all Asset leasing functionality.</span></span> |
| <span data-ttu-id="38fc3-116">Rendi kuvamine</span><span class="sxs-lookup"><span data-stu-id="38fc3-116">View Lease</span></span>     | <span data-ttu-id="38fc3-117">Selle rolliga kasutajad saavad ainult vaadata rendi kirjeid, ajakavu ja käitada aruandeid.</span><span class="sxs-lookup"><span data-stu-id="38fc3-117">Users in this role can only view lease records, schedules, and run reports.</span></span> <span data-ttu-id="38fc3-118">Nad ei saa luua uusi rendikirjeid, muuta olemasolevaid rente ega luua töölehe kandeid rendi suhtes.</span><span class="sxs-lookup"><span data-stu-id="38fc3-118">They can't create new leases, edit existing leases, or create journal entries against leases.</span></span> <span data-ttu-id="38fc3-119">Roll on mõeldud kasutajatele, kes peavad vaid vaatama rente, rendi ajakavasid ja tehinguid, mis selle rendikirjega seoses aset leiavad.</span><span class="sxs-lookup"><span data-stu-id="38fc3-119">The role is designed for users who just have to view leases, lease schedules, and the transactions that occur against those leases.</span></span> |
| <span data-ttu-id="38fc3-120">Rendtnik</span><span class="sxs-lookup"><span data-stu-id="38fc3-120">Lease Clerk</span></span>    | <span data-ttu-id="38fc3-121">Selle rolliga kasutajad saavad luua ainult uusi rendikirjeid.</span><span class="sxs-lookup"><span data-stu-id="38fc3-121">Users in this role can only create new leases.</span></span> <span data-ttu-id="38fc3-122">Nad ei saa muuta ega kustutada olemasolevaid rendikirjeid, vaadata rendi ajakavasid ega sisestada rentimise töölehe kandeid.</span><span class="sxs-lookup"><span data-stu-id="38fc3-122">They can't edit or delete existing leases, view lease schedules, or post leasing journal entries.</span></span> <span data-ttu-id="38fc3-123">See roll on mõeldud kasutajatele, kes töötavad andmesisestuse võimalusega.</span><span class="sxs-lookup"><span data-stu-id="38fc3-123">This role is designed for users who work in a data entry capacity.</span></span> |

<span data-ttu-id="38fc3-124">Järgige järgmisi etappe, et määrata kasutajatele rollid, mida vara rentimisel kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="38fc3-124">Follow these steps to assign users to the roles that are used in Asset leasing.</span></span>

1. <span data-ttu-id="38fc3-125">Minge jaotisesse **Süsteemihaldus \> Turve \> Kasutajate rollidesse määramine**.</span><span class="sxs-lookup"><span data-stu-id="38fc3-125">Go to **System administration \> Security \> Assign users to roles**.</span></span>
2. <span data-ttu-id="38fc3-126">Valige roll **Rendi haldamine**, **Rentnik** või **Rendi vaatamine** ja valige seejärel **Kasutajate käsitsi määramine/välistamine**.</span><span class="sxs-lookup"><span data-stu-id="38fc3-126">Select the **Maintain lease**, **Lease clerk**, or **View lease** role, and then select **Manually assign/exclude users**.</span></span>
3. <span data-ttu-id="38fc3-127">Valige kasutaja, kes rollile määrata ja valige seejärel käsk **Määra rollile**.</span><span class="sxs-lookup"><span data-stu-id="38fc3-127">Select the user to assign to the role, and then select **Assign to role**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
