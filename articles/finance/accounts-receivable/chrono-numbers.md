---
title: Dokumentide ja kannete nummerdamine kronoloogiliselt
description: See teema kirjeldab, kuidas seadistada ja kasutada kohaldatavate dokumentide ning seotud kannete kronoloogilisi numbreid.
author: ikond
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: fe533052b0e5b04a7d27b954ba644761c631d6d7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838857"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a><span data-ttu-id="f8c91-103">Dokumentide ja kannete nummerdamine kronoloogiliselt</span><span class="sxs-lookup"><span data-stu-id="f8c91-103">Numbering documents and vouchers chronologically</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f8c91-104">Mõnes riigis on dokumentide ja seotud kannete kronoloogilises järjestuses nummerdamine juriidiliselt nõutud.</span><span class="sxs-lookup"><span data-stu-id="f8c91-104">In some countries, there is a legal requirement to number documents and related vouchers in chronological order.</span></span> <span data-ttu-id="f8c91-105">Kronoloogia peab hõlmama perioode.</span><span class="sxs-lookup"><span data-stu-id="f8c91-105">The chronology must be supported by periods.</span></span> <span data-ttu-id="f8c91-106">Kõik varasemate perioodide numbrid peavad olema hilisemate perioodide numbritest väiksemad.</span><span class="sxs-lookup"><span data-stu-id="f8c91-106">All of the numbers that belong to earlier periods must be less than the numbers that belong to later periods.</span></span> <span data-ttu-id="f8c91-107">Selle nõude täitmiseks on juurutatud kronoloogilise nummerdamise funktsioon.</span><span class="sxs-lookup"><span data-stu-id="f8c91-107">To meet this requirement, chronological numbering functionality has been implemented.</span></span> <span data-ttu-id="f8c91-108">See teema kirjeldab, kuidas konfigureerida ja kasutada kohaldatavate dokumentide ning seotud kannete kronoloogilisi numbreid.</span><span class="sxs-lookup"><span data-stu-id="f8c91-108">This topic explains how to configure and use chronological numbers for applicable documents and related vouchers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f8c91-109">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="f8c91-109">Prerequisites</span></span>

