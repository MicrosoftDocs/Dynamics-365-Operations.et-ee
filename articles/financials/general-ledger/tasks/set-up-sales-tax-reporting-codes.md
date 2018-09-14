--- 
title: "Saate häälestada käibemaksuaruandluse koode."
description: "Käibemaksu aruandluskoodid viitavad käibemaksuaruande väljanumbrile."
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 4543cf7eaa0b1ef8e32d3fdafa2c354cd3739256
ms.contentlocale: et-ee
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="c7b21-103">Saate häälestada käibemaksuaruandluse koode.</span><span class="sxs-lookup"><span data-stu-id="c7b21-103">Set up sales tax reporting codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c7b21-104">Käibemaksu aruandluskoodid viitavad käibemaksuaruande väljanumbrile.</span><span class="sxs-lookup"><span data-stu-id="c7b21-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="c7b21-105">Neid kasutatakse riigiomastel aruandepaigutustel ja käibemaksu maksmisel koodi aruande alusel käibemaksusummade printimiseks aruandluskoodi kohta summeeritud tasakaalustusperioodi puhul.</span><span class="sxs-lookup"><span data-stu-id="c7b21-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="c7b21-106">Pärast käibemaksu aruandluskoodide loomist saate neid vaadata koodilehe Käibemaks kiirvahekaartidel Aruande seadistus.</span><span class="sxs-lookup"><span data-stu-id="c7b21-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="c7b21-107">Salvestamisel kasutatakse demoettevõtet DEMF.</span><span class="sxs-lookup"><span data-stu-id="c7b21-107">This recording uses the DEMF demo company.</span></span>



1. <span data-ttu-id="c7b21-108">Avage Maks > Seadistus > Käibemaks > Käibemaksuaruandluse koodid.</span><span class="sxs-lookup"><span data-stu-id="c7b21-108">Go to Tax > Setup > Sales tax > Sales tax reporting codes.</span></span>
2. <span data-ttu-id="c7b21-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="c7b21-109">Click New.</span></span>
3. <span data-ttu-id="c7b21-110">Valige aruande küljendus, kuhu aruandluskood kuulub.</span><span class="sxs-lookup"><span data-stu-id="c7b21-110">Select the report layout that the reporting code belongs to.</span></span>
    * <span data-ttu-id="c7b21-111">Seda kavandit kasutatakse käibemaksukoodi puhul saadaolevate aruandluskoodide filtrimiseks.</span><span class="sxs-lookup"><span data-stu-id="c7b21-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="c7b21-112">Iga käibemaksukood kuulub tasakaalustusperioodi, mis kuulub aruande paigutust kasutavale käibemaksuhaldurile.</span><span class="sxs-lookup"><span data-stu-id="c7b21-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="c7b21-113">Sisestage number, mis viitab käibemaksuaruande väljale.</span><span class="sxs-lookup"><span data-stu-id="c7b21-113">Enter a number that refers to a field on a sales tax report.</span></span>
5. <span data-ttu-id="c7b21-114">Sisestage aruannetel kuvatav kirjeldus väljale Aruande tekst.</span><span class="sxs-lookup"><span data-stu-id="c7b21-114">In the Report text field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="c7b21-115">Sisestage kirjeldus asutusesiseseks kasutamiseks väljale Lühikirjeldus.</span><span class="sxs-lookup"><span data-stu-id="c7b21-115">In the Brief description field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="c7b21-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="c7b21-116">Click Save.</span></span>


