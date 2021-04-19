---
title: Tooteteabe tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada tooteteabega töötamisel tekkivaid probleeme.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a05e9957363ef6a659e25ceba84a168507cd641a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841523"
---
# <a name="troubleshoot-product-information"></a><span data-ttu-id="871d1-103">Tooteteabe tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="871d1-103">Troubleshoot product information</span></span>

<span data-ttu-id="871d1-104">Selles teemas kirjeldatakse, kuidas lahendada tooteteabega töötamisel tekkivaid probleeme.</span><span class="sxs-lookup"><span data-stu-id="871d1-104">This topic describes how to fix issues that you might encounter while you work with product information.</span></span>

## <a name="i-cant-delete-a-released-product"></a><span data-ttu-id="871d1-105">Väljastatud toodet ei saa kustutada.</span><span class="sxs-lookup"><span data-stu-id="871d1-105">I can't delete a released product.</span></span>

### <a name="issue-description"></a><span data-ttu-id="871d1-106">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="871d1-106">Issue description</span></span>

<span data-ttu-id="871d1-107">Väljastatud toote ja kõigi selle variante saate kustutada ainult siis, kui väljastatud tootel pole seotud kandeid.</span><span class="sxs-lookup"><span data-stu-id="871d1-107">You can delete a released product and all its variants only if the released product doesn't have any related transactions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="871d1-108">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="871d1-108">Issue resolution</span></span>

<span data-ttu-id="871d1-109">Väljastatud toote või toote koondandmete kustutamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="871d1-109">Follow these steps to delete a released product or product master.</span></span>

1. <span data-ttu-id="871d1-110">Sulgege kaupade kõik avatud kanded.</span><span class="sxs-lookup"><span data-stu-id="871d1-110">Close all open transactions for the items.</span></span>
1. <span data-ttu-id="871d1-111">Vähendage varude väärtuseks 0 (null).</span><span class="sxs-lookup"><span data-stu-id="871d1-111">Reduce the inventory to 0 (zero).</span></span>
1. <span data-ttu-id="871d1-112">Teostage lao sulgemine.</span><span class="sxs-lookup"><span data-stu-id="871d1-112">Perform inventory closing.</span></span>
1. <span data-ttu-id="871d1-113">Kustutage toote koondandmetest kõik toote variandid, mida soovite kustutada.</span><span class="sxs-lookup"><span data-stu-id="871d1-113">Delete all product variants for the product master that you want to delete.</span></span>

## <a name="can-i-change-the-item-number-of-a-released-product"></a><span data-ttu-id="871d1-114">Kas ma saan muuta väljastatud toote kaubakoodi?</span><span class="sxs-lookup"><span data-stu-id="871d1-114">Can I change the item number of a released product?</span></span>

<span data-ttu-id="871d1-115">Enamikul juhtudel ei saa muuta väljastatud toodete kaubakoode, kuna see muudatus põhjustab teabe riknemist.</span><span class="sxs-lookup"><span data-stu-id="871d1-115">In most cases, you can't edit item numbers for released products, because that change will cause data to become corrupted.</span></span> <span data-ttu-id="871d1-116">Kaubakoodi saate muuta ainult siis, kui peate parandama andmete korruptsiooni, mille põhjustas selle väljastatud toote esmase võtme ümbernimetamine, nagu on mainitud [eemaldatud või iganenud funktsioonid Finance and Operations 10.0.0 platvormi uuendusega 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span><span class="sxs-lookup"><span data-stu-id="871d1-116">You can edit the item number only if you must repair data corruption that was caused by a previous rename of the primary key of that released product, as mentioned in the list of [removed or deprecated features for Finance and Operations 10.0.0 with Platform update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span></span>