<span data-ttu-id="f8c91-110">Lülitage tööruumis Funktsioonihaldus sisse funktsioon **Kronoloogiline nummerdamine**.</span><span class="sxs-lookup"><span data-stu-id="f8c91-110">In the Feature management workspace, turn on the **Chronological numbering** feature.</span></span> <span data-ttu-id="f8c91-111">Lisateavet vt [Funktsioonihalduse ülevaatest](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f8c91-111">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="configure-chronological-numbering"></a><span data-ttu-id="f8c91-112">Kronoloogilise nummerdamise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="f8c91-112">Configure chronological numbering</span></span>

<span data-ttu-id="f8c91-113">Kronoloogiline nummerdamine mõjutab järgmisi dokumente.</span><span class="sxs-lookup"><span data-stu-id="f8c91-113">Chronological numbering affects the following documents.</span></span>

<span data-ttu-id="f8c91-114">**Müügireskontro**</span><span class="sxs-lookup"><span data-stu-id="f8c91-114">**Accounts receivable**</span></span>
- <span data-ttu-id="f8c91-115">Kliendiarve</span><span class="sxs-lookup"><span data-stu-id="f8c91-115">Customer invoice</span></span>
- <span data-ttu-id="f8c91-116">Kliendiarve kanne</span><span class="sxs-lookup"><span data-stu-id="f8c91-116">Customer invoice voucher</span></span>
- <span data-ttu-id="f8c91-117">Müügi kreeditarve</span><span class="sxs-lookup"><span data-stu-id="f8c91-117">Sales credit note</span></span>
- <span data-ttu-id="f8c91-118">Müügi kreeditarve kanne</span><span class="sxs-lookup"><span data-stu-id="f8c91-118">Sales credit note voucher</span></span>
- <span data-ttu-id="f8c91-119">Vabas vormis arve</span><span class="sxs-lookup"><span data-stu-id="f8c91-119">Free text invoice</span></span>
- <span data-ttu-id="f8c91-120">Vabas vormis arve kanne</span><span class="sxs-lookup"><span data-stu-id="f8c91-120">Free text invoice voucher</span></span>
- <span data-ttu-id="f8c91-121">Vabas vormis kreeditarve</span><span class="sxs-lookup"><span data-stu-id="f8c91-121">Free text credit note</span></span>
- <span data-ttu-id="f8c91-122">Vabas vormis kreeditarve kanne</span><span class="sxs-lookup"><span data-stu-id="f8c91-122">Free text credit note voucher</span></span>
- <span data-ttu-id="f8c91-123">Saateleht</span><span class="sxs-lookup"><span data-stu-id="f8c91-123">Packing slip</span></span>
- <span data-ttu-id="f8c91-124">Saatelehe kanne</span><span class="sxs-lookup"><span data-stu-id="f8c91-124">Packing slip voucher</span></span>
- <span data-ttu-id="f8c91-125">Saatelehe paranduskanne</span><span class="sxs-lookup"><span data-stu-id="f8c91-125">Packing slip correction voucher</span></span>
- <span data-ttu-id="f8c91-126">Viivisearve kanne</span><span class="sxs-lookup"><span data-stu-id="f8c91-126">Interest note voucher</span></span>
- <span data-ttu-id="f8c91-127">Märgukirja kanne</span><span class="sxs-lookup"><span data-stu-id="f8c91-127">Collection letter voucher</span></span>

<span data-ttu-id="f8c91-128">**Ostureskontro**</span><span class="sxs-lookup"><span data-stu-id="f8c91-128">**Accounts payable**</span></span>
- <span data-ttu-id="f8c91-129">Arve kanne</span><span class="sxs-lookup"><span data-stu-id="f8c91-129">Invoice voucher</span></span>
- <span data-ttu-id="f8c91-130">Kreeditarve kanne</span><span class="sxs-lookup"><span data-stu-id="f8c91-130">Credit note voucher</span></span>
- <span data-ttu-id="f8c91-131">Toote sissetuleku kanne</span><span class="sxs-lookup"><span data-stu-id="f8c91-131">Product receipt voucher</span></span>

<span data-ttu-id="f8c91-132">**Projektihaldus**</span><span class="sxs-lookup"><span data-stu-id="f8c91-132">**Project management**</span></span>
- <span data-ttu-id="f8c91-133">Arve</span><span class="sxs-lookup"><span data-stu-id="f8c91-133">Invoice</span></span>
- <span data-ttu-id="f8c91-134">Arve kanne</span><span class="sxs-lookup"><span data-stu-id="f8c91-134">Invoice voucher</span></span>
- <span data-ttu-id="f8c91-135">Kreeditarve</span><span class="sxs-lookup"><span data-stu-id="f8c91-135">Credit note</span></span>
- <span data-ttu-id="f8c91-136">Kreeditarve kanne</span><span class="sxs-lookup"><span data-stu-id="f8c91-136">Credit note voucher</span></span> 

### <a name="define-number-sequences"></a><span data-ttu-id="f8c91-137">Numbriseeriate määratlemine</span><span class="sxs-lookup"><span data-stu-id="f8c91-137">Define number sequences</span></span>

<span data-ttu-id="f8c91-138">Numbriseeriate määratlemiseks minge jaotisse **Organisatsiooni haldus** > **Numbriseeriad** > **Numbriseeriad**.</span><span class="sxs-lookup"><span data-stu-id="f8c91-138">To define number sequences, go to **Organization administration** > **Number sequences** > **Number sequences**.</span></span> <span data-ttu-id="f8c91-139">Saate määratleda nii palju numbriseeriaid, kui on nõutud dokumentide mõjutatud perioodide katmiseks vaja.</span><span class="sxs-lookup"><span data-stu-id="f8c91-139">You can define as many number sequences as required to cover the affected periods for required documents.</span></span> 

<span data-ttu-id="f8c91-140">Määrake igale numbriseeriale ettevõte.</span><span class="sxs-lookup"><span data-stu-id="f8c91-140">Specify a company for each number sequence.</span></span> <span data-ttu-id="f8c91-141">Numbriseeriate segmendid tuleb määratleda nii, et need korraldavad perioodid kronoloogilisse järjestusse.</span><span class="sxs-lookup"><span data-stu-id="f8c91-141">The segments of the number sequences must be defined so that they provide chronological order for periods.</span></span> <span data-ttu-id="f8c91-142">Näiteks võivad segmentide nimed hõlmata spetsiaalset prefiksit, mis tuvastab konkreetse perioodi.</span><span class="sxs-lookup"><span data-stu-id="f8c91-142">For example, the segment names can contain a special prefix that identifies a specific period.</span></span>

![Numbriseeriate seadistamine](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a><span data-ttu-id="f8c91-144">Numbriseeriate gruppide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="f8c91-144">Configure number sequence groups</span></span>

<span data-ttu-id="f8c91-145">Numbriseeriate gruppide konfigureerimiseks minge jaotisse **Müügireskontro** > **Seadistus** > **Müügireskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="f8c91-145">To configure number sequence groups, go to **Accounts receivable** > **Setup** > **Accounts receivable parameters**.</span></span> <span data-ttu-id="f8c91-146">Määratlege vahekaardil **Numbriseeriad** mõjutatud perioodide katmiseks vajalike numbriseeriate gruppide arv.</span><span class="sxs-lookup"><span data-stu-id="f8c91-146">On the **Number sequences** tab, define as many number sequences groups as required to cover the affected periods.</span></span> 

<span data-ttu-id="f8c91-147">Valige iga grupi jaoks jaotises **Viide** üks toetatud dokumendiviidetest ja vaadake väljal **Numbriseeria kood** vastava perioodi jaoks eelnevalt loodud numbriseeriat.</span><span class="sxs-lookup"><span data-stu-id="f8c91-147">For each group, in the **Reference** section, select one of the supported document references, and in the **Number sequence code** field, refer to a number sequence that was previously created for the related period.</span></span>

![Numbriseeriagrupi seadistus](media/chrono-num-sequence-group.jpg)

<span data-ttu-id="f8c91-149">Samuti konfigureerige numbriseeriate grupid moodulites **Ostureskontro** ja **Projektihaldus ja raamatupidamine**.</span><span class="sxs-lookup"><span data-stu-id="f8c91-149">Similarly, configure number sequence groups in **Accounts payable** and **Project management and accounting** modules.</span></span>

### <a name="configure-number-sequence-groups-chronology"></a><span data-ttu-id="f8c91-150">Numbriseeriate gruppide kronoloogia konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="f8c91-150">Configure number sequence groups chronology</span></span>

<span data-ttu-id="f8c91-151">Numbriseeriate gruppide kronoloogia konfigureerimiseks minge jaotisse **Organisatsiooni haldus** > **Numbriseeriad** > **Kronoloogilised numbriseeriate grupid**.</span><span class="sxs-lookup"><span data-stu-id="f8c91-151">To configure number sequence groups chronology, go to **Organization administration** > **Number sequences** > **Chronological number sequence groups**.</span></span> <span data-ttu-id="f8c91-152">Määratlege numbriseeriate gruppide kohaldatavuse tingimused.</span><span class="sxs-lookup"><span data-stu-id="f8c91-152">Define the applicability conditions for number sequence groups.</span></span>

![Numbrite seadistamine kronoloogiliselt](media/chrono-num-sequence-group-period.jpg)

| <span data-ttu-id="f8c91-154">Field</span><span class="sxs-lookup"><span data-stu-id="f8c91-154">Field</span></span>            | <span data-ttu-id="f8c91-155">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="f8c91-155">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8c91-156">Jõustunud</span><span class="sxs-lookup"><span data-stu-id="f8c91-156">Effective</span></span>  | <span data-ttu-id="f8c91-157">Numbriseeriate grupi kohaldatavuse alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="f8c91-157">The start date of number sequence group applicability.</span></span> |
| <span data-ttu-id="f8c91-158">Aegumine</span><span class="sxs-lookup"><span data-stu-id="f8c91-158">Expiration</span></span>      | <span data-ttu-id="f8c91-159">Numbriseeriate grupi kohaldatavuse lõppkuupäev.</span><span class="sxs-lookup"><span data-stu-id="f8c91-159">The end date of number sequence group applicability.</span></span> <span data-ttu-id="f8c91-160">Kui lõppkuupäeva ei rakendata, valige **Mitte kunagi**.</span><span class="sxs-lookup"><span data-stu-id="f8c91-160">If no end date is applied, select **Never**.</span></span> |
| <span data-ttu-id="f8c91-161">Numbriseeria grupp</span><span class="sxs-lookup"><span data-stu-id="f8c91-161">Number sequence group</span></span> | <span data-ttu-id="f8c91-162">Numbriseeriate grupp, mida kasutatakse selle perioodi jooksul dokumendinumbrite loomiseks.</span><span class="sxs-lookup"><span data-stu-id="f8c91-162">Number sequence group that will be used to generate document numbers during the period.</span></span> |
| <span data-ttu-id="f8c91-163">Algne numbrite seeriagrupp</span><span class="sxs-lookup"><span data-stu-id="f8c91-163">Original number sequence group</span></span> | <span data-ttu-id="f8c91-164">Seda numbriseeriate grupi koodi kasutatakse nende juhtumite täiendavaks filtreerimiseks, kus dokumentidele on juba määratud konkreetne *püsiv* numbriseeriate grupp.</span><span class="sxs-lookup"><span data-stu-id="f8c91-164">This number sequence group code is used for additional filtering for the cases when documents already have a specific *permanent* number sequence group assigned.</span></span> <span data-ttu-id="f8c91-165">Tühja väärtust loetakse konkreetseks väärtuseks.</span><span class="sxs-lookup"><span data-stu-id="f8c91-165">An empty value is considered a specific value.</span></span> <span data-ttu-id="f8c91-166">Kui peate algselt määratud gruppi ignoreerima, kasutage selle seadistuse puhul suvandit **Vaikeväärtus**.</span><span class="sxs-lookup"><span data-stu-id="f8c91-166">If you need to ignore a preliminary assigned group, use the **Default** option for this setup.</span></span> |
| <span data-ttu-id="f8c91-167">Vaikimisi</span><span class="sxs-lookup"><span data-stu-id="f8c91-167">Default</span></span> | <span data-ttu-id="f8c91-168">Kui see on sisse lülitatud, ignoreerib süsteem algselt määratud dokumendi numbriseeriate gruppi ja kasutab kohaldatavuse analüüsis ainult perioodide algus- ja lõppkuupäeva.</span><span class="sxs-lookup"><span data-stu-id="f8c91-168">If turned on, the system ignores the preliminary assigned document number sequence group and uses only the periods start and end dates for applicability analysis.</span></span> <span data-ttu-id="f8c91-169">Kui see on välja lülitatud, kasutab süsteem valikute jaoks täiskombinatsiooni **Jõustumine** + **Aegumine** + **Algne numbriseeriate grupp**.</span><span class="sxs-lookup"><span data-stu-id="f8c91-169">If turned off, the system uses the full combination **Effective** + **Expiration** + **Original number sequence group** for selection.</span></span> |

## <a name="document-posting"></a><span data-ttu-id="f8c91-170">Dokumendi sisestamine</span><span class="sxs-lookup"><span data-stu-id="f8c91-170">Document posting</span></span>
<span data-ttu-id="f8c91-171">Dokumendi sisestamisel määratakse dokumendile selle sisestuskuupäeval põhinev sobiv numbriseeriate grupp ja seejärel kasutatakse seda tuvastatud numbriseeria alusel dokumendi numbri loomiseks.</span><span class="sxs-lookup"><span data-stu-id="f8c91-171">When you post a document, the appropriate number sequence group is assigned to the document, based on document's posting date, and then used to generate a document number based on the detected number sequence.</span></span> <span data-ttu-id="f8c91-172">Süsteem edastab numbriseeriate grupi määramise kohta teate.</span><span class="sxs-lookup"><span data-stu-id="f8c91-172">The system provides a message regarding the number sequence group assignment.</span></span>

![Dokumendi number](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> <span data-ttu-id="f8c91-174">Mõnes riigis on dokumentide nummerdamiseks juba rakendatud kindel loogika.</span><span class="sxs-lookup"><span data-stu-id="f8c91-174">For some countries, there is a specific logic already implemented for document numbering.</span></span> <span data-ttu-id="f8c91-175">Sellisel juhul alistab riigipõhine loogika funktsiooni **Kronoloogiline nummerdamine**.</span><span class="sxs-lookup"><span data-stu-id="f8c91-175">In this case, country-specific logic will override the **Chronological numbering** feature.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
