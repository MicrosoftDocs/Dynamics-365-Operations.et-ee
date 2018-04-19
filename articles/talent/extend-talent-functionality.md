---
title: "Teenuse Microsoft Dynamics 365 for Talent võimaluste laiendamine"
description: "Kui olete loonud Microsoft PowerAppse, saate need rakendused käivitada teenuses Microsoft Dynamics 365 for Talent olevate linkide kaudu."
author: rschloma
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: fbd5335f64865dfe6122d88b3bc45ec614fc0677
ms.openlocfilehash: c01a8f0106ee1181e973da50d428b8fc5e6e5a06
ms.contentlocale: et-ee
ms.lasthandoff: 04/19/2018

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a><span data-ttu-id="1d90c-103">Teenuse Microsoft Dynamics 365 for Talent võimaluste laiendamine</span><span class="sxs-lookup"><span data-stu-id="1d90c-103">Extend the functionality of Microsoft Dynamics 365 for Talent</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="1d90c-104">Kui olete loonud Microsoft PowerAppse, saate need rakendused käivitada teenuses Microsoft Dynamics 365 for Talent olevate linkide kaudu.</span><span class="sxs-lookup"><span data-stu-id="1d90c-104">If you’ve created any Microsoft PowerApps, you can start those applications from links within Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="1d90c-105">Rakendustele juurdepääsu seadistamiseks peate teenuses Talent konfiguratsiooni lehel seadistama teavet, konfiguratsiooni lehe saate avada tööruumis **Süsteemihaldus**.</span><span class="sxs-lookup"><span data-stu-id="1d90c-105">To set up access to your applications, you’ll need to set up some information in Talent on a configuration page that you can open from the **System administration** workspace.</span></span>

## <a name="configuring-embedded-powerapps-within-talent"></a><span data-ttu-id="1d90c-106">Manustatud PowerAppsi konfigureerimine teenuses Talent</span><span class="sxs-lookup"><span data-stu-id="1d90c-106">Configuring embedded PowerApps within Talent</span></span>
<span data-ttu-id="1d90c-107">Kasutage lehte **Manustatud Microsoft PowerAppsi seadistamine**, et konfigureerida teenuse Talent lehed käivitama PowerAppsi rakendusi.</span><span class="sxs-lookup"><span data-stu-id="1d90c-107">Use the **Set embedded Microsoft PowerApps** page to configure Talent pages to start PowerApps applications.</span></span> <span data-ttu-id="1d90c-108">Lehe **Manustatud Microsoft PowerAppsi seadistamine** avamiseks avage tööruum **Süsteemihaldus** ja seejärel avage vahekaart **Lingid**. Valige **Microsoft PowerApps** grupist **Seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="1d90c-108">To open the **Set embedded Microsoft PowerApps** page, open the **System administration** workspace and then open the **Links** tab. Select **Microsoft PowerApps** from the **Setup** group.</span></span> 

