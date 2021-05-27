---
title: Komplekteerimislehe registreerimise ajal asukoha valimisel ilmneb tõrge
description: Komplekteerimislehe registreerimise ajal asukoha valimisel ilmneb tõrge.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b7fc579821f9a80d94aea949fcc0301b9d8f6935
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026423"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a><span data-ttu-id="8c7cc-103">Komplekteerimislehe registreerimise ajal asukoha valimisel ilmneb tõrge</span><span class="sxs-lookup"><span data-stu-id="8c7cc-103">An error occurs when the location is selected during picking list registration</span></span>

<span data-ttu-id="8c7cc-104">KB number: 4613106</span><span class="sxs-lookup"><span data-stu-id="8c7cc-104">KB number: 4613106</span></span>

## <a name="symptoms"></a><span data-ttu-id="8c7cc-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="8c7cc-105">Symptoms</span></span>

<span data-ttu-id="8c7cc-106">See probleem ilmneb, kui süsteem on konfigureeritud müügitellimusi automaatselt reserveerima.</span><span class="sxs-lookup"><span data-stu-id="8c7cc-106">This issue occurs when your system is configured to automatically reserve sales orders.</span></span> <span data-ttu-id="8c7cc-107">Kui püüate valida asukohta komplekteerimislehe registreerimisreale, saate laohalduse (WMS) reserveerimisprotsesside kasutamisel järgmise tõrketeate:</span><span class="sxs-lookup"><span data-stu-id="8c7cc-107">If you try to select the location for a picking list registration line, you receive the following error message when you use warehouse management (WMS) reservation processes:</span></span>

> <span data-ttu-id="8c7cc-108">Kogust ei saa uute dimensioonidega värskendada</span><span class="sxs-lookup"><span data-stu-id="8c7cc-108">Can't update quantity with new dimensions</span></span>

<span data-ttu-id="8c7cc-109">See probleem võib ilmneda, kuna teil ei ole määratud asukohas piisavalt vaba kaubavaru.</span><span class="sxs-lookup"><span data-stu-id="8c7cc-109">This issue can occur because you don't have enough on-hand inventory at a specified location.</span></span>

## <a name="resolution"></a><span data-ttu-id="8c7cc-110">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="8c7cc-110">Resolution</span></span>

<span data-ttu-id="8c7cc-111">Süsteem käitub kavandatud viisil.</span><span class="sxs-lookup"><span data-stu-id="8c7cc-111">The system is behaving as designed.</span></span>

<span data-ttu-id="8c7cc-112">Stsenaariumides, kus kasutate laotaseme reserveerimisprotsessi, kui vaba kaubavaru ei reserveerita kõigil varude dimensioonitasemetel ja teil ei ole määratud asukohas piisavalt vaba kaubavaru, on soovitatav kasutada komplekteerimisrealt käsitsi reserveerimisprotsessi.</span><span class="sxs-lookup"><span data-stu-id="8c7cc-112">In scenarios where you use the warehouse-level reservation process, if the on-hand inventory won't be reserved on all inventory dimension levels, and you don't have enough on-hand inventory at a specified location, we recommend that you use the manual reservation process from the picking line.</span></span> <span data-ttu-id="8c7cc-113">Seejärel saate kasutada funktsiooni *Reserveeri partii* et jaotada madalamad reserveeringud, nt asukoht, kõigi vabade koguste puhul.</span><span class="sxs-lookup"><span data-stu-id="8c7cc-113">You can then use the *Reserve lot* function to distribute the lower reservations, such as location, for all the available on-hand quantities.</span></span>
