---
title: Teksti kärpimise vältimine positsioonihierarhias ja eksportimine Visiosse
description: Selles artiklis selgitatakse, kuidas lahendada probleemi, mille korral üksikisikute ja ametikohtade nimesid kärbitakse, kui klient vaatab ametikoha hierarhiat rakenduses Microsoft Dynamics 365 Human Resources. Teksti kärpimine võib raskendada kuvatõmmise tegemist või hierarhia printimist.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a745543f4d2a2e2a94a820f4ff5f35f8067a83d7
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466372"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a><span data-ttu-id="1f6bb-104">Teksti kärpimise vältimine ametikoha hierarhias ja Visiosse eksportimisel</span><span class="sxs-lookup"><span data-stu-id="1f6bb-104">Avoid text truncation on the position hierarchy and export to Visio</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1f6bb-105">**Väljastamine**</span><span class="sxs-lookup"><span data-stu-id="1f6bb-105">**Issue**</span></span>

<span data-ttu-id="1f6bb-106">Kui klient vaatab ametikoha hierarhiat rakenduses Microsoft Dynamics 365 Human Resources, siis üksikisikute ja ametikohtade nimesid kärbitakse.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-106">When a customer views the position hierarchy in Microsoft Dynamics 365 Human Resources, the names of individuals and positions are truncated.</span></span> <span data-ttu-id="1f6bb-107">Seetõttu võib kuvatõmmise tegemine või hierarhia printimine ja jaotamine olla keeruline.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-107">Therefore, it can be difficult to take a screenshot, or to print and distribute the hierarchy.</span></span>

![Ametikoha hierarhia](media/position-h.png)

<span data-ttu-id="1f6bb-109">**Põhjus**</span><span class="sxs-lookup"><span data-stu-id="1f6bb-109">**Cause**</span></span>

<span data-ttu-id="1f6bb-110">Selline käitumine on nii kavandatud.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-110">This behavior is by design.</span></span>

<span data-ttu-id="1f6bb-111">**Eraldusvõime**</span><span class="sxs-lookup"><span data-stu-id="1f6bb-111">**Resolution**</span></span>

