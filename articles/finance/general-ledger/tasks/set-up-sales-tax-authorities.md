---
title: Maksuhaldurite seadistamine
description: Käibemaksuhaldurid on üksused, kellele tuleb kogutud käibemaks esitada ja maksta.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eff67bc32eafea86d0ff582c56059c28706ed2a1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222231"
---
# <a name="set-up-sales-tax-authorities"></a><span data-ttu-id="c92fc-103">Maksuhaldurite seadistamine</span><span class="sxs-lookup"><span data-stu-id="c92fc-103">Set up sales tax authorities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c92fc-104">Käibemaksuhaldurid on üksused, kellele tuleb kogutud käibemaks esitada ja maksta.</span><span class="sxs-lookup"><span data-stu-id="c92fc-104">Sales tax authorities are entities to which collected sales tax needs to be reported and paid.</span></span> <span data-ttu-id="c92fc-105">Saate tasuda käibemaksu otse haldurile või hankija konto kaudu, mille käibemaksuhaldurile loote.</span><span class="sxs-lookup"><span data-stu-id="c92fc-105">You can pay sales taxes to the authority directly or through a vendor account that you create for the sales tax authority.</span></span> <span data-ttu-id="c92fc-106">Kui teete nii, siis saab ettevõte kasutada oma harilikke makseviise käibemaksuametile õigeaegseks tasumiseks.</span><span class="sxs-lookup"><span data-stu-id="c92fc-106">If you do this, the company can use its usual payment routines to pay the sales tax authority on time.</span></span> <span data-ttu-id="c92fc-107">Kui te ei määra käibemaksuametit tarnijaks, siis peab keegi vastaval maksetähtajal makse käsitsi ette valmistama.</span><span class="sxs-lookup"><span data-stu-id="c92fc-107">If you do not set up the tax authority as a vendor, someone must prepare a manual payment to the tax authority on the appropriate due date.</span></span> <span data-ttu-id="c92fc-108">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="c92fc-108">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="c92fc-109">Avage Maks > Kaudsed maksud > Käibemaks > Käibemaksuhaldurid.</span><span class="sxs-lookup"><span data-stu-id="c92fc-109">Go to Tax > Indirect taxes > Sales tax > Sales tax authorities.</span></span>
2. <span data-ttu-id="c92fc-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="c92fc-110">Click New.</span></span>
3. <span data-ttu-id="c92fc-111">Sisestage väärtus väljale Maksuhaldur.</span><span class="sxs-lookup"><span data-stu-id="c92fc-111">In the Authority field, type a value.</span></span>
4. <span data-ttu-id="c92fc-112">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="c92fc-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c92fc-113">Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="c92fc-113">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="c92fc-114">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c92fc-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="c92fc-115">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="c92fc-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="c92fc-116">Valige oma riigi/regiooni jaoks aruande kavand, kui see on saadaval.</span><span class="sxs-lookup"><span data-stu-id="c92fc-116">Select the report layout for your country/region, if one is available.</span></span> <span data-ttu-id="c92fc-117">Kui aruande kavandid ei ole käibemaksuhalduri nõuetega kooskõlas, kasutage vaikimisi kavandit.</span><span class="sxs-lookup"><span data-stu-id="c92fc-117">If the report layouts do not correspond to the requirements of the sales tax authority, use default layout.</span></span>
9. <span data-ttu-id="c92fc-118">Sisestage väärtused vormi Ümardamine ja väljadele Ümardus, määramaks, kuidas makstava käibemaksu kogusummat ümardatakse.</span><span class="sxs-lookup"><span data-stu-id="c92fc-118">Enter values in the Rounding form and the Round-off fields to specify how the tax total amount to be paid should be rounded.</span></span> <span data-ttu-id="c92fc-119">Mis tahes ümarduserinevused sisestatakse pearaamatus loodud automaatsete kannete kontodele.</span><span class="sxs-lookup"><span data-stu-id="c92fc-119">Any rounding differences will be posted to Accounts for automatic transactions set up in General ledger.</span></span>
10. <span data-ttu-id="c92fc-120">Sisestage number väljale Ümardus.</span><span class="sxs-lookup"><span data-stu-id="c92fc-120">In the Round-off field, enter a number.</span></span>
11. <span data-ttu-id="c92fc-121">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="c92fc-121">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]