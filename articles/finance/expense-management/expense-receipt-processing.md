---
title: Kulu sissetuleku töötlemine
description: See teema annab teavet optilise märgituvastuse (OCR) kohta sissetulekute puhul. Selle funktsiooni eesmärk on parandada kasutaja kogemust, kui kuluaruandeid luuakse rakenduses Microsoftis Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
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
ms.openlocfilehash: 31c08ea264e6caec3217f4b424275495f39123e3
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378227"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="97899-104">Kulusissetuleku töötlemine</span><span class="sxs-lookup"><span data-stu-id="97899-104">Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97899-105">Kulu sisestust on laiendatud optilise märgituvastuse (OCR) kaudu sissetulekute jaoks.</span><span class="sxs-lookup"><span data-stu-id="97899-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="97899-106">Selle funktsiooni eesmärk on parandada kasutajakogemust, kui kuluaruandeid luuakse.</span><span class="sxs-lookup"><span data-stu-id="97899-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="97899-107">Võtmefunktsioonid</span><span class="sxs-lookup"><span data-stu-id="97899-107">Key features</span></span>

- <span data-ttu-id="97899-108">Kaupmehe nimi, kuupäev ja kogusumma ekstraktitakse sissetulekutest.</span><span class="sxs-lookup"><span data-stu-id="97899-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="97899-109">Funktsioon püüab vastendada sidumata sissetulekuid sidumata kulukannetega.</span><span class="sxs-lookup"><span data-stu-id="97899-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="97899-110">Kasutajad saavad luua sissetulekutest käsitsi sisestatud kulukanded.</span><span class="sxs-lookup"><span data-stu-id="97899-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="97899-111">Kasutuse näited</span><span class="sxs-lookup"><span data-stu-id="97899-111">Usage examples</span></span>

<span data-ttu-id="97899-112">Selleks, et lisada automaatselt sissetulekuid, mis sisaldavad krediitkaardi kandeid kuluaruande loomisel, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="97899-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="97899-113">Avage tööruum **Kuluhaldus**.</span><span class="sxs-lookup"><span data-stu-id="97899-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="97899-114">Veenduge, et vahekardil **Sissetulekud** on olemas sidumata sissetulekud.</span><span class="sxs-lookup"><span data-stu-id="97899-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="97899-115">Sissetulekuid saate ka üles laadida vahekaardil **Sissetulekud**.</span><span class="sxs-lookup"><span data-stu-id="97899-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="97899-116">Veenduge, et vahekardil **Kulud** on olemas sidumata kulud.</span><span class="sxs-lookup"><span data-stu-id="97899-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="97899-117">Tavaliselt impordib kulu administraator need kulud krediitkaardi pakkujalt.</span><span class="sxs-lookup"><span data-stu-id="97899-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="97899-118">Valige **Uus kuluaruanne**.</span><span class="sxs-lookup"><span data-stu-id="97899-118">Select **New expense report**.</span></span> <span data-ttu-id="97899-119">Pange tähele, et saate kuluaruande loomisel kaasata nüüd ka kulusid ja sissetulekuid.</span><span class="sxs-lookup"><span data-stu-id="97899-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="97899-120">Kui lisate nii kulusid kui sissetulekuid, käivitatakse sissetulekute automaatne sobitamine kulude alusel.</span><span class="sxs-lookup"><span data-stu-id="97899-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="97899-121">Selleks, et luua kulu või vastendada sissetulekuga kulu, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="97899-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="97899-122">Kuluaruande vahekaardil **Sissetulekud** saate lisada sissetuleku, valides **Lisa sissetulekud**.</span><span class="sxs-lookup"><span data-stu-id="97899-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="97899-123">Sissetuleku üleslaaditud pildi all pange tähele suvandeid **Loo** ja **Vastenda**.</span><span class="sxs-lookup"><span data-stu-id="97899-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="97899-124">Valige **Loo**, et luua käsitsi sisestatud kulukanne ja täitke sissetulekust ekstraktitud väärtused.</span><span class="sxs-lookup"><span data-stu-id="97899-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="97899-125">Kui valite **Vastenda**, proovib süsteem vastendada olemasoleva kulu kviitungiga.</span><span class="sxs-lookup"><span data-stu-id="97899-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="97899-126">Install</span><span class="sxs-lookup"><span data-stu-id="97899-126">Installation</span></span>

