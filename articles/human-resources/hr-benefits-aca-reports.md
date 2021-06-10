---
title: Taskukohase ravikindlustuse eelnõu (ACA) aruannete koostamine
description: Taskukohase ravikindlustuse eelnõu (ACA) aruandlus loob vormid 1095-B ja 1095-C, mis toetavad Taskukohase ravikindlustuse eelnõu **Tööandja kohustuse** osa.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 1091460ee1996b944b760f3771007bd2a26666a9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053197"
---
# <a name="generate-aca-reports"></a><span data-ttu-id="ff7b8-103">ACA aruannete loomine</span><span class="sxs-lookup"><span data-stu-id="ff7b8-103">Generate ACA reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ff7b8-104">Taskukohase ravikindlustuse eelnõu (ACA) aruandlus loob vormid 1095-B ja 1095-C, mis toetavad Taskukohase ravikindlustuse eelnõu **Tööandja kohustuse** osa.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-104">Affordable Care Act (ACA) reporting generates forms 1095-B and 1095-C in support of the **Employer Mandate** portion of the Affordable Care Act.</span></span>

> [!NOTE]
> <span data-ttu-id="ff7b8-105">ACA aruandlus on lubatud ainult USA juriidilistele isikutele.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-105">ACA reporting is only enabled for legal entities in the United States.</span></span>

## <a name="getting-started"></a><span data-ttu-id="ff7b8-106">Alustamine</span><span class="sxs-lookup"><span data-stu-id="ff7b8-106">Getting started</span></span>

<span data-ttu-id="ff7b8-107">Vormide 1095-B ja 1095-C jaoks andmete jälgimiseks looge kõigepealt üks või rohkem ravikindlustusega hõlmatud gruppi.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-107">To track information for forms 1095-B and 1095-C, you must first create one or more Affordable care coverage groups.</span></span> <span data-ttu-id="ff7b8-108">Taskukohase ravikindlustuskattega hõlmatud grupid näitavad järgmist.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-108">Affordable Care coverage groups indicate:</span></span>

- <span data-ttu-id="ff7b8-109">Töötajale kindlustuskaitse pakkumine</span><span class="sxs-lookup"><span data-stu-id="ff7b8-109">The offer of coverage for an employee</span></span>
- <span data-ttu-id="ff7b8-110">Töötaja osa madalaima maksumusega kuumaksest, kui kulu ületab föderaalset vaesuspiiri</span><span class="sxs-lookup"><span data-stu-id="ff7b8-110">The employee’s share of the lowest cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="ff7b8-111">Tööandja kasutatav Safe Harbor, kui see on kohaldatav</span><span class="sxs-lookup"><span data-stu-id="ff7b8-111">Safe Harbor used by the employer, if applicable</span></span>

<span data-ttu-id="ff7b8-112">Taskukohase ravikindlustuse gurpid võimaldavad hallata nendel väljadel olevaid andmeid, ilma et oleks vaja muuta iga töötajakirjet, kus tingimused on samad.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-112">Affordable Care coverage groups allow you to manage the information for these fields without changing every employee record where the conditions are the same.</span></span> <span data-ttu-id="ff7b8-113">Taskukohase ravikindlustuse grupid saab määrata hõlpsasti vähemalt ühele töötajale, kasutades lehel suvandit **Massiline määramine**.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-113">You can easily assign Affordable Care coverage groups to one or more employees by using the **Mass assign** option on the page.</span></span>

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a><span data-ttu-id="ff7b8-114">Mitme kindlustusgrupi versiooni säilitamine</span><span class="sxs-lookup"><span data-stu-id="ff7b8-114">Maintaining multiple versions of a coverage group</span></span>

<span data-ttu-id="ff7b8-115">Saate säilitada mistahes kindlustuskaitse grupist mitu versiooni.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-115">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="ff7b8-116">See funktsioon võimaldab teil teha muudatusi ilma, et peate looma uue grupi ja määrama töötajad sellele ümber.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-116">This functionality allows you to make changes without having to create a new group and reassign employees to it.</span></span> 

<span data-ttu-id="ff7b8-117">Pärast ACA kindlustuskaitse gruppide loomist saate **Massilise määramise** suvandiga määrata grupid töötajatele hulgi.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-117">After you’ve created ACA coverage groups, you can mass assign the groups to employees with the **Mass assignment** option.</span></span> <span data-ttu-id="ff7b8-118">Saate ka individuaalselt näidata, kas jälgida ja esitada ACA-teavet ning määrata töötaja Taskukohase ravikindlustuskaitse gruppi.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-118">You can also individually indicate whether to track and report ACA information, and assign an employee to an Affordable Care coverage group.</span></span>

