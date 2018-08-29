---
title: Juriidilistele isikutele inimressursside (HR) parameetrite seadistamine
description: "Ettevõtete vahel ühiskasutuses olevate kirjete (nt ametikoha kirjete) puhul tuleb seadistada jagatud parameetrid. See artikkel selgitab juriidiliste isikute vahel inimressursside parameetrite seadistamist."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: cc5acf7ba1b350ee2c91923c7de3b4780385f3ef
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---

# <a name="set-up-human-resources-hr-parameters-across-legal-entities"></a><span data-ttu-id="957b6-104">Juriidilistele isikutele inimressursside (HR) parameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="957b6-104">Set up Human resources (HR) parameters across legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="957b6-105">Ettevõtete vahel ühiskasutuses olevate kirjete (nt ametikoha kirjete) puhul tuleb seadistada jagatud parameetrid.</span><span class="sxs-lookup"><span data-stu-id="957b6-105">You must set up shared parameters for records that are shared across companies, such as Position records.</span></span> <span data-ttu-id="957b6-106">See artikkel selgitab juriidiliste isikute vahel inimressursside parameetrite seadistamist.</span><span class="sxs-lookup"><span data-stu-id="957b6-106">This article explains how to set up Human resources parameters across legal entities.</span></span>

<span data-ttu-id="957b6-107">Mõnd tüüpi kirjeid, nt ametikohakirjeid, ühiskasutatakse kõikides ettevõtetes.</span><span class="sxs-lookup"><span data-stu-id="957b6-107">Some types of records, such as Position records, are shared across companies.</span></span> <span data-ttu-id="957b6-108">Nende kirjete puhul peate seadistama ühiskasutatavad parameetrid.</span><span class="sxs-lookup"><span data-stu-id="957b6-108">For these records, you must set up shared parameters.</span></span> <span data-ttu-id="957b6-109">Kasutate näiteks lehte **Inimressursside ühiskasutusega parameetrid**, et seadistada inimressursside parameetrid juriidilistele isikutele.</span><span class="sxs-lookup"><span data-stu-id="957b6-109">For example, you use the **Human resources shared parameters** page to set up Human resources parameters across legal entities.</span></span> 

<span data-ttu-id="957b6-110">Lehel **Inimressursside ühiskasutusega parameetrid** on parameetrid rühmitatud piirkondadeks nende funktsiooni põhjal.</span><span class="sxs-lookup"><span data-stu-id="957b6-110">On the **Human resources shared parameters** page, parameters are grouped into areas, based on their functionality.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="957b6-111">Varem välja antud funktsioonid</span><span class="sxs-lookup"><span data-stu-id="957b6-111">Previously released functionality</span></span>
<span data-ttu-id="957b6-112">Vahekaardil **ID** peate valima ID tüübid, mis esindavad lehel loetletud ID-koode.</span><span class="sxs-lookup"><span data-stu-id="957b6-112">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="957b6-113">Peate seadistama ID tüübid enne, kui saate töötajatele ID teavet sisestada.</span><span class="sxs-lookup"><span data-stu-id="957b6-113">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="957b6-114">Teave isikukoodi, rahvusliku ID-koodi, välismaalase ID-koodi ja isikliku ID-koodi kohta säilitatakse lehel **ID tüüp**.</span><span class="sxs-lookup"><span data-stu-id="957b6-114">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="957b6-115">Uue ID tüübi määratlemiseks või olemasolevate tüüpide loendi ülevaatamiseks klõpsake valikuid **Personalijuhtimine** &gt; **Linkide vahekaart** &gt; **Seadistus** &gt; **Identifikatsiooni tüübid**.</span><span class="sxs-lookup"><span data-stu-id="957b6-115">To define a new identification type or review the list of existing types, click **Personnel management** &gt; **Links tab** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="957b6-116">Saate sisestada lihtsa koodi ja kirjelduse.</span><span class="sxs-lookup"><span data-stu-id="957b6-116">You can enter a simple code and description.</span></span> 

