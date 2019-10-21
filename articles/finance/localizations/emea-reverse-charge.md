---
title: Pöördkäibemaks
description: See teema selgitab, kuidas seadistada Euroopa riikide ja Saudi Araabia pöördkäibemaksu (KM).
author: epodkolz
manager: AnnBe
ms.date: 07/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Saudi Arabia, Spain, Sweden, United Kingdom, Singapore
ms.author: epodkolz
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 530ff52abb1dd36c473ae436d61ea925c5696a30
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183605"
---
# <a name="reverse-charge-vat"></a><span data-ttu-id="1d9bf-103">Pöördkäibemaks</span><span class="sxs-lookup"><span data-stu-id="1d9bf-103">Reverse charge VAT</span></span>


[!include [banner](../includes/banner.md)]


<span data-ttu-id="1d9bf-104">Selles teemas kirjeldatakse üldist lähenemist Euroopa riikide ja Saudi Araabia pöördkäibemaksu (KM) seadistamisele.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-104">This topic describes a generic approach for setting up reverse charge value-added tax (VAT) for Saudi Arabia, Singapore, and European countries.</span></span>

<span data-ttu-id="1d9bf-105">Pöördmaks on maksuskeem, mis viib käibemaksu arvestamise ja registreerimise kohustuse kaupade ja/või teenuste müüjalt ostjale.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-105">Reverse Charge is a tax schema that moves the responsibility for the accounting and reporting of VAT from the seller to the buyer of goods and/or services.</span></span> <span data-ttu-id="1d9bf-106">Seetõttu registreerivad kaupade ja/või teenuste saajad nii arvestatud käibemaksu (müüja rollis) kui ka sisendkäibemaksu (ostja rollis) oma käibemaksuaruandes.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-106">Therefore, recipients of goods and/or services report both the output VAT (in the role of a seller) and the input VAT (in the role of a purchaser) on their VAT statement.</span></span>

<span data-ttu-id="1d9bf-107">Mõnes riigis või regioonis rakendatakse pöördmaksu skeemi ainult mõne kauba ja/või teenuse puhul ja müügisummadele on kehtestatud lisatingimused või piirväärtused.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-107">In some countries or regions, the Reverse Charge schema is implemented only for some goods and/or services, and there are additional conditions or thresholds on sales amounts.</span></span> <span data-ttu-id="1d9bf-108">Teistes riikides või regioonides sõltub vastutus käibemaksu tasumise eest tarnija ja ostja olekust.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-108">In other countries or regions, the responsibility for VAT payment depends on the status of the supplier and the buyer.</span></span> <span data-ttu-id="1d9bf-109">Kui ostja on käibemaksukohustuslane, peab see asjaolu olema tarnija väljastatud arvel märgitud.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-109">If the buyer is liable to pay VAT, this fact must be clearly indicated on the invoice that the supplier issues.</span></span> <span data-ttu-id="1d9bf-110">Näiteks peavad arvel olema sõnad „pöördmaks” ja peab olema näidatud, millised kaubakoodid kuuluvad pöördmaksu skeemi alla.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-110">For example, the invoice must include the words "Reverse charge" and must indicate which positions are under the Reverse Charge schema.</span></span> 

<span data-ttu-id="1d9bf-111">Pöördmaksu rakendamiseks tuleb teha järgmine seadistus.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-111">To apply the reverse charge, you must complete the following setup.</span></span>

## <a name="set-up-sales-tax-codes"></a><span data-ttu-id="1d9bf-112">Saate häälestada käibemaksukoode.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-112">Set up sales tax codes</span></span>
<span data-ttu-id="1d9bf-113">Soovitame kasutada müügi- ja ostutoimingute jaoks eraldi käibemaksukoode.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-113">We recommend that you use separate sales tax codes for sales operations and purchase operations.</span></span>

