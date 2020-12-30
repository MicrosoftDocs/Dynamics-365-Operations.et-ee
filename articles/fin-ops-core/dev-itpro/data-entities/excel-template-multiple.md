---
title: Andmete importimine mitme töölehega Exceli andmeüksuse mallidest
description: Selles teemas kirjeldatakse andmete importimist Exceli andmeüksuse mallidest rakendusse Finance and Operations.
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 618b62364353f409f6971ddd9adc7d55297d09cf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688075"
---
# <a name="import-data-from-excel-data-entity-templates-that-have-multiple-worksheets"></a><span data-ttu-id="b235e-103">Andmete importimine mitme töölehega Exceli andmeüksuse mallidest</span><span class="sxs-lookup"><span data-stu-id="b235e-103">Import data from Excel data entity templates that have multiple worksheets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b235e-104">Andmehaldus rakenduses toetab andmeüksuste puhul Microsoft Exceli põhiseid malle.</span><span class="sxs-lookup"><span data-stu-id="b235e-104">Data management in the application supports Microsoft Excel-based templates for data entities.</span></span> <span data-ttu-id="b235e-105">Need mallid võivad sisaldada üht või mitut töölehte.</span><span class="sxs-lookup"><span data-stu-id="b235e-105">These templates can contain one or more worksheets.</span></span> <span data-ttu-id="b235e-106">Mitme töölehega malle kasutatakse sageli siis, kui andmeid on mugav hallata ühes failis ja importida neid mitmesse andmeüksusse.</span><span class="sxs-lookup"><span data-stu-id="b235e-106">Templates with multiple worksheets are often used when it is convenient to manage data in a single file and import it to multiple data entities.</span></span> <span data-ttu-id="b235e-107">Selleks näiteks oleks laoalad ja laod.</span><span class="sxs-lookup"><span data-stu-id="b235e-107">An example would be sites and warehouses.</span></span>

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a><span data-ttu-id="b235e-108">Faili üks kord üleslaadimine ja kõigi üksustega vastendamine</span><span class="sxs-lookup"><span data-stu-id="b235e-108">Upload a file once and map it to all entities</span></span>
<span data-ttu-id="b235e-109">Oletame näiteks, et meil on üks Exceli fail koos töölehtedega **Laoalad** ja **Laod**.</span><span class="sxs-lookup"><span data-stu-id="b235e-109">Let's take an example where there is one Excel file with worksheets called **Sites** and **Warehouses**.</span></span> <span data-ttu-id="b235e-110">Andmete importimise projekti seadistamiseks lisate esimese andmeüksuse **Laoalad** ja seejärel laadite faili üles.</span><span class="sxs-lookup"><span data-stu-id="b235e-110">To set up the data import project, you would add the first data entity, **Sites** and then upload the file.</span></span> <span data-ttu-id="b235e-111">Saate valida selle üksuse puhul töölehena kasutamiseks **Laoalad**.</span><span class="sxs-lookup"><span data-stu-id="b235e-111">You will be able to select **Sites** as the worksheet to be used for this entity.</span></span>

<span data-ttu-id="b235e-112">Teise üksuse, **Laod**, lisamisel vormilt **Faili lisamine** lahkumata võimaldab töölehe otsing valida töölehe **Laod** jälle ilma faili üles laadimata.</span><span class="sxs-lookup"><span data-stu-id="b235e-112">If you add the second entity **Warehouses** without leaving the **Add file** form, the worksheet lookup will let you select the **Warehouses** worksheet without having to upload the file again.</span></span> <span data-ttu-id="b235e-113">Ainus põhjus uue faili üleslaadimiseks oleks see, kui töölehe **Laod** andmed oleksid eraldi failis.</span><span class="sxs-lookup"><span data-stu-id="b235e-113">The only reason to upload a new file would be if the **Warehouses** data was in a different file.</span></span>

![Mitu töölehte](./media/AddFileMultipleWorkSheets.png)

## <a name="fix-worksheet-to-entity-mapping"></a><span data-ttu-id="b235e-115">Töölehe ja üksuse vastenduse fikseerimine</span><span class="sxs-lookup"><span data-stu-id="b235e-115">Fix worksheet to entity mapping</span></span>

