--- 
title: Konfiguratsioonide kujundus dokumentide loomiseks rakendusandmetega
description: "Selle protseduuri toimingute lõpule viimiseks peate esmalt teostama protseduuri „ER Avalduse andmete värskendusega dokumentide genereerimine (1. osa – konfiguratsioonide import)“."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c883897b63decdbf983e3294899adc20b20e319f
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="design-configurations-to-generate-documents-with-application-data"></a><span data-ttu-id="9e055-103">Konfiguratsioonide kujundus dokumentide loomiseks rakendusandmetega</span><span class="sxs-lookup"><span data-stu-id="9e055-103">Design configurations to generate documents with application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9e055-104">Selle protseduuri toimingute lõpule viimiseks peate esmalt teostama protseduuri "ER Avalduse andmete värskendusega dokumentide genereerimine (1.</span><span class="sxs-lookup"><span data-stu-id="9e055-104">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="9e055-105">Konfiguratsioonipakkuja loomine ja aktiivseks märkimine".</span><span class="sxs-lookup"><span data-stu-id="9e055-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="9e055-106">Selles protseduuris selgitatakse, kuidas kasutada imporditud näidisettevõtte Litware, Inc. jaoks loodud elektroonilise aruandluse (ER) konfiguratsioone elektroonilise dokumendi genereerimiseks.</span><span class="sxs-lookup"><span data-stu-id="9e055-106">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="9e055-107">Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll.</span><span class="sxs-lookup"><span data-stu-id="9e055-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="9e055-108">Need toimingud saab lõpule viia DEMF-i andmekomplekti abil.</span><span class="sxs-lookup"><span data-stu-id="9e055-108">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="9e055-109">Enne alustamist asendage DEMF-ettevõtte riigikontekst DEU (Saksamaa) kontekstiga BEL (Belgia).</span><span class="sxs-lookup"><span data-stu-id="9e055-109">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="9e055-110">Juriidilise isiku DEMF esmase aadressi riigikoodi värskendamiseks avage Organisatsioonihaldus > Organisatsioonid > Juriidilised isikud.</span><span class="sxs-lookup"><span data-stu-id="9e055-110">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="9e055-111">Taaskäivitage avaldus.</span><span class="sxs-lookup"><span data-stu-id="9e055-111">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="9e055-112">Imporditud ER-vormingu käivitamine</span><span class="sxs-lookup"><span data-stu-id="9e055-112">Run imported ER format</span></span>
1. <span data-ttu-id="9e055-113">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="9e055-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="9e055-114">Laiendage puul valikut „Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="9e055-114">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="9e055-115">Tehke puul valik „Intrastat (model)\Intrastat (format)".</span><span class="sxs-lookup"><span data-stu-id="9e055-115">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="9e055-116">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="9e055-116">Click Run.</span></span>
    * <span data-ttu-id="9e055-117">Intrastat-aruande genereerimiseks käivitage elektroonilise aruandluse (ER) vormingu konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="9e055-117">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="9e055-118">Sisestage valiku Sisesta fail nimeväljale „intrastat.xml".</span><span class="sxs-lookup"><span data-stu-id="9e055-118">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="9e055-119">Määrake faili nimi.</span><span class="sxs-lookup"><span data-stu-id="9e055-119">Specify the name of the file.</span></span>  
6. <span data-ttu-id="9e055-120">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9e055-120">Click OK.</span></span>
    * <span data-ttu-id="9e055-121">Vaadake genereeritud XML-fail üle.</span><span class="sxs-lookup"><span data-stu-id="9e055-121">Review the generated XML file.</span></span>  
7. <span data-ttu-id="9e055-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9e055-122">Close the page.</span></span>
8. <span data-ttu-id="9e055-123">Avage Maks > Deklaratsioonid > Väliskaubandus > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="9e055-123">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="9e055-124">Avage see vorm genereeritud elektroonilisse dokumenti kaasatud Intrastati kannete vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="9e055-124">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="9e055-125">Klõpsake valikut „Intrastat archive".</span><span class="sxs-lookup"><span data-stu-id="9e055-125">Click Intrastat archive.</span></span>
    * <span data-ttu-id="9e055-126">Kuna käivitatud elektroonilise aruandluse vorming ei sisalda ühtegi avalduse andmete värskenduse sätet, pole lõpule viidud Intrastat-aruande üksikasjad arhiivitud.</span><span class="sxs-lookup"><span data-stu-id="9e055-126">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="9e055-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9e055-127">Close the page.</span></span>
11. <span data-ttu-id="9e055-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9e055-128">Close the page.</span></span>


