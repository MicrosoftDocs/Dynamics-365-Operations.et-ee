---
title: Finantsaruandluse KKK
description: Selles teemas antakse vastused mõnedele korduma kippuvatele küsimustele finantsaruandluse kohta.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266629"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="49d47-103">Finantsaruandluse KKK</span><span class="sxs-lookup"><span data-stu-id="49d47-103">Financial reporting FAQ</span></span>

<span data-ttu-id="49d47-104">Selles teemas antakse vastused korduma kippuvatele küsimustele finantsaruandluse kohta.</span><span class="sxs-lookup"><span data-stu-id="49d47-104">This topic provides answers to frequently asked questions about Financial reporting.</span></span>

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a><span data-ttu-id="49d47-105">Kuidas piirata puuturbe abil juurdepääsu aruandele?</span><span class="sxs-lookup"><span data-stu-id="49d47-105">How do I restrict access to a report by using tree security?</span></span>

<span data-ttu-id="49d47-106">Järgmises näites kirjeldatakse aruandele juurdepääsu piiramist puuturbe abil.</span><span class="sxs-lookup"><span data-stu-id="49d47-106">The following example shows how to restrict access to a report by using tree security.</span></span>

<span data-ttu-id="49d47-107">Demoettevõttel USMF on **bilansiaruanne**, millele ei pea kõik finantsaruandluse kasutajad juurde pääsema.</span><span class="sxs-lookup"><span data-stu-id="49d47-107">The USMF demo company has a **Balance sheet** report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="49d47-108">Turvapuu abil saate piirata juurdepääsu ühele aruandele nii, et sellele oleks juurdepääs ainult teatud kasutajatel.</span><span class="sxs-lookup"><span data-stu-id="49d47-108">You can use tree security to restrict access to a single report so that only specific users can access it.</span></span>

1. <span data-ttu-id="49d47-109">Logige rakendusse Financial Reporter Report Designer sisse.</span><span class="sxs-lookup"><span data-stu-id="49d47-109">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="49d47-110">Uue puu definitsiooni loomiseks valige **Fail \> Uus \> Puu definitsioon**.</span><span class="sxs-lookup"><span data-stu-id="49d47-110">Select **File \> New \> Tree Definition** to create a new tree definition.</span></span>
3. <span data-ttu-id="49d47-111">Topeltpuudutage (või topeltklõpsake) veerus **Üksuse turve** rida **Kokkuvõte**.</span><span class="sxs-lookup"><span data-stu-id="49d47-111">Double-tap (or double-click) the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="49d47-112">Valige **Kasutajad ja grupid**.</span><span class="sxs-lookup"><span data-stu-id="49d47-112">Select **Users and Groups**.</span></span>
5. <span data-ttu-id="49d47-113">Valige kasutajad või grupid, kellele soovite anda juurdepääsu sellele aruandele.</span><span class="sxs-lookup"><span data-stu-id="49d47-113">Select the users or groups that require access to the report.</span></span>
6. <span data-ttu-id="49d47-114">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="49d47-114">Select **Save**.</span></span>
7. <span data-ttu-id="49d47-115">Lisage aruande definitsioonis uus puudefinitsioon.</span><span class="sxs-lookup"><span data-stu-id="49d47-115">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="49d47-116">Valige puudefinitsioonis **Säte**.</span><span class="sxs-lookup"><span data-stu-id="49d47-116">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="49d47-117">Seejärel valige jaotises **Aruandlusüksuse valik** **Kaasa kõik üksused**.</span><span class="sxs-lookup"><span data-stu-id="49d47-117">Then, under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a><span data-ttu-id="49d47-118">Kuidas tuvastada, millised kontod minu saldodele ei vasta?</span><span class="sxs-lookup"><span data-stu-id="49d47-118">How do I identify which accounts don't match my balances?</span></span>

<span data-ttu-id="49d47-119">Kui teil on aruanne, millel pole kattuvaid saldosid, kasutage iga konto ja hälbe tuvastamiseks järgmisi protseduure.</span><span class="sxs-lookup"><span data-stu-id="49d47-119">If you have a report that doesn't have matching balances, use the following procedures to identify each account and variance.</span></span>

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="49d47-120">Asukohas Financial Reporter Report Designer</span><span class="sxs-lookup"><span data-stu-id="49d47-120">In Financial Reporter Report Designer</span></span>

1. <span data-ttu-id="49d47-121">Looge uus readefinitsioon.</span><span class="sxs-lookup"><span data-stu-id="49d47-121">Create a new row definition.</span></span>
2. <span data-ttu-id="49d47-122">Valige **Redigeeri \> Lisa read dimensioonidest**.</span><span class="sxs-lookup"><span data-stu-id="49d47-122">Select **Edit \> Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="49d47-123">Valige **MainAccount**.</span><span class="sxs-lookup"><span data-stu-id="49d47-123">Select **MainAccount**.</span></span>
4. <span data-ttu-id="49d47-124">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="49d47-124">Select **OK**.</span></span>
5. <span data-ttu-id="49d47-125">Salvestage readefinitsioon.</span><span class="sxs-lookup"><span data-stu-id="49d47-125">Save the row definition.</span></span>
6. <span data-ttu-id="49d47-126">Looge uus veerudefinitsioon.</span><span class="sxs-lookup"><span data-stu-id="49d47-126">Create a new column definition.</span></span>
7. <span data-ttu-id="49d47-127">Looge uus aruande definitsioon.</span><span class="sxs-lookup"><span data-stu-id="49d47-127">Create a new report definition.</span></span>
8. <span data-ttu-id="49d47-128">Valige **Sätted** ja tühjendage selle suvandi ruut.</span><span class="sxs-lookup"><span data-stu-id="49d47-128">Select **Settings** and unmark this option.</span></span>
9. <span data-ttu-id="49d47-129">Looge aruanne.</span><span class="sxs-lookup"><span data-stu-id="49d47-129">Generate the report.</span></span> 
10. <span data-ttu-id="49d47-130">Eksportige aruanne Microsoft Excelisse.</span><span class="sxs-lookup"><span data-stu-id="49d47-130">Export the report to Microsoft Excel.</span></span>

