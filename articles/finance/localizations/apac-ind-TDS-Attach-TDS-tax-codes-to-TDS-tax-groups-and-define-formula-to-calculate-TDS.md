---
title: TDS-i maksukoodide TDS-i maksugruppidele manustamine ja TDS-i arvutamise valemi määratlemine
description: See teema kirjeldab, kuidas seadistada maksugruppides mahaarvatud maksu allika (TDS) ja lisada TDS-i maksukoodid TDS-maksugruppidele. TDS-i maksugrupi TDS-i arvutamiseks peate määrama sellele lisatud TDS-i maksukoodide valemi.
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
ms.openlocfilehash: ec0d683153bd5ab731035159d32881fbdb352d70
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023187"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a><span data-ttu-id="50aa0-104">TDS-i maksukoodide TDS-i maksugruppidele manustamine ja TDS-i arvutamise valemi määratlemine</span><span class="sxs-lookup"><span data-stu-id="50aa0-104">Attach TDS tax codes to TDS tax groups and define the formula for calculating TDS</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50aa0-105">See teema kirjeldab, kuidas seadistada maksugruppides mahaarvatud maksu allika (TDS) ja lisada TDS-i maksukoodid TDS-maksugruppidele.</span><span class="sxs-lookup"><span data-stu-id="50aa0-105">This topic explains how to set up Tax Deducted at Source (TDS) tax groups and attach TDS tax codes to TDS tax groups.</span></span> <span data-ttu-id="50aa0-106">TDS-i maksugrupi TDS-i arvutamiseks peate määrama sellele lisatud TDS-i maksukoodide valemi.</span><span class="sxs-lookup"><span data-stu-id="50aa0-106">To calculate TDS for a TDS tax group, you must define the formula for TDS tax codes that are attached to it.</span></span>

<span data-ttu-id="50aa0-107">Järgige neid samme TDS-i maksugrupi häälestamiseks, lisage TDS-i maksukoodid ja määratlege TDS-i arvutamiseks valem.</span><span class="sxs-lookup"><span data-stu-id="50aa0-107">Follow these steps to set up a TDS tax group, attach TDS tax codes to it, and define the formula for calculating TDS.</span></span>

