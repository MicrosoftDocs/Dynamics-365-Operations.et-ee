---
title: Maksukomponentide häälestamine TDS-i maksutüübi jaoks
description: See teema kirjeldab, kuidas seadistada kinnipeetava maksu komponente allika (TDS) maksutüübis mahaarvatud maksu jaoks. See selgitab ka, kuidas määrata läve limiiti, mida kasutatakse iga TDS-i komponendi TDS-i arvutamiseks.
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
ms.openlocfilehash: 6e0a6a05fcb4afb8c8965e25c3089bc1b3d98431
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023173"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a><span data-ttu-id="8a8ff-104">Maksukomponentide häälestamine TDS-i maksutüübi jaoks</span><span class="sxs-lookup"><span data-stu-id="8a8ff-104">Set up tax components for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a8ff-105">See teema kirjeldab, kuidas seadistada kinnipeetava maksu komponente allika (TDS) maksutüübis mahaarvatud maksu jaoks.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-105">This topic explains how to set up withholding tax components for the Tax Deducted at Source (TDS) tax type.</span></span> <span data-ttu-id="8a8ff-106">TDS-i komponendid on TDS, lisatasu, PE-Cess ja SHE Cess.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-106">The TDS components are TDS, surcharge, PE-Cess, and SHE Cess.</span></span> <span data-ttu-id="8a8ff-107">See selgitab ka, kuidas määrata läve limiiti, mida kasutatakse iga TDS-i komponendi TDS-i arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-107">This topic also explains how to define the threshold that is used to calculate TDS for each TDS component.</span></span> <span data-ttu-id="8a8ff-108">Lisaks saate määratleda erandi läve, mida kasutatakse iga TDS-i komponendi TDS-i arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-108">Additionally, you can define an exception threshold that is used to calculate TDS for each TDS component.</span></span>

<span data-ttu-id="8a8ff-109">TDS komponentidde häälestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-109">Follow these steps to set up TDS components.</span></span>

