---
title: Saatmisteabe häälestamine
description: See teema kirjeldab, kuidas seadistada saatmisteavet moodulis Väljalaadimiskulu.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 5093e42b0b5247c24c271ad50c80889516586d58
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020883"
---
# <a name="shipping-information-setup"></a><span data-ttu-id="60d02-103">Saatmisteabe häälestamine</span><span class="sxs-lookup"><span data-stu-id="60d02-103">Shipping information setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="60d02-104">See teema kirjeldab, kuidas seadistada saatmisteavet moodulis **Väljalaadimiskulu**.</span><span class="sxs-lookup"><span data-stu-id="60d02-104">This topic describes how to set up shipping information for the **Landed cost** module.</span></span>

## <a name="description-of-goods"></a><a name="description-of-goods"></a><span data-ttu-id="60d02-105">Kauba kirjeldus</span><span class="sxs-lookup"><span data-stu-id="60d02-105">Description of goods</span></span>

<span data-ttu-id="60d02-106">Kaubakirjeldused aitavad tuvastada kaupade teekonna, saatmiskonteineri või foolio ning selles sisalduvad kaubad.</span><span class="sxs-lookup"><span data-stu-id="60d02-106">Descriptions of goods help identify a voyage, shipping container, or folio of goods, and the goods in it.</span></span> <span data-ttu-id="60d02-107">Kaupade kirjelduse saate valida saatmiskonteineri päises või foolio päises.</span><span class="sxs-lookup"><span data-stu-id="60d02-107">You can select a description of goods on the shipping container header or the folio header.</span></span>

<span data-ttu-id="60d02-108">Kaubakirjeldustega töötamiseks avage **Väljalaadimiskulu \> Saatmisteabe seadistamine \> Kaupade kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="60d02-108">To work with descriptions of goods, go to **Landed cost \> Shipping information setup \> Description of goods**.</span></span> <span data-ttu-id="60d02-109">Seal saate vaadata, avada, luua ja kustutada kaubakirjelduste kirjeid.</span><span class="sxs-lookup"><span data-stu-id="60d02-109">There, you can view, open, create, and delete records for descriptions of goods.</span></span> <span data-ttu-id="60d02-110">Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.</span><span class="sxs-lookup"><span data-stu-id="60d02-110">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="60d02-111">Field</span><span class="sxs-lookup"><span data-stu-id="60d02-111">Field</span></span> | <span data-ttu-id="60d02-112">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="60d02-112">Description</span></span> |
|---|---|
| <span data-ttu-id="60d02-113">Kauba kirjeldus</span><span class="sxs-lookup"><span data-stu-id="60d02-113">Description of goods</span></span> | <span data-ttu-id="60d02-114">Sisestage seda kirjeldust kasutavate kaubatüübi ainu-ID nimi/number.</span><span class="sxs-lookup"><span data-stu-id="60d02-114">Enter a unique identification name/number for the type of goods that will use this description.</span></span> |
| <span data-ttu-id="60d02-115">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="60d02-115">Description</span></span> | <span data-ttu-id="60d02-116">Sisestage selle kategooria kaubatüübi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="60d02-116">Enter a description of the type of goods in this category.</span></span> |

## <a name="vessels"></a><a name="vessels"></a><span data-ttu-id="60d02-117">Laevad</span><span class="sxs-lookup"><span data-stu-id="60d02-117">Vessels</span></span>

<span data-ttu-id="60d02-118">Laev on saatmisettevõtte või agentuuri kasutatava laeva või aluse kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="60d02-118">A vessel is the unique name of a ship or vessel that a shipping company or agency uses.</span></span> <span data-ttu-id="60d02-119">Teekonna loomisel peate selle jaoks alati valima või sisestama laeva.</span><span class="sxs-lookup"><span data-stu-id="60d02-119">When you create a voyage, you must always either select or enter a vessel for it.</span></span> <span data-ttu-id="60d02-120">Kui kasutate sageli samu laevu, saate uue teekonna loomise kiirendamiseks ja hõlbustamiseks luua iga laeva jaoks laevakirje, mis võimaldab kasutajatel valida laeva loendist selle asemel, et sisestada selle nimi või number iga kord käsitsi.</span><span class="sxs-lookup"><span data-stu-id="60d02-120">If you often use the same vessels, then you can make it faster and easier to create a new voyage by creating a vessel record for each of them, thereby allowing users to select the vessel from a list rather then enter the name or number manually each time.</span></span>

