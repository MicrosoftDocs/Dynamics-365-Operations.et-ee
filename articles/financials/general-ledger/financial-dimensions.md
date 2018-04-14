---
title: Finantsdimensioonid
description: "Selles teemas kirjeldatakse mitmesuguseid finantsdimensioonide tüüpe ja nende seadistamist."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3d3423b1d3cc235fa10f0a26aa5cd880d08be45b
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="financial-dimensions"></a><span data-ttu-id="142c4-103">Finantsdimensioonid</span><span class="sxs-lookup"><span data-stu-id="142c4-103">Financial dimensions</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="142c4-104">Selles teemas selgitatakse mitmesuguseid finantsdimensioonide tüüpe ja nende seadistamist.</span><span class="sxs-lookup"><span data-stu-id="142c4-104">This topic explains the various types of financial dimensions and how they are set up.</span></span>

<span data-ttu-id="142c4-105">Kasutage lehte **Finantsdimensioonid**, et luua finantsdimensioonid, mida saab kasutada kontosegmentidena kontoplaanide puhul.</span><span class="sxs-lookup"><span data-stu-id="142c4-105">Use the **Financial dimensions** page to create financial dimensions that you can use as account segments for charts of accounts.</span></span> <span data-ttu-id="142c4-106">Finantsdimensioone on kaht tüüpi: kohandatud dimensioonid ja üksuse tagatud dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="142c4-106">There are two types of financial dimensions: custom dimensions and entity-backed dimensions.</span></span> <span data-ttu-id="142c4-107">Kohandatud dimensioone kasutavad juriidilised isikud ühiselt ning väärtusi sisestavad ja haldavad kasutajad.</span><span class="sxs-lookup"><span data-stu-id="142c4-107">Custom dimensions are shared across legal entities, and the values are entered and maintained by users.</span></span> <span data-ttu-id="142c4-108">Üksuse tagatud dimensioonide puhul määratletakse väärtused mujal süsteemis, nt üksustes Kliendid või Kauplused.</span><span class="sxs-lookup"><span data-stu-id="142c4-108">For entity-backed dimensions, the values are defined somewhere else in the system, such as Customers or Stores entities.</span></span> <span data-ttu-id="142c4-109">Mõnda üksuse tagatud dimensiooni kasutavad juriidilised isikud ühiselt, samas kui mõni on ettevõttekohane.</span><span class="sxs-lookup"><span data-stu-id="142c4-109">Some entity-backed dimensions are shared across legal entities, whereas other entity-backed dimensions are company-specific.</span></span> 

<span data-ttu-id="142c4-110">Kui olete finantsdimensioonid loonud, kasutage igale finantsdimensioonile täiendavate atribuutide lisamiseks lehte **Finantsdimensiooni väärtused**.</span><span class="sxs-lookup"><span data-stu-id="142c4-110">After you've created the financial dimensions, use the **Financial dimension values** page to assign additional properties to each financial dimension.</span></span> 

<span data-ttu-id="142c4-111">Finantsdimensioone saab kasutada juriidiliste isikute kajastamiseks.</span><span class="sxs-lookup"><span data-stu-id="142c4-111">You can use financial dimensions to represent legal entities.</span></span> <span data-ttu-id="142c4-112">Rakenduses Microsoft Dynamics 365 for Finance and Operations ei pea juriidilisi isikuid looma.</span><span class="sxs-lookup"><span data-stu-id="142c4-112">You don't have to create the legal entities in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="142c4-113">Kuid finantsdimensioonid pole mõeldud juriidiliste isikute tegevus- või ärivajaduste rahuldamiseks.</span><span class="sxs-lookup"><span data-stu-id="142c4-113">However, financial dimensions aren’t designed to address the operational or business requirements of legal entities.</span></span> <span data-ttu-id="142c4-114">Üksustevaheline raamatupidamisfunktsioon rakenduses Finance and Operations on mõeldud ainult iga kande loodavate raamatupidamiskirjete käsitlemiseks.</span><span class="sxs-lookup"><span data-stu-id="142c4-114">The interunit accounting functionality in Finance and Operations is designed to address only the accounting entries that are created by each transaction.</span></span> 

<span data-ttu-id="142c4-115"> Finantsdimensioonide juriidilised isikud häälestamiseks hinnata äriprotsessist järgmistes määratlemiseks, kui teie organisatsioon töö see seadistus:</span><span class="sxs-lookup"><span data-stu-id="142c4-115">Before you set up financial dimensions as legal entities, evaluate your business processes in the following areas to determine whether this setup will work for your organization:</span></span>

