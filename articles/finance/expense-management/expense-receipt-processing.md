---
title: Kulu sissetuleku töötlemine
description: See teema annab teavet optilise märgituvastuse (OCR) kohta sissetulekute puhul. Selle funktsiooni eesmärk on parandada kasutaja kogemust, kui kuluaruandeid luuakse rakenduses Microsoftis Dynamics 365 Finance.
author: stevensporen
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 1ead9039de63e2cf4f3a7faddd1702b9614d7f99
ms.sourcegitcommit: 6aceca43c53c4dde46954c0b6b855d488eb44ed2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027899"
---
# <a name="public-preview-expense-receipt-processing"></a><span data-ttu-id="65602-104">Avalik eelvaade: kulu sissetuleku töötlemine</span><span class="sxs-lookup"><span data-stu-id="65602-104">Public Preview: Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


<span data-ttu-id="65602-105">Kulu sisestust on laiendatud optilise märgituvastuse (OCR) kaudu sissetulekute jaoks.</span><span class="sxs-lookup"><span data-stu-id="65602-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="65602-106">Selle funktsiooni eesmärk on parandada kasutajakogemust, kui kuluaruandeid luuakse.</span><span class="sxs-lookup"><span data-stu-id="65602-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="65602-107">Võtmefunktsioonid</span><span class="sxs-lookup"><span data-stu-id="65602-107">Key features</span></span>

- <span data-ttu-id="65602-108">Kaupmehe nimi, kuupäev ja kogusumma ekstraktitakse sissetulekutest.</span><span class="sxs-lookup"><span data-stu-id="65602-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="65602-109">Funktsioon püüab vastendada sidumata sissetulekuid sidumata kulukannetega.</span><span class="sxs-lookup"><span data-stu-id="65602-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="65602-110">Kasutajad saavad luua sissetulekutest käsitsi sisestatud kulukanded.</span><span class="sxs-lookup"><span data-stu-id="65602-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="65602-111">Kasutuse näited</span><span class="sxs-lookup"><span data-stu-id="65602-111">Usage examples</span></span>

- <span data-ttu-id="65602-112">**Lisage automaatselt sissetulekud, mis sisaldavad krediitkaardi kandeid kuluaruande loomisel.**</span><span class="sxs-lookup"><span data-stu-id="65602-112">**Automatically attach receipts that include credit card transactions when an expense report is created.**</span></span>

    1. <span data-ttu-id="65602-113">Avage tööruum **Kuluhaldus**.</span><span class="sxs-lookup"><span data-stu-id="65602-113">Open the **Expense management** workspace.</span></span>
    2. <span data-ttu-id="65602-114">Veenduge, et vahekardil **Sissetulekud** on olemas sidumata sissetulekud.</span><span class="sxs-lookup"><span data-stu-id="65602-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="65602-115">Sissetulekuid saate ka üles laadida vahekaardil **Sissetulekud**.</span><span class="sxs-lookup"><span data-stu-id="65602-115">You can also upload receipts on the **Receipts** tab.</span></span>
    3. <span data-ttu-id="65602-116">Veenduge, et vahekardil **Kulud** on olemas sidumata kulud.</span><span class="sxs-lookup"><span data-stu-id="65602-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="65602-117">Tavaliselt impordib kulu administraator need kulud krediitkaardi pakkujalt.</span><span class="sxs-lookup"><span data-stu-id="65602-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
    4. <span data-ttu-id="65602-118">Valige **Uus kuluaruanne**.</span><span class="sxs-lookup"><span data-stu-id="65602-118">Select **New expense report**.</span></span> <span data-ttu-id="65602-119">Pange tähele, et saate kuluaruande loomisel kaasata nüüd ka kulusid ja sissetulekuid.</span><span class="sxs-lookup"><span data-stu-id="65602-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="65602-120">Kui lisate nii kulusid kui sissetulekuid, käivitatakse sissetulekute automaatne sobitamine kulude alusel.</span><span class="sxs-lookup"><span data-stu-id="65602-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

- <span data-ttu-id="65602-121">**Looge kulu või vastendage sissetulekuga kulu.**</span><span class="sxs-lookup"><span data-stu-id="65602-121">**Create an expense, or match an expense from a receipt.**</span></span>

    1. <span data-ttu-id="65602-122">Kuluaruande vahekaardil **Sissetulekud** saate lisada sissetuleku, valides **Lisa sissetulekud**.</span><span class="sxs-lookup"><span data-stu-id="65602-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
    2. <span data-ttu-id="65602-123">Sissetuleku üleslaaditud pildi all pange tähele suvandeid **Loo** ja **Vastenda**.</span><span class="sxs-lookup"><span data-stu-id="65602-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

        - <span data-ttu-id="65602-124">Valige **Loo**, et luua käsitsi sisestatud kulukanne ja täitke sissetulekust ekstraktitud väärtused.</span><span class="sxs-lookup"><span data-stu-id="65602-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
        - <span data-ttu-id="65602-125">Kui valite **Vastenda**, proovib süsteem vastendada olemasoleva kulu kviitungiga.</span><span class="sxs-lookup"><span data-stu-id="65602-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="65602-126">Install</span><span class="sxs-lookup"><span data-stu-id="65602-126">Installation</span></span>

