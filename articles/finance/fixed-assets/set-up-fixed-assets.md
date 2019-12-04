---
title: Põhivarade seadistamine
description: Selles teemas antakse ülevaade põhivarade mooduli seadistamisest.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8196ddc879df1f398aabef0c1c4064bf0d4fff2c
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771915"
---
# <a name="set-up-fixed-assets"></a><span data-ttu-id="7d0aa-103">Põhivarade seadistamine</span><span class="sxs-lookup"><span data-stu-id="7d0aa-103">Set up fixed assets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d0aa-104">Selles teemas antakse ülevaade mooduli **Põhivarad** seadistamisest.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-104">This topic provides an overview of the setup of the **Fixed assets** module.</span></span>

## <a name="overview"></a><span data-ttu-id="7d0aa-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="7d0aa-105">Overview</span></span>

<span data-ttu-id="7d0aa-106">Parameetrid juhivad põhivarade mooduli üldist käitumist.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-106">Parameters control the general behavior in Fixed assets.</span></span>

<span data-ttu-id="7d0aa-107">Põhivaragrupid võimaldavad teil varasid grupeerida ja määrata igale gruppi määratud varale atribuute.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-107">Fixed asset groups let you group your assets and specify default attributes for every asset that is assigned to a group.</span></span> <span data-ttu-id="7d0aa-108">Raamatud määratakse põhivaragruppidele.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-108">Books are assigned to fixed asset groups.</span></span> <span data-ttu-id="7d0aa-109">Raamatud jälgivad põhivara finantsväärtust aja jooksul, kasutades kulumireeglites määratletud kulumikonfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-109">Books track the financial value of a fixed asset over time by using the depreciation configuration that is defined in the depreciation profile.</span></span>

<span data-ttu-id="7d0aa-110">Põhivarad määratakse loomisel gruppi.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-110">Fixed assets are assigned to a group when they are created.</span></span> <span data-ttu-id="7d0aa-111">Vaikimisi määratakse põhivaragrupile määratud raamatud seejärel põhivarale.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-111">By default, the books that are assigned to the fixed asset group are then assigned to the fixed asset.</span></span> <span data-ttu-id="7d0aa-112">Põhiraamatusse sisestamiseks konfigureeritud raamatud seostatakse sisestusreeglitega.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-112">Books that are configured to post to the general ledger are associated with a posting profile.</span></span> <span data-ttu-id="7d0aa-113">Pearaamatukontod määratletakse sisestusreeglites iga raamatu kohta ja neid kasutatakse põhivarakannete sisestamisel.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-113">Ledger accounts are defined for each book in the posting profile and are used when fixed asset transactions are posted.</span></span>

