---
title: Meilimallide loomine kandesündmuste jaoks
description: Selles teemas kirjeldatakse, kuidas luua, üles laadida ja konfigureerida meilimalle Microsoft Dynamics 365 Commerce'i kandesündmuste jaoks.
author: bicyclingfool
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: bfc773bec035ceee151e2e2dd8925aa772747452
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019879"
---
# <a name="create-email-templates-for-transactional-events"></a><span data-ttu-id="32aa4-103">Meilimallide loomine kandesündmuste jaoks</span><span class="sxs-lookup"><span data-stu-id="32aa4-103">Create email templates for transactional events</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="32aa4-104">Selles teemas kirjeldatakse, kuidas luua, üles laadida ja konfigureerida meilimalle Microsoft Dynamics 365 Commerce'i kandesündmuste jaoks.</span><span class="sxs-lookup"><span data-stu-id="32aa4-104">This topic describes how to create, upload, and configure email templates for transactional events in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="32aa4-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="32aa4-105">Overview</span></span>

<span data-ttu-id="32aa4-106">Dynamics 365 Commerce pakub valmislahendust meilide saatmiseks, mis teavitavad kliente kandesündmustest (näiteks kui tellimus sisestatakse,kui tellimus on pealevõtmiseks valmis või kui tellimus on saadetud).</span><span class="sxs-lookup"><span data-stu-id="32aa4-106">Dynamics 365 Commerce provides an out-of-box solution for sending emails that alert customers about transactional events (for example, when an order is placed, an order is ready for pickup, or an order has been shipped).</span></span> <span data-ttu-id="32aa4-107">Selles teemas kirjeldatakse kandemeilide saatmiseks kasutatavate meilimallide loomist, üleslaadimist ja konfigureerimist.</span><span class="sxs-lookup"><span data-stu-id="32aa4-107">This topic describes the steps for creating, uploading, and configuring the email templates that are used to send transactional emails.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="32aa4-108">Loo e-kirja mall</span><span class="sxs-lookup"><span data-stu-id="32aa4-108">Create an email template</span></span>

<span data-ttu-id="32aa4-109">Enne kindla kandesündmuse vastendamist meilimallile, peate looma selle malli.</span><span class="sxs-lookup"><span data-stu-id="32aa4-109">Before you can map a specific transactional event to an email template, you must create the template.</span></span>

<span data-ttu-id="32aa4-110">Meilimalli loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="32aa4-110">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="32aa4-111">Avage Commerce'i headquarters, minge **Jaemüük ja Äri \> jaotises \>Organisatsiooni meilimallid** või **Organisatsiooni haldus \> Seadistamine \>  Organisatsiooni meilimallid**.</span><span class="sxs-lookup"><span data-stu-id="32aa4-111">In Commerce headquarters, go to **Retail and Commerce \> Headquarters setup \> Organization email templates** or **Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="32aa4-112">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="32aa4-112">Select **New**.</span></span>
1. <span data-ttu-id="32aa4-113">Seadistage jaotises **Üldine** järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="32aa4-113">Under **General**, set the following fields:</span></span>

    - <span data-ttu-id="32aa4-114">**Meili ID** – meili ID on selle malli kordumatu identifikaator ja see väärtus kuvatakse siis, kui valite malli sündmusele vastendamiseks.</span><span class="sxs-lookup"><span data-stu-id="32aa4-114">**Email ID** – The email ID is the unique identifier for a template, and it's the value that is shown when you select a template to map to an event.</span></span>
    - <span data-ttu-id="32aa4-115">**Meili kirjeldus** – saate kasutada seda valikulist välja malli kirjelduse lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="32aa4-115">**Email description** – You can use this optional field to provide a description of the template.</span></span> <span data-ttu-id="32aa4-116">Sisestatav väärtus kuvatakse ainult Commerce'i peakontoris.</span><span class="sxs-lookup"><span data-stu-id="32aa4-116">The value that you enter appears only in Commerce headquarters.</span></span>
    - <span data-ttu-id="32aa4-117">**Saatja nimi** – sisestatav nimi kuvatakse suurema osa meiliklientide puhul väljal „saatja”.</span><span class="sxs-lookup"><span data-stu-id="32aa4-117">**Sender name** – The name that you enter appears in the "from" field of most email clients.</span></span>
    - <span data-ttu-id="32aa4-118">**Saatja meiliaadress** – sisestage meiliaadress, mida tuleks kasutada selle malli abil saadetavate meilide puhul.</span><span class="sxs-lookup"><span data-stu-id="32aa4-118">**Sender email** – Enter the email address that should be used for emails that are sent by using this template.</span></span>
    - <span data-ttu-id="32aa4-119">**Vaikekeele kood** – see väli määrab vaikimisi saadetava meili lokaliseeritud versiooni, kui seda malli rakendav kanal pole määranud ühtegi keelt.</span><span class="sxs-lookup"><span data-stu-id="32aa4-119">**Default language code** – This field specifies the localized version of the email that is sent by default, if no language is provided by the channel that invokes this template.</span></span>

