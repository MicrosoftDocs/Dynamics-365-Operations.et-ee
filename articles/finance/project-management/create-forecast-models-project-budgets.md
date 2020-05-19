---
title: Eelarvemudelite loomine projektieelarvete jaoks
description: Selles teemas kirjeldatakse, kuidas luua ülejäänud eelarvete kohta eelarvemudel.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321775"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="5e403-103">Eelarvemudelite loomine projektieelarvete jaoks</span><span class="sxs-lookup"><span data-stu-id="5e403-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e403-104">Selles teemas kirjeldatakse, kuidas luua ülejäänud eelarvete kohta eelarvemudel.</span><span class="sxs-lookup"><span data-stu-id="5e403-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="5e403-105">Projekt, millele rakendub eelarve juhtimine, kasutab kahte tüüpi eelarveid: algne ja ülejäänud.</span><span class="sxs-lookup"><span data-stu-id="5e403-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="5e403-106">Projekti eelarve loomisel peate määrama algse ja ülejäänud eelarvemudelid, mis on loodud lehel **Eelarvemudelid** .</span><span class="sxs-lookup"><span data-stu-id="5e403-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="5e403-107">Määratud mudelitel põhinevad projektieelarved luuakse projekti eelarve kooskõlastamisel.</span><span class="sxs-lookup"><span data-stu-id="5e403-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="5e403-108">Eelarvemudelil, mida kasutatakse eelarve juhtimiseks, ei saa olla alammudelit ja seda ei saa kasutada alammudelina.</span><span class="sxs-lookup"><span data-stu-id="5e403-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="5e403-109">Valige **Projektihaldus ja -arvestus** > **Seadistamine** > **Eelarved**  > **Eelarvemudelid**.</span><span class="sxs-lookup"><span data-stu-id="5e403-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="5e403-110">Uue eelarvemudeli loomiseks valige **Uus** ja sisestage seejärel uue mudeli ID-kood ja selle nimi.</span><span class="sxs-lookup"><span data-stu-id="5e403-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="5e403-111">Seadke suvandi **Peatatud** väärtuseks **Jah**, et vältida eelarvemudeli eelarveridade muutusi.</span><span class="sxs-lookup"><span data-stu-id="5e403-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="5e403-112">Kui eelarveread, millega mudel on seostatud, peaks moodustama pearaamatusse likviidsuse planeerimisi, seadke suvandi **Eelarvete kaasamine likviidsuse planeerimisse** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="5e403-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="5e403-113">Kui soovite kasutada arve kuupäevana projekti kuupäeva, siis seadke suvandi **Eelarve arve kuupäev** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="5e403-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="5e403-114">Väljal **Eelarve tüüp** valige üks järgmistest mudelitüüpidest.</span><span class="sxs-lookup"><span data-stu-id="5e403-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="5e403-115">**Algne eelarve**: kasutage algsete eelarvesummade jaoks, mis kooskõlastatakse esialgse eelarve loomisel ja kinnitamisel.</span><span class="sxs-lookup"><span data-stu-id="5e403-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="5e403-116">**Ülejäänud eelarve**: kasutage ülejäänud eelarvesummadega projekti eluea kestel.</span><span class="sxs-lookup"><span data-stu-id="5e403-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="5e403-117">Selle eelarvemudeli saldosid vähendavad tegelikud kanded ja suurendavad või vähendavad eelarve revisjonid.</span><span class="sxs-lookup"><span data-stu-id="5e403-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="5e403-118">**Ülekantav**: kasutage projekti ülekantava eelarve summade puhul.</span><span class="sxs-lookup"><span data-stu-id="5e403-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="5e403-119">Ülekandmine on valikuline protsess, mida saab käivitada üle kandma kasutamata eelarvesummasid ühest finantsaastast teise.</span><span class="sxs-lookup"><span data-stu-id="5e403-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="5e403-120">Seadke järgmised suvandid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="5e403-120">Set the following options as required:</span></span>

   - <span data-ttu-id="5e403-121">Kui soovite kasutada arve kuupäevana projekti kuupäeva, siis lubage **Eelarve arve kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="5e403-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="5e403-122">Lubage poolelioleval tööl (WIP) põhineva eelarve jaoks **WIP-ga eelarve** ja seejärel valige WIP-i tüüp.</span><span class="sxs-lookup"><span data-stu-id="5e403-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="5e403-123">Suvandi **Eelarve tüüp** vaikesätteks saate jätta **Puudub** või sisestada uue tüübi.</span><span class="sxs-lookup"><span data-stu-id="5e403-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="5e403-124">Pärast kirje muutmist ei saa eelarve tüüpi muuta.</span><span class="sxs-lookup"><span data-stu-id="5e403-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="5e403-125">Kui muudate eelarve tüübi vaikesätet, siis muutuvad kõik muud suvandid uuendustele suletuks ja te ei saa seda eelarvemudelit uuesti kasutada.</span><span class="sxs-lookup"><span data-stu-id="5e403-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

