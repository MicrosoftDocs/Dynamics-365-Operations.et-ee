---
title: Puudumistaotluste loomine
description: Selles teemas antakse ülevaade hooldustaotluste haldamise kohta varahalduses.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c911f1a0cd895899f85ae8f5ec4c3fcc847c0cf0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205157"
---
# <a name="maintenance-requests"></a><span data-ttu-id="3d301-103">Puudumistaotluste loomine</span><span class="sxs-lookup"><span data-stu-id="3d301-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="3d301-104">Hooldustaotlused on märkmed või avaldused, mis on loodud teavitama haldurit või plaanijat, et vara võib vajada hooldust või parandustööd, kuid ilma töötellimust loomata.</span><span class="sxs-lookup"><span data-stu-id="3d301-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="3d301-105">Kui hooldustaotluse sisu loetakse kehtivaks, saab töötellimuse seejärel hooldustaotluse põhjal luua.</span><span class="sxs-lookup"><span data-stu-id="3d301-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="3d301-106">Hooldustaotlusi saab luua iga vara kohta varahalduses.</span><span class="sxs-lookup"><span data-stu-id="3d301-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="3d301-107">Sõltuvalt sellest, kuidas teie ettevõte kasutab hooldustaotlusi, saab luua erinevat tüüpi hooldustaotlusi.</span><span class="sxs-lookup"><span data-stu-id="3d301-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="3d301-108">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="3d301-108">Here are some examples:</span></span>

- <span data-ttu-id="3d301-109">Puudumistaotluste loomine</span><span class="sxs-lookup"><span data-stu-id="3d301-109">Maintenance requests</span></span>
- <span data-ttu-id="3d301-110">Märkmed</span><span class="sxs-lookup"><span data-stu-id="3d301-110">Notes</span></span>
- <span data-ttu-id="3d301-111">Parandused või täiustused</span><span class="sxs-lookup"><span data-stu-id="3d301-111">Corrections or enhancements</span></span>
- <span data-ttu-id="3d301-112">Investeeringud</span><span class="sxs-lookup"><span data-stu-id="3d301-112">Investments</span></span>
- <span data-ttu-id="3d301-113">Allika parandamine (seda tüüpi kasutatakse, kui saate varasid mõnest muust asukohast, et saaksite hooldust või parandustööd teha ja seejärel pärast töö lõpule viimist töö tagastada.)</span><span class="sxs-lookup"><span data-stu-id="3d301-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="3d301-114">Puudumistaotluste loomine</span><span class="sxs-lookup"><span data-stu-id="3d301-114">View maintenance requests</span></span>