1. <span data-ttu-id="50aa0-108">Avage **Maks \> Kaudsed maksud \> Kinnipeetav maks \> Kinnipeetava maksu grupid**.</span><span class="sxs-lookup"><span data-stu-id="50aa0-108">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax groups**.</span></span>

    <span data-ttu-id="50aa0-109">[![Kinnipeetava maksugrupi leht](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span><span class="sxs-lookup"><span data-stu-id="50aa0-109">[![Withholding tax groups page](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span></span>

2. <span data-ttu-id="50aa0-110">Tegevuspaanil valige **Uus** TDS-ile kinnipeetava maksu grupi loomiseks ja sisestage nõutavad üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="50aa0-110">On the Action Pane, select **New** to create a withholding tax group for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="50aa0-111">Tehke väljal **Maksu tüüp** valik **TDS**.</span><span class="sxs-lookup"><span data-stu-id="50aa0-111">In the **Tax type** field, select **TDS**.</span></span>
4. <span data-ttu-id="50aa0-112">Tehke uue rea loomiseks kiirkaardil **Seaded** valik **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="50aa0-112">On the **Setup** FastTab, select **Add** to create a line.</span></span>
5. <span data-ttu-id="50aa0-113">Valige väljal **Kinnipeetava maksu kood** kinnipeetava maksu grupi jaoks kinnipeetava maksu kood.</span><span class="sxs-lookup"><span data-stu-id="50aa0-113">In the **Withholding tax code** field, select the TDS tax code for the TDS tax group.</span></span> <span data-ttu-id="50aa0-114">Väljal **Kinnipeetava maksu nimi** kuvatakse TDS-maksukoodi nimi ja väljal **Väärtus** kuvatakse väärtus.</span><span class="sxs-lookup"><span data-stu-id="50aa0-114">The **Withholding tax name** field shows the name of the TDS tax code, and the **Value** field shows the value.</span></span>
6. <span data-ttu-id="50aa0-115">TDS-kannetes TDS-i maksukoodiga seotud TDS-i maksukomponendile määratud läve limiidi ja erandi läve limiidi ignoreerimiseks märkige ära **Unusta lävi** ruut.</span><span class="sxs-lookup"><span data-stu-id="50aa0-115">To ignore the threshold limit and exception threshold limit that are defined for the TDS tax component that is attached to the TDS tax code in TDS transactions, select the **Overlook threshold** check box.</span></span>
7. <span data-ttu-id="50aa0-116">Valige märkeruut **Vabastatud**, et vältida arvutatud summa redigeerimist programmi mallis.</span><span class="sxs-lookup"><span data-stu-id="50aa0-116">To prevent the tax group from being calculated in transactions, select the **Exempt** check box.</span></span>
8. <span data-ttu-id="50aa0-117">Tegevuspaanil valige **Kujundaja** et avada valemikoosturit, nii et saate TDS-i maksugrupi jaoks määratleda TDS-i arvutamise valemi.</span><span class="sxs-lookup"><span data-stu-id="50aa0-117">On the Action Pane, select **Designer** to open the formula designer, so that you can define the formula for calculating TDS for the TDS tax group.</span></span> <span data-ttu-id="50aa0-118">Lehel **Kujundaja** kuvatakse vahekaardil **Maksud** TDS-i maksugrupi jaoks valitud TDS-i maksukoodid.</span><span class="sxs-lookup"><span data-stu-id="50aa0-118">On the **Designer** page, the **Taxes** tab shows the TDS tax codes that have been selected for the TDS tax group.</span></span>

    <span data-ttu-id="50aa0-119">[![Kujundaja leht](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span><span class="sxs-lookup"><span data-stu-id="50aa0-119">[![Designer page](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span></span>

9. <span data-ttu-id="50aa0-120">Rea **Kalkulatsioon** loomiseks valige vahekaardil **Alt+N**.</span><span class="sxs-lookup"><span data-stu-id="50aa0-120">On the **Calculation** tab, select **Alt+N** to create a line.</span></span> <span data-ttu-id="50aa0-121">Väli **ID** näitab automaatselt loodud prioriteedi ID-d TDS-i arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="50aa0-121">The **ID** field shows the automatically generated priority ID for TDS calculation.</span></span>
10. <span data-ttu-id="50aa0-122">Valige väljal **Kinnipeetava maksu kood** kinnipeetava maksu grupi jaoks kinnipeetava maksu kood.</span><span class="sxs-lookup"><span data-stu-id="50aa0-122">In the **Tax code** field, select the TDS tax code to define the formula for.</span></span> <span data-ttu-id="50aa0-123">Kõik TDS-i maksukoodid, mis on TDS-i maksugrupi jaoks valitud, on sellel väljal saadaval.</span><span class="sxs-lookup"><span data-stu-id="50aa0-123">All the TDS tax codes that have been selected for the TDS tax group are available for selection in this field.</span></span>
11. <span data-ttu-id="50aa0-124">Väljal **Maksustatava alus** valige TDS-i arvutamise alus:</span><span class="sxs-lookup"><span data-stu-id="50aa0-124">In the **Taxable basis** field, select the basis for calculating TDS:</span></span>

    - <span data-ttu-id="50aa0-125">**Brutosumma** – Arvutage TDS kande brutosumma (st arve summa) alusel, kasutades maksukoodi jaoks määratletud arvutusavaldist.</span><span class="sxs-lookup"><span data-stu-id="50aa0-125">**Gross amount** – Calculate TDS based on the gross transaction amount (that is, the invoice amount) by using the calculation expression that is defined for the tax code.</span></span>
    - <span data-ttu-id="50aa0-126">**Välja arvatud brutosumma** – Arvutage TDS maksukoodile määratud arvutusavaldise alusel.</span><span class="sxs-lookup"><span data-stu-id="50aa0-126">**Excl Gross amount** – Calculate TDS based on the calculation expression that is defined for the tax code.</span></span>

    > [!NOTE]
    > <span data-ttu-id="50aa0-127">Välja **Maksustatav alus** ei saa seada väärtusele **Välja arvatud brutosumma** TDS-maksukoodi jaoks, mille prioriteedi ID on **1**.</span><span class="sxs-lookup"><span data-stu-id="50aa0-127">The **Taxable basis** field can't be set to **Excl Gross amount** for the TDS tax code that has a priority ID of **1**.</span></span>

12. <span data-ttu-id="50aa0-128">TDS-i arvutus põhineb valemil, mis on määratud arvutusavaldise väljal **Arvutusavaldis** TDS-maksugrupiga seotud maksukoodi jaoks.</span><span class="sxs-lookup"><span data-stu-id="50aa0-128">The TDS calculation is based on the formula that is defined in the **Calculation expression** field for each tax code that is attached to the TDS tax group.</span></span> <span data-ttu-id="50aa0-129">Valige plussmärk (**+**), miinusmärk (**-**), korrutusmärk (**\**_), või jagamismärk (_*/**) TDS-maksukoodi arvutusavaldise sisestamiseks **Arvutusavaldis** väljal.</span><span class="sxs-lookup"><span data-stu-id="50aa0-129">Select the plus sign (**+**), minus sign (**-**), multiplication sign (**\**_), or division sign (_*/**) button to enter the calculation expression for the selected TDS tax code in the **Calculation expression** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="50aa0-130">Arvutusavaldist ei saa määrata TDS-i maksukoodile, mille prioriteedi ID on **1**.</span><span class="sxs-lookup"><span data-stu-id="50aa0-130">No calculation expression can be defined for the TDS tax code that has a priority ID of **1**.</span></span>

13. <span data-ttu-id="50aa0-131">TDS-i maksukoodi arvutusavaldise määratlemiseks **Arvutusavaldise** väljal, lisage saadaolevad TDS-maksukoodid **Maksud** vahekaardile. TDS-i maksukoodide lisamiseks **Arvutusavaldise** väljale saate kasutada mõnda järgmistest meetoditest:</span><span class="sxs-lookup"><span data-stu-id="50aa0-131">To define the calculation expression for the TDS tax code in the **Calculation expression** field, add TDS tax codes that are available on the **Taxes** tab. To add TDS tax codes in the **Calculation expression** field, you can use any of the following methods:</span></span>

    - <span data-ttu-id="50aa0-132">Lohistage nõutav maksukood **Maksud** vahekaardilt **Arvutusavaldise** väljale.</span><span class="sxs-lookup"><span data-stu-id="50aa0-132">Drag the required tax code from the **Taxes** tab to the **Calculation expression** field.</span></span>
    - <span data-ttu-id="50aa0-133">Topeltpuudutage (või topeltklõpsake) vahekaardil **Maksud** nõutavat maksukoodi.</span><span class="sxs-lookup"><span data-stu-id="50aa0-133">Double-tap (or double-click) the required tax code on the **Taxes** tab.</span></span>
    - <span data-ttu-id="50aa0-134">Valige ja hoidke all (või paremklõpsake) nõutavat maksukoodi vahekaardil **Maksud** ja valige **Lisage maksukood**.</span><span class="sxs-lookup"><span data-stu-id="50aa0-134">Select and hold (or right-click) the required tax code on the **Taxes** tab, and then select **Add tax code**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="50aa0-135">Saate lisada arvutusavaldise iga TDS-i maksukoodi ette.</span><span class="sxs-lookup"><span data-stu-id="50aa0-135">Insert a calculation expression before each TDS tax code.</span></span> <span data-ttu-id="50aa0-136">Arvutusavaldisse lisatud TDS-maksukoodid kuvatakse sulgudes (\[...\]).</span><span class="sxs-lookup"><span data-stu-id="50aa0-136">The TDS tax codes that have been added to the calculation expression appear in brackets (\[...\]).</span></span>

14. <span data-ttu-id="50aa0-137">Käibemaksukoodi jaoks määratletud arvutusavaldise tühjendamiseks väljal **Arvutusavaldis** valige **C** nupp.</span><span class="sxs-lookup"><span data-stu-id="50aa0-137">To clear the calculation expression that is defined for a tax code in the **Calculation expression** field, select the **C** button.</span></span>
15. <span data-ttu-id="50aa0-138">Kirje kustutamiseks vahekaardil **Kalkulatsioon** valige **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="50aa0-138">To delete a record on the **Calculation** tab, select **Delete**.</span></span>
16. <span data-ttu-id="50aa0-139">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="50aa0-139">Close the page.</span></span>