1. <span data-ttu-id="32aa4-120">Jaotises **Meilisõnumi sisu** valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="32aa4-120">Under **Email message content**, select **New**.</span></span>
1. <span data-ttu-id="32aa4-121">Sisestage väljale **Keel** meilimalli keel.</span><span class="sxs-lookup"><span data-stu-id="32aa4-121">In the **Language** field, enter the language for the email template.</span></span> <span data-ttu-id="32aa4-122">Hiljem saate lisada rohkem keeli ja lokaliseeritud malle.</span><span class="sxs-lookup"><span data-stu-id="32aa4-122">You can add more languages and localized templates later.</span></span>
1. <span data-ttu-id="32aa4-123">Sisestage väljale **Teema** meilisõnumi teema, mida kuvatakse meili teema väljal.</span><span class="sxs-lookup"><span data-stu-id="32aa4-123">In the **Subject** field, enter the email subject that should appear in the subject field of the email.</span></span>
1. <span data-ttu-id="32aa4-124">Meilimalli üleslaadimiseks valige **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="32aa4-124">Select **Edit** to upload your email template.</span></span>

## <a name="create-an-email-message-body-by-using-html"></a><span data-ttu-id="32aa4-125">Meilisõnumi sisu loomine HTML-i abil</span><span class="sxs-lookup"><span data-stu-id="32aa4-125">Create an email message body by using HTML</span></span>

<span data-ttu-id="32aa4-126">Teie meilisõnumi sisu koosneb HTML-ist.</span><span class="sxs-lookup"><span data-stu-id="32aa4-126">The message body of your email is composed in HTML.</span></span> <span data-ttu-id="32aa4-127">Võite kasutada mis tahes paigutust, laadi ja kaubamärki, mida HTML ja tekstisisene kaskaadlaadistik (CSS) võimaldavad.</span><span class="sxs-lookup"><span data-stu-id="32aa4-127">You can use any layout, styling, and branding that HTML and inline Cascading Style Sheets (CSS) allow for.</span></span> <span data-ttu-id="32aa4-128">Saate kasutada ka pilte, kui hostite neid avalikult kättesaadavas lõpp-punktis veebis.</span><span class="sxs-lookup"><span data-stu-id="32aa4-128">You can also use images, if you host them on a publicly available web endpoint.</span></span> <span data-ttu-id="32aa4-129">Pildi lisamiseks sisestage pildi URL sildile **src** HTML-i atribuut **&lt;img&gt;**.</span><span class="sxs-lookup"><span data-stu-id="32aa4-129">To add an image, enter the image's URL in the **src** attribute of the HTML **&lt;img&gt;** tag.</span></span>

> [!NOTE]
> <span data-ttu-id="32aa4-130">Meilikliendid kehtestavad paigutuse ja stiili piiranguid, mis võivad nõuda sõnumi sisus kasutatava HTML-i ja CSS-i korrigeerimist.</span><span class="sxs-lookup"><span data-stu-id="32aa4-130">Email clients impose layout and style limitations that might require adjustments to the HTML and CSS that you use for the message body.</span></span> <span data-ttu-id="32aa4-131">Soovitame teil tutvuda HTML-i loomise heade tavadega, mida toetavad kõige levinumad meilikliendid.</span><span class="sxs-lookup"><span data-stu-id="32aa4-131">We recommend that you familiarize yourself with the best practices for creating HTML that will be supported by the most popular email clients.</span></span>

## <a name="add-placeholders-to-the-email-message-body"></a><span data-ttu-id="32aa4-132">Meilisõnumi sisule kohatäidete lisamine</span><span class="sxs-lookup"><span data-stu-id="32aa4-132">Add placeholders to the email message body</span></span>

<span data-ttu-id="32aa4-133">Teie meil võib sisaldada kohatäiteid, mis asendatakse kliendi- ja kandepõhiste väärtustega meili loomisel.</span><span class="sxs-lookup"><span data-stu-id="32aa4-133">Your email can contain placeholders that are replaced with customer-specific and transaction-specific values when the email is generated.</span></span> <span data-ttu-id="32aa4-134">Kohatäited on alati protsendimärkide (%) vahel ja sisestatakse otse HTML-dokumenti.</span><span class="sxs-lookup"><span data-stu-id="32aa4-134">Placeholders are always surrounded by percent signs (%) and are inserted directly into the HTML document.</span></span>

<span data-ttu-id="32aa4-135">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="32aa4-135">Here is an example.</span></span>

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a><span data-ttu-id="32aa4-136">Tellimuse kohatäited (müügitellimuse tase)</span><span class="sxs-lookup"><span data-stu-id="32aa4-136">Order placeholders (sales order level)</span></span>

<span data-ttu-id="32aa4-137">Järgmised kohatäited toovad ja kuvavad müügitellimuse tasemel määratletud andmeid (vastupidiselt müügirea tasemele).</span><span class="sxs-lookup"><span data-stu-id="32aa4-137">The following placeholders retrieve and show data that is defined at the sales order level (as opposed to the sales line level).</span></span>