<span data-ttu-id="65602-127">See funktsioon töötab koos funktsiooniga **Kuluaruannete uuendamine**, et aidata lihtsustada kulude kogemust.</span><span class="sxs-lookup"><span data-stu-id="65602-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span>

<span data-ttu-id="65602-128">Nende täpsemate kulude võimaluste kasutamiseks installige Microsofti Dynamics 365 Finance kulude halduse lisandmoodul ja lülitage sisse funktsioonid oma eksemplaris.</span><span class="sxs-lookup"><span data-stu-id="65602-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="65602-129">Saate kasutada lisandmoodulit oma projektist teenuses Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="65602-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="65602-130">Logige LCS-i sisse ja avage soovitud keskkond.</span><span class="sxs-lookup"><span data-stu-id="65602-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="65602-131">Avage **Kõik üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="65602-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="65602-132">Valige **Hooldamine** või kerige alla kiirkaardile **Keskkonna lisandmoodulid**.</span><span class="sxs-lookup"><span data-stu-id="65602-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="65602-133">Valige **Installi uus lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="65602-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="65602-134">Valige **Kulude halduse teenus**.</span><span class="sxs-lookup"><span data-stu-id="65602-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="65602-135">Täitke paigaldusjuhendit ja nõustuge nõuete ja tingimustega.</span><span class="sxs-lookup"><span data-stu-id="65602-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="65602-136">Valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="65602-136">Select **Install**.</span></span>

<span data-ttu-id="65602-137">**Funktsioonide halduse** tööruumis lülitage sisse järgmised funktsioonid:</span><span class="sxs-lookup"><span data-stu-id="65602-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="65602-138">Uuendatud kuluaruanded</span><span class="sxs-lookup"><span data-stu-id="65602-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="65602-139">Kulude automaatne vastendamine ja loomine kviitungist</span><span class="sxs-lookup"><span data-stu-id="65602-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="65602-140">Nende funktsioonide sisselülitamisel ilmnevad järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="65602-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="65602-141">Olemasolev **Kulude halduse** tööruum asendatakse uue tööruumiga.</span><span class="sxs-lookup"><span data-stu-id="65602-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="65602-142">Lisarud on uus menüükäsk kuluvälja nähtavuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="65602-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="65602-143">Saate siiski avada endise **Kuluaruannete** lehe, avades **Kuluhaldus > Minu kulud > Kuluaruanded**.</span><span class="sxs-lookup"><span data-stu-id="65602-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="65602-144">Töövood ja mis tahes kinnitused viivad teid endiselt olemasolevate kuluaruannete lehele.</span><span class="sxs-lookup"><span data-stu-id="65602-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="65602-145">Kviitungeid töödeldakse teenuse Microsoft Azure Cognitive Services kaudu ja metaandmed ekstraktitakse ning lisatakse.</span><span class="sxs-lookup"><span data-stu-id="65602-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="65602-146">Lisati suvand, mis võimaldab teil luua kuluaruande, mis sisaldab vastendatud manustamata kviitungeid.</span><span class="sxs-lookup"><span data-stu-id="65602-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="65602-147">Kuluaruannetele lisatav suvand võimaldab teil luua kviitungist kulurea või üritab sobitada olemasolevat kviitungit olemasoleva kulureaga.</span><span class="sxs-lookup"><span data-stu-id="65602-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="65602-148">Lisateavet kuluaruannete uuendamise funktsiooni kohta vt teemast [Kuluaruannete uuendamine](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="65602-148">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="65602-149">Korduma kippuvad küsimused</span><span class="sxs-lookup"><span data-stu-id="65602-149">Frequently asked questions</span></span>

<span data-ttu-id="65602-150">**Kas Microsoft kasutab oma mudelite jaoks minu andmeid?**</span><span class="sxs-lookup"><span data-stu-id="65602-150">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="65602-151">Ei, Microsoft on oma kviitungite töötlemise teenuse jaoks loonud üldise masinõppe mudeli.</span><span class="sxs-lookup"><span data-stu-id="65602-151">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="65602-152">See mudel ei põhine teie üleslaaditud kviitungitel.</span><span class="sxs-lookup"><span data-stu-id="65602-152">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="65602-153">**Kus see funktsioon on saadaval ja töödeldud?**</span><span class="sxs-lookup"><span data-stu-id="65602-153">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="65602-154">Praegu toetatakse Ameerika Ühendriike.</span><span class="sxs-lookup"><span data-stu-id="65602-154">Currently, the United States is supported.</span></span>

<span data-ttu-id="65602-155">**Kuhu mu kviitungid lähevad?**</span><span class="sxs-lookup"><span data-stu-id="65602-155">**Where do my receipts go?**</span></span>

<span data-ttu-id="65602-156">Finance võtab andmete ekstraktimiseks ühendust teenusega Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="65602-156">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="65602-157">Teenus Cognitive Services säilitab töötlemisel teie kviitungi koopia kuni 24 tunniks.</span><span class="sxs-lookup"><span data-stu-id="65602-157">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="65602-158">Pärast töötluse lõpetamist eemaldab teenus Cognitive Services kviitungi.</span><span class="sxs-lookup"><span data-stu-id="65602-158">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="65602-159">Kviitungid talletatakse endiselt Finance'is.</span><span class="sxs-lookup"><span data-stu-id="65602-159">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="65602-160">Lisateavet vt teemast [Kviitungi mõistmise lubamine vormituvasti uue võimalusega](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="65602-160">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
