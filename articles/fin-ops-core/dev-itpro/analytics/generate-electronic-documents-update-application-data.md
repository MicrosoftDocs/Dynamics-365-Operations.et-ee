---
title: Elektroonilise aruandluse kaudu elektrooniliste dokumentide loomine ja rakenduse andmete värskendamine
description: Saate kujundada elektroonilise aruandluse (ER) vorminguid, mida saab rakenduses väljaminevate elektrooniliste dokumentide loomiseks kasutada. Saate kujundada ka ER-vorminguid, mis sõeluvad sissetulevaid elektroonilisi dokumente ja kasutavad nende dokumentide sisu rakenduse andmete uuendamiseks.
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 333f91cef12b6564ca9bc668732b4cc038f0fa7e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181860"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a><span data-ttu-id="e098c-104">Elektroonilise aruandluse kaudu elektrooniliste dokumentide loomine ja rakenduse andmete värskendamine</span><span class="sxs-lookup"><span data-stu-id="e098c-104">Generate electronic documents and update application data by using ER</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e098c-105">Saate kujundada elektroonilise aruandluse (ER) vorminguid, mida saab rakenduses väljaminevate elektrooniliste dokumentide loomiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="e098c-105">You can design Electronic reporting (ER) formats that can be used in the application to generate outgoing electronic documents.</span></span> <span data-ttu-id="e098c-106">Saate kujundada ka ER-vorminguid, mis sõeluvad sissetulevaid elektroonilisi dokumente ja kasutavad nende dokumentide sisu rakenduse andmete uuendamiseks.</span><span class="sxs-lookup"><span data-stu-id="e098c-106">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span>

<span data-ttu-id="e098c-107">Selle funktsiooniga saab ühte ER-i vormingut kasutada väljaminevate elektrooniliste dokumentide loomiseks ja seejärel rakenduse andmete uuendamiseks.</span><span class="sxs-lookup"><span data-stu-id="e098c-107">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="e098c-108">Seda funktsiooni saab kasutada järgmistes stsenaariumides.</span><span class="sxs-lookup"><span data-stu-id="e098c-108">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="e098c-109">Rakenduse andmete korduva kasutamise vältimiseks järjestikustes protsessides võite märkida rakenduse andmed kohe pärast nende kasutamist elektrooniliste dokumentide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="e098c-109">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="e098c-110">Näiteks saate märkida maksekanded juba töödelduks kohe pärast seda, kui need on koostatud makseteatesse lisatud.</span><span class="sxs-lookup"><span data-stu-id="e098c-110">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="e098c-111">ER-i loogika abil loodud elektrooniliste dokumentide töötlemise üksikasjade salvestamiseks.</span><span class="sxs-lookup"><span data-stu-id="e098c-111">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="e098c-112">Näiteks kordumatu makseteate ID, mis luuakse ER-i avaldise abil.</span><span class="sxs-lookup"><span data-stu-id="e098c-112">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="e098c-113">Avaldis põhineb ER-i vormi käitamisel dokumentide loomiseks ER-i dialoogiboksi sisestatud andmetel.</span><span class="sxs-lookup"><span data-stu-id="e098c-113">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="e098c-114">Lisateabe saamiseks selle funktsiooni kohta esitage tegevusjuhiste kogum Elektrooniline aruandlus. Dokumentide loomine rakenduse andmete uuendamisega (osa äriprotsessist 7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)), mis selgitab Intrastati aruandluse ja arhiivimise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="e098c-114">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="e098c-115">Teatud etappide läbimiseks nendes tegevusjuhistes on vajalikud järgmised failid.</span><span class="sxs-lookup"><span data-stu-id="e098c-115">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="e098c-116">Laadige need failid alla ja salvestage kohalikku arvutisse.</span><span class="sxs-lookup"><span data-stu-id="e098c-116">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="e098c-117">Elektroonilise aruandluse andmemudeli konfiguratsioon: Intrastat (mudel)</span><span class="sxs-lookup"><span data-stu-id="e098c-117">ER data model configuration: Intrastat (model)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="e098c-118">Elektroonilise aruandluse mudeli vastendamise konfiguratsioon: Intrastat (vastendamine)</span><span class="sxs-lookup"><span data-stu-id="e098c-118">ER model mapping configuration: Intrastat (mapping)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="e098c-119">Elektroonilise aruandluse vormingu konfiguratsioon: Intrastat (vorming)</span><span class="sxs-lookup"><span data-stu-id="e098c-119">ER format configuration: Intrastat (format)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)