| <span data-ttu-id="32aa4-138">Kohatäite nimi</span><span class="sxs-lookup"><span data-stu-id="32aa4-138">Placeholder name</span></span>     | <span data-ttu-id="32aa4-139">Kohatäite väärtus</span><span class="sxs-lookup"><span data-stu-id="32aa4-139">Placeholder value</span></span>                                            |
| -------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="32aa4-140">customername</span><span class="sxs-lookup"><span data-stu-id="32aa4-140">customername</span></span>         | <span data-ttu-id="32aa4-141">Tellimuse esitanud kliendi nimi.</span><span class="sxs-lookup"><span data-stu-id="32aa4-141">The name of the customer who placed the order.</span></span>               |
| <span data-ttu-id="32aa4-142">salesid</span><span class="sxs-lookup"><span data-stu-id="32aa4-142">salesid</span></span>              | <span data-ttu-id="32aa4-143">Müügitellimuse müügi ID.</span><span class="sxs-lookup"><span data-stu-id="32aa4-143">The sales ID of the order.</span></span>                                   |
| <span data-ttu-id="32aa4-144">deliveryaddress</span><span class="sxs-lookup"><span data-stu-id="32aa4-144">deliveryaddress</span></span>      | <span data-ttu-id="32aa4-145">Saadetud tellimuste tarneaadress.</span><span class="sxs-lookup"><span data-stu-id="32aa4-145">The delivery address for shipped orders.</span></span>                     |
| <span data-ttu-id="32aa4-146">customeraddress</span><span class="sxs-lookup"><span data-stu-id="32aa4-146">customeraddress</span></span>      | <span data-ttu-id="32aa4-147">Kliendi aadress.</span><span class="sxs-lookup"><span data-stu-id="32aa4-147">The address of the customer.</span></span>                                 |
| <span data-ttu-id="32aa4-148">kliendimeiliaadress</span><span class="sxs-lookup"><span data-stu-id="32aa4-148">customeremailaddress</span></span> | <span data-ttu-id="32aa4-149">Meiliaadress, mille klient väljaregistreerimise ajal sisestas.</span><span class="sxs-lookup"><span data-stu-id="32aa4-149">The email address that the customer entered at checkout.</span></span>     |
| <span data-ttu-id="32aa4-150">deliverydate</span><span class="sxs-lookup"><span data-stu-id="32aa4-150">deliverydate</span></span>         | <span data-ttu-id="32aa4-151">Tarnekuupäev.</span><span class="sxs-lookup"><span data-stu-id="32aa4-151">The delivery date.</span></span>                                           |
| <span data-ttu-id="32aa4-152">shipdate</span><span class="sxs-lookup"><span data-stu-id="32aa4-152">shipdate</span></span>             | <span data-ttu-id="32aa4-153">Lähetuskuupäev.</span><span class="sxs-lookup"><span data-stu-id="32aa4-153">The ship date.</span></span>                                               |
| <span data-ttu-id="32aa4-154">modeofdelivery</span><span class="sxs-lookup"><span data-stu-id="32aa4-154">modeofdelivery</span></span>       | <span data-ttu-id="32aa4-155">Tellimuse tarneviis.</span><span class="sxs-lookup"><span data-stu-id="32aa4-155">The delivery mode of the order.</span></span>                              |
| <span data-ttu-id="32aa4-156">lisakulud</span><span class="sxs-lookup"><span data-stu-id="32aa4-156">charges</span></span>              | <span data-ttu-id="32aa4-157">Tellimuse kogukulud.</span><span class="sxs-lookup"><span data-stu-id="32aa4-157">The total charges for the order.</span></span>                             |
| <span data-ttu-id="32aa4-158">maks</span><span class="sxs-lookup"><span data-stu-id="32aa4-158">tax</span></span>                  | <span data-ttu-id="32aa4-159">Tellimuse maks kokku.</span><span class="sxs-lookup"><span data-stu-id="32aa4-159">The total tax for the order.</span></span>                                 |
| <span data-ttu-id="32aa4-160">kokku</span><span class="sxs-lookup"><span data-stu-id="32aa4-160">total</span></span>                | <span data-ttu-id="32aa4-161">Tellimuse kogusumma.</span><span class="sxs-lookup"><span data-stu-id="32aa4-161">The total amount for the order.</span></span>                              |
| <span data-ttu-id="32aa4-162">ordernetamount</span><span class="sxs-lookup"><span data-stu-id="32aa4-162">ordernetamount</span></span>       | <span data-ttu-id="32aa4-163">Tellimuse kogusumma miinus kogu maks.</span><span class="sxs-lookup"><span data-stu-id="32aa4-163">The total amount for the order, minus the total tax.</span></span>         |
| <span data-ttu-id="32aa4-164">allahindlus</span><span class="sxs-lookup"><span data-stu-id="32aa4-164">discount</span></span>             | <span data-ttu-id="32aa4-165">Tellimuse lõppallahindlus.</span><span class="sxs-lookup"><span data-stu-id="32aa4-165">The total discount for the order.</span></span>                            |
| <span data-ttu-id="32aa4-166">storename</span><span class="sxs-lookup"><span data-stu-id="32aa4-166">storename</span></span>            | <span data-ttu-id="32aa4-167">Poe nimi, kus tellimus esitati.</span><span class="sxs-lookup"><span data-stu-id="32aa4-167">The name of the store where the order was placed.</span></span>            |
| <span data-ttu-id="32aa4-168">storeaddress</span><span class="sxs-lookup"><span data-stu-id="32aa4-168">storeaddress</span></span>         | <span data-ttu-id="32aa4-169">Tellimuse esitanud poe aadress.</span><span class="sxs-lookup"><span data-stu-id="32aa4-169">The address of the store that placed the order.</span></span>              |
| <span data-ttu-id="32aa4-170">storeopenfrom</span><span class="sxs-lookup"><span data-stu-id="32aa4-170">storeopenfrom</span></span>        | <span data-ttu-id="32aa4-171">Tellimuse esitanud poe lahtiolekuaeg.</span><span class="sxs-lookup"><span data-stu-id="32aa4-171">The opening time of the store that placed the order.</span></span>         |
| <span data-ttu-id="32aa4-172">storeopento</span><span class="sxs-lookup"><span data-stu-id="32aa4-172">storeopento</span></span>          | <span data-ttu-id="32aa4-173">Tellimuse esitanud poe sulgemisaeg.</span><span class="sxs-lookup"><span data-stu-id="32aa4-173">The closing time of the store that placed the order.</span></span>         |
| <span data-ttu-id="32aa4-174">pickupstorename</span><span class="sxs-lookup"><span data-stu-id="32aa4-174">pickupstorename</span></span>      | <span data-ttu-id="32aa4-175">Poe nimi, kust tellimus peale võetakse.</span><span class="sxs-lookup"><span data-stu-id="32aa4-175">The name of the store where the order will be picked up.</span></span>     |
| <span data-ttu-id="32aa4-176">pickupstoreaddress</span><span class="sxs-lookup"><span data-stu-id="32aa4-176">pickupstoreaddress</span></span>   | <span data-ttu-id="32aa4-177">Poe aadress, kust tellimus peale võetakse.</span><span class="sxs-lookup"><span data-stu-id="32aa4-177">The address of the store where the order will be picked up.</span></span>  |
| <span data-ttu-id="32aa4-178">pickupopenstorefrom</span><span class="sxs-lookup"><span data-stu-id="32aa4-178">pickupopenstorefrom</span></span>  | <span data-ttu-id="32aa4-179">Poe lahtiolekuaeg, kust tellimus peale võetakse.</span><span class="sxs-lookup"><span data-stu-id="32aa4-179">The opening time of the store where the order will be picked up.</span></span> |
| <span data-ttu-id="32aa4-180">pickupopenstoreto</span><span class="sxs-lookup"><span data-stu-id="32aa4-180">pickupopenstoreto</span></span>    | <span data-ttu-id="32aa4-181">Poe sulgemisaeg, kust tellimus peale võetakse.</span><span class="sxs-lookup"><span data-stu-id="32aa4-181">The closing time of the store where the order will be picked up.</span></span> |

