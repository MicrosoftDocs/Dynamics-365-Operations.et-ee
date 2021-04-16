---
title: Viited algsetele arvetele krediidiarvetes
description: Selles teemas kirjeldatakse, kuidas seadistada ja printida originaalarvete numbreid seotud kreeditarvetes.
author: ilkond
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ce06a0ce4f2a308e1917ac2c7cbc66f0494a2ec5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811506"
---
# <a name="references-to-original-invoices-in-credit-notes"></a><span data-ttu-id="f5383-103">Viited algsetele arvetele krediidiarvetes</span><span class="sxs-lookup"><span data-stu-id="f5383-103">References to original invoices in credit notes</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f5383-104">Mõnes riigis ja regioonis on juriidiline nõue, et prinditud kreeditarved sisaldavad viiteid originaalarvetele.</span><span class="sxs-lookup"><span data-stu-id="f5383-104">In some countries and regions, there is a legal requirement that printed credit notes include references to the original invoices.</span></span> <span data-ttu-id="f5383-105">Selles teemas kirjeldatakse, kuidas seadistada ja printida originaalarvete numbreid seotud kreeditarvetes.</span><span class="sxs-lookup"><span data-stu-id="f5383-105">This topic explains how to set up and print the original invoice numbers in related credit notes.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f5383-106">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="f5383-106">Prerequisites</span></span>

