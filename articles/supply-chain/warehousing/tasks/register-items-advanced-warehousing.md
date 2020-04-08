---
title: Kaupade registreerimine täpsemaks ladustamiseks lubatud kauba puhul saabuva kauba töölehe abil
description: See protseduur selgitab kaupade registreerimist, kasutades kauba saabumise töölehte täpsemate laohaldusprotsesside kasutamisel.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2550e32db8b0d769f62c13654aa1dc1d201388ff
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148321"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="426a0-103">Kaupade registreerimine täpsemaks ladustamiseks lubatud kauba puhul saabuva kauba töölehe abil</span><span class="sxs-lookup"><span data-stu-id="426a0-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="426a0-104">See protseduur selgitab kaupade registreerimist, kasutades kauba saabumise töölehte täpsemate laohaldusprotsesside kasutamisel.</span><span class="sxs-lookup"><span data-stu-id="426a0-104">This procedure shows you how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="426a0-105">Seda teeb üldjuhul vastuvõtuametnik.</span><span class="sxs-lookup"><span data-stu-id="426a0-105">This would usually be done by a receiving clerk.</span></span> 

<span data-ttu-id="426a0-106">Saate seda protseduuri käitada demoettevõtte USMF andmetega või oma andmetega.</span><span class="sxs-lookup"><span data-stu-id="426a0-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="426a0-107">Enne selle juhendi käivitamist peate olema kinnitanud avatud ostutellimuse reaga ostutellimuse.</span><span class="sxs-lookup"><span data-stu-id="426a0-107">You need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="426a0-108">Rea kaup peab olema ladustatav ja see ei tohi kasutada tootevariante ja sellel ei tohi olla jälgimisdimensioone.</span><span class="sxs-lookup"><span data-stu-id="426a0-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="426a0-109">Samuti peavad kaubad olema seostatud laoala dimensioonigrupiga, mille puhul on laohaldusprotsessid lubatud.</span><span class="sxs-lookup"><span data-stu-id="426a0-109">And the item needs to be associated with a warehouse management process enabled storage dimension group.</span></span> <span data-ttu-id="426a0-110">Kasutatav ladu peab olema laohaldusprotsesside jaoks lubatud ja vastuvõtmiseks kasutatav asukoht peab olema litsentsiplaadiga juhitav.</span><span class="sxs-lookup"><span data-stu-id="426a0-110">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span> <span data-ttu-id="426a0-111">USMF-i kasutamisel saate ostutellimuse loomisel kasutada ettevõtte kontot 1001, ladu 51 ja kaupa M9200.</span><span class="sxs-lookup"><span data-stu-id="426a0-111">If you're using USMF, you can use company account 1001, Warehouse 51, and item M9200 to create your PO.</span></span> 

<span data-ttu-id="426a0-112">Märkige üles loodava ostutellimuse number ning ostutellimuse rea jaoks kasutatav kaubakood ja tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="426a0-112">Make a note of the number of the purchase order that you create, and also note the item number and the site that you used for your purchase order line.</span></span>


## <a name="create-an-item-arrival-journal-header"></a><span data-ttu-id="426a0-113">Kauba saabumise töölehe päise loomine</span><span class="sxs-lookup"><span data-stu-id="426a0-113">Create an item arrival journal header</span></span>
1. <span data-ttu-id="426a0-114">Minge jaotisse Kauba saabumine.</span><span class="sxs-lookup"><span data-stu-id="426a0-114">Go to Item arrival.</span></span>
2. <span data-ttu-id="426a0-115">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="426a0-115">Click New.</span></span>
3. <span data-ttu-id="426a0-116">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="426a0-116">In the Name field, type a value.</span></span>
    * <span data-ttu-id="426a0-117">Kui kasutate USMF-i, saate sisestada WHS-i.</span><span class="sxs-lookup"><span data-stu-id="426a0-117">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="426a0-118">Kui kasutate muid andmeid, peavad töölehel, mille nime valite, olema järgmised atribuudid: Kontrolli komplekteerimiskohta peab olema seatud valikule Ei ja Vahelao haldus peab olema seatud valikule Ei.</span><span class="sxs-lookup"><span data-stu-id="426a0-118">If you're using other data, the journal whose name you choose has to have the following properties: Check picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="426a0-119">Sisestage väärtus väljale Arv.</span><span class="sxs-lookup"><span data-stu-id="426a0-119">In the Number field, type a value.</span></span>
