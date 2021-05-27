---
title: TDS-i arvete arvutamine ostutellimuse vormi ja müügitellimuse vormi abil
description: Selles teemas loetletakse töölehtedel allikalt (TDS) maha arvatud maksu arvutamise sammud.
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
ms.openlocfilehash: e7925206f3c060c6332de9d4972c8a7fb0066be2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023168"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a><span data-ttu-id="e08af-103">TDS-i arvete arvutamine ostutellimuse vormi ja müügitellimuse vormi abil</span><span class="sxs-lookup"><span data-stu-id="e08af-103">Calculate TDS invoices using purchase order form and sales order form</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e08af-104">Selles teemas loetletakse allika järgi mahaarvatud maksu arvutamise sammud erinevat tüüpi arvetel, kasutades **Ostutellimuse**, **Ostutöölehe**, **Raamtellimuse**, ja **Müügitellimuse** lehekülgi.</span><span class="sxs-lookup"><span data-stu-id="e08af-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on various types of invoices using the **Purchase order**, **Purchase journal**, **Blanket order**, and **Sales order** pages.</span></span>

1. <span data-ttu-id="e08af-105">Looge loetletud lehte kasutades ostutellimus, ostutööleht, ostu raamtellimus või müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="e08af-105">Create a purchase order, purchase journal, purchase blanket order, or a sales order using the page listed.</span></span> <span data-ttu-id="e08af-106">Sisestage nõutavad üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="e08af-106">Enter the required details.</span></span>

2. <span data-ttu-id="e08af-107">Valige **Seadistus** vahekaart kliendi hinnastja olemuse vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="e08af-107">Select the **Setup** tab to view the nature of the assessee of the vendor or customer.</span></span> <span data-ttu-id="e08af-108">See teave on loetletud **Hinnaastatava olemus** väljal **Kinnipeetava maksu grupp** väljagrupis.</span><span class="sxs-lookup"><span data-stu-id="e08af-108">This information is listed in the **Nature of assessee** field, under the **Withholding tax group** field group.</span></span>

3. <span data-ttu-id="e08af-109">Väljal **TDS grupp** vaadake või muutke hankijale või kliendile määratud vaikimisi TDS-i gruppi.</span><span class="sxs-lookup"><span data-stu-id="e08af-109">In the **TDS group** field, view or modify the default TDS group defined for the vendor or customer.</span></span>

   > [!NOTE]
   > <span data-ttu-id="e08af-110">Väli **TCS-grupp** ei ole saadaval, kui valite TDS-grupi **TDS-grupp** väljal.</span><span class="sxs-lookup"><span data-stu-id="e08af-110">The **TCS group** field isn't available when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="e08af-111">TDS arvutatakse ainult siis, kui on märgitud **Arvuta kinnipeetav maks** ruut kas **Kõik hankijad** või **Kõik kliendid** lehel.</span><span class="sxs-lookup"><span data-stu-id="e08af-111">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** page.</span></span>  

4. <span data-ttu-id="e08af-112">Looge kaubaread vahekaardil **Read** ja sisestage nõutavad üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="e08af-112">Create item lines on the **Lines** tab and enter the required details.</span></span>

5. <span data-ttu-id="e08af-113">Valige vahekaart **Seadistus** (reatase), et vaadata või muuta päise taseme määratletud TDS-gruppi.</span><span class="sxs-lookup"><span data-stu-id="e08af-113">Select the **Setup** tab (line-level) to view or change the TDS group defined at the header-level.</span></span> <span data-ttu-id="e08af-114">TDS-i grupp kuvatakse **TDS-grupi** väljal, mis asub **Kinnipeetava maksu grupi** väljagrupis.</span><span class="sxs-lookup"><span data-stu-id="e08af-114">The TDS group is displayed in the **TDS group** field, which is under the **Withholding tax group** field group.</span></span>

6. <span data-ttu-id="e08af-115">Valige **Maksuteave** vahekaart, vajadusel valige ettevõttele sellel väljal seadistatud alternatiivsed aadressid.</span><span class="sxs-lookup"><span data-stu-id="e08af-115">Select the **Tax information** tab and select alternate addresses that are set up for the company name that's displayed in this field.</span></span> <span data-ttu-id="e08af-116">Ettevõtte nime saate vaadata väljal **Nimi**, mis on **Ettevõtte teave** väljagrupis.</span><span class="sxs-lookup"><span data-stu-id="e08af-116">The company name is displayed in the **Name** field, which is under the **Company information** field group.</span></span> 

   <span data-ttu-id="e08af-117">Valitud ettevõtte TAN kuvatakse väljal **Maksukonto number** (**TAN**) väljal, **Kinnipeetava maksu** väljagrupi all.</span><span class="sxs-lookup"><span data-stu-id="e08af-117">The TAN of the selected company name is displayed in the **Tax Account Number** (**TAN**) field, under the **Withholding tax** field group.</span></span> 

