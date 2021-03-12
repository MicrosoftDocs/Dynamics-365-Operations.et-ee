---
title: Saate häälestada käibemaksuaruandluse koode.
description: Käibemaksu aruandluskoodid viitavad käibemaksuaruandel toodud väljanumbrile.
author: twheeloc
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 821d4abcffbca624382aa7709c02b857fcb6e349
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994511"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="d8596-103">Saate häälestada käibemaksuaruandluse koode.</span><span class="sxs-lookup"><span data-stu-id="d8596-103">Set up sales tax reporting codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d8596-104">Käibemaksu aruandluskoodid viitavad käibemaksuaruandel toodud väljanumbrile.</span><span class="sxs-lookup"><span data-stu-id="d8596-104">The Sales tax reporting codes refer to a field number that's listed on a sales tax report.</span></span> <span data-ttu-id="d8596-105">Neid kasutatakse riigipõhistes aruande paigutustes.</span><span class="sxs-lookup"><span data-stu-id="d8596-105">They are used on country-specific report layouts.</span></span> <span data-ttu-id="d8596-106">Neid kasutatakse ka käibemaksu koodide järgi tasumise aruandes.</span><span class="sxs-lookup"><span data-stu-id="d8596-106">They're also used on the Sales tax payment by code report.</span></span> <span data-ttu-id="d8596-107">Selles aruandes kuvatakse iga aruande koodi kohta summeeritud tasakaalustusperioodi käibemaksu summad.</span><span class="sxs-lookup"><span data-stu-id="d8596-107">That report shows sales tax amounts for a settlement period summarized for each reporting code.</span></span> <span data-ttu-id="d8596-108">Pärast käibemaksu aruandluskoodide loomist saate neid koode vaadata lehe **Käibemaksukood** kiirvahekaartidel Aruande seadistus.</span><span class="sxs-lookup"><span data-stu-id="d8596-108">After you create Sales tax reporting codes, you can refer to those codes on the Report setup FastTabs, which you can access from the **Sales tax code** page.</span></span> 

<span data-ttu-id="d8596-109">Salvestamisel kasutatakse demoettevõtet DEMF.</span><span class="sxs-lookup"><span data-stu-id="d8596-109">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="d8596-110">Avage **Navigeerimispaneel**, seejärel **Maks > Seadistus > Käibemaks > Käibemaksu teavituskoodid**.</span><span class="sxs-lookup"><span data-stu-id="d8596-110">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="d8596-111">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d8596-111">Click **New**.</span></span>
3. <span data-ttu-id="d8596-112">Valige aruande küljendus, kuhu aruandluskood kuulub.</span><span class="sxs-lookup"><span data-stu-id="d8596-112">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="d8596-113">Seda kavandit kasutatakse käibemaksukoodi puhul saadaolevate aruandluskoodide filtrimiseks.</span><span class="sxs-lookup"><span data-stu-id="d8596-113">This layout is used to filter the available reporting codes for a sales tax code.</span></span> <span data-ttu-id="d8596-114">Iga käibemaksukood kuulub tasakaalustusperioodi, mis kuulub aruande paigutust kasutavale käibemaksuhaldurile.</span><span class="sxs-lookup"><span data-stu-id="d8596-114">Each sales tax code belongs to a settlement period, which belongs to a Sales tax authority, which uses a report layout.</span></span>  
4. <span data-ttu-id="d8596-115">Sisestage väljale **Teavituskood** number.</span><span class="sxs-lookup"><span data-stu-id="d8596-115">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="d8596-116">Sisestage aruannetel kuvatav kirjeldus väljale **Teavituskood**.</span><span class="sxs-lookup"><span data-stu-id="d8596-116">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="d8596-117">Sisestage kirjeldus asutusesiseseks kasutamiseks väljale **Lühikirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="d8596-117">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="d8596-118">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d8596-118">Click **Save**.</span></span>