<span data-ttu-id="60d02-121">Laevadega töötamiseks avage **Väljalaadimiskulu \> Saatmisteabe seadistamine \> Laevad**.</span><span class="sxs-lookup"><span data-stu-id="60d02-121">To work with vessels, go to **Landed cost \> Shipping information setup \> Vessels**.</span></span> <span data-ttu-id="60d02-122">Seal saate laevade kirjeid vaadata, avada, luua ja kustutada.</span><span class="sxs-lookup"><span data-stu-id="60d02-122">There, you can view, open, create, and delete records for vessels.</span></span> <span data-ttu-id="60d02-123">Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.</span><span class="sxs-lookup"><span data-stu-id="60d02-123">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="60d02-124">Field</span><span class="sxs-lookup"><span data-stu-id="60d02-124">Field</span></span> | <span data-ttu-id="60d02-125">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="60d02-125">Description</span></span> |
|---|---|
| <span data-ttu-id="60d02-126">Laev</span><span class="sxs-lookup"><span data-stu-id="60d02-126">Vessel</span></span> | <span data-ttu-id="60d02-127">Sisestage teekonnal kaupade transportimiseks kasutatava laeva ainu-ID nimi/number.</span><span class="sxs-lookup"><span data-stu-id="60d02-127">Enter a unique identification name/number for the ship that will be used to transport goods on a voyage.</span></span> |
| <span data-ttu-id="60d02-128">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="60d02-128">Description</span></span> | <span data-ttu-id="60d02-129">Sisestage laeva kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="60d02-129">Enter a description of the vessel.</span></span> <span data-ttu-id="60d02-130">Tavaliselt sisaldab kirjeldus laeva nime ja saatmisettevõtet/agenti.</span><span class="sxs-lookup"><span data-stu-id="60d02-130">Typically, this description identifies the name of the ship and the shipping company/agent.</span></span> |
| <span data-ttu-id="60d02-131">Tarneviis</span><span class="sxs-lookup"><span data-stu-id="60d02-131">Mode of delivery</span></span> | <span data-ttu-id="60d02-132">Valige aluse kasutatav tarneviis (nt _Õhk_, _Ookean_ või _Rong_).</span><span class="sxs-lookup"><span data-stu-id="60d02-132">Select the mode of delivery that the vessel uses (such as _Air_, _Ocean_, or _Train_).</span></span> |

## <a name="exporters"></a><span data-ttu-id="60d02-133">Eksportijad</span><span class="sxs-lookup"><span data-stu-id="60d02-133">Exporters</span></span>

<span data-ttu-id="60d02-134">Iga eksportijakirje tuvastab hankija või eksportija, kelle saab määrata teekonna hankijaks.</span><span class="sxs-lookup"><span data-stu-id="60d02-134">Each exporter record identifies a vendor or exporter that can be defined as the vendor for a voyage.</span></span> <span data-ttu-id="60d02-135">Eksportijat saab seostada teekonnaga ja kasutada aruandluseks.</span><span class="sxs-lookup"><span data-stu-id="60d02-135">The exporter can be associated with a voyage and used for reporting.</span></span>

<span data-ttu-id="60d02-136">Eksportijatega töötamiseks avage **Väljalaadimiskulu \> Saatmisteabe seadistamine \> Eksportijad**.</span><span class="sxs-lookup"><span data-stu-id="60d02-136">To work with exporters, go to **Landed cost \> Shipping information setup \> Exporters**.</span></span> <span data-ttu-id="60d02-137">Seal saate eksportijate kirjeid vaadata, avada, luua ja kustutada.</span><span class="sxs-lookup"><span data-stu-id="60d02-137">There, you can view, open, create, and delete records for exporters.</span></span> <span data-ttu-id="60d02-138">Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.</span><span class="sxs-lookup"><span data-stu-id="60d02-138">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="60d02-139">Field</span><span class="sxs-lookup"><span data-stu-id="60d02-139">Field</span></span> | <span data-ttu-id="60d02-140">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="60d02-140">Description</span></span> |
|---|---|
| <span data-ttu-id="60d02-141">Eksportija</span><span class="sxs-lookup"><span data-stu-id="60d02-141">Exporter</span></span> | <span data-ttu-id="60d02-142">Sisestage teekonnal transporditavate kaupade eksportija ainu-ID nimi/number.</span><span class="sxs-lookup"><span data-stu-id="60d02-142">Enter a unique identification name/number for the exporter of goods that are transported on a voyage.</span></span> |
| <span data-ttu-id="60d02-143">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="60d02-143">Description</span></span> | <span data-ttu-id="60d02-144">Sisestage eksportija kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="60d02-144">Enter a description of the exporter.</span></span> <span data-ttu-id="60d02-145">Tavaliselt sisaldab kirjeldus saatmisettevõtte/agendi täisnime.</span><span class="sxs-lookup"><span data-stu-id="60d02-145">Typically, this description identifies the full name of the shipping company/agent.</span></span> |

## <a name="commodity-codes"></a><span data-ttu-id="60d02-146">Kaubaartiklite koodid</span><span class="sxs-lookup"><span data-stu-id="60d02-146">Commodity codes</span></span>

