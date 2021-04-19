---
title: Kaupade registreerimine täpsemaks ladustamiseks lubatud kauba puhul saabuva kauba töölehe abil
description: See teema kirjeldab stsenaariumit, mis selgitab kaupade registreerimist, kasutades kauba saabumise töölehte täpsemate laohaldusprotsesside kasutamisel.
author: ShylaThompson
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c58aa1cec6c0bfe33fa1ef90267dcd8ac1218157
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830830"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="0a777-103">Kaupade registreerimine täpsemaks ladustamiseks lubatud kauba puhul saabuva kauba töölehe abil</span><span class="sxs-lookup"><span data-stu-id="0a777-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0a777-104">See teema kirjeldab stsenaariumit, mis selgitab kaupade registreerimist, kasutades kauba saabumise töölehte täpsemate laohaldusprotsesside kasutamisel.</span><span class="sxs-lookup"><span data-stu-id="0a777-104">This topic presents a scenario that shows how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="0a777-105">Seda teeb üldjuhul vastuvõtuametnik.</span><span class="sxs-lookup"><span data-stu-id="0a777-105">This would usually be done by a receiving clerk.</span></span>

## <a name="enable-sample-data"></a><span data-ttu-id="0a777-106">Luba näidisandmed</span><span class="sxs-lookup"><span data-stu-id="0a777-106">Enable sample data</span></span>

<span data-ttu-id="0a777-107">Selle stsenaariumi läbimiseks, kasutades selles teemas määratud näidiskirjeid ja -väärtusi, peate kasutama süsteemi, kuhu on installitud standardsed demoandmed, ning enne alustamist peate valima *USMF* juriidilise isiku.</span><span class="sxs-lookup"><span data-stu-id="0a777-107">To work through this scenario using the sample records and values specified in this topic, you must be using a system where the standard demo data is installed, and you must select the *USMF* legal entity before you begin.</span></span>

<span data-ttu-id="0a777-108">Selle stsenaariumi saate läbi töötada, asendades väärtused oma andmetega, kui teil on saadaval järgmised andmed.</span><span class="sxs-lookup"><span data-stu-id="0a777-108">You can instead work through this scenario by substituting values from your own data provided that you have the following data available:</span></span>

- <span data-ttu-id="0a777-109">Kinnitatud ostutellimus peab olema avatud ostutellimuse reaga.</span><span class="sxs-lookup"><span data-stu-id="0a777-109">You must have a confirmed purchase order with an open purchase order line.</span></span>
- <span data-ttu-id="0a777-110">Real olev kaup peab olema ladustatav.</span><span class="sxs-lookup"><span data-stu-id="0a777-110">The item on the line must be stocked.</span></span> <span data-ttu-id="0a777-111">See ei tohi kasutada tootevariante ja sellel ei tohi olla jälgimisdimensioone.</span><span class="sxs-lookup"><span data-stu-id="0a777-111">It must not use product variants, and must not have tracking dimensions.</span></span>
- <span data-ttu-id="0a777-112">Üksus peab olema seotud salvestusmõõtmete grupiga, millel on lubatud laohalduse protsess.</span><span class="sxs-lookup"><span data-stu-id="0a777-112">The item must be associated with a storage dimension group that has warehouse management process enabled.</span></span>
- <span data-ttu-id="0a777-113">Kasutatav ladu peab olema laohaldusprotsesside jaoks lubatud ja vastuvõtmiseks kasutatav asukoht peab olema litsentsiplaadiga juhitav.</span><span class="sxs-lookup"><span data-stu-id="0a777-113">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span>

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a><span data-ttu-id="0a777-114">Kauba saabumise töölehe päise loomine, mis kasutab laohaldust</span><span class="sxs-lookup"><span data-stu-id="0a777-114">Create an item arrival journal header that uses warehouse management</span></span>

<span data-ttu-id="0a777-115">Järgnev stsenaarium näitab, kuidas luua saabuva kauba töölehe päist, mis kasutab laohaldust.</span><span class="sxs-lookup"><span data-stu-id="0a777-115">The following scenario shows how to create an item arrival journal header that uses warehouse management:</span></span>

