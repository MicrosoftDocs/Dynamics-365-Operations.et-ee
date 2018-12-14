---
title: "Talenti kliendi ühendus katkeb"
description: "See teema selgitab, mida teha, kui kliendi ühendus tema keskkonnaga katkeb ja põhjus pole teada."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 4f96b986059c179268f8a96ea7e7725831a93524
ms.contentlocale: et-ee
ms.lasthandoff: 12/04/2018

---

# <a name="talent-client-disconnects"></a><span data-ttu-id="f6af5-103">Talenti kliendi ühendus katkeb</span><span class="sxs-lookup"><span data-stu-id="f6af5-103">Talent client disconnects</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f6af5-104">**Keskkonna üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="f6af5-104">**Environment details**</span></span> 

<span data-ttu-id="f6af5-105">Probleem võib esineda kõigis keskkondades.</span><span class="sxs-lookup"><span data-stu-id="f6af5-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="f6af5-106">**Sümptom**</span><span class="sxs-lookup"><span data-stu-id="f6af5-106">**Symptom**</span></span> 

<span data-ttu-id="f6af5-107">Kliendi ühendus tema keskkonnaga katkeb ja põhjus pole teada.</span><span class="sxs-lookup"><span data-stu-id="f6af5-107">The customer is disconnected from his or her environment and doesn't know why.</span></span> <span data-ttu-id="f6af5-108">Klient saab ühe järgmistest tõrketeadetest:</span><span class="sxs-lookup"><span data-stu-id="f6af5-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="f6af5-109">Teie ühendus on katkenud.</span><span class="sxs-lookup"><span data-stu-id="f6af5-109">We've lost your connection.</span></span> <span data-ttu-id="f6af5-110">Töötamiseks jätkamises klõpsake nuppu Sule.</span><span class="sxs-lookup"><span data-stu-id="f6af5-110">Click Close to continue working.</span></span>
- <span data-ttu-id="f6af5-111">Näib, et olete kaotanud võrguühenduse. Uuesti proovimiseks klõpsake nuppu Proovi uuesti.</span><span class="sxs-lookup"><span data-stu-id="f6af5-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="f6af5-112">**Punane lipp**</span><span class="sxs-lookup"><span data-stu-id="f6af5-112">**Red flag**</span></span>

<span data-ttu-id="f6af5-113">See probleem ilmneb tihti siis, kui kasutajad on juurutusetapis, võrdlevad teavet töö- ja katsekeskkondade vahel ning unustavad, et nad liiguvad seansside vahel.</span><span class="sxs-lookup"><span data-stu-id="f6af5-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="f6af5-114">Kui kasutajad on selles etapis, ilmneb tõenäoliselt see probleem.</span><span class="sxs-lookup"><span data-stu-id="f6af5-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="f6af5-115">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="f6af5-115">**Issue**</span></span> 

<span data-ttu-id="f6af5-116">**Brauserite tüübid:** Google Chrome, Internet Explorer ja Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f6af5-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="f6af5-117">Rakenduse Microsoft Dynamics 365 for Talent platvorm katkestab kasutajate ühendused, kui ühel kasutajal on korraga samas brauseritüübis avatud kaks erinevat seanssi.</span><span class="sxs-lookup"><span data-stu-id="f6af5-117">The Microsoft Dynamics 365 for Talent platform disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="f6af5-118">(Nt, kasutaja A vaatab Chrome’is nii keskkonda 1 kui ka keskkonda 2.) Pole oluline, kas kasutajad avavad erinevad brauseriaknad või erinevad vahekaardid.</span><span class="sxs-lookup"><span data-stu-id="f6af5-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="f6af5-119">Kui samu kasutajamandaate kasutatakse korraga ja samas brauseritüübis nii keskkonda 1 kui ka keskkonda 2 sisselogimiseks, katkestab Talent ühe seansi ühenduse.</span><span class="sxs-lookup"><span data-stu-id="f6af5-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Talent disconnects one of the sessions.</span></span>

<span data-ttu-id="f6af5-120">**Lahendus**</span><span class="sxs-lookup"><span data-stu-id="f6af5-120">**Solution**</span></span>

<span data-ttu-id="f6af5-121">Veenduge, et korraga oleks ühes brauseritüübis avatud ainult üks keskkond.</span><span class="sxs-lookup"><span data-stu-id="f6af5-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="f6af5-122">Kasutajad saavad samas keskkonnas avada mitu seanssi (s.t samas brauseris mitu vahekaarti).</span><span class="sxs-lookup"><span data-stu-id="f6af5-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="f6af5-123">Kasutajad, kes soovivad korraga hüpata kahe keskkonna vahel, peavad kummagi keskkonna avama erinevas brauseritüübis.</span><span class="sxs-lookup"><span data-stu-id="f6af5-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="f6af5-124">(Nt, kasutaja A saab vaadata keskkonda 1 Chrome’is ja keskkonda 2 Microsoft Edge’is.)</span><span class="sxs-lookup"><span data-stu-id="f6af5-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>

