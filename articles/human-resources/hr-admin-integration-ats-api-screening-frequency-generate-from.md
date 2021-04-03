---
title: Skriiningu sageduse loomise vorm
description: Selles teemas kirjeldatakse skriiningu sageduse loomise vormi suvandikomplekti rakendusele Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 238cd5da750d815c904090cc9002e3d1a5d2bcc7
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464570"
---
# <a name="screening-frequency-generate-from"></a><span data-ttu-id="88a54-103">Skriiningu sageduse loomise vorm</span><span class="sxs-lookup"><span data-stu-id="88a54-103">Screening frequency generate from</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="88a54-104">Selles teemas kirjeldatakse skriiningu sageduse loomise vormi suvandikomplekti rakendusele Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="88a54-104">This topic describes the Screening frequency generate from option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="88a54-105">Füüsiline nimi: mshr_hcmfrequencygeneratefrom</span><span class="sxs-lookup"><span data-stu-id="88a54-105">Physical name: mshr_hcmfrequencygeneratefrom</span></span>

<span data-ttu-id="88a54-106">See loetelu annab järgmise vajaliku skriiningu alguskuupäeva arvestuse määramise väärtuste suvandikomplekti.</span><span class="sxs-lookup"><span data-stu-id="88a54-106">This enumeration provides the option set of values for determining the start date of the calculation for the next required screening.</span></span>

| <span data-ttu-id="88a54-107">Väärtus</span><span class="sxs-lookup"><span data-stu-id="88a54-107">Value</span></span> | <span data-ttu-id="88a54-108">Silt</span><span class="sxs-lookup"><span data-stu-id="88a54-108">Label</span></span> | <span data-ttu-id="88a54-109">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="88a54-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="88a54-110">200000000 Pole valitud</span><span class="sxs-lookup"><span data-stu-id="88a54-110">200000000 Not selected</span></span> | <span data-ttu-id="88a54-111">Väärtust pole valitud.</span><span class="sxs-lookup"><span data-stu-id="88a54-111">No value has been selected.</span></span> |
| <span data-ttu-id="88a54-112">200000001 Lõpetamiskuupäev</span><span class="sxs-lookup"><span data-stu-id="88a54-112">200000001 Date completed</span></span> | <span data-ttu-id="88a54-113">Arvestus tehakse alates viimase lõpuleviidud skriiningu kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="88a54-113">Calculation is done from the last screening date completed.</span></span> |
| <span data-ttu-id="88a54-114">200000002 Kuupäev on nõutav</span><span class="sxs-lookup"><span data-stu-id="88a54-114">200000002 Date required</span></span> | <span data-ttu-id="88a54-115">Arvestus tehakse alates viimasest nõutavast skriiningu kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="88a54-115">Calculation is done from the last screening date required.</span></span> |

## <a name="see-also"></a><span data-ttu-id="88a54-116">Vt ka</span><span class="sxs-lookup"><span data-stu-id="88a54-116">See also</span></span>

[<span data-ttu-id="88a54-117">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="88a54-117">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="88a54-118">Palgatava kandidaadi päringu näidis</span><span class="sxs-lookup"><span data-stu-id="88a54-118">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]