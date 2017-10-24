---
title: "Lahknevuste lahendamine arve kogusummade võrdlemisel"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3f7e1261838866688c97529b0edfa1354034247b
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a><span data-ttu-id="a49ab-102">Lahknevuste lahendamine arve kogusummade võrdlemisel</span><span class="sxs-lookup"><span data-stu-id="a49ab-102">Resolve discrepancies during invoice totals matching</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="a49ab-103">Arvete võrdlemise kinnitamise üks tüüp on arvete kogusummade võrdlemine.</span><span class="sxs-lookup"><span data-stu-id="a49ab-103">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="a49ab-104">Selleks, et määrata, et süsteem peaks arvete kogusummasid võrdlema, määrake lehe **Ostureskontro parameetrid** vahekaardil **Arve kinnitamine** suvandi **Arvesummade võrdlemine** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="a49ab-104">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="a49ab-105">Arve koondsummade vastavusseviimist saab kasutada tagamiseks, et arve koondsummad ei erineks eeldatavatest summadest rohkem kui lubatud hälbe võrra.</span><span class="sxs-lookup"><span data-stu-id="a49ab-105">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="a49ab-106">Lehel **Arve kogusummade vastendamise üksikasjad** võrreldakse kuute kogusummat.</span><span class="sxs-lookup"><span data-stu-id="a49ab-106">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="a49ab-107">Kui mõni kogusumma erineb oodatud vastavast ostutellimuse kogusummast, märgitakse võrdluslahknevus.</span><span class="sxs-lookup"><span data-stu-id="a49ab-107">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="a49ab-108">Kogusummade võrdluslahknevusega arve ülevaatamiseks klõpsake tööruumis **Hankija arved** paanil **Ootel arved**.</span><span class="sxs-lookup"><span data-stu-id="a49ab-108">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="a49ab-109">Seejärel klõpsake toimingupaani vahekaardil **Ülevaade** suvandit **Vastanduvad üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="a49ab-109">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="a49ab-110">Kui tuvastatakse võrdluslahknevus, ilmuvad arve summa juurde hoistusikoonid.</span><span class="sxs-lookup"><span data-stu-id="a49ab-110">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="a49ab-111">Saate kogusummade kohta üksikasju vaadata, vaadates arve kogusummade võrdlemise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="a49ab-111">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="a49ab-112">Pärast lahknevuse tuvastamist peate vajaduse korral võtma ühendust hankijaga, kui arvate, et arvel olev teave pole täpne.</span><span class="sxs-lookup"><span data-stu-id="a49ab-112">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="a49ab-113">Olenevalt tulemuseks olevast kokkuleppest hankijaga saate teha ühe järgnevatest toimingutest.</span><span class="sxs-lookup"><span data-stu-id="a49ab-113">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="a49ab-114">Aktsepteerima hinnaerinevust ja sisestama arve, millel on vastenduste lahknevus.</span><span class="sxs-lookup"><span data-stu-id="a49ab-114">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="a49ab-115">Süsteem võib olla seadistatud teilt kinnitust küsima, enne kui saab sisestada, kas võrdluslahknevusi on.</span><span class="sxs-lookup"><span data-stu-id="a49ab-115">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="a49ab-116">Sel juhul peate kinnitama võrdluslahknevuse ja saate valikuliselt sisestada kinnituse kommentaari.</span><span class="sxs-lookup"><span data-stu-id="a49ab-116">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="a49ab-117">Seejärel saate valida, kas soovite arve sisestada.</span><span class="sxs-lookup"><span data-stu-id="a49ab-117">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="a49ab-118">Tegema arve summa ümber eeldatavale summale ja sisestama arve.</span><span class="sxs-lookup"><span data-stu-id="a49ab-118">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="a49ab-119">Taotlema hankijalt täiskrediiti ja uut parandatud arvet.</span><span class="sxs-lookup"><span data-stu-id="a49ab-119">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="a49ab-120">Lisateabe saamiseks vt [Erandite uurimine või lahendamine](tasks/research-resolve-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="a49ab-120">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>



