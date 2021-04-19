---
title: QR-koodi või vöötkoodi lisamine kande- ja kviitungi meilidele
description: See teema selgitab, kuidas sisestada Microsoft Dynamics 365 Commerce kande- ja sissetulekumeilidesse QR-koodid ja vöötkoodid, mis tähistavad tellimuse ID-sid.
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: f8d9408090846799c1bb421c4b6e5e248d37fa07
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797499"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a><span data-ttu-id="c8537-103">QR-koodi või vöötkoodi lisamine kande- ja kviitungi meilidele</span><span class="sxs-lookup"><span data-stu-id="c8537-103">Add a QR code or bar code to transactional and receipt emails</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="c8537-104">See teema selgitab, kuidas sisestada Microsoft Dynamics 365 Commerce kande- ja sissetulekumeilidesse QR-koodid ja vöötkoodid, mis tähistavad tellimuse ID-sid.</span><span class="sxs-lookup"><span data-stu-id="c8537-104">This topic explains how to insert QR codes and bar codes that represent order IDs into transactional and receipt emails in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c8537-105">Saate lihtsalt lisada QR-koodid ja vöötkoodid kande e-kirja, et aidata jaemüügikeskkonnas tellimuse otsinguprotsessi kiirendada.</span><span class="sxs-lookup"><span data-stu-id="c8537-105">You can easily include QR codes and bar codes in transactional emails to help speed up the order lookup process in a retail environment.</span></span> <span data-ttu-id="c8537-106">QR-koodide ja vöötkoodide sisestamiseks e-kirja, kasutage HTML **\<img\>** silti, mis taotleb QR-koodi või vöötkoodi pilti loomisest ja renderdamisteenusest.</span><span class="sxs-lookup"><span data-stu-id="c8537-106">To insert QR codes and bar codes into emails, you use an HTML **\<img\>** tag that requests a QR code or bar code image from a generation and rendering service.</span></span> <span data-ttu-id="c8537-107">Microsoft ei paku seda teenust.</span><span class="sxs-lookup"><span data-stu-id="c8537-107">Microsoft doesn't provide this service.</span></span> <span data-ttu-id="c8537-108">Siiski on palju tasuta või kalleid teenuseid, mis võivad teenindada QR-koode või vöötkoode, mis luuakse dünaamiliselt päringustringis edastatud väärtuse põhjal.</span><span class="sxs-lookup"><span data-stu-id="c8537-108">However, there are many free or inexpensive services that can serve QR codes or bar codes that are dynamically generated based on a value that is passed in a query string.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a><span data-ttu-id="c8537-109">QR-koodi või vöötkoodi lisamine kande- ja kviitungi meilidele</span><span class="sxs-lookup"><span data-stu-id="c8537-109">Add a QR code or bar code to a transactional email</span></span>

<span data-ttu-id="c8537-110">E-kaubanduse ostu osana saadetud kande e-kirjale QR-koodi või vöötkoodi sisestamiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="c8537-110">To insert a QR code or bar code into a transactional email that is sent as part of an e-commerce purchase, follow these steps.</span></span>

1. <span data-ttu-id="c8537-111">Avage kande e-kirja malli lähte-HTML ja lisage HTML-silt, mis osutab teie **\<img\>** QR-koodile või vöötkoodi teenusele.</span><span class="sxs-lookup"><span data-stu-id="c8537-111">Open the source HTML for the transactional email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="c8537-112">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="c8537-112">Here is an example.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    <span data-ttu-id="c8537-113">Siin on võimalike olekute selgitus:</span><span class="sxs-lookup"><span data-stu-id="c8537-113">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="c8537-114">**TEIE\_QR\_KOODI\_VÖÖT\_KOODI\_TEENUS** esindab teie QR-koodi või vöötkoodi teenuse domeeni.</span><span class="sxs-lookup"><span data-stu-id="c8537-114">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="c8537-115">**Andmed** tähistab parameetrit, mida QR-kood või vöötkoodi teenus kasutab, et vastu võtta sisu, mida tuleks renderdada QR-koodina või vöötkoodina.</span><span class="sxs-lookup"><span data-stu-id="c8537-115">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="c8537-116">Sellele **%salesid%** parameetrile peab olema määratud väärtus.</span><span class="sxs-lookup"><span data-stu-id="c8537-116">The value **%salesid%** must be assigned to this parameter.</span></span> <span data-ttu-id="c8537-117">Selles näites pange tähele, et väärtust kasutatakse ka pildi asetekstna.</span><span class="sxs-lookup"><span data-stu-id="c8537-117">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="c8537-118">**parameeter 1** ja **parameeter 2** esindavad täiendavaid valikulisi parameetreid.</span><span class="sxs-lookup"><span data-stu-id="c8537-118">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="c8537-119">Minge rakenduse **Retail ja Commerce  \> Headquarters häälestamise \> parameetrite \> organisatsiooni meilimallidesse** ja laadige värskendatud HTML ülessobivale kande meilimallile.</span><span class="sxs-lookup"><span data-stu-id="c8537-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the appropriate transactional email template.</span></span>

