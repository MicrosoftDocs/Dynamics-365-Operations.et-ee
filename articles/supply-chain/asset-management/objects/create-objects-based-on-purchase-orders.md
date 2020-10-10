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
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 54c129d93e13e032cc5526a91c73d3363ed183db
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889021"
---
# <a name="create-assets-based-on-purchase-orders"></a><span data-ttu-id="52ffc-103">Ostutellimusel põhinevate varade loomine</span><span class="sxs-lookup"><span data-stu-id="52ffc-103">Create assets based on purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="52ffc-104">Selles teemas selgitatakse, kuidas luua vara üksuste loendit, mida saab kasutada varade loomisel hooldustööde jaoks varahalduses.</span><span class="sxs-lookup"><span data-stu-id="52ffc-104">This topic explains how you can create a list of asset items that can be used as a basis for creating assets for maintenance jobs in Asset Management.</span></span> <span data-ttu-id="52ffc-105">Vara üksuste põhjal saate vaadata nende kaupade kohta loodud ostutellimuse ridade loendit.</span><span class="sxs-lookup"><span data-stu-id="52ffc-105">Based on the asset items, you are able to view a list of the purchase order lines that have been created on those items.</span></span> <span data-ttu-id="52ffc-106">Selle funktsiooni eesmärk on hõlpsalt luua ostutellimusel põhinev vara varahalduses.</span><span class="sxs-lookup"><span data-stu-id="52ffc-106">The purpose of this functionality is to easily create an asset in Asset Management based on a purchase order.</span></span>

<span data-ttu-id="52ffc-107">Esmalt saate seadistada kaubad, mida kasutatakse varade loomisel ostutellimuse põhjal suvandis **Kaubagrupid**.</span><span class="sxs-lookup"><span data-stu-id="52ffc-107">First, you set up the items to be used for creating assets from a purchase order in **Asset items**.</span></span> <span data-ttu-id="52ffc-108">Pärast ostutellimuse rea loomist saate luua varad suvandis **Ootel varad**.</span><span class="sxs-lookup"><span data-stu-id="52ffc-108">After creating a purchase order line, you create the assets in **Pending assets**.</span></span> <span data-ttu-id="52ffc-109">Teil on võimalik otsustada, millises ostutellimuse etapis vara luuakse.</span><span class="sxs-lookup"><span data-stu-id="52ffc-109">It is possible to decide at which stage of the purchase order the asset should be created.</span></span>


## <a name="select-asset-items"></a><span data-ttu-id="52ffc-110">Kaubagrupi valimine</span><span class="sxs-lookup"><span data-stu-id="52ffc-110">Select asset items</span></span>

1. <span data-ttu-id="52ffc-111">Klõpsake **Varahaldus** > **Häälestus** > **Varad** > **Kaubad**.</span><span class="sxs-lookup"><span data-stu-id="52ffc-111">Click **Asset management** > **Setup** > **Assets** > **Items**.</span></span>
2. <span data-ttu-id="52ffc-112">Klõpsake suvandit **Uus**, et luua uus vara üksus.</span><span class="sxs-lookup"><span data-stu-id="52ffc-112">Click **New** to create a new asset item.</span></span>
3. <span data-ttu-id="52ffc-113">Valige kaup väljal **Kaubakood**.</span><span class="sxs-lookup"><span data-stu-id="52ffc-113">Select the item in the **Item number** field.</span></span> <span data-ttu-id="52ffc-114">Kui lahkute sellelt väljalt, sisestatakse kauba nimi automaatselt väljale **Toote nimetus**.</span><span class="sxs-lookup"><span data-stu-id="52ffc-114">When you leave that field, the item name is automatically inserted in the **Product name** field.</span></span>
4. <span data-ttu-id="52ffc-115">Kiirkaardil **Üldine** valige kauba jaoks vara tüüp.</span><span class="sxs-lookup"><span data-stu-id="52ffc-115">On the **General** FastTab, select an asset type for the item.</span></span>
5. <span data-ttu-id="52ffc-116">Valige kauba jaoks vara tootja ja mudel.</span><span class="sxs-lookup"><span data-stu-id="52ffc-116">Select asset manufacturer and model for the item.</span></span>
6. <span data-ttu-id="52ffc-117">Salvestage kaup.</span><span class="sxs-lookup"><span data-stu-id="52ffc-117">Save the item.</span></span>


## <a name="create-assets-from-pending-assets"></a><span data-ttu-id="52ffc-118">Varade loomine ootel varadest</span><span class="sxs-lookup"><span data-stu-id="52ffc-118">Create assets from pending assets</span></span>