<span data-ttu-id="60d02-147">Kaubaartiklite koode kasutatakse aitamaks tolliasutusel tuvastada teekonna kaupasid ja arvutada nende tollimaksumäärasid.</span><span class="sxs-lookup"><span data-stu-id="60d02-147">You use commodity codes to help with customs identification and the calculation of duty rates for goods on a voyage.</span></span> <span data-ttu-id="60d02-148">Kaubaartiklite koodid saate valida lehel **Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="60d02-148">You can select commodity codes on the **Released products** page.</span></span>

<span data-ttu-id="60d02-149">Kaubaartiklite koodidega töötamiseks avage **Väljalaadimiskulu \> Saatmisteabe seadistamine \> Kaubaartiklite koodid**.</span><span class="sxs-lookup"><span data-stu-id="60d02-149">To work with commodity codes, go to **Landed cost \> Shipping information setup \> Commodity codes**.</span></span> <span data-ttu-id="60d02-150">Seal saate kaubaartiklite koodide kirjeid vaadata, avada, luua ja kustutada.</span><span class="sxs-lookup"><span data-stu-id="60d02-150">There, you can view, open, create, and delete records for commodity codes.</span></span> <span data-ttu-id="60d02-151">Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.</span><span class="sxs-lookup"><span data-stu-id="60d02-151">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="60d02-152">Field</span><span class="sxs-lookup"><span data-stu-id="60d02-152">Field</span></span> | <span data-ttu-id="60d02-153">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="60d02-153">Description</span></span> |
|---|---|
| <span data-ttu-id="60d02-154">Kaubaartikkel</span><span class="sxs-lookup"><span data-stu-id="60d02-154">Commodity code</span></span> | <span data-ttu-id="60d02-155">Sisestage seda tüüpi kaubaartikli kordumatu kood.</span><span class="sxs-lookup"><span data-stu-id="60d02-155">Enter a unique code for this type of commodity.</span></span> |
| <span data-ttu-id="60d02-156">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="60d02-156">Description</span></span> | <span data-ttu-id="60d02-157">Sisestage kaubaartiklitüübi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="60d02-157">Enter a description of the commodity type.</span></span> |

## <a name="customs-description"></a><span data-ttu-id="60d02-158">Tolli kirjeldus</span><span class="sxs-lookup"><span data-stu-id="60d02-158">Customs description</span></span>

<span data-ttu-id="60d02-159">Tolli kirjeldused aitavad kaupu tuvastada tolliga seotud eesmärkidel.</span><span class="sxs-lookup"><span data-stu-id="60d02-159">Customs descriptions help identify goods for customs purposes.</span></span> <span data-ttu-id="60d02-160">Tolli kirjelduse saate valida lehel **Väljastatud tooted** või ostutellimuse ridadel.</span><span class="sxs-lookup"><span data-stu-id="60d02-160">You can select a customs description on the **Released products** page or on purchase order lines.</span></span>

<span data-ttu-id="60d02-161">Tolli kirjeldustega töötamiseks avage **Väljalaadimiskulu \> Saatmisteabe seadistamine \> Tolli kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="60d02-161">To work with customs descriptions, go to **Landed cost \> Shipping information setup \> Customs description**.</span></span> <span data-ttu-id="60d02-162">Seal saate vaadata, avada, luua ja kustutada tolli kirjelduste kirjeid.</span><span class="sxs-lookup"><span data-stu-id="60d02-162">There, you can view, open, create, and delete records for custom descriptions.</span></span> <span data-ttu-id="60d02-163">Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.</span><span class="sxs-lookup"><span data-stu-id="60d02-163">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="60d02-164">Field</span><span class="sxs-lookup"><span data-stu-id="60d02-164">Field</span></span> | <span data-ttu-id="60d02-165">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="60d02-165">Description</span></span> |
|---|---|
| <span data-ttu-id="60d02-166">Tolli kirjeldus</span><span class="sxs-lookup"><span data-stu-id="60d02-166">Customs description</span></span> | <span data-ttu-id="60d02-167">Sisestage seda tüüpi tolliklassifikatsiooni kordumatu kood.</span><span class="sxs-lookup"><span data-stu-id="60d02-167">Enter a unique code for this type of customs classification.</span></span> <span data-ttu-id="60d02-168">Sageli on see kood ametlik kirjeldus, mille tolliasutus on esitanud kaupade kirjelduse ja kvalitatiivse väärtuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="60d02-168">Often, this code will be the official description that is provided by a customs authority for the description and qualitative value of the goods.</span></span> |
| <span data-ttu-id="60d02-169">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="60d02-169">Description</span></span> | <span data-ttu-id="60d02-170">Sisestage tolliklassifikatsiooni kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="60d02-170">Enter a description of the customs classification.</span></span> |