<span data-ttu-id="3d301-115">Hoolduspäringute vaatamiseks valige **Varahaldus**\>**Ühised**\>**Hooldustaotlused**\>**Kõik hooldustaotlused**, **Aktiivsed hooldustaotlused**või **Minu funktsionaalse asukoha hooldustaotlused**.</span><span class="sxs-lookup"><span data-stu-id="3d301-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="3d301-116">Iga loendileht kuvab osa hooldustaotlusega seotud teabest.</span><span class="sxs-lookup"><span data-stu-id="3d301-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![Hooldusnõuete vaatamine](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="3d301-118">Kasutage loendilehte **Minu funktsionaalse asukoha hooldustaotlused**, et vaadata hooldustaotluste loendit, mis sisaldab kas funktsionaalseid asukohti, millega olete töötajana seotud või varasid, mis on installitud funktsionaalsetele asukohtadele, millega olete töötajana seotud.</span><span class="sxs-lookup"><span data-stu-id="3d301-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="3d301-119">(Lisateavet hooldustöötajate funktsionaalsete asukohtade häälestamise kohta vt teemast [Hooldustöötajad ja töörühmad](../setup-for-objects/workers-and-worker-groups.md).)</span><span class="sxs-lookup"><span data-stu-id="3d301-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="3d301-120">Kuigi kliendikonto teave on saadaval vara teenuse halduses (väline hooldus), see ei ole saadaval varahalduses (sisemine hooldus).</span><span class="sxs-lookup"><span data-stu-id="3d301-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="3d301-121">Kirje üksikasjade vaate avamiseks loendilehel **Kõik hooldustaotlused** ruudustiku vaates, valige link veerus **Hooldustaotlused**.</span><span class="sxs-lookup"><span data-stu-id="3d301-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![Kuva hooldusnõude üksikasjad](media/02-manage-maintenance-requests.png)

<span data-ttu-id="3d301-123">Tegumiriba nupud on korraldatud vahekaartidel.</span><span class="sxs-lookup"><span data-stu-id="3d301-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="3d301-124">Järgmises tabelis kirjeldatakse lühidalt mooduli Asse Management nuppe.</span><span class="sxs-lookup"><span data-stu-id="3d301-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="3d301-125">Nupu nimi</span><span class="sxs-lookup"><span data-stu-id="3d301-125">Button name</span></span>                      | <span data-ttu-id="3d301-126">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3d301-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="3d301-127">Redigeerimine</span><span class="sxs-lookup"><span data-stu-id="3d301-127">Edit</span></span>                             | <span data-ttu-id="3d301-128">Saate redigeerida valitud hankija nõude kaupa.</span><span class="sxs-lookup"><span data-stu-id="3d301-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="3d301-129">Uus</span><span class="sxs-lookup"><span data-stu-id="3d301-129">New</span></span>                              | <span data-ttu-id="3d301-130">Loob uue hankija nõude</span><span class="sxs-lookup"><span data-stu-id="3d301-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="3d301-131">Kustutamine</span><span class="sxs-lookup"><span data-stu-id="3d301-131">Delete</span></span>                           | <span data-ttu-id="3d301-132">Kustuta valitud kategooria taotlus</span><span class="sxs-lookup"><span data-stu-id="3d301-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="3d301-133">Töötellimuse kaust</span><span class="sxs-lookup"><span data-stu-id="3d301-133">Work order pool</span></span>                  | <span data-ttu-id="3d301-134">Ühenda valitud hooldustaotlus töökäsu kaustaga.</span><span class="sxs-lookup"><span data-stu-id="3d301-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="3d301-135">Töötellimus</span><span class="sxs-lookup"><span data-stu-id="3d301-135">Work order</span></span>                       | <span data-ttu-id="3d301-136">Loo töötellimus valitud hooldustaotluse põhjal.</span><span class="sxs-lookup"><span data-stu-id="3d301-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="3d301-137">Vara tõrge</span><span class="sxs-lookup"><span data-stu-id="3d301-137">Asset fault</span></span>                      | <span data-ttu-id="3d301-138">Klõpsake **Vara tõrked**, kus saate luua valitud hooldustaotlusele tõrke registreerimise.</span><span class="sxs-lookup"><span data-stu-id="3d301-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="3d301-139">Töötellimused</span><span class="sxs-lookup"><span data-stu-id="3d301-139">Work orders</span></span>                      | <span data-ttu-id="3d301-140">Saate kuvada kõigi valitud hooldustaotlusega seotud töötellimuste loendi.</span><span class="sxs-lookup"><span data-stu-id="3d301-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="3d301-141">Valige Uuenda hoolduse taotluse olekut.</span><span class="sxs-lookup"><span data-stu-id="3d301-141">Update maintenance request state</span></span> | <span data-ttu-id="3d301-142">Valige Uuenda hoolduse taotluse olekut.</span><span class="sxs-lookup"><span data-stu-id="3d301-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="3d301-143">Elutsükli oleku logi</span><span class="sxs-lookup"><span data-stu-id="3d301-143">Lifecycle state log</span></span>              | <span data-ttu-id="3d301-144">Vaadake logi, mis näitab valitud hooldustaotluse olelustsüklit.</span><span class="sxs-lookup"><span data-stu-id="3d301-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="3d301-145">Hooldustaotluse tüübid</span><span class="sxs-lookup"><span data-stu-id="3d301-145">Maintenance request details</span></span>      | <span data-ttu-id="3d301-146">Saate printida aruande, kus kuvatakse valitud hooldustaotluse üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="3d301-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="3d301-147">Saada laenuvara</span><span class="sxs-lookup"><span data-stu-id="3d301-147">Send loan asset</span></span>                  | <span data-ttu-id="3d301-148">Saate valida laenuvara, mis peaks olema valitud hooldustaotluses valitud vara ajutiseks asenduseks.</span><span class="sxs-lookup"><span data-stu-id="3d301-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="3d301-149">Tagastuslaenu vara</span><span class="sxs-lookup"><span data-stu-id="3d301-149">Return loan asset</span></span>                | <span data-ttu-id="3d301-150">Registreeri laenuvarad tagastatud</span><span class="sxs-lookup"><span data-stu-id="3d301-150">Register the loan asset as returned.</span></span> |