![Põhivara komponendid](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a><span data-ttu-id="7d0aa-115">Kulumireeglid</span><span class="sxs-lookup"><span data-stu-id="7d0aa-115">Depreciation profiles</span></span>

<span data-ttu-id="7d0aa-116">Esmalt peaksite seadistama kulumireeglid.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-116">You should first set up depreciation profiles.</span></span> <span data-ttu-id="7d0aa-117">Kulumireeglites saate konfigureerida, kuidas vara väärtus aja jooksul amortiseerub.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-117">In the depreciation profile, you configure how the value of an asset is depreciated over time.</span></span> <span data-ttu-id="7d0aa-118">Peate määratlema kulumimeetodi, kulumiaasta (kalendriaasta või rahandusaasta) ja kulumi sageduse.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-118">You must define the method of depreciation, the depreciation year (calendar year or fiscal year), and the frequency of depreciation.</span></span> <span data-ttu-id="7d0aa-119">Lisateavet vt teemast [Kulumireeglite seadistamine ja loomine](tasks/set-up-depreciation-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="7d0aa-119">For more information, see [Set up and create depreciation profiles](tasks/set-up-depreciation-profiles.md).</span></span>

## <a name="books"></a><span data-ttu-id="7d0aa-120">Raamatud</span><span class="sxs-lookup"><span data-stu-id="7d0aa-120">Books</span></span>

<span data-ttu-id="7d0aa-121">Pärast kulumireeglite seadistamist peate looma oma varade jaoks nõutavad raamatud.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-121">After you set up depreciation profiles, you must create the required books for your assets.</span></span> <span data-ttu-id="7d0aa-122">Iga raamat jälgib vara sõltumatut rahalist elutsüklit.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-122">Each book tracks an independent financial lifecycle of an asset.</span></span> <span data-ttu-id="7d0aa-123">Raamatud saab konfigureerida sisestama seostatud kandeid pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-123">Books can be configured to post associated transactions to the general ledger.</span></span> <span data-ttu-id="7d0aa-124">See konfiguratsioon on vaikesäte, kuna seda kasutatakse tavaliselt ettevõtte finantsaruandluses.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-124">This configuration is the default setting, because it's typically used for corporate financial reporting.</span></span> <span data-ttu-id="7d0aa-125">Raamatud, mis pearaamatusse ei sisesta, sisestavad ainult põhivara alammoodulisse ja neid kasutatakse tavalisel maksuaruandluses.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-125">Books that don't post to the general ledger post only to the Fixed asset subledger and are typically used for tax reporting purposes.</span></span>

<span data-ttu-id="7d0aa-126">Igale raamatule määratakse esmane kulumireegel.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-126">A primary depreciation profile is assigned to every book.</span></span> <span data-ttu-id="7d0aa-127">Raamatutel on ka alternatiivsed või ülemineku kulumireeglid, kui seda tüüpi reeglid on kohaldatavad.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-127">Books also have an alternative or switchover depreciation profile, if this type of profile is applicable.</span></span> <span data-ttu-id="7d0aa-128">Põhivara raamatu automaatseks kaasamiseks kulumi käitustesse peate lubama suvandi **Arvuta kulum**.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-128">To automatically include the fixed asset book in depreciation runs, you must enable the **Calculate depreciation** option.</span></span> <span data-ttu-id="7d0aa-129">Kui see suvand pole mõne vara puhul lubatud, jätab kulumisoovitus vara vahele.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-129">If this option isn't enabled for an asset, the depreciation proposal skips the asset.</span></span>

<span data-ttu-id="7d0aa-130">Saate seadistada ka tuletatud raamatuid.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-130">You can also set up derived books.</span></span> <span data-ttu-id="7d0aa-131">Määratud tuletatud kanded sisestatakse tuletatud raamatute suhtes esmase kande täpse koopiana.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-131">The specified derived transactions are posted against the derived books as an exact copy of the primary transaction.</span></span> <span data-ttu-id="7d0aa-132">Seetõttu seadistatakse tuletatud kanded tavaliselt soetuste ja likvideerimiste, mitte kulumikannete jaoks.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-132">Therefore, derived transactions are typically set up for acquisitions and disposals, not for depreciation transactions.</span></span> <span data-ttu-id="7d0aa-133">Lisateavet leiate teemast [Väärtusmudelite seadistamine](tasks/set-up-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="7d0aa-133">For more information, see [Set up value models](tasks/set-up-value-models.md).</span></span>

## <a name="fixed-asset-posting-profiles"></a><span data-ttu-id="7d0aa-134">Põhivarade sisestusreeglid</span><span class="sxs-lookup"><span data-stu-id="7d0aa-134">Fixed asset posting profiles</span></span>

<span data-ttu-id="7d0aa-135">Pärast raamatute seadistamist saate luua sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-135">After you set up books, you can create the posting profile.</span></span> <span data-ttu-id="7d0aa-136">Sisestusreeglid tuleb määratleda raamatu järgi, kuid neid saab määratleda ka üksikasjalikumal tasemel.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-136">The posting profile must be defined by book, but it can also be defined at a more detailed level.</span></span> <span data-ttu-id="7d0aa-137">Näiteks saate määratleda sisestusreeglid raamatu ja põhivaragrupi kombinatsioonile või isegi üksiku põhivara raamatule.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-137">For example, you can define the posting profile for the combination of a book and a fixed asset group, or even for an individual fixed asset book.</span></span> <span data-ttu-id="7d0aa-138">Vaikimisi kasutatakse määratletud pearaamatukontosid teie põhivarakannete jaoks.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-138">By default, the ledger accounts that are defined are used for your fixed asset transactions.</span></span>

<span data-ttu-id="7d0aa-139">Peate määratlema pearaamatukontod, mida kasutatakse likvideerimisprotsessides nii likvideerimismüügi kui ka likvideerimise mahakandmise puhul.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-139">You must define the ledger accounts that are used during the disposal processes, both disposal sales and disposal scraps.</span></span> <span data-ttu-id="7d0aa-140">Likvideerimise ajal tühistatakse varem sisestatud põhivarakanded algsetel kontodel.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-140">At the time of disposal, the fixed asset transactions that were previously posted are reversed out of the original accounts.</span></span> <span data-ttu-id="7d0aa-141">Seejärel teisaldatakse netosummad vara likvideerimiseks sobivale kasumi ja kahjumi kontole.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-141">The net amounts are then moved to the appropriate account for gain and loss for asset disposal.</span></span> <span data-ttu-id="7d0aa-142">Kannete õigeks tühistamiseks peate seadistama kontod iga kandetüübi puhul, mida oma ettevõttes kasutate.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-142">To help guarantee that transactions are correctly reversed, you must set up accounts for each type of transaction that you use in your business.</span></span> <span data-ttu-id="7d0aa-143">Põhikontoks peaks olema algne konto, mille selle kandetüübi puhul sisestusreeglites seadistasite ja vastaskontoks peaks olema likvideerimiskonto puhul teie kasumi ja kahjumi konto.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-143">The main account should be the original account that you set on the posting profile for the transaction type, and the offset account should be your gain and loss for disposal account.</span></span> <span data-ttu-id="7d0aa-144">Erandiks on raamatupidamislik jääkväärtus.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-144">The exception is the net book value.</span></span> <span data-ttu-id="7d0aa-145">Sellisel juhul peaks nii põhi- kui ka vastaskonto olema seadistatud likvideerimiskonto puhul kasumi ja kahjumi kontole.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-145">In this case, both the main account and the offset account should be set to the gain and loss for disposal account.</span></span> <span data-ttu-id="7d0aa-146">Lisateabe saamiseks vt [Põhivara sisestusprofiilide seadistamine](tasks/set-up-fixed-asset-posting-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="7d0aa-146">For more information, see [Set up fixed asset posting profiles](tasks/set-up-fixed-asset-posting-profiles.md).</span></span>

## <a name="fixed-asset-groups"></a><span data-ttu-id="7d0aa-147">Põhivaragruppide tabel</span><span class="sxs-lookup"><span data-stu-id="7d0aa-147">Fixed asset groups</span></span>

<span data-ttu-id="7d0aa-148">**Põhivaragrupp** on põhivara loomisel ainus nõutav väli.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-148">The **Fixed asset group** field is the only required field when you create a fixed asset.</span></span> <span data-ttu-id="7d0aa-149">Selle välja väärtus määratleb vara mitme teabevälja vaikeväärtuse.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-149">The value of this field determines the default value of several informational fields for the asset.</span></span> <span data-ttu-id="7d0aa-150">Raamatud seadistatakse nii, et vaikeraamat on määratud grupi igale varale.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-150">Books are set up so that a default book is assigned to each asset in a group.</span></span> <span data-ttu-id="7d0aa-151">Nii saavad raamatutele määratud atribuudid olla omased põhivaragrupile.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-151">In this way, attributes that you set for the books can be specific to a group of assets.</span></span> <span data-ttu-id="7d0aa-152">Need atribuudid hõlmavad tööiga ning kulumiarvestusreeglit.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-152">These attributes include the service life and the depreciation convention.</span></span>

<span data-ttu-id="7d0aa-153">Saate ka määratleda kulumi erihüvitised või lisakulumi põhivaragrupi ja raamatu kindlale kombinatsioonile.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-153">You can also define special depreciation allowances, or bonus depreciation, for a specific combination of a fixed asset group and a book.</span></span> <span data-ttu-id="7d0aa-154">Peate määrama kulumi erihüvitisele prioriteedi, et määrata hüvitiste arvutamise järjekorra, kui raamatule on määratud mitu hüvitist.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-154">You must assign a priority to the special depreciation allowance to specify the order that allowances are calculated in when multiple allowances are assigned to a book.</span></span> <span data-ttu-id="7d0aa-155">Lisateabe saamiseks vt [Põhivaragruppide seadistamine](tasks/set-up-fixed-asset-groups.md).</span><span class="sxs-lookup"><span data-stu-id="7d0aa-155">For more information, see [Set up fixed asset groups](tasks/set-up-fixed-asset-groups.md).</span></span>

## <a name="journal-names"></a><span data-ttu-id="7d0aa-156">Töölehe nimed</span><span class="sxs-lookup"><span data-stu-id="7d0aa-156">Journal names</span></span>

<span data-ttu-id="7d0aa-157">Lehel **Töölehe nimed** peate looma töölehe nimed, mida tuleb põhivarade töölehega kasutada.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-157">On the **Journal names** page, you must create the journal names that should be used with the Fixed assets journal.</span></span> <span data-ttu-id="7d0aa-158">Välja **Töölehe tüüp** väärtuseks peate valima **Sisesta põhivara**.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-158">You must set the **Journal type** field to **Post fixed assets**.</span></span> <span data-ttu-id="7d0aa-159">Välja **Kandeseeria** peate määrama nii, et põhivara töölehe jaoks kasutatakse töölehe nimesid.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-159">Set the **Voucher series** field so that the journal names are used for the Fixed assets journal.</span></span> <span data-ttu-id="7d0aa-160">Põhivara töölehed ei tohi kasutada sätet **Ainult üks kande number**, sest mitme automaatse protsessi, näiteks ülekannete ja tükeldamiste jaoks on vaja kordumatut kandenumbrit.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-160">Fixed assets journals should not use the **One voucher number only** setting, because a unique voucher number is required for several automated processes, such as transfers and splits.</span></span>

## <a name="fixed-asset-parameters"></a><span data-ttu-id="7d0aa-161">Põhivara parameetrid</span><span class="sxs-lookup"><span data-stu-id="7d0aa-161">Fixed asset parameters</span></span>

<span data-ttu-id="7d0aa-162">Viimane etapp on põhivara parameetrite värskendamine.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-162">The last step is to update the fixed asset parameters.</span></span>

<span data-ttu-id="7d0aa-163">Väli **Kapitaliseerimislävi** määratleb amortiseerunud varad.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-163">The **Capitalization threshold** field determines the assets that are depreciated.</span></span> <span data-ttu-id="7d0aa-164">Kui põhivarana on valitud osturida, kuid see ei vasta määratud kapitaliseerimislävele, siis põhivara küll luuakse või värskendatakse, kuid suvandi **Arvuta kulum** säte on **Ei**.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-164">If a purchase line is selected as a fixed asset, but it doesn't meet the specified capitalization threshold, a fixed asset is still created or updated, but the **Calculate depreciation** option is set to **No**.</span></span> <span data-ttu-id="7d0aa-165">Seetõttu ei amortiseerita vara kulumisoovituste osana automaatselt.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-165">Therefore, the asset won't be automatically depreciated as part of the depreciation proposals.</span></span>

<span data-ttu-id="7d0aa-166">Üks oluline suvand on **Kulumi korrigeerimissummade automaatne loomine likvideerimisel**.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-166">One important option is named **Automatically create depreciation adjustment amounts with disposal**.</span></span> <span data-ttu-id="7d0aa-167">Kui valite selle suvandi sätteks **Jah**, korrigeeritakse vara amortiseerumist automaatselt, võttes aluseks kulumisätted vara likvideerimise ajal.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-167">When you set this option to **Yes**, the asset depreciation is automatically adjusted, based on the depreciation settings at the time of asset disposal.</span></span> <span data-ttu-id="7d0aa-168">Teine valik võimaldab soetussummast maha arvata skontod, kui soetate põhivarasid hankija arvega.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-168">Another option lets you deduct cash discounts from the acquisition amount when you acquire fixed assets by using a vendor invoice.</span></span>

<span data-ttu-id="7d0aa-169">Kiirkaardil **Ostutellimused** saate konfigureerida, kuidas varasid ostuprotsessi osana luuakse.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-169">On the **Purchase orders** FastTab, you can configure how assets are created as part of the purchasing process.</span></span> <span data-ttu-id="7d0aa-170">Esimene valik on **Luba vara soetamine ostmiselt**.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-170">The first option is named **Allow asset acquisition from Purchasing**.</span></span> <span data-ttu-id="7d0aa-171">Kui määrate selle suvandi sätteks **Jah**, toimub vara soetamine arve sisestamisel.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-171">If you set this option to **Yes**, asset acquisition occurs when the invoice is posted.</span></span> <span data-ttu-id="7d0aa-172">Kui määrate selle suvandi sätteks **Ei**, saate põhivara panna ikkagi ostutellimusse ja arvele, kuid soetamist ei sisestata.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-172">If you set this option to **No**, you can still put a fixed asset on a purchase order (PO) and invoice, but the acquisition won't be posted.</span></span> <span data-ttu-id="7d0aa-173">Sisestamine tuleb teha eraldi etapina põhivara töölehelt.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-173">Posting must be done as a separate step, from the Fixed assets journal.</span></span> <span data-ttu-id="7d0aa-174">Suvand **Looge vara toote sissetuleku või arve sisestamise ajal** võimaldab luua uue põhivara käigu pealt sisestamise ajal.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-174">The **Create asset during product receipt or invoice posting** option lets you create a new asset "on the fly" during posting.</span></span> <span data-ttu-id="7d0aa-175">Seetõttu ei pea vara enne kannet põhivarana seadistama.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-175">Therefore, the asset doesn't have to be set up as a fixed asset before the transaction.</span></span> <span data-ttu-id="7d0aa-176">Viimane võimalus **Kontrolli põhivarade loomist rea sisestamisel** rakendub ainult ostutaotlustele.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-176">The last option, **Check for fixed assets creation during line entry**, applies only to purchase requisitions.</span></span>

<span data-ttu-id="7d0aa-177">Saate konfigureerida põhjusekoode nii, et need on põhivara muudatuste või kindlate põhivarakannete puhul nõutavad.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-177">You can configure reason codes so that they are required for changes to a fixed asset or for specific fixed asset transactions.</span></span>

<span data-ttu-id="7d0aa-178">Viimasena saate vahekaardil **Numbriseeriad** määratleda põhivarade numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-178">Finally, on the **Number sequences** tab, you define number sequences for fixed assets.</span></span> <span data-ttu-id="7d0aa-179">**Põhivara** numbriseeria saab tühistada üksuse **Põhivaragrupp** numbriseeriaga, kui see on määratud.</span><span class="sxs-lookup"><span data-stu-id="7d0aa-179">The **Fixed asset** number sequence can be overridden by the **Fixed asset group** number sequence if it has been specified.</span></span>

<span data-ttu-id="7d0aa-180">Lisateavet leiate teemast [Põhivara loomine](tasks/create-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="7d0aa-180">For more information, see [Create a fixed asset](tasks/create-fixed-asset.md).</span></span>