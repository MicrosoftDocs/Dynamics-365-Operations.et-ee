---
title: Ülevaade lahknevuste lahendamisest arvete koondsummade võrdlemise ajal
description: Arve koondsummade võrdlemist saab kasutada tagamiseks, et arve koondsummad ei erineks eeldatavatest summadest rohkem kui lubatud hälbe võrra.
author: abruer
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d4a20368385ec43547ee3d29770bd83cdec47e4a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189495"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching-overview"></a><span data-ttu-id="524b2-103">Ülevaade lahknevuste lahendamisest arvete koondsummade võrdlemise ajal</span><span class="sxs-lookup"><span data-stu-id="524b2-103">Resolve discrepancies during invoice totals matching overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="524b2-104">Arvete võrdlemise kinnitamise üks tüüp on arvete kogusummade võrdlemine.</span><span class="sxs-lookup"><span data-stu-id="524b2-104">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="524b2-105">Selleks, et määrata, et süsteem peaks arvete kogusummasid võrdlema, määrake lehe **Ostureskontro parameetrid** vahekaardil **Arve kinnitamine** suvandi **Arvesummade võrdlemine** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="524b2-105">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="524b2-106">Arve koondsummade vastavusseviimist saab kasutada tagamiseks, et arve koondsummad ei erineks eeldatavatest summadest rohkem kui lubatud hälbe võrra.</span><span class="sxs-lookup"><span data-stu-id="524b2-106">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="524b2-107">Lehel **Arve kogusummade vastendamise üksikasjad** võrreldakse kuute kogusummat.</span><span class="sxs-lookup"><span data-stu-id="524b2-107">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="524b2-108">Kui mõni kogusumma erineb oodatud vastavast ostutellimuse kogusummast, märgitakse võrdluslahknevus.</span><span class="sxs-lookup"><span data-stu-id="524b2-108">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="524b2-109">Kogusummade võrdluslahknevusega arve ülevaatamiseks klõpsake tööruumis **Hankija arved** paanil **Ootel arved**.</span><span class="sxs-lookup"><span data-stu-id="524b2-109">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="524b2-110">Seejärel klõpsake toimingupaani vahekaardil **Ülevaade** suvandit **Vastanduvad üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="524b2-110">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="524b2-111">Kui tuvastatakse võrdluslahknevus, ilmuvad arve summa juurde hoistusikoonid.</span><span class="sxs-lookup"><span data-stu-id="524b2-111">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="524b2-112">Saate kogusummade kohta üksikasju vaadata, vaadates arve kogusummade võrdlemise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="524b2-112">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="524b2-113">Pärast lahknevuse tuvastamist peate vajaduse korral võtma ühendust hankijaga, kui arvate, et arvel olev teave pole täpne.</span><span class="sxs-lookup"><span data-stu-id="524b2-113">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="524b2-114">Olenevalt tulemuseks olevast kokkuleppest hankijaga saate teha ühe järgnevatest toimingutest.</span><span class="sxs-lookup"><span data-stu-id="524b2-114">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="524b2-115">Aktsepteerima hinnaerinevust ja sisestama arve, millel on vastenduste lahknevus.</span><span class="sxs-lookup"><span data-stu-id="524b2-115">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="524b2-116">Süsteem võib olla seadistatud teilt kinnitust küsima, enne kui saab sisestada, kas võrdluslahknevusi on.</span><span class="sxs-lookup"><span data-stu-id="524b2-116">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="524b2-117">Sel juhul peate kinnitama võrdluslahknevuse ja saate valikuliselt sisestada kinnituse kommentaari.</span><span class="sxs-lookup"><span data-stu-id="524b2-117">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="524b2-118">Seejärel saate valida, kas soovite arve sisestada.</span><span class="sxs-lookup"><span data-stu-id="524b2-118">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="524b2-119">Tegema arve summa ümber eeldatavale summale ja sisestama arve.</span><span class="sxs-lookup"><span data-stu-id="524b2-119">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="524b2-120">Taotlema hankijalt täiskrediiti ja uut parandatud arvet.</span><span class="sxs-lookup"><span data-stu-id="524b2-120">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="524b2-121">Lisateabe saamiseks vt [Erandite uurimine või lahendamine](tasks/research-resolve-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="524b2-121">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>