<span data-ttu-id="1d90c-109">Sellel lehel saab sisestada või seadistada järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="1d90c-109">The following information is entered or set on this page:</span></span> 

 -  <span data-ttu-id="1d90c-110">Iga PowerAppsi rakenduse kirjeldav nimi või identifikaator.</span><span class="sxs-lookup"><span data-stu-id="1d90c-110">A descriptive name or identifier for each PowerApps application.</span></span>
 -  <span data-ttu-id="1d90c-111">Kordumatu ID (GUID) iga rakenduse jaoks, mille lisate teenuse Talent lehel.</span><span class="sxs-lookup"><span data-stu-id="1d90c-111">A unique identifier (GUID) for each application that you add to a Talent page.</span></span> <span data-ttu-id="1d90c-112">Rakenduse ID on saadaval PowerAppsi saidil [powerapps.com](http://powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="1d90c-112">The app ID is available on the PowerApps site, [powerapps.com](http://powerapps.com/).</span></span> 
 -  <span data-ttu-id="1d90c-113">Leht, millelt kasutajad saavad avada rakendust või aruannet.</span><span class="sxs-lookup"><span data-stu-id="1d90c-113">The page from which users can open an application or report.</span></span> <span data-ttu-id="1d90c-114">Mõned teenuse Talent lehed ei toeta manustatud PowerAppsi ja Power BI aruandeid.</span><span class="sxs-lookup"><span data-stu-id="1d90c-114">Not all Talent pages support embedded PowerApps and Power BI reports.</span></span> 

 > [!NOTE]
 >  <span data-ttu-id="1d90c-115">Sisestage lehe sisemine nimi, mitte lehe ülaosas olev kuvatav nimi.</span><span class="sxs-lookup"><span data-stu-id="1d90c-115">Enter the internal name of the page, rather than the display name that appears at the top of the page.</span></span> <span data-ttu-id="1d90c-116">Sisemise nime leidmiseks avage leht, mille sisemist nime te vajate ja paremklõpsake lehel mis tahes kohas.</span><span class="sxs-lookup"><span data-stu-id="1d90c-116">To find the internal name, open the page that you need the internal name of, and right-click anywhere on the page.</span></span> <span data-ttu-id="1d90c-117">Menüü avanemisel liikuge üksuse **Vormi teave** kohale.</span><span class="sxs-lookup"><span data-stu-id="1d90c-117">When the menu opens, hover over the **Form information** item.</span></span> <span data-ttu-id="1d90c-118">Sisemise vormi nimi kuvatakse menüüs üksuse **Vormi teave** kõrval.</span><span class="sxs-lookup"><span data-stu-id="1d90c-118">The internal form name is displayed next to the **Form information** item in the menu.</span></span>
 
-   <span data-ttu-id="1d90c-119">Määrake vormi juhtelement, millelt rakendus saab hankida konteksti andmeid.</span><span class="sxs-lookup"><span data-stu-id="1d90c-119">Specify the form control from which the application can retrieve context data.</span></span> <span data-ttu-id="1d90c-120">Näiteks võib rakendus kasutada andmeid töötaja kohta.</span><span class="sxs-lookup"><span data-stu-id="1d90c-120">For example, an application might use data about a worker.</span></span> <span data-ttu-id="1d90c-121">Kui sisestate väljal **Kontekst** lehe **Töötaja**, avaneb leht **Töötaja** rakenduse käivitamisel.</span><span class="sxs-lookup"><span data-stu-id="1d90c-121">If you enter the **Worker** page in the **Context** field, the **Worker** page will open when you start the application.</span></span> <span data-ttu-id="1d90c-122">Kirje valikus **Kontekstiväli** on valikuline.</span><span class="sxs-lookup"><span data-stu-id="1d90c-122">An entry in the **Context field** is optional.</span></span> 
-   <span data-ttu-id="1d90c-123">Määrake dialoogiboksi suurus, milles PowerAppsi rakendus edaspidi töötab.</span><span class="sxs-lookup"><span data-stu-id="1d90c-123">Set the size of the dialog box on which the PowerApps application will run.</span></span> <span data-ttu-id="1d90c-124">Dialoogiboksid on määratud kui „väikesed” või „suured”, et optimeerida kasutajaliidest, kui teie rakendus töötab vastavalt telefonis või suuremas seadmes.</span><span class="sxs-lookup"><span data-stu-id="1d90c-124">The dialog boxes are designated as “small” or “large” to optimize the user interface when your application for running on a phone or a larger device, respectively.</span></span> 


<span data-ttu-id="1d90c-125">Samuti saate määrata, milliste juriidiliste isikute jaoks on rakendus saadaval, või saate selle kõigile oma juriidilistele isikutele kättesaadavaks teha.</span><span class="sxs-lookup"><span data-stu-id="1d90c-125">You can also specify which legal entities an application will be available for, or you can make it available to all your legal entities.</span></span> <span data-ttu-id="1d90c-126">Vaikimisi on teie PowerAppsi rakendused saadaval kõigile juriidilistele isikutele.</span><span class="sxs-lookup"><span data-stu-id="1d90c-126">By default, your PowerApps applications are available to all legal entities.</span></span>

## <a name="opening-an-application"></a><span data-ttu-id="1d90c-127">Rakenduse avamine</span><span class="sxs-lookup"><span data-stu-id="1d90c-127">Opening an application</span></span>
<span data-ttu-id="1d90c-128">Kui olete konfigureerinud manustatud PowerAppsi rakendused, lisatakse teie määratud rakenduste lingid teenuses Talent olevatele lehtedele.</span><span class="sxs-lookup"><span data-stu-id="1d90c-128">When you’ve configured embedded PowerApps applications, links to the applications that you specified will be added to the pages within Talent.</span></span> <span data-ttu-id="1d90c-129">Rakenduse avamiseks klõpsake linki.</span><span class="sxs-lookup"><span data-stu-id="1d90c-129">Click a link to open an application.</span></span> 