<span data-ttu-id="ff7b8-119">Te ei pea jälgima mõnda ACA kindlustuskaitse teavet, näiteks osalise tööajaga töötajate puhul.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-119">You don't need to track some ACA coverage information, such as for part-time employees.</span></span> <span data-ttu-id="ff7b8-120">Sellisel juhul määrake välja **Kindlustuskaitse aruandlus** väärtuseks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-120">In this case, set the **Report coverage** field to **No**.</span></span> <span data-ttu-id="ff7b8-121">Kuigi peate määrama iga jälgitava ACA-teabega töötaja Taskukohas ravikindlustuskaitse gruppi, saate erineva väärtusega kuude korral ikka järgmisi suvandeid muuta.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-121">Although you must assign each employee with trackable ACA information to an Affordable Care coverage group, you can still change the following options for months with different values:</span></span>

- <span data-ttu-id="ff7b8-122">**Katvuse pakkumine**</span><span class="sxs-lookup"><span data-stu-id="ff7b8-122">**Offer of coverage**</span></span>
- <span data-ttu-id="ff7b8-123">**Töötaja kulu osa**</span><span class="sxs-lookup"><span data-stu-id="ff7b8-123">**Employee share of cost**</span></span>
- <span data-ttu-id="ff7b8-124">**Safe Harbor**</span><span class="sxs-lookup"><span data-stu-id="ff7b8-124">**Safe Harbor**</span></span>

<span data-ttu-id="ff7b8-125">Erandite sisestamiseks mõnesse taskukohase ravikindlustuse grupi väärtusse valige lehel **Töötaja üksikasjad** vahekaardi **Tööhõive** jaotises **Täiendav teave** link **Ravikindlustusega hõlmatud** .</span><span class="sxs-lookup"><span data-stu-id="ff7b8-125">To enter exceptions for Affordable Care coverage group values, select the **Affordable Care Coverage** link on the **Worker detail** page under the **Additional information** section on the **Employment tab**.</span></span>

## <a name="reporting-health-care-coverage"></a><span data-ttu-id="ff7b8-126">Tervisekindlustuse registreerimine</span><span class="sxs-lookup"><span data-stu-id="ff7b8-126">Reporting health care coverage</span></span>

<span data-ttu-id="ff7b8-127">Lisaks jälgimisele, millist tervisekindlustust täisajaga töötajatele pakuti, kui tööandja pakub tööandja enda sõlmitud tervisekindlustust, millega töötaja on liitunud (olenemata sellest, kas töösuhe on täisajaga või osalise ajaga), tuleb vormil 1095 C esitada lisateavet.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-127">In addition to tracking health insurance coverage offered to full-time employees, if the employer offers employer-sponsored self-insured health coverage for which the employee is enrolled (regardless of whether their employment status is full-time or part-time), additional information needs to be reported on the 1095-C.</span></span> <span data-ttu-id="ff7b8-128">Iga töötaja (sh ülalpeetavad), kelle puhul tööandja toetusega tervisekindlustus kehtib, peavad olema lisatud nende kuude aruandesse, millal neile kindlustus kehtis.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-128">Each employee (including dependents) covered by the employer-sponsored benefit plans needs to be included on the report for the months they were covered.</span></span> 

<span data-ttu-id="ff7b8-129">Saate näidata iga soodustuse plaani kohta, kas see tuleb aruandesse lisada, märkides ruudu **ACA-le esitatav**.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-129">You can indicate whether or not each benefit plan must be reported by selecting the **ACA reportable** check box.</span></span>

<span data-ttu-id="ff7b8-130">Lisaks, kui töötajad on otsustanud lasta oma ülalpeetavatele soodustuse määrata, võite lehel **Soodustuste haldamine** näidata kuupäevad, millal iga töötaja ülalpeetava kaitse kehtis.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-130">In addition, if employees have chosen to have any of their dependents covered under a benefit, you can indicate the dates the dependent was covered for each employee on the **Maintain benefits** page.</span></span> <span data-ttu-id="ff7b8-131">Näitamiseks, et ülalpeetavale kehtib soodustus, valige kiirkaardi **Ülalpeetavad** tegumipaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-131">To indicate that the dependent is covered under the benefit, select the **Edit** button in the action pane of the **Dependents** fast tab.</span></span>

<span data-ttu-id="ff7b8-132">Lehel **Ülalpeetava kindlustuse kuupäevahaldur** saate märkida kuupäevad, millal ülalpeetavale soodustus kehtis.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-132">On the **Dependent coverage date manager** page, you can indicate the dates the dependent was covered by the benefit.</span></span> <span data-ttu-id="ff7b8-133">Kuupäevade sisestamisel sellele lehele märgitakse automaatselt ruut **Kaitstud** lehel **Soodustuste haldamine**.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-133">Entering dates on this page will automatically select the **Covered** checkbox on the **Maintain benefits** page.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="ff7b8-134">Vormide 1095-B ja 1095-C loomine</span><span class="sxs-lookup"><span data-stu-id="ff7b8-134">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="ff7b8-135">Tootest saab luua ka vormid 1095-B ja 1095-C ning jaotada need igale töötajale.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-135">You can also generate 1095-B and 1095-C forms from within the product, and distribute them to each of your employees.</span></span> <span data-ttu-id="ff7b8-136">Süsteem saab elektrooniliselt luua ka 1095-C vorme ja 1094-C IRS-i edastusfaile.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-136">The system can also electronically generate 1095-C forms and the 1094-C IRS transmittal files.</span></span>  

