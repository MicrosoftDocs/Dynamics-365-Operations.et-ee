---
title: Kulutüüpide seadistamine
description: Selles teemas selgitatakse kulutüüpide seadistamist jaotises Vara rentimine.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseExpenseTypeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a1d6667a7c6fe1cd44196f2e753ca72b2ca97649
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880980"
---
# <a name="set-up-expense-types"></a><span data-ttu-id="d441b-103">Kulutüüpide seadistamine</span><span class="sxs-lookup"><span data-stu-id="d441b-103">Set up expense types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d441b-104">Selles teemas selgitatakse kulutüüpide seadistamist jaotises Vara rentimine.</span><span class="sxs-lookup"><span data-stu-id="d441b-104">This topic explains how to set up expense types in Asset leasing.</span></span> <span data-ttu-id="d441b-105">Kulusid, mida maksegraafik ei esinda, nimetatakse *kuluhindadeks*.</span><span class="sxs-lookup"><span data-stu-id="d441b-105">Costs that aren't represented by the payment schedule are known as *expense costs*.</span></span> <span data-ttu-id="d441b-106">Nende kulude näidete hulka kuuluvad kinnisvaramaksud, ühiste pindade hoolduskulud ja kindlustuskulud.</span><span class="sxs-lookup"><span data-stu-id="d441b-106">Examples of these costs include property taxes, common area maintenance costs, and insurance expenses.</span></span>

## <a name="add-an-administrative-expense-type"></a><span data-ttu-id="d441b-107">Halduskulu tüübi lisamine</span><span class="sxs-lookup"><span data-stu-id="d441b-107">Add an administrative expense type</span></span>

1. <span data-ttu-id="d441b-108">Avage **Vara rentimine \> Seadistus \> Kulutüübid**.</span><span class="sxs-lookup"><span data-stu-id="d441b-108">Go to **Asset leasing \> Setup \> Expense types**.</span></span>
2. <span data-ttu-id="d441b-109">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d441b-109">Select **New**.</span></span>
3. <span data-ttu-id="d441b-110">Sisestage vastavatele väljadele uus kulutüüp ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="d441b-110">In the appropriate fields, enter the new expense type and a description.</span></span>

## <a name="assign-accounts-to-administrative-costs"></a><span data-ttu-id="d441b-111">Määrake halduskuludele kontod</span><span class="sxs-lookup"><span data-stu-id="d441b-111">Assign accounts to administrative costs</span></span>

<span data-ttu-id="d441b-112">Järgmisena peaksite seostama kontod kulutüüpidega.</span><span class="sxs-lookup"><span data-stu-id="d441b-112">Next, you should associate accounts with the expense types.</span></span> <span data-ttu-id="d441b-113">Need kontod debiteeritakse siis, kui kulude graafiku kirjed sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="d441b-113">These accounts will be debited when expense schedule entries are posted.</span></span> <span data-ttu-id="d441b-114">Vastaskonto on määratud iga rendi ridadele **Täitekulude maksegraafik**.</span><span class="sxs-lookup"><span data-stu-id="d441b-114">The offset account is specified on the **Executory costs payment schedule** lines on each lease.</span></span>

1. <span data-ttu-id="d441b-115">Avage **Vara rentimine \> Seadistus \> Vara rentimise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="d441b-115">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="d441b-116">Valige kulutüüp vahekaardi **Kontod** kiirkaardi **Täitekulud** väljal **Kulu tüüp**.</span><span class="sxs-lookup"><span data-stu-id="d441b-116">On the **Accounts** tab, on the **Executory costs** FastTab, in the **Expense type** field, select the expense type.</span></span>
3. <span data-ttu-id="d441b-117">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d441b-117">Select **Add**.</span></span>
4. <span data-ttu-id="d441b-118">Valige väljal **Raamatu tüüp** raamatu tüüp halduskuludega sidumiseks.</span><span class="sxs-lookup"><span data-stu-id="d441b-118">In the **Book type** field, select the book type to link to the administrative costs.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d441b-119">Sama kulukontoga võib siduda mitu raamatu tüüpi.</span><span class="sxs-lookup"><span data-stu-id="d441b-119">Multiple book types can be linked to the same expense account.</span></span>

5. <span data-ttu-id="d441b-120">Määratlega väljal **Konto kood**, millistele rentidele raamat peaks kohalduma.</span><span class="sxs-lookup"><span data-stu-id="d441b-120">In the **Account code** field, specify which leases the book should be applied to:</span></span>

    - <span data-ttu-id="d441b-121">**Kõik** – kohalda raamatut kõigile rentidele.</span><span class="sxs-lookup"><span data-stu-id="d441b-121">**All** – Apply the book to all leases.</span></span>
    - <span data-ttu-id="d441b-122">**Grupp** – kohalda raamatud konkreetsele rentide grupile.</span><span class="sxs-lookup"><span data-stu-id="d441b-122">**Group** – Apply the book to a specific group of leases.</span></span>
    - <span data-ttu-id="d441b-123">**Tabel** – kohalda raamatut konkreetsetele rentidele.</span><span class="sxs-lookup"><span data-stu-id="d441b-123">**Table** – Apply the book to specific leases.</span></span>

6. <span data-ttu-id="d441b-124">Kui valisite väljal **Konto kood** suvandi **Grupp** või **Tabel**, siis valige väljal **Konto/grupi number** konto number või grupi number.</span><span class="sxs-lookup"><span data-stu-id="d441b-124">If you selected **Group** or **Table** in the **Account code** field, select an account number or group number in the **Account/Group number** field.</span></span>
7. <span data-ttu-id="d441b-125">Valige vastavatel väljadel kapitalirendi põhikonto ja kasutusrendi põhikonto.</span><span class="sxs-lookup"><span data-stu-id="d441b-125">In the appropriate fields, select the finance lease main account and the operating lease main account.</span></span>

<span data-ttu-id="d441b-126">Kui olete need sammud lõpule viinud, saate valitud rendi lehe **Rendi üksikasjad** ridade **Täitekulude maksegraafik** kaudu kulusid lisada.</span><span class="sxs-lookup"><span data-stu-id="d441b-126">When you've completed these steps, you can add expenses through the **Executory costs payment schedule** lines on the **Lease details** page of a selected lease.</span></span> <span data-ttu-id="d441b-127">Teise võimalusena saate lisada kulusid uue rendilepingu loomisel.</span><span class="sxs-lookup"><span data-stu-id="d441b-127">Alternatively, you can add expenses when you create a new lease.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
