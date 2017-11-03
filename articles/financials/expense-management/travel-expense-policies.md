---
title: "Kulupoliitikate määratlemine"
description: "Saate määratleda kulupoliitikaid, mida teie töötajad peavad järgima, kui nad sisestavad ja esitavad kuluaruandeid ja reisiplaane rakenduses Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: saraschi2
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9a5ce1a3b6519b510c9f5aa5618ab91f77a2d91a
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="expense-policies"></a><span data-ttu-id="5cecf-103">Kulude poliitikad</span><span class="sxs-lookup"><span data-stu-id="5cecf-103">Expense policies</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5cecf-104">Saate määratleda põhimõtted, mida teie töötajad peavad järgima, kui nad kuluaruandeid ja reisiplaane sisestavad ning edastavad.</span><span class="sxs-lookup"><span data-stu-id="5cecf-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span> <span data-ttu-id="5cecf-105">Kulupõhimõtete rakendamine võib aidata teil kulusid tõhusamalt hallata.</span><span class="sxs-lookup"><span data-stu-id="5cecf-105">Implementing expense policies can help you manage expenses effectively.</span></span> 

<span data-ttu-id="5cecf-106">Näiteks võite kehtestada New Yorgi hotellikulude kohta põhimõtte, et ühe öö maksumus hotellis ei tohi ületada 250 USA dollarit.</span><span class="sxs-lookup"><span data-stu-id="5cecf-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span> <span data-ttu-id="5cecf-107">Kui töötaja edastab kuluaruande või reisiplaani, milles toa maksumus ületab selle summa, teatab süsteem töötajale, et kulupoliitikas ettenähtud summat on ületatud.</span><span class="sxs-lookup"><span data-stu-id="5cecf-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="5cecf-108">Poliitika määratlemisel saate konfigureerida teadet, mille töötaja saab.</span><span class="sxs-lookup"><span data-stu-id="5cecf-108">You can configure the message that the worker will receive when you define the policy.</span></span> 

<span data-ttu-id="5cecf-109">Määratleda saab kolme tüüpi poliitikaid.</span><span class="sxs-lookup"><span data-stu-id="5cecf-109">You can define three types of policies:</span></span> 

 - <span data-ttu-id="5cecf-110">Hoiatus – lubab töötajal kuluaruande või reisiplaani esitada, kuid kulu märgitakse kõigile kinnitajatele ja</span><span class="sxs-lookup"><span data-stu-id="5cecf-110">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>  
 <span data-ttu-id="5cecf-111">hilisemaks aruandluseks.</span><span class="sxs-lookup"><span data-stu-id="5cecf-111">for later reporting.</span></span> 
 - <span data-ttu-id="5cecf-112">Tõrge – nõuab töötajalt, et ta enne kuluaruande või reisiplaani esitamist kulu üle vaataks, nii et see vastaks poliitikale.</span><span class="sxs-lookup"><span data-stu-id="5cecf-112">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span> 
 - <span data-ttu-id="5cecf-113">Põhjendus – nõuab, et töötaja või juht sisestaks enne kuluaruande või reisiplaani esitamist põhjenduse poliitika summa ületamise kohta.</span><span class="sxs-lookup"><span data-stu-id="5cecf-113">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span> 

<span data-ttu-id="5cecf-114">Seadistada saab ka kuupäevavahemiku, mille puhul kulupoliitikad kehtivad.</span><span class="sxs-lookup"><span data-stu-id="5cecf-114">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="5cecf-115">Näiteks lennupiletite hind Taani ja New York City vahel võib reisihooajal kõrge olla.</span><span class="sxs-lookup"><span data-stu-id="5cecf-115">For example, airline fares for flights between Denmark and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="5cecf-116">Saate määratleda lennupiletite kulureegli, mis seab New York City lendude hinnapiiriks 5000 taani krooni, ja võite täpsustada, et see reegel kehtib ajavahemikul 15. märtsist kuni 15. septembrini.</span><span class="sxs-lookup"><span data-stu-id="5cecf-116">You can define a flight expense rule that restricts the cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and September 15.</span></span> 