- <span data-ttu-id="f5383-107">Lülitage tööruumis **Funktsioonihaldus** sisse funktsioon **Kreeditarvete paigutus müügi ja projekti arvete aruandlusele**.</span><span class="sxs-lookup"><span data-stu-id="f5383-107">In the **Feature management** workspace, turn on the **Credit invoicing layout for sales and project invoice reports** feature.</span></span> <span data-ttu-id="f5383-108">Lisateavet vt [Funktsioonihalduse ülevaatest](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f5383-108">For more information, see [Feature management overview](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="f5383-109">Prindihalduses tuleb konfigureerida nõutud dokumentide prinditavad vormingud.</span><span class="sxs-lookup"><span data-stu-id="f5383-109">The printable formats of the required documents must be configured in Print management.</span></span>

<span data-ttu-id="f5383-110">Selles teemas kirjeldatud funktsionaalsus kehtib järgmiste dokumentide puhul.</span><span class="sxs-lookup"><span data-stu-id="f5383-110">The functionality that is described in this topic applies to the following documents:</span></span>

<span data-ttu-id="f5383-111">**Müügireskontro**</span><span class="sxs-lookup"><span data-stu-id="f5383-111">**Accounts receivable**</span></span>

- <span data-ttu-id="f5383-112">Vabas vormis kreeditarve</span><span class="sxs-lookup"><span data-stu-id="f5383-112">Free text credit note</span></span>
- <span data-ttu-id="f5383-113">Kliendi kreeditarve</span><span class="sxs-lookup"><span data-stu-id="f5383-113">Customer credit note</span></span>

<span data-ttu-id="f5383-114">**Projektihaldus ja -arvestus**</span><span class="sxs-lookup"><span data-stu-id="f5383-114">**Project management and accounting**</span></span>

- <span data-ttu-id="f5383-115">Projekti kreeditarve</span><span class="sxs-lookup"><span data-stu-id="f5383-115">Project credit note</span></span>

## <a name="configure-accounts-receivable-parameters"></a><span data-ttu-id="f5383-116">Müügireskontro parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="f5383-116">Configure Accounts receivable parameters</span></span>

<span data-ttu-id="f5383-117">Järgige neid samme, et seadistada parameeter, mis kontrollib, kas viited originaalarvetele prinditakse seotud kreeditarvetele.</span><span class="sxs-lookup"><span data-stu-id="f5383-117">Follow these steps to set the parameter that controls whether references to the original invoices are printed in related credit notes.</span></span>

1. <span data-ttu-id="f5383-118">Minge jaotisse **Müügireskontro** \> **Seadistus** \> **Müügireskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="f5383-118">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="f5383-119">Seadke vahekaardil **Värskendused** kiirkaardil **Arve** suvandi **Rakenda kreeditarve paigutus müügi ja projekti arvete aruannetele** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="f5383-119">On the **Updates** tab, on the **Invoice** FastTab, set the **Apply the credit invoicing layout into sales and project invoice reports** option to **Yes**.</span></span>

![Müügireskontro parameetrite konfigureerimine](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a><span data-ttu-id="f5383-121">Viidete määratlemine originaalarvetele</span><span class="sxs-lookup"><span data-stu-id="f5383-121">Define references to original invoices</span></span>

<span data-ttu-id="f5383-122">Dokumenditüübil põhinevate algsete arvete viidete määratlemiseks kasutage järgmisi protseduure.</span><span class="sxs-lookup"><span data-stu-id="f5383-122">Use the following procedures to define references to original invoices, based on the document type.</span></span>

### <a name="free-text-credit-note"></a><span data-ttu-id="f5383-123">Vabas vormis kreeditarve</span><span class="sxs-lookup"><span data-stu-id="f5383-123">Free text credit note</span></span>

1. <span data-ttu-id="f5383-124">Avage **Müügireskontro** \> **Arved** \> **Kõik vabas vormis arved**.</span><span class="sxs-lookup"><span data-stu-id="f5383-124">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="f5383-125">Looge uus kreeditarve või valige olemasolev kreeditarve.</span><span class="sxs-lookup"><span data-stu-id="f5383-125">Create a new credit note, or select an existing credit note.</span></span>
3. <span data-ttu-id="f5383-126">Avage arve.</span><span class="sxs-lookup"><span data-stu-id="f5383-126">Open the invoice.</span></span>
4. <span data-ttu-id="f5383-127">Valige toimingupaani vahekaardil **Arve** grupis **Funktsioonid** suvand **Krediitarveldus**.</span><span class="sxs-lookup"><span data-stu-id="f5383-127">On the Action Pane, on the **Invoice** tab, in the **Functions** group, select **Credit invoicing**.</span></span>
5. <span data-ttu-id="f5383-128">Sisestage viide algsele arvele ja valige paranduse põhjus.</span><span class="sxs-lookup"><span data-stu-id="f5383-128">Enter the reference to the original invoice, and select the reason for the correction.</span></span>

![Vabas vormis arve viite määratlemine](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a><span data-ttu-id="f5383-130">Kliendi kreeditarve</span><span class="sxs-lookup"><span data-stu-id="f5383-130">Customer credit note</span></span>

1. <span data-ttu-id="f5383-131">Avage **Müügireskontro** \> **Tellimused** \> **Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="f5383-131">Go to **Accounts receivable** \> **Orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="f5383-132">Valige ja avage arveldatud müügitellimus, mida tuleb parandada.</span><span class="sxs-lookup"><span data-stu-id="f5383-132">Select and open the invoiced sales order that must be corrected.</span></span>
3. <span data-ttu-id="f5383-133">Valige toimingupaani vahekaardil **Müük** grupis **Kreeditarve** suvand **Kreeditarve**.</span><span class="sxs-lookup"><span data-stu-id="f5383-133">On the Action Pane, on the **Sell** tab, in the **Credit note** group, select **Credit note**.</span></span>
4. <span data-ttu-id="f5383-134">Sisestage paranduse põhjus.</span><span class="sxs-lookup"><span data-stu-id="f5383-134">Enter the reason for the correction.</span></span> <span data-ttu-id="f5383-135">Viide algsele arvele luuakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="f5383-135">The reference to the original invoice is automatically established.</span></span>

![Müügitellimuse viite määratlemine](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a><span data-ttu-id="f5383-137">Projekti kreeditarve</span><span class="sxs-lookup"><span data-stu-id="f5383-137">Project credit note</span></span>

1. <span data-ttu-id="f5383-138">Avage **Projektihaldus ja raamatupidamine** \> **Projektiarved** \> **Projektiarved**.</span><span class="sxs-lookup"><span data-stu-id="f5383-138">Go to **Project management and accounting** \> **Project invoices** \> **Project invoices**.</span></span>
2. <span data-ttu-id="f5383-139">Valige ja avage arveldatud projektiarve, mida tuleb parandada.</span><span class="sxs-lookup"><span data-stu-id="f5383-139">Select and open the project invoice that must be corrected.</span></span>
3. <span data-ttu-id="f5383-140">Valige toimingupaani vahekaardil **Projektiarve** grupis **Funktsioonid** suvand **Vali kreeditarve jaoks**.</span><span class="sxs-lookup"><span data-stu-id="f5383-140">On the Action Pane, on the **Project invoice** tab, in the **Functions** group, select **Select for credit note**.</span></span>
4. <span data-ttu-id="f5383-141">Valige **Kreeditarveldus**.</span><span class="sxs-lookup"><span data-stu-id="f5383-141">Select **Credit invoicing**.</span></span>
5. <span data-ttu-id="f5383-142">Sisestage paranduse põhjus.</span><span class="sxs-lookup"><span data-stu-id="f5383-142">Enter the reason for the correction.</span></span> <span data-ttu-id="f5383-143">Viide algsele arvele luuakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="f5383-143">The reference to the original invoice is automatically established.</span></span>

![Projekti arve viite määratlemine](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a><span data-ttu-id="f5383-145">Kreeditarvete printimine</span><span class="sxs-lookup"><span data-stu-id="f5383-145">Printing credit notes</span></span>

<span data-ttu-id="f5383-146">Kui prindite vaba teksti, kliendi ja projekti kreeditarved, sisaldavad need viidet originaalarvele ja paranduse põhjust.</span><span class="sxs-lookup"><span data-stu-id="f5383-146">When you print free text, customer, and project credit notes, they will include the reference to the original invoice and the correction reason.</span></span>

![Prinditud kreeditarve](media/credit-note-FTI.jpg)

> [!NOTE]
> <span data-ttu-id="f5383-148">Veenduge, et dokumentide prinditavad vormingud on õigesti konfigureeritud, eeldusel, et prinditakse viited originaalarvetele.</span><span class="sxs-lookup"><span data-stu-id="f5383-148">Make sure that the printable formats of the documents are correctly configured, on the assumption that references to original invoices will be printed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
