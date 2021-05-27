---
title: Kinnipeetava maksu aruandluskoodide häälestamine TDS-i maksutüübi jaoks
description: See teema kirjeldab, kuidas seadistada kinnipeetava maksu komponente rühmad, näiteks rent ja töövõtja, maksukohustuslasest mahaarvatud maksu (TDS) jaoks.
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
ms.openlocfilehash: 23124d36389b08726defbedbd1bab9a7eb43c197
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023189"
---
# <a name="set-up-withholding-tax-component-groups-for-the-tds-tax-type"></a><span data-ttu-id="178d8-103">Kinnipeetava maksu aruandluskoodide häälestamine TDS-i maksutüübi jaoks</span><span class="sxs-lookup"><span data-stu-id="178d8-103">Set up withholding tax component groups for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="178d8-104">See teema kirjeldab, kuidas seadistada kinnipeetava maksu komponente rühmad nagu näiteks **Rent** ja **Töövõtja**, maksukohustuslasest mahaarvatud maksu (TDS) jaoks.</span><span class="sxs-lookup"><span data-stu-id="178d8-104">This topic explains how to set up withholding tax component groups, such as **Rent** and **Contractor**, for the Tax Deducted at Source (TDS) tax type.</span></span>

1. <span data-ttu-id="178d8-105">Minge **Maks \> Seadistus \> Kinnipeetav maks \> Kinnipeetava maksu komponendid**.</span><span class="sxs-lookup"><span data-stu-id="178d8-105">Go to **Tax \> Setup \> Withholding tax \> Withholding tax component groups**.</span></span>

    <span data-ttu-id="178d8-106">[![Kinnipeetava maksu komponentide gruppide leht](./media/apac-ind-TDS-8.png)](./media/apac-ind-TDS-8.png)</span><span class="sxs-lookup"><span data-stu-id="178d8-106">[![Withholding tax component groups page](./media/apac-ind-TDS-8.png)](./media/apac-ind-TDS-8.png)</span></span>

2. <span data-ttu-id="178d8-107">Väljal **Maksu tüübi** valige **TDS** kinnipeetava maksu komponentide gruppide häälestamiseks TDS maksutüüpide jaoks.</span><span class="sxs-lookup"><span data-stu-id="178d8-107">In the **Tax type** field, select **TDS** to set up withholding tax component groups for the TDS tax type.</span></span>
3. <span data-ttu-id="178d8-108">Rea loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="178d8-108">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="178d8-109">Sisestage **Kinnipeetava maksu komponentide grupp** väljale TDS-i komponentide grupi nimi.</span><span class="sxs-lookup"><span data-stu-id="178d8-109">In the **Withholding tax component group** field, enter a name for the TDS component group.</span></span>
5. <span data-ttu-id="178d8-110">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="178d8-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="178d8-111">Valige **Üldine** kiirkaardil **Olek** väljal TDS-i komponendigrupi rühma olek.</span><span class="sxs-lookup"><span data-stu-id="178d8-111">On the **General** FastTab, in the **Status** field, select the residential status of the TDS component group.</span></span> <span data-ttu-id="178d8-112">Valikud on **Resident** ja **Mitteresident**.</span><span class="sxs-lookup"><span data-stu-id="178d8-112">The options are **Resident** and **Non-resident**.</span></span>
7. <span data-ttu-id="178d8-113">Sisestage **Jaotise koodi** väljale sektsiooni kood, mida rakendatakse TDS-i komponendigrupile.</span><span class="sxs-lookup"><span data-stu-id="178d8-113">In the **Section code** field, enter the section code that is applied to the TDS component group.</span></span>
8. <span data-ttu-id="178d8-114">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="178d8-114">Close the page.</span></span>
