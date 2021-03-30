---
title: Allettevõte andmete eksportimine faili
description: See teema kirjeldab, kuidas valmistuda andmete eksportimiseks rakendusest Microsoft Dynamics 365 Finance ja seejärel importida need konsolideeritud juriidilisse isikusse.
author: jinniew
manager: AnnBe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 33c17cc2c1dcaa57244bf0bfaa661b11b221e2f6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205495"
---
# <a name="export-subsidiary-data-to-files"></a><span data-ttu-id="f809d-103">Allettevõte andmete eksportimine faili</span><span class="sxs-lookup"><span data-stu-id="f809d-103">Export subsidiary data to files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f809d-104">Kasutage lehte **Eksport** (**Süsteemihaldus \> Tööruumid \> Import/Eksport**), et valmistada allandmete eksportimiseks failidesse, mida saab seejärel importida konsolideeritud juriidilisse isikusse.</span><span class="sxs-lookup"><span data-stu-id="f809d-104">You use the **Export** page (**System administration \> Workspaces \> Import/Export**) to prepare to export subsidiary data to files that can then be imported into a consolidated legal entity.</span></span> <span data-ttu-id="f809d-105">Lisateavet importimise ja eksportimise kohta leiate jaotisest [Andmete importimis- ja eksportimistööde ülevaade](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="f809d-105">For more information about the import and export processes, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>