7. <span data-ttu-id="e08af-118">Valige **Kinnipeetav maks**, et avada **Kinnipeetava maksu kannete** leht.</span><span class="sxs-lookup"><span data-stu-id="e08af-118">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="e08af-119">Järgmised väljad kuvatakse ülemisel paanil **Ajutise kinnipeetava maksu kannete** lehel.</span><span class="sxs-lookup"><span data-stu-id="e08af-119">View the following fields on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="e08af-120">**Kinnipeetava** **maksu** **summa** **koos** **kokku** - TDS-grupi kande jaoks arvutatud TDS-i kogusumma.</span><span class="sxs-lookup"><span data-stu-id="e08af-120">**Withholding** **tax** **amount** **in** **total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="e08af-121">Väljal **Väärtus** - Kuvatakse kande TDS-i arvutamiseks kasutatav koguprotsent.</span><span class="sxs-lookup"><span data-stu-id="e08af-121">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="e08af-122">Koguprotsent põhineb valemil, mis on määratud TDS-grupiga seotud TDS-i maksukoodide jaoks.</span><span class="sxs-lookup"><span data-stu-id="e08af-122">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="e08af-123">**Korrigeeritud kinnipeetava maksu summa kokku** - TDS-i grupi kõikide maksukoodide korrigeeritud TDS-i kogusumma.</span><span class="sxs-lookup"><span data-stu-id="e08af-123">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="e08af-124">**TDS** - Kui see on valitud, lisatakse kandele TDS-grupp.</span><span class="sxs-lookup"><span data-stu-id="e08af-124">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

<span data-ttu-id="e08af-125">Välja **Ülevaade**, **Üldine**, ja **Kohandamine** vahekaardil **Kinnipeetava maksu kannete** lehel kuvatakse TDS-summa ja korrigeeritud TDS-i summa TDS-i grupiga seotud TDS-i maksukoodi kohta.</span><span class="sxs-lookup"><span data-stu-id="e08af-125">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

8. <span data-ttu-id="e08af-126">Valige **Lävend** valimine lehe **Lävendd** avamiseks.</span><span class="sxs-lookup"><span data-stu-id="e08af-126">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="e08af-127">Vaadake sellel leheküljel konkreetse TDS-i maksukoodiga seotud TDS-i maksukomponendi jaoks määratletud lävendi limiiti ja erandi lävendi limiiti.</span><span class="sxs-lookup"><span data-stu-id="e08af-127">View the threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

9. <span data-ttu-id="e08af-128">Valige **Valemikoostur** et avada **Valemikoosturi** leht.</span><span class="sxs-lookup"><span data-stu-id="e08af-128">Select **Formula designer** to open the **Formula designer** page.</span></span> <span data-ttu-id="e08af-129">Vaadake sellel leheküljel konkreetse TDS-i maksukoodi jaoks määratletud valemit.</span><span class="sxs-lookup"><span data-stu-id="e08af-129">View the formula that is defined for a specific TDS tax code on this page.</span></span> 

10. <span data-ttu-id="e08af-130">Sisestage arve.</span><span class="sxs-lookup"><span data-stu-id="e08af-130">Post the invoice.</span></span> <span data-ttu-id="e08af-131">Ostuarvetel arvutatud TDS-i summa sisestatakse ostureskontrole ja müügiarvetel arvutatud TDS-summa sisestatakse müügireskontro kontole, mis on määratud igale TDS-i maksukoodile TDS-grupis.</span><span class="sxs-lookup"><span data-stu-id="e08af-131">The TDS amount calculated on purchase invoices is posted to the payable account and the TDS amount calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="e08af-132">TDS-i maksukoodide ostureskontro või müügireskontrod määratletakse **Kinnipeetava maksu koodide** lehel.</span><span class="sxs-lookup"><span data-stu-id="e08af-132">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

11. <span data-ttu-id="e08af-133">Valige **Päring** nupp **> Arve >Sisestatud kinnipeetav maks** nuppu et avada **Kinnipeetava maksu kannete** leht.</span><span class="sxs-lookup"><span data-stu-id="e08af-133">Select **Inquiry** button **> Invoice > Posted withholding tax** button to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="e08af-134">Väljal **Väärtus** kuvatakse kande TDS-i arvutamiseks kasutatav koguprotsent.</span><span class="sxs-lookup"><span data-stu-id="e08af-134">You can view the total percentage used to calculate TDS for the transaction in the **Value** field.</span></span>

<span data-ttu-id="e08af-135">Väljad **Ülevaade**, **Üldine**, ja **Summa** vahekaardil **Kinnipeetava maksu kannete** lehel kuvavad kande kohta arvutatud TDS-i teabe.</span><span class="sxs-lookup"><span data-stu-id="e08af-135">The fields on the **Overview**, **General**, and **Amount** tabs on the **Withholding tax transactions** page display the information of TDS calculated for the transaction.</span></span> <span data-ttu-id="e08af-136">Vaadake TDS-i kalkulatsiooniteavet iga TDS-grupiga seotud TDS-i maksukoodi kohta.</span><span class="sxs-lookup"><span data-stu-id="e08af-136">View the TDS calculation information for each TDS tax code attached to the TDS group.</span></span>