> [!NOTE]
> <span data-ttu-id="c8537-120">Parameetrid võivad QR-koodi ja vöötkoodi teenuse pakkujate vahel erineda.</span><span class="sxs-lookup"><span data-stu-id="c8537-120">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="c8537-121">Seetõttu võtke ühendust oma teenusepakkujaga, et kinnitada parameetrid, mille juurde peate väärtused määrama.</span><span class="sxs-lookup"><span data-stu-id="c8537-121">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a><span data-ttu-id="c8537-122">QR-koodi või vöötkoodi lisamine kande- ja kviitungi meilidele</span><span class="sxs-lookup"><span data-stu-id="c8537-122">Add a QR code or bar code to a receipt email</span></span> 

<span data-ttu-id="c8537-123">QR-koodi või vöötkoodi sisestamiseks kviitungi e-kirja, mille saab saata pärast seda, kui ost on tehtud müügikohas (POS), järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="c8537-123">To insert a QR code or bar code into a receipt email that can be sent after a purchase is made at the point of sale (POS), follow these steps.</span></span>

1. <span data-ttu-id="c8537-124">Avage kande e-kirja malli lähte-HTML ja lisage HTML-silt, mis osutab teie **\<img\>** QR-koodile või vöötkoodi teenusele.</span><span class="sxs-lookup"><span data-stu-id="c8537-124">Open the source HTML for the receipt email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="c8537-125">Siin on näide allpool.</span><span class="sxs-lookup"><span data-stu-id="c8537-125">Here is an example below.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    <span data-ttu-id="c8537-126">Siin on võimalike olekute selgitus:</span><span class="sxs-lookup"><span data-stu-id="c8537-126">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="c8537-127">**TEIE\_QR\_KOODI\_VÖÖT\_KOODI\_TEENUS** esindab teie QR-koodi või vöötkoodi teenuse domeeni.</span><span class="sxs-lookup"><span data-stu-id="c8537-127">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="c8537-128">**Andmed** tähistab parameetrit, mida QR-kood või vöötkoodi teenus kasutab, et vastu võtta sisu, mida tuleks renderdada QR-koodina või vöötkoodina.</span><span class="sxs-lookup"><span data-stu-id="c8537-128">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="c8537-129">Sellele **%receiptid%** parameetrile peab olema määratud väärtus.</span><span class="sxs-lookup"><span data-stu-id="c8537-129">The value **%receiptid%** must be assigned to this parameter.</span></span> <span data-ttu-id="c8537-130">Selles näites pange tähele, et väärtust kasutatakse ka pildi asetekstna.</span><span class="sxs-lookup"><span data-stu-id="c8537-130">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="c8537-131">**parameeter 1** ja **parameeter 2** esindavad täiendavaid valikulisi parameetreid.</span><span class="sxs-lookup"><span data-stu-id="c8537-131">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="c8537-132">Minge rakenduse **Retail ja Commerce \> Headquarters häälestamise \> parameetrite \> organisatsiooni meilimallidesse** ja laadige värskendatud HTML üles sobivale kande meilimallile **emailivastuvõtja**.</span><span class="sxs-lookup"><span data-stu-id="c8537-132">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the email template that has the email ID **emailrecpt**.</span></span>

> [!NOTE]
> <span data-ttu-id="c8537-133">Parameetrid võivad QR-koodi ja vöötkoodi teenuse pakkujate vahel erineda.</span><span class="sxs-lookup"><span data-stu-id="c8537-133">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="c8537-134">Seetõttu võtke ühendust oma teenusepakkujaga, et kinnitada parameetrid, mille juurde peate väärtused määrama.</span><span class="sxs-lookup"><span data-stu-id="c8537-134">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c8537-135">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c8537-135">Additional resources</span></span>

[<span data-ttu-id="c8537-136">Meilikviitungite saatmine rakendsusest Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="c8537-136">Send email receipts from Modern POS (MPOS)</span></span>](email-receipts.md)

[<span data-ttu-id="c8537-137">Meilimallide loomine kandesündmuste jaoks</span><span class="sxs-lookup"><span data-stu-id="c8537-137">Create email templates for transactional events</span></span>](email-templates-transactions.md)
