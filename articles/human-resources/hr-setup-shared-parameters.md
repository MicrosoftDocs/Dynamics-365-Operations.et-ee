---
title: Ühisparameetrite konfigureerimine
description: Ettevõtete vahel ühiskasutuses olevate kirjete (nt ametikoha kirjete) puhul tuleb seadistada jagatud parameetrid. See artikkel selgitab juriidiliste isikute vahel inimressursside parameetrite seadistamist.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: abcaf42a2e8b227e2c7c1b07ed61ea005832667a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802379"
---
# <a name="configure-shared-parameters"></a><span data-ttu-id="acd96-104">Ühisparameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="acd96-104">Configure shared parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="acd96-105">Ettevõtete vahel ühiskasutuses olevate kirjete (nt ametikoha kirjete) puhul tuleb seadistada jagatud parameetrid.</span><span class="sxs-lookup"><span data-stu-id="acd96-105">You must set up shared parameters for records that are shared across companies, such as Position records.</span></span> <span data-ttu-id="acd96-106">See artikkel selgitab juriidiliste isikute vahel inimressursside parameetrite seadistamist.</span><span class="sxs-lookup"><span data-stu-id="acd96-106">This article explains how to set up Human resources parameters across legal entities.</span></span>

<span data-ttu-id="acd96-107">Mõnd tüüpi kirjeid, nt ametikohakirjeid, ühiskasutatakse kõikides ettevõtetes.</span><span class="sxs-lookup"><span data-stu-id="acd96-107">Some types of records, such as Position records, are shared across companies.</span></span> <span data-ttu-id="acd96-108">Nende kirjete puhul peate seadistama ühiskasutatavad parameetrid.</span><span class="sxs-lookup"><span data-stu-id="acd96-108">For these records, you must set up shared parameters.</span></span> <span data-ttu-id="acd96-109">Kasutate näiteks lehte **Inimressursside ühiskasutusega parameetrid**, et seadistada inimressursside parameetrid juriidilistele isikutele.</span><span class="sxs-lookup"><span data-stu-id="acd96-109">For example, you use the **Human resources shared parameters** page to set up Human resources parameters across legal entities.</span></span> 

<span data-ttu-id="acd96-110">Lehel **Inimressursside ühiskasutusega parameetrid** on parameetrid rühmitatud piirkondadeks nende funktsiooni põhjal.</span><span class="sxs-lookup"><span data-stu-id="acd96-110">On the **Human resources shared parameters** page, parameters are grouped into areas, based on their functionality.</span></span> 

### <a name="previously-released-functionality"></a><span data-ttu-id="acd96-111">Varem välja antud funktsioonid</span><span class="sxs-lookup"><span data-stu-id="acd96-111">Previously released functionality</span></span>
<span data-ttu-id="acd96-112">Vahekaardil **ID** peate valima ID tüübid, mis esindavad lehel loetletud ID-koode.</span><span class="sxs-lookup"><span data-stu-id="acd96-112">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="acd96-113">Peate seadistama ID tüübid enne, kui saate töötajatele ID teavet sisestada.</span><span class="sxs-lookup"><span data-stu-id="acd96-113">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="acd96-114">Teave isikukoodi, rahvusliku ID-koodi, välismaalase ID-koodi ja isikliku ID-koodi kohta säilitatakse lehel **ID tüüp**.</span><span class="sxs-lookup"><span data-stu-id="acd96-114">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="acd96-115">Uue ID tüübi määratlemiseks või olemasolevate tüüpide loendi ülevaatamiseks klõpsake valikuid **Personalijuhtimine** &gt; **Linkide vahekaart** &gt; **Seadistus** &gt; **Identifikatsiooni tüübid**.</span><span class="sxs-lookup"><span data-stu-id="acd96-115">To define a new identification type or review the list of existing types, click **Personnel management** &gt; **Links tab** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="acd96-116">Saate sisestada lihtsa koodi ja kirjelduse.</span><span class="sxs-lookup"><span data-stu-id="acd96-116">You can enter a simple code and description.</span></span> 

