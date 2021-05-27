---
title: Kinnipeetava maksu aruandluskoodide häälestamine TDS-i maksutüübi jaoks
description: Kinnipeetava maksu aruandluskoode kasutatakse vormi 26Q ja vormi 27Q väljavõtete loomiseks allikas mahaarvatud maksude jaoks (TDS). Käesolev teema kirjeldab, kuidas seadistada kinnipeetava maksu aruandluskoodide samme nii, et saate seadistada TDS-i aruandluskoode.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1f9325d182f89b98e8b943ae047c55e7e1aeb02f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023188"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a><span data-ttu-id="79f07-104">Kinnipeetava maksu aruandluskoodide häälestamine TDS-i maksutüübi jaoks</span><span class="sxs-lookup"><span data-stu-id="79f07-104">Set up withholding tax reporting codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79f07-105">Kinnipeetava maksu aruandluskoode kasutatakse vormi 26Q ja vormi 27Q väljavõtete loomiseks allikas mahaarvatud maksude jaoks (TDS).</span><span class="sxs-lookup"><span data-stu-id="79f07-105">Withholding tax reporting codes are used to generate Form 26Q and Form 27Q statements for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="79f07-106">Käesolev teema kirjeldab, kuidas seadistada kinnipeetava maksu aruandluskoodide samme nii, et saate seadistada TDS-i aruandluskoode.</span><span class="sxs-lookup"><span data-stu-id="79f07-106">This topic explains how to set up withholding tax reporting codes steps so that you can set up TDS reporting codes.</span></span>

1. <span data-ttu-id="79f07-107">Minge **Maks \> Seadistus \> Kinnipeetav maks \> Kinnipeetava maksu aruandluskoodid**.</span><span class="sxs-lookup"><span data-stu-id="79f07-107">Go to **Tax \> Setup \> Withholding tax \> Withholding tax reporting codes**.</span></span>

    <span data-ttu-id="79f07-108">[![Kinnipeetava maksu aruandluskoodide leht](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span><span class="sxs-lookup"><span data-stu-id="79f07-108">[![Withholding tax reporting codes page](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span></span>

2. <span data-ttu-id="79f07-109">Väljal **Maksu tüüp** valige **TDS** kinnipeetava maksu aruandluskoodide TDS maksutüübi häälestamiseks.</span><span class="sxs-lookup"><span data-stu-id="79f07-109">In the **Tax type** field, select **TDS** to define withholding tax reporting codes for the TDS tax type.</span></span>
3. <span data-ttu-id="79f07-110">Väljal **Kinnipeetava maksu komponent** valige TDS-i komponent, mille jaoks te kinnipeetava maksu aruandluskoodi määratlete.</span><span class="sxs-lookup"><span data-stu-id="79f07-110">In the **Withholding tax component** field, select the TDS component to that you're defining the withholding tax reporting code for.</span></span> <span data-ttu-id="79f07-111">Väljal **Kinnipeetava maksu komponendigrupp** kuvatakse TDS-i komponendi grupp, mis määratleti teie määratleva TDS-i komponendi jaoks.</span><span class="sxs-lookup"><span data-stu-id="79f07-111">The **Withholding tax component group** field shows the TDS component group that was defined for the TDS component that you're defining.</span></span>

    <span data-ttu-id="79f07-112">Väljal **sektsioonikood** kiirkaardil **Üldine** näitab sektsiooni koodi, mis on seotud TDS-i komponendigrupiga.</span><span class="sxs-lookup"><span data-stu-id="79f07-112">The **Section code** field on the **General** FastTab shows the section code that is attached to the TDS component group.</span></span>

4. <span data-ttu-id="79f07-113">Valige kiirkaardil **Üldine**, väljal **Aruandluskood** sobiv TDS aruandlus kood:</span><span class="sxs-lookup"><span data-stu-id="79f07-113">On the **General** FastTab, in the **Reporting code** field, select the TDS reporting code:</span></span>

    - <span data-ttu-id="79f07-114">TDS</span><span class="sxs-lookup"><span data-stu-id="79f07-114">TDS</span></span>
    - <span data-ttu-id="79f07-115">TCS</span><span class="sxs-lookup"><span data-stu-id="79f07-115">TCS</span></span>
    - <span data-ttu-id="79f07-116">Lisatasu</span><span class="sxs-lookup"><span data-stu-id="79f07-116">Surcharge</span></span>
    - <span data-ttu-id="79f07-117">PE\_Cess</span><span class="sxs-lookup"><span data-stu-id="79f07-117">PE\_Cess</span></span>
    - <span data-ttu-id="79f07-118">SHE\_Cess</span><span class="sxs-lookup"><span data-stu-id="79f07-118">SHE\_Cess</span></span>

5. <span data-ttu-id="79f07-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="79f07-119">Close the page.</span></span>