1. <span data-ttu-id="52ffc-119">Klõpsake**Varahaldus** > **Ühised** > **Varad** > **Ootel varad**.</span><span class="sxs-lookup"><span data-stu-id="52ffc-119">Click **Asset management** > **Common** > **Assets** > **Pending Assets**.</span></span>
2. <span data-ttu-id="52ffc-120">Näete ostutellimuste värskendatud loendit, mis põhineb üksuses **Kaubagrupid** valitud kaupadel.</span><span class="sxs-lookup"><span data-stu-id="52ffc-120">You will see an updated list of the purchase orders based on the items selected in **Asset items**.</span></span>
3. <span data-ttu-id="52ffc-121">Saate filtreerida ostutellimuste olekut, et valida, millises elutsükli olekus vara tuleks luua.</span><span class="sxs-lookup"><span data-stu-id="52ffc-121">You can filter the status of purchase orders to select at which lifecycle state the asset should be created.</span></span> <span data-ttu-id="52ffc-122">Näiteks võite luua varasid ainult siis, kui toote sissetulek on ostutellimusel sisestatud.</span><span class="sxs-lookup"><span data-stu-id="52ffc-122">For example, you may only want to create assets when a product receipt has been posted on a purchase order.</span></span>
4. <span data-ttu-id="52ffc-123">Valige ostutellimuse real link **Viitenumber**, et nähe kauba kohta üksikasjalikku teavet.</span><span class="sxs-lookup"><span data-stu-id="52ffc-123">Select the **Reference number** link on a purchase order line to view detailed information about the item.</span></span>
5. <span data-ttu-id="52ffc-124">Kui soovite redigeerida, milliseid dimensioone kuvatakse kiirkaardil **Laoseisu dimensioonid**, klõpsake nuppu **Kuva dimensioonid** ja tehke oma valikud.</span><span class="sxs-lookup"><span data-stu-id="52ffc-124">If you want to edit which dimensions are displayed on the **Inventory dimensions** FastTab, click the **Display Dimensions** button, and make your selections.</span></span>
6. <span data-ttu-id="52ffc-125">Kui soovite luua ostutellimuse real põhineva vara, märkige loendilehe veeru märkeruut **Märge** ja klõpsake nuppu **Loo varad**.</span><span class="sxs-lookup"><span data-stu-id="52ffc-125">If you want to create an asset based on a purchase order line, select the check box in the **Mark** column for that line on the list page, and click **Create assets**.</span></span> <span data-ttu-id="52ffc-126">Kuvatakse sõnum, mis teavitab teid vara ID-st.</span><span class="sxs-lookup"><span data-stu-id="52ffc-126">A message will be displayed informing you of the asset ID.</span></span>
7. <span data-ttu-id="52ffc-127">Valige vara varade loendist **Kõik varad** ja klõpsake nuppu **Redigeeri**, et lisada vara kohta rohkem teavet.</span><span class="sxs-lookup"><span data-stu-id="52ffc-127">Select the asset in the **All assets** list and click **Edit** to add more information to the asset.</span></span>
8. <span data-ttu-id="52ffc-128">Kui soovite suvandis **Ootel varad** rea kustutada, kuna te ei soovi vara luua, märkige selle rea veerus märkeruut **Märge** ja klõpsake **Hülga ootel varad**.</span><span class="sxs-lookup"><span data-stu-id="52ffc-128">In **Pending assets**, if you want to delete a line because you don't want to create an asset, select the check box in the **Mark** column for that line, and click **Discard pending assets**.</span></span> <span data-ttu-id="52ffc-129">Kuvatakse sõnum, mis teavitab teid vara ID-st.</span><span class="sxs-lookup"><span data-stu-id="52ffc-129">A message will be displayed informing you of the asset ID.</span></span> <span data-ttu-id="52ffc-130">Te ei kustuta ostutellimust ega müügitellimust, vaid kirje, mille põhjal te oleksite saanud luua vara **varahalduses**.</span><span class="sxs-lookup"><span data-stu-id="52ffc-130">You are not deleting the purchase order or sales order, just the record from which you could have created an asset in **Asset Management**.</span></span>

>[!NOTE]
><span data-ttu-id="52ffc-131">Kõik tootedimensioonid (suurus, värv, konfiguratsioon jne) edastatakse automaatselt vara atribuutides.</span><span class="sxs-lookup"><span data-stu-id="52ffc-131">All product dimensions (size, color, configuration etc.) are automatically transferred to the asset attributes.</span></span> <span data-ttu-id="52ffc-132">Jälgimisdimensioonid (seerianumber) talletatakse vara loomisel otse vara juures.</span><span class="sxs-lookup"><span data-stu-id="52ffc-132">Tracking dimensions (serial number) are stored directly on the asset when the asset is created.</span></span>


## <a name="find-pending-assets"></a><span data-ttu-id="52ffc-133">Leia ootel varad</span><span class="sxs-lookup"><span data-stu-id="52ffc-133">Find pending assets</span></span>

<span data-ttu-id="52ffc-134">Ootel varade kontrollimiseks käivitage **Ootel varade loendus**.</span><span class="sxs-lookup"><span data-stu-id="52ffc-134">You can run a **Pending asset count** to check for pending assets.</span></span> <span data-ttu-id="52ffc-135">Näiteks saab seda funktsiooni kasutada teatise vastuvõtmiseks iga kord, kui ootel vara on vara loomiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="52ffc-135">For example, this function can be used for receiving a notification each time a pending asset is ready to be created as an asset.</span></span>

1. <span data-ttu-id="52ffc-136">Klõpsake **Varahaldus** > **Perioodiline** > **Varad** > **Ootel varade loendamine**.</span><span class="sxs-lookup"><span data-stu-id="52ffc-136">Click **Asset management** > **Periodic** > **Assets** > **Pending asset count**.</span></span>
2. <span data-ttu-id="52ffc-137">Klõpsake nuppu **OK** töö käivitamiseks ja loendi uuendamiseks suvandis **Ootel varad**.</span><span class="sxs-lookup"><span data-stu-id="52ffc-137">Click **OK** to run the job and update the list in **Pending assets**.</span></span>
3. <span data-ttu-id="52ffc-138">Selle töö saate seadistada pakett-tööna, nt üks kord päevas.</span><span class="sxs-lookup"><span data-stu-id="52ffc-138">You can set up this job to run as a batch job, for example, once each day.</span></span>

<span data-ttu-id="52ffc-139">**Ettevaatust:** kui andmeid muudetakse ostutellimusel *pärast* seda, kui olete loonud seotud kauba põhjal vara, ei kajastu need muudatused varas.</span><span class="sxs-lookup"><span data-stu-id="52ffc-139">**Caution:** If data is changed on a purchase order *after* you have created an asset based on the appertaining item, those changes will not be reflected on the asset.</span></span>