### <a name="in-dynamics-365-finance"></a><span data-ttu-id="49d47-131">Asukohas Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="49d47-131">In Dynamics 365 Finance</span></span>

1. <span data-ttu-id="49d47-132">Avage **Pearaamat \> Päringud ja aruanded \> Proovibilanss**.</span><span class="sxs-lookup"><span data-stu-id="49d47-132">Go to **General ledger \> Inquiries and reports \> Trial balance**.</span></span>
2. <span data-ttu-id="49d47-133">Seadistage järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="49d47-133">Set the following fields:</span></span>

    - <span data-ttu-id="49d47-134">**Alguskuupäev** – sisestage finantsaasta alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="49d47-134">**From Date** – Enter the start date of the fiscal year.</span></span>
    - <span data-ttu-id="49d47-135">**Lõppkuupäev** – sisestage kuupäev, mille kohta aruande loote.</span><span class="sxs-lookup"><span data-stu-id="49d47-135">**To Date** – Enter the date that you're generating the report for.</span></span>
    - <span data-ttu-id="49d47-136">**Finantsdimensioon** – seadke selle välja väärtuseks **Põhikonto kogum**.</span><span class="sxs-lookup"><span data-stu-id="49d47-136">**Financial Dimension** – Set this field to **Main Account set**.</span></span>

3. <span data-ttu-id="49d47-137">Valige **Arvuta**.</span><span class="sxs-lookup"><span data-stu-id="49d47-137">Select **Calculate**.</span></span>
4. <span data-ttu-id="49d47-138">Eksportige aruanne Excelisse.</span><span class="sxs-lookup"><span data-stu-id="49d47-138">Export the report to Excel.</span></span>

<span data-ttu-id="49d47-139">Nüüd saate kopeerida andmeid Financial Reporteri Exceli aruandest **proovibilansi** aruandesse, et võrrelda veerge **Sulgemissaldo**.</span><span class="sxs-lookup"><span data-stu-id="49d47-139">You should now be able to copy the data from the Financial Reporter Excel report to the **Trial Balance** report, so that you can compare the **Closing Balance** columns.</span></span>

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a><span data-ttu-id="49d47-140">Aruande kujundamisel Report Designeris või finantsaruande genereerimisel kuvati järgmine teate: „Toimingut ei saanud andmepakkuja raamistikus ilmnenud probleemi tõttu lõpule viia.”</span><span class="sxs-lookup"><span data-stu-id="49d47-140">When I design a report in Report Designer, or when I generate a financial report, I received the following message: "The operation could not be completed due to a problem in the data provider framework."</span></span> <span data-ttu-id="49d47-141">Mida peaksin tegema?</span><span class="sxs-lookup"><span data-stu-id="49d47-141">How should I respond?</span></span>

<span data-ttu-id="49d47-142">Teade näitab, et probleem tekkis siis, kui süsteem püüdis tuua finantsmetaandmeid andmevakast finantsaruandluse kasutamise ajal.</span><span class="sxs-lookup"><span data-stu-id="49d47-142">The message indicates that an issue occurred when the system tried to retrieve financial metadata from the data mart while you were using Financial reporting.</span></span> <span data-ttu-id="49d47-143">Selle probleemi lahendamiseks on kaks võimalust.</span><span class="sxs-lookup"><span data-stu-id="49d47-143">There are two ways to respond to this issue:</span></span>

- <span data-ttu-id="49d47-144">Vaadake üle andmete integreerimisolek, tehes Report Designeris valikud **Tööriistad \>integreerimisolek**.</span><span class="sxs-lookup"><span data-stu-id="49d47-144">Review the integration status of the data by going to **Tools \> Integration status** in Report Designer.</span></span> <span data-ttu-id="49d47-145">Kui integreerimine on pooleli, oodake, kuni see on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="49d47-145">If the integration is incomplete, wait for it to be completed.</span></span> <span data-ttu-id="49d47-146">Seejärel proovige uuesti toimingut, mida tegite teate ilmnemisel.</span><span class="sxs-lookup"><span data-stu-id="49d47-146">Then retry what you were doing when you received the message.</span></span>
- <span data-ttu-id="49d47-147">Probleemi tuvastamiseks ja lahendamiseks pöörduge toe poole.</span><span class="sxs-lookup"><span data-stu-id="49d47-147">Contact Support to identify and work through the issue.</span></span> <span data-ttu-id="49d47-148">Süsteemis võivad olla vastuolulised andmed.</span><span class="sxs-lookup"><span data-stu-id="49d47-148">There might be inconsistent data in the system.</span></span> <span data-ttu-id="49d47-149">Tugitehnikud aitavad teil seda probleemi serveris tuvastada ja leida kindlad andmed, mis võivad vajada värskendamist.</span><span class="sxs-lookup"><span data-stu-id="49d47-149">Support engineers can help you identify that issue on the server and find the specific data that might require an update.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