### <a name="order-line-placeholders-sales-line-level"></a><span data-ttu-id="32aa4-182">Tellimuserea kohatäited (müügirea tase)</span><span class="sxs-lookup"><span data-stu-id="32aa4-182">Order line placeholders (sales line level)</span></span>

<span data-ttu-id="32aa4-183">Järgmised kohatäited toovad ja kuvavad müügitellimuse üksikute toodete (ridade) andmeid.</span><span class="sxs-lookup"><span data-stu-id="32aa4-183">The following placeholders retrieve and show data for individual products (lines) in the sales order.</span></span>

| <span data-ttu-id="32aa4-184">Kohatäite nimi</span><span class="sxs-lookup"><span data-stu-id="32aa4-184">Placeholder name</span></span>               | <span data-ttu-id="32aa4-185">Kohatäite väärtus</span><span class="sxs-lookup"><span data-stu-id="32aa4-185">Placeholder value</span></span> |
|--------------------------------|-------------------|
| <span data-ttu-id="32aa4-186">productid</span><span class="sxs-lookup"><span data-stu-id="32aa4-186">productid</span></span>                      | <span data-ttu-id="32aa4-187">Selle rea toote ID.</span><span class="sxs-lookup"><span data-stu-id="32aa4-187">The product ID for the line.</span></span> |
| <span data-ttu-id="32aa4-188">lineproductname</span><span class="sxs-lookup"><span data-stu-id="32aa4-188">lineproductname</span></span>                | <span data-ttu-id="32aa4-189">Toote nimi.</span><span class="sxs-lookup"><span data-stu-id="32aa4-189">The name of the product.</span></span> |
| <span data-ttu-id="32aa4-190">lineproductdescription</span><span class="sxs-lookup"><span data-stu-id="32aa4-190">lineproductdescription</span></span>         | <span data-ttu-id="32aa4-191">Toote kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="32aa4-191">The description of the product.</span></span> |
| <span data-ttu-id="32aa4-192">linequantity</span><span class="sxs-lookup"><span data-stu-id="32aa4-192">linequantity</span></span>                   | <span data-ttu-id="32aa4-193">Sellele reale tellitud ühikute arv koos mõõtühikuga (nt **ea** või **paar**).</span><span class="sxs-lookup"><span data-stu-id="32aa4-193">The number of units that were ordered for the line, plus the unit of measure (for example, **ea**, or **pair**).</span></span> |
| <span data-ttu-id="32aa4-194">lineunit</span><span class="sxs-lookup"><span data-stu-id="32aa4-194">lineunit</span></span>                       | <span data-ttu-id="32aa4-195">Selle rea mõõtühik.</span><span class="sxs-lookup"><span data-stu-id="32aa4-195">The unit of measure for the line.</span></span> |
| <span data-ttu-id="32aa4-196">linequantity_withoutunit</span><span class="sxs-lookup"><span data-stu-id="32aa4-196">linequantity_withoutunit</span></span>       | <span data-ttu-id="32aa4-197">Sellele reale tellitud ühikute arv ilma mõõtühikuta.</span><span class="sxs-lookup"><span data-stu-id="32aa4-197">The number of units that were ordered for the line, without the unit of measure.</span></span> |
| <span data-ttu-id="32aa4-198">linequantitypicked</span><span class="sxs-lookup"><span data-stu-id="32aa4-198">linequantitypicked</span></span>             | <span data-ttu-id="32aa4-199">Sündmuse **PickOrder** kasutamisel komplekteeritud ühikute arv.</span><span class="sxs-lookup"><span data-stu-id="32aa4-199">When the **PickOrder** event is used, the number of units that were picked.</span></span> <span data-ttu-id="32aa4-200">Muul juhul **0** (null).</span><span class="sxs-lookup"><span data-stu-id="32aa4-200">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="32aa4-201">linequantitypicked_withoutunit</span><span class="sxs-lookup"><span data-stu-id="32aa4-201">linequantitypicked_withoutunit</span></span> | <span data-ttu-id="32aa4-202">Sündmuse **PickOrder** kasutamisel komplekteeritud ühikute arv ilma mõõtühikuta.</span><span class="sxs-lookup"><span data-stu-id="32aa4-202">When the **PickOrder** event is used, the number of units that were picked, without the unit of measure.</span></span> <span data-ttu-id="32aa4-203">Muul juhul **0** (null).</span><span class="sxs-lookup"><span data-stu-id="32aa4-203">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="32aa4-204">linequantitypacked</span><span class="sxs-lookup"><span data-stu-id="32aa4-204">linequantitypacked</span></span>             | <span data-ttu-id="32aa4-205">Sündmuste **PackOrder** ja **Tellimus pealevõtmiseks valmis** kasutamisel pakitud ühikute arv.</span><span class="sxs-lookup"><span data-stu-id="32aa4-205">When the **PackOrder** and **Order ready for pickup** events are used, the number of units that were packed.</span></span> <span data-ttu-id="32aa4-206">Muul juhul **0** (null).</span><span class="sxs-lookup"><span data-stu-id="32aa4-206">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="32aa4-207">linequantitypacked_withoutuom</span><span class="sxs-lookup"><span data-stu-id="32aa4-207">linequantitypacked_withoutuom</span></span>  | <span data-ttu-id="32aa4-208">Sündmuste **PackOrder** ja **Tellimus pealevõtmiseks valmis** kasutamisel pakitud ühikute arv ilma mõõtühikuta.</span><span class="sxs-lookup"><span data-stu-id="32aa4-208">When the **PackOrder** and **Order ready for pickup** events are used, the number of units that were packed, without the unit of measure.</span></span> <span data-ttu-id="32aa4-209">Muul juhul **0** (null).</span><span class="sxs-lookup"><span data-stu-id="32aa4-209">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="32aa4-210">linequantityshipped</span><span class="sxs-lookup"><span data-stu-id="32aa4-210">linequantityshipped</span></span>            | <span data-ttu-id="32aa4-211">Alati **0**, välja arvatud juhul, kui kasutatakse kindlaid järgmisel real kirjeldatud sündmusi.</span><span class="sxs-lookup"><span data-stu-id="32aa4-211">Always **0**, except when specific events are used, as described in the next row.</span></span> |
| <span data-ttu-id="32aa4-212">linequantityshipped_withoutuom</span><span class="sxs-lookup"><span data-stu-id="32aa4-212">linequantityshipped_withoutuom</span></span> | <span data-ttu-id="32aa4-213">Sündmuse **ShipOrder** kasutamisel komplekteeritud ühikute arv ilma mõõtühikuta.</span><span class="sxs-lookup"><span data-stu-id="32aa4-213">When the **ShipOrder** event is used, the number of units that were picked, without the unit of measure.</span></span> <span data-ttu-id="32aa4-214">Muul juhul **0** (null).</span><span class="sxs-lookup"><span data-stu-id="32aa4-214">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="32aa4-215">lineprice</span><span class="sxs-lookup"><span data-stu-id="32aa4-215">lineprice</span></span>                      | <span data-ttu-id="32aa4-216">Ühe üksuse hind.</span><span class="sxs-lookup"><span data-stu-id="32aa4-216">The price of a single unit.</span></span> |
| <span data-ttu-id="32aa4-217">linenetamount</span><span class="sxs-lookup"><span data-stu-id="32aa4-217">linenetamount</span></span>                  | <span data-ttu-id="32aa4-218">Rea hind pärast ühikute arvu ja allahindluse rakendamist.</span><span class="sxs-lookup"><span data-stu-id="32aa4-218">The price of the line after the number of units and discount are applied.</span></span> |
| <span data-ttu-id="32aa4-219">linediscount</span><span class="sxs-lookup"><span data-stu-id="32aa4-219">linediscount</span></span>                   | <span data-ttu-id="32aa4-220">Üksiku ühiku allahindlus.</span><span class="sxs-lookup"><span data-stu-id="32aa4-220">The discount for an individual unit.</span></span> |
| <span data-ttu-id="32aa4-221">lineshipdate</span><span class="sxs-lookup"><span data-stu-id="32aa4-221">lineshipdate</span></span>                   | <span data-ttu-id="32aa4-222">Rea lähetuskuupäev.</span><span class="sxs-lookup"><span data-stu-id="32aa4-222">The ship date for the line.</span></span> |
| <span data-ttu-id="32aa4-223">linedeliverydate</span><span class="sxs-lookup"><span data-stu-id="32aa4-223">linedeliverydate</span></span>               | <span data-ttu-id="32aa4-224">Rea tarnekuupäev.</span><span class="sxs-lookup"><span data-stu-id="32aa4-224">The delivery date for the line.</span></span> |
| <span data-ttu-id="32aa4-225">linedeliverymode</span><span class="sxs-lookup"><span data-stu-id="32aa4-225">linedeliverymode</span></span>               | <span data-ttu-id="32aa4-226">Rea tarneviis.</span><span class="sxs-lookup"><span data-stu-id="32aa4-226">The delivery mode for the line.</span></span> |
| <span data-ttu-id="32aa4-227">linedeliveryaddress</span><span class="sxs-lookup"><span data-stu-id="32aa4-227">linedeliveryaddress</span></span>            | <span data-ttu-id="32aa4-228">Rea tarneaadress.</span><span class="sxs-lookup"><span data-stu-id="32aa4-228">The delivery address for the line.</span></span> |
| <span data-ttu-id="32aa4-229">giftcardnumber</span><span class="sxs-lookup"><span data-stu-id="32aa4-229">giftcardnumber</span></span>                 | <span data-ttu-id="32aa4-230">Kinkekaardi number kinkekaardi tüübi toodete puhul.</span><span class="sxs-lookup"><span data-stu-id="32aa4-230">The gift card number, for products of the gift card type.</span></span> |
| <span data-ttu-id="32aa4-231">giftcardbalance</span><span class="sxs-lookup"><span data-stu-id="32aa4-231">giftcardbalance</span></span>                | <span data-ttu-id="32aa4-232">Kinkekaardi saldo kinkekaardi tüübi toodete puhul.</span><span class="sxs-lookup"><span data-stu-id="32aa4-232">The gift card balance, for products of the gift card type.</span></span> |
| <span data-ttu-id="32aa4-233">giftcardmessage</span><span class="sxs-lookup"><span data-stu-id="32aa4-233">giftcardmessage</span></span>                | <span data-ttu-id="32aa4-234">Kinkekaardi sõnum kinkekaardi tüübi toodete puhul.</span><span class="sxs-lookup"><span data-stu-id="32aa4-234">The gift card message, for products of the gift card type.</span></span> |
| <span data-ttu-id="32aa4-235">giftcardpin</span><span class="sxs-lookup"><span data-stu-id="32aa4-235">giftcardpin</span></span>                    | <span data-ttu-id="32aa4-236">Kinkekaardi isiklik ID-number (PIN-kood) kinkekaardi tüübi toodete puhul.</span><span class="sxs-lookup"><span data-stu-id="32aa4-236">The personal identification number (PIN) of the gift card, for products of the gift card type.</span></span> <span data-ttu-id="32aa4-237">(See kohatäide on omane välistele kinkekaartidele.)</span><span class="sxs-lookup"><span data-stu-id="32aa4-237">(This placeholder is specific to external gift cards.)</span></span> |
| <span data-ttu-id="32aa4-238">giftcardexpiration</span><span class="sxs-lookup"><span data-stu-id="32aa4-238">giftcardexpiration</span></span>             | <span data-ttu-id="32aa4-239">Kinkekaardi aegumiskuupäev kinkekaardi tüübi toodete puhul.</span><span class="sxs-lookup"><span data-stu-id="32aa4-239">The expiration date of the gift card, for products of the gift card type.</span></span> <span data-ttu-id="32aa4-240">(See kohatäide on omane välistele kinkekaartidele.)</span><span class="sxs-lookup"><span data-stu-id="32aa4-240">(This placeholder is specific to external gift cards.)</span></span> |
| <span data-ttu-id="32aa4-241">giftcardrecipientname</span><span class="sxs-lookup"><span data-stu-id="32aa4-241">giftcardrecipientname</span></span>          | <span data-ttu-id="32aa4-242">Kinkekaardi saaja nimi kinkekaardi tüübi toodete puhul.</span><span class="sxs-lookup"><span data-stu-id="32aa4-242">The name of the gift card recipient, for products of the gift card type.</span></span> |
| <span data-ttu-id="32aa4-243">giftcardbuyername</span><span class="sxs-lookup"><span data-stu-id="32aa4-243">giftcardbuyername</span></span>              | <span data-ttu-id="32aa4-244">Kinkekaardi osta nimi kinkekaardi tüübi toodete puhul.</span><span class="sxs-lookup"><span data-stu-id="32aa4-244">The name of the gift card buyer, for products of the gift card type.</span></span> |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a><span data-ttu-id="32aa4-245">Tellimuserea kohatäidete vorming meilisõnumi sisus</span><span class="sxs-lookup"><span data-stu-id="32aa4-245">Format of order line placeholders in the email message body</span></span>

