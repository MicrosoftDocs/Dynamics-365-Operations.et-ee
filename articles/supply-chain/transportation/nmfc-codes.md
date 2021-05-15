---
title: Riikliku autoveose klassifikatsiooni (NMFC) koodid
description: See teema kirjeldab, kuidas töötada Riikliku autoveose klassifikatsiooni (NMFC) koodidega Microsoftis Dynamics 365 Supply Chain Management
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0307437d3868f7ac34fa16a0913907a046ac14d4
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941878"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a><span data-ttu-id="a3eb9-103">Riikliku autoveose klassifikatsiooni (NMFC) koodid</span><span class="sxs-lookup"><span data-stu-id="a3eb9-103">National Motor Freight Classification (NMFC) codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3eb9-104">Riikliku autoveose klassifikatsiooni (NMFC) koodid aitavad klassifitseerida saadetavaid kaupu.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-104">National Motor Freight Classification (NMFC) codes help you classify items that can be shipped.</span></span> <span data-ttu-id="a3eb9-105">NMFC-kood on tähistus, mida kasutatakse kaupade grupeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-105">The NMFC code is a designation that is used to group commodities.</span></span> <span data-ttu-id="a3eb9-106">See võimaldab transpordiettevõtetel hinnata kaupade saatmist, klassifitseerides kaubad, võttes aluseks sellised kaalutlused nagu veoki sobivus, laadimise probleemid, käsitsemisprobleemid ja lähetuse läbimine.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-106">It enables transport companies to evaluate goods for shipment by classifying items based on considerations such as truck fit, loading issues, handling issues, and perishability.</span></span> <span data-ttu-id="a3eb9-107">Kaubad grupeeritakse ühte 18 veose klassist, kasutades numbreid vahemikus 50 kuni 500.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-107">Commodities are grouped into one of 18 freight classes by using a range of numbers from 50 to 500.</span></span> <span data-ttu-id="a3eb9-108">Klass, mille alla kaup grupeeritakse, põhineb nelja transpordiomaduse (tihedus, tihedus, koormus, käsitsemine ja kohustus) hindamisel.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-108">The class that a commodity is grouped into is based on an evaluation of four transportation characteristics: density, stowability, handling, and liability.</span></span> <span data-ttu-id="a3eb9-109">Koos määravad need omadused kauba transporditavuse.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-109">Together, these characteristics establish the commodity's transportability.</span></span>

<span data-ttu-id="a3eb9-110">NMFC-kood on seotud iga alla laadurikoormuse (LTL) saatmiskaubaga.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-110">An NMFC code is associated with every less than truckload (LTL) shipping item.</span></span> <span data-ttu-id="a3eb9-111">Näiteks võib sülearvutile määrata NMFC, mis on klassist 2.5, samas kui elektriseadmetele võidakse määrata NMFC, mis on klassist 65.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-111">For example, a laptop might be assigned an NMFC that is classed at 2.5, whereas electrical cords might be assigned an NMFC that is classed at 65.</span></span>

<span data-ttu-id="a3eb9-112">See funktsioon aitab töötajatel kasutada NMFC-koode LTL-i saadetise kaupade klassifitseerimiseks.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-112">This feature can help workers use NMFC codes to classify LTL shipping items.</span></span> <span data-ttu-id="a3eb9-113">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-113">Here are some examples:</span></span>

- <span data-ttu-id="a3eb9-114">Kui teie ettevõte lisab veose kirjelduste veokirjale (BOL), on vedajal aimu sellest, mida veos sisaldab.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-114">If your company includes a freight description on the bill of lading (BOL), the carrier will have some idea what the freight is.</span></span> <span data-ttu-id="a3eb9-115">Veos on oluline klassifikatsioon, kuna paljud transpordiettevõtted tuginevad oma ärimudeli tervenisti veose tüüpidele, mida nad tarnivad.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-115">Freight is an important classification because many transportation companies base their whole business model on the types of freight that they ship.</span></span>
- <span data-ttu-id="a3eb9-116">See klassifikatsioon võib olla teie ettevõttele oluline, kuna seda kasutatakse antud koormuse kulu määramiseks.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-116">This classification might be essential to your company because it's used to determine the cost of a given load.</span></span>
- <span data-ttu-id="a3eb9-117">Teie ettevõte saab tuvastada LTL-logistika ja transpordiettevõtte tulunäitaja.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-117">Your company can identify the profitability of an LTL logistics and transportation company.</span></span>

<span data-ttu-id="a3eb9-118">Selles teemas kirjeldatakse, kuidas töötada NMFC-koodidega rakenduses Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-118">This topic describes how to work with NMFC codes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a3eb9-119">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="a3eb9-119">Prerequisites</span></span>

<span data-ttu-id="a3eb9-120">Enne NMFC-koodide loomiseks peate häälestama kõik LTL-veoklassid, mis tuleb nendega vastendada.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-120">Before you can create NMFC codes, you must set up all the LTL freight classes that must be mapped to them.</span></span> <span data-ttu-id="a3eb9-121">LTL-veoseklassid esindavad kaupade kategooriaid, samas kui NMFC-koodid on seotud kindlate kaupadega igasühes 18 veose klassist.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-121">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span> <span data-ttu-id="a3eb9-122">Lisateavet selle kohta, kuidas LTL-klassidega töötada, vt jaotist [Klassid alla veokikoormuse (LTL)](ltl-class.md).</span><span class="sxs-lookup"><span data-stu-id="a3eb9-122">For more information about how to work with LTL classes, see [Less than truckload (LTL) classes](ltl-class.md).</span></span>