<span data-ttu-id="97899-127">See funktsioon töötab koos funktsiooniga **Kuluaruannete uuendamine**, et aidata lihtsustada kulude kogemust.</span><span class="sxs-lookup"><span data-stu-id="97899-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="97899-128">See funktsioon on saadaval ainult Järgu 2+ keskkondades, mis on liivakasti- ja tootmiskeskkonnad.</span><span class="sxs-lookup"><span data-stu-id="97899-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="97899-129">Nende täpsemate kulude võimaluste kasutamiseks installige Microsofti Dynamics 365 Finance kulude halduse lisandmoodul ja lülitage sisse funktsioonid oma eksemplaris.</span><span class="sxs-lookup"><span data-stu-id="97899-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="97899-130">Saate kasutada lisandmoodulit oma projektist teenuses Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="97899-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="97899-131">Logige LCS-i sisse ja avage soovitud keskkond.</span><span class="sxs-lookup"><span data-stu-id="97899-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="97899-132">Avage **Kõik üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="97899-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="97899-133">Valige **Hooldamine** või kerige alla kiirkaardile **Keskkonna lisandmoodulid**.</span><span class="sxs-lookup"><span data-stu-id="97899-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="97899-134">Valige **Installi uus lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="97899-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="97899-135">Valige **Kulude halduse teenus**.</span><span class="sxs-lookup"><span data-stu-id="97899-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="97899-136">Täitke paigaldusjuhendit ja nõustuge nõuete ja tingimustega.</span><span class="sxs-lookup"><span data-stu-id="97899-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="97899-137">Valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="97899-137">Select **Install**.</span></span>

<span data-ttu-id="97899-138">**Funktsioonide halduse** tööruumis lülitage sisse järgmised funktsioonid:</span><span class="sxs-lookup"><span data-stu-id="97899-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="97899-139">Uuendatud kuluaruanded</span><span class="sxs-lookup"><span data-stu-id="97899-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="97899-140">Kulude automaatne vastendamine ja loomine kviitungist</span><span class="sxs-lookup"><span data-stu-id="97899-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="97899-141">Nende funktsioonide sisselülitamisel ilmnevad järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="97899-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="97899-142">Olemasolev **Kulude halduse** tööruum asendatakse uue tööruumiga.</span><span class="sxs-lookup"><span data-stu-id="97899-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="97899-143">Lisarud on uus menüükäsk kuluvälja nähtavuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="97899-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="97899-144">Saate siiski avada endise **Kuluaruannete** lehe, avades **Kuluhaldus > Minu kulud > Kuluaruanded**.</span><span class="sxs-lookup"><span data-stu-id="97899-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="97899-145">Töövood ja mis tahes kinnitused viivad teid endiselt olemasolevate kuluaruannete lehele.</span><span class="sxs-lookup"><span data-stu-id="97899-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="97899-146">Kviitungeid töödeldakse teenuse Microsoft Azure Cognitive Services kaudu ja metaandmed ekstraktitakse ning lisatakse.</span><span class="sxs-lookup"><span data-stu-id="97899-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="97899-147">Lisati suvand, mis võimaldab teil luua kuluaruande, mis sisaldab vastendatud manustamata kviitungeid.</span><span class="sxs-lookup"><span data-stu-id="97899-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="97899-148">Kuluaruannetele lisatav suvand võimaldab teil luua kviitungist kulurea või üritab sobitada olemasolevat kviitungit olemasoleva kulureaga.</span><span class="sxs-lookup"><span data-stu-id="97899-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="97899-149">Lisateavet kuluaruannete uuendamise funktsiooni kohta vt teemast [Kuluaruannete uuendamine](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="97899-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="97899-150">Korduma kippuvad küsimused</span><span class="sxs-lookup"><span data-stu-id="97899-150">Frequently asked questions</span></span>

<span data-ttu-id="97899-151">**Kas Microsoft kasutab oma mudelite jaoks minu andmeid?**</span><span class="sxs-lookup"><span data-stu-id="97899-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="97899-152">Ei, Microsoft on oma kviitungite töötlemise teenuse jaoks loonud üldise masinõppe mudeli.</span><span class="sxs-lookup"><span data-stu-id="97899-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="97899-153">See mudel ei põhine teie üleslaaditud kviitungitel.</span><span class="sxs-lookup"><span data-stu-id="97899-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="97899-154">**Kus see funktsioon on saadaval ja töödeldud?**</span><span class="sxs-lookup"><span data-stu-id="97899-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="97899-155">Praegu toetatakse Ameerika Ühendriike.</span><span class="sxs-lookup"><span data-stu-id="97899-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="97899-156">**Kuhu mu kviitungid lähevad?**</span><span class="sxs-lookup"><span data-stu-id="97899-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="97899-157">Finance võtab andmete ekstraktimiseks ühendust teenusega Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="97899-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="97899-158">Teenus Cognitive Services säilitab töötlemisel teie kviitungi koopia kuni 24 tunniks.</span><span class="sxs-lookup"><span data-stu-id="97899-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="97899-159">Pärast töötluse lõpetamist eemaldab teenus Cognitive Services kviitungi.</span><span class="sxs-lookup"><span data-stu-id="97899-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="97899-160">Kviitungid talletatakse endiselt Finance'is.</span><span class="sxs-lookup"><span data-stu-id="97899-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="97899-161">Lisateavet vt teemast [Kviitungi mõistmise lubamine vormituvasti uue võimalusega](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="97899-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
