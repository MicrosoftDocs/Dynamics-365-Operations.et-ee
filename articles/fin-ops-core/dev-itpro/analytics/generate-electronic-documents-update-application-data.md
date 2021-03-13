---
title: Elektroonilise aruandluse kaudu elektrooniliste dokumentide loomine ja rakenduse andmete värskendamine
description: Saate kujundada elektroonilise aruandluse (ER) vorminguid, mida saab rakenduses väljaminevate elektrooniliste dokumentide loomiseks kasutada.
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
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ae3405a882ac37fd9758d8ff0902896562fa06b
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093869"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a><span data-ttu-id="28ed4-103">Elektrooniliste dokumentide loomine ja rakenduse andmete värskendamine ER-i abil</span><span class="sxs-lookup"><span data-stu-id="28ed4-103">Generate electronic documents and update application data by using ER</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28ed4-104">Saate kujundada elektroonilise aruandluse (ER) vorminguid, mida saab rakenduses väljaminevate elektrooniliste dokumentide loomiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="28ed4-104">You can design Electronic reporting (ER) formats that can be used in the application to generate outgoing electronic documents.</span></span> <span data-ttu-id="28ed4-105">Saate kujundada ka ER-vorminguid, mis sõeluvad sissetulevaid elektroonilisi dokumente ja kasutavad nende dokumentide sisu rakenduse andmete uuendamiseks.</span><span class="sxs-lookup"><span data-stu-id="28ed4-105">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span>

<span data-ttu-id="28ed4-106">Selle funktsiooniga saab ühte ER-i vormingut kasutada väljaminevate elektrooniliste dokumentide loomiseks ja seejärel rakenduse andmete uuendamiseks.</span><span class="sxs-lookup"><span data-stu-id="28ed4-106">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="28ed4-107">Seda funktsiooni saab kasutada järgmistes stsenaariumides.</span><span class="sxs-lookup"><span data-stu-id="28ed4-107">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="28ed4-108">Rakenduse andmete korduva kasutamise vältimiseks järjestikustes protsessides võite märkida rakenduse andmed kohe pärast nende kasutamist elektrooniliste dokumentide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="28ed4-108">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="28ed4-109">Näiteks saate märkida maksekanded juba töödelduks kohe pärast seda, kui need on koostatud makseteatesse lisatud.</span><span class="sxs-lookup"><span data-stu-id="28ed4-109">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="28ed4-110">ER-i loogika abil loodud elektrooniliste dokumentide töötlemise üksikasjade salvestamiseks.</span><span class="sxs-lookup"><span data-stu-id="28ed4-110">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="28ed4-111">Näiteks kordumatu makseteate ID, mis luuakse ER-i avaldise abil.</span><span class="sxs-lookup"><span data-stu-id="28ed4-111">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="28ed4-112">Avaldis põhineb ER-i vormi käitamisel dokumentide loomiseks ER-i dialoogiboksi sisestatud andmetel.</span><span class="sxs-lookup"><span data-stu-id="28ed4-112">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="28ed4-113">Lisateabe saamiseks selle funktsiooni kohta esitage tegevusjuhiste kogum Elektrooniline aruandlus. Dokumentide loomine rakenduse andmete uuendamisega (osa äriprotsessist 7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)), mis selgitab Intrastati aruandluse ja arhiivimise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="28ed4-113">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="28ed4-114">Teatud etappide läbimiseks nendes tegevusjuhistes on vajalikud järgmised failid.</span><span class="sxs-lookup"><span data-stu-id="28ed4-114">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="28ed4-115">Laadige need failid alla ja salvestage kohalikku arvutisse.</span><span class="sxs-lookup"><span data-stu-id="28ed4-115">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="28ed4-116">Elektroonilise aruandluse andmemudeli konfiguratsioon: Intrastat (mudel)</span><span class="sxs-lookup"><span data-stu-id="28ed4-116">ER data model configuration: Intrastat (model)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="28ed4-117">Elektroonilise aruandluse mudeli vastendamise konfiguratsioon: Intrastat (vastendamine)</span><span class="sxs-lookup"><span data-stu-id="28ed4-117">ER model mapping configuration: Intrastat (mapping)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="28ed4-118">Elektroonilise aruandluse vormingu konfiguratsioon: Intrastat (vorming)</span><span class="sxs-lookup"><span data-stu-id="28ed4-118">ER format configuration: Intrastat (format)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