- <span data-ttu-id="142c4-116">Varud</span><span class="sxs-lookup"><span data-stu-id="142c4-116">Inventory</span></span>
- <span data-ttu-id="142c4-117">Müügi ja ostu finantsdimensioonide ja juriidilised isikud</span><span class="sxs-lookup"><span data-stu-id="142c4-117">Sales and purchases between financial dimensions and legal entities</span></span>
- <span data-ttu-id="142c4-118">Käibemaksuaruandluse koodi genereerimine</span><span class="sxs-lookup"><span data-stu-id="142c4-118">Sales tax calculation and reporting</span></span>
- <span data-ttu-id="142c4-119">Tegevuse aruandlus</span><span class="sxs-lookup"><span data-stu-id="142c4-119">Operational reporting</span></span>

<span data-ttu-id="142c4-120">Siin on mõned neist piirangutest.</span><span class="sxs-lookup"><span data-stu-id="142c4-120">Here are some of the limitations:</span></span>

- <span data-ttu-id="142c4-121">Ainult juriidiliste isikutega, finantsdimensioonide, saate käibemaksu funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="142c4-121">You can use sales tax functionality only with legal entities, not with financial dimensions.</span></span>
- <span data-ttu-id="142c4-122">Mõned aruanded ei sisalda finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="142c4-122">Some reports don't include financial dimensions.</span></span> <span data-ttu-id="142c4-123">Seega võib finantsdimensioonide alusel aruande koostamiseks olla vaja aruandeid muuta.</span><span class="sxs-lookup"><span data-stu-id="142c4-123">Therefore, to report by financial dimension, you might have to modify the reports.</span></span>

## <a name="custom-dimensions"></a><span data-ttu-id="142c4-124">Kohandatud dimensioonid</span><span class="sxs-lookup"><span data-stu-id="142c4-124">Custom dimensions</span></span>

