---
title: Süsteemiadministraatorid ei saa tellimuste ootelolekuid tühjendada, sest nad pole autoriseeritud
description: Süsteemiadministraatorid ei saa tellimuste ootelolekuid tühjendada, sest nad pole autoriseeritud.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026456"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a><span data-ttu-id="7a5c2-103">Süsteemiadministraatorid ei saa tellimuste ootelolekuid tühjendada, sest nad pole autoriseeritud</span><span class="sxs-lookup"><span data-stu-id="7a5c2-103">System administrators can't clear order holds because they aren't authorized</span></span>

<span data-ttu-id="7a5c2-104">KB number: 4614642</span><span class="sxs-lookup"><span data-stu-id="7a5c2-104">KB number: 4614642</span></span>

## <a name="symptoms"></a><span data-ttu-id="7a5c2-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="7a5c2-105">Symptoms</span></span>

<span data-ttu-id="7a5c2-106">Süsteemiadministraatorid ei saa müügitellimuste ootel olemist tühjendada, kui neil pole tellimuse ootele määratud konkreetset rolli.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-106">System administrators can't clear sales order holds unless they have the specific role that is assigned in the order hold code.</span></span>

## <a name="resolution"></a><span data-ttu-id="7a5c2-107">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="7a5c2-107">Resolution</span></span>

<span data-ttu-id="7a5c2-108">Juurdepääs teatud toimingutele, näiteks müügitellimuste kinnipidamiste kustutamine, on tingitud äripoliitika seadistamisest.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-108">Access to some operations, such as clearing sales order holds, is driven by the setup of a business policy.</span></span> <span data-ttu-id="7a5c2-109">Süsteemiadministraatoritel pole tavaliselt lubatud seda tüüpi toiminguid sooritada.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-109">System administrators aren't typically allowed to perform operations of this type.</span></span> 

<span data-ttu-id="7a5c2-110">Sageli reguleerib juurdepääsu konkreetsele toimingule äripoliitika ning seda ülesannet saavad täita ainult organisatsiooni konkreetsed isikud.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-110">More often, access to perform a specific task is governed by business policies, and only specific persons in an organization are approved to perform that task.</span></span> <span data-ttu-id="7a5c2-111">Näited hõlmavad kinnitusi, mis on töövoo kinnituste tulemus ja töövoo konfiguratsioonist tulenevad konkreetsed ülesanded.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-111">Examples include approvals that are the result of workflow approvals and specific tasks that are the result of a workflow configuration.</span></span>

<span data-ttu-id="7a5c2-112">Kuigi ühtegi töövoogu ei ole tellimuste ootel olekuga seostatud, on põhimõte sarnane.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-112">Although no workflow is associated with order holds, the principle is similar.</span></span> <span data-ttu-id="7a5c2-113">Asjakohane roll määrab organisatsioonis konkreetse inimeste grupi, kellel on õigus tellimuse ootel olemised kustutada.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-113">A relevant role designates the specific group of people in an organization who have the right to clear order holds.</span></span> <span data-ttu-id="7a5c2-114">Seda õigust ei tuleks tingimata anda kõikidele administraatoritele, kuna see lähenemine rikub määratletud äripoliitikat.</span><span class="sxs-lookup"><span data-stu-id="7a5c2-114">This right should not necessarily be granted to all administrators, because that approach violates the defined business policy.</span></span>
