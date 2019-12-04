---
title: Kulupoliitikate määratlemine
description: Saate määratleda kulupoliitikad, mida teie töötajad peavad järgima, kui nad rakenduses Microsoft Dynamics 365 Finance kuluaruandeid ja reisiplaane sisestavad ning edastavad.
author: ryansandness
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7d3b4a8f6cf74bb1fe7e53a4dfdd607f604e16e3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187448"
---
# <a name="define-expense-policies"></a><span data-ttu-id="5c1b8-103">Kulupoliitikate määratlemine</span><span class="sxs-lookup"><span data-stu-id="5c1b8-103">Define expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c1b8-104">Saate määratleda põhimõtted, mida teie töötajad peavad järgima, kui nad kuluaruandeid ja reisiplaane sisestavad ning edastavad.</span><span class="sxs-lookup"><span data-stu-id="5c1b8-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="5c1b8-105">Kulupõhimõtete rakendamine võib aidata teil kulusid tõhusamalt hallata.</span><span class="sxs-lookup"><span data-stu-id="5c1b8-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="5c1b8-106">Näiteks võite kehtestada New Yorgi hotellikulude kohta põhimõtte, et ühe öö maksumus hotellis ei tohi ületada 250 USA dollarit.</span><span class="sxs-lookup"><span data-stu-id="5c1b8-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="5c1b8-107">Kui töötaja esitab kuluaruande või reisiplaani, milles toa maksumus ületab selle summa, teatab süsteem</span><span class="sxs-lookup"><span data-stu-id="5c1b8-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="5c1b8-108">töötajale, et kulupoliitikas ettenähtud summat on ületatud.</span><span class="sxs-lookup"><span data-stu-id="5c1b8-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="5c1b8-109">Poliitika määratlemisel saate konfigureerida teadet,</span><span class="sxs-lookup"><span data-stu-id="5c1b8-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="5c1b8-110">mille töötaja saab.</span><span class="sxs-lookup"><span data-stu-id="5c1b8-110">define the policy.</span></span>      
        
<span data-ttu-id="5c1b8-111">Määratleda saab kolme tüüpi poliitikaid.</span><span class="sxs-lookup"><span data-stu-id="5c1b8-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="5c1b8-112">Hoiatus – lubab töötajal kuluaruande või reisiplaani esitada, kuid kulu märgitakse kõigile kinnitajatele ja</span><span class="sxs-lookup"><span data-stu-id="5c1b8-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="5c1b8-113">hilisemaks aruandluseks.</span><span class="sxs-lookup"><span data-stu-id="5c1b8-113">for later reporting.</span></span>        

- <span data-ttu-id="5c1b8-114">Tõrge – nõuab töötajalt, et ta enne kuluaruande või reisiplaani esitamist kulu üle vaataks, nii et see vastaks poliitikale.</span><span class="sxs-lookup"><span data-stu-id="5c1b8-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="5c1b8-115">Põhjendus – nõuab, et töötaja või juht sisestaks enne kuluaruande või reisiplaani esitamist põhjenduse poliitika summa ületamise kohta.</span><span class="sxs-lookup"><span data-stu-id="5c1b8-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="5c1b8-116">Poliitika näpunäited</span><span class="sxs-lookup"><span data-stu-id="5c1b8-116">Policy tips</span></span>
<span data-ttu-id="5c1b8-117">Siin on mõned soovitused, millest on kasu uue kuluhalduse poliitika loomisel.</span><span class="sxs-lookup"><span data-stu-id="5c1b8-117">Here are a few suggestions that can assist you whe creating new policies for expense management.</span></span> 
* <span data-ttu-id="5c1b8-118">Poliitikatel on jõustumiskuupäevad ja need ei jõustu, kui poliitika luuakse pärast kulu tekkimise kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="5c1b8-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="5c1b8-119">Näiteks kui loote täna uue poliitika, et kehtestada maksimaalseks eine kuluks 50 dollarit, siis kõiki eile sisestatud kulusid ei kontrollita selle poliitika suhtes.</span><span class="sxs-lookup"><span data-stu-id="5c1b8-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="5c1b8-120">Kui loote kulukategooria jaoks poliitika, mida saab üksikasjalikult kasutada, kaaluge kulurea tüübi tingimuse lisamist.</span><span class="sxs-lookup"><span data-stu-id="5c1b8-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="5c1b8-121">Mõned poliitikad, nagu kviitungi nõudmine, ei pruugi olla konkreetsete üksikasjalike ridade jaoks sobilikud ja neid tuleks rakendada ainult päise või üksikasjalikustamata reale.</span><span class="sxs-lookup"><span data-stu-id="5c1b8-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="5c1b8-122">Millal hinnata poliitikaid</span><span class="sxs-lookup"><span data-stu-id="5c1b8-122">When to evaluate policies</span></span>

<span data-ttu-id="5c1b8-123">Kuluhalduse parameetrites on võimalus hinnata kuluhalduse poliitikaid, kui rida on salvestatud, või kui kuluaruanne on esitatud.</span><span class="sxs-lookup"><span data-stu-id="5c1b8-123">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="5c1b8-124">Kui otsustate hinnata salvestatud rida, siis tagab see, et kasutajatel on varem võimalik näha, mida nad peavad tegema, et lõpetada kõik kuluaruanded korraga.</span><span class="sxs-lookup"><span data-stu-id="5c1b8-124">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="5c1b8-125">Võite ka poliitika hindamise edasi lükata ja aega säästa, kui kontrollimine toimub lõpus, töövoogu esitamise ajal.</span><span class="sxs-lookup"><span data-stu-id="5c1b8-125">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>