<table>
<body>
<tr>
<td><span data-ttu-id="1d9bf-114"><strong>Müügi käibemaksukood</strong></span><span class="sxs-lookup"><span data-stu-id="1d9bf-114"><strong>Sales tax code for sales</strong></span></span></td>
<td><span data-ttu-id="1d9bf-115">Looge käibemaksukood müügi pöördmaksu toimingutele (<strong>Maks</strong> &gt; <strong>Kaudsed maksud</strong> &gt; <strong>Käibemaks</strong> &gt; <strong>Käibemaksukoodid</strong>).</span><span class="sxs-lookup"><span data-stu-id="1d9bf-115">Create a sales tax code for reverse charge sales operations (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax codes</strong>).</span></span>
</td>
</tr>
<tr>
<td><span data-ttu-id="1d9bf-116"><strong>Ostude käibemaksukood</strong></span><span class="sxs-lookup"><span data-stu-id="1d9bf-116"><strong>Sales tax code for purchases</strong></span></span></td>
<td><p><span data-ttu-id="1d9bf-117">Looge positiivsed ja negatiivsed käibemaksukoodid ostude pöördkäibemaksule (<strong>Maks</strong> &gt; <strong>Kaudsed maksud</strong> &gt; <strong>Käibemaks</strong> &gt; <strong>Käibemaksukoodid</strong>).</span><span class="sxs-lookup"><span data-stu-id="1d9bf-117">Create positive and negative sales tax codes for the reverse charge VAT for purchases (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax codes</strong>).</span></span></p>
<ol>
<li><span data-ttu-id="1d9bf-118">Looge positiivse väärtusega käibemaksukood.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-118">Create a sales tax code that has a positive value.</span></span></li>
<li><span data-ttu-id="1d9bf-119">Looge negatiivse väärtusega käibemaksukood.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-119">Create a sales tax code that has a negative value.</span></span> <span data-ttu-id="1d9bf-120">Määrake valiku <strong>Luba negatiivset käibemaksuprotsenti</strong> väärtuseks <strong>Jah</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-120">Set the <strong>Allow negative sales tax percentage</strong> option to <strong>Yes</strong>.</span></span>
<span data-ttu-id="1d9bf-121">See negatiivne käibemaksukood tuleb määrata kauba käibemaksugrupile ja seejärel selle kauba käibemaksugrupi kaupadele, mis kuuluvad pöördmaksuga käibemaksustamisele.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-121">You must assign this negative sales tax code to an item sales tax group and then assign that item sales tax group to the items that are subject to the reverse charge VAT.</span></span></li>
</ol>
<p><span data-ttu-id="1d9bf-122">Lisateavet leiate järgmisest jaotisest &quot;Käibemaksugruppide ja kauba käibemaksugruppide häälestamine&quot;.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-122">For more information, see the next section, &quot;Set up sales tax groups and item sales tax groups.&quot;</span></span></p>
</td>
</tr>
</tbody>
</table>

## <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="1d9bf-123">Käibemaksugruppide ja kauba käibemaksugruppide seadistamine</span><span class="sxs-lookup"><span data-stu-id="1d9bf-123">Set up sales tax groups and item sales tax groups</span></span>
<span data-ttu-id="1d9bf-124">Soovitame kasutada müügi- ja ostutoimingute jaoks eraldi käibemaksugruppe.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-124">We recommend that you use separate sales tax groups for sales operations and purchase operations.</span></span>

