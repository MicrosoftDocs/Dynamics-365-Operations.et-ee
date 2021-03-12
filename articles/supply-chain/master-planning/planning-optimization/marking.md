---
title: Varude märkimine planeerimise optimeerimisega
description: See teema annab teavet valikute kohta, mis on saadaval varude märkimiseks, kui kasutate planeerimise optimeerimist.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 236e1955dd80564e748aab1c595b017cb78e9418
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983487"
---
# <a name="inventory-marking-with-planning-optimization"></a><span data-ttu-id="59cb1-103">Varude märkimine planeerimise optimeerimisega</span><span class="sxs-lookup"><span data-stu-id="59cb1-103">Inventory marking with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="59cb1-104">See teema annab teavet valikute kohta, mis on saadaval varude märkimiseks, kui kasutate planeerimise optimeerimist.</span><span class="sxs-lookup"><span data-stu-id="59cb1-104">This topic provides information about the options that are available for marking inventory in firmed orders when you use Planning Optimization.</span></span>

<span data-ttu-id="59cb1-105">*Märkimist* kasutatakse pakkumise ja nõudluse linkimiseks.</span><span class="sxs-lookup"><span data-stu-id="59cb1-105">*Marking* is used to link supply and demand.</span></span> <span data-ttu-id="59cb1-106">See meenutab *sidumist*, mis näitab, kuidas koondplaneerimise abil soovitakse nõudlusele vastata.</span><span class="sxs-lookup"><span data-stu-id="59cb1-106">It resembles *pegging*, which indicates how master planning expects to cover demand.</span></span> <span data-ttu-id="59cb1-107">Planeerimise vaatepunktist on peamiseks erinevuseks see, et märgistus on sidumisest püsivam.</span><span class="sxs-lookup"><span data-stu-id="59cb1-107">From a planning point of view, the main difference is that marking is more permanent than pegging.</span></span>

<span data-ttu-id="59cb1-108">Märgistus võeti kasutusele, et toetada spetsiaalseid kuluarvestuse stsenaariume FIFO-laomudeli (esimesena sisse, esimesena välja) ja LIFO-laomudeli (viimasena sisse, esimesena välja) korral.</span><span class="sxs-lookup"><span data-stu-id="59cb1-108">Marking was introduced to support special costing scenarios for first in, first out (FIFO) and last in, first out (LIFO).</span></span> <span data-ttu-id="59cb1-109">Kuid seda kasutatakse nüüd ka mõne mittekulupõhise stsenaariumi puhul.</span><span class="sxs-lookup"><span data-stu-id="59cb1-109">However, it's now also used for some non-costing scenarios.</span></span> <span data-ttu-id="59cb1-110">Pakkumise ja nõudluse vaheline märgistus on valikuline ja peaaegu püsiv.</span><span class="sxs-lookup"><span data-stu-id="59cb1-110">Marking between supply and demand is optional and almost permanent.</span></span> <span data-ttu-id="59cb1-111">Kasutaja saab märgistuse eemaldada käsitsi või kasutades müügitellimusrea jaotamist, kus on valitud suvand **Eemalda märgistus**.</span><span class="sxs-lookup"><span data-stu-id="59cb1-111">Marking can be removed manually by a user, or it can be removed by running a sales order line explosion where the **Remove marking** option is selected.</span></span>

<span data-ttu-id="59cb1-112">Sidumist juhitakse laovarude planeerimise ajal koondplaneerimise käigus, et siduda nõudlus vajaliku pakkumisega.</span><span class="sxs-lookup"><span data-stu-id="59cb1-112">Pegging is controlled by master planning during coverage to link demand with the required supply.</span></span> <span data-ttu-id="59cb1-113">Sidumist saab uuendada igaks planeerimiseks, et optimeerida pakkumist, mis on vajalik nõudluse katmiseks.</span><span class="sxs-lookup"><span data-stu-id="59cb1-113">Pegging can be updated for each planning run to optimize the supply that is required to cover demand.</span></span> <span data-ttu-id="59cb1-114">Kui koondplaneerimisel värskendatakse sidumiseteavet, arvestatakse olemasoleva märgistusega.</span><span class="sxs-lookup"><span data-stu-id="59cb1-114">When master planning updates pegging information, it respects any existing marking.</span></span>

