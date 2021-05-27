---
title: Kinnipeetava maksu tasakaalustusperioodide häälestamine TDS-i maksutüübi jaoks
description: See teema kirjeldab, kuidas seadistada maksegraafikuid allika (TDS) eraldamisel mahaarvatud maksuga.
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
ms.openlocfilehash: 9430bc1386f127d02b598d6cad1b53f66e0cf2ba
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023165"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a><span data-ttu-id="1e7e9-103">Kinnipeetava maksu tasakaalustusperioodide häälestamine TDS-i maksutüübi jaoks</span><span class="sxs-lookup"><span data-stu-id="1e7e9-103">Set up withholding tax settlement periods for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e7e9-104">See teema kirjeldab, kuidas seadistada maksegraafikuid allika (TDS) eraldamisel mahaarvatud maksuga.</span><span class="sxs-lookup"><span data-stu-id="1e7e9-104">This topic explains how to set up settlement periods for Tax Deducted at Source (TDS) settlement periods.</span></span>

1. <span data-ttu-id="1e7e9-105">Avage **Maks \> Kaudsed maksud \> Kinnipeetav maks \> Kinnipeetava maksu tasakaalustusperioodid**.</span><span class="sxs-lookup"><span data-stu-id="1e7e9-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="1e7e9-106">[![Kinnipeetava maksu tasakaalustusperioodide leht](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span><span class="sxs-lookup"><span data-stu-id="1e7e9-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span></span>

2. <span data-ttu-id="1e7e9-107">Väljal **Maksu tüüpi** valige **TDS** kinnipeetava maksu komponentide gruppide häälestamiseks TDS maksutüüpide jaoks.</span><span class="sxs-lookup"><span data-stu-id="1e7e9-107">In the **Tax type** field, select **TDS** to set up withholding tax settlement periods for the TDS tax type.</span></span>
3. <span data-ttu-id="1e7e9-108">Valige uue rea loomiseks suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1e7e9-108">Select **New** to create a line.</span></span>
4. <span data-ttu-id="1e7e9-109">Väljale **Tasakaalustusperioodi** sisestage TDS-i tasakaalustusperioodi nimi.</span><span class="sxs-lookup"><span data-stu-id="1e7e9-109">In the **Settlement period** field, enter a name for the TDS settlement period.</span></span>
5. <span data-ttu-id="1e7e9-110">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="1e7e9-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="1e7e9-111">Väljal **Kinnipeetava maksu haldur** valige TDS-i haldur, kelle jaoks te TDS-i tasakaalustusperioodi määratlete.</span><span class="sxs-lookup"><span data-stu-id="1e7e9-111">In the **Withholding tax authority** field, select the TDS authority that you're defining the TDS settlement period for.</span></span>
7. <span data-ttu-id="1e7e9-112">Valige **Üldine** kiirkaardil **Perioodi intervall** väljal valige TDS-i tasakaalustusperioodi perioodiintervalli tüüp.</span><span class="sxs-lookup"><span data-stu-id="1e7e9-112">On the **General** FastTab, in the **Period interval** field, select the type of period interval for the TDS settlement period.</span></span>
8. <span data-ttu-id="1e7e9-113">Määrake **Ühikute arv** väljal ühikute arv perioodiintervalli tüübi lehel.</span><span class="sxs-lookup"><span data-stu-id="1e7e9-113">In the **Number of units** field, specify the number of units for the period interval type.</span></span>
9. <span data-ttu-id="1e7e9-114">Kiirkaardil **Perioodid** väljal **Kuupäevast** valige TDS-i tasakaalustusperioodi alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="1e7e9-114">On the **Periods** FastTab, in the **From date** field, select the start date for the TDS settlement period.</span></span> <span data-ttu-id="1e7e9-115">Väljale **Kuupäevani** sisestage lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="1e7e9-115">In the **To date** field, select the end date.</span></span>
10. <span data-ttu-id="1e7e9-116">Järgneva TDS-i tasakaalustusperioodi loomiseks olemasolevale perioodile perioodiintervalli ja perioodiühikute alusel valige väärtus **Uus periood**.</span><span class="sxs-lookup"><span data-stu-id="1e7e9-116">To create a subsequent TDS settlement period for an existing period, based on the period interval and period units, select **New period**.</span></span>
11. <span data-ttu-id="1e7e9-117">Kindla tasakaalustusperioodi jooksul käitatud perioodilise TDS-i tasakaalustuse üksikasjade vaatamiseks valige **Kinnipeetava maksu maksed** et avada **Kinnipeetava maksu makse** leht.</span><span class="sxs-lookup"><span data-stu-id="1e7e9-117">To view the details of the periodic TDS settlement that is run for a specific settlement period, select **Withholding tax payments** to open the **Withholding tax payment** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1e7e9-118">Perioodilise TDS-i tasakaalustusprotsessi käivitamiseks minge **Pearaamat \> Perioodiline \> Kinnipeetav maks \> Kinnipeetava maksu makse**.</span><span class="sxs-lookup"><span data-stu-id="1e7e9-118">To run the periodic TDS settlement process, go to **General ledger \> Periodic \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="1e7e9-119">[![Kinnipeetava maksu makse leht](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span><span class="sxs-lookup"><span data-stu-id="1e7e9-119">[![Withholding tax payment page](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span></span>

12. <span data-ttu-id="1e7e9-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1e7e9-120">Close the page.</span></span>
