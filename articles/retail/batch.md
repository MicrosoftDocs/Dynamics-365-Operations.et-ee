---
title: Partii jälgimisega kaupade täiustatud käsitlemine
description: Selles teemas kirjeldatakse täiustusi, mis on tehtud jaemüügiväljavõtete sisestamisprotsessi käigus partii jälgimisega kaupade partiide käsitlemisele.
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 5bbddf649f66ded9588cdb1e3f43c75630dc248a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770159"
---
# <a name="improved-handling-of-batch-tracked-items"></a><span data-ttu-id="39786-103">Partii jälgimisega kaupade täiustatud käsitlemine</span><span class="sxs-lookup"><span data-stu-id="39786-103">Improved handling of batch-tracked items</span></span>


[!include [banner](includes/banner.md)]


<span data-ttu-id="39786-104">Jaemüügikassas (POS) ei saa partiinumbreid partii jälgimisega kaupade puhul müügi hetkel jäädvustada.</span><span class="sxs-lookup"><span data-stu-id="39786-104">In Retail Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</span></span> <span data-ttu-id="39786-105">Kui müügiandmed sisestatakse peakontoris klienditellimuste või väljavõtete sisestuse käigus, siis eeldab süsteem Microsoft Dynamics teatud konfiguratsioonide korral, et partii jälgimisega kaupade jaoks on olemas sobivad partiinumbrid ja neid kasutatakse arveldusprotsessis.</span><span class="sxs-lookup"><span data-stu-id="39786-105">However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</span></span>

<span data-ttu-id="39786-106">Kui toodete jaoks on saadaval sobivad partiinumbrid, kasutavad väljavõtete sisestamise käigus toimuv klienditellimuste arveldamise protsess ja müügitellimuste arveldamise protsess neid partiinumbreid.</span><span class="sxs-lookup"><span data-stu-id="39786-106">If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</span></span> <span data-ttu-id="39786-107">Vastasel korral ei saa klienditellimuste arveldamise protsess andmeid sisestada ja kassa kasutaja saab tõrketeate.</span><span class="sxs-lookup"><span data-stu-id="39786-107">Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</span></span> <span data-ttu-id="39786-108">Väljavõtete sisestus läheb siis tõrkeolekusse.</span><span class="sxs-lookup"><span data-stu-id="39786-108">Statement posting then goes into an error state.</span></span> <span data-ttu-id="39786-109">See tõrkeolek ilmneb ka siis, kui negatiivsed varud on toodete jaoks sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="39786-109">This error state occurs even when negative inventory has been turned on for the products.</span></span>

<span data-ttu-id="39786-110">Retaili versioonis 10.0.4 ja uuemates tehtud täiustused aitavad tagada, et kui partii jälgimisega kaupade jaoks on sisse lülitatud negatiivsed varud, ei blokeerita nende kaupade puhul väljavõtete sisestuse kaudu toimuvat klienditellimuste arveldust ega müügitellimuste arveldust, kui varude väärtus on 0 (null) või partiinumber pole saadaval.</span><span class="sxs-lookup"><span data-stu-id="39786-110">Improvements that have been made in Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</span></span> <span data-ttu-id="39786-111">Kui partiinumbrid pole saadaval, kasutab see uus funktsioon müügiridade jaoks partii vaike-ID-d.</span><span class="sxs-lookup"><span data-stu-id="39786-111">The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</span></span>

<span data-ttu-id="39786-112">Klienditellimuste jaoks kasutatava partii vaike-ID määratlemiseks määrake lehe **Jaemüügi parameetrid** vahekaardi **Kliendi tellimused** kiirkaardil **Tellimus** väli **Vaikimisi partii ID**.</span><span class="sxs-lookup"><span data-stu-id="39786-112">To define the default batch ID that is used for customer orders, on the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, set the **Default batch id** field.</span></span>

<span data-ttu-id="39786-113">Väljavõtete sisestamise kaudu tehtava müügitellimuste arvelduse jaoks kasutatava partii vaike-ID määratlemiseks määrake lehe **Jaemüügi parameetrid** vahekaardi **Sisestamine** kiirkaardil **Laoseisu uuendamine** väli **Vaikimisi partii ID**.</span><span class="sxs-lookup"><span data-stu-id="39786-113">To define the default batch ID that is used for sales order invoicing through statement posting, on the **Retail parameters** page, on the **Posting** tab, on the **Inventory update** FastTab, set the **Default batch id** field.</span></span>

> [!NOTE]
> <span data-ttu-id="39786-114">See funktsioon on saadaval ainult juhul, kui konkreetse kaupluse lao ja kaupade jaoks on sisse lülitatud täpsem laohaldus.</span><span class="sxs-lookup"><span data-stu-id="39786-114">This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</span></span> <span data-ttu-id="39786-115">Uuemas versioonis toetatakse funktsiooni ka selliste stsenaariumite puhul, kus täpsemat laohaldust ei kasutata.</span><span class="sxs-lookup"><span data-stu-id="39786-115">In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</span></span>

> [!NOTE]
> <span data-ttu-id="39786-116">Retaili versioonis 10.0.5 on täpsemat laohaldust mittekasutatavates stsenaariumites kasutusele võetud partii jälgimisega kaupade täiustatud käsitlemine väljavõtte sisestamise ajal.</span><span class="sxs-lookup"><span data-stu-id="39786-116">Support for improved handling of batch-tracked items during statement posting for non-advanced warehouse management scenarios was introduced in Retail version 10.0.5.</span></span>