<span data-ttu-id="59cb1-115">Sidumist alustatakse vastava märgistuse, vabade reserveeringute ja tellimuse reserveeringute kaasamisega järgmises järjestuses.</span><span class="sxs-lookup"><span data-stu-id="59cb1-115">Pegging starts by including relevant marking, on-hand reservations, and on-order reservations, in the following sequence:</span></span>

1. <span data-ttu-id="59cb1-116">Nõudluse ja tarnimise vaheline märgistus</span><span class="sxs-lookup"><span data-stu-id="59cb1-116">Marking between demand and supply</span></span>
1. <span data-ttu-id="59cb1-117">Vabad reserveeringud</span><span class="sxs-lookup"><span data-stu-id="59cb1-117">On-hand reservations</span></span>
1. <span data-ttu-id="59cb1-118">Tellimuse reserveeringud</span><span class="sxs-lookup"><span data-stu-id="59cb1-118">On-order reservations</span></span>

<span data-ttu-id="59cb1-119">Kui kinnitate plaanitud tellimust, pakutakse dialoogiboksis **Kinnitamine** välja **Märkimise värskendamine**, mida saate kasutada kinnitamise ajal loodud tellimuste märkimissuvandite määramiseks.</span><span class="sxs-lookup"><span data-stu-id="59cb1-119">When you firm a planned order, the **Firming** dialog box provides an **Update marking** field that you use to set marking options for the orders that are created during firming.</span></span> <span data-ttu-id="59cb1-120">Valige üks järgmistest väärtustest.</span><span class="sxs-lookup"><span data-stu-id="59cb1-120">Select one of the following values:</span></span>

- <span data-ttu-id="59cb1-121">**Ei** – varude märkimist ei rakendata.</span><span class="sxs-lookup"><span data-stu-id="59cb1-121">**No** – No inventory marking is applied.</span></span>
- <span data-ttu-id="59cb1-122">**Tavaline** – varude märkimine värskendatakse sidumise alusel.</span><span class="sxs-lookup"><span data-stu-id="59cb1-122">**Standard** – Inventory marking is updated according to the pegging.</span></span> <span data-ttu-id="59cb1-123">Vajaduse tellimus (nõudlus) märgitakse täitmise tellimusega (pakkumisega) võrreldes.</span><span class="sxs-lookup"><span data-stu-id="59cb1-123">A requirement order (demand) is marked against a fulfillment order (supply).</span></span> <span data-ttu-id="59cb1-124">Kui täitmise tellimusele jääb mõni kogus alles, siis seda ei märgita ja viideteteavet ei lisata.</span><span class="sxs-lookup"><span data-stu-id="59cb1-124">If some quantity remains on the fulfillment order, it isn't marked, and the reference information is left blank.</span></span> <span data-ttu-id="59cb1-125">Näiteks kui müügitellimus (100 ea) on seotud ostutellimusega (150 ea), määratakse viiteteave ainult müügitellimusele.</span><span class="sxs-lookup"><span data-stu-id="59cb1-125">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned only to the sales order.</span></span>
- <span data-ttu-id="59cb1-126">**Laiendatud** – märgitakse nii vajaduse (nõudluse) kui täitmise (pakkumise) tellimused, sõltumata sellest, kas täitmise tellimusele jääb teatud kaubakogus või mitte.</span><span class="sxs-lookup"><span data-stu-id="59cb1-126">**Extended** – Both the requirement order (demand) and the fulfillment order (supply) are marked, regardless of any quantity that remains on the fulfillment order.</span></span> <span data-ttu-id="59cb1-127">Näiteks kui müügitellimus (100 ea) on seotud ostutellimusega (150 ea), määratakse viiteteave nii müügi- kui ka ostutellimusele.</span><span class="sxs-lookup"><span data-stu-id="59cb1-127">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned to both the sales order and the purchase order.</span></span>