<span data-ttu-id="871d1-117">Kui soovite redigeerida väljastatud toodete kaubakoode, siis [hääletage selle idee poolt ideede portaalis](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span><span class="sxs-lookup"><span data-stu-id="871d1-117">If you want to be able to edit item numbers for released products, [vote for this idea in Ideas portal](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span></span>

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a><span data-ttu-id="871d1-118">Toote vaikimisi tühjendamise põhimõtet ei sisestata koosluse reale.</span><span class="sxs-lookup"><span data-stu-id="871d1-118">The default flushing principle from the product isn't being entered on the bill of materials line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="871d1-119">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="871d1-119">Issue description</span></span>

<span data-ttu-id="871d1-120">Kui lisate koosluse reale kauba, ei kasuta süsteem kaubale seadistatud vaikimisi tühjendamise põhimõtte teavet.</span><span class="sxs-lookup"><span data-stu-id="871d1-120">When you add an item to a bill of materials (BOM) line, the system doesn't use the default flushing principle information that is set up for the item.</span></span> <span data-ttu-id="871d1-121">Teisisõnu ei kuvata kauba tühjendamise põhimõtet **Koosluse real**.</span><span class="sxs-lookup"><span data-stu-id="871d1-121">In other words, the flushing principle from the item doesn't appear on the **BOM line** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="871d1-122">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="871d1-122">Issue resolution</span></span>

<span data-ttu-id="871d1-123">Kui määrate koosluse rea jaoks tühjendamise põhimõtte, rakendub see koosluse reale.</span><span class="sxs-lookup"><span data-stu-id="871d1-123">If you specify a flushing principle on a BOM line, it will apply to that BOM line.</span></span> <span data-ttu-id="871d1-124">Kui tühjendamise põhimõte on tühi või kui see pole seatud koosluse reale, rakendub koosluse reale endiselt kaubale seadistatud tühjendus, kuigi seda ei ole koosluse real kuvatud.</span><span class="sxs-lookup"><span data-stu-id="871d1-124">However, if the flushing principle is blank, or if it isn't set on a BOM line, the flushing principle that is set on the item will still apply to that BOM line, even though it isn't shown on the BOM line.</span></span>

<span data-ttu-id="871d1-125">Microsoft Dynamics 365 Supply Chain Management rakenduse muude funktsioonide vaike-loogika ei tööta tavaliselt sel viisil.</span><span class="sxs-lookup"><span data-stu-id="871d1-125">The defaulting logic for other features in Microsoft Dynamics 365 Supply Chain Management doesn't usually work in this way.</span></span> <span data-ttu-id="871d1-126">Praegust käitumist ei saa aga muuta.</span><span class="sxs-lookup"><span data-stu-id="871d1-126">However, the current behavior can't be changed.</span></span> <span data-ttu-id="871d1-127">Vastasel korral võidakse mõned olemasolevad kohandused, mis sellele tuginevad, katki minna.</span><span class="sxs-lookup"><span data-stu-id="871d1-127">Otherwise, some existing customizations that rely on it might be broken.</span></span>

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a><span data-ttu-id="871d1-128">Süsteem võimaldab mul salvestada erinevatele kaupadele või erinevate dimensioonidega samale kaubale dubleeritud vöötkoode.</span><span class="sxs-lookup"><span data-stu-id="871d1-128">The system lets me save duplicate bar codes for different items or for the same item that has different dimensions.</span></span>

<span data-ttu-id="871d1-129">Süsteem ei jõusta praegu kordumatuid vöötkoode ja selle piirangu lisamine oleks murranguline muutus.</span><span class="sxs-lookup"><span data-stu-id="871d1-129">The system doesn't currently enforce unique bar codes, and the addition of this restriction would be a breaking change.</span></span> <span data-ttu-id="871d1-130">Microsoftil on tõestus selle kohta, et see muudatus rikub mõningate olemasolevate klientide paigaldused.</span><span class="sxs-lookup"><span data-stu-id="871d1-130">In fact, Microsoft has evidence that some existing customer installations would be broken by this change.</span></span> <span data-ttu-id="871d1-131">Siiski kaalume laiemat kujunduse muudatust, et seda funktsiooni tulevikus lubada.</span><span class="sxs-lookup"><span data-stu-id="871d1-131">However, we will consider a broader design change to enable this feature in the future.</span></span>

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a><span data-ttu-id="871d1-132">Kauba kirje mallide redigeerimisel kuvatakse järgmine tõrketeade: "Lao asukohta ei saa luua, kuna kaupa ei ole laos.</span><span class="sxs-lookup"><span data-stu-id="871d1-132">I receive the following error message when I edit item record templates: "The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="871d1-133">Laos olevate kaupade puhul peab seostatud kauba mudeli grupis olema valitud laos olev toode. "</span><span class="sxs-lookup"><span data-stu-id="871d1-133">To stock items, the Stocked product option on the associated item model group must be selected."</span></span>

### <a name="issue-description"></a><span data-ttu-id="871d1-134">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="871d1-134">Issue description</span></span>

<span data-ttu-id="871d1-135">See probleem ilmneb juhul, kui te järgite neid samme, et proovida luua malli kauba jaoks, mida ei ole laos.</span><span class="sxs-lookup"><span data-stu-id="871d1-135">This issue occurs if you follow these steps to try to create a template for an item that isn't stocked.</span></span>

1. <span data-ttu-id="871d1-136">Avage väljastatud toode, mida ei ole laos.</span><span class="sxs-lookup"><span data-stu-id="871d1-136">Open a released product that isn't stocked.</span></span>
1. <span data-ttu-id="871d1-137">Toiminguriba vahekaardil **Valikud** valige suvand **Teabe salvestamine**.</span><span class="sxs-lookup"><span data-stu-id="871d1-137">On the Action Pane, on the **Options** tab, select **Record info**.</span></span>
1. <span data-ttu-id="871d1-138">Valige **Teabe salvestamine** dialoogiaknas **Ettevõtte kontode mall**.</span><span class="sxs-lookup"><span data-stu-id="871d1-138">In the **Record information** dialog box, select **Company accounts template**.</span></span>

<span data-ttu-id="871d1-139">Sellisel juhul kuvatakse järgnev veateade:</span><span class="sxs-lookup"><span data-stu-id="871d1-139">In this case, you receive the following error message:</span></span>

> <span data-ttu-id="871d1-140">Lao asukohta ei saa luua, kuna kaupa ei ole laos.</span><span class="sxs-lookup"><span data-stu-id="871d1-140">The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="871d1-141">Laos olevate kaupade puhul peab seostatud kauba mudeli grupis olema valitud laos olev toode.</span><span class="sxs-lookup"><span data-stu-id="871d1-141">To stock items, the Stocked product option on the associated item model group must be selected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="871d1-142">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="871d1-142">Issue resolution</span></span>

<span data-ttu-id="871d1-143">Toote mallide loomise protsess nõuab täiendavat toote-spetsiifilist loogikat.</span><span class="sxs-lookup"><span data-stu-id="871d1-143">The process of creating product templates requires extra product-specific logic.</span></span> <span data-ttu-id="871d1-144">Seetõttu ei saa selleks otstarbeks kasutada üldist **Ettevõte kontode mallid** nuppu.</span><span class="sxs-lookup"><span data-stu-id="871d1-144">Therefore, you can't use the generic **Company accounts template** button for this purpose.</span></span> <span data-ttu-id="871d1-145">Selle asemel toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="871d1-145">Instead, follow these steps.</span></span>

1. <span data-ttu-id="871d1-146">Avage väljastatud toode.</span><span class="sxs-lookup"><span data-stu-id="871d1-146">Open a released product.</span></span>
1. <span data-ttu-id="871d1-147">Toiminguribal valige **Toote** vahekaardil **Uus** grupis **Mall \> Loo jagatud mall**.</span><span class="sxs-lookup"><span data-stu-id="871d1-147">On the Action Pane, on the **Product** tab, in the **New** group, select **Template \> Create shared template**.</span></span>

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a><span data-ttu-id="871d1-148">Toote atribuutides lisatud vaikimisi abiteksti ei sisestata väljastatud tootesse.</span><span class="sxs-lookup"><span data-stu-id="871d1-148">Default Help text that is added in product attributes isn't entered in a released product.</span></span>

<span data-ttu-id="871d1-149">Kirjeldus ja abitekst, mis lisatakse toote atribuutidele, ei ole kuvatud ega sisestatud vaikimisi väljastatud toodetes.</span><span class="sxs-lookup"><span data-stu-id="871d1-149">A description and Help text that are added in the product attributes aren't visible or entered by default in the released products.</span></span> <span data-ttu-id="871d1-150">Selline käitumine on nii kavandatud.</span><span class="sxs-lookup"><span data-stu-id="871d1-150">This behavior is by design.</span></span>

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a><span data-ttu-id="871d1-151">Vaikimisi sisestatav kogus erineb, kui see on registreeritud kooslusest ja kui see on registreeritud koosluse versioonist.</span><span class="sxs-lookup"><span data-stu-id="871d1-151">The default quantity that is entered differs when it's registered from a BOM and when it's registered from a BOM version.</span></span>

### <a name="issue-description"></a><span data-ttu-id="871d1-152">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="871d1-152">Issue description</span></span>

<span data-ttu-id="871d1-153">Kui lisate kauba kooslusele, seatakse koguse väärtuseks 1, selle asemel, et näidata **Min tellimuse kogus** väljal defineeritud kogust valitud toote **Vaikimisi valitud sätete** lehel.</span><span class="sxs-lookup"><span data-stu-id="871d1-153">By default, when you add an item to a BOM, the quantity is set to 1 instead of the quantity that is defined in the **Min. order quantity** field on the **Default order settings** page for a selected product.</span></span> <span data-ttu-id="871d1-154">Kuid kui lisate kauba koosluse versioonist ning kaup ja variant on valitud, võtab vaikimisi sisestatud kogus arvesse minimaalset kogust, mis on määratud kindla dimensiooni jaoks määratud vaikimisi tellimuse sätetes.</span><span class="sxs-lookup"><span data-stu-id="871d1-154">However, when you add an item from a BOM version, and the item and variant are selected, the quantity that is entered by default takes into account the minimum quantity that is set in the default order settings for the specific dimensions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="871d1-155">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="871d1-155">Issue resolution</span></span>

<span data-ttu-id="871d1-156">Selline käitumine on oodatud.</span><span class="sxs-lookup"><span data-stu-id="871d1-156">This behavior is expected.</span></span> <span data-ttu-id="871d1-157">Kuid seejuures on teada probleem, et see loogika erinev koosluses ja koosluse versioonis.</span><span class="sxs-lookup"><span data-stu-id="871d1-157">However, the fact that the logic differs in the BOM and the BOM version is a known issue.</span></span> <span data-ttu-id="871d1-158">Sellegipoolest ei muudeta seda käitumist, kuna muudatus võib mõjutada paljude erinevate klientide stsenaariume.</span><span class="sxs-lookup"><span data-stu-id="871d1-158">Nevertheless, this behavior won't be changed, because a change could affect many different customer scenarios.</span></span>

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a><span data-ttu-id="871d1-159">Väljastatud toote üksikasjades ei saa muuta manustatud pilte, mis laaditi alla toote dokumendi manuste andmete üksusest.</span><span class="sxs-lookup"><span data-stu-id="871d1-159">In the released product details, I can't change the attached images that were uploaded from the Product document attachments data entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="871d1-160">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="871d1-160">Issue description</span></span>

<span data-ttu-id="871d1-161">See probleem võib ilmneda, kui manustate pildi kaubale, kasutades *Toote dokumendi manustes* olevaid andmeid.</span><span class="sxs-lookup"><span data-stu-id="871d1-161">This issue can occur when you attach an image to an item by using the *Product document attachments* data entity.</span></span> <span data-ttu-id="871d1-162">Sel juhul kuvatakse kauba pilt kauba kohta.</span><span class="sxs-lookup"><span data-stu-id="871d1-162">In this case, the item image is shown for the item.</span></span> <span data-ttu-id="871d1-163">Kui aga valite **Muuda pilti**, ei kuvata üleslaetud piltide loendis mitte midagi.</span><span class="sxs-lookup"><span data-stu-id="871d1-163">However, if you select **Change image**, nothing is shown in the list of uploaded images.</span></span> <span data-ttu-id="871d1-164">Lisaks ei kuvata kaubale manuseid.</span><span class="sxs-lookup"><span data-stu-id="871d1-164">Additionally, no attachments are shown for the item.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="871d1-165">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="871d1-165">Issue resolution</span></span>

<span data-ttu-id="871d1-166">*EcoResProductDocumentAttachmentEntity* üksus (*Toote dokumendi manused*) impordib dokumendi manused *toodetele*, kuid mitte *väljastatud toodetele*.</span><span class="sxs-lookup"><span data-stu-id="871d1-166">The *EcoResProductDocumentAttachmentEntity* entity (*Product document attachments*) imports document attachments for *products* but not for *released products*.</span></span> <span data-ttu-id="871d1-167">(Väljastatud tooted on tuntud ka kui *kaubad*.) Kui soovite vaadata kauba manuseid **Väljastatud toote üksikasjade** lehel, peate selle asemel kasutama *EcoResReleasedProductDocumentAttachmentEntity* üksust (*Väljastatud toote dokumendi manused*).</span><span class="sxs-lookup"><span data-stu-id="871d1-167">(Released products are also known as *items*.) To view the attachments for an item on the **Released product details** page, you must use the *EcoResReleasedProductDocumentAttachmentEntity* entity (*Released product document attachments*) instead.</span></span>

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a><span data-ttu-id="871d1-168">Microsoft Flow ühendus näitab järgmist tõrketeadet: "Värskendamine pole välja"ProductNumber" jaoks lubatud."</span><span class="sxs-lookup"><span data-stu-id="871d1-168">The Microsoft Flow connector shows the following error message: "Update not allowed for field 'ProductNumber'."</span></span>

### <a name="issue-description"></a><span data-ttu-id="871d1-169">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="871d1-169">Issue description</span></span>

<span data-ttu-id="871d1-170">See probleem ilmneb juhul, kui proovite uuendada välja **Tootenumber**, kasutades *Väljastatud toodete* üksust V2 ja Microsoft Flow rakendust.</span><span class="sxs-lookup"><span data-stu-id="871d1-170">This issue occurs if you try to update the **Product number** field by using the *Released products* entity V2 and Microsoft Flow.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="871d1-171">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="871d1-171">Issue resolution</span></span>

<span data-ttu-id="871d1-172">Selline käitumine on oodatud.</span><span class="sxs-lookup"><span data-stu-id="871d1-172">This behavior is expected.</span></span> <span data-ttu-id="871d1-173">Väljastatud toote tootenumbri redigeerimise võimalus eemaldati Dynamics 365 Finance and Operations 10.0.0 platvormiuuendusega 24, et aidata vältida andmete korruptsiooni.</span><span class="sxs-lookup"><span data-stu-id="871d1-173">The ability to edit the product number for a released product was removed in Dynamics 365 Finance and Operations 10.0.0 with platform update 24 to help prevent data corruption.</span></span> <span data-ttu-id="871d1-174">Erandjuhtudel, kui peate parandama rikutud andmeid, mille põhjustas väljastatud toote peamise võtme ümbernimetamine, võtke ühendust Microsofti tugiteenusega selle piirangu ajutise eemaldamise taotlemiseks.</span><span class="sxs-lookup"><span data-stu-id="871d1-174">In exceptional cases, where you must repair data corruption that was caused by a previous rename of the primary key of a released product, you can ask Microsoft Support to temporarily remove this restriction.</span></span>

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a><span data-ttu-id="871d1-175">Ma ei saa luua väljastatud toote varianti teises juriidilises isikus.</span><span class="sxs-lookup"><span data-stu-id="871d1-175">I can't create a released product variant in another legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="871d1-176">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="871d1-176">Issue description</span></span>

<span data-ttu-id="871d1-177">Kui proovite väljastada toote koondandmeid, millel pole variante, ja seejärel luua igas juriidilises isikus (ettevõttes) variandid, nagu need on nõutud, ei saa te variante väljastada kasutades selleks variantide soovitusi.</span><span class="sxs-lookup"><span data-stu-id="871d1-177">If you try to release a product master without variants, and then create the variants in each legal entity (company) as they are required, you won't be able to release the variants by using variant suggestions.</span></span> <span data-ttu-id="871d1-178">Samuti ei saa te variante käsitsi luua.</span><span class="sxs-lookup"><span data-stu-id="871d1-178">You also won't be able to manually create the variants.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="871d1-179">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="871d1-179">Issue resolution</span></span>

<span data-ttu-id="871d1-180">Selline käitumine on nii kavandatud.</span><span class="sxs-lookup"><span data-stu-id="871d1-180">This behavior is by design.</span></span> <span data-ttu-id="871d1-181">Toote koondandmete seoseid ja dimensioone, mida koondandmed saavad rakendada, hoitakse ühiskasutataval tasemel.</span><span class="sxs-lookup"><span data-stu-id="871d1-181">The relations of a product master and the dimensions that the master can take are kept at a shared level.</span></span> <span data-ttu-id="871d1-182">Seetõttu ei saa te luua saadaolevaid dimensioone ühise toote koondandmetele kindlas juriidilises isikus, kus need dimensioonid väljastatakse, ja seejärel korrata protsessi igas juriidilises isikus, kus dimensioone nõutakse.</span><span class="sxs-lookup"><span data-stu-id="871d1-182">Therefore, you can't create the available dimensions for a shared product master in the specific legal entity where those dimensions are released and then replicate the process in each legal entity where the dimensions are required.</span></span> <span data-ttu-id="871d1-183">Selle asemel peate muutma oma väljastusprotsessi, et kohanduda kavandatud protsessiga.</span><span class="sxs-lookup"><span data-stu-id="871d1-183">Instead, you must change your release process to adapt to the designed process.</span></span>

<span data-ttu-id="871d1-184">Siin on toodete väljastamise protsess.</span><span class="sxs-lookup"><span data-stu-id="871d1-184">Here is the process for releasing products.</span></span>

1. <span data-ttu-id="871d1-185">Looge ühiskasutatava toote koondandmed ja dimensioonid, mida saab juriidilistele isikutele väljastada.</span><span class="sxs-lookup"><span data-stu-id="871d1-185">Create the shared product master and the dimensions that can be released to the legal entities.</span></span>
1. <span data-ttu-id="871d1-186">Väljastage tooted juriidilistele isikutele kasutades variantide soovitusi või lisage väljastatavad kombinatsioonid käsitsi.</span><span class="sxs-lookup"><span data-stu-id="871d1-186">Release the products to the legal entities either by using variant suggestions or by manually adding the combinations that should be released.</span></span>

<span data-ttu-id="871d1-187">Teise võimalusena saate väljastatud toote luua otse.</span><span class="sxs-lookup"><span data-stu-id="871d1-187">Alternatively, you can directly create the released product.</span></span>

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a><span data-ttu-id="871d1-188">Kui ma vabastan variandi teises ettevõttes, kuvatakse järgmine tõrketeade: "Toote variant koos määratud dimensioonidega on juba loodud."</span><span class="sxs-lookup"><span data-stu-id="871d1-188">When I release a variant in another company, I receive the following error message: "Product variant with specified dimensions has already been created."</span></span>

### <a name="issue-description"></a><span data-ttu-id="871d1-189">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="871d1-189">Issue description</span></span>

<span data-ttu-id="871d1-190">Kui toote variant on juba väljastatud ettevõttes A ja proovite selle väljastada ettevõttes B, kasutades nuppu **Uus**, mis asub **Väljastatud toote variandid** lehel, kuvatakse järgmine tõrketeade:</span><span class="sxs-lookup"><span data-stu-id="871d1-190">If a product variant has already been released in a company A, and you try to release it in company B by using the **New** button on the **Released product variants** page, you will receive the following error message:</span></span>

> <span data-ttu-id="871d1-191">Määratud dimensioonidega tootevariant on juba loodud.</span><span class="sxs-lookup"><span data-stu-id="871d1-191">Product variant with specified dimensions has already been created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="871d1-192">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="871d1-192">Issue resolution</span></span>

<span data-ttu-id="871d1-193">**Uus** nupp **Väljastatud toote variandid** lehel loob variandi ja väljastab selle ettevõtte kontekstis.</span><span class="sxs-lookup"><span data-stu-id="871d1-193">The **New** button on the **Released product variants** page creates the variant and releases it in the company context.</span></span> <span data-ttu-id="871d1-194">Kui variant on juba loodud, ei saa te kasutada nuppu **Uus**, et see väljastada teises ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="871d1-194">If the variant has already been created, you can't use the **New** button to release it in another company.</span></span>

<span data-ttu-id="871d1-195">Probleemi lahendamiseks avage **Toote koondandmed** ja valige **Väljasta toode**, et väljastada olemasolev variant soovitud ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="871d1-195">To fix the issue, open the **Product master** page, and select **Release product** to release the existing variant in the desired company.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]