### <a name="if-youre-using-dynamics-365-human-resources"></a><span data-ttu-id="acd96-117">Rakenduse Dynamics 365 Human Resources kasutamisel</span><span class="sxs-lookup"><span data-stu-id="acd96-117">If you're using Dynamics 365 Human Resources</span></span>
<span data-ttu-id="acd96-118">Vahekaardil **ID** peate valima ID tüübid, mis esindavad lehel loetletud ID-koode.</span><span class="sxs-lookup"><span data-stu-id="acd96-118">On the **Identification** tab, you must select the identification types that represent the identification numbers that are listed on the page.</span></span> <span data-ttu-id="acd96-119">Peate seadistama ID tüübid enne, kui saate töötajatele ID teavet sisestada.</span><span class="sxs-lookup"><span data-stu-id="acd96-119">You must set up identification types before you can enter identification information for workers.</span></span> <span data-ttu-id="acd96-120">Teave isikukoodi, rahvusliku ID-koodi, välismaalase ID-koodi ja isikliku ID-koodi kohta säilitatakse lehel **ID tüüp**.</span><span class="sxs-lookup"><span data-stu-id="acd96-120">Information about the Social Security number, national ID number, alien ID number, and personal ID code is maintained on the **Identification type** page.</span></span> <span data-ttu-id="acd96-121">Uue ID tüübi määratlemiseks või olemasolevate tüüpide loendi ülevaatamiseks klõpsake suvandeid **Inimressursid** &gt; **Seadistus** &gt; **Identifikatsiooni tüübid**.</span><span class="sxs-lookup"><span data-stu-id="acd96-121">To define a new identification type or review the list of existing types, click **Human resources** &gt; **Setup** &gt; **Identification types**.</span></span> <span data-ttu-id="acd96-122">Saate sisestada lihtsa koodi ja kirjelduse.</span><span class="sxs-lookup"><span data-stu-id="acd96-122">You can enter a simple code and description.</span></span> 

<span data-ttu-id="acd96-123">Vahekaardil **Numbriseeriad** saate valida numbriseeriad, mida kasutatakse järgmiste kirjete puhul: Personalinumber, Ametikoht, Kasutajanõude ID, I-9 dokument, Kandidaat, Arutelu, Soodustuse ID ja Personalitoiming (kui see kirje tüüp on lubatud).</span><span class="sxs-lookup"><span data-stu-id="acd96-123">On the **Number sequences** tab, you can select the number sequences that are used for the following records: Personnel number, Position, User request ID, I-9 document, Applicant, Discussion, Benefit ID, and Personnel action (if this record type is enabled).</span></span> <span data-ttu-id="acd96-124">Numbriseeria viidete ja koodide säilitamiseks kasutage loendilehte **Numbriseeriad**.</span><span class="sxs-lookup"><span data-stu-id="acd96-124">To maintain number sequence references and codes, use the **Number sequences** list page.</span></span> <span data-ttu-id="acd96-125">Selle lehe leidmiseks kasutage lehe otsimise funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="acd96-125">To find this page, use the page search feature.</span></span> 

<span data-ttu-id="acd96-126">Osutage vahekaardil **Ametikohad**, kas määramisele on saadaval vaikimisi uusi ametikohti.</span><span class="sxs-lookup"><span data-stu-id="acd96-126">On the **Positions** tab, indicate whether new positions are available for assignment by default:</span></span>

-   <span data-ttu-id="acd96-127">**Alati** – ametikohtade loomisel saate töötajaid uutele ametikohtadele määrata.</span><span class="sxs-lookup"><span data-stu-id="acd96-127">**Always** – You can assign workers to new positions when positions are created.</span></span> <span data-ttu-id="acd96-128">Ametikohtade loomisel seatakse valiku **Määramiseks saadaval** kuupäev ja kellaaeg lehe **Ametikoht** vahekaardil **Üldine** automaatselt loomise kuupäevale ja kellaajale.</span><span class="sxs-lookup"><span data-stu-id="acd96-128">When positions are created, the **Available for assignment** date and time on the **General** tab of the **Position** page are automatically set to the creation date and time.</span></span>
-   <span data-ttu-id="acd96-129">**Mitte kunagi** – töötajaid ei saa ametikohtade loomisel uutele ametikohtadele määrata.</span><span class="sxs-lookup"><span data-stu-id="acd96-129">**Never** – You can't assign workers to new positions when positions are created.</span></span> <span data-ttu-id="acd96-130">Selle suvandi valimisel peata avama lehe **Ametikoht** iga uue ametikoha jaoks kohe, kui see muutub kättesaadavaks, ja sisestama siis vahekaardile **Üldine** suvandi **Määramiseks saadaval** kuupäeva, et lubada töötaja määramine.</span><span class="sxs-lookup"><span data-stu-id="acd96-130">If you select this option, you must open the **Position** page for each new position as it becomes available, and then, on the **General** tab, enter the **Available for assignment** date to enable worker assignment.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]