<table>
<tr>
<td><span data-ttu-id="1d9bf-125"><strong>Müügi käibemaksugrupid</strong></span><span class="sxs-lookup"><span data-stu-id="1d9bf-125"><strong>Sales tax groups for sales</strong></span></span></td>
<td><span data-ttu-id="1d9bf-126">Looge käibemaksugrupp pöördmaksuga müügitoimingutele (<strong>Maks</strong> &gt; <strong>Kaudsed maksud</strong> &gt; <strong>Käibemaks</strong> &gt; <strong>Käibemaksugrupid</strong>).</span><span class="sxs-lookup"><span data-stu-id="1d9bf-126">Create a sales tax group for sales operations that have the reverse charge (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax groups</strong>).</span></span> <span data-ttu-id="1d9bf-127">Vahekaardil <strong>Seadistus</strong> lisage sellesse gruppi pöördmaksu käibemaksukood.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-127">On the <strong>Setup</strong> tab, include the sales tax code for the reverse charge in this group.</span></span> <span data-ttu-id="1d9bf-128">Märkige käibemaksukoodi väljad <strong>Vabastus</strong> ja <strong>Pöördmaks</strong>.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-128">Select the <strong>Exempt</strong> and <strong>Reverse charge</strong> check boxes for the sales tax code.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d9bf-129"><strong>Ostude käibemaksugrupid</strong></span><span class="sxs-lookup"><span data-stu-id="1d9bf-129"><strong>Sales tax groups for purchases</strong></span></span></td>
<td><span data-ttu-id="1d9bf-130">Looge käibemaksugrupp pöördmaksuga ostutoimingutele (<strong>Maks</strong> &gt; <strong>Kaudsed maksud</strong> &gt; <strong>Käibemaks</strong> &gt; <strong>Käibemaksugrupid</strong>).</span><span class="sxs-lookup"><span data-stu-id="1d9bf-130">Create a sales tax group for purchase operations that have the reverse charge (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax groups</strong>).</span></span> <span data-ttu-id="1d9bf-131">Lisage vahekaardile <strong>Seadistus</strong> nii positiivsed kui ka negatiivsed käibemaksukoodid selles grupis.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-131">On the <strong>Setup</strong> tab, include both positive and negative sales tax codes in this group.</span></span> <span data-ttu-id="1d9bf-132">Märkige ruut <strong>Pöördmaks</strong> käibemaksukoodile, millel on negatiivne väärtus.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-132">Select the <strong>Reverse charge</strong> check box for the sales tax code that has a negative value.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1d9bf-133"><strong>Kauba käibemaksugrupid</strong></span><span class="sxs-lookup"><span data-stu-id="1d9bf-133"><strong>Item sales tax groups</strong></span></span></td>
<td><span data-ttu-id="1d9bf-134">Looge või värskendage kauba käibemaksugrupp käibemaksukoodiga, millel on negatiivne väärtus (<strong>Maks</strong> &gt; <strong>Kaudsed maksud</strong> &gt; <strong>Käibemaks</strong> &gt; <strong>Kauba käibemaksugrupid</strong>).</span><span class="sxs-lookup"><span data-stu-id="1d9bf-134">Create or update the item sales tax group with the sales tax code that has a negative value (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Item sales tax groups</strong>).</span></span> <span data-ttu-id="1d9bf-135">Kauba käibemaksu vaikegrupp tuleb määrata toodetele ja kategooriatele, millele kohaldatakse pöördmaksu.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-135">You must assign the default item sales tax group to the products and categories that are subject to the reverse charge.</span></span></td>
</tr>
</table>

## <a name="set-up-reverse-charge-groups"></a><span data-ttu-id="1d9bf-136">Pöördmaksu gruppide seadistamine</span><span class="sxs-lookup"><span data-stu-id="1d9bf-136">Set up reverse charge groups</span></span>
<span data-ttu-id="1d9bf-137">Lehel **Pöördmaksu kaubagrupid** (**Maks** &gt; **Seadistus** &gt; **Käibemaks** &gt; **Pöördmaksu kaubagrupid**) saate määratleda toodete või teenuste gruppe või eraldi tooteid või teenuseid, millele pöördmaksu saab rakendada.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-137">On the **Reverse charge item groups** page (**Tax** &gt; **Setup** &gt; **Sales tax** &gt; **Reverse charge item groups**), you can define groups of products or services, or individual products or services, that the reverse charge can be applied to.</span></span> <span data-ttu-id="1d9bf-138">Määratlege iga pöördmaksu kaubagrupi puhul kaupade loend, kaubagrupid ja kategooriad müügi ja/või ostude jaoks.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-138">For each reverse charge item group, define the list of items, item groups, and categories for sales and/or purchases.</span></span>

## <a name="set-up-reverse-charge-rules"></a><span data-ttu-id="1d9bf-139">Pöördmaksu reeglite häälestamine</span><span class="sxs-lookup"><span data-stu-id="1d9bf-139">Set up reverse charge rules</span></span>
<span data-ttu-id="1d9bf-140">Lehel **Pöördmaksu reeglid** (**Maks** &gt; **Seadistus** &gt; **Käibemaks** &gt; **Pöördmaksu reeglid**) saate määratleda rakendatavuse reeglid ostu ja müügi eesmärkidele.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-140">On the **Reverse charge rules** page (**Tax** &gt; **Setup** &gt; **Sales tax** &gt; **Reverse charge rules**), you can define the applicability rules for purchase and sales purposes.</span></span> <span data-ttu-id="1d9bf-141">Saate konfigureerida pöördmaksu rakendatavuse reeglikogumi.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-141">You can configure a set of reverse charge applicability rules.</span></span> <span data-ttu-id="1d9bf-142">Määrake igale reeglile järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-142">For each rule, set the following fields:</span></span>

