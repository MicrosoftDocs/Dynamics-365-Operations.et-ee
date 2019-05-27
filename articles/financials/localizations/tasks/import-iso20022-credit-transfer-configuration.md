---
title: ISO20022 kreeditiülekande konfiguratsiooni importimine
description: See protseduur näitab, kuidas importida hankija makse elektroonilise aruandluse konfiguratsiooni.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fbd2e39f488696ebe8db5579ed88595e246ce97
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573113"
---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="8277b-103">ISO20022 kreeditiülekande konfiguratsiooni importimine</span><span class="sxs-lookup"><span data-stu-id="8277b-103">Import ISO20022 credit transfer configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8277b-104">See protseduur näitab, kuidas importida hankija makse elektroonilise aruandluse konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="8277b-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="8277b-105">Näitena on kasutatud Saksamaa ISO 20022 kreeditülekande vormingut.</span><span class="sxs-lookup"><span data-stu-id="8277b-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="8277b-106">Seda protseduuri saab kasutada teiste saadaolevate elektroonilise aruandluse vormingute puhul.</span><span class="sxs-lookup"><span data-stu-id="8277b-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="8277b-107">See ülesanne loodi, kasutades demoettevõtte DEMF andmeid, kuid võite kasutada selle ülesande täitmiseks mis tahes demoettevõtet.</span><span class="sxs-lookup"><span data-stu-id="8277b-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="8277b-108">See on esimene viiest ülesandest, mis illustreerivad koos hankija makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="8277b-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="8277b-109">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="8277b-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="8277b-110">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="8277b-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="8277b-111">Valige saadaolevate konfiguratsiooni pakkujate loendist Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8277b-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="8277b-112">Klõpsake valikut Määra aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="8277b-112">Click Set active.</span></span>
4. <span data-ttu-id="8277b-113">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="8277b-113">Click Repositories.</span></span>
5. <span data-ttu-id="8277b-114">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="8277b-114">Click Open.</span></span>
6. <span data-ttu-id="8277b-115">Klõpsake suvandit Näita filtreid.</span><span class="sxs-lookup"><span data-stu-id="8277b-115">Click Show filters.</span></span>
7. <span data-ttu-id="8277b-116">Rakendage järgmised filtrid: sisestage filtri väärtus „ISO20022 kreeditülekanne (DE)” väljale „Konfiguratsiooni nimi”, kasutades filtri tehtemärki „algab üksusega”</span><span class="sxs-lookup"><span data-stu-id="8277b-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="8277b-117">Teine võimalus on otsida konfiguratsioon loendist üles, valida see ja teisaldada see siis importimisülesandesse.</span><span class="sxs-lookup"><span data-stu-id="8277b-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="8277b-118">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="8277b-118">Click Import.</span></span>
    * <span data-ttu-id="8277b-119">Kui nupp Impordi pole saadaval, tähendab see, et see konfiguratsioon on juba imporditud.</span><span class="sxs-lookup"><span data-stu-id="8277b-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="8277b-120">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="8277b-120">Click Yes.</span></span>

