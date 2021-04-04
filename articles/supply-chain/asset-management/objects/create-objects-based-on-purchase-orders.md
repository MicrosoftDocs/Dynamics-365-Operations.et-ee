---
title: Ostutellimusel põhinevate varade loomine
description: Selles teemas selgitatakse, kuidas luua vara üksuste loendit, mida saab kasutada varade loomisel hooldustööde jaoks varahalduses.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97b40528db4acc2627b087e8ee90bfd1fd79efa7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253274"
---
# <a name="create-assets-based-on-purchase-orders"></a><span data-ttu-id="ade0e-103">Ostutellimusel põhinevate varade loomine</span><span class="sxs-lookup"><span data-stu-id="ade0e-103">Create assets based on purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="ade0e-104">Selles teemas selgitatakse, kuidas luua vara üksuste loendit, mida saab kasutada varade loomisel hooldustööde jaoks varahalduses.</span><span class="sxs-lookup"><span data-stu-id="ade0e-104">This topic explains how you can create a list of asset items that can be used as a basis for creating assets for maintenance jobs in Asset Management.</span></span> <span data-ttu-id="ade0e-105">Vara üksuste põhjal saate vaadata nende kaupade kohta loodud ostutellimuse ridade loendit.</span><span class="sxs-lookup"><span data-stu-id="ade0e-105">Based on the asset items, you are able to view a list of the purchase order lines that have been created on those items.</span></span> <span data-ttu-id="ade0e-106">Selle funktsiooni eesmärk on hõlpsalt luua ostutellimusel põhinev vara varahalduses.</span><span class="sxs-lookup"><span data-stu-id="ade0e-106">The purpose of this functionality is to easily create an asset in Asset Management based on a purchase order.</span></span>

<span data-ttu-id="ade0e-107">Esmalt saate seadistada kaubad, mida kasutatakse varade loomisel ostutellimuse põhjal suvandis **Kaubagrupid**.</span><span class="sxs-lookup"><span data-stu-id="ade0e-107">First, you set up the items to be used for creating assets from a purchase order in **Asset items**.</span></span> <span data-ttu-id="ade0e-108">Pärast ostutellimuse rea loomist saate luua varad suvandis **Ootel varad**.</span><span class="sxs-lookup"><span data-stu-id="ade0e-108">After creating a purchase order line, you create the assets in **Pending assets**.</span></span> <span data-ttu-id="ade0e-109">Teil on võimalik otsustada, millises ostutellimuse etapis vara luuakse.</span><span class="sxs-lookup"><span data-stu-id="ade0e-109">It is possible to decide at which stage of the purchase order the asset should be created.</span></span>


## <a name="select-asset-items"></a><span data-ttu-id="ade0e-110">Kaubagrupi valimine</span><span class="sxs-lookup"><span data-stu-id="ade0e-110">Select asset items</span></span>

1. <span data-ttu-id="ade0e-111">Klõpsake **Varahaldus** > **Häälestus** > **Varad** > **Kaubad**.</span><span class="sxs-lookup"><span data-stu-id="ade0e-111">Click **Asset management** > **Setup** > **Assets** > **Items**.</span></span>
2. <span data-ttu-id="ade0e-112">Klõpsake suvandit **Uus**, et luua uus vara üksus.</span><span class="sxs-lookup"><span data-stu-id="ade0e-112">Click **New** to create a new asset item.</span></span>
3. <span data-ttu-id="ade0e-113">Valige kaup väljal **Kaubakood**.</span><span class="sxs-lookup"><span data-stu-id="ade0e-113">Select the item in the **Item number** field.</span></span> <span data-ttu-id="ade0e-114">Kui lahkute sellelt väljalt, sisestatakse kauba nimi automaatselt väljale **Toote nimetus**.</span><span class="sxs-lookup"><span data-stu-id="ade0e-114">When you leave that field, the item name is automatically inserted in the **Product name** field.</span></span>
4. <span data-ttu-id="ade0e-115">Kiirkaardil **Üldine** valige kauba jaoks vara tüüp.</span><span class="sxs-lookup"><span data-stu-id="ade0e-115">On the **General** FastTab, select an asset type for the item.</span></span>
5. <span data-ttu-id="ade0e-116">Valige kauba jaoks vara tootja ja mudel.</span><span class="sxs-lookup"><span data-stu-id="ade0e-116">Select asset manufacturer and model for the item.</span></span>
6. <span data-ttu-id="ade0e-117">Salvestage kaup.</span><span class="sxs-lookup"><span data-stu-id="ade0e-117">Save the item.</span></span>


