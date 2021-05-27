---
title: TDS-i arvutamine arvetel vabas vormis arve lehelt
description: See teema kirjeldab, kuidas arvutada arvetel allika järgi mahaarvatud maks (TDS), kasutades vabas vormis arvelehte.
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
ms.openlocfilehash: 7d551a8ba6ba9ca282fd9de3fa7d7c7303e394ed
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023184"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a><span data-ttu-id="f8865-103">TDS-i arvutamine arvetel vabas vormis arve lehelt</span><span class="sxs-lookup"><span data-stu-id="f8865-103">TDS calculation on invoices from the Free text invoice page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8865-104">See teema kirjeldab, kuidas arvutada arvetel allika järgi mahaarvatud maks (TDS), kasutades **vabas vormis arvelehe** lehte.</span><span class="sxs-lookup"><span data-stu-id="f8865-104">This topic explains how to calculate Tax Deducted at Source (TDS) on invoices by using the **Free text invoice** page.</span></span>

1. <span data-ttu-id="f8865-105">Avage **Müügireskontro \> Arved \> Kõik vabas vormis arved**.</span><span class="sxs-lookup"><span data-stu-id="f8865-105">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>

    <span data-ttu-id="f8865-106">[![Vabas tekstis arve leht](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span><span class="sxs-lookup"><span data-stu-id="f8865-106">[![Free text invoice page](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span></span>

2. <span data-ttu-id="f8865-107">Tehke valik **Uus**, et luua maksetööleht, ja sisestage seejärel nõutavad üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="f8865-107">Select **New** to create a free text invoice, and enter the required details.</span></span>
3. <span data-ttu-id="f8865-108">Vaadake hankija või kliendi hinnalepete kategooria olemust **Arve** vahekaardil, **Kinnipeetava maksu** väljagrupis ja **Hinna hindamise** väljal.</span><span class="sxs-lookup"><span data-stu-id="f8865-108">Select the **Invoice** tab. In the **Withholding tax group** section, the **Nature of assessee** field shows the nature of assessee category of the customer.</span></span>
4. <span data-ttu-id="f8865-109">Väljal **TDS grupp** vaadake või muutke hankijale või kliendile määratud vaikimisi TDS-i gruppi.</span><span class="sxs-lookup"><span data-stu-id="f8865-109">In the **TDS group** field, review or change the default TDS group that is defined for the customer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f8865-110">Väli **TCS-grupp** ei ole saadaval, kui valite TDS-grupi väärtuse **TDS-grupp** väljal.</span><span class="sxs-lookup"><span data-stu-id="f8865-110">When you select a value in the **TDS group** field, the **TCS group** field becomes unavailable.</span></span> <span data-ttu-id="f8865-111">TDS arvutatakse ainult siis, kui on märgitud **Arvuta kinnipeetav maks** valik **Jah** klientide jaoks **Kõik kliendid** lehel.</span><span class="sxs-lookup"><span data-stu-id="f8865-111">TDS is calculated only if the **Calculate withholding tax** option is set to **Yes** for the customer on the **All customers** page.</span></span>

5. <span data-ttu-id="f8865-112">Vahekaardil **Maksuteave**, **Ettevõtte teave** jaotises **Nimi** väljal valige ettevõtte nimi, mis on seadistatud alternatiivse aadressi jaoks.</span><span class="sxs-lookup"><span data-stu-id="f8865-112">On the **Tax information** tab, in the **Company information** section, in the **Name** field, select the company name for an alternate address that has been set up for the company.</span></span>

    <span data-ttu-id="f8865-113">**Kinnipeetava maksu** jaotises kuvatakse väljal **Maksukonto number (TAN)** väljal kuvatakse valitud ettevõtte maksukonto number (TAN).</span><span class="sxs-lookup"><span data-stu-id="f8865-113">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the tax account number (TAN) for the selected company.</span></span>

6. <span data-ttu-id="f8865-114">Looge kaubaread vahekaardil **Arve read** ja sisestage nõutavad üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="f8865-114">On the **Invoice lines** tab, create invoice lines, and enter the required details.</span></span>

    <span data-ttu-id="f8865-115">**Kinnipeetava maksu grupi** jaotises näitab väli **Maksukonto number (TAN)** väljal näitab TANi ja **TDS-grupp** väli TDS-gruppi.</span><span class="sxs-lookup"><span data-stu-id="f8865-115">In the **Withholding tax group** section, the **Tax Account Number (TAN)** field shows the TAN, and the **TDS group** field shows the TDS group.</span></span>

7. <span data-ttu-id="f8865-116">Valige **Kinnipeetav maks**, et avada **Kinnipeetava maksu kannete** leht.</span><span class="sxs-lookup"><span data-stu-id="f8865-116">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="f8865-117">Selle lehekülje ülemisel osal on järgmised väljad:</span><span class="sxs-lookup"><span data-stu-id="f8865-117">The upper part of this page has the following fields:</span></span>

    - <span data-ttu-id="f8865-118">**Kinnipeetava maksu summa kokku** - TDS-grupi kande jaoks arvutatud TDS-i kogusumma.</span><span class="sxs-lookup"><span data-stu-id="f8865-118">**Withholding tax amount in total** – The total TDS that was calculated for the transaction for the TDS group.</span></span>
    - <span data-ttu-id="f8865-119">Väljal **Väärtus** - Kuvatakse kande TDS-i arvutamiseks kasutatav koguprotsent.</span><span class="sxs-lookup"><span data-stu-id="f8865-119">**Value** – The total percentage that was used to calculate TDS for the transaction.</span></span> <span data-ttu-id="f8865-120">Koguprotsent põhineb valemil, mis on määratud TDS-grupiga seotud TDS-i maksukoodide jaoks.</span><span class="sxs-lookup"><span data-stu-id="f8865-120">The total percentage is based on the formula that is defined for the TDS tax codes and attached to the TDS group.</span></span>
    - <span data-ttu-id="f8865-121">**Korrigeeritud kinnipeetava maksu summa kokku** - TDS-i grupi kõikide maksukoodide korrigeeritud TDS-i kogusumma.</span><span class="sxs-lookup"><span data-stu-id="f8865-121">**Adjusted withholding tax amount in total** – The total adjusted TDS amount for all tax codes in the TDS group.</span></span>
    - <span data-ttu-id="f8865-122">**TDS** – valitud märkeruut näitab, et TDS-grupp on kandega seotud.</span><span class="sxs-lookup"><span data-stu-id="f8865-122">**TDS** – A selected checkbox indicates that a TDS group is attached to the transaction.</span></span>

    <span data-ttu-id="f8865-123">Välja **Ülevaade**, **Üldine**, ja **Summa** vahekaardil kinnipeetava maksu kannete lehel kuvatakse TDS-summa ja korrigeeritud TDS-i summa TDS-i grupiga seotud TDS-i maksukoodi kohta.</span><span class="sxs-lookup"><span data-stu-id="f8865-123">The fields on the **Overview**, **General**, and **Adjustment** tabs show the calculated TDS amount and details of the adjusted TDS amount for each TDS tax code that is attached to the TDS group.</span></span>

8. <span data-ttu-id="f8865-124">Valige **Lävi** et avada leht **Lävi** kus saate üle vaadata läve piirmäära, mis on määratud konkreetse TDS-maksukoodiga seotud TDS-i maksukomponendile.</span><span class="sxs-lookup"><span data-stu-id="f8865-124">Select **Threshold** to open the **Threshold** page, where you can review the threshold limit that is defined for the TDS tax component that is attached to a specific TDS tax code.</span></span>
9. <span data-ttu-id="f8865-125">Valige **Valemikoostur** et avada **Valemikoosturi leht** kus saate üle vaadata TDS-i maksukoodi jaoks määratud valemi.</span><span class="sxs-lookup"><span data-stu-id="f8865-125">Select **Formula designer** to open the **Formula designer** page, where you can review the formula that is defined for a specific TDS tax code.</span></span>
10. <span data-ttu-id="f8865-126">Vabas vormis arve sisestamine.</span><span class="sxs-lookup"><span data-stu-id="f8865-126">Post the free text invoice.</span></span> <span data-ttu-id="f8865-127">Müügiarvetel arvutatud TDS-summa sisestatakse tasumisele kuuluvale kontole, mis on määratud igale TDS-i maksukoodile TDS-grupis.</span><span class="sxs-lookup"><span data-stu-id="f8865-127">The TDS amount that is calculated for the free text invoice is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="f8865-128">TDS-i maksukoodide ostureskontro või müügireskontrod määratletakse **Kinnipeetava maksu koodide** lehel.</span><span class="sxs-lookup"><span data-stu-id="f8865-128">The receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>
11. <span data-ttu-id="f8865-129">Valige **Sisestatud kinnipeetav maks**, et avada **Kinnipeetava maksu kannete** leht.</span><span class="sxs-lookup"><span data-stu-id="f8865-129">Select **Posted withholding tax** to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="f8865-130">Väljal **Väärtus** kuvatakse kande TDS-i arvutamiseks kasutatav koguprotsent.</span><span class="sxs-lookup"><span data-stu-id="f8865-130">The **Value** field shows the total percentage that was used to calculate TDS for the transaction.</span></span>

    <span data-ttu-id="f8865-131">Vahekaartide **Ülevaade** **Üldine** ja **Summa** väljadel kuvatakse arveridadel arvutatud TDS-summad.</span><span class="sxs-lookup"><span data-stu-id="f8865-131">The fields on the **Overview**, **General**, and **Amount** tabs show the TDS amounts that were calculated on the invoice lines.</span></span>

12. <span data-ttu-id="f8865-132">Vaadake TDS-i kalkulatsiooniteavet iga TDS-grupiga seotud TDS-i maksukoodi kohta.</span><span class="sxs-lookup"><span data-stu-id="f8865-132">Review the TDS calculation information for each TDS tax code that is attached to the TDS group.</span></span>