<span data-ttu-id="b235e-116">Töölehe vastenduse andmeüksusega imporditöös saab ruudustikust fikseerida.</span><span class="sxs-lookup"><span data-stu-id="b235e-116">The mapping of the worksheet to a data entity in the import job can be fixed from the grid.</span></span> <span data-ttu-id="b235e-117">Ruudustiku veerus **Tööleht** kuvatakse vastendatud failist pärit töölehed.</span><span class="sxs-lookup"><span data-stu-id="b235e-117">The **Worksheet** column in the grid shows the worksheets from the file that was mapped.</span></span> <span data-ttu-id="b235e-118">Saate valida ripploendist erinevaid töölehti.</span><span class="sxs-lookup"><span data-stu-id="b235e-118">You can choose a different worksheet from the drop-down menu.</span></span> <span data-ttu-id="b235e-119">Kui valitud tööleht on mõne andmeprojekti üksusega juba vastendatud, palub süsteem teil muudatus kinnitada.</span><span class="sxs-lookup"><span data-stu-id="b235e-119">If the chosen worksheet is already mapped to an entity in the data project, the system asks you to confirm the change.</span></span> <span data-ttu-id="b235e-120">Soovitame teil kõik vastendused ruudustikus fikseerida.</span><span class="sxs-lookup"><span data-stu-id="b235e-120">We recommend that you fix all mappings in the grid.</span></span>

![Töölehe vastenduse värskendamine](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a><span data-ttu-id="b235e-122">Uuesti vastendamine uue failiga</span><span class="sxs-lookup"><span data-stu-id="b235e-122">Re-map to a new file</span></span>

<span data-ttu-id="b235e-123">Juhul kui andmeprojekti olemasolevate üksuste puhul tuleb üles laadida sama faili uus versioon või täiesti uus fail, peate kasutama funktsiooni **Faili lisamine** ja üksused uuesti lisama, nagu teeksite seda esimest korda.</span><span class="sxs-lookup"><span data-stu-id="b235e-123">In cases where a new version of the same file or a completely new file must be uploaded for existing entities in a data project, you must use the **Add file** experience, and add the entities again as if they were being added for the first time.</span></span> <span data-ttu-id="b235e-124">Süsteem kinnitab teie soovi enne jätkamist andmeprojekti olemasolevad üksused üle kirjutada.</span><span class="sxs-lookup"><span data-stu-id="b235e-124">The system will confirm that you want to overwrite the existing entities in the data project before proceeding.</span></span> <span data-ttu-id="b235e-125">Üksused, mida uuesti ei lisata (ülekirjutamiseks) säilitavad varasemad vasted eelmisest failist.</span><span class="sxs-lookup"><span data-stu-id="b235e-125">Entities that are not added again (or overwritten) will continue to hold the previous mappings from the previous file.</span></span>

## <a name="upload-a-file-using-run-project"></a><span data-ttu-id="b235e-126">Faili üleslaadimine suvandiga Projekti käivitamine</span><span class="sxs-lookup"><span data-stu-id="b235e-126">Upload a file using Run project</span></span>

<span data-ttu-id="b235e-127">Impordiprojekti käivitamiseks saate Exceli faili üles laadida suvandiga **Projekti käivitamine**.</span><span class="sxs-lookup"><span data-stu-id="b235e-127">You can upload an Excel file while using the **Run project** option to execute an import project.</span></span> <span data-ttu-id="b235e-128">Jälgige hoolikalt, et laadiksite üles ainult failid, millel on samad töölehed kui andmeprojekti andmeüksuste olemasolevatel vastendustel.</span><span class="sxs-lookup"><span data-stu-id="b235e-128">You must be careful to upload only files that have the same worksheets as the existing mappings on the data entities in the data project.</span></span> <span data-ttu-id="b235e-129">Kui äsja üleslaaditud failist töölehte ei leita, kuvab süsteem tõrke ja peatab importimise.</span><span class="sxs-lookup"><span data-stu-id="b235e-129">If a worksheet is not found in the newly uploaded file, the system displays an error and will stop the import.</span></span> <span data-ttu-id="b235e-130">Kui mõne üksuse puhul tuleb töölehega vastendust muuta, tuleb vastendusi andmeprojektis kõigepealt andmeprojekti sees värskendada, enne kui kasutate faili funktsioonis **Projekti käivitamine**.</span><span class="sxs-lookup"><span data-stu-id="b235e-130">If the mapping to the worksheet must be changed for an entity, then the mappings in the data project must be first updated from within the data project before using the file in the **Run project** experience.</span></span>
