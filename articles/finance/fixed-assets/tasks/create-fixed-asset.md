---
title: Uue põhivara loomine
description: Selles teemas selgitatakse, kuidas luua uut põhivara kirjet loendilehel Põhivara.
author: moaamer
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bbbafb1732a9628cb90ad284fce224e3d8172afd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227036"
---
# <a name="create-a-fixed-asset"></a><span data-ttu-id="67ef3-103">Uue põhivara loomine</span><span class="sxs-lookup"><span data-stu-id="67ef3-103">Create a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="67ef3-104">Selles teemas selgitatakse, kuidas luua uut põhivara kirjet loendilehel **Põhivara**.</span><span class="sxs-lookup"><span data-stu-id="67ef3-104">This topic explains how to create a new fixed asset record from the **Fixed asset** list page.</span></span>

<span data-ttu-id="67ef3-105">Süsteem määrab vara numbri põhivara grupile määratud numbriseeria põhjal.</span><span class="sxs-lookup"><span data-stu-id="67ef3-105">The system assigns the asset number, based on the number sequence that is assigned to the fixed asset group.</span></span> <span data-ttu-id="67ef3-106">Kui kasutate põhivara malli varade importimiseks Microsoft Exceli lisandmooduli kaudu või kui kasutate mõnda muud imporditööd, loob süsteem automaatselt põhivara kirjed ja suurendab vara numbrit.</span><span class="sxs-lookup"><span data-stu-id="67ef3-106">If you use the fixed asset template to import assets via the Microsoft Excel add-in, or if you use another import job, the system automatically creates fixed asset records and increments the asset number.</span></span>

<span data-ttu-id="67ef3-107">Vara kirje käsitsi loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="67ef3-107">To manually create an asset record, follow these steps.</span></span>

1. <span data-ttu-id="67ef3-108">Avage **Navigeerimispaan \> Moodulid \> Põhivarad \> Põhivarad \> Põhivarad**.</span><span class="sxs-lookup"><span data-stu-id="67ef3-108">Go to **Navigation pane \> Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="67ef3-109">Valige **Toimingupaanil** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="67ef3-109">On the **Action pane**, select **New**.</span></span>
3. <span data-ttu-id="67ef3-110">Väljale **Põhivara grupp** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="67ef3-110">In **the Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="67ef3-111">Väli **Arv** on vaikimisi, kui olete lubanud valikud **Nummerda põhivarade funktsioonid automaatselt**, **Põhivarade parameetrid** ja **Põhivara grupp**.</span><span class="sxs-lookup"><span data-stu-id="67ef3-111">The **Number** field will default if you have enabled **Autonumber fixed assets functionality** in the **Fixed assets parameters** and the **Fixed asset group**.</span></span> <span data-ttu-id="67ef3-112">Kui te seda teinud pole, sisestage põhivara tuvastamiseks kordumatu number.</span><span class="sxs-lookup"><span data-stu-id="67ef3-112">If not, you must enter a unique number to identify the fixed asset.</span></span>
4. <span data-ttu-id="67ef3-113">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="67ef3-113">In the **Name** field, enter a value.</span></span> <span data-ttu-id="67ef3-114">Sisestage lisateave, mida teie ettevõte selle vara puhul vajab.</span><span class="sxs-lookup"><span data-stu-id="67ef3-114">Enter the additional information that your business needs for this asset.</span></span>
5. <span data-ttu-id="67ef3-115">Valige **Toimingupaanil** suvand **Raamatud**.</span><span class="sxs-lookup"><span data-stu-id="67ef3-115">On the **Action pane**, select **Books**.</span></span>
6. <span data-ttu-id="67ef3-116">Väljale **Soetamiskuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="67ef3-116">In the **Acquisition date** field, enter a date.</span></span>
7. <span data-ttu-id="67ef3-117">Väljale **Soetusmaksumus** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="67ef3-117">In the **Acquisition price** field, enter a number.</span></span>

    - <span data-ttu-id="67ef3-118">Sisestage lisateave, mida teie ettevõte selle raamatu puhul vajab.</span><span class="sxs-lookup"><span data-stu-id="67ef3-118">Enter the additional information that your business needs for this book.</span></span>
    - <span data-ttu-id="67ef3-119">Sisestage täiendav teave, mida teie ettevõte ülejäänud raamatute jaoks vajab.</span><span class="sxs-lookup"><span data-stu-id="67ef3-119">Enter the additional information that your business needs for the remaining books.</span></span>

8. <span data-ttu-id="67ef3-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="67ef3-120">Close the page.</span></span>

<span data-ttu-id="67ef3-121">Põhivarasid saate importida ka Exceli lisandmooduli abil või käivitades imporditöö tööruumis **Andmehaldus**.</span><span class="sxs-lookup"><span data-stu-id="67ef3-121">You can also import fixed assets by using the Excel add-in or by running an import job from the **Data management** workspace.</span></span> <span data-ttu-id="67ef3-122">Enne impordi käivitamist sisestage malli nõutavate väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="67ef3-122">Before you run the import, enter the values for required fields in the template.</span></span>

<span data-ttu-id="67ef3-123">Kui te ei määratlenud põhivara numbrit Exceli lisandmooduli mallis või tööruumis Andmehaldus, loob süsteem iga imporditud vara jaoks põhivara numbri ja suurendab automaatselt iga üksuse numbriseeriat.</span><span class="sxs-lookup"><span data-stu-id="67ef3-123">If you didn't define the fixed asset number in the template of the Excel add-in, or in Data management, the system creates a fixed asset number for each imported asset and automatically increments the number sequence for each.</span></span> <span data-ttu-id="67ef3-124">Kuid kui impordite varad ja määratlete varade numbrid mallis, **ei** suurenda süsteem numbriseeriat automaatselt.</span><span class="sxs-lookup"><span data-stu-id="67ef3-124">However, if you import assets and define asset numbers in the template, the system does **not** automatically increment the number sequence.</span></span> <span data-ttu-id="67ef3-125">Sellisel juhul peab administraator numbriseeriat käsitsi uuendama.</span><span class="sxs-lookup"><span data-stu-id="67ef3-125">In this case, an admin might have to manually update the number sequence.</span></span> <span data-ttu-id="67ef3-126">Kui määratlete põhivara numbri Exceli lisandmooduli mallis, kasutab süsteem määratletud põhivara numbrit ja suurendab numbriseeriat.</span><span class="sxs-lookup"><span data-stu-id="67ef3-126">If you defined the fixed asset number in the template of the Excel add-in, the system uses the defined fixed asset number and increments the number sequence.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="67ef3-127">Pärast kulumi sisestamist väljad **Teenusesse saadetud** ja **Amortiseerimise algus** lukustatakse lehel **Raamat**.</span><span class="sxs-lookup"><span data-stu-id="67ef3-127">After posting the depreciation, the **Placed in service** and **Depreciation run date** fields will be locked on the **Book** page.</span></span> <span data-ttu-id="67ef3-128">Samuti ei uuendata kumbagi välja andmeüksusest.</span><span class="sxs-lookup"><span data-stu-id="67ef3-128">Also, both neither field will be updated from the data entity.</span></span>

> [!WARNING]
> <span data-ttu-id="67ef3-129">Põhivara kirjet ei kustutata, kui kanded sisestati seotud raamatusse või kui vastloodud põhivara sisestatakse töölehe reale, kuid ei sisestata.</span><span class="sxs-lookup"><span data-stu-id="67ef3-129">The fixed asset record won't be deleted if transactions were posted to the associated book, or if the newly created fixed asset is entered on a journal line but not posted.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]