1. <span data-ttu-id="8a8ff-110">Minge **Maks \> Seadistus \> Kinnipeetav maks \> Kinnipeetava maksu komponendid**.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-110">Go to **Tax \> Setup \> Withholding tax \> Withholding tax components**.</span></span>

    <span data-ttu-id="8a8ff-111">[![Kinnipeetava maksu komponentide leht](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span><span class="sxs-lookup"><span data-stu-id="8a8ff-111">[![Withholding tax components page](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span></span>

2. <span data-ttu-id="8a8ff-112">**Maksu tüübi** väljal valige **TDS** kinnipeetava maksu komponentide häälestamiseks.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-112">In the **Tax type** field, select **TDS** to set up withholding tax components for the TDS tax type.</span></span>
3. <span data-ttu-id="8a8ff-113">Rea loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-113">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="8a8ff-114">Sisestage **Kinnipeetava maksu** väljale TDS-i komponendi nimi.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-114">In the **Withholding tax component** field, enter a name for the TDS component.</span></span>
5. <span data-ttu-id="8a8ff-115">Väljal **Kinnipeetava maksu komponendigrupp** valige TDS-i kinnipeetava maksu komponendi grupp, et lisada TDS-i komponent.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-115">In the **Withholding tax component group** field, select the TDS withholding tax component group to attach the TDS component to.</span></span>
6. <span data-ttu-id="8a8ff-116">Sisestage TDS komponendi kirjeldus kiirkaardi **Üldine** väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-116">On the **General** FastTab, in the **Description** field, enter a description of  the TDS component.</span></span>
7. <span data-ttu-id="8a8ff-117">Tegevuspaanil valige **Avamisläve** lehel **Lävi** leht, nii et saate määratleda läve, mida kasutatakse TDS-i komponendi jaoks TDS-i arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-117">On the Action Pane, select **Threshold** to open **Threshold** page, so that you can define the threshold that is used to calculate TDS for the TDS component.</span></span>
8. <span data-ttu-id="8a8ff-118">Kasutage välju **Alates** ja **Kuni** et määrata periood, mille suhtes lävi kehtib.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-118">Use the **From date** and **To date** fields to define the period that the threshold is applicable to.</span></span>
9. <span data-ttu-id="8a8ff-119">**Üldisele** kiirkaardile **Läve** väljal sisestage lävendsumma, mida kasutatakse TDS-i komponendi jaoks TDS-i arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-119">On the **General** FastTab, in the **Threshold** field, enter the threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="8a8ff-120">Maks arvatakse maha allika juures ainult siis, kui kumulatiivne arvesumma ületab läve.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-120">The tax will be deducted at the source only when the cumulative invoice amount crosses the threshold.</span></span>

    <span data-ttu-id="8a8ff-121">Näiteks kui lävisumma on 10 000, siis arvutatakse TDS pärast seda, kui kumulatiivne arvesumma on suurem kui 10 000 (teisisõnu, kui see on 10 001 või enam).</span><span class="sxs-lookup"><span data-stu-id="8a8ff-121">For example, if the threshold amount is 10,000, TDS is calculated after the cumulative invoice amount exceeds 10,000 (in other words, when it's 10,001 or more).</span></span>

10. <span data-ttu-id="8a8ff-122">Kaardile **Erani lävi** väljal sisestage lävendsumma, mida kasutatakse TDS-i komponendi jaoks TDS-i arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-122">In the **Exception threshold** field, enter the exception threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="8a8ff-123">Maks arvatakse maha allika juures ainult siis, kui kumulatiivne arvesumma ületab läve.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-123">The tax on an invoice line will be deducted at the source only when the amount crosses the exception threshold.</span></span>

    <span data-ttu-id="8a8ff-124">Näiteks kui erandi lävisumma on 5000, siis arvutatakse TDS konkreetsel arvereal, kui arve rea summa ületab 5000 (teisisõnu on see 5001 või rohkem).</span><span class="sxs-lookup"><span data-stu-id="8a8ff-124">For example, if the exception threshold amount is 5,000, TDS is calculated on a specific invoice line if the invoice line amount exceeds 5,000 (in other words, if it's 5,001 or more).</span></span>

    <span data-ttu-id="8a8ff-125">[![Läve leht](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span><span class="sxs-lookup"><span data-stu-id="8a8ff-125">[![Threshold page](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="8a8ff-126">Erandi lävisumma peab olema lävisummast väiksem või sellega võrdne.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-126">The exception threshold amount must be less than or equal to the threshold amount.</span></span>
    >
    > <span data-ttu-id="8a8ff-127">Kande maks arvatakse maha, kui kande summa ületab erandi läve, isegi kui kumulatiivne arvesumma ei ületa **Läve** määratud välja.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-127">The tax is deducted for a transaction if the transaction amount crosses the exception threshold, even if the cumulative invoice amount doesn't cross the threshold that is specified in the **Threshold** field.</span></span>

11. <span data-ttu-id="8a8ff-128">Sulgege leht **Lävi**, et naasta **kinnipeetava maksu komponentide** lehele.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-128">Close the **Threshold** page to return to the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="8a8ff-129">Tegevuspaanil valige suvand Kopeeri, et avada dialoogiboks Kinnipeetava maksu komponentide kopeerimine, nii et saate kopeerida ühe TDS-i komponendigrupi jaoks seadistatud TDS-i komponendid teise **Kopeeri** et avada dialoogiboks **Kinnipeetava maksu komponentide kopeerimine** nii et saate kopeerida ühe TDS-i komponendigrupi jaoks seadistatud TDS-i komponendid teise TDSi komponendigruppi.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-129">On the Action Pane, select **Copy** to open the **Copy withholding tax components** dialog box, so that you can copy the TDS components that were set up for one TDS component group to another TDS component group.</span></span>
13. <span data-ttu-id="8a8ff-130">Valige väljal **Alates** komponendigrupp TDS, millelt TDS-i komponente kopeerida.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-130">In the **From** field, select the TDS component group to copy the TDS components from.</span></span> <span data-ttu-id="8a8ff-131">Valige väljal **Alates** komponendigrupp TDS, millelt TDS-i komponente kopeerida.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-131">In the **To** field, select the withholding tax component group to copy the TDS components to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8a8ff-132">TDS-i mõlema komponendigrupiga seotud ühiseid TDS-i komponente ei kopeerita.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-132">Common TDS components that are attached to both TDS component groups aren't copied.</span></span>

14. <span data-ttu-id="8a8ff-133">Valige **OK** et kopeerida ja luua TDS-i komponente muule TDS-i komponendigrupile **kinnipeetava maksu komponentide** lehel.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-133">Select **OK** to copy and create TDS components for the other TDS component group on the **Withholding tax components** page.</span></span>

    <span data-ttu-id="8a8ff-134">[![Kinnipeetava maksu komponentide dialoogiboksi kopeerimine](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span><span class="sxs-lookup"><span data-stu-id="8a8ff-134">[![Copy withholding tax components dialog box](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span></span>

15. <span data-ttu-id="8a8ff-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="8a8ff-135">Close the page.</span></span>
