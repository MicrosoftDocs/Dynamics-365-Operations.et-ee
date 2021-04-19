---
title: Koorma koostamise ja saadetiste tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada koorma koostamise ja saadetistega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e9964376a794661058da78152879d2142dd7ec51
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828198"
---
# <a name="troubleshoot-load-building-and-shipments"></a><span data-ttu-id="ad147-103">Koorma koostamise ja saadetiste tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="ad147-103">Troubleshoot load building and shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad147-104">Selles teemas kirjeldatakse, kuidas lahendada koorma koostamise ja saadetistega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.</span><span class="sxs-lookup"><span data-stu-id="ad147-104">This topic describes how to fix common issues that you might encounter while you work with load building and shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a><span data-ttu-id="ad147-105">Kuvatakse järgmine tõrketeade: "Te ei saa selle tellimuserea jaoks koorma rida luua, kuna see sisaldab varude dimensioone, mis on kehtetud..."</span><span class="sxs-lookup"><span data-stu-id="ad147-105">I receive the following error message: "You can't create a load line for this order line because it contains inventory dimensions that are invalid..."</span></span>

### <a name="issue-description"></a><span data-ttu-id="ad147-106">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ad147-106">Issue description</span></span>

<span data-ttu-id="ad147-107">Kui proovite tagastada müügitellimust lattu, kuvatakse järgmine tõrketeade:</span><span class="sxs-lookup"><span data-stu-id="ad147-107">You receive the following error message when you try to release a return sales order to the warehouse:</span></span>

> <span data-ttu-id="ad147-108">Te ei saa selle tellimuserea jaoks koorma rida luua, kuna see sisaldab varude dimensioone, mis on kehtetud.</span><span class="sxs-lookup"><span data-stu-id="ad147-108">You can't create a load line for this order line because it contains inventory dimensions that are invalid.</span></span> <span data-ttu-id="ad147-109">Te ei saa viidata varude dimensioonidele, mis asuvad reserveerimise hierarhias asukoha dimensiooni all.</span><span class="sxs-lookup"><span data-stu-id="ad147-109">You can't reference inventory dimensions that are located below the location dimension in the reservation hierarchy.</span></span> <span data-ttu-id="ad147-110">Eemaldage tellimuse realt kehtetud dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="ad147-110">Remove the invalid dimensions from the order line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ad147-111">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="ad147-111">Issue resolution</span></span>

<span data-ttu-id="ad147-112">Kahjuks ei toeta toode koorma töötlemist müügiks tagastamise protsessiks.</span><span class="sxs-lookup"><span data-stu-id="ad147-112">Unfortunately, the product doesn't support load processing for a sales return process.</span></span> <span data-ttu-id="ad147-113">Seetõttu ei saa väljastada lattu tagastamise müügitellimust.</span><span class="sxs-lookup"><span data-stu-id="ad147-113">Therefore, you can't release the return sales order to the warehouse.</span></span>

<span data-ttu-id="ad147-114">Müügitellimuste tehingutes ei saa viidata varude dimensioonidele, mis asuvad reserveerimise hierarhias **Location** dimensiooni all.</span><span class="sxs-lookup"><span data-stu-id="ad147-114">On sales order transactions, you can't reference inventory dimensions that are located below the **Location** dimension in the reservation hierarchy.</span></span> <span data-ttu-id="ad147-115">Lahenduseks on eemaldada tellimuse realt kehtetud dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="ad147-115">The resolution is to remove the invalid dimensions from the order line.</span></span>

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a><span data-ttu-id="ad147-116">Kuvatakse järgmine tõrketeade: "Üks rida on juba koormal.</span><span class="sxs-lookup"><span data-stu-id="ad147-116">I receive the following error message: "One of the lines is already on a load.</span></span> <span data-ttu-id="ad147-117">Ei ole võimalik lattu väljastada."</span><span class="sxs-lookup"><span data-stu-id="ad147-117">Unable to release to warehouse."</span></span>

### <a name="issue-description"></a><span data-ttu-id="ad147-118">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ad147-118">Issue description</span></span>

