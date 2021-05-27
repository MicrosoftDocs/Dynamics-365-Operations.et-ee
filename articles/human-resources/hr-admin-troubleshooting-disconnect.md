---
title: Kliendi ühendus katkeb
description: See artikkel selgitab, mida teha, kui kliendi ühendus tema keskkonnaga katkeb ja põhjus pole teada.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: db0e8efec1a5a6f01c9b7c4d9334a959fc42886b
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027983"
---
# <a name="client-disconnects"></a><span data-ttu-id="ba8e7-103">Kliendi ühendus katkeb</span><span class="sxs-lookup"><span data-stu-id="ba8e7-103">Client disconnects</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ba8e7-104">**Keskkonna üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="ba8e7-104">**Environment details**</span></span> 

<span data-ttu-id="ba8e7-105">Probleem võib esineda kõigis keskkondades.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-105">This issue can occur in all environments.</span></span>
 
<span data-ttu-id="ba8e7-106">**Sümptom**</span><span class="sxs-lookup"><span data-stu-id="ba8e7-106">**Symptom**</span></span> 

<span data-ttu-id="ba8e7-107">Kliendi ühendus keskkonnaga katkeb ja selle põhjus pole teada.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-107">The customer is disconnected from the environment and doesn't know why.</span></span> <span data-ttu-id="ba8e7-108">Klient saab ühe järgmistest tõrketeadetest:</span><span class="sxs-lookup"><span data-stu-id="ba8e7-108">The customer receives one of the following error messages:</span></span>

- <span data-ttu-id="ba8e7-109">Teie ühendus on katkenud.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-109">We've lost your connection.</span></span> <span data-ttu-id="ba8e7-110">Töötamiseks jätkamises klõpsake nuppu Sule.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-110">Click Close to continue working.</span></span>
- <span data-ttu-id="ba8e7-111">Näib, et olete kaotanud võrguühenduse. Uuesti proovimiseks klõpsake nuppu Proovi uuesti.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-111">It appears you lost network connectivity, click Retry to try again.</span></span>

<span data-ttu-id="ba8e7-112">**Punane lipp**</span><span class="sxs-lookup"><span data-stu-id="ba8e7-112">**Red flag**</span></span>

<span data-ttu-id="ba8e7-113">See probleem ilmneb tihti siis, kui kasutajad on juurutusetapis, võrdlevad teavet töö- ja katsekeskkondade vahel ning unustavad, et nad liiguvad seansside vahel.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-113">This issue often occurs when users are in the implementation stage, are comparing information across production and test environments, and forget that they are moving between sessions.</span></span> <span data-ttu-id="ba8e7-114">Kui kasutajad on selles etapis, ilmneb tõenäoliselt see probleem.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-114">If users are at this stage, they will most likely experience this issue.</span></span>

<span data-ttu-id="ba8e7-115">**Väljastamine**</span><span class="sxs-lookup"><span data-stu-id="ba8e7-115">**Issue**</span></span> 

<span data-ttu-id="ba8e7-116">**Brauserite tüübid:** Google Chrome, Internet Explorer ja Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ba8e7-116">**Browser types:** Google Chrome, Internet Explorer, and Microsoft Edge</span></span>

<span data-ttu-id="ba8e7-117">Rakendus Microsoft Dynamics 365 Human Resources katkestab kasutajate ühendused, kui ühel kasutajal on korraga samas brauseritüübis avatud kaks erinevat seanssi.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-117">Microsoft Dynamics 365 Human Resources disconnects users when two different sessions are open at the same time for the same user and the same browser type.</span></span> <span data-ttu-id="ba8e7-118">(Nt, kasutaja A vaatab Chrome’is nii keskkonda 1 kui ka keskkonda 2.) Pole oluline, kas kasutajad avavad erinevad brauseriaknad või erinevad vahekaardid.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-118">(For example, user A is viewing both environment 1 and environment 2 in Chrome.) It doesn't matter whether the users open different browser windows or different tabs.</span></span> <span data-ttu-id="ba8e7-119">Kui samu kasutajamandaate kasutatakse korraga ja samas brauseritüübis nii keskkonda 1 kui ka keskkonda 2 sisselogimiseks, katkestab Human Resources ühe seansi ühenduse.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-119">If the same user credentials are used to sign in to both environment 1 and environment 2 at the same time and in the same browser type, Human Resources disconnects one of the sessions.</span></span>

<span data-ttu-id="ba8e7-120">**Lahendus**</span><span class="sxs-lookup"><span data-stu-id="ba8e7-120">**Solution**</span></span>

<span data-ttu-id="ba8e7-121">Veenduge, et korraga oleks ühes brauseritüübis avatud ainult üks keskkond.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-121">Make sure that only one environment is open at a time for a given browser type.</span></span> <span data-ttu-id="ba8e7-122">Kasutajad saavad samas keskkonnas avada mitu seanssi (s.t samas brauseris mitu vahekaarti).</span><span class="sxs-lookup"><span data-stu-id="ba8e7-122">Users can open multiple sessions to the same environment (that is, multiple tabs in the same browser).</span></span>

<span data-ttu-id="ba8e7-123">Kasutajad, kes soovivad korraga hüpata kahe keskkonna vahel, peavad kummagi keskkonna avama erinevas brauseritüübis.</span><span class="sxs-lookup"><span data-stu-id="ba8e7-123">Users who want to jump between two environments at the same time should open each environment in a different browser type.</span></span> <span data-ttu-id="ba8e7-124">(Nt, kasutaja A saab vaadata keskkonda 1 Chrome’is ja keskkonda 2 Microsoft Edge’is.)</span><span class="sxs-lookup"><span data-stu-id="ba8e7-124">(For example, user A can view environment 1 in Chrome and environment 2 in Microsoft Edge.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]