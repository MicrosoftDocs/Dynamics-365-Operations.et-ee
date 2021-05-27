---
title: Kinnipeetava maksu koodide häälestamine TDS-i maksutüübi jaoks
description: See teema kirjeldab, kuidas tasakaalustada allikas (TDS) mahaarvatud perioodilist maksu.
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
ms.openlocfilehash: d56a23f7af7633e1761a8a7c48f71381d6f14df2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023190"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a><span data-ttu-id="7be3e-103">Kinnipeetava maksu koodide häälestamine TDS-i maksutüübi jaoks</span><span class="sxs-lookup"><span data-stu-id="7be3e-103">Set up withholding tax codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7be3e-104">See teema kirjeldab, kuidas tasakaalustada allikas (TDS) mahaarvatud perioodilist maksu.</span><span class="sxs-lookup"><span data-stu-id="7be3e-104">This topic explains how to set up tax codes for Tax Deducted at Source (TDS).</span></span>

1. <span data-ttu-id="7be3e-105">Avage **Maks \> Kaudsed maksud \> Kinnipeetav maks \> Kinnipeetava maksu koodid**.</span><span class="sxs-lookup"><span data-stu-id="7be3e-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax codes**.</span></span>

    <span data-ttu-id="7be3e-106">[![Kinnipeetava maksu koodide leht](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span><span class="sxs-lookup"><span data-stu-id="7be3e-106">[![Withholding tax codes page](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span></span>

2. <span data-ttu-id="7be3e-107">Tegevuspaanil valige **Uus** TDS-ile kinnipeetava maksu grupi loomiseks ja sisestage nõutavad üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="7be3e-107">On the Action Pane, select **New** to create a withholding tax code for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="7be3e-108">Väljal **Üldine** kiirkaardil **Maksu tüüp** valige **TDS** maksukood, et maksukoodi liigitada.</span><span class="sxs-lookup"><span data-stu-id="7be3e-108">On the **General** FastTab, in the **Tax type** field, select **TDS** to categorize the tax code as a TDS tax code.</span></span>
4. <span data-ttu-id="7be3e-109">Väljal **Tasakaalustusperiood** valige TDS-i tasakaalustusperiood, mille tasakaalustusprotsessi käivitada.</span><span class="sxs-lookup"><span data-stu-id="7be3e-109">In the **Settlement period** field, select the TDS settlement period for the TDS tax code.</span></span>
5. <span data-ttu-id="7be3e-110">Väljal **Põhikonto** valige pearaamatukonto, mille kohta tuleb TDS-summa sisestada.</span><span class="sxs-lookup"><span data-stu-id="7be3e-110">In the **Main account** field, select the ledger account that the TDS amount should be posted to.</span></span>
6. <span data-ttu-id="7be3e-111">Väljal **Müügireskontro** valige müügireskontro konto, mille kohta tuleb sisestadamüügikannetes mahaarvatud TDS-summa.</span><span class="sxs-lookup"><span data-stu-id="7be3e-111">In the **Receivable account** field, select the receivable account that the TDS amount that is deducted in sales transactions should be posted to.</span></span>

    <span data-ttu-id="7be3e-112">Välja **Päritolu** väärtuseks seatakse automaatselt **Protsent brutosummast** ja seda väärtust ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="7be3e-112">The **Origin** field is automatically set to **Percentage of gross amount**, and the value can't be changed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7be3e-113">Te ei saa määrata päritolu väärtusele **Protsent netosummast** maksukoodide puhul, mille maksutüüp on TDS.</span><span class="sxs-lookup"><span data-stu-id="7be3e-113">You can't set the origin to **Percentage of net amount** for tax codes of the TDS tax type.</span></span>

7. <span data-ttu-id="7be3e-114">Väljal **Kinnipeetava maksu komponent** valige TDS maksu komponent TDS-i maksukoodiks.</span><span class="sxs-lookup"><span data-stu-id="7be3e-114">In the **Withholding tax component** field, select the TDS tax component for the TDS tax code.</span></span>
8. <span data-ttu-id="7be3e-115">Tegevuspaanil valige **Väärtused** et avada **Vahekaartide kujundamine** leht.</span><span class="sxs-lookup"><span data-stu-id="7be3e-115">On the Action Pane, select **Values** to open the **Withholding tax values** page.</span></span>
9. <span data-ttu-id="7be3e-116">Valige arvutuse jaoks alguskuupäev väljal **Kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="7be3e-116">In the **From date** field, enter the start date for the TDS value.</span></span> <span data-ttu-id="7be3e-117">Väljale **Kuupäevani** sisestage lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="7be3e-117">In the **To date** field, enter the end date.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7be3e-118">Väljad **Alampiir**, **Ülempiir**, ja **Välista %** on TDS-maksutüübiga maksukoodide puhul saadaval.</span><span class="sxs-lookup"><span data-stu-id="7be3e-118">The **Minimum limit**, **Upper limit**, and **Exclude %** fields aren't available for tax codes of the TDS tax type.</span></span>

10. <span data-ttu-id="7be3e-119">Sisestage **Väärtus** väljale TDS protsent TDS maksu koodiks.</span><span class="sxs-lookup"><span data-stu-id="7be3e-119">In the **Value** field, enter the percentage of TDS for the TDS tax code.</span></span>
11. <span data-ttu-id="7be3e-120">Sulgege **Kinnipeetava maksu väärtus** leht, et naasta **Kinnipeetava maksu koodid** lehele.</span><span class="sxs-lookup"><span data-stu-id="7be3e-120">Close the **Withholding tax values** page to return to the **Withholding tax codes** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7be3e-121">**Limiidid** nupp **Kinnipeetava maksu koodid** lehel ei ole saadaval maksukoodide puhul, mille tüüp on TDS.</span><span class="sxs-lookup"><span data-stu-id="7be3e-121">The **Limits** button on the **Withholding tax codes** page isn't available for tax codes of the TDS tax type.</span></span>

12. <span data-ttu-id="7be3e-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="7be3e-122">Close the page.</span></span>