1. <span data-ttu-id="0a777-116">Veenduge, et teie süsteem sisaldaks kinnitatud ostutellimust, mis vastab eelmises jaotises toodud nõuetele.</span><span class="sxs-lookup"><span data-stu-id="0a777-116">Make sure your system contains a confirmed purchase order that fulfils the requirements outlined in the previous section.</span></span> <span data-ttu-id="0a777-117">See stsenaarium kasutab ostutellimust ettevõttele *USMF*, hankija kontole *1001*, laole *51* tellimuse reaga *10 PL* (10 kaubaalust) kaubakoodiga *M9200*.</span><span class="sxs-lookup"><span data-stu-id="0a777-117">This scenario uses a purchase order for company *USMF*, vendor account *1001*, warehouse *51*, with an order line for *10 PL* (10 pallets) of item number *M9200*.</span></span>
1. <span data-ttu-id="0a777-118">Märkige üles ostutellimuse number, mida kasutate.</span><span class="sxs-lookup"><span data-stu-id="0a777-118">Make a note of the purchase order number that you will use.</span></span>
1. <span data-ttu-id="0a777-119">Avage **Varude haldus \> Töölehe sisestused \> Kauba saabumine \> Kauba saabumine**.</span><span class="sxs-lookup"><span data-stu-id="0a777-119">Go to **Inventory management \> Journal entries \> Item arrival \> Item arrival**.</span></span>
1. <span data-ttu-id="0a777-120">Valige Toimingupaanil suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="0a777-120">Select **New** on the Action Pane.</span></span>
1. <span data-ttu-id="0a777-121">Avaneb dialoogiboks **Laohalduse töölehe loomine**.</span><span class="sxs-lookup"><span data-stu-id="0a777-121">The **Create warehouse management journal** dialog box opens.</span></span> <span data-ttu-id="0a777-122">Valige väljal **Nimi** töölehe nimi.</span><span class="sxs-lookup"><span data-stu-id="0a777-122">Select a journal name in the **Name** field.</span></span>
    - <span data-ttu-id="0a777-123">Kui kasutate *USMF* näidisandmeid, valige *WHS*.</span><span class="sxs-lookup"><span data-stu-id="0a777-123">If you are using *USMF* sample data, select *WHS*.</span></span>
    - <span data-ttu-id="0a777-124">Kui kasutate oma andmeid, peab teie valitava töölehe valik **Kontrolli komplekteerimisasukohta** olema seadistatud valikule *Ei* ja **Vahelao haldus** valikule *Ei*.</span><span class="sxs-lookup"><span data-stu-id="0a777-124">If you're using your own data, the journal you choose must have **Check picking location** set to *No* and **Quarantine management** set to *No*.</span></span>
1. <span data-ttu-id="0a777-125">Määrake **Viide** väärtuseks *Ostutellimus*.</span><span class="sxs-lookup"><span data-stu-id="0a777-125">Set **Reference** to *Purchase order*.</span></span>
1. <span data-ttu-id="0a777-126">Määrake **Konto number** väärtuseks *1001*.</span><span class="sxs-lookup"><span data-stu-id="0a777-126">Set **Account number** to *1001*.</span></span>
1. <span data-ttu-id="0a777-127">Määrake **Number** selle ostutellimuse numbrile, mille selle teostamistaotluse puhul määratlete.</span><span class="sxs-lookup"><span data-stu-id="0a777-127">Set **Number** to the number of the purchase order that you identified for this exercise.</span></span>

    <span data-ttu-id="0a777-128">![Saabuva kauba tööleht](../media/item-arrival-journal-header.png "Saabuva kauba tööleht")</span><span class="sxs-lookup"><span data-stu-id="0a777-128">![Item arrival journal](../media/item-arrival-journal-header.png "Item arrival journal")</span></span>