<span data-ttu-id="32aa4-246">Kui loote meilisõnumi sisus üksikute tellimuseridade HTML-i, pange nende ridade HTML-i ja kohatäidete korduv üksus järgmiste kohatäidete vahele, mis pannakse HTML-kommentaari siltide sisse.</span><span class="sxs-lookup"><span data-stu-id="32aa4-246">When you create the HTML for the individual order lines in the email message body, surround the repeating block of HTML and placeholders for the lines with the following placeholders that are put inside HTML comment tags.</span></span>

```html
<!--%tablebegin.salesline%-->

(Insert the repeating block of HTML and placeholders for individual lines here.)

<!--%tableend.salesline%-->
```

<span data-ttu-id="32aa4-247">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="32aa4-247">Here is an example.</span></span>

```HTML
<table>
    <tr>
        <td>Product name</td>
        <td>Quantity</td>
        <td>Price</td>
    </tr>
    <!--%tablebegin.salesline%-->
    <tr>
        <td>%lineproductname%</td>
        <td>%linequantity_withoutunit%</td>
        <td>%lineprice%</td>
    </tr>
    <!--%tableend.salesline%-->
</table>
```

## <a name="create-a-template-for-emailed-receipts"></a><span data-ttu-id="32aa4-248">Saadetud kviitungite malli loomine</span><span class="sxs-lookup"><span data-stu-id="32aa4-248">Create a template for emailed receipts</span></span>

