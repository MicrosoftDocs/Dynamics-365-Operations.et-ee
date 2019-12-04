---
title: ISO20022 otsekorralduse konfiguratsiooni importimine
description: See protseduur näitab, kuidas importida kliendi makse elektroonilise aruandluse konfiguratsiooni.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7eee00021f49ac0110d7bde07faba8095348e1b4
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185746"
---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="03f61-103">ISO20022 otsekorralduse konfiguratsiooni importimine</span><span class="sxs-lookup"><span data-stu-id="03f61-103">Import ISO20022 direct debit configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="03f61-104">See protseduur näitab, kuidas importida kliendi makse elektroonilise aruandluse konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="03f61-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="03f61-105">Protseduur kasutab näitena ISO-20022 otsekorralduse vormingut.</span><span class="sxs-lookup"><span data-stu-id="03f61-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="03f61-106">See protseduur loodi, kasutades demoettevõtte DEMF andmeid, kuid võite kasutada selleks mis tahes demoettevõtet.</span><span class="sxs-lookup"><span data-stu-id="03f61-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="03f61-107">See on esimene viiest protseduurist, mis näitab kliendi makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="03f61-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="03f61-108">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="03f61-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="03f61-109">Valige saadaolevate konfiguratsiooni pakkujate loendist Microsoft.</span><span class="sxs-lookup"><span data-stu-id="03f61-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="03f61-110">Klõpsake valikut Määra aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="03f61-110">Click Set active.</span></span>
4. <span data-ttu-id="03f61-111">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="03f61-111">Click Repositories.</span></span>
5. <span data-ttu-id="03f61-112">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="03f61-112">Click Open.</span></span>
6. <span data-ttu-id="03f61-113">Klõpsake suvandit Näita filtreid.</span><span class="sxs-lookup"><span data-stu-id="03f61-113">Click Show filters.</span></span>
7. <span data-ttu-id="03f61-114">Rakendage järgmised filtrid: sisestage filtri väärtus „ISO20022 otsekorraldus (DE)” väljale „Konfiguratsiooni nimi”, kasutades filtri tehtemärki „algab üksusega”</span><span class="sxs-lookup"><span data-stu-id="03f61-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="03f61-115">Soovi korral võite otsida konfiguratsiooni loendist üles, selle valida ja selle toimingu vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="03f61-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="03f61-116">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="03f61-116">Click Import.</span></span>
    * <span data-ttu-id="03f61-117">Kui nupp Impordi pole saadaval, tähendab see, et see konfiguratsioon on juba imporditud.</span><span class="sxs-lookup"><span data-stu-id="03f61-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="03f61-118">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="03f61-118">Click Yes.</span></span>
