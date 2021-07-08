---
title: Global Inventory Accounting pearaamat
description: Selles teemas kirjeldatakse Global Inventory Accounting pearaamatuid, mis on määratletud valuuta, kalendri, reegli ja juriidilise isikuga seose kombinatsiooniga.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea3434675aa3b7f2304be93ef9b489747994fa9d
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273142"
---
# <a name="global-inventory-accounting-ledger"></a><span data-ttu-id="e1b34-103">Global Inventory Accounting pearaamat</span><span class="sxs-lookup"><span data-stu-id="e1b34-103">Global Inventory Accounting ledger</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="e1b34-104">Global Inventory Accounting laoarvestusel on oma pearaamatute kogum.</span><span class="sxs-lookup"><span data-stu-id="e1b34-104">Global Inventory Accounting has its own set of ledgers.</span></span> <span data-ttu-id="e1b34-105">Iga kord, kui asjaomase juriidilise isiku jaoks töödeldakse varudega seotud kannet, saab süsteem seda kannet vastavalt vajadusele arvestada mis tahes arvuga Global Inventory Accounting pearaamatutes.</span><span class="sxs-lookup"><span data-stu-id="e1b34-105">Each time an inventory-related transaction is processed for a relevant legal entity, the system can account for that transaction in any number of Global Inventory Accounting ledgers, as required.</span></span>

<span data-ttu-id="e1b34-106">Pearaamat on deebet- ja kreeditmõõdikute register.</span><span class="sxs-lookup"><span data-stu-id="e1b34-106">A ledger is a register of debit and credit measures.</span></span> <span data-ttu-id="e1b34-107">Need meetmed liigitatakse kuluelementide ja alampearaamatu kontode abil.</span><span class="sxs-lookup"><span data-stu-id="e1b34-107">These measures are classified by using cost elements and subledger accounts.</span></span> <span data-ttu-id="e1b34-108">Global Inventory Accounting pearaamat määratletakse valuuta, kalendri, reegli ja juriidilise isikuga seose kombinatsiooniga.</span><span class="sxs-lookup"><span data-stu-id="e1b34-108">A Global Inventory Accounting ledger is defined by its combination of a currency, a calendar, a convention, and an association with a legal entity.</span></span>

<span data-ttu-id="e1b34-109">Global Inventory Accounting pearaamatute seadistamiseks minge **Globaalse laoarvestus \>Seadistustamine \>Globaalse laoarvestuse pearaamat**.</span><span class="sxs-lookup"><span data-stu-id="e1b34-109">To set up your Global Inventory Accounting ledgers, go to **Global inventory accounting \> Setup \> Global inventory accounting ledgers**.</span></span> <span data-ttu-id="e1b34-110">Määrake igale pearaamatule järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="e1b34-110">For each ledger, set the following fields:</span></span>