<span data-ttu-id="32aa4-249">Kviitungeid saab saata klientidele, kes teevad oste jaemüügikassas (POS).</span><span class="sxs-lookup"><span data-stu-id="32aa4-249">Receipts can be emailed to customers who make purchases at a retail point of sale (POS).</span></span> <span data-ttu-id="32aa4-250">Üldiselt sarnanevad meili teel saadetava kviitungi malli loomise etapid muude kandesündmuste mallide loomisega.</span><span class="sxs-lookup"><span data-stu-id="32aa4-250">In general, the steps for creating the emailed receipt template are the same as the steps for creating templates for other transactional events.</span></span> <span data-ttu-id="32aa4-251">Kuid järgmisi muudatusi on vaja teha.</span><span class="sxs-lookup"><span data-stu-id="32aa4-251">However, the following changes are required:</span></span>

- <span data-ttu-id="32aa4-252">Kviitungi tekst sisestatakse meili kohatäite **%message%** abil.</span><span class="sxs-lookup"><span data-stu-id="32aa4-252">The text of the receipt is inserted into the email by using the **%message%** placeholder.</span></span> <span data-ttu-id="32aa4-253">Tagamaks, et kviitungi sisu oleks õigesti renderdatud, lisage **%message%** kohatäide HTML-iga **&lt;pre&gt;** ja **&lt;pre&gt;** vahele.</span><span class="sxs-lookup"><span data-stu-id="32aa4-253">To ensure that the receipt body is correctly rendered, surround the **%message%** placeholder with HTML **&lt;pre&gt;** and **&lt;/pre&gt;** tags.</span></span>
- <span data-ttu-id="32aa4-254">Kohatäitjat **%receiptid%** saab kasutada QR-koodi või vöötkoodi näitamiseks, mis tähistab kviitungi ID-d.</span><span class="sxs-lookup"><span data-stu-id="32aa4-254">The **%receiptid%** placeholder can be used to show a QR code or bar code that represents the receipt ID.</span></span> <span data-ttu-id="32aa4-255">(QR-koodid ja vöötkoodid on dünaamiliselt loodud ja neid teenuseid teenuseid loonud kolmanda osapoole teenus.) Lisateavet selle kohta, kuidas kuvada QR-kood või vöötkood meiliga saadetud kviitungis, vt [Lisa QR-kood või vöötkood kande- ja kviitungi meilidele](add-qr-code-barcode-email.md).</span><span class="sxs-lookup"><span data-stu-id="32aa4-255">(QR codes and bar codes are dynamically generated and served by a third-party service.) For more information about how to show a QR code or bar code in an emailed receipt, see [Add a QR code or bar code to transactional and receipt emails](add-qr-code-barcode-email.md).</span></span>

