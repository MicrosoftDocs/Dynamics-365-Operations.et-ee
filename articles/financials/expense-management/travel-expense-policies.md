---
title: "Kulupoliitikate määratlemine"
description: "Saate määratleda kulupoliitikaid, mida teie töötajad peavad järgima, kui nad sisestavad ja esitavad kuluaruandeid ja reisiplaane rakenduses Microsoft Dynamics 365 for Finance and Operations."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 062d6f01bb07324ad5b8dc6b9fd7617756502c17
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="expense-policies"></a><span data-ttu-id="10b55-103">Kulude poliitikad</span><span class="sxs-lookup"><span data-stu-id="10b55-103">Expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10b55-104">Saate määratleda põhimõtted, mida teie töötajad peavad järgima, kui nad kuluaruandeid ja reisiplaane sisestavad ning edastavad.</span><span class="sxs-lookup"><span data-stu-id="10b55-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="10b55-105">Kulupõhimõtete rakendamine võib aidata teil kulusid tõhusamalt hallata.</span><span class="sxs-lookup"><span data-stu-id="10b55-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="10b55-106">Näiteks võite kehtestada New Yorgi hotellikulude kohta põhimõtte, et ühe öö maksumus hotellis ei tohi ületada 250 USA dollarit.</span><span class="sxs-lookup"><span data-stu-id="10b55-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="10b55-107">Kui töötaja esitab kuluaruande või reisiplaani, milles toa maksumus ületab selle summa, teatab süsteem</span><span class="sxs-lookup"><span data-stu-id="10b55-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="10b55-108">töötajale, et kulupoliitikas ettenähtud summat on ületatud.</span><span class="sxs-lookup"><span data-stu-id="10b55-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="10b55-109">Poliitika määratlemisel saate konfigureerida teadet,</span><span class="sxs-lookup"><span data-stu-id="10b55-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="10b55-110">mille töötaja saab.</span><span class="sxs-lookup"><span data-stu-id="10b55-110">define the policy.</span></span>      
        
<span data-ttu-id="10b55-111">Määratleda saab kolme tüüpi poliitikaid.</span><span class="sxs-lookup"><span data-stu-id="10b55-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="10b55-112">Hoiatus – lubab töötajal kuluaruande või reisiplaani esitada, kuid kulu märgitakse kõigile kinnitajatele ja</span><span class="sxs-lookup"><span data-stu-id="10b55-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="10b55-113">hilisemaks aruandluseks.</span><span class="sxs-lookup"><span data-stu-id="10b55-113">for later reporting.</span></span>        

- <span data-ttu-id="10b55-114">Tõrge – nõuab töötajalt, et ta enne kuluaruande või reisiplaani esitamist kulu üle vaataks, nii et see vastaks poliitikale.</span><span class="sxs-lookup"><span data-stu-id="10b55-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
  - <span data-ttu-id="10b55-115">Põhjendus – nõuab, et töötaja või juht sisestaks enne kuluaruande või reisiplaani esitamist põhjenduse poliitika summa ületamise kohta.</span><span class="sxs-lookup"><span data-stu-id="10b55-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        
 
  <span data-ttu-id="10b55-116">Seadistada saab ka kuupäevavahemiku, mille puhul kulupoliitikad kehtivad.</span><span class="sxs-lookup"><span data-stu-id="10b55-116">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="10b55-117">Näiteks võivad lennukipiletite hinnad Taani</span><span class="sxs-lookup"><span data-stu-id="10b55-117">For example, airline fares for flights between Denmark</span></span>      
  <span data-ttu-id="10b55-118">ja New York City vahel reisihooajal kõrged olla.</span><span class="sxs-lookup"><span data-stu-id="10b55-118">and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="10b55-119">Saate määratleda lennupiletite kulureegli, mis seab</span><span class="sxs-lookup"><span data-stu-id="10b55-119">You can define a flight expense rule that restricts the</span></span>      
  <span data-ttu-id="10b55-120">New York City lendude hinnapiiriks 5000 taani krooni, ja võite täpsustada, et see reegel kehtib ajavahemikul 15. märtsist kuni</span><span class="sxs-lookup"><span data-stu-id="10b55-120">cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and</span></span>      
  <span data-ttu-id="10b55-121">15. septembrini.</span><span class="sxs-lookup"><span data-stu-id="10b55-121">September 15.</span></span>