- <span data-ttu-id="1d9bf-143">**Dokumendi tüüp** – valige **Ostutellimus**, **Hankija arve tööleht**, **Müügitellimus**, **Vabas vormis arve**, **Kliendi arve tööleht** ja/või **Hankija arve**.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-143">**Document type** – Select **Purchase order**, **Vendor invoice journal**, **Sales order**, **Free text invoice**, **Customer invoice journal**, and/or **Vendor invoice**.</span></span>
- <span data-ttu-id="1d9bf-144">**Partneri riigi/piirkonna tüüp** – valige **Kodumaine**, **EL** või **Välismaine**.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-144">**Country/region type of the partner** – Select **Domestic**, **EU**, or **Foreign**.</span></span> <span data-ttu-id="1d9bf-145">Kui reeglit ei saa rakendada kõigile äripartneritele, olenemata nende aadressi riigist või piirkonnast, siis on teine võimalus valida **Kõik**.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-145">Alternatively, if the rule can be applied to all trade partners, regardless of the country or region of their address, select **All**.</span></span>
- <span data-ttu-id="1d9bf-146">**Riigisisene tarneaadress** – märkige see ruut reegli rakendamiseks tarnetele samas riigis või piirkonnas.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-146">**Domestic delivery address** – Select this check box to apply the rule to deliveries within the same country or region.</span></span> <span data-ttu-id="1d9bf-147">Seda ruutu ei saa dokumenditüüpide **Hankija arve tööleht** ja **Kliendi arve tööleht** puhul valida.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-147">This check box can't be selected for the **Vendor invoice journal** and **Customer invoice journal** document types.</span></span>
- <span data-ttu-id="1d9bf-148">**Pöördmaksu kaubagrupp** – valige grupp, millele reeglit saab rakendada.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-148">**Reverse charge item group** – Select the group that the rule can be applied to.</span></span>
- <span data-ttu-id="1d9bf-149">**Lävisumma** – pöördmaksu skeem rakendatakse arvele ainult juhul, kui pöördmaksu kaubagrupis sisalduvate kaupade ja/või teenuste väärtus ületab siin määratud piirväärtuse.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-149">**Threshold amount** – The Reverse Charge schema is applied to an invoice only if the value of items and/or services that are included in the reverse charge item group exceeds the limit that you specify here.</span></span>

<span data-ttu-id="1d9bf-150">Võite kasutada ka välju **Jõustumiskuupäev** ja **Aegumiskuupäev** reegli kehtivusperioodi määramiseks.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-150">You can also use the **Effective date** and **Expiration date** fields to define the period when the rule is effective.</span></span>

<span data-ttu-id="1d9bf-151">Lisaks saate määrata, kas kuvatakse teade ja dokumendireale lisatakse pöördkäibemaksu vaikegrupp, kui selle dokumendirea tingimus on täidetud.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-151">Additionally, you can specify whether a notification appears and the document line is updated with the default reverse charge sales tax group if the condition for that document line is met.</span></span> <span data-ttu-id="1d9bf-152">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="1d9bf-152">The following options are available:</span></span>

- <span data-ttu-id="1d9bf-153">**Puudub** – dokumendirida ei uuendata.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-153">**None** – The document line isn't updated.</span></span>
- <span data-ttu-id="1d9bf-154">**Küsi** – kuvatakse teade, milles küsitakse kinnitust, kas pöördmaksu saab rakendada.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-154">**Prompt** – A notification appears to confirm that the reverse charge can be applied.</span></span>
- <span data-ttu-id="1d9bf-155">**Määra** – dokumendi rida uuendatakse täiendava teatiseta.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-155">**Set** – The document line is updated without additional notification.</span></span>