## <a name="create-assets-from-pending-assets"></a><span data-ttu-id="ade0e-118">Varade loomine ootel varadest</span><span class="sxs-lookup"><span data-stu-id="ade0e-118">Create assets from pending assets</span></span>

1. <span data-ttu-id="ade0e-119">Klõpsake **Varahaldus** > **Ühised** > **Varad** > **Ootel varad**.</span><span class="sxs-lookup"><span data-stu-id="ade0e-119">Click **Asset management** > **Common** > **Assets** > **Pending Assets**.</span></span>
2. <span data-ttu-id="ade0e-120">Näete ostutellimuste värskendatud loendit, mis põhineb üksuses **Kaubagrupid** valitud kaupadel.</span><span class="sxs-lookup"><span data-stu-id="ade0e-120">You will see an updated list of the purchase orders based on the items selected in **Asset items**.</span></span>
3. <span data-ttu-id="ade0e-121">Saate filtreerida ostutellimuste olekut, et valida, millises elutsükli olekus vara tuleks luua.</span><span class="sxs-lookup"><span data-stu-id="ade0e-121">You can filter the status of purchase orders to select at which lifecycle state the asset should be created.</span></span> <span data-ttu-id="ade0e-122">Näiteks võite luua varasid ainult siis, kui toote sissetulek on ostutellimusel sisestatud.</span><span class="sxs-lookup"><span data-stu-id="ade0e-122">For example, you may only want to create assets when a product receipt has been posted on a purchase order.</span></span>
4. <span data-ttu-id="ade0e-123">Valige ostutellimuse real link **Viitenumber**, et nähe kauba kohta üksikasjalikku teavet.</span><span class="sxs-lookup"><span data-stu-id="ade0e-123">Select the **Reference number** link on a purchase order line to view detailed information about the item.</span></span>
5. <span data-ttu-id="ade0e-124">Kui soovite redigeerida, milliseid dimensioone kuvatakse kiirkaardil **Laoseisu dimensioonid**, klõpsake nuppu **Kuva dimensioonid** ja tehke oma valikud.</span><span class="sxs-lookup"><span data-stu-id="ade0e-124">If you want to edit which dimensions are displayed on the **Inventory dimensions** FastTab, click the **Display Dimensions** button, and make your selections.</span></span>
6. <span data-ttu-id="ade0e-125">Kui soovite luua ostutellimuse real põhineva vara, märkige loendilehe veeru märkeruut **Märge** ja klõpsake nuppu **Loo varad**.</span><span class="sxs-lookup"><span data-stu-id="ade0e-125">If you want to create an asset based on a purchase order line, select the check box in the **Mark** column for that line on the list page, and click **Create assets**.</span></span> <span data-ttu-id="ade0e-126">Kuvatakse sõnum, mis teavitab teid vara ID-st.</span><span class="sxs-lookup"><span data-stu-id="ade0e-126">A message will be displayed informing you of the asset ID.</span></span>
7. <span data-ttu-id="ade0e-127">Valige vara varade loendist **Kõik varad** ja klõpsake nuppu **Redigeeri**, et lisada vara kohta rohkem teavet.</span><span class="sxs-lookup"><span data-stu-id="ade0e-127">Select the asset in the **All assets** list and click **Edit** to add more information to the asset.</span></span>
8. <span data-ttu-id="ade0e-128">Kui soovite suvandis **Ootel varad** rea kustutada, kuna te ei soovi vara luua, märkige selle rea veerus märkeruut **Märge** ja klõpsake **Hülga ootel varad**.</span><span class="sxs-lookup"><span data-stu-id="ade0e-128">In **Pending assets**, if you want to delete a line because you don't want to create an asset, select the check box in the **Mark** column for that line, and click **Discard pending assets**.</span></span> <span data-ttu-id="ade0e-129">Kuvatakse sõnum, mis teavitab teid vara ID-st.</span><span class="sxs-lookup"><span data-stu-id="ade0e-129">A message will be displayed informing you of the asset ID.</span></span> <span data-ttu-id="ade0e-130">Te ei kustuta ostutellimust ega müügitellimust, vaid kirje, mille põhjal te oleksite saanud luua vara **varahalduses**.</span><span class="sxs-lookup"><span data-stu-id="ade0e-130">You are not deleting the purchase order or sales order, just the record from which you could have created an asset in **Asset Management**.</span></span>