<span data-ttu-id="1f6bb-112">Kahjuks ei saa kasutajad hõlpsalt teksti suurust muuta.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-112">Unfortunately, users can't easily change the size of the text.</span></span> <span data-ttu-id="1f6bb-113">Samas saate ametikoha hierarhia rakendusest Human Resources välja eksportida ja seejärel selle Microsoft Visiosse importida.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-113">However, you can export the position hierarchy out of Human Resources and then import it into Microsoft Visio.</span></span> <span data-ttu-id="1f6bb-114">Kuigi järgmine artikkel kirjutati Microsoft Dynamics AX 2012 jaoks, kehtib see ka rakenduse Human Resources puhul: [Ametikoha hierarhia eksportimine Microsoft Visiosse](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span><span class="sxs-lookup"><span data-stu-id="1f6bb-114">Although the following article was written for Microsoft Dynamics AX 2012, the process still applies to Human Resources: [Export a position hierarchy to Microsoft Visio](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span></span>

<span data-ttu-id="1f6bb-115">Järgige neid samme, et eksportida Visiosse.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-115">Follow these steps to export to Visio.</span></span>

1. <span data-ttu-id="1f6bb-116">Avage rakenduses Human Resources loendi **Ametikohad** leht.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-116">In Human Resources, open the **Positions** list page.</span></span>

    <span data-ttu-id="1f6bb-117">Organisatsiooni struktuuri diagrammi lisateabe lisamiseks lisage loendisse **Ametikohad** välju, et need oleksid saadaval, kui kasutate viisardit hiljem selles protseduuris.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-117">To include more information in the organization structure diagram, add fields to the **Positions** list, so that they are available when you use the wizard later in this procedure.</span></span>

2. <span data-ttu-id="1f6bb-118">Valige toimingupaanil nupp **Ava Microsoft Office’is** ja seejärel valige jaotises **Ekspordi Excelisse** suvand **Ametikohad**.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-118">On the Action Pane, select the **Open in Microsoft Office** button, and then, under **Export to Excel**, select **Positions**.</span></span> <span data-ttu-id="1f6bb-119">Või vajutage klahvikombinatsiooni Ctrl+T.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-119">Alternatively, press Ctrl+T.</span></span>

    ![Ametikohtade loendilehe eksportimine Excelisse](media/org-admin.png)

3. <span data-ttu-id="1f6bb-121">Salvestage eksporditud Exceli fail.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-121">Save the Excel file that is exported.</span></span>

    ![Dialoogiboks Ekspordi Excelisse](media/export-excel.png)

4. <span data-ttu-id="1f6bb-123">Visios valige **Visio – loo uus** ja valige mallikategooria **Ettevõte**.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-123">In Visio, select **Visio - Create New**, and select the **Business** template category.</span></span>

    ![Uus diagramm](media/new.png)

5. <span data-ttu-id="1f6bb-125">Valige **Organisatsiooni skeemi viisard** ja seejärel valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-125">Select **Organization Chart Wizard**, and then select **Create**.</span></span>

    ![Dialoogiboks Organisatsiooni skeemi viisard](media/orgchart-wizard.png)

6. <span data-ttu-id="1f6bb-127">Valige **Teave, mis on juba faili või andmebaasi talletatud** ja seejärel valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-127">Select **Information that's already stored in a file or database**, and then select **Next**.</span></span>

    ![Organisatsiooni skeemi viisard 1](media/orgchart-wizard7.png)

7. <span data-ttu-id="1f6bb-129">Valige **Tekst, Org Plus (\*.txt), või Exceli fail** ja seejärel valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-129">Choose **A text, Org Plus (\*.txt), or Excel file**, and then select **Next**.</span></span>

    ![Organisatsiooni skeemi viisard 2](media/orgchart-wizard3.png)

8. <span data-ttu-id="1f6bb-131">Sirvige, et valida eksporditud Exceli fail, mis sisaldab ametikoha hierarhiat ja seejärel valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-131">Browse to select the exported Excel file that contains the position hierarchy, and then select **Next**.</span></span>

    ![Organisatsiooni skeemi viisard 3](media/orgchart-wizard2.png)

9. <span data-ttu-id="1f6bb-133">Määrake välja **Nimi** väärtuseks **Ametikoht**, määrake välja **Aruannete sihtkoht** väärtuseks **Aruanded ametikohale** ja seejärel valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-133">Set the **Name** field to **Position**, set the **Reports to** field to **Reports to position**, and then select **Next**.</span></span>

    ![Organisatsiooni skeemi viisard 4](media/orgchart-wizard1.png)

10. <span data-ttu-id="1f6bb-135">Valige väljad, mida tuleks igas sõlmes kuvada ja seejärel valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-135">Select the fields that should be shown on each node, and then select **Next**.</span></span>

    ![Organisatsiooni skeemi viisard 5](media/orgchart-wizard5.png)

11. <span data-ttu-id="1f6bb-137">Lisage veerg **Ametikoht** loendisse **Kujundi andmeväljad** ja seejärel valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-137">Add the **Position** column to the **Shape Data fields** list, and then select **Next**.</span></span>

    ![Organisatsiooni skeemi viisard 6](media/orgchart-wizard6.png)

12. <span data-ttu-id="1f6bb-139">Pildid ei ole praegu saadaval.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-139">Pictures aren't currently available.</span></span> <span data-ttu-id="1f6bb-140">Seetõttu valige järgmisel lehel **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-140">Therefore, on the next page, select **Next**.</span></span>
13. <span data-ttu-id="1f6bb-141">Valige **Soovin, et viisard jaotaks mu organisatsiooniskeemi erinevate lehtede vahel**.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-141">Select **I want the wizard to automatically break my organization chart across pages**.</span></span>

    ![Organisatsiooni skeemi viisard 7](media/orgchart-wizard4.png)

14. <span data-ttu-id="1f6bb-143">Valige **Lõpeta**.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-143">Select **Finish**.</span></span>

    <span data-ttu-id="1f6bb-144">Kui on ametikohti, mis pole struktuuris, palutakse teil need diagrammi lisada.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-144">If there are any positions that aren't in the structure, you're asked to include them in the diagram.</span></span>

<span data-ttu-id="1f6bb-145">Visios loodud diagramm kuvab iga halduri eraldi töölehel.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-145">The diagram that is generated in Visio shows each manager on a separate worksheet.</span></span>

<span data-ttu-id="1f6bb-146">Väljade põhjal, mille valisite, et soovite diagrammi lisada, kuvab iga sõlm Visio faili loomisel vastava teabe.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-146">Based on the fields that you selected to include in the diagram, each node shows the appropriate information when the Visio file is generated.</span></span>

![Hierarhiaskeem](media/hierarchy.png)

<span data-ttu-id="1f6bb-148">**Lisasuvand**</span><span class="sxs-lookup"><span data-stu-id="1f6bb-148">**Additional option**</span></span>

<span data-ttu-id="1f6bb-149">Rakenduses Human Resources saate võib-olla kasutada ka tööruumi **Inimesed**, et vaadata hierarhiaga seotud teavet.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-149">In Human Resources, you might also be able to use the **People** workspace to view some hierarchy-related information.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]