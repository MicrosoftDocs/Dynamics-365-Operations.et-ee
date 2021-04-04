---
title: Arhiivi prinditud kliendi arved räsinumbritega
description: See teema kirjeldab, kuidas lubada arhiveerimine, et talletada prinditud kliendiarved koos räsinumbritega.
author: ilyako
manager: AnnBe
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d502ec5d286573c72e207419b66f283183009c09
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557476"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a><span data-ttu-id="8c04f-103">Arhiivi prinditud kliendi arved räsinumbritega</span><span class="sxs-lookup"><span data-stu-id="8c04f-103">Archive printed customer invoices with hash numbers</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="8c04f-104">Mõnedes riikides on juriidiline nõue talletada süsteemis arvutatud räsinumbrid koos mõne dokumendi väljaprintiga.</span><span class="sxs-lookup"><span data-stu-id="8c04f-104">In some countries, there is a legal requirement to store calculated hash numbers in the system together with printouts of some documents.</span></span> <span data-ttu-id="8c04f-105">Räsinumbreid saab kasutada ametivõimudele aruandluseks ja auditi ajal.</span><span class="sxs-lookup"><span data-stu-id="8c04f-105">Hash numbers can be used for reporting to authorities and during audits.</span></span>

<span data-ttu-id="8c04f-106">See teema kirjeldab, kuidas lubada arhiveerimine, et talletada prinditud kliendiarved koos räsinumbritega.</span><span class="sxs-lookup"><span data-stu-id="8c04f-106">This topic explains how to configure archiving in order to store printed customer invoices with hash numbers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8c04f-107">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="8c04f-107">Prerequisites</span></span>

- <span data-ttu-id="8c04f-108">**Funktsioonihalduse** tööruumis lülitage funktsioon sisse, **arhiveerige prinditud kliendiarved koos numbriga**.</span><span class="sxs-lookup"><span data-stu-id="8c04f-108">In the **Feature management** workspace, turn on the feature, **Archive printed customer invoices with hash numbers**.</span></span> <span data-ttu-id="8c04f-109">Lisateavet vt [Funktsioonihalduse ülevaatest](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8c04f-109">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="8c04f-110">**Prindihalduses** tuleb konfigureerida nõutud dokumentide prinditavad vormingud.</span><span class="sxs-lookup"><span data-stu-id="8c04f-110">Configure the printable formats of required documents in **Print management**.</span></span>

<span data-ttu-id="8c04f-111">See funktsioon on rakendatav järgmiste dokumentide puhul.</span><span class="sxs-lookup"><span data-stu-id="8c04f-111">This functionality is applicable to the following documents.</span></span>

<span data-ttu-id="8c04f-112">**Müügireskontro**</span><span class="sxs-lookup"><span data-stu-id="8c04f-112">**Accounts receivable**</span></span>
- <span data-ttu-id="8c04f-113">Kliendiarve</span><span class="sxs-lookup"><span data-stu-id="8c04f-113">Customer invoice</span></span>
- <span data-ttu-id="8c04f-114">Kliendi kreeditarve</span><span class="sxs-lookup"><span data-stu-id="8c04f-114">Customer credit note</span></span>
- <span data-ttu-id="8c04f-115">Vabas vormis arve</span><span class="sxs-lookup"><span data-stu-id="8c04f-115">Free text invoice</span></span>
- <span data-ttu-id="8c04f-116">Vabas vormis kreeditarve</span><span class="sxs-lookup"><span data-stu-id="8c04f-116">Free text credit note</span></span>

<span data-ttu-id="8c04f-117">**Projektihaldus ja -arvestus**</span><span class="sxs-lookup"><span data-stu-id="8c04f-117">**Project management and accounting**</span></span>
- <span data-ttu-id="8c04f-118">Projektiarve</span><span class="sxs-lookup"><span data-stu-id="8c04f-118">Project invoice</span></span>
- <span data-ttu-id="8c04f-119">Projekti kreeditarve</span><span class="sxs-lookup"><span data-stu-id="8c04f-119">Project credit note</span></span>

## <a name="configure-customer-master-data"></a><span data-ttu-id="8c04f-120">Kliendi koondandmete haldamine  </span><span class="sxs-lookup"><span data-stu-id="8c04f-120">Configure customer master data</span></span>
<span data-ttu-id="8c04f-121">Viige kliendi andmete konfigureerimiseks lõpule järgmised sammud ja lülitage sisse võimalus prinditud arved manustena automaatselt salvestada.</span><span class="sxs-lookup"><span data-stu-id="8c04f-121">Complete the following steps to configure customer data and turn on the ability to automatically save printed invoices as attachments.</span></span>

1. <span data-ttu-id="8c04f-122">Avage **Saadaolevad arved** > **Kõik kliendid**.</span><span class="sxs-lookup"><span data-stu-id="8c04f-122">Go to **Accounts receivable** > **All customers**.</span></span> 
2. <span data-ttu-id="8c04f-123">Valige klient ning valige **Arve ja kohaletoimetamine** kiirkaardil **E-arve**, jaotises **manus** valige **jah**.</span><span class="sxs-lookup"><span data-stu-id="8c04f-123">Select a customer, and on the **Invoice and delivery** FastTab, in the **E-INVOCE** section, in the **eInvoice attachment** field, select **Yes**.</span></span>

## <a name="print-invoices"></a><span data-ttu-id="8c04f-124">Prindi arve</span><span class="sxs-lookup"><span data-stu-id="8c04f-124">Print invoices</span></span>
<span data-ttu-id="8c04f-125">Saate eelmises protseduuris konfigureeritud kliendile sisestada ja printida vabas vormis, kliendi- ja projektiarve või kreeditarve.</span><span class="sxs-lookup"><span data-stu-id="8c04f-125">You can post and print any free text, customer, and project invoice or credit note for the customer configured in the previous procedure.</span></span>

<span data-ttu-id="8c04f-126">Saate avada **Manused** prinditud arve lehe.</span><span class="sxs-lookup"><span data-stu-id="8c04f-126">Open the **Attachments** page for the printed invoice.</span></span> <span data-ttu-id="8c04f-127">**Manused** kiirkaardil **Täiendavad üksikasjad** väljal **Dokumendi räsinumber**, leidke prinditud arve jaoks salvestatud räsinumber.</span><span class="sxs-lookup"><span data-stu-id="8c04f-127">On the **Attachment** FastTab, in the **Additional details** field group, in **Document hash number** field, find the stored hash number calculated for the printed invoice.</span></span>

![Manuse räsinumber](media/attach-hash-num.jpg)