## <a name="upload-the-email-html"></a><span data-ttu-id="32aa4-256">Meili HTML-i üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="32aa4-256">Upload the email HTML</span></span>

<span data-ttu-id="32aa4-257">Pärast meili sisu HTML-i loomist ja testimist, tuleb see üles laadida Commerce'i peakontorisse.</span><span class="sxs-lookup"><span data-stu-id="32aa4-257">After you've created and tested the HTML for your message body, it must be uploaded to Commerce headquarters.</span></span> <span data-ttu-id="32aa4-258">Praegu ei saa meili HTML-i eksportida.</span><span class="sxs-lookup"><span data-stu-id="32aa4-258">Currently, email HTML can't be exported.</span></span> <span data-ttu-id="32aa4-259">Seetõttu peate oma HTML-i põhikoopiat säilitama väljaspool Commerce'i peakontorit.</span><span class="sxs-lookup"><span data-stu-id="32aa4-259">Therefore, you must maintain the master copy of your HTML outside Commerce headquarters.</span></span>

<span data-ttu-id="32aa4-260">Uue või redigeeritud meilimalli HTML-i üleslaadimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="32aa4-260">To upload a new or edited email template HTML, follow these steps.</span></span>

1. <span data-ttu-id="32aa4-261">Avage Commerce'i peakontori jaotis **Jaemüük ja kaubandus \> Peakontori seadistamine \> Organisatsiooni meilimallid**.</span><span class="sxs-lookup"><span data-stu-id="32aa4-261">In Commerce headquarters, go to **Retail and Commerce \> Headquarters setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="32aa4-262">Valige keele rida, mille jaoks soovite HTML-i lisada või asendada.</span><span class="sxs-lookup"><span data-stu-id="32aa4-262">Select the row for the language that you want to add or replace HTML for.</span></span> <span data-ttu-id="32aa4-263">Teiseks võimaluseks on valida suvand **Uus** uue keele jaoks rea loomiseks.</span><span class="sxs-lookup"><span data-stu-id="32aa4-263">Alternatively, select **New** to create a row for a new language.</span></span>
1. <span data-ttu-id="32aa4-264">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="32aa4-264">Select **Edit**.</span></span>
1. <span data-ttu-id="32aa4-265">Kuvatavas dialoogiboksis tehke valik **Sirvi**.</span><span class="sxs-lookup"><span data-stu-id="32aa4-265">In the dialog box that appears, select **Browse**.</span></span> <span data-ttu-id="32aa4-266">Sirvige HTML-dokumendini, mida soovite üles laadida, valige see ja seejärel valige **Ava**.</span><span class="sxs-lookup"><span data-stu-id="32aa4-266">Browse to the HTML document that you want to upload, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="32aa4-267">Valige nupp **Laadi üles**.</span><span class="sxs-lookup"><span data-stu-id="32aa4-267">Select **Upload**.</span></span>
1. <span data-ttu-id="32aa4-268">Pärast meili HTML-i kuvamist eelvaate aknas valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="32aa4-268">After your email HTML appears in the preview window, select **OK**.</span></span>
1. <span data-ttu-id="32aa4-269">Kontrollige, et real on ruut **On sisu** märgitud.</span><span class="sxs-lookup"><span data-stu-id="32aa4-269">Make sure that the **Has body** check box is selected for the row.</span></span>