## <a name="set-up-default-parameters"></a><span data-ttu-id="1d9bf-156">Vaikeparameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="1d9bf-156">Set up default parameters</span></span>
<span data-ttu-id="1d9bf-157">Pöördkäibemaksu funktsiooni lubamiseks määrake lehel **Pearaamatu parameetrid** vahekaardil **Pöördmaks** suvandi **Luba pöördmaks** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-157">To enable the functionality for reverse charge VAT, on the **General ledger parameters** page, on the **Reverse charge** tab, set the **Enable reverse charge** option to **Yes**.</span></span> <span data-ttu-id="1d9bf-158">Valige väljadel **Ostutellimuse käibemaksugrupp** ja **Müügitellimuse maksugrupp** käibemaksu vaikegrupid.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-158">In the **Purchase order sales tax group** and **Sales order tax group** fields, select the default sales tax groups.</span></span> <span data-ttu-id="1d9bf-159">Kui pöördmaksu rakendatavuse tingimus on täidetud, lisatakse müügi- või ostutellimuse reale need käibemaksugrupid.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-159">When a reverse charge applicability condition is met, the sales or purchase order line is updated with these sales tax groups.</span></span>

## <a name="reverse-charge-on-a-sales-invoice"></a><span data-ttu-id="1d9bf-160">Pöördmaks müügiarvel</span><span class="sxs-lookup"><span data-stu-id="1d9bf-160">Reverse charge on a sales invoice</span></span>
<span data-ttu-id="1d9bf-161">Müügi korral pöördmaksu skeemi alusel ei küsi müüja käibemaksu.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-161">For sales under the Reverse Charge schema, the seller doesn't charge VAT.</span></span> <span data-ttu-id="1d9bf-162">Selle asemel on arvel näidatud nii kaubad, millelt nõutakse pöördkäibemaksu, kui ka pöördkäibemaksu koondsumma.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-162">Instead, the invoice indicates both the items that are subject to the reverse charge VAT and the total amount of the reverse charge VAT.</span></span>

<span data-ttu-id="1d9bf-163">Kui sisestatakse pöördkäibemaksuga müügiarve, on müügikannetel maksusuund **Tasumisele kuuluv käibemaks** ja nullkäibemaks ning ruut **Pöördmaks** on märgitud.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-163">When a sales invoice that has the reverse charge is posted, the sales tax transactions have the **Sales tax payable** tax direction and zero sales tax, and the **Reverse charge** check box is selected.</span></span>

## <a name="reverse-charge-on-a-purchase-invoice"></a><span data-ttu-id="1d9bf-164">Pöördmaks ostuarvel</span><span class="sxs-lookup"><span data-stu-id="1d9bf-164">Reverse charge on a purchase invoice</span></span>
<span data-ttu-id="1d9bf-165">Ostude korral pöördmaksu skeemi alusel tegutseb ostja, kes saab pöördmaksuga arve, käibemaksuarvestuse seisukohast ostja ja müüjana.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-165">For purchases under the Reverse Charge schema, the purchaser who receives the invoice that has the reverse charge acts as a buyer and a seller for VAT accounting purposes.</span></span>

<span data-ttu-id="1d9bf-166">Pöördmaksuga ostuarve sisestamisel luuakse kaks käibemaksukannet.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-166">When a purchase invoice that has the reverse charge is posted, two sales tax transactions are created.</span></span> <span data-ttu-id="1d9bf-167">Ühel kandel on maksusuund **Saadaolev käibemaks**.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-167">One transaction has the **Sales tax receivable** tax direction.</span></span> <span data-ttu-id="1d9bf-168">Teisel kandel on maksusuund **Tasumisele kuuluv käibemaks** ja märgitud on ruut **Pöördmaks**.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-168">The other transaction has the **Sales tax payable** tax direction, and the **Reverse charge** check box is selected.</span></span>

<span data-ttu-id="1d9bf-169">Järgneval kuvatõmmisel on ühe kande suund **Saadaolev käibemaks** ja teise kande suund **Tasumisele kuuluv käibemaks**.</span><span class="sxs-lookup"><span data-stu-id="1d9bf-169">In the following screenshot, one transaction has the **Sales tax receivable** direction, and the other transaction has the **Sales tax payable** direction.</span></span> 

![Sisestatud käibemaks](media/apac-sau-posted-sales-tax.png)