5. <span data-ttu-id="426a0-120">Sisestage väärtus väljale Koht.</span><span class="sxs-lookup"><span data-stu-id="426a0-120">In the Site field, type a value.</span></span>
    * <span data-ttu-id="426a0-121">Valige tegevuskoht, mida kasutasite oma ostutellimuse rea puhul.</span><span class="sxs-lookup"><span data-stu-id="426a0-121">Select the site that you used for your purchase order line.</span></span> <span data-ttu-id="426a0-122">See toimib vaikeväärtusena kõigile töölehe ridadele.</span><span class="sxs-lookup"><span data-stu-id="426a0-122">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="426a0-123">Kui kasutasite USMF-is ladu 51, valige tegevuskoht 5.</span><span class="sxs-lookup"><span data-stu-id="426a0-123">If you used warehouse 51 in USMF, choose site 5.</span></span>  
6. <span data-ttu-id="426a0-124">Sisestage väärtus väljale Ladu.</span><span class="sxs-lookup"><span data-stu-id="426a0-124">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="426a0-125">Valige valitud tegevuskoha jaoks kehtiv ladu.</span><span class="sxs-lookup"><span data-stu-id="426a0-125">Select a valid warehouse for the site that you've selected.</span></span> <span data-ttu-id="426a0-126">See toimib vaikeväärtusena kõigile töölehe ridadele.</span><span class="sxs-lookup"><span data-stu-id="426a0-126">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="426a0-127">Kui kasutate USMF-i näidisväärtusi, valige 51.</span><span class="sxs-lookup"><span data-stu-id="426a0-127">If you're using the example values in USMF, select 51.</span></span>  
7. <span data-ttu-id="426a0-128">Tippige väärtus väljale Asukoht.</span><span class="sxs-lookup"><span data-stu-id="426a0-128">In the Location field, type a value.</span></span>
    * <span data-ttu-id="426a0-129">Valige valitud lao jaoks kehtiv asukoht.</span><span class="sxs-lookup"><span data-stu-id="426a0-129">Select a valid location in the warehouse that you've selected.</span></span> <span data-ttu-id="426a0-130">Asukoht peab olema seotud litsentsiplaadiga juhitava asukohaprofiiliga.</span><span class="sxs-lookup"><span data-stu-id="426a0-130">The location has to be associated with a location profile, which is license plate controlled.</span></span> <span data-ttu-id="426a0-131">See toimib vaikeväärtusena kõigile töölehe ridadele.</span><span class="sxs-lookup"><span data-stu-id="426a0-131">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="426a0-132">Kui kasutate USMF-i näidisväärtusi, valige Bulk-008.</span><span class="sxs-lookup"><span data-stu-id="426a0-132">If you're using the example values in USMF, select Bulk-008.</span></span>  