<span data-ttu-id="142c4-125">Kasutaja määratletud finantsdimensiooni loomiseks tehke väljal **Kasuta väärtusi allikast** valik **&lt; Kohandatud dimensioon &gt;**.</span><span class="sxs-lookup"><span data-stu-id="142c4-125">To create a user-defined financial dimension, in the **Use values from** field, select **&lt; Custom dimension &gt;**.</span></span> <span data-ttu-id="142c4-126">Samuti saate määrata kontomaski, et piirata dimensiooniväärtuste puhul sisestatava teabe hulka ja tüüpi.</span><span class="sxs-lookup"><span data-stu-id="142c4-126">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span> <span data-ttu-id="142c4-127">Saate sisestada märke, mis jäävad samaks igale dimensiooniväärtusele, näiteks tähti või sidekriipsu (-).</span><span class="sxs-lookup"><span data-stu-id="142c4-127">You can enter characters that remain the same for each dimension value, such as letters or a hyphen (-).</span></span> <span data-ttu-id="142c4-128">Saate sisestada ka trelle (\#) ning ja-märke (&) kohatäidetena tähtede ja numbrite jaoks, mis muutuvad iga kord, kui luuakse dimensiooniväärtus.</span><span class="sxs-lookup"><span data-stu-id="142c4-128">You can also enter number signs (\#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="142c4-129">Kasutage numbrimärki (\#) kohatäitena numbrile ning ja-märki (&) kohatäitena tähele.</span><span class="sxs-lookup"><span data-stu-id="142c4-129">Use a number sign (\#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span> <span data-ttu-id="142c4-130">Vormingumaski väli on saadaval ainult siis, kui valite väljal **Kasuta välja väärtusi** suvandi **&lt; Kohandatud dimensioon &gt;**.</span><span class="sxs-lookup"><span data-stu-id="142c4-130">The field for the format mask is available only when you select **&lt; Custom dimension &gt;** in the **Use values from** field.</span></span>

<span data-ttu-id="142c4-131">**Näide**</span><span class="sxs-lookup"><span data-stu-id="142c4-131">**Example**</span></span>

<span data-ttu-id="142c4-132">Dimensiooniväärtuse piiramiseks tähtede CC ja kolme arvuga saate vormingumaskina sisestada **CC-\#\#\#**.</span><span class="sxs-lookup"><span data-stu-id="142c4-132">To limit the dimension value to the letters "CC" and three numbers, enter **CC-\#\#\#** as the format mask.</span></span>

## <a name="entity-backed-dimensions"></a><span data-ttu-id="142c4-133">Üksuse tagatud dimensioonid</span><span class="sxs-lookup"><span data-stu-id="142c4-133">Entity-backed dimensions</span></span>

<span data-ttu-id="142c4-134">Üksuse tagatud finantsdimensiooni loomiseks valige väljalt **Kasuta väärtusi** allikast süsteemi määratletud üksus, millele finantsdimensioon tugineb.</span><span class="sxs-lookup"><span data-stu-id="142c4-134">To create an entity-backed financial dimension, in the **Use values from** field, select a system-defined entity to base the financial dimension on.</span></span> <span data-ttu-id="142c4-135">Finantsdimensiooni väärtused luuakse siis sellest üksusest.</span><span class="sxs-lookup"><span data-stu-id="142c4-135">Financial dimension values are then created from that entity.</span></span> <span data-ttu-id="142c4-136">Näiteks projektide dimensiooniväärtuste loomiseks valige **Projektid**.</span><span class="sxs-lookup"><span data-stu-id="142c4-136">For example, to create dimension values for projects, select **Projects**.</span></span> <span data-ttu-id="142c4-137">Siis luuakse igale projektinimele dimensiooniväärtus.</span><span class="sxs-lookup"><span data-stu-id="142c4-137">A dimension value is then created for each project name.</span></span> <span data-ttu-id="142c4-138">Lehel **Finantsdimensiooni väärtused** on näha üksuse väärtused.</span><span class="sxs-lookup"><span data-stu-id="142c4-138">The **Financial dimension values** page shows the values for the entity.</span></span> <span data-ttu-id="142c4-139">Kui need väärtused on ettevõttepõhised, kuvatakse lehel ka ettevõte.</span><span class="sxs-lookup"><span data-stu-id="142c4-139">If those values are company-specific, the page also shows the company.</span></span>

## <a name="activating-dimensions"></a><span data-ttu-id="142c4-140">Dimensioonide aktiveerimine</span><span class="sxs-lookup"><span data-stu-id="142c4-140">Activating dimensions</span></span>

<span data-ttu-id="142c4-141">Finantsdimensiooni aktiveerimisel uuendatakse tabelit, nii et see sisaldab finantsdimensiooni nime.</span><span class="sxs-lookup"><span data-stu-id="142c4-141">When you activate a financial dimension, the table is updated so that it includes the name of the financial dimension.</span></span> <span data-ttu-id="142c4-142">Kustutatud dimensioonid eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="142c4-142">Deleted dimensions are removed.</span></span> <span data-ttu-id="142c4-143">Võite sisestada dimensiooniväärtused enne finantsdimensiooni aktiveerimist.</span><span class="sxs-lookup"><span data-stu-id="142c4-143">You can enter dimension values before you activate a financial dimension.</span></span> <span data-ttu-id="142c4-144">Kuid finantsdimensiooni ei saa enne aktiveerimist tarbida.</span><span class="sxs-lookup"><span data-stu-id="142c4-144">However, a financial dimension can't be consumed anywhere until it's activated.</span></span> <span data-ttu-id="142c4-145">Näiteks ei saa te lisada finantsdimensiooni kontostruktuurile, enne kui finantsdimensioon on aktiveeritud.</span><span class="sxs-lookup"><span data-stu-id="142c4-145">For example, you can't add a financial dimension to an account structure until the financial dimension has been activated.</span></span> <span data-ttu-id="142c4-146">Kui klõpsate nuppu **Aktiveeri**, siis uuendatakse kõiki dimensioone ja kuvatakse nende oleku muutused.</span><span class="sxs-lookup"><span data-stu-id="142c4-146">When you click **Activate**, all dimensions are updated and show status changes.</span></span> 

## <a name="translations"></a><span data-ttu-id="142c4-147">Tõlked</span><span class="sxs-lookup"><span data-stu-id="142c4-147">Translations</span></span>

<span data-ttu-id="142c4-148">Lehele **Teksti tõlge** võite sisestada valitud finantsdimensiooni teksti mitmesugustes keeltes.</span><span class="sxs-lookup"><span data-stu-id="142c4-148">On the **Text translation** page, you can enter text for the selected financial dimension in various languages.</span></span> <span data-ttu-id="142c4-149">Lehele **Põhikonto** võite sisestada põhikonto teksti mitmesugustes keeltes.</span><span class="sxs-lookup"><span data-stu-id="142c4-149">On the **Main account translation** page, you can enter text for the main account in various languages.</span></span> 

## <a name="legal-entity-overrides"></a><span data-ttu-id="142c4-150">Juriidilise isiku alistamised</span><span class="sxs-lookup"><span data-stu-id="142c4-150">Legal entity overrides</span></span>

<span data-ttu-id="142c4-151">Kõik dimensioonid ei sobi kõigile juriidilistele isikutele.</span><span class="sxs-lookup"><span data-stu-id="142c4-151">Not all dimensions are valid for all legal entities.</span></span> <span data-ttu-id="142c4-152">Lisaks võivad mõningad dimensioonid olla asjakohased ainult konkreetse perioodi jooksul.</span><span class="sxs-lookup"><span data-stu-id="142c4-152">Additionally, some dimensions might be relevant only for a specific period.</span></span> <span data-ttu-id="142c4-153">Sel juhul saab kasutada jaotist **Juriidilise isiku tühistamised** tuvastamiseks, milliste ettevõtete dimensioon tuleks peatada, kes on omanik ja mis ajaperioodil on dimensioon aktiivne.</span><span class="sxs-lookup"><span data-stu-id="142c4-153">In these cases, you can use the **Legal entity overrides** section to specify the companies that the dimension should be suspended for, the owner, and the period when the dimension is active.</span></span>

## <a name="deleting-financial-dimensions"></a><span data-ttu-id="142c4-154">Finantsdimensioonide kustutamine</span><span class="sxs-lookup"><span data-stu-id="142c4-154">Deleting financial dimensions</span></span>

<span data-ttu-id="142c4-155">Andmete viiteterviklikkuse säilitamiseks saab finantsdimensioone harva kustutada.</span><span class="sxs-lookup"><span data-stu-id="142c4-155">To help maintain referential integrity of the data, financial dimensions can rarely be deleted.</span></span> <span data-ttu-id="142c4-156">Kui püüate finantsdimensiooni kustutada, hinnatakse järgmisi kriteeriume.</span><span class="sxs-lookup"><span data-stu-id="142c4-156">If you try to delete a financial dimension, the following criteria are evaluated:</span></span>

- <span data-ttu-id="142c4-157">Kas finantsdimensiooni on mõnes sisestatud või sisestamata kandes või mõnes dimensiooniväärtuste kombinatsiooni tüübis kasutatud?</span><span class="sxs-lookup"><span data-stu-id="142c4-157">Has the financial dimension been used on any posted or unposted transactions, or any type of dimension value combination?</span></span>
- <span data-ttu-id="142c4-158">Kas finantsdimensiooni on kasutatud mõnes aktiivses kontostruktuuris, täpsema reegli struktuuris või finantsdimensioonide kogumis?</span><span class="sxs-lookup"><span data-stu-id="142c4-158">Is the financial dimension used in any active account structure, advanced rule structure, or financial dimension set?</span></span>
- <span data-ttu-id="142c4-159">Kas finantsdimensioon kuulub mõnesse finantsdimensiooni integreerimise vaikevormingusse?</span><span class="sxs-lookup"><span data-stu-id="142c4-159">Is the financial dimension part of a default financial dimension integration format?</span></span>
- <span data-ttu-id="142c4-160">Kas finantsdimensioon on seadistatud vaikedimensiooniks?</span><span class="sxs-lookup"><span data-stu-id="142c4-160">Has the financial dimension been set up as a default dimension?</span></span>

<span data-ttu-id="142c4-161">Kui mõni neist kriteeriumidest on täidetud, ei saa finantsdimensiooni kustutada.</span><span class="sxs-lookup"><span data-stu-id="142c4-161">If any of the criteria are met, you can't delete the financial dimension.</span></span>


<span data-ttu-id="142c4-162">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="142c4-162">For more information, see the following topics:</span></span>
- [<span data-ttu-id="142c4-163">Finantsdimensioonide määratlemine</span><span class="sxs-lookup"><span data-stu-id="142c4-163">Define financial dimensions</span></span>](tasks/define-financial-dimensions.md)
- [<span data-ttu-id="142c4-164">Finantsdimensiooni vaikemallide haldamine</span><span class="sxs-lookup"><span data-stu-id="142c4-164">Maintain financial dimension default templates</span></span>](tasks/maintain-financial-dimension-default-templates.md)