<span data-ttu-id="ad147-119">Kui loote käsitsi koormaid või kui seadistate protsessi nii, et koormad on juba enne müügitellimuse rea sisestamist loodud, on eelduseks, et järgnev väljastus tehakse käsitsi ning kasutatakse koorma protsessi ja hinnangut.</span><span class="sxs-lookup"><span data-stu-id="ad147-119">If you manually create loads, or if you set up the process so that loads are already created before sales order line entry occurs, the assumption is that the subsequent release will be done manually, and that the route and rating from the load will be used.</span></span>

<span data-ttu-id="ad147-120">Teises võimalikus stsenaariumis proovite teha automaatset väljastamist lattu, kuid voo protsessil ei õnnestunud tööd luua.</span><span class="sxs-lookup"><span data-stu-id="ad147-120">In another possible scenario, you're trying to do an automatic release to the warehouse, but the wave process failed to create work.</span></span> <span data-ttu-id="ad147-121">Seetõttu luuakse avatud saadetis või koorem.</span><span class="sxs-lookup"><span data-stu-id="ad147-121">Therefore, an open shipment or load is still created.</span></span> <span data-ttu-id="ad147-122">See avatud saadetis või koorem blokeerib seejärel järgmised katsed tellimuse automaatselt väljastamiseks, kuni te kas kustutate avatud saadetise või koorma või töötlete uue voo käsitsi uuesti.</span><span class="sxs-lookup"><span data-stu-id="ad147-122">This open shipment or load then blocks subsequent attempts to automatically release the order until you either delete the open shipment or load, or manually reprocess the wave.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ad147-123">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="ad147-123">Issue resolution</span></span>

<span data-ttu-id="ad147-124">Saate väljastada müügitellimuse lehelt või teha automaatse väljastamise müügitellimuse lehelt ainult juhul, kui koormat pole enne lattu väljastamist olemas.</span><span class="sxs-lookup"><span data-stu-id="ad147-124">You can release from the sales order page, or automatic release can be done from the release sales order page, only if no load exists before the release to the warehouse.</span></span> <span data-ttu-id="ad147-125">Koorem luuakse automaatselt pärast voo töötlemist.</span><span class="sxs-lookup"><span data-stu-id="ad147-125">The load will automatically be created after the wave is processed.</span></span>

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a><span data-ttu-id="ad147-126">Kuvatakse järgmine tõrketeade: "Saatelehe parandust ei saa töödelda.</span><span class="sxs-lookup"><span data-stu-id="ad147-126">I receive the following error message: "The delivery note correction can't be processed.</span></span> <span data-ttu-id="ad147-127">Saateleht sisaldab ainult kaupu, mille kohta kehtivad laohalduse protsessid, kuna need ei toeta saatelehe parandust."</span><span class="sxs-lookup"><span data-stu-id="ad147-127">The delivery note only contains items that are subject to warehouse management processes, as these are not supported by Delivery Note correction."</span></span>

### <a name="issue-description"></a><span data-ttu-id="ad147-128">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ad147-128">Issue description</span></span>

<span data-ttu-id="ad147-129">Pärast saatelehe sisestamist ei saa seda tühistada, kuna **Tühista** nupp ei ole saadaval.</span><span class="sxs-lookup"><span data-stu-id="ad147-129">After you post a delivery note, you can't cancel it, because the **Cancel** button is unavailable.</span></span> <span data-ttu-id="ad147-130">Samuti ei saa saatelehte parandada.</span><span class="sxs-lookup"><span data-stu-id="ad147-130">You also can't correct the delivery note.</span></span> <span data-ttu-id="ad147-131">Kui proovite, kuvatakse see tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="ad147-131">If you try, you receive this error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ad147-132">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="ad147-132">Issue resolution</span></span>

<span data-ttu-id="ad147-133">Täpsema laohalduse (WMS) jaoks lubatud kaupade sisestatud saatelehtede korrigeerimiseks peate tegema sisestuse koormast, mitte otse tellimusest.</span><span class="sxs-lookup"><span data-stu-id="ad147-133">To correct posted packing slips for items that are enabled for advanced warehouse management (WMS), you must do the posting from the load, not directly from the order.</span></span>

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a><span data-ttu-id="ad147-134">Kuidas ma saan luua tööd voo asemel väljaminevatest koormatest?</span><span class="sxs-lookup"><span data-stu-id="ad147-134">How can I create work from outbound loads instead of waves?</span></span>

