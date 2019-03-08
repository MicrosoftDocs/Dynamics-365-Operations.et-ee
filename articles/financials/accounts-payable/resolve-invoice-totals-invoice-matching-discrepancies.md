---
title: Lahknevuste lahendamine arve kogusummade võrdlemisel
description: Arve koondsummade vastavusseviimist saab kasutada tagamiseks, et arve koondsummad ei erineks eeldatavatest summadest rohkem kui lubatud hälbe võrra.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67aa0b89eed1f82290659029dfcce92ca3710aea
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "331502"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching"></a><span data-ttu-id="caa88-103">Lahknevuste lahendamine arve kogusummade võrdlemisel</span><span class="sxs-lookup"><span data-stu-id="caa88-103">Resolve discrepancies during invoice totals matching</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="caa88-104">Arvete võrdlemise kinnitamise üks tüüp on arvete kogusummade võrdlemine.</span><span class="sxs-lookup"><span data-stu-id="caa88-104">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="caa88-105">Selleks, et määrata, et süsteem peaks arvete kogusummasid võrdlema, määrake lehe **Ostureskontro parameetrid** vahekaardil **Arve kinnitamine** suvandi **Arvesummade võrdlemine** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="caa88-105">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="caa88-106">Arve koondsummade vastavusseviimist saab kasutada tagamiseks, et arve koondsummad ei erineks eeldatavatest summadest rohkem kui lubatud hälbe võrra.</span><span class="sxs-lookup"><span data-stu-id="caa88-106">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="caa88-107">Lehel **Arve kogusummade vastendamise üksikasjad** võrreldakse kuute kogusummat.</span><span class="sxs-lookup"><span data-stu-id="caa88-107">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="caa88-108">Kui mõni kogusumma erineb oodatud vastavast ostutellimuse kogusummast, märgitakse võrdluslahknevus.</span><span class="sxs-lookup"><span data-stu-id="caa88-108">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="caa88-109">Kogusummade võrdluslahknevusega arve ülevaatamiseks klõpsake tööruumis **Hankija arved** paanil **Ootel arved**.</span><span class="sxs-lookup"><span data-stu-id="caa88-109">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="caa88-110">Seejärel klõpsake toimingupaani vahekaardil **Ülevaade** suvandit **Vastanduvad üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="caa88-110">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="caa88-111">Kui tuvastatakse võrdluslahknevus, ilmuvad arve summa juurde hoistusikoonid.</span><span class="sxs-lookup"><span data-stu-id="caa88-111">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="caa88-112">Saate kogusummade kohta üksikasju vaadata, vaadates arve kogusummade võrdlemise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="caa88-112">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="caa88-113">Pärast lahknevuse tuvastamist peate vajaduse korral võtma ühendust hankijaga, kui arvate, et arvel olev teave pole täpne.</span><span class="sxs-lookup"><span data-stu-id="caa88-113">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="caa88-114">Olenevalt tulemuseks olevast kokkuleppest hankijaga saate teha ühe järgnevatest toimingutest.</span><span class="sxs-lookup"><span data-stu-id="caa88-114">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="caa88-115">Aktsepteerima hinnaerinevust ja sisestama arve, millel on vastenduste lahknevus.</span><span class="sxs-lookup"><span data-stu-id="caa88-115">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="caa88-116">Süsteem võib olla seadistatud teilt kinnitust küsima, enne kui saab sisestada, kas võrdluslahknevusi on.</span><span class="sxs-lookup"><span data-stu-id="caa88-116">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="caa88-117">Sel juhul peate kinnitama võrdluslahknevuse ja saate valikuliselt sisestada kinnituse kommentaari.</span><span class="sxs-lookup"><span data-stu-id="caa88-117">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="caa88-118">Seejärel saate valida, kas soovite arve sisestada.</span><span class="sxs-lookup"><span data-stu-id="caa88-118">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="caa88-119">Tegema arve summa ümber eeldatavale summale ja sisestama arve.</span><span class="sxs-lookup"><span data-stu-id="caa88-119">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="caa88-120">Taotlema hankijalt täiskrediiti ja uut parandatud arvet.</span><span class="sxs-lookup"><span data-stu-id="caa88-120">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="caa88-121">Lisateabe saamiseks vt [Erandite uurimine või lahendamine](tasks/research-resolve-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="caa88-121">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>


