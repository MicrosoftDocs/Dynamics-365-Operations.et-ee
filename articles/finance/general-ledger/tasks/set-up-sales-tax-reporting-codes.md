---
title: Saate häälestada käibemaksuaruandluse koode.
description: Käibemaksu aruandluskoodid viitavad käibemaksuaruande väljanumbrile.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4751256858da417ec9bb1b7d9ccd16fb6bef1cac
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185930"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="0556d-103">Saate häälestada käibemaksuaruandluse koode.</span><span class="sxs-lookup"><span data-stu-id="0556d-103">Set up sales tax reporting codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0556d-104">Käibemaksu aruandluskoodid viitavad käibemaksuaruande väljanumbrile.</span><span class="sxs-lookup"><span data-stu-id="0556d-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="0556d-105">Neid kasutatakse riigiomastel aruandepaigutustel ja käibemaksu maksmisel koodi aruande alusel käibemaksusummade printimiseks aruandluskoodi kohta summeeritud tasakaalustusperioodi puhul.</span><span class="sxs-lookup"><span data-stu-id="0556d-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="0556d-106">Pärast käibemaksu aruandluskoodide loomist saate neid vaadata koodilehe Käibemaks kiirvahekaartidel Aruande seadistus.</span><span class="sxs-lookup"><span data-stu-id="0556d-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="0556d-107">Salvestamisel kasutatakse demoettevõtet DEMF.</span><span class="sxs-lookup"><span data-stu-id="0556d-107">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="0556d-108">Avage **Navigeerimispaneel**, seejärel **Maks > Seadistus > Käibemaks > Käibemaksu teavituskoodid**.</span><span class="sxs-lookup"><span data-stu-id="0556d-108">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="0556d-109">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="0556d-109">Click **New**.</span></span>
3. <span data-ttu-id="0556d-110">Valige aruande küljendus, kuhu aruandluskood kuulub.</span><span class="sxs-lookup"><span data-stu-id="0556d-110">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="0556d-111">Seda kavandit kasutatakse käibemaksukoodi puhul saadaolevate aruandluskoodide filtrimiseks.</span><span class="sxs-lookup"><span data-stu-id="0556d-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="0556d-112">Iga käibemaksukood kuulub tasakaalustusperioodi, mis kuulub aruande paigutust kasutavale käibemaksuhaldurile.</span><span class="sxs-lookup"><span data-stu-id="0556d-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="0556d-113">Sisestage väljale **Teavituskood** number.</span><span class="sxs-lookup"><span data-stu-id="0556d-113">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="0556d-114">Sisestage aruannetel kuvatav kirjeldus väljale **Teavituskood**.</span><span class="sxs-lookup"><span data-stu-id="0556d-114">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="0556d-115">Sisestage kirjeldus asutusesiseseks kasutamiseks väljale **Lühikirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="0556d-115">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="0556d-116">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0556d-116">Click **Save**.</span></span>