>[!NOTE]
><span data-ttu-id="ade0e-131">Kõik tootedimensioonid (suurus, värv, konfiguratsioon jne) edastatakse automaatselt vara atribuutides.</span><span class="sxs-lookup"><span data-stu-id="ade0e-131">All product dimensions (size, color, configuration etc.) are automatically transferred to the asset attributes.</span></span> <span data-ttu-id="ade0e-132">Jälgimisdimensioonid (seerianumber) talletatakse vara loomisel otse vara juures.</span><span class="sxs-lookup"><span data-stu-id="ade0e-132">Tracking dimensions (serial number) are stored directly on the asset when the asset is created.</span></span>


## <a name="find-pending-assets"></a><span data-ttu-id="ade0e-133">Leia ootel varad</span><span class="sxs-lookup"><span data-stu-id="ade0e-133">Find pending assets</span></span>

<span data-ttu-id="ade0e-134">Ootel varade kontrollimiseks käivitage **Ootel varade loendus**.</span><span class="sxs-lookup"><span data-stu-id="ade0e-134">You can run a **Pending asset count** to check for pending assets.</span></span> <span data-ttu-id="ade0e-135">Näiteks saab seda funktsiooni kasutada teatise vastuvõtmiseks iga kord, kui ootel vara on vara loomiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="ade0e-135">For example, this function can be used for receiving a notification each time a pending asset is ready to be created as an asset.</span></span>

1. <span data-ttu-id="ade0e-136">Klõpsake **Varahaldus** > **Perioodiline** > **Varad** > **Ootel varade loendamine**.</span><span class="sxs-lookup"><span data-stu-id="ade0e-136">Click **Asset management** > **Periodic** > **Assets** > **Pending asset count**.</span></span>
2. <span data-ttu-id="ade0e-137">Klõpsake nuppu **OK** töö käivitamiseks ja loendi uuendamiseks suvandis **Ootel varad**.</span><span class="sxs-lookup"><span data-stu-id="ade0e-137">Click **OK** to run the job and update the list in **Pending assets**.</span></span>
3. <span data-ttu-id="ade0e-138">Selle töö saate seadistada pakett-tööna, nt üks kord päevas.</span><span class="sxs-lookup"><span data-stu-id="ade0e-138">You can set up this job to run as a batch job, for example, once each day.</span></span>

<span data-ttu-id="ade0e-139">**Ettevaatust:** kui andmeid muudetakse ostutellimusel *pärast* seda, kui olete loonud seotud kauba põhjal vara, ei kajastu need muudatused varas.</span><span class="sxs-lookup"><span data-stu-id="ade0e-139">**Caution:** If data is changed on a purchase order *after* you have created an asset based on the appertaining item, those changes will not be reflected on the asset.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]