## <a name="create-an-nmfc-code"></a><span data-ttu-id="a3eb9-123">NMFC-koodi loomine</span><span class="sxs-lookup"><span data-stu-id="a3eb9-123">Create an NMFC code</span></span>

<span data-ttu-id="a3eb9-124">NMFC-koodi loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-124">To create an NMFC code, follow these steps.</span></span>

1. <span data-ttu-id="a3eb9-125">Järgige üht neist sammudest.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-125">Follow one of these steps:</span></span>

    - <span data-ttu-id="a3eb9-126">Minge jaotisse **Laohaldus \> Seadistus \> Inventar \> NMFC-koodid**.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-126">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
    - <span data-ttu-id="a3eb9-127">Avage **Transpordihaldus \> Seadistused \> Transpordistandardid \> NMFC-koodid**.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-127">Go to **Transportation management \> Setup \> Transportation standards \> NMFC codes**.</span></span>

1. <span data-ttu-id="a3eb9-128">Valige NMFC-koodi loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-128">Select **New** to create an NMFC code.</span></span> <span data-ttu-id="a3eb9-129">Seejärel määrake järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-129">Then set the following fields:</span></span>

    - <span data-ttu-id="a3eb9-130">**NMFC kood** – sisestage kauba tüübi kohta NMFC kood.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-130">**NMFC code** – Enter the NMFC code for the commodity type.</span></span>
    - <span data-ttu-id="a3eb9-131">**Nimi** – sisestage NMFC-koodi nimi.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-131">**Name** – Enter a name for the NMFC code.</span></span>
    - <span data-ttu-id="a3eb9-132">**LTL-klass** – valige NMFC-koodiga seostatud LTL-klass.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-132">**LTL class** – Select the LTL class that is associated with the NMFC code.</span></span>
    - <span data-ttu-id="a3eb9-133">**Veose käsitsemise ühik** – määratlege saadetise vaikimisi käsitsemistüüp.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-133">**BOL handling unit** – Define the default handling type for the shipment.</span></span>

## <a name="example-set-up-nmfc-codes"></a><span data-ttu-id="a3eb9-134">Näide: NMFC-koodide häälestamine</span><span class="sxs-lookup"><span data-stu-id="a3eb9-134">Example: Set up NMFC codes</span></span>

<span data-ttu-id="a3eb9-135">Järgmine näide näitab, kuidas seadistada kahte erinevat NMFC-koodi, mida saab kasutada erinevat tüüpi toodetega.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-135">The following example shows how to set up two different NMFC codes that can be used with different products.</span></span>

1. <span data-ttu-id="a3eb9-136">Minge jaotisse **Laohaldus \> Seadistus \> Inventar \> NMFC-koodid**.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-136">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
1. <span data-ttu-id="a3eb9-137">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-137">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a3eb9-138">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-138">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a3eb9-139">**NMFC kood:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="a3eb9-139">**NMFC code:** *92.5*</span></span>
    - <span data-ttu-id="a3eb9-140">**Nimi:** *Arvutid*</span><span class="sxs-lookup"><span data-stu-id="a3eb9-140">**Name:** *Computers*</span></span>
    - <span data-ttu-id="a3eb9-141">**LTL klass:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="a3eb9-141">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="a3eb9-142">**Kauba käsitsemise ühik:** *ühik*</span><span class="sxs-lookup"><span data-stu-id="a3eb9-142">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="a3eb9-143">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-143">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="a3eb9-144">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-144">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a3eb9-145">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-145">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a3eb9-146">**NMFC kood:** *125*</span><span class="sxs-lookup"><span data-stu-id="a3eb9-146">**NMFC code:** *125*</span></span>
    - <span data-ttu-id="a3eb9-147">**Nimi:** *telefonid*</span><span class="sxs-lookup"><span data-stu-id="a3eb9-147">**Name:** *Phones*</span></span>
    - <span data-ttu-id="a3eb9-148">**LTL klass:** *125*</span><span class="sxs-lookup"><span data-stu-id="a3eb9-148">**LTL class:** *125*</span></span>
    - <span data-ttu-id="a3eb9-149">**Kauba käsitsemise ühik:** *ühik*</span><span class="sxs-lookup"><span data-stu-id="a3eb9-149">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="a3eb9-150">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="a3eb9-150">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a3eb9-151">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a3eb9-151">Additional resources</span></span>

- [<span data-ttu-id="a3eb9-152">Klassid "Vähem kui koormatäis" (LTL)</span><span class="sxs-lookup"><span data-stu-id="a3eb9-152">Less than truckload (LTL) classes</span></span>](ltl-class.md)
- [<span data-ttu-id="a3eb9-153">Veokirja loomine</span><span class="sxs-lookup"><span data-stu-id="a3eb9-153">Create a bill of landing</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
