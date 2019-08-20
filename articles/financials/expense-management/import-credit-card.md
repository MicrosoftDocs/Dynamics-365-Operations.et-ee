---
title: Krediitkaardikannete importimine ja haldamine
description: Selles teemas kirjeldatakse kuludega seotud krediitkaardikannete importimist ja haldamist. Neid kandeid saab seadistada nii, et need imporditakse automaatselt korduva graafiku alusel või neid saab vajaduse järgi käsitsi importida.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4484ea6fa446c73b8854e7822237bb3c6b9f9023
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840933"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="a40d6-104">Krediitkaardikannete importimine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="a40d6-104">Import and maintain credit card transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a40d6-105">Kuludega seotud krediitkaardikandeid saab seadistada nii, et neid imporditakse automaatselt korduva graafiku alusel.</span><span class="sxs-lookup"><span data-stu-id="a40d6-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="a40d6-106">Teise võimalusena saab kandeid vajaduse järgi käsitsi importida.</span><span class="sxs-lookup"><span data-stu-id="a40d6-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="a40d6-107">Krediitkaardikanded imporditakse krediitkaardikannete andmeüksuse kaudu.</span><span class="sxs-lookup"><span data-stu-id="a40d6-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="a40d6-108">Andmeüksuste kohta leiate lisateavet jaotisest [Andmeüksused](../../dev-itpro/data-entities/data-entities.md).</span><span class="sxs-lookup"><span data-stu-id="a40d6-108">For more information about data entities, see [Data entities](../../dev-itpro/data-entities/data-entities.md).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="a40d6-109">Saate importida krediitkaardikanded.</span><span class="sxs-lookup"><span data-stu-id="a40d6-109">Import credit card transactions</span></span>

1. <span data-ttu-id="a40d6-110">Tehke lehel **Krediitkaardikanded** valik **Kannete importimine**.</span><span class="sxs-lookup"><span data-stu-id="a40d6-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="a40d6-111">Kui avate andmehalduse esimest korda, peab süsteem andmeüksuste loendi värskendama, enne kui jätkata saate.</span><span class="sxs-lookup"><span data-stu-id="a40d6-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="a40d6-112">Sisestage väljale **Nimi** imporditöö kordumatu kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="a40d6-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="a40d6-113">Valige väljalt **Lähteandmete vorming** imporditavaid krediitkaardikandeid sisaldava faili vorming.</span><span class="sxs-lookup"><span data-stu-id="a40d6-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="a40d6-114">Valige **Laadi üles** ja otsige siis üles ja valige imporditav fail.</span><span class="sxs-lookup"><span data-stu-id="a40d6-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="a40d6-115">Kui fail on üles laaditud, siis valideerige krediitkaardikande faili vastendus ja krediitkaardi kannete andmeüksuse veerud, valides paanilt lingi **Kuva kaart**.</span><span class="sxs-lookup"><span data-stu-id="a40d6-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="a40d6-116">Kui ilmneb vastendamistõrkeid või kui vastendust on vaja muuta, siis tehke vastendamise muudatused vahekaardilt **Vastendamise visualiseering** või vahekaardilt **Vastendamise üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="a40d6-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="a40d6-117">Krediitkaardikannete automatiseerimiseks valige **Korduva andmetöö loomine**.</span><span class="sxs-lookup"><span data-stu-id="a40d6-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="a40d6-118">Siis saate määrata kordumise, mis määratleb, kui sageli krediitkaardikandeid tuleks importida.</span><span class="sxs-lookup"><span data-stu-id="a40d6-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="a40d6-119">Kui olete lõpetanud, valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="a40d6-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="a40d6-120">Valitud faili kohe importimiseks valige **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="a40d6-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="a40d6-121">Kui importimise ajal tekib tõrge, saate vaadata käivituslogi või koondatud andmeid, et näha, milliseid vigu on vaja eduka importimise tagamiseks parandada.</span><span class="sxs-lookup"><span data-stu-id="a40d6-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="a40d6-122">Kui importida on vaja mitut failivormingut, tuleb luua igale vormingu tüübile eraldi imporditööd.</span><span class="sxs-lookup"><span data-stu-id="a40d6-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="a40d6-123">Lõpetatud töötajate krediitkaardikannete ümbermääramine</span><span class="sxs-lookup"><span data-stu-id="a40d6-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="a40d6-124">Pärast töötaja kirje lõpetamist keelatakse töötaja Active Directory domeeniteenuste (ADDS) konto.</span><span class="sxs-lookup"><span data-stu-id="a40d6-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="a40d6-125">Kuid võib olla aktiivseid krediitkaardikandeid, mis tuleb siiski kuludesse kanda ja korvata.</span><span class="sxs-lookup"><span data-stu-id="a40d6-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="a40d6-126">Lehelt **Krediitkaardikanded** saate määrata töötaja ümber mis tahes krediitkaardikandele, kus seostatud töötaja on lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="a40d6-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="a40d6-127">Valige vähemalt üks krediitkaardikanne ja seejärel **Kannete ümbermääramine**.</span><span class="sxs-lookup"><span data-stu-id="a40d6-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="a40d6-128">Seejärel saate valida teise töötaja, kellele krediitkaardikanded määrata.</span><span class="sxs-lookup"><span data-stu-id="a40d6-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="a40d6-129">Pärast nende krediitkaardikannete ümbermääramist saab need kuluaruande jaoks valida ja tasuda tavalise kuluaruande korvamise protsessi kaudu.</span><span class="sxs-lookup"><span data-stu-id="a40d6-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