<span data-ttu-id="32aa4-270">Kui olete Commerce'i peakontori juba meili saatmiseks konfigureerinud, saadetakse teie uus või värskendatud meil kõigile klientidele, kes sooritavad kande, mis käivitab mallile vastendatud sündmuse.</span><span class="sxs-lookup"><span data-stu-id="32aa4-270">If you've already configured Commerce headquarters to send email, your new or updated email will be sent to all customers who perform a transaction that invokes the event that is mapped to the template.</span></span>

<span data-ttu-id="32aa4-271">Lisateavet Dynamics 365 Commerce'is meilide konfigureerimise kohta vt teemast [Meili konfigureerimine ja saatmine](../fin-ops-core/fin-ops/organization-administration/configure-email.md).</span><span class="sxs-lookup"><span data-stu-id="32aa4-271">For more information about how to configure emails in Dynamics 365 Commerce, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="32aa4-272">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="32aa4-272">Additional resources</span></span> 

[<span data-ttu-id="32aa4-273">Meiliteatise profiili seadistamine</span><span class="sxs-lookup"><span data-stu-id="32aa4-273">Set up an email notification profile</span></span>](email-notification-profiles.md)

[<span data-ttu-id="32aa4-274">Meilisõnumi konfigureerimine ja saatmine</span><span class="sxs-lookup"><span data-stu-id="32aa4-274">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[<span data-ttu-id="32aa4-275">Seadistage meilisissetulekud</span><span class="sxs-lookup"><span data-stu-id="32aa4-275">Set up email receipts</span></span>](/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[<span data-ttu-id="32aa4-276">Meilikviitungite saatmine kaasaegsest kassast </span><span class="sxs-lookup"><span data-stu-id="32aa4-276">Send email receipts from Modern POS </span></span>](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]