<span data-ttu-id="ff7b8-137">1095-C vormi loomisel sisestage asjakohane maksuaasta ja näidake, kas isikukood peaks olema varjatud.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-137">When generating the 1095-C form, enter the appropriate tax year and indicate if social security numbers should be masked.</span></span> <span data-ttu-id="ff7b8-138">Rohkem kui 500 töötaja 1095-C vormi printimisel saate rohkem kui ühe PDF-faili.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-138">If you're printing 1095-C forms for more than 500 employees, you'll receive more than one PDF file.</span></span> <span data-ttu-id="ff7b8-139">On soovitatav, et suurendate väärtust **Faili maksimummaht** aknas **Dokumendihalduse parameetrid** väärtuseni 150 MB.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-139">It’s recommended that you increase the **Maximum file size** in the **Document management parameters** window to 150 MB.</span></span>

## <a name="viewing-information"></a><span data-ttu-id="ff7b8-140">Teabe vaatamine</span><span class="sxs-lookup"><span data-stu-id="ff7b8-140">Viewing information</span></span>

<span data-ttu-id="ff7b8-141">Lehelt **Töötaja taskukohane ravikindlustus** saate vaadata, millised töötajad on igasse kindlustusgruppi määratud, milliseid töötajaid pole vaja aruandesse lisada ja millised töötajad on määramata.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-141">You can use the **Worker Affordable Care coverage** page to see which employees have been assigned to each coverage group, which employees don’t need to be included on a report, and which employees are unassigned.</span></span>

<span data-ttu-id="ff7b8-142">Kui mõni väärtus taskukohase ravikindlustuse grupist on alistatud, kuvatakse muudetud väärtuse kõrval tärn.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-142">If any of the default values from the Affordable Care coverage group have been overridden, an asterisk will appear next to the value that was changed.</span></span> <span data-ttu-id="ff7b8-143">Kui kõigi 12 kuu väärtused on samad ja neid pole alistatud, prinditakse väärtus veerus **Kõik 12 kuud**.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-143">If the values for all 12 months are the same and haven’t been overridden, the value will print in the **All 12 months** column.</span></span>

<span data-ttu-id="ff7b8-144">Päringuakent saate kasutada ka selleks, et mõista, millised töötajad on märgitud mitte ACA-aruandlusesse kaasatuteks.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-144">You can also use the inquiry window to understand which employees have been flagged as not ACA reportable.</span></span> <span data-ttu-id="ff7b8-145">Te ei pea jälgima, kas neile kindlustuskaitset pakuti ja nende kohta ei ole vaja aasta lõpus esitada vormi 1095-C.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-145">You don’t need to track whether coverage was offered to them and won't need to issue a 1095-C to them at the end of the year.</span></span> <span data-ttu-id="ff7b8-146">Kõigi selliste töötajate loendi loomiseks, kes ei saa vormi 1095-c valige suvand **Ei ole ACA-le esitatav** väljal **Filtreerimisalus**.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-146">Select **Not ACA reportable** in the **Filter by** field to generate a list of all employees who won't receive a 1095-C.</span></span>

<span data-ttu-id="ff7b8-147">Lisaks saate vaadata ka töötajaid, kes on määramata (väli **ACA aruandesse kuuluv** on tühi) või kes on määratud taskukohase ravikindlustuse gruppi, mis on väljal **Aasta** valitud aasta puhul aegunud.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-147">In addition, you can view any employees who are unassigned (the **ACA Report coverage** field is empty) or who have been assigned to an Affordable Care coverage group that is expired for the year selected in the **Year** field.</span></span>

<span data-ttu-id="ff7b8-148">Saate koostatud töötajate nimekirju eksportida, kasutades mis tahes Exceli filtreerimisvalikuid.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-148">You can export lists of employees that were generated using any of the filtering options to Excel.</span></span>

<span data-ttu-id="ff7b8-149">Kui peate kindlustuskaitsega inimestest teatama, sest pakute isekindlustuskaitset, saate vaadata ülalpeetavaid, kes on soodustusplaanidega kaitstud ja märgitud kui **ACA-aruandele lisatavad**.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-149">If you need to report covered individuals because you provide self-insured coverage, you can view any dependents covered under benefit plans marked as **ACA reportable**.</span></span> <span data-ttu-id="ff7b8-150">Valige toimingupaanil nupp **Vaata ülalpeetavate kindlustuskaitset**.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-150">Select **View Dependent coverage** on the action pane.</span></span>

> [!NOTE]
> <span data-ttu-id="ff7b8-151">Päringuaknas kuvatakse ainult soodustusplaanid, mis on märgitud kui **ACA-aruandele lisatavad**.</span><span class="sxs-lookup"><span data-stu-id="ff7b8-151">Only benefit plans marked as **ACA reportable** display in the inquiry window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]