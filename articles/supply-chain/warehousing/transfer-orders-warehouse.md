---
title: Ladude seadistamine üleviimistellimuste jaoks
description: Selles teemas kirjeldatakse ladude seadistamist üleviimistellimuste jaoks.
author: Mirzaab
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 91db6e8f921bd674211f6d478b6d0f0a832c983c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847011"
---
# <a name="set-up-warehouses-for-transfer-orders"></a><span data-ttu-id="699ed-103">Ladude seadistamine üleviimistellimuste jaoks</span><span class="sxs-lookup"><span data-stu-id="699ed-103">Set up warehouses for transfer orders</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="699ed-104">Ladudevahelisi üleviimistellimusi toetava hierarhia loomiseks saate kasutada laotasemeid.</span><span class="sxs-lookup"><span data-stu-id="699ed-104">You can use warehouse levels to create a hierarchy that supports transfer orders between warehouses.</span></span> <span data-ttu-id="699ed-105">Tuginedes sellele sättele, arvutab koondplaneerimine välja iga laotaseme kaubavajadused ning loob määratud lähtelaole plaanitud tellimusi nende täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="699ed-105">Based on this setup, master scheduling calculates item requirements at the individual warehouse level and generates planned transfer orders from an assigned source warehouse to fulfill them.</span></span>

1.  <span data-ttu-id="699ed-106">Klõpsake valikuid **Varude haldus > Seadistus > Laovarude jaotamine > Laod**.</span><span class="sxs-lookup"><span data-stu-id="699ed-106">Click **Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>

2.  <span data-ttu-id="699ed-107">Valige ladu, mille soovite uuesti täita.</span><span class="sxs-lookup"><span data-stu-id="699ed-107">Select the warehouse that you want to refill.</span></span>

3.  <span data-ttu-id="699ed-108">Märkige kiirkaardil **Koondplaneerimine** ruut **Taastäitmine**.</span><span class="sxs-lookup"><span data-stu-id="699ed-108">On the **Master planning** FastTab, select the **Refilling** check box.</span></span>

4.  <span data-ttu-id="699ed-109">Valige väljal **Pealadu** ladu, mille soovite määrata taastäitmislaoks.</span><span class="sxs-lookup"><span data-stu-id="699ed-109">In the **Main warehouse** field, select the warehouse that you want to assign as the refilling warehouse.</span></span> <span data-ttu-id="699ed-110">Koondplaneerimine arvutab välja valitud lao üleviimisvajadused ja loob väljal **Pealadu** valitud pealaole plaanitud üleviimistellimuse.</span><span class="sxs-lookup"><span data-stu-id="699ed-110">Master scheduling calculates a transfer requirement for the selected warehouse and generates a planned transfer order from the assigned **Main warehouse**.</span></span>
   
    > [!NOTE]
    > <P><span data-ttu-id="699ed-111">Kui jätate ruudu <STRONG>Taastäitmine</STRONG> tühjaks, määratakse valitud laole laotase vastavalt väärtusele <STRONG>Pealadu</STRONG>, kuid <STRONG>Pealadu</STRONG> ei seadistata taastäitmislaona.</span><span class="sxs-lookup"><span data-stu-id="699ed-111">If you clear the <STRONG>Refilling</STRONG> check box, the selected warehouse is assigned a warehouse level in regard to the <STRONG>Main warehouse</STRONG>, but the <STRONG>Main warehouse</STRONG> is not set up as a refilling warehouse.</span></span></P>

5.  <span data-ttu-id="699ed-112">Uue seadistuse rakendamiseks sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="699ed-112">Close the page to apply the new setup.</span></span>


> [!TIP]
> <P><span data-ttu-id="699ed-113">Kui soovite määrata taastäitmiseks lao, peate lao lehel <STRONG>Varude dimensioonid seadistama</STRONG> varude dimensioonina.</span><span class="sxs-lookup"><span data-stu-id="699ed-113">If you want to assign a warehouse for refilling, you must first set up the warehouse as a storage dimension on the <STRONG>Storage dimension groups</STRONG> page.</span></span> <span data-ttu-id="699ed-114">Sellel lehel valige lao puhul väli <STRONG>Aktiivne</STRONG> ja väli <STRONG>Laovarude planeerimine dimensioonide kaupa</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="699ed-114">On this page, select the <STRONG>Active</STRONG> field and the <STRONG>Coverage plan by dimension</STRONG> field for the warehouse.</span></span></P>

## <a name="set-up-transport-lead-time"></a><span data-ttu-id="699ed-115">Transpordi täitmisaja seadistamine</span><span class="sxs-lookup"><span data-stu-id="699ed-115">Set up transport lead time</span></span>

<span data-ttu-id="699ed-116">Peate ka seadistama transpordi täitmisaja ladude vahel lehel **Transpordipäevad**.</span><span class="sxs-lookup"><span data-stu-id="699ed-116">You must also set up the transport lead time between the warehouses on the **Transport days** page.</span></span> 
1. <span data-ttu-id="699ed-117">Minge jaotisse **Varude haldus > Seadistus > Jaotus > Transpordipäevad**.</span><span class="sxs-lookup"><span data-stu-id="699ed-117">Go to **Inventory management > Setup > Distribution > Transport days**.</span></span>
2. <span data-ttu-id="699ed-118">Valige väljal **Vastuvõtupunkt** säte **ladu**.</span><span class="sxs-lookup"><span data-stu-id="699ed-118">In the **Receiving point** field, select **warehouse**.</span></span>
3. <span data-ttu-id="699ed-119">Valige **Lähetav ladu**, **Vastuvõttev ladu** ja **Transpordi päevas**.</span><span class="sxs-lookup"><span data-stu-id="699ed-119">Select the **Shipping warehouse**, **Receiving warehouse**, and **Transport days**.</span></span> 
4. <span data-ttu-id="699ed-120">(Valikuline) Saate määrata ka tarneviisist oleneva transpordiaja vahekaardil **Transpordipäevi tarneviisi kohta**.</span><span class="sxs-lookup"><span data-stu-id="699ed-120">(Optional) You can also set transport time, depending on the mode of delivery, under the **Transport days per mode of delivery** tab.</span></span>