1. <span data-ttu-id="0a777-129">Valige töölehe päise loomiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a777-129">Select the **OK** to create the journal header.</span></span>
1. <span data-ttu-id="0a777-130">Valige jaotises **Töölehe read** suvand **Lisa rida** ja sisestage järgmised andmed.</span><span class="sxs-lookup"><span data-stu-id="0a777-130">In the **Journal lines** section, select **Add line** and enter the following data:</span></span>
    - <span data-ttu-id="0a777-131">**Kauba number** – määrake väärtuseks *M9200*.</span><span class="sxs-lookup"><span data-stu-id="0a777-131">**Item number** – Set to *M9200*.</span></span> <span data-ttu-id="0a777-132">**Piirkond**, **Ladu** ja **Kogus** seatakse 10 kaubaaluse laokande andmete põhjal (1000 ea.).</span><span class="sxs-lookup"><span data-stu-id="0a777-132">The **Site**, **Warehouse**, and **Quantity** will get set based on the inventory transaction data for the 10 pallets (1000 ea.).</span></span>
    - <span data-ttu-id="0a777-133">**Asukoht** – seadistage väärtuseks *001*.</span><span class="sxs-lookup"><span data-stu-id="0a777-133">**Location** – Set to  *001*.</span></span> <span data-ttu-id="0a777-134">See konkreetne asukoht ei jälgi litsentsiplaate.</span><span class="sxs-lookup"><span data-stu-id="0a777-134">This specific location does not track license plates.</span></span>

    <span data-ttu-id="0a777-135">![Kauba saabumistöölehtede rida](../media/item-arrival-journal-line.png "Kauba saabumistöölehtede rida")</span><span class="sxs-lookup"><span data-stu-id="0a777-135">![Item arrival journal line](../media/item-arrival-journal-line.png "Item arrival journal line")</span></span>

    > [!NOTE]
    > <span data-ttu-id="0a777-136">Väli **Kuupäev** määratleb kuupäeva, millal selle kauba vaba kaubavaru kogus laos registreeritakse.</span><span class="sxs-lookup"><span data-stu-id="0a777-136">The **Date** field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    >
    > <span data-ttu-id="0a777-137">**Partii ID** sisestab süsteem, kui esitatud teabe põhjal on võimalik see üheselt tuvastada.</span><span class="sxs-lookup"><span data-stu-id="0a777-137">The **Lot ID** will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="0a777-138">Vastasel juhul peate selle sisestama käsitsi.</span><span class="sxs-lookup"><span data-stu-id="0a777-138">Otherwise you will have to enter this manually.</span></span> <span data-ttu-id="0a777-139">See on vajalik väli, mis seob registreeringu kindla lähtedokumendi reaga.</span><span class="sxs-lookup"><span data-stu-id="0a777-139">This is a required field, which links this registration to a specific source document line.</span></span>  

1. <span data-ttu-id="0a777-140">Valige toimingupaanil **Valideeri**.</span><span class="sxs-lookup"><span data-stu-id="0a777-140">Select **Validate** on the Action Pane.</span></span> <span data-ttu-id="0a777-141">See kontrollib, kas tööleht on sisestamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="0a777-141">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="0a777-142">Kui kontrollimine nurjub, peate tõrked enne töölehe sisestamist kõrvaldama.</span><span class="sxs-lookup"><span data-stu-id="0a777-142">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
1. <span data-ttu-id="0a777-143">Avaneb dialoogiboks **Kontrolli töölehti**.</span><span class="sxs-lookup"><span data-stu-id="0a777-143">The **Check journal** dialog box opens.</span></span> <span data-ttu-id="0a777-144">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a777-144">Select **OK**.</span></span>
1. <span data-ttu-id="0a777-145">Vaadake üle sõnumiriba.</span><span class="sxs-lookup"><span data-stu-id="0a777-145">Review the message bar.</span></span> <span data-ttu-id="0a777-146">Kuvatama peaks teade, et toiming on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="0a777-146">There should be a message denoting that the operation was completed.</span></span>  
1. <span data-ttu-id="0a777-147">Tehke toimingupaanil valik **Väljastamine**.</span><span class="sxs-lookup"><span data-stu-id="0a777-147">Select **Post** on the Action Pane.</span></span>
1. <span data-ttu-id="0a777-148">Avaneb dialoogiboks **Sisesta tööleht**.</span><span class="sxs-lookup"><span data-stu-id="0a777-148">The **Post journal** dialog box opens.</span></span> <span data-ttu-id="0a777-149">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a777-149">Select **OK**.</span></span>
1. <span data-ttu-id="0a777-150">Vaadake üle sõnumiriba.</span><span class="sxs-lookup"><span data-stu-id="0a777-150">Review the message bar.</span></span> <span data-ttu-id="0a777-151">Kuvatama peaks teade, et toiming on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="0a777-151">There should be messages denoting that the operation completed.</span></span>
1. <span data-ttu-id="0a777-152">Valige toimingupaanil **Funktsioonid > Toote tšekk** ostutellimuse rea värskendamiseks ja toote tšeki sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="0a777-152">Select **Functions > Product receipt** on the Action Pane to update the purchase order line and post a product receipt.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