### <a name="issue-description"></a><span data-ttu-id="ad147-135">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ad147-135">Issue description</span></span>

<span data-ttu-id="ad147-136">Siin on üks viis selle probleemi taasesitamiseks.</span><span class="sxs-lookup"><span data-stu-id="ad147-136">Here is one way to reproduce this issue.</span></span>

1. <span data-ttu-id="ad147-137">Looge väljaminev koorem müügitellimust või üleviimistellimust kasutades.</span><span class="sxs-lookup"><span data-stu-id="ad147-137">Create an outbound load by using a sales order or transfer order.</span></span>
2. <span data-ttu-id="ad147-138">Väljasta koormus lattu.</span><span class="sxs-lookup"><span data-stu-id="ad147-138">Release the load to the warehouse.</span></span>
3. <span data-ttu-id="ad147-139">Pange tähele, et komplekteerimise tööd pole veel loodud.</span><span class="sxs-lookup"><span data-stu-id="ad147-139">Notice that no picking work has yet been generated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ad147-140">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="ad147-140">Issue resolution</span></span>

<span data-ttu-id="ad147-141">Kui töö tuleb luua kohe, kui koorem on väljastatud, tuleb teil voo mall vastavalt konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="ad147-141">If work must be generated immediately when the load is released, you must configure the wave template accordingly.</span></span> <span data-ttu-id="ad147-142">Voo mallis seadke järgmised valikud väärtusele *Jah*:</span><span class="sxs-lookup"><span data-stu-id="ad147-142">On the wave template, set the following options to *Yes*:</span></span>

- <span data-ttu-id="ad147-143">Automatiseeri voo loomine</span><span class="sxs-lookup"><span data-stu-id="ad147-143">Automate wave creation</span></span>
- <span data-ttu-id="ad147-144">Töötle voogu lattu vabastamisel</span><span class="sxs-lookup"><span data-stu-id="ad147-144">Process wave at release to warehouse</span></span>
- <span data-ttu-id="ad147-145">Automatiseeri voog vabastamine</span><span class="sxs-lookup"><span data-stu-id="ad147-145">Automate wave release</span></span>

## <a name="i-cant-re-release-a-partially-shipped-load"></a><span data-ttu-id="ad147-146">Osaliselt saadetud koormat ei saa uuesti väljastada.</span><span class="sxs-lookup"><span data-stu-id="ad147-146">I can't re-release a partially shipped load.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ad147-147">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ad147-147">Issue description</span></span>

<span data-ttu-id="ad147-148">Te ei saa osaliselt lähetatud koormat lattu väljastada.</span><span class="sxs-lookup"><span data-stu-id="ad147-148">You can't release a partially shipped load to the warehouse.</span></span> <span data-ttu-id="ad147-149">Kui teete lattu väljastamise, kuvatakse teade "Toiming lõpetatud", kuid midagi ei juhtu ja ülejäänud koguse jaoks tööd ei looda.</span><span class="sxs-lookup"><span data-stu-id="ad147-149">When you do the release to the warehouse, an "Operation complete" message appears, but nothing happens, and no work is created for the remaining quantity.</span></span> <span data-ttu-id="ad147-150">See probleem ilmneb, kui kasutate transpordi koorma funktsiooni ja esineb puudulik reserveerimine.</span><span class="sxs-lookup"><span data-stu-id="ad147-150">This issue occurs when you use transport load functionality and there is an incomplete reservation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ad147-151">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="ad147-151">Issue resolution</span></span>

<span data-ttu-id="ad147-152">[KB Issue 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Osaliselt saadetud koormaid saab uuesti levitada ja uuesti töödelda") on fikseeritud [versioonis 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span><span class="sxs-lookup"><span data-stu-id="ad147-152">[KB issue 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Partially shipped loads can be re-waved and re-processed") is fixed in [release 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]