1. <span data-ttu-id="f809d-106">Juriidilise isiku loomine konsolideerimisprotsessiks.</span><span class="sxs-lookup"><span data-stu-id="f809d-106">Create a legal entity for the consolidation process.</span></span> <span data-ttu-id="f809d-107">Lisateavet juriidiliste isikute loomise kohta leiate jaotisest [Juriidilise isiku loomine](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span><span class="sxs-lookup"><span data-stu-id="f809d-107">For information about how to create legal entities, see [Create a legal entity](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span></span> <span data-ttu-id="f809d-108">Lisateavet leiate jaotisest [Juriidilise isiku ettevalmistamine konsolideerimisprotsessis kasutamiseks](prepare-company-for-consolidation.md) ja [Allettevõtte juriidilise isiku seadistamine konsolideerimiseks](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="f809d-108">For more information, see [Prepare a legal entity for use in the consolidation process](prepare-company-for-consolidation.md) and [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span> 

2. <span data-ttu-id="f809d-109">Avage **Konsolideerimised \> Ekspordi ettevõtte saldod**.</span><span class="sxs-lookup"><span data-stu-id="f809d-109">Go to **Consolidations \> Export company balances**.</span></span> <span data-ttu-id="f809d-110">Määratlege lehe **Ekspordi ettevõtte saldod** vahekaardil **Kriteeriumid** konsolideerimise üksikasjad, seadistades järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="f809d-110">On the **Export company balances** page, on the **Criteria** tab, specify the details of the consolidation by setting the following fields.</span></span>

    | <span data-ttu-id="f809d-111">Field</span><span class="sxs-lookup"><span data-stu-id="f809d-111">Field</span></span>                             | <span data-ttu-id="f809d-112">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="f809d-112">Description</span></span> |
    |-----------------------------------|-------|
    | <span data-ttu-id="f809d-113">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="f809d-113">Main account</span></span>                      | <span data-ttu-id="f809d-114">Määrake konsolideeridavad kontod.</span><span class="sxs-lookup"><span data-stu-id="f809d-114">Specify the accounts to consolidate.</span></span> <span data-ttu-id="f809d-115">Kõikide kontode kaasamiseks jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="f809d-115">To include all accounts, leave this field blank.</span></span> |
    | <span data-ttu-id="f809d-116">Konsolideerimiskonto kasutamine</span><span class="sxs-lookup"><span data-stu-id="f809d-116">Use consolidation account</span></span>         | <span data-ttu-id="f809d-117">Kui olete konsolideerimiskontod määranud, määrake selle valiku väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="f809d-117">If you've specified consolidation accounts, set this option to **Yes**.</span></span> |
    | <span data-ttu-id="f809d-118">Vali konsolideerimiskonto asukohast</span><span class="sxs-lookup"><span data-stu-id="f809d-118">Select consolidation account from</span></span> | <span data-ttu-id="f809d-119">Valige kas **Põhikonto** või **Konsolideerimiskontode grupp**.</span><span class="sxs-lookup"><span data-stu-id="f809d-119">Select either **Main account** or **Consolidation account group**.</span></span> |
    | <span data-ttu-id="f809d-120">Konsolideerimiskonto grupp</span><span class="sxs-lookup"><span data-stu-id="f809d-120">Consolidation account group</span></span>       | <span data-ttu-id="f809d-121">Valige konsolideerimiskontode grupp valitud konsolideerimiskontole.</span><span class="sxs-lookup"><span data-stu-id="f809d-121">Select a consolidation account group for the consolidation account that you selected.</span></span> |
    | <span data-ttu-id="f809d-122">Konsolideerimisperiood</span><span class="sxs-lookup"><span data-stu-id="f809d-122">Consolidation period</span></span>              | <span data-ttu-id="f809d-123">Määratlege konsolideerimise kuupäevad "alates" ja "kuni".</span><span class="sxs-lookup"><span data-stu-id="f809d-123">Specify "from" and "to" dates for the consolidation.</span></span> |
    | <span data-ttu-id="f809d-124">Tegelike summade kaasamine</span><span class="sxs-lookup"><span data-stu-id="f809d-124">Include actual amounts</span></span>            | <span data-ttu-id="f809d-125">Tegelike summade kaasamist seadistage see suvand väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="f809d-125">Set this option to **Yes** to include actual amounts.</span></span> |
    | <span data-ttu-id="f809d-126">Eelarvesummade kaasamine</span><span class="sxs-lookup"><span data-stu-id="f809d-126">Include budget amounts</span></span>            | <span data-ttu-id="f809d-127">Eelarvesummade konsolideerimisse kaasamiseks seadistage see suvand väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="f809d-127">Set this option to **Yes** to include budget amounts in consolidations.</span></span> |
    | <span data-ttu-id="f809d-128">Eelarvemudelid</span><span class="sxs-lookup"><span data-stu-id="f809d-128">Budget models</span></span>                     | <span data-ttu-id="f809d-129">Määrake kaasatav eelarvemudel.</span><span class="sxs-lookup"><span data-stu-id="f809d-129">Specify the budget model to include.</span></span> |

3. <span data-ttu-id="f809d-130">Vahekaardil **Finantsdimensioonid** määratlege konsolideerimise üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="f809d-130">On the **Financial dimensions** tab, specify the details of the consolidation:</span></span>

    - <span data-ttu-id="f809d-131">Määratlege finantsdimensiooni teave, mis tuleks kanda tütarettevõtte kontode kannetest üle konsolideeritud juriidilise üksuse kannetesse.</span><span class="sxs-lookup"><span data-stu-id="f809d-131">Specify the financial dimension information that should be transferred from the transactions in the subsidiary accounts to the transactions in the consolidated legal entity.</span></span>
    - <span data-ttu-id="f809d-132">Valige finantsdimensioonid loendist.</span><span class="sxs-lookup"><span data-stu-id="f809d-132">Select financial dimensions in the list.</span></span>
    - <span data-ttu-id="f809d-133">Tuvastage iga konsolideeritud finantsdimensiooni jaoks õige spetsifikatsioon.</span><span class="sxs-lookup"><span data-stu-id="f809d-133">Identify the correct specification for each financial dimension that is consolidated.</span></span> <span data-ttu-id="f809d-134">Saadaval on valikud **Dimensioon**, **Grupi dimensioon**, **Ettevõtte kontod** ja **Konto**.</span><span class="sxs-lookup"><span data-stu-id="f809d-134">The available options include **Dimension**, **Group dimension**, **Company accounts**, and **Account**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="f809d-135">Suvand **Grupidimensiooni** võimaldab teil määratleda dimensiooniväärtuse, mida konsolideeritavate ettevõtete grupp kasutab.</span><span class="sxs-lookup"><span data-stu-id="f809d-135">The **Group dimension** option lets you define the dimension value that is used by the group of companies that is being consolidated.</span></span>

    - <span data-ttu-id="f809d-136">Määrake segmendijärjestus, milles konsolideerida.</span><span class="sxs-lookup"><span data-stu-id="f809d-136">Specify the segment order to consolidate in.</span></span>

4. <span data-ttu-id="f809d-137">Järgige vahekaardil **Juriidilised isikud** näid samme, et määratleda juriidiline isik, keda ekspordite.</span><span class="sxs-lookup"><span data-stu-id="f809d-137">On the **Legal entities** tab, follow these steps to specify the legal entity that you're exporting:</span></span>

    1. <span data-ttu-id="f809d-138">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f809d-138">Select **New**.</span></span>
    2. <span data-ttu-id="f809d-139">Sisestage juriidiline isik väljale **Algne juriidiline isik**.</span><span class="sxs-lookup"><span data-stu-id="f809d-139">In the **Source legal entity** field, enter the legal entity.</span></span>

        <span data-ttu-id="f809d-140">Kui samad kriteeriumid kehtivad mitmetele tütarettevõtetele, mis on samas andmebaasis, saate nende tütarettevõtete andmed ühe toiminguga eraldi ekspordifailidesse üle kanda.</span><span class="sxs-lookup"><span data-stu-id="f809d-140">If the same criteria apply to several subsidiaries that are in the same database, you can transfer data from those subsidiaries to separate export files in a single operation:</span></span>

        1. <span data-ttu-id="f809d-141">Looge rida iga tütarettevõttest juriidilisele isiku jaoks, kelle kontod eksporditakse failidesse.</span><span class="sxs-lookup"><span data-stu-id="f809d-141">Create a line for each subsidiary legal entity for which accounts should be exported to files.</span></span> <span data-ttu-id="f809d-142">Need failid imporditakse hiljem konsolideeritud juriidilisele isikule.</span><span class="sxs-lookup"><span data-stu-id="f809d-142">These files will be imported into the consolidated legal entity later.</span></span>
        2. <span data-ttu-id="f809d-143">Sisestage iga allettevõtte jaoks allettevõtte nimi ja ekspordifaili nimi, mis luuakse eksporditöö jooksul.</span><span class="sxs-lookup"><span data-stu-id="f809d-143">For each subsidiary, enter the subsidiary name and the name of the export file that will be created during the export job.</span></span>

    3. <span data-ttu-id="f809d-144">Valige väljal **Teisenduserinevuste kontotüüp** suvand **Kasum ja kahjum** või **Bilanss**.</span><span class="sxs-lookup"><span data-stu-id="f809d-144">In **Account type of conversion differences** field, Select **Profit and loss** or **Balance sheet**.</span></span>
    4. <span data-ttu-id="f809d-145">Sisestage faili nimi loodava ekspordifaili jaoks.</span><span class="sxs-lookup"><span data-stu-id="f809d-145">Enter a file name for the export file that will be created.</span></span>

5. <span data-ttu-id="f809d-146">Ekspordi käivitamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="f809d-146">Select **OK** to run the export.</span></span>

<span data-ttu-id="f809d-147">Kui eksport on lõpetatud, saate sõnumi, mis loetleb kirjete arvu, mis igasse faili salvestati.</span><span class="sxs-lookup"><span data-stu-id="f809d-147">When the export is completed, you receive a message that shows the number of records that were saved in each file.</span></span> <span data-ttu-id="f809d-148">Seejärel saate importida failid konsolideeritud juriidilisele isikule.</span><span class="sxs-lookup"><span data-stu-id="f809d-148">You can then import the files into the consolidated legal entity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]