### <a name="if-youre-using-dynamics-365-for-talent"></a><span data-ttu-id="957b6-117">Kui kasutate Dynamics 365 for Talentit</span><span class="sxs-lookup"><span data-stu-id="957b6-117">If you're using Dynamics 365 for Talent</span></span>
<span data-ttu-id="957b6-118">Vahekaardil **ID** peate valima ID tüübid, mis esindavad lehel loetletud ID-koode.</span><span class="sxs-lookup"><span data-stu-id="957b6-118">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="957b6-119">Peate seadistama ID tüübid enne, kui saate töötajatele ID teavet sisestada.</span><span class="sxs-lookup"><span data-stu-id="957b6-119">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="957b6-120">Teave isikukoodi, rahvusliku ID-koodi, välismaalase ID-koodi ja isikliku ID-koodi kohta säilitatakse lehel **ID tüüp**.</span><span class="sxs-lookup"><span data-stu-id="957b6-120">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="957b6-121">Uue ID tüübi määratlemiseks või olemasolevate tüüpide loendi ülevaatamiseks klõpsake suvandeid **Inimressursid** &gt; **Seadistus** &gt; **Identifikatsiooni tüübid**.</span><span class="sxs-lookup"><span data-stu-id="957b6-121">To define a new identification type or review the list of existing types, click **Human resources** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="957b6-122">Saate sisestada lihtsa koodi ja kirjelduse.</span><span class="sxs-lookup"><span data-stu-id="957b6-122">You can enter a simple code and description.</span></span> 

<span data-ttu-id="957b6-123">Vahekaardil **Numbriseeriad** saate valida numbriseeriad, mida kasutatakse järgmiste kirjete puhul: Personalinumber, Ametikoht, Kasutajanõude ID, I-9 dokument, Kandidaat, Arutelu, Soodustuse ID ja Personalitoiming (kui see kirje tüüp on lubatud).</span><span class="sxs-lookup"><span data-stu-id="957b6-123">On the **Number sequences** tab, you can select the number sequences that are used for the following records: Personnel number, Position, User request ID, I-9 document, Applicant, Discussion, Benefit ID, and Personnel action (if this record type is enabled).</span></span> <span data-ttu-id="957b6-124">Numbriseeria viidete ja koodide säilitamiseks kasutage loendilehte **Numbriseeriad**.</span><span class="sxs-lookup"><span data-stu-id="957b6-124">To maintain number sequence references and codes, use the **Number sequences** list page.</span></span> <span data-ttu-id="957b6-125">Selle lehe leidmiseks kasutage lehe otsimise funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="957b6-125">To find this page, use the page search feature.</span></span> 

<span data-ttu-id="957b6-126">Osutage vahekaardil **Ametikohad**, kas määramisele on saadaval vaikimisi uusi ametikohti.</span><span class="sxs-lookup"><span data-stu-id="957b6-126">On the **Positions** tab, indicate whether new positions are available for assignment by default:</span></span>

-   <span data-ttu-id="957b6-127">**Alati** – ametikohtade loomisel saate töötajaid uutele ametikohtadele määrata.</span><span class="sxs-lookup"><span data-stu-id="957b6-127">**Always** – You can assign workers to new positions when positions are created.</span></span> <span data-ttu-id="957b6-128">Ametikohtade loomisel seatakse valiku **Määramiseks saadaval** kuupäev ja kellaaeg lehe **Ametikoht** vahekaardil **Üldine** automaatselt loomise kuupäevale ja kellaajale.</span><span class="sxs-lookup"><span data-stu-id="957b6-128">When positions are created, the **Available for assignment** date and time on the **General** tab of the **Position** page are automatically set to the creation date and time.</span></span>
-   <span data-ttu-id="957b6-129">**Mitte kunagi** – töötajaid ei saa ametikohtade loomisel uutele ametikohtadele määrata.</span><span class="sxs-lookup"><span data-stu-id="957b6-129">**Never** – You can't assign workers to new positions when positions are created.</span></span> <span data-ttu-id="957b6-130">Selle suvandi valimisel peata avama lehe **Ametikoht** iga uue ametikoha jaoks kohe, kui see muutub kättesaadavaks, ja sisestama siis vahekaardile **Üldine** suvandi **Määramiseks saadaval** kuupäeva, et lubada töötaja määramine.</span><span class="sxs-lookup"><span data-stu-id="957b6-130">If you select this option, you must open the **Position** page for each new position as it becomes available, and then, on the **General** tab, enter the **Available for assignment** date to enable worker assignment.</span></span>


<a name="additional-resources"></a><span data-ttu-id="957b6-131">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="957b6-131">Additional resources</span></span>
--------

[<span data-ttu-id="957b6-132">Ettevõttekohaste inimressursside parameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="957b6-132">Set up company specific HR parameters</span></span>](set-up-company-specific-hr-parameters.md)




