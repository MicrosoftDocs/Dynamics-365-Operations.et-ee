---
title: Skriiningu sageduse loomise vorm
description: Selles teemas kirjeldatakse skriiningu sageduse loomise vormi suvandikomplekti rakendusele Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bee0522ea244cab2f5d6864b2a763df6e314e02d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805150"
---
# <a name="screening-frequency-generate-from"></a><span data-ttu-id="d5d97-103">Skriiningu sageduse loomise vorm</span><span class="sxs-lookup"><span data-stu-id="d5d97-103">Screening frequency generate from</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d5d97-104">Selles teemas kirjeldatakse skriiningu sageduse loomise vormi suvandikomplekti rakendusele Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d5d97-104">This topic describes the Screening frequency generate from option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="d5d97-105">Füüsiline nimi: mshr_hcmfrequencygeneratefrom</span><span class="sxs-lookup"><span data-stu-id="d5d97-105">Physical name: mshr_hcmfrequencygeneratefrom</span></span>

<span data-ttu-id="d5d97-106">See loetelu annab järgmise vajaliku skriiningu alguskuupäeva arvestuse määramise väärtuste suvandikomplekti.</span><span class="sxs-lookup"><span data-stu-id="d5d97-106">This enumeration provides the option set of values for determining the start date of the calculation for the next required screening.</span></span>

| <span data-ttu-id="d5d97-107">Väärtus</span><span class="sxs-lookup"><span data-stu-id="d5d97-107">Value</span></span> | <span data-ttu-id="d5d97-108">Silt</span><span class="sxs-lookup"><span data-stu-id="d5d97-108">Label</span></span> | <span data-ttu-id="d5d97-109">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d5d97-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d5d97-110">200000000 Pole valitud</span><span class="sxs-lookup"><span data-stu-id="d5d97-110">200000000 Not selected</span></span> | <span data-ttu-id="d5d97-111">Väärtust pole valitud.</span><span class="sxs-lookup"><span data-stu-id="d5d97-111">No value has been selected.</span></span> |
| <span data-ttu-id="d5d97-112">200000001 Lõpetamiskuupäev</span><span class="sxs-lookup"><span data-stu-id="d5d97-112">200000001 Date completed</span></span> | <span data-ttu-id="d5d97-113">Arvestus tehakse alates viimase lõpuleviidud skriiningu kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="d5d97-113">Calculation is done from the last screening date completed.</span></span> |
| <span data-ttu-id="d5d97-114">200000002 Kuupäev on nõutav</span><span class="sxs-lookup"><span data-stu-id="d5d97-114">200000002 Date required</span></span> | <span data-ttu-id="d5d97-115">Arvestus tehakse alates viimasest nõutavast skriiningu kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="d5d97-115">Calculation is done from the last screening date required.</span></span> |

## <a name="see-also"></a><span data-ttu-id="d5d97-116">Vt ka</span><span class="sxs-lookup"><span data-stu-id="d5d97-116">See also</span></span>

[<span data-ttu-id="d5d97-117">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="d5d97-117">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="d5d97-118">Palgatava kandidaadi päringu näidis</span><span class="sxs-lookup"><span data-stu-id="d5d97-118">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]