- <span data-ttu-id="e1b34-111">**Nimi** – sisestage pearaamatu nimi.</span><span class="sxs-lookup"><span data-stu-id="e1b34-111">**Name** – Enter the name of the ledger.</span></span>
- <span data-ttu-id="e1b34-112">**Kirjeldus** – sisestage pearaamatu kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="e1b34-112">**Description** – Enter a description of the ledger.</span></span>
- <span data-ttu-id="e1b34-113">**Rahanduskalender** – määrake pearaamatu rahanduskalender.</span><span class="sxs-lookup"><span data-stu-id="e1b34-113">**Fiscal calendar** – Specify the fiscal calendar for the ledger.</span></span>
- <span data-ttu-id="e1b34-114">**Valuuta ja vahetuskursi liik** – kasutage selle kiirkaardi välju, et valida pearaamatu kasutatav arvestusvaluuta ja vahetuskursi liik.</span><span class="sxs-lookup"><span data-stu-id="e1b34-114">**Currency and exchange rate type** – Use the fields on this FastTab to select the accounting currency that the ledger uses, and the exchange rate type.</span></span> <span data-ttu-id="e1b34-115">Valitud valuuta võib erineda valuutast, mida juriidiline isik kasutab.</span><span class="sxs-lookup"><span data-stu-id="e1b34-115">The currency that you select can differ from the currency that the legal entity uses.</span></span> <span data-ttu-id="e1b34-116">Global Inventory Accounting laoarvestuses saavad kasutajad määratleda suvalise arvu kuluarvestusandmikke.</span><span class="sxs-lookup"><span data-stu-id="e1b34-116">In Global Inventory Accounting, users can define as many costing ledgers as they require.</span></span> <span data-ttu-id="e1b34-117">Global Inventory Accounting laoarvestus toetab laoarvestust mitmes valuutas ja mitmes hindamises.</span><span class="sxs-lookup"><span data-stu-id="e1b34-117">Global Inventory Accounting supports inventory accounting in multiple currencies and in multiple valuations.</span></span> <span data-ttu-id="e1b34-118">Seadistage järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="e1b34-118">Set the following fields:</span></span>

    - <span data-ttu-id="e1b34-119">**Valuuta** – valige kuluarvestuse valuuta, milles varudega seotud väärtusi hoitakse.</span><span class="sxs-lookup"><span data-stu-id="e1b34-119">**Currency** – Select the costing currency that inventory-related values are maintained in.</span></span> <span data-ttu-id="e1b34-120">Need väärtused hõlmavad laoväärtust, müüdud kaupade maksumust, transiitvarusid ja igat liiki hälbeid.</span><span class="sxs-lookup"><span data-stu-id="e1b34-120">These values include the inventory value, cost of goods sold, inventory in transit, and all kinds of variance.</span></span>
    - <span data-ttu-id="e1b34-121">**Vahetuskursi tüüp** – valige vahetuskurss, mida süsteem peaks kasutama kandesumma ja kaupade standardkulu teisendamiseks kuluarvestuse valuutasse.</span><span class="sxs-lookup"><span data-stu-id="e1b34-121">**Exchange rate type** – Select the exchange rate that the system should use to convert the transaction amount in the transaction currency and the standard cost of the items into the costing currency.</span></span>

- <span data-ttu-id="e1b34-122">**Reegli nimi** – määrake reegel.</span><span class="sxs-lookup"><span data-stu-id="e1b34-122">**Convention name** – Specify a convention.</span></span> <span data-ttu-id="e1b34-123">Reegel on poliitikate kogum, mis määrab, kuidas kulusid selles pearaamatus arvestatakse.</span><span class="sxs-lookup"><span data-stu-id="e1b34-123">A convention is a collection of policies that establish how costs will be accounted in this ledger.</span></span>
- <span data-ttu-id="e1b34-124">**Juriidiline isik** – pearaamat kajastab valitud juriidilisele isikule sisestatud dokumente.</span><span class="sxs-lookup"><span data-stu-id="e1b34-124">**Legal entity** – The ledger will account the documents that are posted to the selected legal entity.</span></span>
- <span data-ttu-id="e1b34-125">**Ettevalmistamine** – saate valida, kas enne pearaamatu loomist loodud laokandeid tuleks töödelda vastavalt pearaamatu valuutale ja konventsioonile.</span><span class="sxs-lookup"><span data-stu-id="e1b34-125">**Priming** – Select whether inventory transactions that were created before the ledger was created should be processed according to the currency and convention in the ledger.</span></span> <span data-ttu-id="e1b34-126">Valige üks järgmistest väärtustest.</span><span class="sxs-lookup"><span data-stu-id="e1b34-126">Select one of the following values:</span></span>

    - <span data-ttu-id="e1b34-127">**Aktiveeritud** – pearaamat peaks töötlema kandeid, mis loodi enne pearaamatu loomist.</span><span class="sxs-lookup"><span data-stu-id="e1b34-127">**Activated** – The ledger should process transactions that were created before the ledger was created.</span></span>
    - <span data-ttu-id="e1b34-128">**Deaktiveeritud** – pearaamat peaks töötlema ainult kandeid, mis loodi pärast pearaamatu loomist.</span><span class="sxs-lookup"><span data-stu-id="e1b34-128">**Deactivated** – The ledger should process only transactions that are created after the ledger was created.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="e1b34-129">Pärast uute dokumentide sisestamist **ei** saa te tagasi tulla ega seda välja seada.</span><span class="sxs-lookup"><span data-stu-id="e1b34-129">You will **not** be able to come back and set this field after you enter new documents.</span></span>

- <span data-ttu-id="e1b34-130">**Olek** – süsteem seab vastloodud pearaamatute olekuks automaatselt *Ettevalmistamine*.</span><span class="sxs-lookup"><span data-stu-id="e1b34-130">**Status** – The system automatically sets the status of newly created ledgers to *Prepare*.</span></span>