8. <span data-ttu-id="426a0-133">Paremklõpsake rippnoolt väljal Llitsentsiplaat ja valige suvand Kuva üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="426a0-133">Right-click on the drop-down arrow in the License plate field and then select View details.</span></span>
9. <span data-ttu-id="426a0-134">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="426a0-134">Click New.</span></span>
10. <span data-ttu-id="426a0-135">Sisestage väärtus väljale Litsentsiplaat.</span><span class="sxs-lookup"><span data-stu-id="426a0-135">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="426a0-136">Märkige väärtus üles.</span><span class="sxs-lookup"><span data-stu-id="426a0-136">Make a note of the value.</span></span>  
11. <span data-ttu-id="426a0-137">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="426a0-137">Click Save.</span></span>
12. <span data-ttu-id="426a0-138">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="426a0-138">Close the page.</span></span>
13. <span data-ttu-id="426a0-139">Sisestage väärtus väljale Litsentsiplaat.</span><span class="sxs-lookup"><span data-stu-id="426a0-139">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="426a0-140">Sisestage vastloodud litsentsiplaadi väärtus.</span><span class="sxs-lookup"><span data-stu-id="426a0-140">Enter the value of the license plate that you just created.</span></span> <span data-ttu-id="426a0-141">See toimib vaikeväärtusena kõigile töölehe ridadele.</span><span class="sxs-lookup"><span data-stu-id="426a0-141">This will serve as a default value, which will default to all lines in the journal.</span></span>  
14. <span data-ttu-id="426a0-142">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="426a0-142">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="426a0-143">Rea lisamine</span><span class="sxs-lookup"><span data-stu-id="426a0-143">Add a line</span></span>
1. <span data-ttu-id="426a0-144">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="426a0-144">Click Add line.</span></span>
2. <span data-ttu-id="426a0-145">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="426a0-145">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="426a0-146">Sisestage ostutellimuse real kasutatav kaubakood.</span><span class="sxs-lookup"><span data-stu-id="426a0-146">Enter the item number that you used on the purchase order line.</span></span>  
3. <span data-ttu-id="426a0-147">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="426a0-147">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="426a0-148">Sisestage kogus, mille soovite registreerida.</span><span class="sxs-lookup"><span data-stu-id="426a0-148">Enter the quantity that you want to register.</span></span>  
    * <span data-ttu-id="426a0-149">Väli Kuupäev määratleb kuupäeva, millal selle kauba vaba kaubavaru kogus laos registreeritakse.</span><span class="sxs-lookup"><span data-stu-id="426a0-149">The Date field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    * <span data-ttu-id="426a0-150">Partii ID sisestab süsteem, kui esitatud teabe põhjal on võimalik see üheselt tuvastada.</span><span class="sxs-lookup"><span data-stu-id="426a0-150">The lot ID will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="426a0-151">Vastasel juhul peate selle lisama käsitsi.</span><span class="sxs-lookup"><span data-stu-id="426a0-151">Otherwise you will have to add this manually.</span></span> <span data-ttu-id="426a0-152">See on kohustuslik väli, mis seob registreeringu kindla lähtedokumendi reaga.</span><span class="sxs-lookup"><span data-stu-id="426a0-152">This is a mandatory field, which links this registration to a specific source document line.</span></span>  

## <a name="complete-the-registration"></a><span data-ttu-id="426a0-153">Registreerimise lõpule viimine</span><span class="sxs-lookup"><span data-stu-id="426a0-153">Complete the registration</span></span>
1. <span data-ttu-id="426a0-154">Klõpsake suvandit Kinnita.</span><span class="sxs-lookup"><span data-stu-id="426a0-154">Click Validate.</span></span>
    * <span data-ttu-id="426a0-155">See kontrollib, kas tööleht on sisestamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="426a0-155">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="426a0-156">Kui kontrollimine nurjub, peate tõrked enne töölehe sisestamist kõrvaldama.</span><span class="sxs-lookup"><span data-stu-id="426a0-156">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
2. <span data-ttu-id="426a0-157">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="426a0-157">Click OK.</span></span>
    * <span data-ttu-id="426a0-158">Klõpsake OK ja kontrollige teadet.</span><span class="sxs-lookup"><span data-stu-id="426a0-158">After you clicked OK, check the message.</span></span> <span data-ttu-id="426a0-159">Kuvatama peaks teade, et tööleht on korras.</span><span class="sxs-lookup"><span data-stu-id="426a0-159">There should be a message saying that the journal is OK.</span></span>  
3. <span data-ttu-id="426a0-160">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="426a0-160">Click Post.</span></span>
4. <span data-ttu-id="426a0-161">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="426a0-161">Click OK.</span></span>
    * <span data-ttu-id="426a0-162">Pärast OK klõpsamist kontrollige teateriba.</span><span class="sxs-lookup"><span data-stu-id="426a0-162">After you have clicked OK, check the message bar.</span></span> <span data-ttu-id="426a0-163">Kuvatama peaks teade, et toiming on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="426a0-163">There should be a message saying that the operation completed.</span></span>  
5. <span data-ttu-id="426a0-164">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="426a0-164">Close the page.</span></span>

